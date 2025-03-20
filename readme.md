# 🎨 Enhanced Chalk

**Enhanced Chalk** is a powerful extension of the [chalk](https://github.com/chalk/chalk) library, allowing you to use **predefined colors, dynamically register custom colors, and tint text** using RGB values.

---

## 📦 Installation

To install **Enhanced Chalk**, ensure you are using **your private Verdaccio registry**:

```sh
npm install @yourusername/enhanced-chalk --registry http://localhost:4873
```

Or, if publishing to npm:
```sh
npm install @yourusername/enhanced-chalk
```

---

## 🚀 Usage

### **1️⃣ Importing the Library**
```js
import enhancedChalk from '@yourusername/enhanced-chalk';
```

### **2️⃣ Using Predefined Colors**
Your package includes a set of predefined **named colors** from `colors.js`. Example usage:

```js
console.log(enhancedChalk.orange("This is orange!"));
console.log(enhancedChalk.teal("This is teal!"));
console.log(enhancedChalk.gold("This is gold!"));
```

---

### 🎨 **Available Colors by Category**

| **Reds & Pinks**   | **Blues**       | **Greens**       | **Yellows & Browns** |
|--------------------|----------------|-----------------|----------------------|
| Crimson (220,20,60) | Sapphire (15,82,186) | Lime (50,205,50) | Gold (255,215,0) |
| Ruby (224,17,95)   | SkyBlue (135,206,235) | Olive (107,142,35) | Amber (255,191,0) |
| Rose (255,0,127)   | SteelBlue (70,130,180) | Mint (189,252,201) | Mustard (255,219,88) |
| Fuchsia (255,0,255) | Periwinkle (204,204,255) | Chartreuse (127,255,0) | Khaki (240,230,140) |

| **Purples & Violets** | **Oranges & Coral** | **Neutrals & Others** |
|----------------------|---------------------|---------------------|
| Indigo (75,0,130)  | Orange (255,165,0) | Beige (245,245,220) |
| Violet (138,43,226) | Coral (255,127,80) | Sepia (112,66,20) |
| Lavender (230,230,250) | Salmon (250,128,114) | Ivory (255,255,240) |
| Plum (221,160,221) | Peach (255,218,185) | Mahogany (192,64,0) |

---

### **3️⃣ Tinting Text with RGB Colors**
Use the `tint()` function to apply a custom RGB color:

```js
console.log(enhancedChalk.tint(255, 165, 0, "This is orange!"));
```

---

### **4️⃣ Registering a Custom Color**
Define your own colors dynamically using `registerColor(name, r, g, b)`. Example:

```js
enhancedChalk.registerColor("neonPurple", 153, 50, 204);
console.log(enhancedChalk.neonPurple("This is neon purple!"));
```

---

### **5️⃣ Retrieving a Custom Color**
Once registered, you can retrieve colors dynamically:

```js
console.log(enhancedChalk.getColor("neonPurple", "This is also neon purple!"));
```

If the color doesn’t exist, it will return a gray **"Color not found"** message.

---

### **6️⃣ Displaying All Available Colors**
To print all registered colors:

```js
console.log(enhancedChalk.toString());
```

This will return a list of all **predefined and custom colors**.

---

## 📜 License
MIT License. Feel free to contribute and improve!

---

## ⭐ Contributions
Want to add more features? Fork the repository and submit a pull request!

---

## 🛠️ Troubleshooting
- Ensure you're using Node.js **14+**.
- If colors aren't displaying correctly, check your terminal settings (ANSI support).

🚀 **Happy coding with Enhanced Chalk!** 🎨