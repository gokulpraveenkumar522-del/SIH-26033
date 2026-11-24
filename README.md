# Smart India Hackathon Workshop
# Date: 24-11-2026
## Reference Number: 26019369
## Name: GOKUL SP

## Problem Title
SIH 26033: Multiple intermediaries reduce farmers earnings and increase consumer prices.

## Problem Creater's Organization
Ministry of Consumer Affairs, Food & Public Distribution

## Theme
Agriculture, FoodTech & Rural Development

## Problem Description
Expected Solution: Create a digital marketplace that:

• Connects farmers/FPOs directly with consumers and bulk buyers.
• Provides logistics support.
• Uses AI for demand forecasting and route optimization.

## Benefits:

• Better prices for farmers.
• Lower prices for consumers.
• Reduced supply chain inefficiencies.

## Proposed Solution

1. Detailed explanation of the proposed solution

HarvestBridge connects farmers to buyers before the crop is harvested. Buyers commit to quantity and price ranges in advance, so farmers no longer have to accept whatever the local trader offers at harvest time.

Pre-harvest contract engine: Buyers (retailers, processors, institutional kitchens, exporters) post demand requests such as "20 tonnes of tomatoes, Grade A, delivery in 6 weeks". Farmers or FPOs accept them in groups, and the platform splits the quantity fairly among the members.
WhatsApp and IVR-first access: Farmers without a smartphone app habit can register, view offers, accept contracts and check payments through a WhatsApp chatbot or a toll-free voice call in their own language.
AI quality grading: The farmer photographs the produce, and an on-device vision model gives an instant grade (size, colour, defects). This reduces disputes at the buyer's end.
Village micro-hubs: Local entrepreneurs run small collection and weighing points with digital scales that sync automatically with the platform.
Warehouse receipt credit: Produce stored at a hub gets a digital receipt, which farmers can use to get a short-term loan instead of making a distress sale.
QR traceability: Every lot carries a QR code, so buyers can see the farm, harvest date and grade.

2. How it addresses the problem

Problem	How HarvestBridge addresses it
Farmers sell at harvest-time lows	Pre-harvest contracts lock in a price band before sowing or harvest
Middlemen control price information	Buyer demand and price ranges are visible to farmers in advance
Grading disputes reduce the price	Photo-based AI grading gives an objective, recorded grade
Small farmers can't reach bulk buyers	Group acceptance of contracts through FPOs and village hubs
Cash-flow pressure forces distress sales	Warehouse-receipt loans let farmers wait for a better price
Low smartphone and app literacy	WhatsApp bot and voice (IVR) access in regional languages

3. Innovation and uniqueness

Shifts the model from "list and sell" to "demand first, grow and supply second".
Works over WhatsApp and phone calls, so it does not depend on app adoption.
Combines contract farming, AI grading and credit in one flow.
Fair-share algorithm that divides large orders among small farmers by capacity and past reliability.
Reliability score for each farmer, which unlocks better contracts and lower loan rates over time.
End-to-end QR traceability that gives buyers confidence and earns a quality premium.
Technical Approach

1. Technologies to be used

Frontend: Flutter (lightweight farmer and hub-operator app), React.js (buyer and admin dashboard)
Messaging and voice: WhatsApp Business API, Twilio or Exotel for IVR, Bhashini for speech and translation
Backend: Python FastAPI with Celery for background jobs, REST APIs
Database: PostgreSQL with PostGIS (users, contracts, hubs, geo data), Redis (queues and caching), S3-compatible storage (images, receipts)
AI/ML: TensorFlow Lite with MobileNet or YOLO for produce grading, gradient boosting (XGBoost) for price-band prediction, a rule-based allocation engine for fair-share distribution
IoT: Bluetooth/Wi-Fi digital weighing scales at hubs
Payments and credit: UPI payouts, Account Aggregator framework for consent-based credit scoring, integration with an NBFC or bank partner for receipt-backed loans
Data sources: Agmarknet and e-NAM prices, IMD weather and rainfall data, crop-sowing data
Cloud and DevOps: Docker, Kubernetes, AWS or Azure, GitHub Actions
Security: OTP and Aadhaar-optional KYC, role-based access, audit logs, encryption at rest and in transit

2. Methodology and process for implementation

Field survey of farmers, hub operators and bulk buyers; collection of grading standards for selected crops.
Collection of produce images and training of the grading model for 2 to 3 crops.
Build the contract engine, allocation logic and WhatsApp/IVR flows.
Develop the hub-operator app and buyer dashboard.
Integrate weighing scales, UPI payouts and QR code generation.
Pilot in one block with one FPO and one institutional buyer.
Add warehouse-receipt credit, then expand to more crops and districts.

Process flow

Buyer posts demand: crop,grade, quantity, date
Platform matches nearbyFPOs and farmers
Farmers accept viaWhatsApp / IVR / app
Fair-share allocation amongfarmers
Harvest and photo-based AIgrading
Weighing and QR taggingat village hub
Pickup and delivery tobuyer
Buyer confirms quality andquantity
UPI payout to farmers
Reliability score updatedand credit unlocked

System architecture

WhatsApp Bot
API Gateway
IVR Voice Line
Farmer / Hub App
Buyer Dashboard
Contract and AllocationService
Grading Service: on-deviceand cloud models
Hub and Warehouse Service
Payment and Credit Service
PostgreSQL + PostGIS
Digital scales
Mandi, weather and sowingdata

Working prototype / screenshots: to be added here.

Feasibility and Viability

1. Analysis of the feasibility of the idea

Technical: WhatsApp APIs, image classification, UPI and geospatial databases are mature, and grading models can start with only a few crops.
Operational: Uses existing FPOs and local entrepreneurs as hub operators, so there is no need to build physical infrastructure from scratch.
Economic: Revenue from a small contract-facilitation fee, grading fees from buyers, hub service charges, and interest sharing on receipt-backed loans.
Social: Familiarity with WhatsApp and UPI in rural areas, together with FPO promotion schemes, supports adoption.

2. Potential challenges and risks

Contract defaults by buyers or farmers (side-selling when market prices rise)
Accuracy of AI grading under varied lighting and crop varieties
Weather or pest losses that prevent farmers from meeting commitments
Hub operator training and trust-building
Regulatory compliance for contract farming and lending
Initial shortage of committed buyers

3. Strategies for overcoming these challenges

Price bands with a floor and ceiling so both sides gain from fair pricing, plus penalties and reliability scores to discourage side-selling
Retrain the grading model continuously with field images, and allow a human re-check for disputed lots
Tolerance clauses for weather loss, and optional crop-insurance linkage
Local-language training and small incentives for hub operators
Partner with licensed NBFCs and follow the state APMC and model contract farming guidelines
Start with institutional buyers (hotel chains, school meal programmes, processors) who need steady supply
Impact and Benefits

1. Potential impact on the target audience

Farmers/FPOs: Price certainty before harvest, fewer distress sales, access to credit and bigger markets.
Buyers: Predictable supply, consistent quality and traceable sourcing.
Hub operators and youth: New rural entrepreneurship and employment.
Government and banks: Better data on sowing and supply, and safer lending backed by receipts.

2. Benefits of the solution

Economic: Higher and more stable farmer income, lower buyer procurement risk, and reduced dependence on informal moneylenders.
Social: Includes small and marginal farmers in organized markets, and builds digital and financial inclusion.
Environmental: Planned production reduces surplus and spoilage, and consolidated pickups lower transport emissions.
Supply chain efficiency: Fewer handoffs, objective grading and faster, traceable settlement.
Research and References
Agmarknet, mandi price and arrival data: https://agmarknet.gov.in
e-NAM (National Agriculture Market): https://enam.gov.in
Warehousing Development and Regulatory Authority (WDRA), e-NWR: https://wdra.gov.in
Account Aggregator framework (Sahamati): https://sahamati.org.in
Open Network for Digital Commerce (ONDC): https://ondc.org
TensorFlow Lite, on-device machine learning: https://www.tensorflow.org/lite
Bhashini, Indian language AI services: https://bhashini.gov.in
