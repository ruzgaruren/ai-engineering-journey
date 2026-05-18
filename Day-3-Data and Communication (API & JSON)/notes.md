Day 3 — Data & Communication (API & JSON)

Modern AI systems are not just prompts and chatbots.
They are networks of APIs, JSON, servers, databases, and data flows communicating continuously.

The Big Picture

Today’s topic is actually:

“The day AI learns how to communicate with the internet.”

Modern AI systems do not work alone.

Real-world AI applications constantly:

fetch data
communicate with external services
process files
access databases
connect to payment systems
call other AI models
exchange structured information

And almost all of this communication happens through:

APIs + JSON + HTTP

This is where real AI Engineering begins.

The Transformation

Before:

AI User

After:

AI Systems Builder

You are moving from:

“Using AI tools”

to:

“Programmatically controlling intelligent systems.”

The Real Architecture of Modern AI Systems

Most beginners imagine AI like this:

User → ChatGPT → Answer

Reality is far more complex:

User
↓
Frontend (Web / Mobile App)
↓
API Request
↓
Backend Server
↓
Database
↓
LLM API (OpenAI / Claude / Gemini)
↓
JSON Response
↓
Frontend
↓
User

Modern AI applications are essentially:

Data Flow Systems
1 — What is an API?
API = Communication Layer Between Systems

API stands for:

Application Programming Interface

But the important part is not the definition.

The important part is the idea:

APIs allow software systems to communicate safely and predictably.

Real-World Analogy
Real World	Software World
Customer	Frontend
Waiter	API
Kitchen	Backend
Order	Request
Food	Response

The customer never enters the kitchen directly.

The API acts as the communication bridge.

Why APIs Matter

Without APIs:

mobile apps cannot communicate with servers
websites cannot fetch live data
payment systems cannot work
AI systems cannot access tools or databases
automation systems collapse

Modern internet infrastructure is built on APIs.

Modern AI infrastructure is built on:

API Orchestration
Request → Response Cycle

Almost all modern systems follow this pattern:

Client
↓
Request
↓
Server Processing
↓
Response
↓
Client Display
Example — Weather App

Request:

GET /weather?city=Silopi

Response:

{
  "city": "Silopi",
  "temperature": 31,
  "weather": "Sunny"
}

This is how most applications operate internally.

2 — REST APIs

REST is the dominant API architecture of the modern web.

REST APIs work through:

Endpoints + HTTP Methods + Responses
Endpoints

An endpoint is a specific API address.

Endpoint	Purpose
/users	User data
/products	Product data
/messages	Messaging system
/orders	Orders

Think of endpoints as:

Different doors leading to different resources.

HTTP Methods

HTTP methods describe intention.

Method	Purpose
GET	Retrieve data
POST	Send/Create data
PUT	Update data
DELETE	Remove data
GET Example
GET /users

Meaning:

“Fetch all users.”

POST Example
POST /users

Meaning:

“Create a new user.”

PUT Example
PUT /users/5

Meaning:

“Update user #5.”

DELETE Example
DELETE /users/5

Meaning:

“Delete user #5.”

The Critical Insight

HTTP methods are not random commands.

They communicate:

Intent

They tell the server:

what you want
what action should happen
why the request exists
3 — HTTP Status Codes

Every API response includes a status code.

Status codes tell you:

Whether the request succeeded or failed.

Essential Status Codes
Code	Meaning
200	Success
201	Resource Created
400	Bad Request
401	Unauthorized
403	Forbidden
404	Not Found
500	Internal Server Error
Real Engineering Starts Here

Beginners focus on:

Making code run

Professionals focus on:

Understanding failures

Debugging is one of the most important engineering skills.

Example
print(response.status_code)

If the result is:

404

It means:

The requested endpoint does not exist.

401 vs 403
401 Unauthorized
Authentication failed

You are not verified.

403 Forbidden
Permission denied

You are authenticated but not allowed.

404 vs 500
404

Problem is usually on the client side.

500

Problem is usually on the server side.

The server crashed internally.

4 — Headers

Headers contain metadata about the request.

Examples:

Authorization
Content-Type
User-Agent
Accept
Authorization Header

One of the most important headers:

Authorization: Bearer API_KEY

Used in:

OpenAI API
GitHub API
Stripe API
Anthropic API
Bearer Tokens

Bearer tokens tell the server:

“This requester has permission.”

They act as digital credentials.

Content-Type Header
Content-Type: application/json

Meaning:

“The data being sent is JSON.”

5 — Webhooks
Traditional API Flow

Normally systems repeatedly ask:

"Any updates?"
"Any updates?"
"Any updates?"

This is called:

Polling
Webhook Flow

Instead of asking repeatedly:

The server automatically notifies you.

Example:

"New payment received."
Why Webhooks Matter

Webhooks are:

faster
event-driven
more efficient
resource-friendly
Event-Driven Systems

Webhook systems activate when events happen.

Examples:

payment completed
user registered
GitHub push triggered
AI task finished
PDF uploaded
AI Workflow Example
User uploads PDF
↓
Webhook triggers
↓
AI summarizes document
↓
Result sent back to user

This is how many automation systems work internally.

6 — JSON
JSON = The Language of Modern AI Systems

JSON stands for:

JavaScript Object Notation

But practically:

JSON is a structured data format for communication.

Why JSON Dominates

JSON is:

lightweight
human-readable
machine-readable
easy to parse
API-friendly
standardized
Basic JSON Structure
{
  "key": "value"
}
JSON = Key → Value

Everything in JSON is built around:

Key → Value relationships
JSON Data Types
String
{
  "name": "Ruzgar"
}
Number
{
  "age": 22
}
Boolean
{
  "is_student": true
}
Array
{
  "skills": ["Python", "AI", "API"]
}
Object
{
  "address": {
    "city": "Silopi",
    "country": "Turkey"
  }
}
Nested JSON

Real-world APIs are deeply nested.

Example:

{
  "user": {
    "name": "Ruzgar",
    "projects": [
      {
        "name": "AI Chatbot",
        "status": "active"
      }
    ]
  }
}
The Most Important JSON Skill

You must understand:

Which data exists at which level.

Because production API responses can become extremely large and complex.

Common JSON Errors
Missing Quotes

Wrong:

{
  name: "Ali"
}

Correct:

{
  "name": "Ali"
}
Trailing Comma

Wrong:

{
  "name": "Ali",
}

JSON syntax is strict.

Small mistakes break parsing.

7 — API Requests with Python
The requests Library

The most common Python HTTP library:

requests
Installation
!pip install requests

Usually pre-installed in Google Colab.

First GET Request
import requests

url = "https://jsonplaceholder.typicode.com/posts/1"

response = requests.get(url)

print(response.status_code)
print(response.text)
What Happens Internally?
Step 1 — Import Library
import requests

Loads the HTTP request system.

Step 2 — Define Endpoint
url = "https://jsonplaceholder.typicode.com/posts/1"

Specifies the API endpoint.

Step 3 — Send Request
response = requests.get(url)

Sends the GET request.

Step 4 — Inspect Status Code
print(response.status_code)

Checks whether the request succeeded.

Step 5 — Print Raw Response
print(response.text)

Displays raw response data.

JSON Parsing

Professional approach:

import requests

url = "https://jsonplaceholder.typicode.com/posts/1"

response = requests.get(url)

data = response.json()

print(data)
Critical Concept
response.json()

Converts:

JSON → Python Dictionary
Python Dictionary Example
user = {
    "name": "Ruzgar",
    "age": 22
}

Python dictionaries are structurally very similar to JSON.

Accessing Data
print(data["title"])

Retrieves the "title" field from the response.

POST Request Example
import requests

url = "https://jsonplaceholder.typicode.com/posts"

data = {
    "title": "AI Engineer Journey",
    "body": "Learning APIs and JSON",
    "userId": 1
}

response = requests.post(url, json=data)

print(response.status_code)
print(response.json())
What Happens Here?
Step 1 — Prepare Data
data = {
    "title": "AI Engineer Journey"
}
Step 2 — Send POST Request
requests.post(url, json=data)
Step 3 — Server Processes Request

The backend receives and handles the data.

Step 4 — Response Returned

Usually something like:

{
  "id": 101,
  "title": "AI Engineer Journey"
}
The Core Pattern of Modern AI Systems

Most AI systems fundamentally work like this:

Send JSON
↓
Call API
↓
Receive JSON
↓
Process Data

This is the hidden infrastructure behind modern AI.

OpenAI API Logic

Even OpenAI APIs work exactly like this.

You send:

{
  "model": "gpt-5",
  "messages": [
    {
      "role": "user",
      "content": "Hello"
    }
  ]
}

And receive structured JSON responses.

Final Insight

Modern AI Engineering is not only about prompts.

It is about:

Communication
↓
Orchestration
↓
Data Flow
↓
Automation
↓
System Integration
Core Principle
Modern AI Engineering =
LLMs + APIs + JSON + Data Flow

Once you deeply understand this:

you stop being someone who merely uses AI,

and start becoming someone who builds intelligent systems.
