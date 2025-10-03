# nasa-project.github.io

# NASA Design Project – Force Balance Wind Tunnel  

This project began with a simple idea: build a system that could measure lift and drag inside a wind tunnel. It grew into a collaboration that blended electrical engineering, mechanical design, and aerospace principles into one working prototype.  
---

## Choosing the Airfoil  

We selected the NACA 0015 airfoil. Its symmetrical design was an advantage, allowing for a pressure balance when the angle of attack changed. This meant that the lift produced was equal in both directions, giving us stability and a solid lift-to-drag ratio 


![Airfoil Profile](images/Screenshot 2025-10-02 at 10.29.49 PM.png)  

---

## Building the Force Balance  

The force balance itself used a double cantilever design. Much like a diving board, it was fixed on one end and free on the other. This structure reduced sensitivity to bending moments and allowed us to measure forces more accurately. With two load cells working in tandem, we created a dual-axis measurement system capable of detecting both lift and drag. We built the frame from PLA, a lightweight and inexpensive material that was easy to customize 

![Balance](images/Screenshot 2025-10-02 at 10.30.54 PM.png)  

---

## Running the Analysis  

Once the model was in place, we turned to load analysis. Our data showed that the average lift coefficient was 1.1412, while the average drag coefficient was 0.0576. These numbers confirmed that the NACA 0015 was a good fit for the tunnel conditions  

![Load analysis](/images/Screenshot 2025-10-02 at 10.34.23 PM.png)

---

## Coding and Integration  

The Arduino acted as the brain of the system. We used a set of libraries—Adafruit for display graphics, HX711 for the load cells, and others for input, storage, and communication. The load cells were calibrated with known weights, and their readings were continuously logged to a CSV file on an SD card. Each record included the run number, angle of attack, drag and lift forces, pressures, and fan frequency. At the same time, the data appeared in real-time on an OLED screen, giving us immediate feedback during experiments.

![Wiring Diagram](images/Screenshot 2025-10-02 at 10.32.07 PM.png)  

---

## Safety First  

Wind tunnels can be unforgiving, so we built safety into the system. If the fan exceeded 1400 RPM, or if either force balance read more than 10.45 lbs, the Arduino would trigger an emergency stop relay. This ensured the equipment stayed protected and the data remained reliable.

---

## Testing the System  

When everything came together, we ran tests in the tunnel. The balance captured forces as expected, logging them to the SD card and showing results on the OLED screen. Watching the system work was rewarding, but we also noticed areas to improve. The mounting plate needed to be more rigid. The vertical support could be streamlined to reduce drag. The SD card should create a new file for each run instead of overwriting old data. And recording RPM directly, rather than indirectly, would give us better insight.

![Graphs](images/Screenshot 2025-10-02 at 10.31.29 PM.png)  

---

## Reflections  

The project was more than just a technical build - it was an exercise in teamwork across disciplines. Our force balance told a story of collaboration, problem-solving, and the kind of learning that only happens when theory meets practice! 
