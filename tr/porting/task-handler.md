# Task Handler

To handle the tasks of LittlevGL you need to call `lv_task_handler()` periodically in one of the followings:
- *while(1)* of *main()* function 
- timer interrupt periodically (low priority then `lv_tick_inc()`)
- an OS task periodically

The timing is not critical but it should be about 5 milliseconds to keep the system responsive.

Example:
```c
while(1) {
  lv_task_handler();
  my_delay_ms(5);
}
```

To learn more about task visit the [Tasks](/overview/task) section.

