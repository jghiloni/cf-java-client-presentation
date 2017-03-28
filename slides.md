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
public List<Integer> squaredIntegers(Integer... ints) {
	return Arrays.stream(ints).map((i) -> i * i).collect(Collectors.toList());
}
```

```
public List<Integer> positiveIntegers(Integer... ints) {
	return Arrays.stream(ints).filter((i) -> i > 0).collect(Collectors.toList());
}
```

---

# Introduction to Project Reactor

--

## Introduction to Project Reactor

* Non-blocking API
* Compatible with Standard Java Features
* Typed sequences
	* `Publisher` - Reactive Standard (used for 0 .. *N* items)
		* `Mono` - Used for 0 .. 1 items
		* `Flux` - Used for *N* items

---

## Interacting with the Cloud Foundry API

Two global components:
* `ConnectionContext` - Info about foundation
* `TokenProvider` - Authentication information

--

## Interacting with the Cloud Foundry API

Client interface:
* `ConnectionContext` - Info about foundation
* `TokenProvider` - Authentication information
* `UaaClient` - Work with the Cloud Foundry UAA

--

## Interacting with the Cloud Foundry API

### Demo!

--

## Interacting with the Cloud Foundry API

Client interface:
* `ConnectionContext` - Info about foundation
* `TokenProvider` - Authentication information
* `UaaClient` - Work with the Cloud Foundry UAA
* `CloudFoundryClient` - Work with the Cloud Foundry REST API

--

## Interacting with the Cloud Foundry API

### Demo!

--

## Interacting with the Cloud Foundry API

Client interface:
* `ConnectionContext` - Info about foundation
* `TokenProvider` - Authentication information
* `UaaClient` - Work with the Cloud Foundry UAA
* `CloudFoundryClient` - Work with the Cloud Foundry REST API
* `DopplerClient` - Work with the Cloud Foundry Firehose

--

## Interacting with the Cloud Foundry API

### Demo!

---

# Thanks!

## Any questions?
