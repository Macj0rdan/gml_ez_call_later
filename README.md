# EZ Call Later

A wrapper for GameMaker’s `call_later`  
Tested on GM Runtime v2024.13.1.242

---

## Constructor

```gml
ez_call_later(callback, time_period, [unit=time_source_units_seconds], [loop=false])
```

* `callback` - function to call
* `time_period` - time until execution
* `unit` - `time_source_units_seconds` or `time_source_units_frames`
* `loop` - repeat (`true`) or one-shot (`false`)

---

## Methods

* `start()` - start the timer
* `stop()` - stop if running
* `restart([time_period])` - restart with optional new period
* `run_now_and_schedule()` - run once immediately, then schedule
* `set_callback(function)` - change callback
* `set_time_period(period)` - change delay
* `set_unit(unit)` - change unit
* `set_repeat(bool)` - change loop mode
* `is_running()` - returns whether active

---

## Examples

```gml
// Call once after 2 seconds
var once = new ez_call_later(some_function, 2);
once.start();

// Repeat every 60 frames
var looped = new ez_call_later(some_function, 60, time_source_units_frames, true);
looped.start();

// Restart with new delay
looped.restart(120);
```

