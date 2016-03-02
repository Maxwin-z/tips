
```
// In UINavigationController's subclass
if ([self respondsToSelector:@selector(_cachedInteractionController)]
   && self._cachedInteractionController
   && [self._cachedInteractionController respondsToSelector:@selector(handleNavigationTransition:)]
   ) {
   UIPanGestureRecognizer *pan = [[UIPanGestureRecognizer alloc] initWithTarget:self._cachedInteractionController action:@selector(handleNavigationTransition:)];
   [self.view addGestureRecognizer:pan];
}
```

Reference: http://liudanyun.com/blog/?p=452

