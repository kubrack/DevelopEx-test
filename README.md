# Overview
	DevelopEx test task.
	
# Installation
```
	git clone https://github.com/kubrack/DevelopEx-test.git
	make
```
# Testing
```
	make func-test
```
# Usage
```
	application:ensure_all_started(cache).
	cache:set(foo, bar).
	cache:set(foo, bar, [{ttl, 120}]).
	cache:set(foo, bar, [{ttl, infinity}]).
	cache:get(foo).
```
# API
```
	cache:get(Key :: term()) -> {ok, Val :: term()} | {error, not_found}.
	cache:set(Key :: term(), Val :: term()) -> ok.
	cache:set(Key :: term(), Val :: term(), Opts :: [{ttl, Seconds :: infinity | non_neg_integer()}]) -> ok.
```
# TODO
	- ct tests?

# Notes
	- Since Logger introduced in Erlang/OTP 21.0 so at least this version required.
