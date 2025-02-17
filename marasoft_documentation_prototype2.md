---

# **ORDERS AND BILLS**  
**Beginner-Friendly Technical Guide**  

---

## **1. Departments > Categories > Sub-Categories > Items**  
### **1.1 Hierarchical Organization**  
The system organizes items into a **tree structure** for easy management:  
```  
DEPARTMENT (e.g., "Kitchen")  
│  
├── CATEGORY (e.g., "Beverages")  
│   │  
│   ├── SUB-CATEGORY (e.g., "Cold Drinks")  
│   │   └── ITEM: "Coca-Cola 500ml"  
│   │  
│   └── SUB-CATEGORY (e.g., "Hot Drinks")  
│       └── ITEM: "Coffee"  
│  
└── CATEGORY (e.g., "Bakery")  
    └── ITEM: "Whole Wheat Bread"  
```  

#### **Table 1: Structure Definitions**  
| **Level**       | **Role**                                  | **Example**              | **Rules**                              |  
|------------------|-------------------------------------------|--------------------------|----------------------------------------|  
| **Department**   | Broad division (e.g., physical location). | `Kitchen`, `Bar`         | Required for categories/items.         |  
| **Category**     | Groups similar items.                     | `Beverages`, `Bakery`    | Must belong to a department.           |  
| **Sub-Category** | Optional subdivision for granularity.     | `Cold Drinks`, `Breads`  | Requires a parent category.            |  
| **Item**         | Specific product or material.             | `Coca-Cola 500ml`, `Flour` | Must belong to a category/sub-category. |  

---

## **2. Creating Categories/Departments**  
### **2.1 Step-by-Step Process**  
1. **Navigate**: Go to **Orders & Bills > Create New Categories/Departments**.  
2. **Input**:  
   - **Department**: Select existing or enter a new name (e.g., `Kitchen`).  
   - **Category**: Enter a name (e.g., `Beverages`).  
   - **Sub-Category** (Optional): Add finer grouping (e.g., `Cold Drinks`).  
3. **Actions**:  
   - **+ADD**: Add multiple entries in one session.  
   - **Delete Icon (🗑️)**: Remove unwanted departments/categories.  
4. **Finalize**: Click **Create Category**.  

**Note**:  
- Categories cannot exist without a department.  

---

## **3. Item Types & Visibility**  
### **3.1 Types of Items**  
| **Item Type**      | **Definition**                          | **Show in Menu?** | **Show in Store?** | **Uses Raw Materials?** | **Example**              |  
|---------------------|------------------------------------------|-------------------|--------------------|-------------------------|--------------------------|  
| **Whole Item**      | Sold directly to customers.             | ✔️                | ✔️                 | ❌                      | `Canned Soda`, `Bread`   |  
| **Raw Material**    | Used to make other items (not sold).     | ❌                | ✔️                 | ❌                      | `Flour`, `Sugar`         |  
| **Prepared Item**   | Made from raw materials (e.g., recipes). | ✔️                | ❌                 | ✔️                      | `Burger`, `Pizza`        |  

### **3.2 Creating Items**  
1. **Navigate**: **Orders & Bills > Create New Items (Menu/Store)**.  
2. **Form Fields**:  
   - **Category/Sub-Category**: Select from dropdowns.  
   - **Item Name**: Unique identifier (e.g., `Coca-Cola 500ml`).  
   - **Description**: Details (e.g., `Sugar-free carbonated drink`).  
   - **Cost Price**: Optional (e.g., `₦200`).  
   - **Sales Price**: Mandatory (e.g., `₦300`).  
   - **Currency**: `NGN` (default) or `KSH`.  
   - **Image**: Upload item photo (JPEG/PNG).  
3. **Visibility**:  
   - **Show in Menu**: Display to customers.  
   - **Show in Store**: Display in internal inventory.  
   - **Item Uses Raw Material**: Tag as Prepared Item.  
4. **Actions**:  
   - **Preview**: See a preview before confirmation to add the new ingredient.  

---

## **4. Editing Items**  
### **4.1 Edit Workflow**  
1. **Navigate**: **Orders & Bills > Manage All Items > Edit Item**.  
2. **Editable Fields**:  
   - Name, category, description, cost/sales price, image.  
3. **Visibility Override**:  
   - **Don’t Modify This Section**:  
     - ✔️ Checked → Retain original item type settings.  
     - ❌ Unchecked → Apply new item type settings.  
4. **Save**: Click **Update Item Details**.  

#### **Table 2: Edit Behavior**  
| **Checkbox State**          | **Outcome**                                                                 |  
|-----------------------------|-----------------------------------------------------------------------------|  
| **Don’t Modify (Checked)**  | Original "Show in Menu/Store" and "Uses Raw Material" settings preserved.   |  
| **Don’t Modify (Unchecked)**| Newly selected visibility settings applied.                                 |  

---

## **5. Managing Inventory**  
### **5.1 Transferring Items Between Departments**  
**Rule**: Items must be **removed** from one department before **adding** to another.  

#### **Step-by-Step Workflow**:  
1. **Remove Items to Department Inventory**:  
   - Go to **Orders & Bills > Manage All Items (Edit) > Manage All Items Settings > Remove Items to Department Inventory**.  
   - Select item (e.g., `Flour`), enter quantity (e.g., `10 kg`), add comment.  
   - Click **Remove from Department Inventory**.  
2. **Add Items**:  
   - Go to **Orders & Bills > Manage All Items (Edit) > Manage All Items Settings > Add Items to Department Store**.  
   - Select same item (`Flour`), confirm quantity, and click **Add**.  

### **5.2 Viewing Department Inventory**  
- **Filters**:  
  - **All Departments**: Default view.  
  - **Reset Filter**: Clear selections.  
- **Actions**:  
  - **Request from Store**: Generate stock requests.  
  - **View Entry Logs**: Track transfers with timestamps.  

---

## **6. Menu Item Management**  
### **6.1 Status Toggles**  
- **General Status**: Visibility to staff (e.g., waiters).  
- **Public Status**: Visibility to customers.  

#### **Actions via Three-Dot Menu (...)**  
| **Action**             | **Outcome**                              |  
|------------------------|------------------------------------------|  
| **General Activate**   | Item appears on staff menus.             |  
| **General Deactivate** | Item hidden from staff menus.            |  
| **Public Activate**    | Item appears on customer menus.          |  
| **Public Deactivate**  | Item hidden from customer menus.         |  
| **Delete**             | Move item to **Deleted Items List**.     |  

**Note**: Deleted items can be restored indefinitely.  

---

## **6. Ingredients & Recipes**  
### **6.1 Creating Ingredients**  
1. **Navigate**: **Orders & Bills > Create New Ingredients**.  
2. **Input Fields**:  
   - **Name**: E.g., `Raw Rice`.  
   - **Measurement Type**: `Weight (kg)`, `Volume (L)`, or `Custom`.  
   - **Conversion Factor**:  
     - **Custom**: Define units (e.g., `1 Cup = 0.5 kg`).  
     - **Per Unit**: Standard units (e.g., `1 Bag = 50 kg`).  
   - **Threshold Reminder**: Set low-stock alerts (e.g., `Alert at 45 kg`).  

#### **Table 3: Conversion Examples**  
| **Type**           | **Input**              | **Output**               |  
|---------------------|------------------------|--------------------------|  
| **Custom**          | `1 Cup = 0.5 kg`       | 2 Cups → 1 kg            |  
| **Per Unit**        | `1 Bag = 50 kg`        | 2 Bags → 100 kg          |  

---

## **8. Glossary**  
| **Term**               | **Definition**                                                                 |  
|------------------------|-------------------------------------------------------------------------------|  
| **Threshold Reminder** | Alerts when stock falls below a set level (e.g., `Alert when flour ≤ 10kg`).  |  
| **Entry Logs**         | Records of item transfers between departments.                                |  

--- 