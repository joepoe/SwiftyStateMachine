## [0.3.0][] • work in progress

- Updated to Swift 2.1 (Xcode 7.1).

- Made references to class-based subjects weak.  This helps to remove
  subject-machine reference cycles, but it also means you have to keep a
  strong reference to a subject somewhere else (which you usually already do).
  When subject references become `nil`, transitions are no longer performed.
  Thanks to @bartekchlebek for work on this issue! :clap:

- Added default `DOTLabel` implementation (`return "\(self)"`).  You don't
  have to change anything.  If you have custom `DOTLabel` implementations,
  you can keep using them, but if the only thing you do is `case Foo: return
  "Foo"`, you can safely delete this code.

- Renamed `StateMachine<T>` to `StateMachine<Schema>`.


## [0.2.0][] • 2015-06-06

- #2: Changed `StateMachine` into a class (was a struct).
- #5: Lowered the minimum deployment targets to iOS 8.0 and OS X 10.9.
- #6: Added support for CocoaPods.


## [0.1.0][] • 2015-04-29

Initial release.


  [0.3.0]: https://github.com/macoscope/SwiftyStateMachine/compare/0.2.0...0.3.0
  [0.2.0]: https://github.com/macoscope/SwiftyStateMachine/compare/0.1.0...0.2.0
  [0.1.0]: https://github.com/macoscope/SwiftyStateMachine/compare/928b1d1...0.1.0
