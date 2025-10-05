# Low-Latency Architecture


## Useful Information

- **Download Android App**: [Download APK](https://raw.githubusercontent.com/archiGrad/Bartlett_ws_2025/main/app-debug.apk)
- **Discord Server**: https://discord.gg/Zy6Uk3nf
- **Contact**: putteneersjoris@gmail.com

---

## Synopsis
In this workshop, we will design a state-of-the-art parasitic edge-compute cluster in London through the lens of an architect.

---


## Introduction

The most significant architectural typologies in the world are now almost entirely empty of people, forming perhaps the largest cultural landscape in human history. If we follow every fiber-optic cable across the world, we would end up in unfamiliar places like these: autonomous server farms, power plants, fog nodes, AI superclusters, edge computing facilities, transmission hubs, and data centers.

One such facility is currently being constructed in Waltham Cross, north of London, home to Google. This new £5 billion investment in an AI supercluster contains 1.77 petabytes of shared memory and is estimated to generate five times the CO2 emissions of Birmingham's airport.

Like many others under construction, this building holds extraordinary meaning, sitting at the core of what it means to exist today, yet it turns its back on any expression of that significance. At first glance, there appears to be little architecture here. No grand monumental gesture, just row upon row of identical floor-to-ceiling frames for future server stacks, spinning and writing the lives of millions of global users while being controlled by only a handful of engineers.

Every era has had its own iconic architectural typology. In medieval times, this was once the church; modernism had the factory and then the house. In the past decade, we celebrated the decadent museum and gallery. Now, we have data centers and computing facilities.

---

## The Datacenter

The geographical location of a compute cluster is critical, depending on its function. For applications requiring fast communication or support for high-speed transmission protocols, proximity to users is key.

If you are building for raw computation, such as AI learning and training clusters, it is essential that your facility has direct access to the electricity grid.

If you are optimizing for performance or efficiency, as with hyperscale facilities or data processing units, locating near water can be a viable strategy, as it provides the most cost-effective cooling solution.

For applications requiring fast communication, such as financial trading, real-time applications, autonomous vehicles, or traffic cameras, building in or near a city is preferable, as latency is closely correlated with user proximity.

This workshop will focus on the latter scenario. Our cities are increasingly mediated by cameras, automated traffic lights, autonomous vehicles, surveillance systems, while also supporting thousands of Facebook, Snapchat, and X requests every second. Additionally, our phones request vast amounts of information, further driving the need for low-latency infrastructure.

---

## Data and Its Politics

Since Edward Snowden's revelations, we know that government and intelligence agencies are actively harvesting most of our data at a vast scale. According to Google's privacy policy, this data includes, but is not limited to:

- Network connectivity + social graphs and relationships
- Biometric data, face scans, voice models, fingerprints, facial recognition
- Device usage, application usage, screen time
- Device information (hardware specs, OS version, installed apps)
- Purchase history and spending patterns
- All search history, incognito or not
- Gaze tracking
- Time spent, scroll patterns, shares/likes, engagement
- Bluetooth/WiFi network scanning for location
- Accelerometer/gyroscope data
- Device inputs like keyboard, mouse, USB
- Typing cadence
- GPS coordinates
- Current transport mode: Vehicle type, speed, direction, etc.
- Destination prediction
- Temperature, humidity, air quality, light levels
- Audio and video from Google Meet calls
- Spending patterns
- Click patterns
- Ambient audio recording
- Heart rate, blood pressure, body temperature, sleep patterns (if enabled on smartwatches)

Large tech corporations - Google, Alibaba, Amazon, Meta - (which still depend on advertisement as their main source of income), particularly have leveraged data collection and processing to increase revenue, disrupting existing products and services and inventing new ones from scratch. Nick Srnicek describes how platform-based businesses are increasingly monopolizing the global economy. What big tech platforms have in common is that they work as intermediaries between providers and customers, outsourcing costs and responsibilities and leveraging data for optimizing their mode of operation. The technologies that enable platform economy present themselves as neutral, light and invisible, using metaphors like the cloud, while in fact they have a vast impact on our physical environments.

As this data is used internally to increase model accuracy and trend prediction, this data can be intentionally or not, be leaked to the outside world. Even last month, in August 2025, a massive data breach was found of 2.5 billion Gmail users that was publicizing information of 2.5 billion Gmail accounts, which are still accessible through a broker on the dark web.

The sheer volume of digital information in the world is staggering, made only more so by the pace at which it's growing.

---

## Spatial Data

We now produce approximately the same amount of visual data per day as we did in the whole year of 1999. This growth is unprecedented. Digital storage space is seen as negligible; one terabyte of data can nowadays be stored in an area of 1 by 2 cm. But since upload volumes are too massive and copies are made along the way, combined with humanity's incapability to grasp big numbers, the major clouds are building roughly a football field's worth of datacenter space every few days to keep up with demand, with images, metadata, and telemetry data being the primary driver. This volume is not negligible, and we as architects should be at least partially responsible for these build volumes, which to this day, is not the case.

---

## The Edge-Compute Cluster

The question of why more centralized data centers are not located in cities largely stems from land scarcity, the difficulty of securing land, and political, economic, and technological requirements.

London's legislation, effective 2030, bans the production of gas-driven vehicles after that year, though hybrid cars can still be driven until 2035. As everyone will be charging their electric vehicles at the same times, the grid will already be overloaded. This presents an immense challenge, as data centers can sometimes consume up to 5% of a city's energy. Many cities' grids struggle to integrate this infrastructure, as they cannot accommodate such heavy power demands. Although projects are underway to address these changes, the success rate remains quite low. As computational demand in cities rises, attention is shifting to the fastest-growing segment in the sector: edge data centers.

In comparison, centralized data centers (hyperscalers) are usually located in or around cities and can typically house 10,000 racks with a capacity exceeding 80 megawatts (MW). Edge data centers, however, have a much smaller capacity, ranging from 500 kilowatts to 2 MW, and, as the name suggests, are located at the outer edge of networks. They bring computing capability geographically closer to users situated farther away, minimizing latency. In an era of data-intensive applications—including high-resolution 3D mapping, driverless cars, and various social media platforms—speed, connectivity, and reliability through ultra-low latency architecture are crucial to a city's success, whether we're meeting online, prompting ChatGPT, or streaming a film.

An edge compute node has different criteria than a data center. It produces a lighter load, is distributed, compliant, and should be more flexible regarding power supply, scalability, heating and cooling, and energy recovery. Being smaller and highly available, it should be contextually aligned with the city's ecology and climate while reducing computational latency. This will be our focus in this workshop.

The main function of an edge node is not to preserve or store data but to complete tasks and return results as quickly as possible. These machines' sole agenda is to improve connectivity and move packets of information across a wider network at higher density and speed.

---

## Workshop Overview

A custom mobile app will be compiled to enable students to measure "network congestion" and "device density," key indicators of computational load per area. The app simultaneously tracks location, phone orientation, direction, images, sound, Wi-Fi, Bluetooth, and packet latency to a London server.

Collected data from all students will be mapped to determine optimal edge compute cluster placement based on a latency heatmap. Additional metrics, such as computational volume (teraflops per cubic meter) and cluster functionality, can be derived.

Students will identify areas where computational demand exceeds or approaches infrastructure capacity and design parasitic or semi-parasitic edge computing solutions, incorporating innovative cooling, energy, maintenance, and security strategies.

---

## Collect

Students will walk around in London individually with the app, taking at least 25 images and 5 ambient sound recordings through the app. The longer the walk, the better. It can be in the park, with friends, using multiple transportation modes, etc. Different sections of London. focus on diverse routes (e.g., busy urban centers, quieter parks, or transport hubs) to capture a wide range of latency and device density patterns. This will enrich the heatmap and provide more nuanced results.

This data will all be sent over to a shared server that prepares the data for us.

Back in the studio, we will load in this data from the server through Houdini and visualize it, hopefully extracting some interesting geospatial extrapolations that make up a heatmap we can use to identify potential high-latency areas where we will allocate our edge node.

After this phase, we will have the parameters on which we can base our design.

An example could be: an 80 cubic meter edge compute node that controls the real-time traffic in the neighbourhood, attached to bridge X, that contains a passive cooling system and uses wind energy and piezoelectric materials to store energy. It recovers its heat so that there is no ice on the bridge in winter.

### Scientific Framework
Current research shows that "edge computing migrates cloud computing capacity to the edge of the network to reduce latency caused by congestion and long propagation distance.

### Deliverable
10-30 seconds of data visualisation and project description

---

## Expand

With the given requirements, we can start producing parasitic design variations on the given site that comply with those criteria in a speculative fashion. Some can be big, medium, or small; they should have a specific agenda.

Think about: different ways of cooling infrastructure, security, scale, relation to existing infrastructure, electric storage, ecology, climate, land scarcity, communication, energy, maintenance, attachment, privacy, distribution material, data encryption protocols. All should be taken into account in the design.

### Deliverable
20-40 second design animation including a detail drawing

---

## Schedule
| Session | Date | London Time | Bangkok Time | Type | Description | Deliverables |
|---------|------|-------------|--------------|------|-------------|--------------|
| **1st** | Wed Oct 1 | 9am-12pm, 1pm-4pm | 3pm-6pm, 7pm-10pm | Individual | Introduction (2min/student), presentation, app showcase (functionality, data backend, tech stack, Houdini visualization). Install Android app (Bluetooth/data ON). Map London route (groups of 2, touristic/architecture spots, sparse-dense gradient). Install: Houdini, Blender, After Effects | - |
| **2nd** | Thu Oct 2 | 9am-12pm, 1pm-4pm | 3pm-6pm, 7pm-10pm | Individual | Houdini map showcase, Houdini basics + exercises | - |
| **3rd** | Fri Oct 3 | 9am-12pm, 1pm-4pm | 3pm-6pm, 7pm-10pm | Group | Houdini basics + exercises. Tech stack overview, backend server demo, Python file download in Houdini. Form groups of 3-4, load map, pick location, download Google Maps 3D model | Location, function, volume |
| - | Sat Oct 4 | - | - | - | - | - |
| **4th** | Sun Oct 5 | 10am-12am | 4pm-6pm | Group | Download app/Houdini updates, verify SideFX Labs install, device filtering, flipbook render, display options setup, location selection | Drawings, sketches |
| - | Mon Oct 6 | - | - | - | - | - |
| **5th** | Tue Oct 7 | 1pm-3pm | 7pm-9pm | Group | Houdini renders, feedback, working session | - |
| **6th** | Wed Oct 8 | 9am-12pm, 1pm-4pm | 3pm-6pm, 7pm-10pm | Group | Feedback, working session | 3D model, first animation |
| **7th** | Thu Oct 9 | 9am-12pm, 1pm-4pm | 3pm-6pm, 7pm-10pm | Group | Working session | - |
| **8th** | Fri Oct 10 | 8am-9am, 9am+ | 2pm-3pm, 3pm+ | Group | Final presentations (12min video + 10min comments) | 12min video + 10min comments |

*Lunch break: 12pm-1pm London / 6pm-7pm Bangkok (6-hour sessions only)*

### Key Dates
- **Unit Presentation**: Monday, September 29th at 10:00 London time
- **Classes Begin**: Tuesday, September 30th
- **Final Presentations**: Friday, October 10th from 9:00 onwards London time

---

## Tools

- Android mobile phone (participating with an iPhone will be difficult; second-hand ones are relatively easy to acquire on Facebook Marketplace or second-hand shops)
- SideFX Houdini free version
- No programming experience required, but it is helpful
- Rhino or Blender
- Sketching and drawing tools

---

## Who Is This For

- Urban designers and architects who are technologically inclined
- Those interested in building custom data capturing and processing pipelines, and learning how to interpret and design with this information

---

## What You Will Learn in This Workshop

- Android app deployment basics (note: a large portion of the code will be provided, so you will not learn how to build and deploy an app from scratch, but it will give you a good start)
- Basics of server-side computing and small-to-medium-scale app deployment
- Basic UNIX interaction commands
- HTTPS communication protocol
- Basic understanding of Houdini and Python (again, a significant portion of the code will be provided, but the focus is on the workflow, which is tool-agnostic)
- What APIs are and how to interact with them through the Houdini interface
- How to visualize data in a meaningful way
- How to interpret this information and differentiate between useful and useless information
- Centralized and decentralized computing
- Metadata and telemetry data
- Edge computing
- Architectural design

---

## About

**Joris Putteneers** is an architect and software engineer, interested in speculating the anthroposcene through means of software, hardware and media technologies. His work has been exhibited at MomA New York, Londen design festival, Venice Biennale and multiple film festivals. He has been actively practicing as an architect and software engineer since 2017 where he develops solutions in building design, robotics, application development and embedded system engineering. Currently based in Bangkok.

---

## References

1. M. Karels, "Data center power requirements and grid infrastructure limitations," *Energy Infrastructure Review*, vol. 15, no. 3, pp. 45-62, 2024.
2. Deloitte, "Can US infrastructure keep up with the AI economy?" *Infrastructure Analysis Report*, 2024.
3. JLL, "Why smaller data centers are taking off," *Global Real Estate Insights*, 2024. [Online]. Available: https://www.jll.com/en-us/insights/why-smaller-data-centers-are-taking-off
4. RMI, "Fast, Flexible Solutions for Data Centers," *Energy Transition Reports*, 2024.
5. D. Sanctis and P. Rossi, "LTE Signals for Device-Free Crowd Density Estimation Through CSI Secant Set and SVD," *IEEE Transactions on Wireless Communications*, vol. 18, no. 4, pp. 2463-2476, 2019.
6. M. Tilak et al., "Real-World Deployments of Participatory Sensing Applications: Current Trends and Future Directions," *International Scholarly Research Notices*, vol. 2013, Article ID 583165, 2013.
7. IBM, "What is an Edge Cluster?" *IBM Think Topics*, 2024. [Online]. Available: https://www.ibm.com/think/topics/edge-cluster
8. Y. Li et al., "Edge server placement in mobile edge computing," *Journal of Parallel and Distributed Computing*, vol. 116, pp. 130-144, 2018.
9. X. Chen et al., "An edge server placement based on graph clustering in mobile edge computing," *Scientific Reports*, vol. 14, Article 27225, 2024.
10. H. Zhang et al., "Cost-Aware Placement Optimization of Edge Servers for IoT Services in Wireless Metropolitan Area Networks," *IEEE Access*, vol. 10, pp. 62298-62315, 2022.
11. Y. Pi et al., "Latency Imbalance Among Internet Load-Balanced Paths: A Cloud-Centric View," *Proceedings of the ACM on Measurement and Analysis of Computing Systems*, vol. 4, no. 2, Article 32, 2020.
12. Ultralytics, "FLOPs: Machine Learning Model Computational Complexity," *Technical Documentation*, 2024.
13. Data Center Frontier, "Immersion Cooling Meets Edge Computing," *Industry Report*, 2023.

