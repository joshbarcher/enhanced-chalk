# 🎨 Enhanced Chalk

**Enhanced Chalk** is a powerful extension of the [chalk](https://github.com/chalk/chalk) library, allowing you to use **predefined colors, dynamically register custom colors, and tint text** using RGB values.

---

## 📦 Installation

To install **Enhanced Chalk**, ensure you are using **your private Verdaccio registry**:

```sh
npm install @yourusername/enhanced-chalk
```

## 🚀 Usage

### **1️⃣ Importing the Library**
```js
import chalk from '@yourusername/enhanced-chalk';
```

### **2️⃣ Using Predefined Colors**
Your package includes a set of predefined **named colors** from `colors.js`. Example usage:

```js
console.log(chalk.orange("This is orange!"));
console.log(chalk.teal("This is teal!"));
console.log(chalk.gold("This is gold!"));
```

---

### 🎨 **Available Colors by Category**

| **Oranges & Yellows** | **Reds & Pinks** | **Blues** | **Greens** | **Purples** | **Neutrals & Others** |
|----------------|----------------|--------------|--------------|--------------|----------------|
| Orange (255,165,0) | Crimson (220,20,60) | SkyBlue (135,206,235) | Lime (50,205,50) | Indigo (75,0,130) | Brown (139,69,19) |
| Gold (255,215,0) | Ruby (224,17,95) | Teal (0,128,128) | Chartreuse (127,255,0) | Violet (138,43,226) | Beige (245,245,220) |
| Amber (255,191,0) | Cinnabar (227,66,52) | Turquoise (64,224,208) | Emerald (80,200,120) | Lavender (230,230,250) | Ivory (255,255,240) |
| Sunflower (255,204,0) | Persimmon (236,88,0) | Sapphire (15,82,186) | Jade (0,168,107) | Plum (221,160,221) | Almond (239,222,205) |
| Mustard (255,219,88) | Vermilion (227,66,52) | SteelBlue (70,130,180) | Fern (79,121,66) | Periwinkle (204,204,255) | Apricot (251,206,177) |
| Khaki (240,230,140) | Watermelon (242,71,63) | SapphireBlue (0,103,165) | MossGreen (138,154,91) | Fuchsia (255,0,255) | Eggshell (240,234,214) |
| | PersianRed (204,51,51) | Cobalt (0,71,171) | | Lilac (200,162,200) | Wheat (245,222,179) |
| | Pink (255,105,180) | PacificBlue (28,169,201) | | Orchid (218,112,214) | Flax (238,220,130) |
| | Rose (255,0,127) | Denim (21,96,189) | | Wisteria (201,160,220) | Khaki (240,230,140) |
| | CarnationPink (255,166,201) | PersianBlue (28,57,187) | | Amethyst (153,102,204) | Sepia (112,66,20) |
| | DustyRose (201,99,117) | Cerulean (0,123,167) | | Mauve (224,176,255) | Mahogany (192,64,0) |
| | Boysenberry (135,50,96) | MidnightBlue (25,25,112) | | Heliotrope (223,115,255) | Maroon (128,0,0) |
| | DeepRed (180,0,0) | SteelBlue (70,130,180) | | | Terracotta (204,102,102) |
| | | Onyx (53,56,57) | | | Coffee (111,78,55) |

---

### **3️⃣ Tinting Text with RGB Colors**
Use the `tint()` function to apply a custom RGB color:

```js
console.log(chalk.tint(255, 165, 0, "This is orange!"));
```

---

### **4️⃣ Registering a Custom Color**
Define your own colors dynamically using `registerColor(name, r, g, b)`. Example:

```js
chalk.registerColor("neonPurple", 153, 50, 204);
console.log(chalk.neonPurple("This is neon purple!"));
```

---

### **5️⃣ Retrieving a Custom Color**
Once registered, you can retrieve colors dynamically:

```js
console.log(chalk.getColor("neonPurple", "This is also neon purple!"));
```

If the color doesn’t exist, it will return a gray **"Color not found"** message.

---

### **6️⃣ Displaying All Available Colors**
To print all registered colors:

```js
console.log(chalk.toString());
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
