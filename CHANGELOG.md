<h2 class="github">Changelog</h2>

This list is not intended to be all-encompassing - it will document major and breaking API changes with their rationale
when appropriate:

### v2.19.0.0
- **all** : Upgrade of dependencies including Kotlin to v2.0.10, and gradle to 8.9
- **result4k-strikt** : [New module] Assertions for Strikt. H/T @potfur

### v2.19.0.0
- **all** : Upgrade of dependencies including Kotlin to v2 and gradle.
- **result4k** : Add fold and bidimap functions

- **data4k** [Fix] Problem with deserialisation of numeric value types (due to int/long coercion by Jackson

### v2.18.0.1
- **data4k** [Fix] Problem with deserialisation of numeric value types (due to int/long coercion by Jackson

### v2.18.0.0
- **data4k** Make DataContainer contents mutable as chaining does not work otherwise.
- **data4k** Added updateWith() method to DataContainer to allow making a update of objects with an updated field

### v2.17.0.0
- **data4k** [Possible Break] DataContainers make a copy of their content data on construction. 
- **data4k** Added copy() method to DataContainer to allow making a copy of objects with an updated field

## v2.16.1.0
- **data4k** Finalise methods (should have been non-open)

### v2.16.0.1
- **data4k** Fix serialisation of booleans.

### v2.16.0.0
- **data4k** [Unlikely Break] : Better support for values4k tiny types - we use the correct representation as per the show method if there is a non-primitive datatype underneath the covers.

### v2.15.2.0
- **all** : Upgrade of dependencies and gradle. Convert build to kotlin.

### v2.15.1.0
- **data4k** : Rename methods for consistency. Old methods have been deprecated.

### v2.15.0.1
- **state4k** : Remove errant system out

### v2.15.0.0
- **all** : Upgrade of dependencies and gradle.
- **state4k** : [Breaking change] Migrated to new construction mechanic. We now define sent commands with `onEnter(commands)` and these are defined on the state itself. This allows for a more consistent way of defining state transitions.

### v2.14.1.0
- **result4k** : Add `resultFromCatching` to catch some (but not all!) exceptions and turn them into a `Result4k` H/T @MarcusDunn

### v2.14.0.0
- **all** : Upgrade of dependencies, including Kotlin to 1.9.23
- **data4k** : Add ability to declare child data-type fields (eg. JsonNode or submap) with data() and optionalData()
- **data4k** : [Breaking] Renamed content() to unwrap().

### v2.13.1.0
- **all** : Upgrade of dependencies
- **state4k** : [New module] Simple state machine modelling

### v2.13.0.0
- **data4k** : Tidying up of Metadatum interfaces

### v2.12.4.0
- **data4k** : Support for Property metadata being stored against properties

### v2.12.3.1
- **data4k** : Fix conversion of BigIntegers to int/long/bigdecimal

### v2.12.3.0
- **all** : Upgrade of dependencies
- **values4k** : Add CharValueFactory

### v2.12.2.0
- **data4k** : Add missing node types

### v2.12.1.1
- **data4k** : Fix problem with Jackson not replacing node

### v2.12.1.0
- **data4k** : Encapsulate data in `content()` function.

### v2.11.1.0
- **data4k** : Add support for Value classes and removed inner class structures to tidy up.

### v2.11.0.0
- **data4k** : [New module] [data4k](https://github.com/fork-handles/forkhandles/blob/trunk/data4k/README.md): Typesafe data-oriented programming.

### v2.10.1.0
- **all** : Upgrade of dependencies
- **values4k** : Added extension functions

### v2.10.0.0
- **all** : Upgrade of dependencies, including Kotlin to 1.9.20
- **values4k** : [Fix] InstantValue now uses format

### v2.9.0.0
- **values4k** : InstantValue value can now take a format

### v2.8.0.0
- **mock4k** : Rename mode argument.
- **result4k-kotest** : Made `shouldBeSuccess()` return value and `shouldBeFailure()` return reason.

### v2.7.1.0
- **mock4k** : mock4k: Added relaxed and strict modes (pass these to `mock(MockMode.Relaxed)`)

### v2.7.0.0
- **all** : Upgrade of dependencies
- **mock4k** : [New module] [mock4k](https://github.com/fork-handles/forkhandles/blob/trunk/mock4k/README.md): The very cheapest mocking framework platform.

### v2.6.0.0
- **all** : Upgrade of dependencies
- **fabrikate4k** : [Breaking] Changes to API to allow for recursive scenarios. See readme for details.

### v2.5.0.0
- **all** : Upgrade of dependencies, including Kotlin to 1.8.21 and Gradle to 8.1.1
- **values4k** : [Fix] Bug in Maskers.substring and added Maskers.reveal
- **values4k** : Add base 16, 32, 36, and 64 value factories H/T @oharaandrew314

### v2.4.0.0
- **all** : Upgrade of dependencies, including Kotlin to 1.8.10 and Gradle to 8.0.2
- **result4k-kotest** : Added Kotest matchers for result4k
- **result4k-hamkrest** : Added HamKrest matchers for result4k

### v2.3.0.0
- **all** : Upgrade of dependencies, including Kotlin to 1.7.20

### v2.2.0.0
- **all** : [Unlikely break] Remove dependency on kotlin stdlib JDK 8 as we don't need it to compile. If this causes a
  problem, simply re-add `api(Kotlin.stdlib.jdk8)` to your project dependency list.
- **all-*** : Fix provided dependencies included as runtime.

### v2.1.2.0
- **values4k** : Open up `of()` and `parse()` so that custom implementations can be supplied.

### v2.1.1.0
- **values4k** : [Fix] Accidental removal of `InstantValue` typealias.

### v2.1.0.0
- **values4k** : [Possible break] More utility methods for construction. Moved to extension functions so may require
  import.

### v2.0.1.0
- **all** : Upgrade of dependencies, including Kotlin to 1.6.20
- **values4k** : Adding utility methods to get `ZERO` and `random()` values

### v2.0.0.0
- **all** : Upgrade of dependencies, including Kotlin to 1.6.10
- **all** : Removal of deprecated methods.
- **values4k** : [Breaking] Deprecation of ValueFactory `invoke()` method. This enforces the usage of the of() method which will NOT bypass the validation.

### v1.14.0.1
- **time4k** : [Breaking] Merge DeterministicScheduler and TaskScheduler. One is a drop-in replacement for the other. H/T @time4tea

### v1.13.0.0
- **time4k** : Added TaskScheduler classes.

### v1.12.2.0
- **all** : Downgrade to Java 8 target - as not needed really.

### v1.12.1.0
- **all** : Upgrade to Java 11 target, gradle to v7.

### v1.12.0.0
- **all** : Upgrade of dependencies, including Kotlin to 1.6.0

### v1.11.2.1
- **fabrikate4k** : Revert change to provide more info on InstanceFabrikator as was blowing up on first try.

### v1.11.2.0
- **fabrikate4k** : Provide more information when InstanceFabricator cannot create an instance H/T @huanlui
- **fabrikate4k** : Fix Random generation of UUIDs so it is deterministic

### v1.11.1.0
- **all** : Upgrade of dependencies
- **fabrikate4k** Make Nullable creation behaviour configurable. H/T @huanlui
- **fabrikate4k** Fix #26 - added Boolean fabricator.

### v1.11.0.0
- **all** : Upgrade of dependencies, including Kotlin to 1.5.30.

### v1.10.3.0
- **fabrikate4k** Allow registered Fabricators to override defaults. H/T @LeoJohannsson-imtf

### v1.10.2.0
- **fabrikate4k** Use deprecated hidden constructors as last option only. H/T @saibot
- **all** : Upgrade of dependencies, including Kotlin to 1.5.21.

### v1.10.1.0
- **tuples4k** : support the `in` and `!in` operators for tuples with all elements of the same type
- **values4k** : interface and abstract base class for comparable values
- **values4k** : ValueFactory implements (PRIMITIVE)->DOMAIN

### v1.10.0.0
- **values4k** : Added support for Kotlin Result type using naming of style.. `ofResult()`
- **all** : Upgrade to Kotlin 1.5.0.

### v1.9.1.0
- **values4k** : Improved messages on error.

### v1.9.0.0
- **partial4k** : Reduce scope of functions to arity 5 with 3 placeholders. Massively reduces JAR size.

### v1.8.7.0
- **fabrikate4k** : Add random test data generator module. H/T @toastshaman
- **partial4k** : Add partial application module.
- **result4k** : Add convenience typealias for `Result4k` (to avoid clashes with Kotlin StdLib)

### v1.8.6.0
- **values4k** : Add unwrap() and fix validations.

### v1.8.5.0
- **values4k** : Add `NonBlankStringValueFactory`.

### v1.8.4.3
- release from MC

### v1.8.4.0
- **values4k** : Add `NonEmptyStringValueFactory`.

### v1.8.3.0
- **result4k** : Add flatZip(). h/t @razvn

### v1.8.2.0
- test release process (remove jcenter)

### v1.8.1.0
- **values4k** : [Deprecation]: Rename `print()` to `show()` as less confusing.

### v1.8.0.0
- **values4k** : [Breaking] Add proper support for inline classes through an interface. Rename `Value` to `AbstractValue`, reintroduce `Value` as an interface
- **values4k** : Add print() to value factory, so we have a nice symmetric interface for String <-> Value conversions.
- **values4k** : [Breaking] Undo-rename `of` to `invoke` for construction of values. This was considered to be a bad move.

### v1.7.0.0
- **values4k** : [Breaking] Rename `of` to `invoke` for construction of values.

### v1.3.0.0
- **values4k** : New module!

### v1.2.0.0 (and before)
- **forkhandles-bom** : Existing module!
- **bunting4k** : Existing module!
- **parser4k** : Existing module!
- **result4k** : Existing module!
- **time4k** : Existing module!
