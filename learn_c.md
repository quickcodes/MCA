### Memory leak in c
'''
#include<stdio.h>
#include<stdlib.h>

void foo(){
	int *ptr;
	int val = 1000;
	ptr = &val;
	printf("The value is: %d", *ptr);
	// if we will not use free(ptr) the pointer will
	// still remain in memory even after foo is done
	// which can become a cause of memory leak
	// free(ptr);
}

int main(){
	foo();
	printf("function done");
	int val;
	scanf("%d", &val);
	return 0;
}
'''
