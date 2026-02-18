Laptop Request Catalog Item
Project Overview

The Laptop Request Catalog Item project is designed to simplify and automate the process of requesting laptops within an organization using ServiceNow. Instead of manual requests, employees can submit structured laptop requests through a dynamic and user-friendly Service Catalog form.

This solution improves efficiency, accuracy, and governance by introducing validations, UI policies, and update set management.

Problem Statement

In many organizations, laptop requests are handled manually, which often leads to:

Delays in processing

Incomplete or incorrect information

Lack of dynamic guidance for users

Poor tracking and governance

To overcome these challenges, a Service Catalog item with dynamic behavior and proper deployment control was required.

Objective

To design and implement a ServiceNow Service Catalog Item that:

Allows employees to request laptops easily

Uses dynamic fields for better user experience

Applies validations and UI policies

Supports governance using update sets

Enables migration across instances

Category

ServiceNow System Administration

Technologies & Skills Used

ServiceNow

UiPath (Conceptual Skill Reference)

Tanzu Application Service (Conceptual Skill Reference)

Implementation Steps
1. Create Local Update Set

Navigate to System Update Sets → Local Update Sets

Create a new update set named Laptop Request

Mark it as Current

2. Create Service Catalog Item

Navigate to Service Catalog → Maintain Items

Create a new catalog item:

Field	Value
Name	Laptop Request
Catalog	Service Catalog
Category	Hardware
Short Description	Use this item to request a new laptop
3. Add Variables

The following variables were created:

Laptop Model – Single Line Text

Justification – Multi Line Text

Additional Accessories – Checkbox

Accessories Details – Multi Line Text

4. Configure Catalog UI Policy

A UI Policy was created to control dynamic behavior:

Condition: When Additional Accessories is checked

Action:

Show Accessories Details

Make it Mandatory

5. Create UI Action (Reset Form)

A client-side UI Action was implemented on the Shopping Cart table to reset the form.

Functionality:

Clears all fields

Displays confirmation message

6. Export Update Set

Set update set state to Complete

Export as XML

7. Retrieve Update Set

In the target instance:

Import XML file

Preview Update Set

Commit Update Set

8. Testing

Verified that:

✔ Catalog item is visible
✔ Variables behave correctly
✔ UI policy works dynamically
✔ Mandatory rules apply
✔ Form reset action works

Key Features

Dynamic form behavior

Mandatory field enforcement

Clean user interface

Governance via update sets

Easy deployment across instances

Conclusion

The project successfully replaces a manual laptop request process with an automated and structured workflow using ServiceNow. It enhances:

User experience

Data accuracy

Processing speed

Instance governance

This implementation demonstrates how ServiceNow Service Catalog can streamline internal IT service requests efficiently.
