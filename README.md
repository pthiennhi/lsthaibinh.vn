# Law Firm Web Application

A full-stack web application for a law firm, developed using **Next.js 14**, **NestJS**, **GraphQL**, and **PostgreSQL**. The application supports client-facing features for legal service inquiries and internal tools for managing cases, clients, and documents.

<!-- ## Features

- **Client Portal**: Clients can view their cases, submit documents, and communicate with the firm.
- **Admin Dashboard**: Internal dashboard for managing cases, clients, and legal documents.
- **GraphQL API**: Seamless communication between the frontend and backend for efficient data fetching.
- **User Authentication**: Secure login for both clients and admins.
- **PostgreSQL Database**: Robust database for managing client and case data. -->

## Tech Stack

- **Frontend**: [Next.js 14](https://nextjs.org/)
  - Server-side rendering for fast initial page loads
  - Static and dynamic routes for client and admin interfaces
  - Optimized for SEO and performance

- **Backend**: [NestJS](https://nestjs.com/)
  - Modular architecture for scalability and maintainability
  - Integrated with GraphQL for API design
  - Authentication and authorization using JWT

- **Database**: [PostgreSQL](https://www.postgresql.org/)
  - Relational database for storing cases, client information, and legal documents
  - Supports complex queries and relationships

- **GraphQL**: [Apollo Server](https://www.apollographql.com/docs/apollo-server/)
  - Efficient querying and mutation of data from the PostgreSQL database
  - Flexible schema design for easy updates and expansions

## Installation

### Prerequisites

- Node.js (v18+)
- PostgreSQL (v14+)
- Yarn (or npm)

### Backend Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/law-firm-app.git
   cd law-firm-app/backend
   ```

2. Install dependencies:
   ```bash
   yarn install
   ```

3. Configure environment variables by creating a `.env` file:
   ```bash
   DATABASE_URL=postgres://user:password@localhost:5432/lawfirmdb
   JWT_SECRET=your_jwt_secret
   ```

4. Run database migrations:
   ```bash
   yarn run migration:run
   ```

5. Start the NestJS server:
   ```bash
   yarn start:dev
   ```

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd ../frontend
   ```

2. Install dependencies:
   ```bash
   yarn install
   ```

3. Configure environment variables in `.env.local`:
   ```bash
   NEXT_PUBLIC_API_URL=http://localhost:4000/graphql
   ```

4. Run the Next.js development server:
   ```bash
   yarn dev
   ```

5. Open the app in your browser:
   ```bash
   http://localhost:3000
   ```

## Running Tests

- Backend (NestJS):
  ```bash
  yarn test
  ```

- Frontend (Next.js):
  ```bash
  yarn test
  ```

## Deployment

### Docker

To deploy the application using Docker:

1. Build the Docker images for both the frontend and backend:
   ```bash
   docker-compose build
   ```

2. Start the application:
   ```bash
   docker-compose up
   ```

### Environment Variables

- `DATABASE_URL`: PostgreSQL connection URL
- `JWT_SECRET`: Secret key for signing JWTs
- `NEXT_PUBLIC_API_URL`: The URL for the GraphQL API

## Contributing

1. Fork the repository.
2. Create your feature branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m 'Add some feature'
   ```
4. Push to the branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a pull request.