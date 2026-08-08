# Data Dictionary: Uber Rides Dataset

| Field Name | Data Type | Description | Sample Values |
| :--- | :--- | :--- | :--- |
| `Date` | Date | Date of booking | `2025-09-22` |
| `Time` | Time | Timestamp of booking | `06:39:39` |
| `Booking ID` | String | Unique transaction ID | `T1984811` |
| `Booking Status` | String | Status of ride | `Completed`, `Cancelled by Driver` |
| `Customer ID` | String | Unique customer identifier | `C6701334` |
| `Vehicle Type` | String | Vehicle category | `Auto`, `Go Mini`, `Uber XL` |
| `Pickup Location` | String | Starting location | `Dilshad Garden`, `Udyog Vihar` |
| `Drop Location` | String | Destination location | `Qutub Minar`, `Saket` |
| `Cancelled Rides by Customer` | Float | Binary flag for customer cancellation | `1.0`, `NaN` |
| `Reason for cancelling by Customer` | String | Cause of customer cancellation | `Change of plans`, `Driver Not Moving` |
| `Cancelled Rides by Driver` | Float | Binary flag for driver cancellation | `1.0`, `NaN` |
| `Driver Cancellation Reason` | String | Cause of driver cancellation | `Personal & Car related issue` |
| `Incomplete Rides` | Float | Binary flag for incomplete trips | `1.0`, `NaN` |
| `Incomplete Rides Reason` | String | Cause for incomplete trip | `Vehicle breakdown` |
| `Booking Value` | Float | Fare amount | `557.49` |
| `Ride Distance` | Float | Trip distance | `15.2` |
| `Driver Ratings` | Float | Customer rating for driver (1-5) | `4.2` |
| `Customer Rating` | Float | Driver rating for customer (1-5) | `4.5` |
| `Payment Method` | String | Method of payment | `UPI`, `Cash`, `Credit Card` |
