Title: This Week in Rust 316
Number: 316
Date: 2019-12-10
Category: This Week in Rust

Hello and welcome to another issue of *This Week in Rust*!
[Rust](http://rust-lang.org) is a systems language pursuing the trifecta: safety, concurrency, and speed.
This is a weekly summary of its progress and community.
Want something mentioned? Tweet us at [@ThisWeekInRust](https://twitter.com/ThisWeekInRust) or [send us a pull request](https://github.com/cmr/this-week-in-rust).
Want to get involved? [We love contributions](https://github.com/rust-lang/rust/blob/master/CONTRIBUTING.md).

*This Week in Rust* is openly developed [on GitHub](https://github.com/cmr/this-week-in-rust).
If you find any errors in this week's issue, [please submit a PR](https://github.com/cmr/this-week-in-rust/pulls).

# Updates from Rust Community

## News & Blog Posts

* [A rusty radio: Si4703 FM radio receiver driver](https://blog.eldruin.com/si4703-fm-radio-receiver-driver-in-rust/)

### #Rust2020

Find all #Rust2020 posts at [Read Rust](https://readrust.net/rust-2020/).

# Crate of the Week

This week's crate is [StaticVec](https://github.com/slightlyoutofphase/staticvec), a nightly-only const-generics-backed fixed size vec crate.

Thanks to [ABagOfChips](https://users.rust-lang.org/t/crate-of-the-week/2704/682) for the suggestions!

[Submit your suggestions and votes for next week][submit_crate]!

[submit_crate]: https://users.rust-lang.org/t/crate-of-the-week/2704

# Call for Participation

Always wanted to contribute to open-source projects but didn't know where to start?
Every week we highlight some tasks from the Rust community for you to pick and get started!

Some of these tasks may also have mentors available, visit the task page for more information.

* [heed: Support windows and make the tests pass](https://github.com/Kerollmops/heed/pull/25). Heed is a fully typed LMDB wrapper with minimum overhead.
* [crates.io: carols10cents will be mentoring multiple issues for the month of November & December](https://github.com/rust-lang/crates.io/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc+label%3AE-mentor).

If you are a Rust project owner and are looking for contributors, please submit tasks [here][guidelines].

[guidelines]: https://users.rust-lang.org/t/twir-call-for-participation/4821

# Updates from Rust Core

247 pull requests were [merged in the last week][merged]

[merged]: https://github.com/search?q=is%3Apr+org%3Arust-lang+is%3Amerged+merged%3A2019-12-02..2019-12-09

* [implement `#[track_caller]` attribute](https://github.com/rust-lang/rust/pull/65881) (RFC #[2091](https://rust-lang.github.io/rfcs/2091-inline-semantic.html))
* [syntax: unify macro and attribute arguments in AST](https://github.com/rust-lang/rust/pull/66935)
* [stdarch: add CRC32 detection to arm32](https://github.com/rust-lang/stdarch/pull/830)
* [fix `TypedArena` returning wrong pointers for recursive allocations](https://github.com/rust-lang/rust/pull/67003)
* [make `ForeignItem` an alias of `Item`](https://github.com/rust-lang/rust/pull/67114)
* [remove boxed closures in address parser](https://github.com/rust-lang/rust/pull/67085)
* [rustc: hide HirId's fmt::Debug output from -Z span_free_formats](https://github.com/rust-lang/rust/pull/66850)
* [make `process_obligations()` greedier](https://github.com/rust-lang/rust/pull/66408)
* [check break target availability when checking breaks with values](https://github.com/rust-lang/rust/pull/66863)
* [include a span in more `expected...found` notes](https://github.com/rust-lang/rust/pull/67011)
* [do not ICE on async fn with non-Copy inferred type arg](https://github.com/rust-lang/rust/pull/67004)
* [make try_mark_previous_green aware of cycles](https://github.com/rust-lang/rust/pull/66846)
* [add feature gate for mut refs in const fn](Add feature gate for mut refs in const fn)
* [change unused_labels from allow to warn](https://github.com/rust-lang/rust/pull/66325)
* [show the sign for signed ops on `exact_div`](https://github.com/rust-lang/rust/pull/66148)
* [chalk: convert ensure_answer_recursively to be iterative instead of recursive](https://github.com/rust-lang/chalk/pull/281)
* [handle diverging functions forwarding their return place](https://github.com/rust-lang/rust/pull/66827)
* [cleanup `BodyCache`](https://github.com/rust-lang/rust/pull/66991)
* [remove hack for top-level or-patterns in match checking](https://github.com/rust-lang/rust/pull/66967)
* [const-prop: fix ICE calculating enum discriminant](https://github.com/rust-lang/rust/pull/66960)
* [miri: tweak and use `OsStr` interfaces](https://github.com/rust-lang/miri/pull/1099)
* [only memoize const fn calls during const eval](https://github.com/rust-lang/rust/pull/66866)
* [miri: add flag to ignore memory leaks](https://github.com/rust-lang/miri/pull/1106)
* [better way to ignore tests in miri](https://github.com/rust-lang/miri/pull/1105)
* [codegen "unreachable" for invalid `SetDiscriminant`](https://github.com/rust-lang/rust/pull/67054)
* [codegen: Migrate to `LLVM`{`Get`, `Set`}`ValueName2`](https://github.com/rust-lang/rust/pull/67033)
* [update the minimum external LLVM to 7](https://github.com/rust-lang/rust/pull/66973)
* [implement illegal subset relations errors using Polonius](https://github.com/rust-lang/rust/pull/67016)
* [add `ExitStatusExt` into prelude](https://github.com/rust-lang/rust/pull/67041)
* [rename `bool::then_*` to `bool::to_option_*` and use where appropriate](https://github.com/rust-lang/rust/pull/65195)
* [add `{f32,f64}::approx_unchecked_to<Int>` unsafe methods](https://github.com/rust-lang/rust/pull/66841)
* [add test for `NAME` environment variable when `cargo new`](https://github.com/rust-lang/cargo/pull/7667)
* [cargo: remove `--offline` empty index error](https://github.com/rust-lang/cargo/pull/7655)
* [cargo: add a `--offline` hint](https://github.com/rust-lang/cargo/pull/7654)
* [rustdoc: less minification](https://github.com/rust-lang/rust/pull/66828)
* [rustfmt: switch to non-recursive mode by default](https://github.com/rust-lang/rustfmt/pull/3938)
* [rustup: output the previous version of a toolchain when it is updated](https://github.com/rust-lang/rustup/pull/2143)
* [rustup: resolve potential future shock (x.yyy.zz)](https://github.com/rust-lang/rustup/pull/2132)
* [crates.io: add audit trail to the publish, yank and unyank transactions](https://github.com/rust-lang/crates.io/pull/1700)

## Approved RFCs

Changes to Rust follow the Rust [RFC (request for comments)
process](https://github.com/rust-lang/rfcs#rust-rfcs). These
are the RFCs that were approved for implementation this week:

*No RFCs were approved this week.*

## Final Comment Period

Every week [the team](https://www.rust-lang.org/team.html) announces the
'final comment period' for RFCs and key PRs which are reaching a
decision. Express your opinions now.

### [RFCs](https://github.com/rust-lang/rfcs/labels/final-comment-period)

*No RFCs are currently in final comment period.*

### [Tracking Issues & PRs](https://github.com/rust-lang/rust/labels/final-comment-period)

* [disposition: merge] [Add method Result::into_ok](https://github.com/rust-lang/rust/pull/66045).
* [disposition: merge] [From<NonZero*> impls for wider NonZero types](https://github.com/rust-lang/rust/pull/66277).
* [disposition: merge] [Change unused_labels from allow to warn](https://github.com/rust-lang/rust/pull/66325).

## New RFCs

* [process-handle-for-async](https://github.com/rust-lang/rfcs/pull/2823).

# Upcoming Events

### Europe

* [Dec 11. Hamburg, DE - Rust Hack & Learn December 2019](https://www.meetup.com/Rust-Meetup-Hamburg/events/266610252/).
* [Dec 11. Berlin, DE - OpenTechSchool Berlin - Rust Hack and Learn](https://www.meetup.com/opentechschool-berlin/events/nxdpgryzqbpb/).
* [Dec 12. Kyiv, UA - Rails Reactor - Rust Ukraine Meetup](https://www.facebook.com/events/1173477969528421/).
* [Dec 12. Turin, IT - Mozilla Torino - Gruppo di studio Rust](https://www.meetup.com/Mozilla-Torino/events/266750624).
* [Dec 16. Amsterdam, NL - Rust Nederland - Rust - Talks & Demos](https://www.meetup.com/Rust-Nederland/events/266888452/).
* [Dec 20. Stuttgart, DE - Meetup Stuttgart - Rust Hack and Learn](https://www.meetup.com/de-DE/Rust-Community-Stuttgart/events/267063341/).

### North America

* [Dec 10. Seattle, WA, US - Seattle Rust Meetup - Monthly meetup](https://www.meetup.com/Seattle-Rust-Meetup/events/prbtdryzqbnb/).
* [Dec 11. Mesa, AZ, US - Desert Rust - Rust: Crates and Organization](https://www.meetup.com/Desert-Rustaceans/events/wmmphryzpbkc/).
* [Dec 11. Vancouver, BC, CA - Vancouver Rust meetup](https://www.meetup.com/Vancouver-Rust/events/rwcpfryzqbpb/).
* [Dec 12. San Diego, CA, US - San Diego Rust December Meetup](https://www.meetup.com/San-Diego-Rust/events/266502136/).
* [Dec 12. Columbus, OH, US - Columbus Rust Society - Monthly Meeting](https://www.meetup.com/columbus-rs/events/dpkhgryzqbqb/).
* [Dec 12. Lehi, UT, US - Utah Rust - December 2019 Regular Meetup](https://www.meetup.com/utah-rust/events/265905262/).

If you are running a Rust event please add it to the [calendar] to get
it mentioned here. Please remember to add a link to the event too.
Email the [Rust Community Team][community] for access.

[calendar]: https://www.google.com/calendar/embed?src=apd9vmbc22egenmtu5l6c5jbfc%40group.calendar.google.com
[community]: mailto:community-team@rust-lang.org

# Rust Jobs

*Tweet us at [@ThisWeekInRust](https://twitter.com/ThisWeekInRust) to get your job offers listed here!*

# Quote of the Week

> So, in this regard and IMO, C++ has a saner model here. And if C++ is saner than you, that's not a good sign ☺

– [Boris Kolpackov on rust internals](https://internals.rust-lang.org/t/crate-dependency-discovery/11418/4)

Thanks to [UtherII](https://users.rust-lang.org/t/twir-quote-of-the-week/328/753) for the suggestion!

[Please submit quotes and vote for next week!](https://users.rust-lang.org/t/twir-quote-of-the-week/328)

*This Week in Rust is edited by: [nasa42](https://github.com/nasa42), [llogiq](https://github.com/llogiq), and [Flavsditz](https://github.com/Flavsditz).*

<small>[Discuss on r/rust]().</small>
