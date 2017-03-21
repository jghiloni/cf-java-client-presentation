## Cloud Foundry Java Client For Fun and Profit<sup>†</sup>

Josh Ghiloni

jghiloni@ecsteam.com

<img class="logo" src="/images/Twitter_Social_Icon_Blue.png" />@joshghiloni

<span style="font-size:16px;"><sup>†</sup>Fun and Profit Not Guaranteed</span>

---

## Agenda
1. What's new in Java 8?
1. Introduction to Project Reactor
1. Interacting with the UAA
1. Interacting with the Cloud Foundry API
1. Interacting with the Firehose

---

# What's New In Java 8?

--

## What's New In Java 8?

### (Completeable) Futures

```
public void doSomethingAsynchronously() {
	CompleteableFuture.supplyAsync(this::someReceiverMethod)
		.thenCompose(this::someOtherAsyncMethod)
		.thenApply(this::someBlockingMethod);
}
```

--

## What's New In Java 8?

### Functional Interfaces

```
public interface Function<T, R> {
	R apply(T input);
}
```

--

## What's New In Java 8?

### Streams

```
public <T> Stream<T> of(T... items) {
	return Arrays.stream(items);
}
```

--

## What's New In Java 8?

![And ... Omega Mu!](/images/lambda.jpg)

--

## What's New In Java 8?

### Lambdas

```
public <T> List<String> of(T... items) {
	Arrays.stream(items).map(t -> t.toString()).collect(Collectors.toList());
}
```

--

## What's New In Java 8?

### Lambdas

```
public <T> List<String> of(T... items) {
	Arrays.stream(items).map(Object::toString).collect(Collectors.toList());
}
```

---

# Introduction to Project Reactor

--

## Introduction to Project Reactor

* Non-blocking API
* Compatible with Standard Java Features
	* `Stream`
	* `CompleteableFuture`
* Typed sequences
	* `Publisher` - Reactive Standard (used for 0 .. *N* items)
		* `Mono` - Used for 0 .. 1 items
		* `Flux` - Used for *N* items

---

# Thanks!

## Any questions?
