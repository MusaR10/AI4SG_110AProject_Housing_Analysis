# AI4SG_110AProject_Housing_Analysis
Musa Rana and Minhtri Nguyen Housing Analysis Project. 

##The Problem and who it affects:

San Jose State University students who need off-campus housing often rely on short rental posts and photos. The system breaks down when a student cannot quickly tell whether a listing matches their actual needs, such as price, location, parking, roommate preference, cleanliness, safety, or building age.

This affects students searching near San Jose State University, especially renters with limited time, limited transportation, or strict budgets. A listing may look acceptable at first, but important details are scattered across text and images. 

They struggle to find a living space that meets their minimum needs and requirements, while also being within their budget. If they find a living space the right size, it may not have air conditioning, if they find one with both, it may not have a parking spot, meanwhile others who don't need a parking spot are paying a premium on their rent since it come with a parking lot and they could have found a living space that has similar amenities to their own while not having a parking spot and thus being cheaper. Additionally, when they have found a spot, they are quick to jump into a lease without even analysing other potential flaws they might not have noticed. The house could have numerous safety and sanitary concerns as well. Too often people overlook these problems and have to deal with these issues later. This problem affects masses of people, anyone looking to find a new living space may want to see whether or not any given space fits their needs, and may need a 3rd party unbiased eye who could point out other potential issues as well or highlight the best parts of a potential living space and give them advice on whether or not it is worth it. If they simply ask the salesman, they of course will try to sell them the home as they will make a profit.

##The AI capability used and why it fits:

This project uses Gemini 2.5 Flash for two lab-tested AI capabilities: Structured extraction from unstructured text and Image analysis of housing photos

This fits the problem because housing decisions require comparing written resident needs against visual evidence from a listing photo. In our lab output, Gemini successfully converted a resident’s written request into JSON fields and then evaluated the uploaded home image for safety, cleanliness, size, style, and fit. 

##Workflow

##Input:
The person looking for housing enters a housing request by letting the chatbot know what they are looking for, they will provide them with some details that are important to them such as budget, location, size, safety concerns, etc. 
The input I used:
“I need to rent a room near San Jose State University for under $1500 per month. It would be nice to have a room to myself and a parking spot, and I would not want it to be too old.”

##AI Step 1: Extract Requirements
Gemini converts the resident message into structured JSON. 

##Output: Structured Data
{
  "location": "data",
  "Price": "data",
  "Shared": "data",
  "Amenities": "data",
  "Safety": "data",
  "House mates?": "data",
  "Miscelanious": "data"
} 


Our Output in response to the inputs: 
![Workflow screenshot](images/image (1).png)



##Input: 
User Uploads an image of the potential living space
The input we provided:


AI Step 2: Image Analysis
Gemini Analyzes the the uploaded image and answers questions about Safety, Style, Rating, Cleansiness, Size, and Fit 

Output: 
Output of the analysis of the image, most importantly the rating of the house, its safety concerns, and whether or not the living space is a fit for the needs of the user.
Our Output:
--- Safety ---
Yes, there are several visible safety problems in this image, primarily related to neglect and poor maintenance:

1.  **Overgrown Vegetation (Severe Tripping Hazard & Pest Harborage):** The entire front yard is covered in very tall, dense weeds and grass.
    *   **Tripping Hazard:** This extensive growth completely obscures the ground, making it impossible to see uneven surfaces, holes, debris, or roots, posing a significant tripping hazard for anyone approaching the house.
    *   **Pest Harborage:** Such dense vegetation provides an ideal habitat for rodents (mice, rats), insects (ticks, mosquitoes, spiders), and potentially snakes, increasing the risk of bites, stings, and infestations.
    *   **Fire Hazard:** In dry conditions, this overgrown vegetation becomes highly flammable, increasing the risk of a brush fire spreading to the house or adjacent properties.
    *   **Security Risk:** It provides concealment for trespassers or unauthorized individuals approaching the property.

2.  **Deteriorated Driveway (Tripping Hazard):** The concrete or asphalt driveway leading to the garage and front door is visibly cracked, broken, and has weeds growing through the fissures.
    *   **Tripping Hazard:** The uneven surfaces, raised edges from cracking, and vegetation growth create numerous opportunities for trips and falls.

3.  **General Neglect (Indicator of Potential for Further Hazards):** The overall appearance of the property suggests it is either abandoned or very poorly maintained. This isn't a direct hazard itself, but it increases the likelihood of other, less immediately visible, safety concerns:
    *   **Structural Issues:** While not visible here, prolonged neglect often leads to deteriorated structural components (e.g., roof, foundation, porch supports) that could collapse.
    *   **Vandalism/Squatters:** Unoccupied and neglected properties are prone to vandalism, illegal dumping, and squatting, which can lead to unsafe conditions inside (e.g., fires, dangerous debris, lack of utilities).
    *   **Weathered Roof:** The roof shingles appear old and worn, which, while not a direct hazard currently visible, suggests potential for leaks and further deterioration over time, and could indicate a fragile surface if someone needed to access it.

The most immediate and directly visible safety concerns are the severe tripping hazards posed by the overgrown yard and the cracked driveway, along with the increased fire and pest risks from the vegetation.

--- Style ---
Based on the image:

1.  **Type of Home:** This is clearly a **single-family home**. It is a detached structure with its own yard and an attached garage, not part of a larger complex or building with multiple units.

2.  **Architectural Style:** The architectural style is best described as a **Ranch-style house** (or simply a Ranch house). Key characteristics that point to this include:
    *   **Single-story layout:** All living spaces are on one floor.
    *   **Low-pitched roof:** The roof has a gentle slope.
    *   **Long, linear, and often rambling footprint:** The house spreads out horizontally.
    *   **Attached garage:** Common with Ranch homes, integrated into the design.
    *   **Modest ornamentation:** Generally functional and less ornate than older styles.

This particular house appears to be a rather simple or "modest" example of a Ranch style, likely built sometime in the mid-20th century.

--- Rating ---
This home is **LOW tier**.

The property exhibits significant signs of disrepair and neglect, evidenced by the severely overgrown yard, cracked driveway, and a generally dated and unkempt exterior. Its basic ranch-style architecture, standard siding, and single-car garage lack any premium features or meticulous upkeep, placing it firmly at the lower end of the housing market.

--- Cleansiness ---
Based on the image:

*   **Clean and Tidy:** No, the home does not appear clean and tidy. The yard is severely overgrown with tall grass and weeds, obscuring the front of the house and the driveway. The driveway itself looks cracked and untended. The exterior of the house also shows signs of weathering and neglect.
*   **Modern or Old:** The house appears to be **old**. Its architectural style (a single-story ranch-style home with a low-pitched roof and traditional siding/windows) is characteristic of mid-20th-century construction (e.g., 1940s-1970s). It does not exhibit any features typically associated with modern architecture.

--- Size ---
The home appears **too large** for the requested living situation.

**Explanation:**
While the house, being a single-family dwelling, provides the desired "Shared: No" living situation and a "Parking spot" amenity, its overall size (a full house with an attached garage) would almost certainly make its rental price far exceed the "Less than $1500" requirement, especially in the high-cost-of-living area around San Jose State University. Therefore, from a practical and financial standpoint based on the complete resident requirements, it is too large.

--- Fit ---
This home is a **Poor Fit** for the resident's housing requirements.

Here's a breakdown of the comparison:

1.  **Location (San Jose State University):**
    *   **Fit:** Poor fit.
    *   **Explanation:** The image displays a standalone house in what appears to be a rural or neglected suburban setting, characterized by an extensively overgrown yard and surrounding trees. This visual does not align with the typical environment or housing options expected near an urban university campus like San Jose State University. There is no information in the image to suggest it is in San Jose.

2.  **Price (Less than $1500):**
    *   **Fit:** Cannot be determined.
    *   **Explanation:** The image provides no information regarding the price of the property.

3.  **Shared (No):**
    *   **Fit:** Partial fit.
    *   **Explanation:** This appears to be a single-family home. If rented as an entire unit, it would satisfy the "No Shared" requirement.

4.  **Amenities (Parking spot):**
    *   **Fit:** Good fit.
    *   **Explanation:** The house has an attached single-car garage and a visible driveway (though somewhat dilapidated and overgrown), clearly providing a parking spot.

5.  **Safety (Building age not too old):**
    *   **Fit:** Poor fit.
    *   **Explanation:** The house appears to be an older style, likely mid-20th century, with visible signs of neglect. The overgrown yard, weathered exterior, and overall disheveled appearance suggest poor maintenance and potential structural issues or general disrepair. While "not too old" is subjective, the visible condition of the house indicates it might be considered too old or, more critically, unsafe due to its apparent state of neglect.

6.  **House mates? / Miscelanious:**
    *   **Fit:** Not applicable.
    *   **Explanation:** These requirements are not specified, so no comparison can be made.

**Conclusion:**
Despite offering a parking spot and potentially being a non-shared unit, the overwhelming visual evidence points to a significant mismatch in **location** and serious concerns regarding the **safety and general condition** of the building due to its apparent age and severe neglect. These factors make it a poor fit for the stated requirements.





 Output: Additional Questions
Ask your own question about the image:

Our Input: 
Would it be safe fore me to raise a family? 

AI Step 3: 
Answers the question the user asks using gemini
Output:
--- Response ---
Based solely on the provided image, I would say **no, not as it currently appears.**

Here's why, and what would need to happen to make it safe for a family:

**Visible Concerns:**

1.  **Extreme Neglect:** The most obvious issue is the severely overgrown yard and driveway. This suggests the property has been vacant or poorly maintained for a long time.
    *   **Hazards:** Overgrowth can conceal trip hazards, broken glass, sharp objects, and attract pests like rodents, snakes, and ticks.
2.  **Exterior Condition:**
    *   **Roof:** The roof appears older and possibly worn, which could indicate leaks, water damage, and potential mold issues inside.
    *   **Siding and Trim:** The siding looks dated and the trim around windows/doors appears weathered, suggesting a lack of recent maintenance. This can lead to moisture intrusion and further deterioration.
    *   **Windows:** Some windows look old. Old windows are less energy-efficient and might not offer good security.
3.  **Overall Appearance:** The house has a general air of abandonment or severe disrepair.

**Inferred Concerns (Highly Likely in a house of this apparent condition and age):**

1.  **Lead Paint:** If built before 1978 (which its style suggests), it's highly likely to contain lead-based paint, a significant hazard, especially for young children who might ingest paint chips.
2.  **Asbestos:** Older homes often contain asbestos in materials like insulation, floor tiles, roofing, or textured ceilings. If disturbed during renovations, it can release dangerous fibers.
3.  **Mold and Mildew:** Given potential roof or window leaks and general neglect, mold growth is a high probability, which can cause respiratory issues and allergies.
4.  **Pest Infestations:** A neglected home with an overgrown yard is a magnet for rodents (mice, rats), insects (cockroaches, termites, carpenter ants), and other wildlife.
5.  **Outdated Electrical and Plumbing:** Older homes often have electrical systems that aren't up to modern code (e.g., knob and tube wiring, insufficient amperage) and plumbing systems that could have lead pipes, corroded pipes, or be prone to leaks. These are fire and water damage risks.
6.  **Structural Issues:** Prolonged neglect can lead to foundation problems, rotten wood (beams, subflooring), or other structural compromises that aren't immediately visible from the exterior.
7.  **Radon:** This naturally occurring radioactive gas can seep into homes and is a long-term health risk. It's not visible, but a possibility in any home and requires testing.
8.  **Security:** An apparently vacant and neglected home can be a target for vandalism, squatters, or break-ins.

**To make this house safe for a family, you would need to undertake a significant project, including:**

*   **Professional Inspections:** A comprehensive home inspection, including specialists for lead, asbestos, mold, structural integrity, electrical, plumbing, and HVAC.
*   **Hazard Remediation:** Safely remove or encapsulate lead paint and asbestos. Address any mold issues.
*   **Major Repairs/Renovations:** This would likely include a new roof, updated electrical and plumbing, potentially foundation work, new windows, and addressing any structural rot.
*   **Pest Control:** Eradicate any infestations.
*   **Extensive Cleaning:** Deep cleaning after renovations, especially for dust and potential contaminants.
*   **Yard Cleanup:** Clear all overgrowth, remove debris, and address any potential external hazards.
*   **Security Upgrades:** Ensure all doors and windows are secure.

In conclusion, while it *could* potentially become a safe home, it would require substantial financial investment, time, and professional expertise to address the numerous safety and health concerns that are either visible or highly probable. It is certainly not move-in ready for a family. 






Failure Case



The failure case lies in the image analysis section of our model. The first input provided by the user was, “I need a room or small studio in San Jose for under $1600 a month. Safety is very important to me, and I want to live in a very safe neighborhood near San Jose State University with parking and good public transportation.” After being given the structured extraction of all the requirements that was asked for, the uploaded picture was used as a reference. In our image-analysis test, the model described the uploaded property as appearing generally safe based on the well-maintained property, highlighting the exterior lighting around the house. This is a major flaw in the system, as the model has no real access to actual crime patterns/data. Variables like traffic risk, nighttime conditions, and even the area of the house are not accounted for. The problem is that factors like neighborhood safety cannot be confirmed solely from the image. Rather, there needs to be real data that the model can accurately base its output on.

Oversight Decision and Change

When the system makes a recommendation about the potential safety of a property, there should always be some sort of human review. As seen in the failure case, the AI fails to account for various factors that make up the safety of a potential property. Instead, the model bases its output on surface-level features that do not matter as much for safety. Although the AI can summarize requirements, organize them, and describe visual features from an image, human review is ultimately needed when using any output regarding safety. The main tradeoff for this is that requiring human review slows down the whole process and reduces the automation that AI is mostly used for. The main change that we can introduce to the system is to not allow our model to give a final safety judgement. Instead, the system should list what factors about the safety of the given property it can confirm and what it cannot. Although the model will sound less confident, the system ultimately becomes more honest about uncertainty and reduces the risk of false/invalidated confidence.
