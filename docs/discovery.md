# Crypto Dashboard — Discovery Document

# Project Overview

This project aims to build a cryptocurrency dashboard application that
displays real-time market data for multiple cryptocurrencies.

The application will present cryptocurrencies as interactive cards. Each
card will represent a cryptocurrency and will display summary
information such as name, price, and market ranking.

When a user selects a card, the interface expands to show detailed
analytics, including historical price charts and comparisons with other
major cryptocurrencies.

The goal of this project is to practice:

-   API integration
-   Data visualization
-   Interactive UI design
-   Component-based architecture
-   State management

------------------------------------------------------------------------

# Target Features

## Cryptocurrency Cards

The main screen will display a list of cryptocurrencies as cards.

Each card will include:

-   Cryptocurrency name
-   Symbol
-   Current price
-   Market rank
-   24h price change
-   Logo

Example:

[ Bitcoin ] Price: R$ 320,000 24h Change: +2.3% Rank: #1

------------------------------------------------------------------------

## Card Interaction

Clicking on a card will expand it into a detailed view.

This view will show:

-   Full price chart
-   Currency selector (BRL / USD)
-   Historical data
-   Comparison charts

------------------------------------------------------------------------

## Data Visualization

The expanded view will include the following charts:

Price History Chart

Displays the cryptocurrency price across a configurable period.

User can choose:

-   7 days
-   30 days
-   90 days
-   1 year

------------------------------------------------------------------------

## Currency Comparison

Users can switch between:

-   BRL
-   USD

This will update the chart values accordingly.

------------------------------------------------------------------------

## Market Comparison Chart

Displays the selected cryptocurrency compared to the top 5
cryptocurrencies by market capitalization.

If the selected cryptocurrency is already in the top 5, the comparison
will include the top 6 instead.

------------------------------------------------------------------------

# Data Source

This project will use the public API from:

CoinGecko API

Key endpoints expected to be used:

/coins/markets /coins/{id} /coins/{id}/market_chart

Data retrieved will include:

-   price
-   market cap
-   volume
-   historical price data

------------------------------------------------------------------------

# Application Structure (High-Level)

crypto-dashboard │ ├── main.py │ ├── api │ └── coingecko_client.py │ ├──
components │ ├── crypto_card.py │ ├── chart_component.py │ └──
expanded_card_view.py │ ├── services │ └── crypto_service.py │ ├──
models │ └── crypto_model.py │ └── assets

------------------------------------------------------------------------

# UI Architecture

The interface will follow a component-based structure.

Primary components:

CryptoCard

Displays summary data for a cryptocurrency.

ExpandedCryptoView

Displays detailed analytics for the selected cryptocurrency.

ChartComponent

Reusable component for price visualization.

------------------------------------------------------------------------

# Technical Stack

Language: - Python

Framework: - Flet

External APIs: - CoinGecko API

Visualization: - Chart library compatible with Flet

------------------------------------------------------------------------

# Learning Goals

This project aims to practice:

-   Consuming REST APIs
-   Parsing JSON responses
-   Structuring Python applications
-   Building reusable UI components
-   Implementing interactive dashboards
-   Working with financial data

------------------------------------------------------------------------

# Future Enhancements

Possible future improvements include:

-   Search functionality
-   Favorite cryptocurrencies
-   Portfolio tracking
-   Notifications for price changes
-   Dark / light mode
-   Mobile layout optimization

------------------------------------------------------------------------

# Success Criteria

The project will be considered successful when:

-   Cryptocurrency data loads correctly from the API
-   Cards render dynamically
-   Charts display historical price data
-   Currency conversion works
-   Market comparison charts render correctly
