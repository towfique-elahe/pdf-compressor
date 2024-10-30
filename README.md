# PDF Compression Tool with Image Optimization

### Description: <br>
A Python tool designed to reduce PDF file size by compressing and downscaling images within the PDF. This program uses PyMuPDF to access and manipulate PDF images and Pillow to resize and compress image quality. Ideal for reducing large PDF files containing high-resolution images, making them more manageable for storage, sharing, or web uploads.

### Features: <br>
<ul>
  <li>Image Downscaling and Compression: Reduces the resolution of images embedded within PDF pages based on a user-defined DPI (default 72 DPI), which results in smaller file sizes.</li>
  <li>JPEG Quality Adjustment: Enables control over JPEG quality (0-100), allowing users to balance between file size and image quality.</li>
  <li>Flexible Output: Saves the compressed file as a new PDF, preserving the layout and structure while optimizing for size.</li>
  <li>Easy Customization: Parameters for DPI and JPEG quality allow users to tailor the compression level according to their needs.</li>
</ul>

### Technical Details: <br>
**Dependencies:** <br>
<ul>
  <li>PyMuPDF (fitz): For accessing and manipulating PDF file structure, extracting and replacing images on each page.</li>
  <li>Pillow (PIL): For image manipulation, resizing, and quality adjustment.</li>
</ul>

**Key Parameters:** <br>
<ul>
  <li>dpi: Controls the resolution for image downscaling (default is 72 DPI; higher values result in less compression).</li>
  <li>quality: JPEG compression quality (default is 50, with 0 being lowest quality and 100 being maximum).</li>
</ul>

**Usage Example:** <br>
<ol>
  <li>Install dependencies with pip install pymupdf pillow.</li>
  <li>Run the compress_pdf function, specifying the input and output PDF paths, desired DPI, and quality.</li>
  <li>The output file will be significantly reduced in size, especially for image-heavy PDFs.</li>
</ol>

### Usage Example

To compress a PDF, use the following code:

```python
# Define paths and compression settings
input_pdf = "path/to/large_file.pdf"
output_pdf = "compressed_file.pdf"
desired_dpi = 72  # Lower DPI for higher compression
jpeg_quality = 50  # Lower quality for higher compression

# Compress the PDF
compress_pdf(input_pdf, output_pdf, dpi=desired_dpi, quality=jpeg_quality)
```
