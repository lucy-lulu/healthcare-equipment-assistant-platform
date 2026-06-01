# Healthcare Equipment Assistant Platform

A full-stack healthcare equipment assistant designed for [Novis Healthcare](https://novis.com.au/), an Australian assistive technology and healthcare equipment provider. The platform helps NDIS participants, carers, and business partners search for suitable assistive products and manage quote requests more efficiently.

The platform was developed for a real client context involving NOVIS Healthcare, where equipment selection is often handled through a manual process. The goal of this project is to make product discovery, accessibility-aware browsing, and quote-request workflows easier to use, easier to maintain, and more scalable.

---

## Demo & Prototype

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>Live Demo</h3>
      <p>
        <a href="http://13.211.212.24/login">Open Live Demo</a>
      </p>
      <p><strong>Demo Accounts</strong></p>
      <p>
        <strong>Business Partner</strong><br/>
        Username: <code>partner_jane</code><br/>
        Password: <code>password</code>
      </p>
      <p>
        <strong>Admin</strong><br/>
        Username: <code>admin_jane</code><br/>
        Password: <code>password</code>
      </p>
      <p><em>These are demo accounts for portfolio review only.</em></p>
    </td>
    <td width="50%" valign="top">
      <h3>Figma Prototype</h3>
      <p>
        <a href="https://www.figma.com/proto/rG02DzTzSoGmnUWFHcz2WL/Novis-Frontend?node-id=149-3703&p=f&t=ibopKxSO0lndZZIy-0&scaling=min-zoom&content-scaling=fixed&page-id=148%3A3699&starting-point-node-id=149%3A3700">Open Figma Prototype</a>
      </p>
      <p>
        The prototype explores the product discovery flow, role-based user experience,
        and accessibility-oriented interface design.
      </p>
    </td>
  </tr>
</table>

---

## Why This Project

Choosing assistive healthcare equipment can be difficult because users often need to consider disability needs, product suitability, funding constraints, supplier workflows, and professional recommendations.

In the original client context, parts of this process were handled manually. This project explores how a web platform can make the workflow more scalable by supporting:

- structured product search and filtering
- product detail review
- enquiry submission and reply workflows
- order and quote-related workflows
- role-based access for different user types
- future integration with enterprise systems such as SAP or HubSpot

---

## Key Features

### Product Discovery

- Browse healthcare equipment products
- Search products by keyword
- View detailed product information
- Support product categories and structured product attributes

### Enquiry Workflow

- Submit product-related enquiries
- View enquiry status
- Allow authorised users to reply to enquiries
- Track pending and answered enquiries

### Order / Quote Workflow

- Create product orders or quote-style requests
- View personal order history
- View order details with product items and quantities
- Admin access for broader order management

### Authentication and Authorisation

- Login-based user authentication
- JWT-based API access
- Role-based access control
- Separate permissions for partner, sales, occupational therapist, and admin users

### Admin / Partner Support

- Admin-facing management workflows
- Business partner access for submitting and tracking requests
- Backend APIs designed around practical healthcare product operations

---

## Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | React 18, TypeScript, Vite |
| UI | Ant Design, Tailwind CSS, Ant Design Icons |
| State / Routing | Zustand, React Router |
| API Client | Axios |
| Backend | Java 21, Spring Boot 3.4.4 |
| API | Spring Web, RESTful JSON APIs |
| Authentication | Spring Security, JWT |
| Database / Persistence | MySQL, MyBatis, Spring Data JPA |
| Validation | Jakarta Validation, Hibernate Validator |
| Documentation | OpenAPI / Swagger, GitHub Wiki |
| Testing | Spring Boot Test, Spring Security Test, MyBatis Test |
| Build Tools | Maven, npm, Vite |
| Design | Figma |
| Project Management | GitHub Projects, Agile/Scrum |

---

## Architecture Overview

```text
React + TypeScript Frontend
        |
        | Axios / JSON
        v
Spring Boot REST API
        |
        | Service + Security Layer
        v
MyBatis / JPA Persistence Layer
        |
        v
MySQL Database
```

The frontend communicates with the backend through RESTful JSON APIs. The backend handles authentication, product management, enquiry workflows, order workflows, and user/role-based access control.

---

## API Highlights

The backend provides REST APIs for:

- user authentication and logout
- product listing, product details, and product search
- category retrieval
- order creation and order history
- enquiry creation, enquiry listing, and enquiry replies
- role-based user operations

Example endpoints:

```text
POST /api/auth/login
GET  /api/products
GET  /api/products/{id}
GET  /api/products/search?query=cushion
GET  /api/orders/my
POST /api/orders/place
GET  /api/enquiries/my
POST /api/enquiries/send
POST /api/enquiries/{id}/reply
```

---

## Repository Structure

```text
.
├── backend/                  # Spring Boot backend application
│   ├── src/                  # Backend source code
│   ├── sql/                  # Database scripts
│   ├── pom.xml               # Maven configuration
│   └── API_DOCUMENTATION_EN.md
│
├── frontend/
│   └── code/
│       └── nov-project/      # React + TypeScript + Vite frontend
│
├── docs/                     # Project documentation and design materials
└── README.md
```

---


## My Contribution

My work focused on both backend engineering and product delivery:

- contributed to backend API and database design
- implemented and supported core backend workflows using Java and Spring Boot
- helped design product search, quote/order, and enquiry-related workflows
- supported role-based access control design
- contributed to technical documentation and client-facing demonstrations
- coordinated sprint planning, task allocation, team communication, and progress tracking as Scrum Master
- helped translate client needs into user stories, acceptance criteria, and implementable product features



## Team & Credits

**Team Members**

- Luyun Li — Client Liaison / Scrum Master, Back-end
- Zongliang Han — Product Owner, Back-end
- Zihao Wang — Backend Lead, Back-end
- Ning Yang — Frontend Lead, Front-end
- Shenyi Hu — Developer, Front-end
- Shuran Yang — Developer, Front-end
- Xinze Li — Developer, Front-end
- Zixun Qiu — Developer, Front-end
- Chan Tang — Developer, Back-end
- Jiale Xu — Developer, Back-end
- Tingyu Wang — Developer, Back-end
- Wenxu Guo — Developer, Back-end

**Mentor:** Dr. Geoff Jenkins  
**Client:** Jim McKinlay
