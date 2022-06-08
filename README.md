ecos package
---

### Introduction
Economic Statistics System of Bank of Korea through the OPEN API  
(https://ecos.bok.or.kr/api/#/)

### Installation
```r
if (!require(devtools)) install.packages("devtools"); require(devtools)  
devtools::install_github("seokhoonj/ecos", force = TRUE)  
library(ecos)
```

### examples
```r
# data search (if you don't know the stat_code / item_code)
interest_rate <- statSearch(api_key = _your_api_token_)
Please insert stat_code: 902Y006
Please insert item_code: US

# or simply
interest_rate <- statSearch(api_key = _your_api_token_, stat_code = "902Y006", item_code = "US")

# data search (using item_code, item_code2 and item_code3)
non_bank_loans <- statSearch(api_key, stat_code = "088Y015", item_code = "AEX10000", item_code2 = "0920", item_code3 = "U00")
```

