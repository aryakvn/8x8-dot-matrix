# 8×8 Dot Matrix HEX Generator

A simple, browser-based tool to design **8×8 dot-matrix patterns** using checkboxes and automatically convert them into **HEX values per row** — ideal for microcontrollers, AVR, Arduino, and LED matrix projects.

Repository: https://github.com/aryakvn/8x8-dot-matrix/

---

## Features

- Interactive **8×8 checkbox grid**
- Real-time conversion of each row to:
  - Binary (8-bit)
  - HEX (`0x00` – `0xFF`)
- No dependencies
- Runs completely **offline**
- Perfect for:
  - LED dot-matrix displays
  - Character/font design
  - Embedded C / Arduino projects

---

## Demo / Usage

1. Clone or download the repository:
    ```bash
      git clone https://github.com/aryakvn/8x8-dot-matrix.git
    ```

2. Open the HTML file in your browser:

   ```bash
   index.html
   ```

3. Click the checkboxes to design your pattern.

4. HEX values update automatically for each row.

---

## Output Format

Each row of the matrix is converted to:

* **Binary** (MSB → LSB)
* **HEX value**

Example row:

```
11110000 → 0xF0
```

---

## Example: Using Output in C / Arduino

```c
uint8_t pattern[8] = {
  0x18,
  0x24,
  0x42,
  0x7E,
  0x42,
  0x42,
  0x42,
  0x00
};
```

This format works well for:

* AVR
* Arduino
* ESP32 / ESP8266
* STM32 (with minor adaptation)

---

## Notes

* Bit order is **left-to-right**
* Row 0 corresponds to the **top row**
* Logic assumes **1 = LED ON**, **0 = LED OFF**
* You may need to invert bits depending on:

  * Common anode vs common cathode
  * Your driver IC (MAX7219, 74HC595, etc.)

---

## Possible Improvements

* Export as C array / Arduino sketch
* Column-wise HEX output
* Drag-to-draw support
* Invert bits option
* Save/load patterns

Pull requests and suggestions are welcome 🙂

---

## License

MIT License
Free to use, modify, and distribute.

---

## Author

**Arya Kavian**
GitHub: [https://github.com/aryakvn](https://github.com/aryakvn)

