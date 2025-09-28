
# Smart Yard Management System - Documentation

## Table of Contents

1. [System Overview](#system-overview)
2. [Dashboard Features](#dashboard-features)
3. [Live Map Visualization](#live-map-visualization)
4. [Trailer Management](#trailer-management)
5. [Yard Truck Operations](#yard-truck-operations)
6. [Warehouse Door Management](#warehouse-door-management)
7. [Parking Management](#parking-management)
8. [Driver Management](#driver-management)
9. [Outside Trailers](#outside-trailers)
10. [Analytics & Reporting](#analytics--reporting)
11. [Activity Logging](#activity-logging)
12. [Real-time Features](#real-time-features)
13. [User Interface Components](#user-interface-components)
14. [API & Data Management](#api--data-management)

---

## System Overview

The Smart Yard Management System is a comprehensive solution for managing yard operations, trailer movements, and fleet coordination. It provides real-time visualization, automated routing, and efficient resource allocation.

### Core Features
- **Real-time yard visualization** with live trailer tracking
- **Automated task assignment** for yard trucks and drivers
- **Intelligent parking management** with 120+ designated spots
- **Warehouse door coordination** with queue management
- **Analytics dashboard** with performance metrics
- **Activity logging** for compliance and optimization

---

## Dashboard Features

### Main Dashboard (`/`)
The primary control center providing:

#### Status Overview Cards
- **Total Trailers**: Complete count of trailers in the system
- **In Motion**: Trailers currently being moved by yard trucks
- **Outside Yard**: Trailers waiting at gates for entry
- **Door Utilization**: Percentage of warehouse doors currently occupied

#### Real-time Simulation Controls
- **Start/Stop Simulation**: Toggle real-time movement simulation
- **Reset Simulation**: Return all entities to initial positions
- **Real-time Updates Toggle**: Control live data refresh

#### Tabbed Interface
- **Yard Map - Live View**: Interactive canvas with trailer positions
- **Outside Trailers**: Management of trailers awaiting entry
- **Parking Management**: Control of 120+ parking spots across 7 lots
- **Yard Trucks**: Fleet management for 14 yard trucks
- **Warehouse Doors**: Status and queue management for 10 doors

---

## Live Map Visualization

### Interactive Canvas Features

#### Trailer Visualization
- **Color-coded status indicators**:
  - 🔴 **Red**: Parked trailers
  - 🟠 **Orange**: Moving trailers
  - 🟢 **Green**: Loading/unloading trailers
  - ⚫ **Gray**: Outside trailers

#### Yard Truck Visualization
- **Diamond-shaped indicators** to distinguish from trailers
- **Status colors**:
  - 🟢 **Green**: Active trucks
  - 🟡 **Yellow**: Idle trucks
  - 🔴 **Red**: Maintenance trucks
  - ⚫ **Gray**: Offline trucks

#### Interactive Features
- **Click Selection**: Select trailers and trucks for task assignment
- **Hover Tooltips**: Display detailed information on mouse hover
- **Path Visualization**: Show routes when hovering over active yard trucks
- **Destination Assignment**: Click-to-assign destinations for selected trailers

#### Parking Lot Layout
- **7 Named Parking Lots**:
  - **North Lot A (NA)**: Priority for incoming trailers
  - **North Lot B (NB)**: Standard parking
  - **Central East (CE)**: Express loading queue
  - **Central West (CW)**: Maintenance hold area
  - **South Lot A (SA)**: Overnight parking
  - **South Lot B (SB)**: Staging for departure
  - **Reserve Area (RA)**: Overflow and long-term storage

#### Warehouse Doors
- **10 Loading/Unloading Doors** (D1-D10)
- **Color-coded availability**:
  - 🟢 **Green**: Available
  - 🟠 **Orange**: Occupied
  - 🔴 **Red**: Maintenance

---

## Trailer Management

### Trailer Lifecycle

#### Status Progression
1. **Outside Waiting**: Trailer at gate awaiting entry
2. **Entering**: Being brought in by road truck
3. **Parked**: Positioned in designated parking spot
4. **Moving to Warehouse**: En route to loading dock
5. **Loading**: Active loading/unloading operations
6. **Moving to Gate**: Departing to exit gate
7. **Exiting**: Being picked up by road truck
8. **Departed**: Left facility

#### Assignment Features
- **Destination Selection**: Choose from parking lots, warehouse doors, or gates
- **Driver Assignment**: Assign specific drivers to trailer movements
- **Priority Management**: Set priority levels (1-3) for urgent trailers
- **Notes & Instructions**: Add special handling instructions

#### Status Cards
Each trailer displays:
- **Current Location**: Real-time position
- **Assigned Truck**: Yard truck responsible for movement
- **ETA**: Estimated time to destination
- **Priority Level**: Urgency indicator
- **Last Updated**: Timestamp of last status change

---

## Yard Truck Operations

### Fleet Management (14 Trucks)

#### Truck Status Types
- **Idle**: Available for task assignment
- **Moving Empty**: Traveling without trailer
- **Moving with Trailer**: Transporting assigned trailer
- **Loading Trailer**: At warehouse door during operations
- **Maintenance**: Out of service for repairs

#### Assignment System
- **Quick Task Assignment**: Select truck, trailer, and destination
- **Automatic Routing**: System calculates optimal paths
- **Collision Avoidance**: 10-meter safety distance maintenance
- **Battery Monitoring**: Track electric truck battery levels

#### Operational Rules
- **Internal Movement Only**: Yard trucks cannot leave facility
- **Trailer Restrictions**: Can only move trailers already inside facility
- **Priority Task Handling**: Higher priority trailers processed first

---

## Warehouse Door Management

### Door Configuration (10 Doors)

#### Door Types
- **Loading Only**: Outbound shipments
- **Unloading Only**: Inbound shipments  
- **Both**: Flexible loading/unloading operations

#### Queue Management
- **Priority-based Queuing**: High-priority trailers advance
- **Wait Time Estimation**: Calculated based on current operations
- **Capacity Management**: Maximum trailers per door
- **Equipment Tracking**: Associated machinery and tools

#### Utilization Metrics
- **Daily Utilization Percentage**: Door usage efficiency
- **Throughput Tracking**: Trailers processed per hour
- **Maintenance Scheduling**: Preventive maintenance windows
- **Operating Hours**: Configurable operational timeframes

---

## Parking Management

### Parking Infrastructure (120 Spots)

#### Lot Organization
- **Grid Layout**: 12 spots per row, 10 rows total
- **Section Codes**: Two-letter identifiers (NA, NB, CE, CW, SA, SB, RA)
- **Spot Numbering**: Sequential numbering within each section
- **Coordinate System**: X,Y positioning for precise placement

#### Spot Status Management
- **Available**: Open for new trailer assignment
- **Occupied**: Currently housing a trailer
- **Reserved**: Held for specific incoming trailer
- **Maintenance**: Temporarily out of service

#### Features
- **Reservation System**: Pre-assign spots to incoming trailers
- **Expiration Management**: Automatic reservation timeout
- **Lot-specific Rules**: Different purposes for each parking area
- **Notes & Instructions**: Spot-specific handling information

---

## Driver Management

### Driver Database

#### Driver Information
- **Personal Details**: Name, email, phone contact
- **Shift Schedules**: Morning/Afternoon/Night assignments
- **Experience Levels**: Trainee, Junior, Senior, Expert
- **Certifications**: CDL types, equipment authorizations
- **Work Hours**: Daily hour tracking and limits

#### Status Management
- **Active**: Currently working and available
- **Break**: On scheduled break
- **Off Duty**: Not currently scheduled
- **Sick**: Unavailable due to illness
- **Vacation**: Scheduled time off

#### Assignment Features
- **Truck Assignment**: Link drivers to specific yard trucks
- **Task Tracking**: Monitor current driver activities
- **Performance Metrics**: Hours worked, tasks completed
- **Certification Verification**: Ensure proper qualifications

---

## Outside Trailers

### Gate Management

#### Trailer Queue
- **Arrival Tracking**: Timestamp and wait time monitoring
- **Priority Assignment**: Expedite critical shipments
- **ETA Management**: Estimated arrival times
- **Status Updates**: Waiting, arriving, delayed classifications

#### Admission Process
- **Location Pre-assignment**: Designate parking upon entry
- **Driver Coordination**: Ensure road truck compliance
- **Documentation**: Cargo type and special instructions
- **Queue Optimization**: Minimize wait times

#### Filtering & Management
- **Status Filters**: View by waiting, arriving, or delayed
- **Priority Filters**: Focus on high-priority shipments
- **Batch Operations**: Process multiple trailers efficiently

---

## Analytics & Reporting

### Performance Metrics

#### Operational KPIs
- **Average Wait Time**: Time trailers spend waiting
- **Average Dwell Time**: Total time in facility
- **Door Utilization**: Percentage of time doors are occupied
- **Truck Utilization**: Yard truck efficiency metrics
- **Throughput Rate**: Trailers processed per hour

#### Visual Analytics
- **Door Usage Charts**: Bar charts showing door performance
- **Hourly Throughput**: Line graphs of processing rates
- **Trend Analysis**: Performance changes over time
- **Alert System**: Notification of concerning metrics

#### Queue Analytics
- **Maximum Queue Length**: Peak congestion levels
- **Average Queue Length**: Typical waiting times
- **Queue Duration**: Time spent waiting in line

---

## Activity Logging

### Event Tracking

#### Logged Events
- **Trailer Movements**: All position changes and destinations
- **Status Changes**: Updates to trailer and truck statuses
- **Assignment Events**: Driver and truck assignments
- **Gate Operations**: Entry and exit activities
- **Loading Operations**: Start and completion of dock activities

#### Log Features
- **Timestamp Precision**: Exact time of each event
- **Entity Tracking**: Links events to specific trailers/trucks
- **Duration Calculation**: Time spent in each status
- **Search & Filter**: Find specific events quickly
- **Export Capability**: Generate reports for analysis

#### Compliance Support
- **Audit Trail**: Complete history of all operations
- **Duration Tracking**: Verify regulatory compliance
- **Exception Reporting**: Identify unusual patterns

---

## Real-time Features

### Live Updates

#### Simulation Engine
- **Movement Animation**: Smooth trailer position updates
- **Status Synchronization**: Real-time status changes
- **Collision Detection**: Prevent truck conflicts
- **Path Optimization**: Dynamic route calculation

#### Update Controls
- **Refresh Rate**: Configurable update frequency
- **Pause/Resume**: Control simulation flow
- **Reset Capability**: Return to initial state
- **Manual Override**: Force specific updates

#### WebSocket Integration
- **Live Data Streaming**: Continuous updates without refresh
- **Multi-user Synchronization**: Consistent views across users
- **Event Broadcasting**: Immediate notification of changes

---

## User Interface Components

### Design System

#### Component Library
- **shadcn/ui**: Accessible component foundation
- **Radix UI**: Primitive component building blocks
- **Tailwind CSS**: Utility-first styling system
- **Lucide Icons**: Consistent iconography

#### Responsive Design
- **Mobile Support**: Optimized for tablet/mobile use
- **Grid Layout**: Flexible responsive columns
- **Touch Interaction**: Mobile-friendly controls
- **Accessibility**: WCAG compliance standards

#### Theme Support
- **Dark/Light Mode**: User preference themes
- **Color Coding**: Consistent status indicators
- **Typography**: IBM Plex Sans font family
- **Spacing System**: Consistent margin/padding

---

## API & Data Management

### Data Architecture

#### State Management
- **React Query**: Server state caching and synchronization
- **Local State**: Component-level state with React hooks
- **Persistent Storage**: Browser localStorage for preferences

#### Mock Data System
- **Realistic Simulation**: 50 trailers, 14 trucks, 10 doors
- **Dynamic Updates**: Procedural status changes
- **Configurable Parameters**: Adjustable simulation settings

#### Future Integration
- **Database Ready**: PostgreSQL schema prepared
- **API Endpoints**: RESTful service architecture
- **Real Hardware**: IoT sensor integration capability

---

## Getting Started

### Development Setup
1. **Install Dependencies**: `npm install`
2. **Start Development**: `npm run dev`
3. **Access Application**: Navigate to development server URL

### Key File Locations
- **Main Application**: `client/src/App.tsx`
- **Dashboard**: `client/src/components/Dashboard.tsx`
- **Live Map**: `client/src/components/LiveMap.tsx`
- **Management Components**: `client/src/components/*Management.tsx`

### Configuration
- **Simulation Speed**: Adjustable in Dashboard controls
- **Data Refresh**: Configurable update intervals
- **Display Settings**: Theme and layout preferences

---

## Support & Maintenance

### Troubleshooting
- **Console Logging**: Detailed event logging for debugging
- **Error Boundaries**: Graceful error handling
- **Performance Monitoring**: Built-in performance tracking

### Future Enhancements
- **AI Routing**: Machine learning path optimization
- **Predictive Analytics**: Forecasting and capacity planning
- **Hardware Integration**: Real sensor and truck connectivity
- **Advanced Reporting**: Comprehensive business intelligence

---

*This documentation covers all major features and components of the Smart Yard Management System. For specific technical implementation details, refer to the source code in the respective component files.*
