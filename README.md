# project
> Inflation = pdfetch_FRED("CPALTT01USM659N")
> names(Inflation) = "Inflation"
> Inflation = ts(Inflation, start=c(1960, 1), frequency=12)
> CPI = pdfetch_FRED("PCEPILFE")
> names(CPI) = "CPI"
> Inflation = diff(log(CPI), lag = 12) * 100
> names(Inflation) = "Inflation"
> Inflation = ts(Inflation, start=c(1959, 1), frequency=12)
> Inflation = na.omit(Inflation)
> Inflation = pdfetch_FRED("CORESTICKM159SFRBATL")
> names(Inflation) = "Inflation"
> Inflation = ts(Inflation, start=c(1967, 12), frequency=12)
TCU = pdfetch_FRED("TCU")
> names(TCU) = "TCU"
> TCU = ts( TCU , start=c(1967, 1), frequency=12)
