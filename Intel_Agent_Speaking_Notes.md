# Demo Fest: RC-INTEL IOC Enrichment Agent
**Presenter:** Dane Zielinski, Senior Detection Automation Engineer (DAE)

---

### **Slide 1: Title Slide – RC-INTEL IOC Enrichment Agent**
*   **Key Focus:** Introduction and setting the stage for the unified suite of agents.
> "Good afternoon, everyone. I’m **Dane Zielinski, a Senior Detection Automation Engineer on the DAE team.** I’m excited to kick off what will be a series of demos showcasing a **unified suite of specialized agents** we’ve been developing. Each of these agents is designed to build on the work of the last, creating a seamless flow of intelligence from ingestion to action.
> 
> We’re starting today with the RC-INTEL IOC Enrichment Agent. The core philosophy here is inclusivity—specifically, how we can better leverage **3rd-party intelligence** to round out the picture. While our internal telemetry is world-class, this agent fills a critical gap by providing the external reputation and context needed to make our detections truly comprehensive."

---

### **Slide 2: Problem Statement & Impact**
*   **Key Focus:** The volume vs. context gap.
> "To understand the 'Why,' looking at our current volume which is tracked in Splunk. We see thousands of matches monthly, but our escalation rate is hampered by a lack of immediate, external context. When an indicator arrives without its 'full context' attached, it creates a bottleneck where analysts have to pause and verify. This is where we lose the most time—in that initial gap between seeing a match and knowing its global reputation."

---

### **Slide 3: Current State – The "First Mile" Friction**
*   **Key Focus:** The fatigue caused by manual research.
> "Currently, our Detection Engineers spend a significant portion of their Intel investigations on 'pivot-heavy' research—jumping between various 3rd-party platforms to verify hashes or IPs. This manual process is the primary driver of our 'Time-to-Confidence' gap. We want to move away from manual lookups and move toward a model where the intelligence is already waiting for the engineer."

---

### **Slide 4: Customer and Operational Impacts (Current State)**
*   **Key Focus:** Consistency and customer trust.
> "The impact here is two-fold. Operationally, it’s difficult to maintain consistency when external research is done manually. For our customers, it means we sometimes provide broader guidance or vague situational findings. We want to tighten that loop and provide a high-fidelity narrative from the very first event."

---

### **Slide 5: Post-Transformation – The "Upstream Catalyst"**
*   **Key Focus:** Personal workflow anecdote and automating the "Detective Work."
> "If you look at these screenshots from our current portal, you see the reality we face every day. Often, an Intel profile gives us less than a single sentence of description with hopefully a external reference link. Even when we pivot to VirusTotal, it’s hit-or-miss. Many times, the hash isn't even in VT yet, leaving us with zero context.
> 
> **When I personally handle an Intel-based investigation, I’m not just looking at a detection count.** I’m diving into the **Community and Behavior sections of VT** to actually understand the 'How' and the 'Why.' I’m also spending significant time digging through our own **prior investigations** to see why an IOC was added and how a peer wrote it up prior.
> 
> That 'detective work' is vital, but it’s incredibly time-consuming. The RC-INTEL Agent transforms this by automating that deep-dive. It pulls that community sentiment, behavioral analysis, and historical context into the record 'at birth,' ensuring that when a Detection Engineer or Future Automation perfroms an investigation, the story is already told."

---

### **Slide 6: Customer and Operational Impacts (Post-Transformation)**
*   **Key Focus:** Speed and "Day Zero" confidence.
> "The result is what we call 'Day Zero' confidence. We’ve removed the need to go outside our platform to validate a threat’s reputation. For the customer, this translates to a faster, more precise response. They aren't just getting an alert; they’re getting an enriched profile that includes global context and investigation steps right out of the gate."

---

### **Slide 7: The Path Forward & Expected Outcome**
*   **Key Focus:** The "Intelligence Backbone" and future demos.
> "The path forward is about establishing this as our **Intelligence Backbone.** By bridging the gap between internal telemetry and 3rd-party data, we’re creating a more inclusive and powerful detection environment. This is the first step in a broader strategy to ensure our automation suite is as informed and as fast as the threats we're fighting."

---

### **Slide 8: Architecture – Under the Hood**
*   **Key Focus:** Technical efficiency and normalization.
> "On the technical side, we’ve focused on speed and reliability. We utilize local lookup tables to bypass the usual 3rd-party API bottlenecks, allowing for sub-millisecond bulk matching if we choose. We take that unstructured external data, normalize it into clean JSON, and in the future feed it directly into our detection pipeline. It’s about making 3rd-party intel a native part of our workflow."

---

### **Slide 9: LIVE DEMO TRANSITION**
*   **Key Focus:** Moving from theory to practice.
> "I’ve talked about the theory; now let’s look at the reality. I’m going to show you exactly how this looks in the live environment."

---

### **Slide 10: The Outcome – A Unified Approach**
*   **Key Focus:** Final summary and looking ahead.
> "To wrap up: we are establishing a new reality for Detection Engineering—one where the 'First Mile' of research is a solved problem. By rounding out our picture with automated 3rd-party intelligence, we're building a faster, more inclusive foundation for our entire team. Thank you for your time, and we look forward to showing you how the next agents in this suite will build on this foundation in our upcoming demos."
