# NexGen Sales

A recruiting site and training portal for a direct-sales organization. The public side advertises the opportunity and takes applications. Behind a login, reps work through courses, video trainings, and quizzes, and admins manage the whole thing.

**Live site:** https://recruit-gamma.vercel.app/

## Overview

NexGen Sales is a Nuxt 3 app with server-side rendering. The front of the site is a marketing homepage, a blog, and an application form for candidates. Accepted reps get a portal with structured courses, trainings, and quizzes for onboarding. There is also a small product/checkout flow and a set of admin dashboards for editing every record in the system.

## Features

- Marketing homepage and blog for a sales recruiting org
- Candidate application form with validation and reCAPTCHA
- Gated rep portal: courses, video trainings, and quizzes
- Product listing, cart, checkout, and order confirmation
- Square payment integration
- AWS S3 for image and asset hosting, AWS Lambda for transactional email
- Google sign-in plus JWT sessions, passwords hashed with bcrypt
- Support ticket handling
- Admin dashboards to edit users, blog posts, courses, trainings, bundles, and affiliates
- Auto-deploy on push to `main`

## Stack

- Nuxt 3 (Vue 3, SSR), Pinia for state
- Nuxt server routes for the API
- MongoDB Atlas via Mongoose
- AWS S3 (`@aws-sdk/client-s3`) and AWS Lambda
- Square SDK for payments
- Google OAuth, `jsonwebtoken`, `bcrypt`, reCAPTCHA v3
- Deployed on Vercel

## Getting started

```bash
npm install
npm run dev
```

Set the environment variables:

```
NUXT_AWS_ACCESS_KEY=your_aws_access_key
NUXT_AWS_SECRET_KEY=your_aws_secret_key
NUXT_AWS_REGION=your_aws_region
NUXT_S3_BUCKET=your_s3_bucket_name
DB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
GOOGLE_CLIENT_ID=your_google_oauth_client_id
GOOGLE_CLIENT_SECRET=your_google_oauth_client_secret
```

Build and run production:

```bash
npm run build
npm run start
```

Built by HARTECHO.
