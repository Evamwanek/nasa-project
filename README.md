# NASA Design Project – Force Balance Wind Tunnel  

This project began with a simple idea: build a system that could measure lift and drag inside a wind tunnel. It grew into a collaboration that blended electrical engineering, mechanical design, and aerospace principles into one working prototype.  
---

## Choosing the Airfoil  

We selected the NACA 0015 airfoil. Its symmetrical design was an advantage, allowing for a pressure balance when the angle of attack changed. This meant that the lift produced was equal in both directions, giving us stability and a solid lift-to-drag ratio 

<img width="263" height="336" alt="Screenshot 2025-10-02 at 10 29 49 PM" src="https://github.com/user-attachments/assets/9ed44491-9bf7-4965-8013-cd4c16a62c15" />

---

## Building the Force Balance  

The force balance itself used a double cantilever design. Much like a diving board, it was fixed on one end and free on the other. This structure reduced sensitivity to bending moments and allowed us to measure forces more accurately. With two load cells working in tandem, we created a dual-axis measurement system capable of detecting both lift and drag. We built the frame from PLA, a lightweight and inexpensive material that was easy to customize 

<img width="908" height="427" alt="Screenshot 2025-10-02 at 10 29 15 PM" src="https://github.com/user-attachments/assets/d2fa27fa-0f47-4da6-a444-39bae56e74bc" />

---

## Running the Analysis  

Once the model was in place, we turned to load analysis. Our data showed that the average lift coefficient was 1.1412, while the average drag coefficient was 0.0576. These numbers confirmed that the NACA 0015 was a good fit for the tunnel conditions  

<img width="564" height="405" alt="Screenshot 2025-10-02 at 10 34 23 PM" src="https://github.com/user-attachments/assets/ae5bdae2-a1ba-4de8-b590-ebb3e06a58bd" />


---

## Coding and Integration  

The Arduino acted as the brain of the system. We used a set of libraries—Adafruit for display graphics, HX711 for the load cells, and others for input, storage, and communication. The load cells were calibrated with known weights, and their readings were continuously logged to a CSV file on an SD card. Each record included the run number, angle of attack, drag and lift forces, pressures, and fan frequency. At the same time, the data appeared in real-time on an OLED screen, giving us immediate feedback during experiments.

<img width="794" height="437" alt="Screenshot 2025-10-02 at 10 32 07 PM" src="https://github.com/user-attachments/assets/15f9a306-4b19-48ad-9884-e66c1a847431" />


---

## Safety First  

Wind tunnels can be unforgiving, so we built safety into the system. If the fan exceeded 1400 RPM, or if either force balance read more than 10.45 lbs, the Arduino would trigger an emergency stop relay. This ensured the equipment stayed protected and the data remained reliable.

---

## Testing the System  

When everything came together, we ran tests in the tunnel. The balance captured forces as expected, logging them to the SD card and showing results on the OLED screen. Watching the system work was rewarding, but we also noticed areas to improve. The mounting plate needed to be more rigid. The vertical support could be streamlined to reduce drag. The SD card should create a new file for each run instead of overwriting old data. And recording RPM directly, rather than indirectly, would give us better insight.

<img width="964" height="190" alt="Screenshot 2025-10-02 at 10 31 29 PM" src="https://github.com/user-attachments/assets/7d463e5d-d762-4c28-a585-b0d0d4d8ca53" />

---

## Reflections  

This project really opened my eyes to cross-disciplinary work, and seeing how all the pieces came together was an amazing experience! I’m grateful I had the chance to work with such a strong team. 

Two big take aways for me were 1. In a team setting, over-communicating is almost always better than under-communicating. 2. It’s not just about thinking outside the box - it’s about finding the box.
