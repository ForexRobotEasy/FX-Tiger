# FX Tiger Indicator

## Overview

The FX Tiger Indicator is a custom Forex indicator developed by the Forex Robot Easy Team. It is designed to identify strong and weak currencies based on their strength and weakness scores. The indicator calculates the currency scores and provides a user-friendly interface for pairing strong and weak currencies.

For detailed reviews and trading results of this product, please visit the official website: [FX Tiger Review - Boost Your Trades with Advanced Forex Indicator](https://forexroboteasy.com/forex-robot-review/fx-tiger-review-boost-your-trades-with-advanced-forex-indicator/)

Please note that ForexRobotEasy is not the official developer of this product. We are showcasing a sample code that can work as described in this product. To find the official developer of this product, please use MQL5.

## Currency Score Calculation

The `CalculateCurrencyScore` function takes a currency code as input and returns a score based on the currency's strength and weakness. The calculation logic is not provided in the code and should be added separately.

```
double CalculateCurrencyScore(string currency)
{
    double score = 0;
    
    // Add code to calculate score based on currency strength and weakness
    
    return score;
}
```

## Identify Strong and Weak Currencies

The `IdentifyStrongWeakCurrencies` function retrieves a list of major currencies and calculates the score for each currency using the `CalculateCurrencyScore` function. It then identifies the strong and weak currencies based on the calculated scores.

```
void IdentifyStrongWeakCurrencies()
{
    // Get list of all major currencies
    string[] majorCurrencies = {'USD', 'EUR', 'GBP', 'JPY', 'AUD', 'CAD', 'CHF'};
    
    // Calculate score for each currency
    double[] scores = new double[majorCurrencies.Length];
    for (int i = 0; i < majorCurrencies.Length; i++)
    {
        scores[i] = CalculateCurrencyScore(majorCurrencies[i]);
    }
    
    // Identify strong and weak currencies
    List<string> strongCurrencies = new List<string>();
    List<string> weakCurrencies = new List<string>();
    
    for (int i = 0; i < scores.Length; i++)
    {
        if (scores[i] >= 5)
        {
            strongCurrencies.Add(majorCurrencies[i]);
        }
        else if (scores[i] <= -5)
        {
            weakCurrencies.Add(majorCurrencies[i]);
        }
    }
    
    // Print the results
    Print('Strong Currencies: ' + string.Join(', ', strongCurrencies.ToArray()));
    Print('Weak Currencies: ' + string.Join(', ', weakCurrencies.ToArray()));
}
```

## User Interface

The `OnChartEvent` function is triggered when a chart event, specifically a click event, occurs. It is responsible for displaying a user-friendly interface for pairing strong and weak currencies. The code for the user interface is not provided and should be added separately.

```
void OnChartEvent(const int id, const long& lparam, const double& dparam, const string& sparam)
{
    if (id == CHARTEVENT_CLICK)
    {
        // Display a user-friendly interface for pairing strong and weak currencies
        // Add code for user interface here
    }
}
```

## Main Function

The `OnStart` function is the main entry point of the code. It calls the `IdentifyStrongWeakCurrencies` function to identify strong and weak currencies. Additional code for trading functions, testing, and documentation can be added after the call to `IdentifyStrongWeakCurrencies`.

```
void OnStart()
{
    // Identify strong and weak currencies
    IdentifyStrongWeakCurrencies();
    
    // Add code for trading functions here
    
    // Add code for testing here
    
    // Add code for documentation here
}
```

Please refer to the official website for detailed reviews and trading results of the FX Tiger Indicator: [FX Tiger Review - Boost Your Trades with Advanced Forex Indicator](https://forexroboteasy.com/forex-robot-review/fx-tiger-review-boost-your-trades-with-advanced-forex-indicator/)
