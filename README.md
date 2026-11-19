# Input Cost Monitor

## The company

Midlands Precision Components Ltd. a fictional UK manufacturer of machined metal parts for the automotive and industrial sectors.

## Who needs this

The Head of Procurement and finance managers, who need early warning of rising material costs.

## The problem

Cost increases are only discovered when invoices arrive

## Questions this project answers

How much has each materials cost changed, and how much of that came from the suppliers price versus the exchange rate?

## What we track (materials, countries, currencies)

Steel, aluminium and copper imports from China, Germany and the USA, in USD, EUR and CNY against GBP.

## KPIs

Cost per kg in GBP, monthly % change, and the split between price effect and currency effect.

## Data sources

UN Comtrade for import prices, Frankfurter for exchange rates and ONS for UK inflation.

## Architecture

Data is pulled daily from the APIs into Bronze as raw files, cleaned into Silver tables in Azure SQL, and turned into Gold views that answer procurement's questions, all scheduled by GitHub Actions.

## Data requirements

Monthly data per material and country, with at least 3 years of history, refreshed daily.

## Done looks like

A daily automated pipeline loads clean data into Azure SQL, with tests and CI on GitHub.

## Out of scope

Real company data, forecasting future prices, and automatic buying decisions.
