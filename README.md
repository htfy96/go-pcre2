# go-pcre2

This is a fork of github.com/Jemmic/go-pcre2 . The main differences are:

1. Removed all `runtime.setFinalizer` call. They cause major slowdowns under performance load. It's now user's responsibility to call `pattern.Free` or `match.Free`
2. Manage dependencies with go modules

[![GoDoc](https://godoc.org/github.com/htfy96/go-pcre2?status.svg)](https://godoc.org/github.com/htfy96/go-pcre2)

This is a Go language package providing support for version 2 of
Perl Compatible Regular Expressions (PCRE).

## Installation

Install the package for Debian as follows:

    sudo apt-get install libpcre2-dev
    go get github.com/Jemmic/go-pcre2

## Usage

Go programs that depend on this package should import
this package as follows to allow automatic downloading:

    import "github.com/Jemmic/go-pcre2"

## History

This is based on
[go-pcre](https://github.com/gijsbers/go-pcre) by [gijsbers](https://github.com/gijsbers)
and [go-pcre2](https://github.com/lestrrat/go-pcre2) by [lestrrat](https://github.com/lestrrat)
and [go-pcre2](github.com/Jemmic/go-pcre2) by [Jemmic](github.com/Jemmic)
