# Iran Geography Data - Neighborhoods

This repository contains detailed geographical data for neighborhoods across Iran in JSON format. The data can be used for a variety of purposes, such as geospatial analysis, location-based services, or demographic studies.

## File Overview

### neighborhoods.json
The `neighborhoods.json` file includes structured data representing neighborhoods in Iran. Each entry contains information about a specific neighborhood, such as its name, city, province, and geographical boundaries (if applicable).

## Features
- **Comprehensive Data**: Covers neighborhoods in multiple cities and provinces of Iran.
- **JSON Format**: Easy-to-use, human-readable, and compatible with most programming languages and tools.
- **Geographical Information**: May include boundaries or coordinates for spatial analysis.

## Usage

### Prerequisites
To use the data, you'll need basic knowledge of JSON and access to tools or programming languages that can parse JSON, such as:
- Python
- JavaScript
- R
- GIS software like QGIS or ArcGIS

### Accessing the Data
Clone this repository to your local machine:
```bash
git clone https://github.com/babaie774/Iran-geography-data.git
```

Navigate to the file location:
```bash
cd Iran-geography-data
```

### Sample Usage
#### Python Example
```python
import json

# Load the data
with open('neighborhoods.json', 'r', encoding='utf-8') as file:
    neighborhoods = json.load(file)

# Example: Print all neighborhoods in a specific city
city_name = "Tehran"
for neighborhood in neighborhoods:
    if neighborhood['city'] == city_name:
        print(neighborhood)
```

#### JavaScript Example
```javascript
const fs = require('fs');

// Load the data
fs.readFile('neighborhoods.json', 'utf8', (err, data) => {
    if (err) {
        console.error(err);
        return;
    }
    const neighborhoods = JSON.parse(data);

    // Example: Filter neighborhoods by province
    const provinceName = "Tehran Province";
    const filtered = neighborhoods.filter(n => n.province === provinceName);
    console.log(filtered);
});
```

### GIS Software
You can convert `neighborhoods.json` into GeoJSON format (if not already in GeoJSON format) for direct use in GIS applications such as QGIS or ArcGIS.

## Contributing
Contributions to enhance the data or add new features are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes and push them to your fork.
4. Open a pull request with a detailed description of your changes.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Acknowledgments
Special thanks to contributors who have helped curate and maintain this dataset.

---

### Contact
For questions, suggestions, or issues, please open an [issue](https://github.com/babaie774/Iran-geography-data/issues) or contact the repository owner.

---

Enjoy exploring Iran's neighborhoods with this dataset!
