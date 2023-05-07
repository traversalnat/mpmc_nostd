# mpmc_nostd
A Copy from std(crossbeam-channel crate), attempting to port mpmc to nostd environment

Zero is removed (because of Mutex).
Remove thread related functions.
An Instant implementation needs to be implemented in time.rs. Now Instant is just like follow:
```rust
#[derive(Copy, Clone, PartialEq, Eq, PartialOrd, Ord, Hash)]
pub struct Instant(u64);

impl Instant {
    pub fn now() -> Self {
        // TODO archive real Instant
        Self(0)
    }
}
```
