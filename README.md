# Odoo

[![Build Status](https://runbot.odoo.com/runbot/badge/flat/1/master.svg)](https://runbot.odoo.com/runbot)
[![Tech Doc](https://img.shields.io/badge/master-docs-875A7B.svg?style=flat&colorA=8F8F8F)](https://www.odoo.com/documentation/master)
[![Help](https://img.shields.io/badge/master-help-875A7B.svg?style=flat&colorA=8F8F8F)](https://www.odoo.com/forum/help-1)
[![Nightly Builds](https://img.shields.io/badge/master-nightly-875A7B.svg?style=flat&colorA=8F8F8F)](https://nightly.odoo.com/)

Odoo is a suite of web based open source business apps.

The main Odoo Apps include an [Open Source CRM](https://www.odoo.com/page/crm),
[Website Builder](https://www.odoo.com/app/website),
[eCommerce](https://www.odoo.com/app/ecommerce),
[Warehouse Management](https://www.odoo.com/app/inventory),
[Project Management](https://www.odoo.com/app/project),
[Billing &amp; Accounting](https://www.odoo.com/app/accounting),
[Point of Sale](https://www.odoo.com/app/point-of-sale-shop),
[Human Resources](https://www.odoo.com/app/employees),
[Marketing](https://www.odoo.com/app/social-marketing),
[Manufacturing](https://www.odoo.com/app/manufacturing),
[...](https://www.odoo.com/)

Odoo Apps can be used as stand-alone applications, but they also integrate seamlessly so you get
a full-featured [Open Source ERP](https://www.odoo.com) when you install several Apps.

## Getting started with Odoo

For a standard installation please follow the [Setup instructions](https://www.odoo.com/documentation/master/administration/install/install.html)
from the documentation.

To learn the software, we recommend the [Odoo eLearning](https://www.odoo.com/slides),
or [Scale-up, the business game](https://www.odoo.com/page/scale-up-business-game).
Developers can start with [the developer tutorials](https://www.odoo.com/documentation/master/developer/howtos.html).

## Odoo for Restaurant POS and Management

Odoo's Point of Sale (POS) module provides a comprehensive solution for restaurant management, offering features tailored for food service operations.

### Developer Experience
- **Custom Module Development**: Easily extend POS functionality using Python and XML
- **Debugging Tools**: Integrated debugging with Odoo's development mode
- **API Access**: REST APIs for integration with third-party systems
- **Testing Framework**: Automated testing for custom modules using Odoo's test cases

### User Perspectives
**Clients (Restaurant Owners):**
- Real-time sales analytics
- Inventory management for kitchen supplies
- Staff scheduling and payroll
- Customer relationship management

**Workers (Waitstaff/Kitchen):**
- Intuitive order interface
- Table management with floor plans
- Split bills and apply discounts
- Kitchen display system (KDS) integration

### Module Extension Features
- **Menu Engineering**: Analyze dish profitability
- **Reservation System**: Table booking and waitlist management
- **Delivery Integration**: Third-party delivery service APIs
- **Loyalty Programs**: Customizable reward systems
- **Recipe Management**: Ingredient-level cost tracking

### Offline Capabilities
- Orders process without internet connection
- Automatic sync when connection restored
- Local data storage on POS hardware
- Supports cash transactions during outages

### Printer Integration (Epson)
- **Supported Models**: TM-T20, TM-T70, TM-T88V
- **Configuration**:
  ```xml
  <record id="epson_printer" model="pos.printer">
      <field name="name">Kitchen Printer</field>
      <field name="epson_printer_ip">192.168.1.100</field>
      <field name="product_categories" eval="[(6, 0, [ref('product.pos_category_meals')])]"/>
  </record>
  ```
- **Direct Printing**: Supports receipt and kitchen order printing
- **Driverless Setup**: Automatic detection via network

### Hardware POS Installation
1. **Requirements**:
   - x86 or ARM processor
   - 4GB RAM minimum
   - Touchscreen display
   - Ethernet or WiFi connectivity

2. **Installation Steps**:
   ```bash
   # Download Odoo POS image
   wget https://nightly.odoo.com/pos/odoo-pos-18.0.iso

   # Create bootable USB
   sudo dd if=odoo-pos-18.0.iso of=/dev/sdb bs=4M status=progress

   # Boot from USB on POS hardware
   # Follow on-screen configuration
   ```

3. **Peripheral Setup**:
   - Connect Epson printer via Ethernet/USB
   - Configure cash drawer interface
   - Set up barcode scanners for inventory

## Security

If you believe you have found a security issue, check our [Responsible Disclosure page](https://www.odoo.com/security-report)
for details and get in touch with us via email.
