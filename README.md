#NSTimer-WeakTarget

A simple but powerful NSTimer category which adds the support of weak target for NSTimer.

##What is it?

With this NSTimer category. You will NEVER worry about NSTimer retain it's target.

*妈妈再也不担心我用NSTimer了*

##What's included?

Tree method. Turn target-action based NSTimer, to a weak target-action based NSTimer. NSTimer created with these methods will NOT retain it's target, and will automatically invalidate after the target is disposed.

```
@interface NSTimer (WeakTarget)

- (id)initWithFireDate:(NSDate *)date
              interval:(NSTimeInterval)timeInterval
            weakTarget:(id)target
              selector:(SEL)selector
              userInfo:(id)userInfo
               repeats:(BOOL)repeats;

+ (NSTimer *)timerWithTimeInterval:(NSTimeInterval)timeInterval
                        weakTarget:(id)target
                          selector:(SEL)selector
                          userInfo:(id)userInfo
                           repeats:(BOOL)repeats;

+ (NSTimer *)scheduledTimerWithTimeInterval:(NSTimeInterval)timeInterval
                                 weakTarget:(id)target
                                   selector:(SEL)selector
                                   userInfo:(id)userInfo
                                    repeats:(BOOL)repeats;

@end
```
##Requirements

- Automatic Reference Counting (ARC)
- iOS 5.0+
- Xcode 4.5+

##Contributing

If you find a bug and know exactly how to fix it, please open a pull request.

If you can't make the change yourself, please open an issue after making sure that one isn't already logged.

##License

The MIT license, as aways.