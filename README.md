# Shivar Peth Platform V4

A production-oriented foundation for a Marathi rural marketplace/facilitator platform with separate Admin/User control, PostgreSQL, Redis-ready workers, opt-in campaign architecture, AI, WhatsApp, payments, weather and maps adapters.

## Important
External credentials are intentionally NOT bundled. Never put real secrets in source control or the frontend.

## Start
1. Copy `.env.example` to `.env` and set secrets.
2. `npm install`
3. `npm run db:migrate`
4. `npm run db:seed` (change the seed password immediately)
5. `npm start`
6. `npm run check`

## Production
Use HTTPS, a managed PostgreSQL instance, Redis, backups, monitoring, secret management, restricted API keys, and a real domain. Configure Meta/WhatsApp, OpenAI, Razorpay and Google credentials only from their official dashboards.

## Master data
The bundled workbook contains the 36-district seed and import templates. It deliberately does not invent a full village list. The Maharashtra State Data Bank publishes a `District,Taluka,Village Master` dataset/report and should be used as the authoritative source when importing the current full hierarchy: https://mahasdb.maharashtra.gov.in/planningReport.do

## Core modules
- Admin authentication/RBAC and audit foundation
- User authentication and trial
- District/Taluka/Village hierarchy
- Excel/CSV location import
- Opt-in campaign foundation
- AI ad generation adapter
- WhatsApp template messaging adapter
- Razorpay order/signature/webhook foundation
- Weather and Maps adapters
- PostgreSQL schema + indexes
- Redis/BullMQ dependency foundation
