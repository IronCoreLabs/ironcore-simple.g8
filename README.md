# scala-simple.g8
g8 template for basic sbt scala projects for a quick stand-up of best practices.

## Usage

Install g8 and then use the following command, which will ask a series of questions and then generate a new project directory for you:

    g8 ironcorelabs/scala-simple

## Linting

For linting, it includes:

* Scalariform
* Wartremover
* Scalastyle

Configuration taken from @leifwickland's lint skeleton and recommendations.

## Scalac Defaults

Strict defaults for the scala compiler to make warnings fatal and check for common issues like discarded errors.

## Frequently used libraries

Its easier to remove libraries added in the `build.sbt` template than to look up how to add them, so we start with a suite of scalaz, knobs, spire, scodec and shapeless, the tools of the trade of the scala functional programmer.

For testing we use scalatest, scalacheck and typelevel's scalaz test extensions for scalatest.

## Base test file

An example test file is put in place along with a base test class to make it turnkey to get going with common scalatest pieces in place.

## Documentation

A number of plugins and config are in place to make it easy to drop in documentation.  In particular, we use tut to test all tutorial code blocks by running them through scala and then capturing their output for the repo and the website.  We've also added plugins and a directory structure for producing a project website that includes any tutorials and uses github pages and jekyll to run.

## Publishing and CI

Work will need to be done to get publishing and CI going, but a basic configuration and setup including the necessary plugins are in place for using Travis for CI (and doing lint checks, testing the docuentation and running tests as part of that). The necessary plugins for publishing to sonatype and signing the jars with pgp are also in place.  Details on how to use these things are in the CONTRIBUTING.md file after you clone the template.

