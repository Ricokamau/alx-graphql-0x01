# ALX GraphQL - Rick and Morty App (Next.js + Apollo Client)

## Description
This project is the initial setup of a Next.js application with TypeScript, Apollo Client, and Tailwind CSS to query the Rick and Morty GraphQL API.

## Setup

### 1️⃣ Create the project
```bash
npx create-next-app@latest alx-rick-and-morty-app --typescript --eslint --tailwind
2️⃣ Install dependencies
bash
Copy
Edit
cd alx-rick-and-morty-app
npm install @apollo/client graphql
npm install @types/graphql
3️⃣ GraphQL setup
Create graphql/apolloClient.ts with Apollo Client configuration.

Create graphql/queries.ts with GET_EPISODES query.

4️⃣ Wrap app with ApolloProvider
In pages/_app.tsx:

tsx
Copy
Edit
import "@/styles/globals.css";
import type { AppProps } from "next/app";
import { ApolloProvider } from "@apollo/client";
import client from "@/graphql/apolloClient";

export default function App({ Component, pageProps }: AppProps) {
  return (
    <ApolloProvider client={client}>
      <Component {...pageProps} />
    </ApolloProvider>
  )
}
5️⃣ Run the project
bash
Copy
Edit
npm run dev
Visit: http://localhost:3000
