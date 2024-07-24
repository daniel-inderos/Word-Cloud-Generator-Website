# Advanced Automated Word Cloud Generator

This project is a web-based application that generates interactive word clouds from either a provided URL or an uploaded text file. It offers a user-friendly interface and advanced features for creating, exploring, and exporting word clouds.

## Features

- Generate word clouds from:
  - Website content (by entering a URL)
  - Uploaded text files
- Interactive word cloud visualization
- Click on words to see their frequency
- Export word cloud as a PNG image
- Responsive design for various screen sizes
- Error handling and loading indicators

## Technologies Used

- HTML5
- CSS3
- JavaScript (ES6+)
- D3.js (v5.16.0) for data visualization
- D3-Cloud (v1.2.5) for word cloud layout
- FileSaver.js (v2.0.5) for exporting images

## How to Use

1. Clone this repository or download the HTML file.
2. Open the HTML file in a modern web browser.
3. To generate a word cloud:
   - Enter a website URL in the input field, or
   - Upload a text file using the file input
4. Click the "Generate Word Cloud" button.
5. Once generated, interact with the word cloud by clicking on words to see their frequency.
6. To save the word cloud, click the "Export as PNG" button.

## Features in Detail

### Word Extraction and Processing
- Removes HTML tags from website content
- Converts text to lowercase
- Filters out common stop words and numeric strings
- Limits the cloud to the top 100 most frequent words

### Word Cloud Visualization
- Uses a color scheme for better word differentiation
- Applies random rotation (0° or 90°) to words for varied appearance
- Sizes words based on their frequency in the text

### User Interaction
- Clicking on a word displays its frequency
- Loading indicator during word cloud generation
- Error messages for invalid inputs or processing issues

## Customization

You can customize the word cloud by modifying the following parameters in the JavaScript code:

- `width` and `height`: Change the size of the word cloud
- `stopWords`: Add or remove words from this set to customize excluded words
- Color scheme: Modify the `colorScheme` variable in the `draw` function
- Word sizing: Adjust the `fontSize` calculation in the D3-Cloud layout configuration

## Notes

- The application uses a CORS proxy (AllOrigins) to fetch content from URLs. This may have limitations or require replacement in a production environment.
- For large text inputs, the generation process may take a few moments. The application provides a loading indicator during this time.

## License

This project is open-source and available under the MIT License.