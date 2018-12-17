---
layout: post
title:  "About Completion Handler"
date:   2018-12-16 18:37:53 -0600
categories: jekyll update
---

# Completion Handler 
  - Do stuff when things have been done.
  - You are telling your boss that you are going home(stuff) only after you have finished working

## Introducing Completion Handler

**Example Code**
```
import UIKit

let firstVC = UIViewController() 
let nextVC = UIViewController() 

firstVC.present(nextVC, animation: true, completion: nil)
```
The **completion** parameter is asking to enter a closure block whose type is **()->()** or **()->Void**.

```
firstVC.present(nextVC, animation: true, completion: { () in 
  print('Done")
})
```
Here, print "Done" will be printed only after **firstVC** has moved to **nextVC**
Same code but using **Trailing Closure** 
```
firstVC.present(nextVC, animation: true) { () in 
  print("Done")
}
```

## Pass Data Through Completion Handler
  - **Most Important Part**. If you have used ```NSURL```, any type of API that you grab from **JSON/Data** from other platforms 
  
