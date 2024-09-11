# Real Estate Price Prediction

## Contributors

| Name               | Student ID | Contribution |
|--------------------|------------|--------------|
| Đặng Thị Kim Anh  | 21280084   | 30%          |
| Lê Hồ Hoàng Anh   | 21280085   | 40%          |
| Nguyễn Phúc Loan  | 21280098   | 30%          |

## Web Scraping

### Libraries Used
- **BeautifulSoup**: For parsing HTML content.
- **urllib.request**: For downloading HTML.
- **requests**: For handling HTTP requests.
- **pandas**: For data manipulation and saving data.
- **numpy**: For numerical operations.
- **re**: For regular expression operations.

### Functions
- `download_html(url)`: Downloads HTML content from a specified URL.
- `scrape_room(soup_link)`: Extracts the number of bedrooms (`so_PN`) and bathrooms (`so_WC`) from a webpage.
- `scrape_block(house_block, pos)`: Scrapes detailed property information from a single listing.
- `scrape_house_page(house_blocks)`: Collects data from all property listings on a given page.

### Execution
The script loops through real estate pages, collects property data, and saves it into a CSV file. The dataset includes details such as acreage, number of rooms, price, and location.

## Data Processing and Analysis

### Handling Missing Data
- Missing values are addressed using the Multiple Imputation by Chained Equations (MICE) method from the `fancyimpute` library.

### Price Conversion
- Prices are standardized into a consistent unit (billion VND) by converting terms such as 'Thỏa thuận', 'nghìn', 'triệu', 'tỷ' into numerical values.

### Feature Engineering
- Categorical variables are encoded, and missing values are handled appropriately.

## Model Training and Evaluation

### Models
- **Linear Regression**
- **Ridge Regression**
- **Lasso Regression**
- **Random Forest**
- **Gradient Boosting**

### Metrics
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **Mean Absolute Error (MAE)**
- **R² Score**

### Results
- **Linear Regression**:
  - Train R² Score: [Value]
  - Test R² Score: [Value]
- **Ridge Regression**:
  - Train R² Score: [Value]
  - Test R² Score: [Value]
- **Lasso Regression**:
  - Train R² Score: [Value]
  - Test R² Score: [Value]
- **Random Forest**:
  - Train R² Score: [Value]
  - Test R² Score: [Value]
- **Gradient Boosting**:
  - Train R² Score: [Value]
  - Test R² Score: [Value]

## Conclusion

The Gradient Boosting model is preferred over Random Forest due to its better adaptation to errors and learning capability. Both models show similar R² scores, but Gradient Boosting demonstrates superior performance in handling data complexity.

---

**Note**: Replace `[Value]` placeholders with actual R² scores obtained from your analysis.
