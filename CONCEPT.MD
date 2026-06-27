# Glance
A data management system for optical clinics and business built upon the electron js framework. 

**Features**

1. Authentication
    -	One-Time Registration 
    -	One-Time Set up Screen (Like the ones on Windows Setup)
    -	Admin/Operator fields (Username, Email, Password, Full Name)
    -	Forgot Password Email Code
    -	Security
        1.	Rate Limiting
        2.	Hashing
        3.	SafeStorage
        4.	Cryptography like bcrypt
        5.	Runtime Hardening (Context Isolation, Sandboxing, IPC Validation)
        6.	JWT

2.	Data Handling
    -	Included tabs (Patients, Sales, Statistics, Inventory)
    -	Develop Eloquent ORM for query building
    -	Can only make requests if logged in
    -	Enforce Strict IPC Communication
    -	JWT for request
    -	Caching, preloading the data before the user clicks on the data
3.	Inventory Management
    -	There are inventory classification presets (eyewear, eye lens, services, etc)
    -	Inventory fields are determined through their classification
    -	Image upload is optional for some classification
4.	Statistical Visualization
    -	Sales
    -	Patient Activity
    -	Inventory
5.	Backups & Syncing
    -	Can export a backup file that can be used to restore a newly installed app
    -	Can potentially make cloud backups if set up
    -	Can also make cloud storage backups if set up
    -	Use PowerSync to sync backend db with the SQLite
    -	If manual syncing, use uuid for proper syncing
    -	Try to use Postgres for backup database and SQLite for offline database
6.	App Configuration
    -	Users can change their user information (Username, Email, Password, Full Name)
    -	Can also configure system information (Clinic Name)
    -	Can configure auto back up
    -	Can switch themes
    -	Eye Comfort option
    -	API Configuration
    -	Save all configuration changes on a separate SQLite database
7.	Port Forwarding (Try)
    -	The ability to upload or use a phones camera for the images through local network
    -	Make it secure like adding a DNS
8.	API Handling (Try)
    -	Ability to set up available APIs like (Cloud Database, Cloud Storage, SMS API)
    -	If not provided, all will be offline and will not include extra features
9.	UI/UX
    -	Configure the windows of the electron app
    -	Should have an opening animation
    -	Flexible with a minimum screen size of 720p
    -	Should look clean, complete and user friendly
10.	System Tools/Languages
    -	React JS (Frontend)
        1.	Vite
        2.	React Zod
        3.	React Hook Form
        4.	Zustand
        5.	TanStack
    -	Node JS (Backend)
        1.	Express JS (Only for phone)
        2.	Prisma (Eloquent ORM)
        3.	CORS
        4.	JWT
        5.	Zod
        6.	Audit Logging
    -	TypeScript
    -	Electron JS
        1.	ContextBridge (Don’t expose node directly)
        2.	Store secrets safely	 
    -	SQLite (w/ SQLCipher) & Postgre
    -	Postman
    -	Jest (For testing)
    -	Tailwind
    -	Canva
    -	Git
    -   Supabase
    -   Cloudflare R2
