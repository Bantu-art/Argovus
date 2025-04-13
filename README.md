# Argovus

Argovus is a Django-based microservices application that handles authentication and M-Pesa payment processing. The system consists of two main APIs that communicate with each other to provide a seamless user experience.

## Project Structure

The project is divided into two main components:

1. **Authentication API (parent_auth)**
   - Handles user registration and authentication
   - Manages user profiles and permissions
   - Provides JWT-based authentication
   - Communicates with the Payment API for transaction verification

2. **Payment API (mpesa_payment)**
   - Handles M-Pesa payment processing
   - Manages payment transactions and status
   - Provides payment verification endpoints
   - Communicates with the Authentication API for user validation

## Features

### Authentication API
- User registration and login
- JWT token-based authentication
- User profile management
- Role-based access control
- Secure password handling

### Payment API
- M-Pesa payment integration
- Transaction status tracking
- Payment verification
- Transaction history
- Secure payment processing

## Prerequisites

- Python 3.8+
- Django 4.0+
- PostgreSQL
- M-Pesa API credentials
- Redis (for caching)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Bantu-art/Argovus.git
cd Argovus
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
```bash
cp .env.example .env
# Edit .env with your configuration
```

5. Run migrations:
```bash
python manage.py migrate
```

6. Start the development server:
```bash
python manage.py runserver
```

## API Documentation

### Authentication API Endpoints
- `/api/auth/register/` - User registration
- `/api/auth/login/` - User login
- `/api/auth/profile/` - User profile management

### Payment API Endpoints
- `/api/payment/initiate/` - Initiate M-Pesa payment
- `/api/payment/status/` - Check payment status
- `/api/payment/verify/` - Verify payment transaction

## Security

- All API endpoints are protected with JWT authentication
- Sensitive data is encrypted
- Regular security audits are performed
- M-Pesa API credentials are securely stored

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

Brian Bantu - brianbaraza40@gmail.com

Project Link: [https://github.com/Bantu-art/Argovus](https://github.com/Bantu-art/Argovus)