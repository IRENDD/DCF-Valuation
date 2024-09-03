## About the project
An automated DCF analysis tool that extracts and processes financial data from SEC 10-K forms using Selenium and Pandas, enabling efficient calculation of key valuation metrics.

## Code Steps
1. This code automate the process of extracting financial information from the SEC's EDGAR database for a targeted company. The script uses Selenium WebDriver to interact with the SEC's website, retrieve the latest 10-K fillings (up to a specified maximum), and download them for further analysis. Additionally, the script captures key company details such as the industry category, ticker, and operating location.
2. Then, it extracts financial information from a set of SEC filings in Excel format using Pandas. Specifically designed for a targeted company, it locates key financial data across multiple financial statements, such as the balance sheet, income statement, and cash flow statement, and stores them in a dictionary categorized by dates.
3. This script automates the extraction and processing of financial data from SEC filings by leveraging Sentence Transformers to accurately match and identify financial attributes. It retrieves key metrics such as revenue growth, tax rates, working capital, and operating income, among others, from multiple financial statements. The data is organized and categorized by date, allowing for a chronological analysis of the company’s financial performance. Additionally, the script calculates both singular and compound financial metrics, providing a comprehensive overview of the company's financial health. The results are then displayed in a structured format, making them easy to analyze and interpret.
4. Based on Aswath Damodaran's approach, we capitalize R&D expenses and operating leases to accurately reflect their long-term economic impact on key financial metrics like EBIT, invested capital, equity, and debt.
5. The script calculates both singular and compound Discounted Cash Flow (DCF) metrics, including cost of equity and capital, and projects Free Cash Flow to Firm (FCFF) over a specified period. It also uses the SentenceTransformer package to enhance financial term matching accuracy, ultimately determining the company's valuation and whether its stock is under or over-valued.

## Why are we capitalizing R&D and Opearing Lease?
1. The reasoning for capitalizing R&D expenses is rooted in the understanding that these expenses create long-term benefits, much like investments in land, plant, and equipment. In many firms, especially in sectors like pharmaceuticals and high technology, R&D expenditures often have even more extended benefits than physical capital investments. Therefore, according to Aswath Damodaran's approach, R&D expenses should be treated as capital expenditures
2. Similarly, capitalizing operating leases reflects their nature as long-term financial commitments that are akin to debt. Operating leases create future payment obligations that, if left off the balance sheet, can distort a firm's true financial position by underestimating its liabilities and invested capital. By treating operating leases as debt-like obligations, we align financial statements more closely with economic reality, ensuring more accurate measures of leverage, profitability, and return on assets, while improving comparability across firms with differing leasing practices.

## To be uptdated
1. Preferred Stocks calculations and addition to the DCF 
2. Plotting different graphs regarding to the DCF valuation and other metrics using Matlab
3. Automatic extraction of targeted company's share price through Yahoo website using Selenium
4. Dynamic Assumptions for DCF Valuations
5. More flexible calculation of beta (such as Jensen's alpha, bottom-up beta and etc.)
6. FCFE, FCFF 3-steps projections
7. Employ NLP for finding financial attributes from Excel 10-K

## Reference
1. Aswath Damodaran's Valuation Course in NYU - https://www.youtube.com/watch?v=LYGYvN5LUbA&list=PLUkh9m2BorqmtIQKZ1jv3uuZDM_bQIICg
2. Reasoning for capitalizing Operating Lease - https://pages.stern.nyu.edu/~adamodar/pdfiles/papers/oplev.pdf
3. Reasoning for capitalizing R&D - https://pages.stern.nyu.edu/~adamodar/pdfiles/papers/R_D.pdf
4. Country Default Spreads and Risk Premiums - https://pages.stern.nyu.edu/~adamodar/New_Home_Page/datafile/ctryprem.html
5. Average metrics for different Industries - https://pages.stern.nyu.edu/~adamodar/New_Home_Page/datafile/Betas.html
