# Axion CRM

A comprehensive, modern CRM system designed specifically for door-to-door sales companies. Manage leads, track sales pipelines, optimize territories, and grow your business.

## Features

✅ **Lead Management** - Track prospects and customer interactions
✅ **Sales Pipeline** - Visualize and manage your sales funnel
✅ **Territory Management** - Assign and optimize sales territories
✅ **Customer Database** - Centralized customer information
✅ **Performance Analytics** - Real-time dashboards and reports
✅ **Mobile Responsive** - Works seamlessly on all devices
✅ **Team Collaboration** - Assign leads, track team performance
✅ **Commission Tracking** - Monitor commissions and payouts

## Tech Stack

- **Frontend**: React 18 + TypeScript + Tailwind CSS
- **Backend**: Node.js + Express + TypeScript
- **Database**: PostgreSQL
- **Authentication**: JWT
- **Deployment**: Docker ready

## Quick Start

### With Docker (Easiest)
```bash
docker-compose up -d
```
Application will be available at http://localhost:3000

### Manual Setup

1. Clone the repository
```bash
git clone https://github.com/pgagne68/axioncrm.git
cd axioncrm
```

2. Install backend dependencies
```bash
cd backend
npm install
cp .env.example .env
npm run db:migrate
```

3. Install frontend dependencies
```bash
cd ../frontend
npm install
cp .env.example .env
```

4. Start development servers
```bash
# Terminal 1 - Backend
cd backend
npm run dev

# Terminal 2 - Frontend
cd frontend
npm start
```

## Project Structure

```
axioncrm/
├── backend/                 # Express API server
│   ├── src/
│   │   ├── controllers/    # Route handlers
│   │   ├── models/         # Database models
│   │   ├── routes/         # API routes
│   │   ├── middleware/     # Custom middleware
│   │   ├── services/       # Business logic
│   │   └── config/         # Configuration
│   ├── migrations/         # Database migrations
│   └── package.json
├── frontend/               # React application
│   ├── src/
│   │   ├── components/     # React components
│   │   ├── pages/          # Page components
│   │   ├── services/       # API services
│   │   ├── hooks/          # Custom hooks
│   │   └── types/          # TypeScript types
│   └── package.json
└── docker-compose.yml      # Docker configuration
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/logout` - Logout user
- `POST /api/auth/refresh` - Refresh token

### Leads
- `GET /api/leads` - Get all leads
- `POST /api/leads` - Create new lead
- `GET /api/leads/:id` - Get lead details
- `PUT /api/leads/:id` - Update lead
- `DELETE /api/leads/:id` - Delete lead

### Customers
- `GET /api/customers` - Get all customers
- `POST /api/customers` - Create customer
- `GET /api/customers/:id` - Get customer details
- `PUT /api/customers/:id` - Update customer

### Sales
- `GET /api/sales` - Get sales records
- `POST /api/sales` - Create sale
- `GET /api/sales/analytics` - Get analytics

### Territories
- `GET /api/territories` - Get territories
- `POST /api/territories` - Create territory
- `PUT /api/territories/:id` - Update territory
- `GET /api/territories/:id/performance` - Territory performance

## Environment Variables

**Backend (.env)**
```
DATABASE_URL=postgresql://axioncrm_user:axioncrm_password@localhost:5432/axioncrm
JWT_SECRET=your_super_secret_jwt_key_change_this_in_production
NODE_ENV=development
PORT=5000
```

**Frontend (.env)**
```
REACT_APP_API_URL=http://localhost:5000/api
```

## Deployment

### Deploy with Docker
```bash
docker-compose -f docker-compose.yml up -d
```

### Deploy to Heroku
```bash
heroku create axioncrm
git push heroku main
```

### Deploy to DigitalOcean/AWS
See deployment guides in the `/docs` folder

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

MIT License - see LICENSE file for details

## Roadmap

- [ ] Mobile app (React Native)
- [ ] Advanced analytics dashboard
- [ ] AI-powered lead scoring
- [ ] Email/SMS integration
- [ ] Multi-language support
- [ ] Real-time notifications
- [ ] Advanced territory optimization

## Support

For questions or issues, please open a GitHub issue.

---

Built with ❤️ for door-to-door sales teams
