# flutter_timer

A sailing starting line timer

## Files
- ticker.dart: The ticker will be our data source for the timer application. It will expose a stream of ticks which we can subscribe and react to.
- timer_bloc.dart:
  - TimerInitial — ready to start counting down from the specified duration. 
    - if the state is TimerInitial the user will be able to start the timer.
  - TimerRunInProgress-actively counting down from the specified duration. 
    - if the state is TimerRunInProgress the user will be able to pause and reset the timer as well as see the remaining duration.
  - TimerRunPause-paused at some remaining duration. 
    - if the state is TimerRunPause the user will be able to resume the timer and reset the timer.
  - TimerRunComplete-completed with a remaining duration of 0.
    - if the state is TimerRunComplete the user will be able to reset the timer.