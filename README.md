# Web Scraping Beauty Products from Snapklik.com

![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)
![Web Scraping](https://img.shields.io/badge/Web%20Scraping-FF6B6B?style=for-the-badge)
![Data Analysis](https://img.shields.io/badge/Data%20Analysis-4ECDC4?style=for-the-badge)

A comprehensive web scraping project that extracts beauty and skincare products from Snapklik.com using R, with advanced JavaScript content handling and intelligent product classification.

## 🎯 Project Overview

This project demonstrates advanced web scraping techniques by extracting beauty product data from a modern JavaScript-heavy e-commerce website. Originally specified to use Python, I adapted the solution to R to leverage my expertise with the `chromote` package for handling dynamic content.

### Key Achievements
- ✅ Successfully scraped **9 beauty products** from 1,470+ total products
- ✅ Handled dynamic JavaScript content loading
- ✅ Implemented intelligent product filtering and classification
- ✅ Created meaningful ingredient-based product groupings
- ✅ Overcame technical challenges with modern SPA architecture

## 🛠️ Technical Stack

- **Language**: R
- **Web Scraping**: `chromote` (headless Chrome automation)
- **Data Processing**: `dplyr`, `stringr`
- **HTML Parsing**: `rvest`
- **Dynamic Content**: JavaScript execution via Chrome DevTools Protocol

## 📊 Data Extracted

### Product Information
- Product ID, Brand Name, Product Name
- High-resolution product images (Amazon CDN)
- Size/Volume specifications
- Product descriptions and skin concerns  
- Ingredient compositions
- Source URLs

### Sample Products
- **Neutrogena** - Makeup Remover Cleansing Face Wipes
- **NYX Professional Makeup** - Mechanical Eyeliner Pencil
- **Maybelline New York** - Sky High Washable Mascara
- **Grande Cosmetics** - GrandeLASH-MD Lash Enhancing Serum
- **Bioderma** - Sensibio H2O Micellar Water

## 🧪 Ingredient Analysis & Grouping

Products are intelligently grouped by shared ingredients:

| Group | Shared Ingredients | Products | Use Case |
|-------|-------------------|----------|----------|
| **A** | Wax, Pigments | Sky High Mascara, Eye Pencils, Brow Products | Color cosmetics |
| **B** | Water, Cleansing Agents | Makeup Remover, Micellar Water | Facial cleansing |
| **C** | Wax, Mechanical Formula | Mechanical Eyeliner, Brow Pencils | Precision application |
| **D** | Growth Complex, Peptides | GrandeLASH Serum | Enhancement products |

## 🚀 Quick Start

### Prerequisites
```r
# Install required packages
install.packages(c("chromote", "rvest", "dplyr", "stringr"))
```

### Running the Scraper
```r
# Clone the repository
git clone https://github.com/yourusername/snapklik-beauty-scraper.git
cd snapklik-beauty-scraper

# Run the main scraping script
source("scripts/snapklik_scraper.R")
```

### Output Files
- `data/processed/snapklik_beauty_products.csv` - Complete product dataset
- `data/processed/product_ingredient_groups.csv` - Ingredient-based groupings

## 📁 Repository Structure

```
snapklik-beauty-scraper/
├── README.md
├── scripts/
│   └── snapklik_scraper.R          # Main scraping script
├── data/
│   ├── raw/                        # Raw scraped data (if any)
│   └── processed/                  # Cleaned, structured data
│       ├── snapklik_beauty_products.csv
│       └── product_ingredient_groups.csv
├── docs/
│   └── methodology.md              # Detailed process documentation
├── .gitignore
└── requirements.txt                # R package dependencies
```

## 🔧 Technical Challenges Solved

### 1. Dynamic Content Loading
- **Challenge**: JavaScript-rendered content not accessible via traditional scraping
- **Solution**: Used `chromote` for headless browser automation with proper wait strategies

### 2. Popup Handling  
- **Challenge**: Location-based popups blocking content access
- **Solution**: Implemented multiple dismissal strategies with fallback options

### 3. Product Classification
- **Challenge**: 1,470+ mixed products requiring beauty-specific filtering  
- **Solution**: Created intelligent regex patterns and keyword-based classification

### 4. Modern SPA Architecture
- **Challenge**: Angular framework with dynamic component names
- **Solution**: Raw HTML pattern matching instead of traditional DOM parsing

## 📈 Data Quality Metrics

- **Total Products Discovered**: 1,470+
- **Beauty Products Identified**: 16  
- **Quality Products Extracted**: 9
- **Data Completeness**: 90%+ (missing only barcode and pricing data)
- **False Positive Rate**: <1% (1 automotive product removed)

## 🔍 Key Features

### Robust Error Handling
- Multiple popup dismissal strategies
- Graceful handling of missing data fields
- Automatic retry mechanisms for failed requests

### Intelligent Filtering
- Beauty-specific keyword detection
- Pattern-based product classification  
- Automated false positive removal

### Scalable Architecture
- Modular code structure for easy extension
- Configurable product categories
- Export functionality for multiple formats

## 📚 Documentation

Comprehensive documentation includes:
- **Process Documentation**: Step-by-step methodology and challenges
- **Code Comments**: Detailed inline explanations  
- **Technical Notes**: Architecture decisions and lessons learned

## 🤝 Contributing

Contributions are welcome! Areas for enhancement:
- Price extraction from individual product pages
- Enhanced ingredient analysis via cosmetic databases
- Multi-language support
- Automated re-scraping schedules

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Alfred Agbashe**
- GitHub: [@AlfredAgbashe](https://github.com/AlfredAgbahe)
- LinkedIn: [AlfredAgbashe](https://linkedin.com/in/alfred-agbashe-/)

## 🙏 Acknowledgments

- Veefyed Team for the challenging and engaging interview task
- Chromote package developers for excellent JavaScript handling capabilities
- R community for robust web scraping ecosystem

---

*This project was developed as part of a technical interview process, demonstrating advanced web scraping capabilities and problem-solving skills in handling modern web architectures.*
