# LEIN-JUNIT [![Build Status](https://travis-ci.org/febeling/lein-junit.png)](https://travis-ci.org/febeling/lein-junit)

A Leiningen plugin that runs Java tests via JUnit.

## Installation

Via Clojars: http://clojars.org/lein-junit

## Example Configuration

    (defproject sample-project "0.0.1-SNAPSHOT"
      :min-lein-version "2.0.0"
      :dependencies [[org.clojure/clojure "1.6.0"]]
      :profiles {:dev {:dependencies [[junit/junit "4.11"]]}}
      :plugins [[lein-junit "1.1.8"]]
      :source-paths ["src/clojure"]
      :java-source-paths ["src/java" "test/java"]
      :junit ["test/java"]
      :jvm-opts ["-XX:MaxPermSize=128m"])

## Usage

Run all junit tests.

    lein junit

Run all junit tests matching a pattern.

    lein junit com.example

## License

Copyright (C) 2013-2015 Florian Ebeling, Roman Scherer

Distributed under the Eclipse Public License, the same as Clojure.
