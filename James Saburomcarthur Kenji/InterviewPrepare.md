### "Tell us about your experience using CASMO and SIMULATE. What specific analyses have you performed with these tools?"

Over the past five years at GE Hitachi Nuclear Energy, I’ve worked with the CASMO5/SIMULATE5 suite for core physics analysis and digital system integration. My primary focus was on PWR core design and monitoring. I implemented a project to modernize a 1000 MWe PWR plant’s core monitoring system, where I developed and validated cross-section libraries using CASMO5 and used SIMULATE5 for nodal power distribution and core follow analyses.

One highlight was coupling SIMULATE5 predictions with the digital protection system to implement dynamic protection setpoints. This enhanced operational flexibility by 25% and improved safety margins. I also designed control rod optimization algorithms using SIMULATE5 data, which led to a 15% reduction in power distribution anomalies.

In addition, I developed automated workflows in Python to validate SIMULATE5 predictions against plant data, which helped improve core monitoring accuracy and saved significant analysis time.



### “Can you walk us through a core design project you led using SIMULATE?”

"Certainly. One of the key projects I led at GE Hitachi Nuclear Energy was the PWR core monitoring system upgrade for a 1000 MWe unit. The goal was to transition from an aging analog system to a modern digital platform that could leverage SIMULATE5 for real-time analysis and decision support.

I started by working with CASMO5 to generate multigroup cross-section libraries for the plant’s reload core. Then, using SIMULATE5, I performed core follow calculations, power distribution mapping, and thermal margin assessments. A critical part of the project involved integrating SIMULATE5 outputs with the plant's digital I&C system, allowing dynamic core behavior predictions to drive control and protection setpoints in real time.

One major challenge we faced was recurring power distribution anomalies during control rod maneuvering. I used SIMULATE5 to optimize rod patterns based on nodal predictions, which reduced those anomalies by 15%. We also built a Python-based tool to automate validation against plant measurements, improving monitoring accuracy by 40%.

The project improved system reliability by 35%, and the plant saved around $2M annually in maintenance by eliminating legacy hardware."


### “How do you validate the accuracy of your SIMULATE5 results?”

"Validation is a critical part of using SIMULATE5 effectively, especially when it's integrated into digital I&C systems. My approach involves cross-verification with plant operational data and benchmarking against measured parameters.

For example, in the core monitoring modernization project I led, I implemented an automated cross-validation framework between SIMULATE5 predictions and live plant measurements—such as axial power profiles, detector readings, and outlet temperatures—using Python and OSIsoft PI data. We flagged deviations exceeding a defined threshold and traced them to model assumptions or cross-section inaccuracies.

Additionally, I used CASMO5-generated nodal libraries with controlled variations to perform sensitivity studies, which helped refine the input parameters for SIMULATE5. This not only improved the fidelity of the model but also allowed early detection of anomalies in real-world conditions.

By validating SIMULATE5 against actual operating data over several cycles, we achieved a 40% improvement in prediction accuracy, which was essential for dynamic protection system integration."


### “Have you ever integrated SIMULATE5 with digital I&C systems or protection logic?”

"Yes, I’ve had direct experience integrating SIMULATE5 with digital instrumentation and control systems, particularly during a core monitoring and protection system modernization project at a 1000 MWe PWR plant.

The core of the project was to develop a dynamic interface between SIMULATE5 core predictions and the digital reactor protection system. I implemented a framework where SIMULATE5 would provide real-time predictions of nodal powers, axial offset, and critical safety parameters, which were then used to dynamically adjust protection setpoints based on actual core conditions.

This coupling allowed for more flexible operation, because the protection system could adapt to changing power distribution, instead of relying on fixed conservative limits. As a result, the plant saw an 8% improvement in operational efficiency while maintaining and even enhancing safety margins.

From a systems integration perspective, I worked with ControlLogix PLCs and Ovation DCS, ensuring that signal communication from SIMULATE5 was validated, redundant, and cybersecurity-compliant according to NEI 08-09.

This real-time coupling was a first-of-its-kind implementation at our site and required extensive testing, simulation, and licensing support to demonstrate to regulators that the dynamic setpoints maintained compliance with safety analysis limits."


### “How do you handle CASMO5 library generation for reload analysis?”

"In my recent role at GE Hitachi Nuclear Energy, I was responsible for generating CASMO5 multigroup cross-section libraries for reload core design and real-time monitoring with SIMULATE5.

The process started with defining the fuel assembly types, enrichment levels, burnable absorber configurations, and expected operational conditions such as temperature, boron concentration, and moderator density. I used CASMO5 to generate state-point libraries that captured a range of burnup and exposure conditions relevant to the operating cycle.

To ensure accuracy, I applied spectrum-weighted cross-section collapsing and generated the nodal data required by SIMULATE5, including diffusion coefficients, discontinuity factors, and assembly discontinuity factors (ADFs). I also used Python scripting to automate batch CASMO runs and post-process the outputs into SIMULATE-ready formats.

Before deployment, I conducted cross-validation using legacy libraries and performed sensitivity studies to examine the effects of minor perturbations in fuel composition and coolant parameters. This helped ensure consistency and stability in downstream SIMULATE5 power distribution predictions.

As part of our QA process, we documented the entire workflow in accordance with 10 CFR 50 Appendix B and NQA-1, and I collaborated closely with reactor physics, operations, and licensing teams to ensure the libraries were benchmarked against historical cycle data."

### “Tell me about a time you used SIMULATE5 for anomaly detection or transient prediction.”

"One of the most impactful applications I led involved using SIMULATE5 for real-time anomaly detection in the core monitoring system.

During a digital modernization effort at a 1000 MWe PWR, I developed an integrated system where SIMULATE5 was continuously updated with live plant data, allowing it to serve as a predictive model for expected core behavior. We used this to build a framework that compared predicted versus actual readings — including detector signals, outlet temperatures, and axial offsets.

To enhance this, I created an automated anomaly detection algorithm in Python that flagged deviations beyond predefined thresholds. These deviations were then ranked by severity and linked to potential root causes, such as failed sensors, control rod misalignments, or unexpected boron concentration shifts.

We identified and diagnosed a recurring minor anomaly in power peaking near the periphery, which had gone undetected using the legacy analog system. Once resolved, we saw a 15% reduction in power distribution anomalies, and the system was robust enough to flag potential issues before they affected reactor operation.

Later, we extended the framework using machine learning models trained on historical SIMULATE5 output to predict core behavior during transients, reducing engineering analysis turnaround by 70% during fast power maneuvers or equipment trips."