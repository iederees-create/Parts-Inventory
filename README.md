# Parts & Inventory Management System

A web-based application for managing electronic components and inventory tracking.

## Features

- **Part Management**
  - Register new parts with detailed specifications
  - Edit existing part information
  - View comprehensive part details
  - Bulk upload part images

- **Inventory Tracking**
  - Track stock levels across multiple locations
  - Set minimum levels and reorder points
  - Adjust stock quantities (add/remove/set)
  - View inventory history

- **Search & Filtering**
  - Global search across all part fields
  - Filter by SKU, category, supplier, and keywords
  - Quick view and edit functionality

- **Additional Features**
  - Part categorization
  - Manufacturer and supplier information
  - Technical specifications management
  - Document attachments (datasheets, CAD files)
  - Audit log for all changes

## Technologies Used

- **Frontend**: HTML5, CSS3, JavaScript
- **Data Storage**: Browser localStorage (for demo purposes)
- **Compatibility**: Modern browsers (Chrome, Firefox, Edge, Safari)

## Installation

No installation required for the demo version. Simply open the `index.html` file in any modern web browser.

For production use, you would need to:
1. Host the HTML file on a web server
2. Replace the localStorage data persistence with a proper backend database

## Usage

### Basic Navigation
- Use the main navigation menu to access different sections
- The Parts section is the main interface for managing components

### Managing Parts
1. **Viewing Parts**
   - The main table shows all registered parts
   - Click "View" to see detailed information
   - Use filters to narrow down the list

2. **Adding a New Part**
   - Click "Register New Part" button
   - Fill in all required fields
   - Add specifications and initial inventory
   - Upload images if available
   - Click "Save Part"

3. **Editing a Part**
   - From the parts list, click "Edit" on any part
   - Or, when viewing part details, click "Edit Part"
   - Make your changes and click "Save Changes"

### Inventory Management
1. **Viewing Inventory**
   - Navigate to the "Inventory" tab in part details
   - See current stock levels across all locations

2. **Adjusting Stock**
   - Click "Adjust Stock" from the inventory tab
   - Select location and action type
   - Enter quantity and optional notes
   - Click "Update Stock"

### Bulk Operations
- Use "Bulk Upload Images" to add multiple images at once
- Files should contain SKUs in their names for automatic matching

## Data Structure

The system stores parts with the following structure:
```javascript
{
  id: String,              // Unique identifier
  sku: String,             // Stock Keeping Unit
  name: String,            // Part name
  manufacturer: String,    // Manufacturer name
  manufacturer_pn: String, // Manufacturer part number
  preferred_supplier: String,
  cost: Number,            // Unit cost
  description: String,
  status: String,          // Active/Obsolete/Discontinued
  category: String,        // Resistors/Capacitors/etc.
  main_image: String,      // URL to main image
  thumbnails: Array,       // Additional images
  specifications: Array,   // Technical specs
  inventory: Array,        // Stock locations
  history: Array,          // Change log
  attachments: Array       // Related documents
}
