- **Typography**: Changed the font to **Lusitana** for specific headings and the logo.

[View Home Screen Screenshot](./screenshots/image.png)

## Chapter 3 Completion

- **Font Optimization**: Successfully integrated the `lusitana` font using `next/font`.
- **Image Optimization**: Added the `next/image` component to handle desktop and mobile hero images efficiently.
- **Component Restoration**: Re-enabled the `AcmeLogo` component in the main page.

[View Chapter 3 Evidence](./screenshots/image.png)

## Chapter 4

- **Nested Routing**: Created the `/dashboard` route along with nested routes for `/dashboard/customers` and `/dashboard/invoices`.
- **Shared Layouts**: Implemented a structural `layout.tsx` for the dashboard to enable a shared sidebar navigation across all sub-pages.
- **Route Segments**: Successfully used folder-based routing to define the application's dashboard structure.

[View Chapter 4 Evidence](./screenshots/Screenshot%202026-02-22%20130335.png)

[View Chapter 4 Evidence_2](./screenshots/Screenshot%202026-02-22%20130400.png)

## Chapter 5

- **Navigation**: Replaced `<a>` tags with the `<Link />` component from `next/link` to enable fast, client-side navigation.
- **Active Link Pattern**: Used the `usePathname()` hook to track the current route and highlight the active link in the sidebar.
- **Conditional Styling**: Applied the `clsx` utility to dynamically toggle CSS classes for a better user experience during navigation.

[View Chapter 5 Navigation Evidence](./screenshots/Screenshot%202026-02-22%20130400.png)

## Chapter 6

- **Database Setup**: Initialized a PostgreSQL database and connected it to the application using environment variables.
- **Data Seeding**: Implemented a seeding script to populate the database with initial users, customers, invoices, and revenue data.
- **SQL Queries**: Successfully verified database connectivity and data retrieval by creating a `/query` route to fetch specific records using SQL.

[View Chapter 6 Database Query Evidence](./screenshots/Screenshot%202026-02-22%20135835.png)

## Chapter 7

- **Data Fetching**: Fetched data using SQL for the dashboard components, including revenue, invoices, and card statistics.
- **Dashboard Overview**: Completed the main dashboard page by populating the `RevenueChart`, `LatestInvoices`, and `<Card>` components with real data from the database.
- **Server Components**: Leveraged React Server Components to fetch data directly on the server, improving performance and security.
- **Async/Await**: Used standard JavaScript `async/await` syntax to handle asynchronous data fetching within the page component.

[View Chapter 7 Dashboard Evidence](./screenshots/Screenshot%202026-02-22%20141756.png)
