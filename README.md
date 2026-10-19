# Hotel Booking System - UML Class Diagram

**Course:** UML Class Diagram Modelling Assignment - Kigali Independent University (ULK)
**Instructor:** Eric Maniraguha
**Group members:** Ahmed Ibrahim Ahmed (202512591) and Ahmed Elmotaz Fathi (202512126)
**Submission:** 20 October 2026

## Business idea
A hotel needs an information system to manage guests, rooms, room types, bookings and payments, replacing
paper registers that cause double bookings and lost records.

## Scope
**Covered:** guest records, rooms and room types, availability checks, creating/modifying/cancelling bookings,
payments and receipts, staff handling of check-in and check-out.
**Not covered:** a working application, online payment gateways, restaurant/spa/housekeeping, payroll,
accounting, multi-branch hotels. The project is a UML design exercise.

## Main classes
| Class | Responsibility |
|---|---|
| **Guest** | Stores guest details; creates, views and cancels bookings. |
| **Booking** | Central record of a reservation: dates, status and total cost. |
| **Room** | Represents a physical hotel room and its availability. |
| **Staff** | Hotel employee who processes bookings, check-in and check-out. |
| **Payment** | Records money paid for a booking and issues receipts/refunds. |
| **RoomType** | Category of room (Single, Double, Suite) with price and capacity. |

## Relationships
| Class A | Mult. | Relationship | Mult. | Class B | Type |
|---|---|---|---|---|---|
| Guest | 1 | makes | 0..* | Booking | Association |
| Booking | 0..* | reserves | 1 | Room | Association |
| Staff | 1 | handles | 0..* | Booking | Association |
| Booking | 1 | is paid by | 0..* | Payment | Composition |
| Room | 0..* | is of type | 1 | RoomType | Association |

## Diagram
![UML Class Diagram](diagrams/uml_class_diagram.png)

## Repository structure
```
uml-class-diagram-assignment/
├── README.md
├── documentation/
│   ├── report_1_project_description.pdf
│   └── report_2_uml_class_diagram.pdf
└── diagrams/
    ├── uml_class_diagram.drawio
    └── uml_class_diagram.png
```
The `.drawio` file can be opened and edited at https://app.diagrams.net.
