Rock, Paper, Scissors Challenge Attempt
==========================

The original README text is retained below.


Current Issues
--------------

- The web application is rendering in standard, not styled HTML and doesn't look too exciting - I could try adding a layout.erb file to see I can make things more interesting
- I haven't been able to get around to creating the extended game logic - it might be possible to add this logic to the current rps class, but it might be better to have a seperate class for it?
- Would it be better to create seperate game views for the different game mode? Or use a similar conditional approach to the multiplayer session variable? I feel new views on the whole are probably clearer.


Approach
--------

Divide responsibilities up between classes, keep methods short, use private methods when appropriate, use a strict TDD approach to develop classes, methods and feature testss, make sure tests are independent, stick to the Single Responsibility Principle as much as possible. Use webhelpers to reduce clutter in tests and try to make output as human readable as possible.

I have tried to use conditionals to reduce the number of POST/redirect/GETS and therefore use some of the same pages twice. I'm not sure if that is the best way to do things in the end, it might be better
to have specific views for all two player interactions that are distinct from one player views.

I wanted to try to improve my tests and I feel that these are a lot better, I am starting to get to grips with using mocks and tried experimenting with contexts blocks to aid readability.

This challenge was a lot of fun!

===========================================================================

Original README below

# RPS Challenge

## Instructions

* Challenge time: until the end of the day
* Feel free to use google, your notes, books etc but please work on your own
* Please raise a pull request when you start this challenge, and keep pushing updates as and when you make commits throughout the day
* Please submit a _diagram_ of how the browser interacts with a server from either your battle challenge or this challenge. This can be a photo of a pen/paper picture or a computer diagram.
* There is _no expectation_ to finish all or any of the user stories, please use this time to reflect on where you feel you are with the skill and what may support your learning.
* If you get blocked, please reflect on what blocked you and any strategies you adopted that helped you make progress.

## Set up

```bash
$ bundle install
$ rspec
# You should output that includes:
# 1 example, 0 failures
```

## Task

Knowing how to build web applications is getting us almost there as web developers!

The Makers Academy Marketing Array ( **MAMA** ) have asked us to provide a game for them. Their daily grind is pretty tough and they need time to steam a little.

Your task is to provide a _Rock, Paper, Scissors_ game for them so they can play on the web with the following user stories:

```
As a marketeer
So that I can see my name in lights
I would like to register my name before playing an online game

As a marketeer
So that I can enjoy myself away from the daily grind
I would like to be able to play rock/paper/scissors
```

Hints on functionality

- the marketeer should be able to enter their name before the game
- the marketeer will be presented the choices (rock, paper and scissors)
- the marketeer can choose one option
- the game will choose a random option
- a winner will be declared

As usual please start by:

* Forking this repo
* Test-driving development of your app

## Resources

* [HTML forms](https://www.w3schools.com/html/html_forms.asp)
* [Capybara cheatsheet](https://devhints.io/capybara)
* [Twitter bootstrap css library](https://getbootstrap.com/)
* [Hosting on heroku](https://heroku.com)

## Bonus level 1: Multiplayer

Change the game so that two marketeers can play against each other ( _yes there are two of them_ ).

## Bonus level 2: Rock, Paper, Scissors, Spock, Lizard

Use the _special_ rules ( _you can find them here http://en.wikipedia.org/wiki/Rock-paper-scissors-lizard-Spock_)

## Basic Rules

- Rock beats Scissors
- Scissors beats Paper
- Paper beats Rock

In code review we'll be hoping to see:

* All tests passing
* High [Test coverage](https://github.com/makersacademy/course/blob/master/pills/test_coverage.md) (>95% is good)
* The code is elegant: every class has a clear responsibility, methods are short etc.
* Commits and short and scoped

Reviewers will potentially be using this [code review rubric](docs/review.md).  Referring to this rubric in advance may make the challenge somewhat easier.  You should be the judge of how much challenge you want this weekend.

## Notes on test coverage

Please ensure you have the following **AT THE TOP** of your `spec/spec_helper.rb` in order to have test coverage stats generated on your pull request:

```ruby
require 'simplecov'
require 'simplecov-console'

SimpleCov.formatter = SimpleCov::Formatter::MultiFormatter.new([
  SimpleCov::Formatter::Console,
  # Want a nice code coverage website? Uncomment this next line!
  # SimpleCov::Formatter::HTMLFormatter
])
SimpleCov.start
```

You can see your test coverage when you run your tests. If you want this in a graphical form, uncomment the `HTMLFormatter` line and see what happens!
