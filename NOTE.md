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

## Chapter 8

- **Static vs Dynamic Rendering**: Explored the differences between static and dynamic rendering and their impact on performance.
- **Dynamic Rendering**: Switched to dynamic rendering for the dashboard to ensure users always see the latest data.
- **Handling Slow Data**: Observed how synchronous data fetching can lead to a "waterfall" effect, where slow requests block the entire page from rendering.
- **Artificial Delay**: Implemented a 3-second artificial delay in the data fetch to simulate real-world networking issues and observe its effect on the application.

[View Chapter 8 Evidence](./screenshots/Screenshot%202026-02-22%20143353.png)

## Chapter 9

- **Streaming Data**: Implemented streaming data fetching using `useEffect` and `useRef` to handle real-time updates.
- **Data Updates**: Successfully updated the dashboard components in real-time as new data arrives.
- **Error Handling**: Added error handling for network issues and data processing errors.
- **Performance Optimization**: Reduced the number of re-renders by using `useMemo` and `useCallback`.

[View Chapter 9 Streaming Evidence](./screenshots/Screenshot%202026-02-22%20170438.png)

## Chapter 10

- **Search Functionality**: Implemented a search bar using URL search parameters (`useSearchParams`, `usePathname`, and `useRouter`).
- **URL-State Sync**: Ensured the search input stays in sync with the URL, allowing for bookmarkable and shareable search results.
- **Server-Side Filtering**: Updated the data fetching logic to filter invoices based on the search query provided through the URL.
- **Pagination**: Implemented server-side pagination to navigate through large datasets of invoices efficiently.
- **Dynamic Table**: Successfully rendered the `InvoicesTable` component which dynamically updates based on both search queries and current page selection.

[View Chapter 10 Search & Pagination Evidence](./screenshots/Screenshot%202026-02-24%20220611.png)

## Chapter 11

- **Server Actions**: Implemented React Server Actions to handle form submissions securely on the server without needing manual API endpoints.
- **Form Data Validation**: Used the `zod` library to define schemas and validate form data before performing database mutations.
- **Creating Invoices**: Developed the "Create Invoice" workflow, mapping form fields to SQL `INSERT` statements using the `postgres` library.
- **Cache Revalidation**: Utilized `revalidatePath` to clear the Next.js Data Cache for the invoices route, ensuring the table reflects new data immediately.
- **Redirects**: Used the `redirect` function to navigate users back to the main `/dashboard/invoices` page after a successful data update.

[View Chapter 11 Mutating Data Evidence](./screenshots/Screenshot%202026-02-25%20144112.png)

## Chapter 12

- **Updating Data**: Created dynamic route segments `[id]` and server actions to fetch and update existing invoice records.
- **Deleting Data**: Implemented functionality to remove invoices from the database using a server action and the `DELETE` SQL command.
- **Error Handling**: Integrated `error.tsx` to catch unexpected runtime errors and provide a fallback UI with a reset option.
- **404 Not Found**: Leveraged the `notFound()` function and `not-found.tsx` to handle scenarios where a specific invoice record does not exist in the database.

[View Chapter 12 Handling Errors Evidence](./screenshots/Screenshot%202026-02-25%20151037.png)

## Chapter 13

- **Improving Accessibility**: Focused on making the application more accessible to users with impairments.
- **Form Validation**: Implemented server-side validation using `useActionState` (or `useFormState`) to handle form data and return descriptive error messages.
- **ARIA Attributes**: Added ARIA attributes like `aria-describedby`, `aria-atomic`, and `role="alert"` to improve the experience for screen readers.
- **User Experience**: Enhanced the form feedback loop by displaying specific field errors (e.g., missing amount or status) directly in the UI, ensuring users can correct mistakes easily.

[View Chapter 13 Accessibility Evidence](./screenshots/Screenshot%202026-02-26%20222810.png)

## Chapter 14

- **Authentication**: Integrated NextAuth.js to add authentication to the application.
- **Login Page**: Created a fully functional login page at `/login` with email and password fields using the `LoginForm` component.
- **Middleware Protection**: Configured `middleware.ts` to protect dashboard routes, redirecting unauthenticated users to the login page.
- **Sign In/Sign Out**: Implemented `signIn` and `signOut` server actions using NextAuth.js to handle user sessions securely.
- **Credentials Provider**: Set up the credentials-based authentication provider with password verification using `bcrypt`.

[View Chapter 14 Authentication Evidence](./screenshots/Chapter14.png)

## Chapter 15

- **Metadata**: Added metadata to the application using the Next.js Metadata API to improve SEO and shareability.
- **Title Template**: Configured a `title.template` in the root `layout.tsx` to dynamically generate page titles in the format `%s | Acme Dashboard`.
- **Page-Level Metadata**: Added specific `metadata` exports to individual pages (e.g., invoices, dashboard) to override the default title template.
- **Open Graph**: Ensured the application is ready for social sharing with a proper `description` and `metadataBase` configuration.
