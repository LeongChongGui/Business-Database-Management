## **README.md**

# 📊 Netflix Database Management System

A comprehensive two-phase database project for Netflix, designed as part of the **IS105 Business Data Management** course. This project demonstrates full database lifecycle management from conceptual modeling to implementation and querying.

## 🎯 Project Overview

This project involved designing and implementing a complete database system for Netflix's streaming platform. The work was divided into two phases:

- **Phase 1**: ER Model Design - Conceptual database design with business rules and requirements
- **Phase 2**: Database Implementation - Physical database creation with SQL queries and analytics

## 🏗️ System Architecture

### **Core Entities (12 Total)**
- **Member Management**: `MEMBER`, `PROFILE`, `DEVICE`
- **Subscription & Payment**: `SUBSCRIPTION_PLAN`, `PAYMENT`, `MEMBER_SUBSCRIPTION_PAYMENT`
- **Content Library**: `CONTENT`, `FILM`, `EPISODE`, `SERIES`, `SEASON`, `ACTOR`
- **User Engagement**: `WATCH_HISTORY`, `RECOMMENDATION`
- **Content Attributes**: `CONTENT_ACTOR`, `CONTENT_CREATOR`, `CONTENT_MOOD`, `CONTENT_GENRE`

### **Key Relationships**
- Weak Entity: `PROFILE` depends on `MEMBER`
- Supertype/Subtype: `CONTENT` → `FILM` and `EPISODE`
- Ternary Relationship: `WATCH_HISTORY` connects `PROFILE`, `CONTENT`, and time
- Multiple M:N relationships with associative entities

## 🔧 Technical Implementation

### **Database Features**
- **Complex ER Model**: 12+ entities with weak entities, supertype/subtype, and ternary relationships
- **Full SQL Implementation**: Complete DDL with constraints and realistic test data
- **Business Analytics**: 4 complex queries addressing real Netflix business needs
- **Data Integrity**: Proper foreign key constraints and data validation

### **Key SQL Queries**
1. **Content Analytics**: Top 5 most-watched series in 2024
2. **Financial Reporting**: Monthly revenue by subscription plan
3. **Subscription Compliance**: Active device monitoring per member
4. **Customer Retention**: Identifying members likely to churn

## 🚀 Getting Started

### **Prerequisites**
- MySQL Server 8.0+
- MySQL Workbench or command-line client

### **Installation**
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/netflix-database-project.git
   ```
2. Navigate to the project directory:
   ```bash
   cd netflix-database-project
   ```
3. Execute the SQL script:
   ```bash
   mysql -u username -p < Phase2/netflix_database.sql
   ```

### **Running Queries**
Connect to your MySQL instance and use the database:
```sql
USE netflix;
-- Execute any of the functional queries from the SQL file
```

## 📊 Sample Analytics Output

### **Top 5 Series (2024)**
| Series | Year | View Count |
|--------|------|------------|
| Stranger Things | 2024 | 42 |
| Squid Game | 2024 | 38 |
| Arcane | 2024 | 35 |
| The Politician | 2024 | 28 |
| The Haunting of Hill House | 2024 | 25 |

### **Revenue by Plan (Oct 2024)**
| Plan Type | Monthly Revenue | Active Users |
|-----------|----------------|--------------|
| Premium | $233.82 | 9 |
| Standard | $119.88 | 6 |
| Basic | $41.94 | 3 |

## 🎓 Learning Outcomes

### **Phase 1 Learnings**
- Translating business requirements into conceptual models
- Designing complex ER diagrams with various entity types
- Identifying stakeholders and use cases
- Presenting technical designs effectively

### **Phase 2 Learnings**
- Converting ER models to relational schemas
- Writing comprehensive SQL DDL and DML
- Creating meaningful business queries
- Database testing and validation techniques
- Team collaboration on technical projects

## 👥 Team Members
- **Elsen Soh** - Team Lead & Database Design
- **Leong Chong Gui** - Business Requirements Analysis
- **Teo Jie Ying** - SQL Implementation & Testing
- **Shamaine Wong** - Documentation & Presentation
- **Florance Gwee** - Query Design & Analytics

## 📚 Course Context
This project was completed for **IS105 Business Data Management** at Singapore Management University, demonstrating proficiency in:
- Database design principles
- Entity-Relationship modeling
- SQL programming and optimization
- Business requirements analysis
- Team-based project development

## 🔗 Related Resources
- [MySQL Documentation](https://dev.mysql.com/doc/)
- [ER Diagram Notation Guide](https://www.lucidchart.com/pages/er-diagrams)
- [Database Design Best Practices](https://www.guru99.com/database-design.html)

---

*This project is for educational purposes and is not affiliated with Netflix, Inc.*
