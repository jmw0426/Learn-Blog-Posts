---
layout: post
title:      "CLI Data Gem Project"
date:       2020-09-17 20:18:29 +0000
permalink:  cli_data_gem_project
---


Have you ever needed to convert US dollars into Polish złoty, turn Croatian kuna into Romanian leu, or exchange Swedish krona with Israeli new shekel? Now you can with the Currency Exchange CLI Data Gem! This project was built so that you have two modes from which to choose: Default Mode and Free Mode. In Default mode you can compare the US dollar to one of 32 other currencies. In Free Mode you can choose from 33 different currencies and convert them into any other currency that is recognized by the European Central Bank. 

This gem utilizes HTTParty to parse data from https://api.exchangeratesapi.io/ which, in turn, populates a class variable array by iterating through the hash "rates" and shovelling in mass created objects that each have two instance variables: name and value. In Default Mode, the selector works by calling a method that reads the place value of the associated object within the class variable array and returning its associated name and value. Free Mode, on the other hand, utilizes a call to the API in order to create objects to reference and then uses the user's input to associate the class variable array place value to the proper directory within the API; creating, at least, two separate calls per session. Both of these modes are conjoined by a class called 'CLI' in order to create easy navigation throughout the program. 

Speaking of navigation, there are multiple options that are implemented throughout both modes. The first option, exit, prompts the user for confirmation and asks if they want to exit the program, continue on their current mode, or select a different mode with a different session. The second option, menu, redirects the user to select another currency within their current mode. Any entry made outside of these parameters will, depending on the user's place in the program, redirect to currency selection or render an error message that asks for input again while saving the user's progress. 

Lastly, both modes utilize basic multiplication on the exchange rates that are parsed from the API. Both display the comparison in currency value and allow the user to enter any number to convert from the base currency to the selected currency. Additionally. the entirety of the Currency Exchange is voice guided and allows the user to enter their name; which will be referenced throughout the mode they select. 

If you would like to check out this gem that I created for the FlatIron School, please go to https://github.com/jmw0426/currency_exchange.
