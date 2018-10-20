# Spin-the-Wheel Coin Matching Game
* Author: Dr. Jody Paul
* Version: 20181015.1
* Copyright (c) 2018 by Dr. Jody Paul


## 1. Project Name

**Spin-the-Wheel Coin Matching Game**


## 2. Background - Game Description

A wheel contains a ring of coins.

The wheel is in a winning state whenever all of the coins in the wheel
are in the same state (all heads-up or all tails-up).

In documentation, the state heads-up is represented as H;
the state tails-up as T.
Thus, the wheel is in a winning state whenever all coins in the wheel
are indicated as T or all as H.

A game involves a player attempting to configure a wheel into a
winning state.

An instance of a game involves a wheel with a specified number of coins.
All coins states are initially hidden from the player.

An instance of a game also specifies the maximum number of turns a
player may take while attempting to configure the wheel into a
winning state.
If the player successfully configures the wheel into a winning state,
then they player wins that game.
If the player does not configure the wheel into a winning state
before the number of turns has been used, the player loses that game.

An instance of a game also specifies the number of coins whose states
will be revealed simultaneously to the player in a given turn.

A turn proceeds as follows:

(0) If the wheel is in a winning state, the player wins and the game is over.<br>
 &nbsp;&nbsp;&nbsp;&nbsp;If the number of turns per game is exceeded, the player loses and the game is over.

(1) The player indicates which of coins are to be revealed in this turn
and the state of each indicated coin is disclosed to the player.

(2) After observing the revealed coin states, the player may elect to
modify any of the states of the revealed coins.

(3) After the coin states have been set, the coins are again hidden and the
wheel is spun by an amount not determinable by the player.


## 3. Directory Organization

### 3.1 Top-Level:
- Overview and Instructions (README.TXT)
- Java source code in unnamed package (*.java)
- JUnit source code test classes (*Test.java)
- Buildfile for Ant (build.xml)
- Proguard configuration (*.pro)
- Directory of support tools for development and testing (lib/)

### 3.2 lib/
- Files that support JUnit, JaCoCo, Checkstyle, Java2HTML, CPD, PMD, Proguard

- See:
  - https://junit.org
  - https://www.jacoco.org/jacoco/trunk/doc
  - http://checkstyle.sourceforge.net
  - http://www.java2html.com
  - https://pmd.github.io
  - https://sourceforge.net/projects/proguard/


## 4. Automation via Ant
See: https://ant.apache.org

The default target (all) removes artifacts from previous builds and tests,
creates maintainer-appropriate API documentation (doc-private), generates HTML
formatted versions of the source code, verifies adherence to some Java
coding conventions, runs JUnit tests and formats results, determines code
coverage of the tests, and flags areas of the source code most likely to
contain weaknesses (including complexity metrics).

The set of main targets can be displayed at the command line using: `ant -p`

For example...
```
% ant -p
Buildfile: build.xml

      Build file for StrategicPlayer project
  
Main targets:

 checkstyle           generate checkstyle report
 clean                clean up
 compile              compile the source
 cpd                  proccess source with CPD
 dist                 generate the distribution
 doc                  generate the usage documentation
 doc-private          generate the maintenance documentation
 env                  display build parameters
 format               generate formatted versions of source code
 optimize             optimize using proguard
 pmd                  process source with PMD
 report               format junit test results
 run                  run driver
 test                 run junit tests
 testCoverage         run junit tests with JaCoCo instrumentation
 testCoverageReport   format JUnit and JaCoCo test results
 testOptimized        run junit tests using optimized jar
 testOptimizedReport  format junit test results using optimized jar
Default target: all
%
```

## 5. TODO
- Add support for FindBugs/SpotBugs
