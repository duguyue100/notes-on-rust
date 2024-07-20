# Notes On Rust

I've been trying to learn Rust through [this tutorial](https://google.github.io/comprehensive-rust/).
I'm a beginner, and I'm getting familiar with syntax and so on. So far so good.

Here I documented some personal notes and opinions on Rust. Most of them are useless rants.
I think I should make the pretext clear: I've been using Python as my main programming language
for research and work for the past 10 years. So I'm deep in the Python rabbit hole.
I began my programming journey with Pascal, transit to Java in college, and learned C/C++ for
competitive programming.

So, there you go, here are my notes:

## println!

I'm not gonna say anything, I'm sure there are so many legit reasons behind it.

## Immutable variables

I'm not familiar with this concept, from Pascal to C to Java, I'm used to having mutable variables.
The fact that I have to do
```rust
let mut x: i32 = 20;
```
is weird.

## Built-in Types

I hate that `int8` is `i8` and `float32` is `f32`. What's wrong with spelling them out?
And why wouldn't `char` be `c` and `bool` be `b`?

## Loop

I'm glad they implemented the `do-while` loop. But let's face it, no one is gonna use this.

Has anyone realized how ugly this is?
```rust
for i in 1..=n
```

## Labels

I'm not sure how good or bad this is. Certainly, this is not something I've seen. (The code is copied from the tutorial)
```rust
fn main() {
    let s = [[5, 6, 7], [8, 9, 10], [21, 15, 32]];
    let mut elements_searched = 0;
    let target_value = 10;
    'outer: for i in 0..=2 {
        for j in 0..=2 {
            elements_searched += 1;
            if s[i][j] == target_value {
                break 'outer;
            }
        }
    }
    print!("elements searched: {elements_searched}");
}
```

## Macros

From the tutorial alone, there are useful macros such as `todo!`, `assert_eq!` that I like.

## Arrays and Tuples

I don't like how Rust defines arrays.

```rust
let mut a: [i8; 10] = [42; 10];
```

Equally, I don't understand why an array element can be accessed via indices `a[i]`, but
a tuple needs to use `a.0`. Maybe I haven't read enough. What if I want to do `a.i`, can I do it?

## References

The concept of "borrowing" is a really important concept. I like how this is done.
But I certainly need more practice and project experience to master it.
So I just leave the [link](https://google.github.io/comprehensive-rust/references.html) to this
chapter here.

## println! round 2

```rust
    let mut a: [i32; 6] = [10, 20, 30, 40, 50, 60];
    println!("a: {a:?}");
```
How does this make sense to anyone?

