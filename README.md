# UART-Interfacing-with-LPC2148
UART configuration with LPC 2148 which is ARM7 (TDMI) family Microcontroller.
Main.c
#include<global.h>
#include<lpc2148.h>
#include<pll0.h> 
#include<uart0.h>
#include<pconp.h>

void main()
{
	unsigned int A;
	Power_Off_Peripherals();
	Init_PLL0(); 
	Init_UART();
  //Set_UART0_Data('A'); 
	
	while(1)
	{
		 A = Get_UART0_data();
		Set_UART0_Data(A);
 }
