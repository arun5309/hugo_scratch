+++
date = '2026-09-20T14:28:39+05:30'
draft = false
title = 'Proposal Chess'
toc = false
+++

# TLDR

Proposal chess is a chess variant that aims to reduce the emphasis on opening preparation similar to [Chess960](https://en.wikipedia.org/wiki/Chess960). Unlike Chess960 which achieves this by starting with a position that is likely unfamiliar to both the two players, proposal chess achieves this by having each player proposing a starting position for their proposing board. This does not eliminate the need for preparation completely but reduces it as there is only one position you need to prepare per game. Also, you can possibly forget your preparation once the game is over as it unlikely that you will reuse the same preparation (this is not applicable to online games or for lower-rated players). Naively, letting a player propose has the problem of the player proposing a position in which they will mate their opponent in one move. This is resolved by having one player propose the starting position and letting the other player decide who plays with what color. This resolves the issue in a manner similar to how the [cake-cutting](https://en.wikipedia.org/wiki/Fair_cake-cutting) problem is solved.

# Mathematical Inspiration (Skip if not interested)

## Cake-Cutting Background

The cake-cutting problem is a game theory problem in which a resource like a cake or a chess position has to be fairly divided among two people (generally it is applicable to more than two people but we won't worry about it here). The most common solution to this problem is one person cuts the cake into two pieces and the other person chooses who gets what piece. This solution is adopted to proposal chess as one player proposing a starting position and the other player deciding who gets what color. This achieves fairness in that if two rational chess gods who always play perfectly play against each other, neither of them are going to be forced to start with a bad position.

## Achieving Complete Symmetry

If we only have one board there is still the practical advantage for the player proposing to come with home preparation. This issue is resolved by, having two boards in which each player is a proposer on exactly one of the boards. The players should also simultaneously propose their positions without looking at their opponent's proposal even partially. This has the positive side-effect of achieving complete symmetry which is not the case with even regular chess. As in regular chess the player with the white pieces usually has a slight practical advantage (although the preference may differ for some players or based on context).

# Basic Rules of Proposal Chess

## Entities

* The two players will be referred to as Player X and Player Y. 

* The two boards will be referred to as Board 1 and Board 2.

## Glossary

* *Starting position*: This constitutes the placement of pieces for both white and black sides on a standard chessboard, which side (white or black) should play the first move, what kind of castlings are allowed for both sides if any, what kind of en passant is allowed if any. Basically contains all the information in a [FEN](https://en.wikipedia.org/wiki/Forsyth%E2%80%93Edwards_Notation) except for information regarding move count or information regarding fifty move (or hundred move) rule. There is also no need to specify any information regarding threefold repetition the starting position will be considered to be reached for the first time.

## Phases of Play

### Proposal Phase

* At the start of this phase Player X will propose the starting position of Board 1, and Player Y will propose the starting position of Board 2. They will both do so without looking at the starting position proposed by their opponent even partially. Ideally they would come with their starting positions printed on a piece of paper and hand it to the arbiter.

* Then both the players get to see the starting position proposed by their opponent. Then Player X will choose if he will play with white or black pieces on Board 2, and Player Y will choose if he will play with white or black pieces on Board 1. All of this should happen within a pre-specified duration, that will be referred to as the 'choosing time'. They will choose without revealing their choice to the opponent. This can be perfomed by placing a coin under a opaque cup, with heads corresponding to white and tails corresponding to black. If a player fails to choose his color within the choosing time they are considered lost on that board but not considered lost on the entire game and they are allowed to play the other board.

### Playing Phase

* At start of the playing phase, the choices made by the players will be revealed to each other.

* Then immedietely they play against each other from the proposed starting positions with their chosen sides under some pre-specified time control that will be referred to as 'playing time control'. This time control can have Fischer increment or Bronstein delay like in standard chess. There will be two chess clocks set to the playing time control, one per board.

* The playing rules are largely same as that of standard chess with exception of starting position, any ambiguities regarding who should move first or castling or en passant is resolved by referring to the specification of the starting position.

## Scoring and Winner Determination

* A simple scoring system of winning on a board gives 1 point, drawing on a board gets 0.5 points, and losing gets 0 points.

* The total score for a player is the sum of the scores on both boards.

* The player with the higher score wins.  

# Analysis of Strategies

## Proposing a One-Sided Position

Proposing a position in which one-side is clearly winning is a poor strategy as your opponent will simply choose the winning side.

## Proposing an Equal Position

Proposing an objectively equal position is the best strategy mathematically speaking. However, it must be an interesting position for the proposing player to get an advantage out of the proposal. This will be strategy that will be adopted by chess gods who play perfect chess. One could also propose a posistion that plays to your strengths or plays against your opponent's weaknesses. Like, proposing a complex tactical position against a positional player.

## Gambling with the Proposal

The proposer can gamble by proposing a position that is winning for one-side but that is hard for humans to understand. This is a viable strategy in practice but comes with a lot of risks.

# Additional Rules and Variations

The following rules could additionally be adopted:

* One could disallow players from proposing certain positions. Like positions with weird pawn structures, or unusual positions with weird combination of pieces like five minor pieces versus three rooks positions. This would ideally be decided by a software that the players had access to while they were preparing what position to propose.

* Time formats (proposal and play. heterogenous and homogenous). Time scrambles. Number of moves.

* Armageddon (both propose and play with bidding time, lower time bidder gets plays with draw odds)

* 50/100 move rule, 3-fold repetition

* Point system for tournaments

* Sequential play instead of simultaneous but committed to the position initially. Time scrambles.

* Allowing to look at opponents proposal and changing.

* Early cutoff of proposal time

* Should we reveal whether the opponent has decided or not.

* Failing to choose consider completely lost?

* Alternative scoring?

# Join the Conversation

* Already knows

* Feedback on additional rules

* Quality of games

* Other two player board games (no need to restrict to chess)

* Play and have fun
