# 🖼️ CSS Image Gallery with Lightbox (HTML + CSS Only)

This project is a **responsive image gallery** built using only **HTML and CSS**, featuring a **lightbox-style popup** that allows users to view images in a larger format.  
It uses the **checkbox trick** (or alternatively the `:target` selector) — no JavaScript required!

---

## 🚀 Features

- 📷 Click any image to view it in a larger lightbox popup  
- 🧭 Simple, clean layout built with HTML & CSS only  
- 💡 Fully functional using the `checkbox` or `:target` pseudo-class  
- 🎨 Smooth transitions, hover effects, and responsive design  
- 🔒 No external libraries or JS dependencies required  
- ⚙️ Optional JavaScript version (for single reusable popup container)

---

## 📁 Project Structure

```

ImageGallery/
│
├── assets/
│   ├── Im (45).jpg
│   ├── Im (46).jpg
│   ├── Im (47).jpg
│   └── ...more images
│
├── Gallery.html          # Main HTML file
├── Gallery.css           # CSS for gallery & popup styling
└── README.md           # Project documentation (this file)

````

---

## 💻 How It Works

### ✅ CSS-Only (Checkbox Method)
Each image is wrapped inside a `<label>` linked to a hidden `<input type="checkbox">`.  
When the image is clicked:
1. The checkbox becomes checked (`:checked` selector triggers CSS).
2. The lightbox container’s opacity changes from `0 → 1`.
3. The corresponding image is displayed in full size.

### 🧩 Key Concept:
```css
#check:checked ~ #container {
  opacity: 1;
  pointer-events: auto;
}
````

### ⚠️ Limitation:

Using only CSS, **each image must have its own container** (or predefined section), since CSS cannot dynamically change the `src` attribute of an `<img>` tag.

---


## 🧩 Styling Highlights

* **Gallery Grid:** Uses `flex` for easy alignment and wrapping.
* **Hover Effect:** Slight zoom-in animation for interactivity.
* **Lightbox Overlay:** A fixed-position div covering the viewport with semi-transparent background.
* **Responsive Design:** Images scale proportionally within their container.

Example snippet:

```css
.gallery img {
  width: 200px;
  border-radius: 8px;
  transition: transform 0.3s ease;
}

.gallery img:hover {
  transform: scale(1.05);
}

#container {
  position: fixed;
  inset: 0;
  display: none;
  align-items: center;
  justify-content: center;
  background-color: rgba(0, 0, 0, 0.8);
}
```

---

## 🎨 Customization

You can easily adjust:

* Background color / opacity for the overlay
* Image transition duration
* Padding / margins between images
* Font style (currently uses [Poppins](https://fonts.google.com/specimen/Poppins))

---

## 🧰 Technologies Used

* **HTML5**
* **CSS3 (Flexbox + Pseudo-classes)**

---

## 🧪 Future Improvements

* Add keyboard navigation (Next / Previous)
* Add **JavaScript** (for single-popup version)
* Add smooth zoom and fade transitions
* Integrate lazy loading for performance optimization

---

## 📸 Preview

A simple representation of functionality:

| Action             | Result                          |
| ------------------ | ------------------------------- |
| Hover over image   | Slight zoom-in effect           |
| Click image        | Opens full-screen lightbox view |
| Click ❌ or outside | Closes lightbox                 |

---

## 🧑‍💻 Author

**Abhishek Verma**
Built with ❤️ using HTML & CSS only.

---

## 📄 License

This project is open-source and available under the **MIT License**.

```

---

Would you like me to tailor the README so it specifically documents **your exact HTML structure** (the one with the `#check` input and `#container` div that changes opacity)?  
That would make it a perfect match to your codebase.
```
