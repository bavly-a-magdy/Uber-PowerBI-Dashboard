// =============================================
// UBER DASHBOARD - DAX MEASURES & CALCULATIONS
// =============================================

// --- Key Performance Indicators (KPIs) ---

Total Bookings = 
COUNT('Uber_Dataset'[Booking ID])

Completed Bookings = 
CALCULATE(
    COUNT('Uber_Dataset'[Booking ID]),
    'Uber_Dataset'[Booking Status] = "Completed"
)

Lost Bookings = 
CALCULATE(
    COUNT('Uber_Dataset'[Booking ID]),
    'Uber_Dataset'[Booking Status] <> "Completed"
)

Total Revenue = 
SUM('Uber_Dataset'[Booking Value])

Average Revenue per Booking = 
AVERAGEX(
    FILTER('Uber_Dataset', 'Uber_Dataset'[Booking Status] = "Completed"),
    'Uber_Dataset'[Booking Value]
)

Total Distance Traveled (Miles/KM) = 
SUM('Uber_Dataset'[Ride Distance])

// --- Cancellation & Lost Rates ---

Lost Booking Rate = 
DIVIDE([Lost Bookings], [Total Bookings], 0)

Driver Cancellation Rate = 
DIVIDE(
    CALCULATE([Total Bookings], 'Uber_Dataset'[Booking Status] = "Cancelled by Driver"),
    [Lost Bookings],
    0
)

Customer Cancellation Rate = 
DIVIDE(
    CALCULATE([Total Bookings], 'Uber_Dataset'[Booking Status] = "Cancelled by Customer"),
    [Lost Bookings],
    0
)

// --- Satisfaction Ratings ---

Average Customer Rating = 
AVERAGE('Uber_Dataset'[Customer Rating])

Average Driver Rating = 
AVERAGE('Uber_Dataset'[Driver Ratings])