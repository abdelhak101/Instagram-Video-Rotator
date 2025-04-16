# Instagram Video Rotator

Instagram Video Rotator is a lightweight Chrome extension that injects a button with a rotating icon under Instagram video elements. Clicking the button applies a CSS rotation animation to the video, giving it a smooth 360° spin.

## Features

- **Automatic Button Injection:**  
  The extension dynamically adds a rotation button below every video on Instagram, including content loaded dynamically after the initial page load.
  
- **Animated Rotation Effect:**  
  A CSS animation rotates the video 360° when the button is clicked.
  
- **Responsive Design:**  
  Designed with a simple, inline-flex button that fits naturally into Instagram's UI.

## Project Structure

instagram-video-rotator/
├── manifest.json       # Extension configuration file (Manifest V3)
├── content.js          # Content script that adds the button and handles the rotation effect
├── icons/
│   ├── icon16.png      # Extension icon (16x16)
│   ├── icon48.png      # Extension icon (48x48)
│   └── icon128.png     # Extension icon (128x128)
└── logo.svg            # SVG logo used for generating the PNG icons

## Installation

To install the extension in Chrome:

1. **Clone or Download the Repository:**  
   bash
   git clone https://github.com/yourusername/instagram-video-rotator.git
   
2. **Load the Extension in Chrome:**  
   - Open [chrome://extensions/](chrome://extensions/) in your browser.
   - Enable **Developer Mode** (toggle the switch in the upper right corner).
   - Click on **Load unpacked** and select the project folder (`instagram-video-rotator`).

3. **Test the Extension:**  
   Visit [Instagram](https://www.instagram.com) and navigate to a page containing videos. You should see a rotation button appear beneath each video.

## Usage

- **Button:**  
  The rotation button includes a built-in icon (an SVG image) that rotates when clicked.
  
- **Effect:**  
  Clicking the button adds a temporary CSS class to the video element that triggers a 360° rotation via a CSS keyframes animation. When the animation finishes, the class is removed so the effect can be re-triggered.

## Customization

- **Animation Duration:**  
  The CSS animation is set to run for 1 second by default. Feel free to adjust the duration in `content.js` by modifying the `animation` property within the `.rotate-effect` class.
  
- **Styling:**  
  You can modify the button styling (background color, border, etc.) directly within the injected CSS in the `content.js` file.

## Contributing

Contributions are welcome! Here’s how you can help:

1. Fork the repository.
2. Create your feature branch: `git checkout -b feature/YourFeature`
3. Commit your changes: `git commit -m 'Add Your Feature'`
4. Push to the branch: `git push origin feature/YourFeature`
5. Open a Pull Request.

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgments

- [Chrome Extensions Documentation](https://developer.chrome.com/docs/extensions/mv3/)
- Thanks to the developers and contributors of the open-source community for their inspiration and guidance.
