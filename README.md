# Cube2Equirect

A web-based tool for converting cubemap images to equirectangular panoramic format. Transform 6-face cube maps into 360° panoramas with support for resolutions up to 8K.

## Features

- 🎯 **Drag & Drop Interface** - Easy upload for all six cubemap faces
- 📐 **Multiple Resolutions** - Support for 1K, 2K, 4K, and 8K output
- ⚡ **Real-time Conversion** - Fast client-side processing using HTML5 Canvas
- 💾 **Direct Download** - Export panoramas as PNG images
- 🎨 **Minimalist Design** - Clean, dark theme interface

## Usage

1. **Open the Tool**
   - Open `index.html` in your browser
   - Or visit the live site (if hosted on GitHub Pages)

2. **Upload Cubemap Faces**
   - Click on each face panel or drag & drop images
   - Required faces: Front (+Z), Back (-Z), Left (-X), Right (+X), Top (+Y), Bottom (-Y)
   - All faces should be the same resolution for best results

3. **Select Output Resolution**
   - Choose from preset options (1K to 8K)
   - Higher resolutions provide better quality but take longer to process

4. **Convert & Download**
   - Click "Convert" to generate the equirectangular panorama
   - Download the result as a PNG file

## Technical Details

The converter uses spherical coordinate mapping to transform cube face pixels into a continuous equirectangular projection. This format is compatible with:

- 360° image viewers
- VR applications
- Panoramic video platforms
- 3D rendering software

### Algorithm

The conversion process:
1. Maps each pixel in the equirectangular output to spherical coordinates (θ, φ)
2. Converts spherical coordinates to 3D cartesian coordinates on a unit sphere
3. Determines which cube face contains the corresponding pixel
4. Samples the color from the appropriate face using UV coordinates
5. Writes the sampled color to the output image

## Browser Compatibility

Works on all modern browsers that support:
- HTML5 Canvas API
- File API
- ES6 JavaScript

Tested on:
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Acknowledgments

Built with vanilla JavaScript and HTML5 Canvas for maximum compatibility and performance.