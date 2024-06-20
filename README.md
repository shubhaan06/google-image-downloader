# Google Image Downloader

Google Image Downloader is a Python-based tool that leverages the `icrawler` library to efficiently download images from Google Images. This project provides a straightforward and customizable solution for collecting images for research, datasets, or personal use.

## Features

- **Automated Image Downloading**: Easily download images from Google Images using specified keywords.
- **Customizable Search Parameters**: Tailor the number of images, image size, color, and type to your needs.
- **Organized Output**: Save images in structured directories based on search queries.
- **Robust Error Handling**: Built-in mechanisms to handle errors and retries, ensuring reliable downloads.

## Installation

To install the necessary dependencies, run:

```bash
pip install icrawler
```


## Usage

Here’s a basic example to get you started:

```python
from icrawler.builtin import GoogleImageCrawler

def download_images(keyword, max_num):
    google_crawler = GoogleImageCrawler(storage={'root_dir': f'./images/{keyword}'})
    google_crawler.crawl(keyword=keyword, max_num=max_num)

# Example usage
download_images('puppies', 100)
```
## Customization

You can customize search parameters by modifying the `crawl` method parameters:

- **keyword**: The search term for finding images.
- **max_num**: The maximum number of images to download.
- **filters**: A dictionary for additional filters such as size, color, and type.

Example with additional filters:

```python
from icrawler.builtin import GoogleImageCrawler

def download_images_with_filters(keyword, max_num, filters):
    google_crawler = GoogleImageCrawler(storage={'root_dir': f'./images/{keyword}'})
    google_crawler.crawl(keyword=keyword, max_num=max_num, filters=filters)

# Example usage with filters
filters = {
    'size': 'large',
    'color': 'blackandwhite',
    'type': 'photo'
}

download_images_with_filters('sunsets', 50, filters)
```
## Contributing

We welcome contributions! If you have suggestions for improvements or new features, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License.

## Contact

For any questions or inquiries, please contact [shubhaan2004@gmail.com](mailto:shubhaan2004@gmail.com).





