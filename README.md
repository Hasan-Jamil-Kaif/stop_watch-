# stop_watch-
Author -kaif 
vecho "# stop-watch-" >> README.md
//c program to desine a digital clock
#include <stdio.h>
#include <time.h> 
// for sleep ()function
#include <unistd.h>
#include <stdlib.h>
int main (){
int hour ,minute ,second;
hour =minute =second =0;
while (1)
{
//CLEAR OUTPUT SCREEN
system ("clear");
//print time in HH:MM:SS formet
 printf("%02d :%02d :%02d", hour ,minute,second);

 //clear output buffer in gcc
 fflush (stdout) ;
 //increase second
 second ++ ;
 // update hour ,minute and second
 if (second==60){
minute +=1;
second=0;
 }
if(minute ==60){
    hour +=1;
    minute =0;
}
if(hour ==24){
    hour =0;
    minute =0;
    second =0;
}
sleep (1);//wait till 1 second 
}
}
