##### 1. 請概述C語言的編譯流程。 #####

##### 2. 承上，請詳述全域變數(global)與局部(local)變數在編譯過程中的差異。 #####

##### 3. 堆疊框架(stack frame)的結構組成如下，請簡述其含義。 #####
> 1.	回傳位址(return address)
2.	區域資料儲存空間
3.	函數參數儲存空間
4.	堆疊框架指標(sp : stack pointer)

##### 4. 請舉例如何使用malloc函數，宣告的型態與記憶體配置有何相關？並簡述什麼情況下會產生記憶體洩漏？ #####
##### 5. 請解釋以下語法有何不同？ #####

```c
	int num = 5;
    int* const pi = &num ; 			
    const int* pi = &num ; 
```

##### 6.  #####
將多維陣列`matrix`傳入`display2DArray`函數，顯示每個元素的位址與數值。 

```c
void main()
{
	int matrix[2][5] = { {1,2,3,4,5}, {6,7,8,9,10} };
	
	display2DArray(matrix,2);
	
}

```
`display2DArray`函數內容實作。
	
```c
{
	int i = j = 0;
	for(i = 0; i < 2; i++)
	{
		for(j = 0; j < 5; j++)
		{
			printf("matrix[%1d][%1d] Address: %p Value: %1d\n", i, j, &matrix+j, matrix[i][j]);
		}
	}
}

```
請問以下哪一種函數介面宣告方式無法如預期動作？並解釋原因。
	
```c
void display2DArray(int arr[][5], int rows);
	
void display2DArray(int (*arr)[5], int rows);
	
void display2DArray(int *arr[5], int rows);

```
	
##### 7. 承上，若matrix位址為0x100，則`matrix+1`的位址為？  #####
##### 8. 請簡述以下`allocateArray`函數實作內容何者有誤？ #####

```c
#define size 5
int value = 45;
int* vector = allocateArray(value);
	...
free(vector);
```

```c
int* allocateArray(int v)
{
	int arr[size];
	int i = 0;
	for(i = 0; i < size; i++)
	{
		arr[i] = v;
	}
	
	return arr;
}
```

##### 9. 請使用switch case實作輸入一個任意`int` X ，可判斷其為偶數或奇數。 #####
##### 10. 請實作輸入一行字串，分別統計出其英文字母，空格，數字總個數。 #####
##### 11. 請使用資料結構實作老鼠走迷宮。 #####
##### 12. 請使用資料結構實作氣泡排序法。 #####




