# scheduler
The function of scheduling and monitoring program execution.

# example
<pre><code>
package main

import (
	"fmt"
	"runtime"
	"time"
	"github.com/hippper/scheduler"
)

func main() {
	job := func() {
		t := time.Now()
		fmt.Println("Time's up! @", t.UTC())
	}
	
	// run job every 2 seconds
	scheduler.Every(2).Seconds().NotImmediately().Run(job)
	
    runtime.Goexit()
}
</code></pre>

