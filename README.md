### TIM1

Configured as the Master timer by "triggering" a timer event on the `TRGO` line when it overflows
```
sMasterConfig.MasterOutputTrigger = TIM_TRGO_UPDATE;
sMasterConfig.MasterSlaveMode = TIM_MASTERSLAVEMODE_ENABLE
```

### TIM2

Configured in Slave mode via `TIM_SLAVEMODE_EXTERNAL1`, by listening for events on the `ITR0` trigger source.


### Interupts

Interupts are configured for `TIM1` via the following HAL functions:
- `HAL_NVIC_SetPriority`
- `HAL_NVIC_EnableIRQ`
- `HAL_TIM_IRQHandler`