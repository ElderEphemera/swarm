# Revision history for swarm

## **0.4.0.0** - 2023-08-18

### Bugfixes
* Save completion time immediately upon finishing scenario by @xsebek
  ([#1118](https://github.com/swarm-game/swarm/pull/1118))
* Fix rightward bleeding of custom attributes by @kostmo ([#1137](https://github.com/swarm-game/swarm/pull/1137))
* Recreate `GameState` from scratch when starting a scenario by @byorgey ([#1277](https://github.com/swarm-game/swarm/pull/1277))
* Load persistent state from disk only once and reuse for all integration tests by @byorgey ([#1383](https://github.com/swarm-game/swarm/pull/1383))
* Continue parsing the rest of the scenarios in a directory when one fails by @byorgey ([#1391](https://github.com/swarm-game/swarm/pull/1391))
* Throw an error instead of crashing on impredicative types by @byorgey ([#1418](https://github.com/swarm-game/swarm/pull/1418))

### New Features

#### Tutorials
* Some tutorial improvements, and enforce in CI that commands and entities are introduced before they are required by @kostmo ([#1186](https://github.com/swarm-game/swarm/pull/1186))

#### Swarm language
* The `drill` command now returns the first inventory addition by @kostmo ([#1165](https://github.com/swarm-game/swarm/pull/1165))
* Type ascription syntax by @Alexander-Block ([#1164](https://github.com/swarm-game/swarm/pull/1164))
* Records and record types by @byorgey ([#1148](https://github.com/swarm-game/swarm/pull/1148))
* `requirements` command for viewing requirements of any expression by
  @byorgey ([#1183](https://github.com/swarm-game/swarm/pull/1183))
* `stride` command by @kostmo ([#1219](https://github.com/swarm-game/swarm/pull/1219))
* Many new robot sensing commands by @kostmo:
  * `detect` ([#1170](https://github.com/swarm-game/swarm/pull/1170))
  * `sniff` and `chirp` ([#1181](https://github.com/swarm-game/swarm/pull/1181))
  * `resonate` ([#1204](https://github.com/swarm-game/swarm/pull/1204))
  * `watch` and `surveil` ([#1201](https://github.com/swarm-game/swarm/pull/1201))
  * `scout` ([#1209](https://github.com/swarm-game/swarm/pull/1209))
* New key input handler framework by @byorgey, so you can program robots to
  respond to keypresses ([#1214](https://github.com/swarm-game/swarm/pull/1214))
* `instant` command (unrestricted variant of `atomic`) by @kostmo ([#1231](https://github.com/swarm-game/swarm/pull/1231))
* `push` command by @kostmo ([#1235](https://github.com/swarm-game/swarm/pull/1235))
* `density` command by @kostmo ([#1296](https://github.com/swarm-game/swarm/pull/1296))
* `use` command by @kostmo ([#1287](https://github.com/swarm-game/swarm/pull/1287))
* `halt` command by @byorgey ([#1256](https://github.com/swarm-game/swarm/pull/1256))
* `backup` command by @kostmo ([#1400](https://github.com/swarm-game/swarm/pull/1400))

#### Entities + recipes
* Make `sand` a bit harder to get by @byorgey ([#1024](https://github.com/swarm-game/swarm/pull/1024))
* New `tweezers` entity to enable debugging view and single-stepping CESK machine by @xsebek ([#1081](https://github.com/swarm-game/swarm/pull/1081))
* `ADT calculator` description now mentions `unit` and `void` types [#1226](https://github.com/swarm-game/swarm/pull/1226)
* Allow zero-tick recipes to apply immediately by @kostmo ([#1272](https://github.com/swarm-game/swarm/pull/1272))
* New `hourglass` device that provides relative (`wait`) but not absolute (`time`) capability by @kostmo ([#1261](https://github.com/swarm-game/swarm/pull/1261))
* New `binoculars` device that provides `scout` command by @kostmo ([#1337](https://github.com/swarm-game/swarm/pull/1337))
* Separate entities to provide each text operation by @kostmo ([#1339](https://github.com/swarm-game/swarm/pull/1339))

#### World features
* Structure templates by @kostmo ([#1332](https://github.com/swarm-game/swarm/pull/1332))
* Waypoints and portals by @kostmo ([#1356](https://github.com/swarm-game/swarm/pull/1356))
* Subworlds by @kostmo ([#1353](https://github.com/swarm-game/swarm/pull/1353))
* World description DSL by @byorgey ([#1376](https://github.com/swarm-game/swarm/pull/1376))

#### LSP improvements
* `let`-`in` syntax highlighting by @kostmo ([#1162](https://github.com/swarm-game/swarm/pull/1162))

#### Web API
* Web API to parse, render, and run code by @kostmo ([#1142](https://github.com/swarm-game/swarm/pull/1142))

#### Command line options
* CLI option to set initial speed by @kostmo ([#1255](https://github.com/swarm-game/swarm/pull/1255))

#### New scenarios
* Adventure game scenario by @kostmo ([#1136](https://github.com/swarm-game/swarm/pull/1136))
* Run around in circles by @kostmo ([#1158](https://github.com/swarm-game/swarm/pull/1158))
* hackman by @kostmo ([#1135](https://github.com/swarm-game/swarm/pull/1135))
* Whack-a-mole by @kostmo ([#1026](https://github.com/swarm-game/swarm/pull/1026))
* Additional tutorial level on `give` by @byorgey ([#1249](https://github.com/swarm-game/swarm/pull/1249))
* Lights out by @kostmo ([#1273](https://github.com/swarm-game/swarm/pull/1273))
* Pig capturing scenario by @kostmo ([#1258](https://github.com/swarm-game/swarm/pull/1258))
* Sokoban levels by @kostmo ([#1269](https://github.com/swarm-game/swarm/pull/1269))
* Traffic vignette by @kostmo ([#1334](https://github.com/swarm-game/swarm/pull/1334))
* Active trapdoor demo by @kostmo ([#976](https://github.com/swarm-game/swarm/pull/976))
* Sliding puzzle by @kostmo ([#1237](https://github.com/swarm-game/swarm/pull/1237))
* Scenario with enemies by @kostmo ([#971](https://github.com/swarm-game/swarm/pull/971))
* Arbitrage scenario by @kostmo ([#1192](https://github.com/swarm-game/swarm/pull/1192))
* Powerset scenario by @kostmo ([#1342](https://github.com/swarm-game/swarm/pull/1342))

#### UI enhancements
* Allow scrolling the world map unless explicitly disallowed by @byorgey ([#1109](https://github.com/swarm-game/swarm/pull/1109))
* Add random "static" to `view` outside a certain range by @byorgey ([#1110](https://github.com/swarm-game/swarm/pull/1110), [#1241](https://github.com/swarm-game/swarm/pull/1241))
* Display the scenario in which an achievement was obtained by @kostmo ([#1175](https://github.com/swarm-game/swarm/pull/1175))
* World editor prototype by @kostmo ([#873](https://github.com/swarm-game/swarm/pull/873))
* Scenario launch options selection by @kostmo ([#1010](https://github.com/swarm-game/swarm/pull/1010))
* Record best code size by @kostmo ([#974](https://github.com/swarm-game/swarm/pull/974))
* Inventory search/filter mode by @byorgey ([#1250](https://github.com/swarm-game/swarm/pull/1250))
* Display higher clock resolution at lower speeds by @kostmo ([#1253](https://github.com/swarm-game/swarm/pull/1253))
* Make REPL panel collapsible by @ussgarci ([#1076](https://github.com/swarm-game/swarm/pull/1076))
* Better typechecking error messages by @byorgey
  ([#1308](https://github.com/swarm-game/swarm/pull/1308), [#1318](https://github.com/swarm-game/swarm/pull/1318))
* Rename inventory to compendium by @kostmo ([#1346](https://github.com/swarm-game/swarm/pull/1346))
* Goal dialog suppression with `--autoplay` by @kostmo ([#1344](https://github.com/swarm-game/swarm/pull/1344))
* Change binding for Hide REPL to `M-,` by @noahyor ([#1375](https://github.com/swarm-game/swarm/pull/1375))
* Highlight ticks per frame in red when it reaches the cap by @byorgey ([#1386](https://github.com/swarm-game/swarm/pull/1386))
* Parse and render markdown descriptions by @xsebek ([#1106](https://github.com/swarm-game/swarm/pull/1106), [#1413](https://github.com/swarm-game/swarm/pull/1413))

#### Achievements

* Achievement for disorientation by @kostmo ([#1173](https://github.com/swarm-game/swarm/pull/1173))


## **0.3.0.1** - 2023-02-01

A few critical bug fixes and improvements:

* Make sure the base always has a `logger` installed in every tutorial level, by @byorgey in [#1067](https://github.com/swarm-game/swarm/pull/1067) and @xsebek in [#1073](https://github.com/swarm-game/swarm/pull/1073)
* Allow dialog boxes to scroll by @byorgey in [#1071](https://github.com/swarm-game/swarm/pull/1071)
* Fix bug that sometimes caused scenarios to be skipped or repeated by @byorgey in [#1065](https://github.com/swarm-game/swarm/pull/1065)

## **0.3.0.0** - 2023-01-30

This is the first release of 2023! It contains:
- various new features and bugfixes (see subsections below)
- UI tweaks
- fewer typos (thanks @bwignall and @kostmo)
- upgraded dependencies (`>=lsp-1.6` and `>=brick-1.5`) and raised Stack resolver to use GHC 9.4 [#1001](https://github.com/swarm-game/swarm/pull/1001)
- a ton of internal refactoring

### Fixed bugs
* copy parent robot context to child when executing `build` by @byorgey in [#817](https://github.com/swarm-game/swarm/pull/817)
* Merge new requirements context with existing when running from REPL by @byorgey in [#965](https://github.com/swarm-game/swarm/pull/965)
* Reset `lastFrameTime` when starting a new scenario by @byorgey in [#855](https://github.com/swarm-game/swarm/pull/855)
* Fix capability checking, and refactor/add lots of comments by @byorgey in [#959](https://github.com/swarm-game/swarm/pull/959)
* Fix `EntityMap` merging by @byorgey in [#962](https://github.com/swarm-game/swarm/pull/962)
* Fix: add first heard message to log by @xsebek in [#842](https://github.com/swarm-game/swarm/pull/842)
* Fix hypothetical result of condition by @xsebek in [#940](https://github.com/swarm-game/swarm/pull/940)
* One file per achievement record by @kostmo in [#954](https://github.com/swarm-game/swarm/pull/954)
* Show duplicate robot logs by @xsebek in [#1022](https://github.com/swarm-game/swarm/pull/1022)
* Copy requirements map to robot context when loading a new `ProcessedTerm` by @byorgey in [#827](https://github.com/swarm-game/swarm/pull/827)
* Set REPL to `Working` when base has `program` field specified by @byorgey in [#846](https://github.com/swarm-game/swarm/pull/846)
* Create swarm subdirectories as necessary by @xsebek in [#943](https://github.com/swarm-game/swarm/pull/943)

### New Features

#### Swarm language
* implement Equip/Unequip by @kostmo in [#887](https://github.com/swarm-game/swarm/pull/887)
  * The great `install`/`equip` switch by @byorgey in [#989](https://github.com/swarm-game/swarm/pull/989)
* Meeting other robots by @byorgey in [#920](https://github.com/swarm-game/swarm/pull/920)
* New `heading` command by @byorgey in [#955](https://github.com/swarm-game/swarm/pull/955)
* Add `isempty : cmd bool` to check whether current cell has an entity by @byorgey in [#968](https://github.com/swarm-game/swarm/pull/968)

#### Entities
* Add `GPS receiver` device to provide `senseloc` capability by @byorgey in [#956](https://github.com/swarm-game/swarm/pull/956)
* Device with recipe for 'appear' capability by @kostmo in [#1027](https://github.com/swarm-game/swarm/pull/1027)
* device for setname by @kostmo in [#1028](https://github.com/swarm-game/swarm/pull/1028)

#### LSP improvements
* swarm-lang IDE hover by @kostmo in [#972](https://github.com/swarm-game/swarm/pull/972)
* Include `SrcLoc` info with variable binding sites by @byorgey in [#993](https://github.com/swarm-game/swarm/pull/993)
* Annotate ASTs with types at every node by @byorgey in [#991](https://github.com/swarm-game/swarm/pull/991)
* Improve OnHover for Def/Let, App and Const by @xsebek in [#986](https://github.com/swarm-game/swarm/pull/986)
* warn of unused variables by @kostmo in [#983](https://github.com/swarm-game/swarm/pull/983)

#### Web API
* Expose REPL history via web interface by @kostmo in [#821](https://github.com/swarm-game/swarm/pull/821)

#### Command line options
* Add full color mode option by @xsebek in [#851](https://github.com/swarm-game/swarm/pull/851)

#### New scenarios
* New ranching scenario by @kostmo in [#835](https://github.com/swarm-game/swarm/pull/835)
* new bind tutorial by @kostmo in [#895](https://github.com/swarm-game/swarm/pull/895)
* A "bucket brigade" of robots by @kostmo in [#885](https://github.com/swarm-game/swarm/pull/885)
* Ice Cream Shop by @kostmo in [#1008](https://github.com/swarm-game/swarm/pull/1008)
* word search by @kostmo in [#999](https://github.com/swarm-game/swarm/pull/999)
* Wolf, Goat, Cabbage scenario by @kostmo in [#944](https://github.com/swarm-game/swarm/pull/944)
* swarm logo animation by @kostmo in [#1018](https://github.com/swarm-game/swarm/pull/1018)

#### Scenario development
* Boolean expressions of objective prerequisites by @kostmo in [#927](https://github.com/swarm-game/swarm/pull/927)
* support 'orientationMap' by @kostmo in [#1023](https://github.com/swarm-game/swarm/pull/1023)
* support custom attributes defined in scenarios by @kostmo in [#1058](https://github.com/swarm-game/swarm/pull/1058)

#### UI enhancements
* show devices that enable commands by @kostmo in [#899](https://github.com/swarm-game/swarm/pull/899)
* Add a "driving mode" to the REPL by @kostmo in [#819](https://github.com/swarm-game/swarm/pull/819)

#### Achievements
* achievements board by @kostmo in [#796](https://github.com/swarm-game/swarm/pull/796)
* first tutorial completion achievement by @kostmo in [#925](https://github.com/swarm-game/swarm/pull/925)
* Add achievement for losing by @kostmo in [#945](https://github.com/swarm-game/swarm/pull/945)

#### Debugging
* Better CESK machine pretty-printing by @byorgey in [#948](https://github.com/swarm-game/swarm/pull/948)
* Add the full expected location for the data directory by @TristanCacqueray in [#908](https://github.com/swarm-game/swarm/pull/908)
* Extend logs for warnings by @xsebek in [#982](https://github.com/swarm-game/swarm/pull/982)

## **0.2.0.0** - 2022-11-01

A bunch of small fixes and improvements; special thanks to new
contributors @0xcefaedfe, @kostmo, @ussgarci, and @valyagolev. Notable changes include:

- New UI features:
    - REPL improvements:
        - Expose the last evaluated result as `it`, and previous results
          as `itN` ([#734](https://github.com/swarm-game/swarm/pull/734))
        - Allow clicking in the REPL input to move the cursor
          ([#750](https://github.com/swarm-game/swarm/pull/750))
        - Autocomplete entity names in the repl ([#798](https://github.com/swarm-game/swarm/pull/798))
        - REPL cursor no longer blinks when REPL panel is not selected ([#801](https://github.com/swarm-game/swarm/pull/801))
    - Improve user experience around quitting & moving between
      tutorial challenges ([#754](https://github.com/swarm-game/swarm/pull/754))
        - Add a button to the Quit dialog to restart a
          scenario. ([#767](https://github.com/swarm-game/swarm/pull/767))
        - Use scenario name as Goal dialog title ([#774](https://github.com/swarm-game/swarm/pull/774))
    - `autoplay` flag for automatically demonstrating scenario
      solutions ([#792](https://github.com/swarm-game/swarm/pull/792))
    - Improved inventory sorting and user-controllable sort criteria ([#793](https://github.com/swarm-game/swarm/pull/793))
    - Ability to temporarily hide robots so you can see what's under
      them ([#802](https://github.com/swarm-game/swarm/pull/802))
- New language features:
    - New `void` type ([#735](https://github.com/swarm-game/swarm/pull/735))
- Bug fixes:
    - Fix bug in the first tutorial challenge that froze the game and
      ate all memory if the user said anything other than expected
      ([#762](https://github.com/swarm-game/swarm/pull/762), [#810](https://github.com/swarm-game/swarm/pull/810))
- Documentation:
    - Generate all wiki "cheat sheets" automatically ([#769](https://github.com/swarm-game/swarm/pull/769))
- Support for building on GHC 9.4 ([#752](https://github.com/swarm-game/swarm/pull/752))

There were several other small fixes and improvements; see the [full
changelog
here](https://github.com/swarm-game/swarm/compare/0.1.1.0...0.2.0.0).

## **0.1.1.0** - 2022-10-14

A couple new features and an important bugfix for the Hackage release.

- Update to `hsnoise-0.0.3`, fixing some world generation bugs that
  only showed up in the Hackage
  release. ([#746](https://github.com/swarm-game/swarm/pull/746))
- New "blank" creative scenario
  ([#741](https://github.com/swarm-game/swarm/pull/741))
- REPL improvements
    - `Ctrl-D` at an empty REPL prompt now triggers a quit
      ([#743](https://github.com/swarm-game/swarm/pull/743))
    - The REPL panel now persists in showing the type of the most
      recently evaluated expression ([#733](https://github.com/swarm-game/swarm/pull/733))

## **0.1.0.1** - 2022-10-06

A bugfix release for a few minor bugs that plagued the first release:

- Fall back to to the swarm data directory when a `run` file is not
  found ([#730](https://github.com/swarm-game/swarm/pull/730))
  - This bug caused the move tutorial to be unplayable because it tried to execute
    `run "data/scenarios/Tutorials/move_system.sw"`
- Fix version check when there is no GitInfo
  ([#729](https://github.com/swarm-game/swarm/pull/729))
  - This bug caused the game to always report that there was a new
    version available even when you already had the latest (and only!) version.

## **0.1.0.0** - 2022-10-06

First Swarm release! Swarm already has:

- a programming language based on the polymorphic
  lambda calculus + recursion, with a command monad for describing
  first-class imperative actions
- scenarios which can be loaded from YAML files
  - the release comes with official challenges and an in-game tutorial
  - the default Classic and Creative modes use the same YAML syntax
  - we include JSON schemas for editor support when writing scenarios 
- procedural 2D world generation
- LSP server built into the Swarm executable
- Terminal UI interface
  - running the executable opens the Main menu by default
  - game screen with a world view, inventory and REPL
    - popup windows for messages, challenge descriptions, etc.
