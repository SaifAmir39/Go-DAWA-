<div align="center">
  <img src="assets/images/insta_dawaa_logo.png" alt="Go Dawa Logo" width="220" style="border-radius: 20px;"/>
  
  # Go Dawa
  
  **Enterprise-Grade B2B Pharmaceutical Supply Chain Management Platform**
  
  [![Flutter][flutter-badge]][flutter-url]
  [![Dart][dart-badge]][dart-url]
  [![Clean Architecture][clean-architecture-badge]][clean-architecture-url]
  [![BLoC Pattern][bloc-badge]][bloc-url]
  [![Firebase][firebase-badge]][firebase-url]
  [![Platforms][platforms-badge]][platforms-url]
  
  [flutter-badge]: https://img.shields.io/badge/Flutter-3.x-02569B?logo=flutter&logoColor=white&style=for-the-badge
  [flutter-url]: https://flutter.dev
  [dart-badge]: https://img.shields.io/badge/Dart-3.9.2+-0175C2?logo=dart&logoColor=white&style=for-the-badge
  [dart-url]: https://dart.dev
  [clean-architecture-badge]: https://img.shields.io/badge/Architecture-Clean%20Architecture-FF6B6B?style=for-the-badge
  [clean-architecture-url]: #-architecture
  [bloc-badge]: https://img.shields.io/badge/State%20Management-BLoC%20%26%20Cubit-4C63FF?style=for-the-badge
  [bloc-url]: https://bloclibrary.dev
  [firebase-badge]: https://img.shields.io/badge/Firebase-Cloud%20Messaging-FFCA28?logo=firebase&logoColor=white&style=for-the-badge
  [firebase-url]: https://firebase.google.com
  [platforms-badge]: https://img.shields.io/badge/Platforms-Android%20%7C%20iOS-blue?style=for-the-badge
  [platforms-url]: #-platforms--versions
  
  ***
  
  Transform your pharmaceutical supply chain with an intelligent, scalable, and user-friendly ordering platform.
  
  ***
</div>

## 📚 Quick Navigation

- 📖 [Documentation](#-documentation)
- 🚀 [Quick Start](#-getting-started)
- 💻 [Tech Stack](#-tech-stack)
- 🏗 [Architecture](#-architecture)
- 📦 [Features](#-features)

---

## 📖 Documentation Sections

- [Overview](#-overview---english)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Architecture & Design Patterns](#-architecture)
- [Tech Stack](#-tech-stack)
- [Feature Modules](#-feature-modules-detailed)
- [Core Services](#-core-services)
- [State Management](#-state-management)
- [Getting Started](#-getting-started)
- [Configuration & Setup](#-configuration)
- [Localization](#-localization)
- [API Reference](#-api-reference)
- [Security & Authentication](#-security)
- [UI Theme & Design](#-ui-theme--design)
- [Testing Strategy](#-testing)
- [Troubleshooting](#-troubleshooting)
- [Contributing](#-contributing-guidelines)
- [Project Statistics](#-project-statistics)

---

## 🎯 Overview

**Go Dawa** is a comprehensive **enterprise-grade B2B pharmaceutical supply chain management platform** designed to revolutionize how pharmacies and pharmacy chains manage their medicine procurement operations.

### Purpose & Vision

Go Dawa bridges the gap between pharmacies and pharmaceutical suppliers/warehouses by providing:
- **Seamless Ordering** — Multiple intuitive channels for order creation (search, voice, file upload)
- **Real-Time Visibility** — Complete order lifecycle tracking and supply management
- **Business Intelligence** — Analytics on profitability, inventory, and order patterns
- **Operational Efficiency** — Automated workflows for returns, quotas, and routine ordering

### Target Audience

| User Type | Use Cases |
|-----------|-----------|
| **Individual Pharmacies** | Quick ordering, status tracking, returns management |
| **Pharmacy Chains** | Centralized ordering, multi-location management, analytics |
| **Pharmacy Managers** | Inventory oversight, profitability analysis, device management |
| **Pharmacy Staff** | Voice-based ordering, quick product search |

### Project Identity

| Key Details | Value |
|---|---|
| **Package Name** | `com.example.godawa_app` |
| **Current Version** | 1.0.0 (Build 1) |
| **API Base URL** | `https://instadawa11.azurewebsites.net` |
| **Min Android SDK** | 21+ (with Flutter defaults) |
| **Min iOS Version** | 13.0 |
| **Primary Markets** | Middle East (Arabic-first) |

---

## ✨ Features

### 🔍 **Discovery & Search**
- **Advanced Product Search** with real-time suggestions
- **Multi-filter Search**: supplier, manufacturer, warehouse, category
- **Availability Checker**: cross-warehouse inventory lookup
- **Best Price Comparison**: view pricing across different suppliers
- **Warehouse Catalog Browser**: browse complete supplier inventories

### 🛒 **Ordering & Cart**
- **Multi-Channel Order Creation**:
  - Traditional search-based ordering
  - Voice-activated ordering with speech-to-text
  - Bulk file/image upload for invoices
- **Smart Cart Management**:
  - Warehouse-grouped cart organization
  - Bulk add/edit/delete operations
  - Per-warehouse clear functionality
  - Real-time quantity & price updates

### 📦 **Order Management**
- **Complete Order Lifecycle**:
  - Order creation & checkout
  - Real-time status tracking with timeline
  - Order cancellation (where permitted)
  - Delivery confirmation & acceptance
  - Invoice download (PDF & Excel formats)
- **Order History** with pagination and filtering
- **Reviews & Ratings** for received items

### 🏭 **Warehouse & Supplier Management**
- **Warehouse Browser** with search & filtering
- **Supplier Product Catalogs**
- **Delivery Round Information**
- **Direct Ordering** from supplier views
- **Pricing & Availability** across locations

### 📋 **Returns & Compliance**
- **Returns Workflow**:
  - Invoice-based product selection
  - Return reason specification
  - Automated return request processing
  - Return status tracking

### 📊 **Analytics & Intelligence**
- **Top Profitable SKUs** — identify best-selling products
- **Seasonal Items Catalog** — specialized product collections
- **Quota Management** — view allocated purchasing limits
- **Recent Supply History** — paginated delivery records

### 🔔 **Communications**
- **Push Notifications** (Firebase Cloud Messaging)
- **Local Notifications** for app-based alerts
- **Notification Center** with read/unread management
- **Telesales Callbacks** — request direct agent contact
- **Contact Us** — direct support communication

### 👤 **Account & Device Management**
- **User Profile** — view/edit personal information
- **Multi-Language Support** — Arabic (RTL) & English
- **Active Devices** — view all logged-in sessions
- **Device Revocation** — remote logout from other devices
- **Password Management** — secure reset & change workflows
- **Preference Settings** — language, notifications, privacy

---

## 📁 Project Structure

```
godawa_app/
│
├── 📄 lib/
│   ├── 🎨 main.dart                          # App entry point & Firebase init
│   ├── 🎨 app_colors.dart                    # Color palette constants
│   ├── ⚙️  constances.dart                    # Global API & token constants
│   ├── 🔥 firebase_options.dart              # Firebase configuration
│   │
│   ├── 🔧 core/                              # Shared services & utilities
│   │   ├── 📡 bloc/                          # Global BLoCs (CheckAvailability)
│   │   ├── ❌ errors/                        # Custom exception classes
│   │   ├── 🛣️  helper/                       # Route generation logic
│   │   ├── 🌐 localization/                  # i18n utilities
│   │   ├── 📦 models/                        # Shared data models
│   │   ├── 🔐 service/
│   │   │   ├── 🌐 Api/                       # HTTP client (Dio + interceptors)
│   │   │   ├── 📡 connectivity/              # Network monitoring
│   │   │   ├── 💾 Locale_storge/             # SharedPreferences cache
│   │   │   └── 🔔 notfications/              # Firebase + local messaging
│   │   └── 🛠️  utils/                         # Shared widgets, styling, DI
│   │
│   ├── 📦 features/                          # Feature modules (Clean Arch)
│   │   ├── 🔐 auth/                          # Authentication
│   │   │   ├── 📊 data/                      # Models & repository implementations
│   │   │   ├── 🎯 domain/                    # Entities & abstract repository
│   │   │   └── 🎨 presntation/               # Views & state managers (Cubits)
│   │   │
│   │   ├── 🏠 home/                          # Main dashboard & navigation
│   │   ├── 🛒 cart/                          # Shopping cart
│   │   ├── 🔍 search_produict/               # Advanced product search
│   │   ├── 🏭 wharehouse/                    # Supplier & warehouse browsing
│   │   ├── 📦 orders/                        # Order management & tracking
│   │   ├── 📋 profile/                       # User account & settings
│   │   ├── 🔔 notification/                  # Notification center
│   │   ├── ↩️  returns_approval/              # Product returns workflow
│   │   ├── ⚡ flash_offers/                   # Promotional offers
│   │   ├── 🌱 Seasonal_items/                # Seasonal products
│   │   ├── 💎 top_profitable_sKUs/           # Profitability analytics
│   │   ├── 📊 couta_items/                   # Quota management
│   │   ├── 🎤 create_order_voice/            # Voice ordering
│   │   ├── 📁 Create_order_File/             # File-based ordering
│   │   ├── ☎️  telly_sales_call/             # Telesales requests
│   │   ├── 📱 active_devices/                # Session management
│   │   ├── 📜 recent_supplies/               # Supply history
│   │   ├── 🎬 onboarding/                    # First-time user guide
│   │   ├── 🚀 Splash/                        # App launch screen
│   │   └── 📵 no_internet/                   # Offline screen
│   │
│   ├── 🌍 generated/                         # Auto-generated i18n classes
│   └── 📍 l10n/                              # Translation files (AR + EN)
│
├── 📱 android/                               # Android native code
├── 🍎 ios/                                   # iOS native code
├── 🌐 web/                                   # Web platform (future)
├── 🖥️  windows/                               # Windows platform (future)
├── 🐧 linux/                                 # Linux platform (future)
├── 🔧 macos/                                 # macOS platform (future)
│
├── 📦 test/                                  # Unit & widget tests
├── 📋 pubspec.yaml                           # Dependencies & metadata
├── 📋 pubspec.lock                           # Locked dependency versions
├── ⚙️  analysis_options.yaml                  # Dart/Flutter linting rules
├── 🔥 firebase.json                          # Firebase project config
├── 📍 l10n.yaml                              # Localization configuration
├── 📄 README.md                              # This file
└── 📄 .env                                   # Environment variables (not in VCS)
```

### Feature Module Structure (Clean Architecture)

Each feature follows consistent Clean Architecture patterns:

```
feature/
├── data/
│   ├── datasources/
│   │   ├── remote_data_source.dart           # API calls
│   │   └── local_data_source.dart            # Cache operations
│   ├── models/
│   │   └── model.dart                        # JSON-serializable models
│   └── repositories/
│       └── repository_impl.dart              # Repository implementation
│
├── domain/
│   ├── entities/
│   │   └── entity.dart                       # Business logic models
│   ├── repositories/
│   │   └── repository.dart                   # Abstract interface
│   └── usecases/
│       └── usecase.dart                      # Business logic actions
│
└── presntation/
    ├── manger/
    │   ├── bloc/
    │   │   └── feature_bloc.dart             # Event-driven state
    │   └── cubit/
    │       └── feature_cubit.dart            # Method-driven state
    └── views/
        ├── feature_view.dart                 # Screen widgets
        └── widgets/
            └── custom_widget.dart            # Reusable components
```

---

## 🏗 Architecture

### Design Pattern: Clean Architecture

Go Dawa follows **Uncle Bob's Clean Architecture** principles, ensuring:
- ✅ **Independence of Frameworks** — easy to swap UI/API layers
- ✅ **Testability** — business logic isolated from UI/network
- ✅ **Independence of UI** — UI changes don't affect business logic
- ✅ **Independence of Database** — storage implementation can change
- ✅ **Independence of Entities** — core business rules remain stable

### Layered Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                   🎨 PRESENTATION LAYER                      │
│  Widgets (Views) ⇄ BLoC/Cubit (State Management)            │
│                                                              │
│  - Flutter Widgets          - User Interactions            │
│  - Navigation               - State Updates                │
│  - UI Logic                 - Data Binding                 │
└─────────────────┬───────────────────────────────────────────┘
                  │
┌─────────────────┴───────────────────────────────────────────┐
│                    🎯 DOMAIN LAYER                             │
│  Business Logic ⇄ Entities ⇄ Repositories (Abstract)        │
│                                                              │
│  - Entities                 - Use Cases                    │
│  - Repository Interfaces    - Business Rules              │
│  - No Framework Deps        - Platform-Independent        │
└─────────────────┬───────────────────────────────────────────┘
                  │
┌─────────────────┴───────────────────────────────────────────┐
│                    📊 DATA LAYER                              │
│  Repository Implementations ⇄ Models ⇄ Data Sources          │
│                                                              │
│  - Concrete Repositories   - Remote/Local Sources         │
│  - Models (JSON/DB)        - API & Cache Management      │
│  - Data Source Contracts   - Platform-Specific Code       │
└─────────────────────────────────────────────────────────────┘
```

### Data Flow Architecture

```
┌──────────┐         ┌──────────┐         ┌──────────────┐
│   View   │ ──────▶ │ BLoC /   │ ──────▶ │  Repository  │
│ (Widget) │◀────── │ Cubit    │◀────── │ (Abstract)   │
└──────────┘ Events  └──────────┘ Calls   └──────┬───────┘
                                                  │
                                  ┌───────────────┼──────────────┐
                                  ▼               ▼              ▼
                              ┌─────────┐   ┌──────────┐   ┌──────────┐
                              │  Dio    │   │ Shared   │   │  Local   │
                              │ Http    │   │ Prefs    │   │Database  │
                              │ Client  │   │ Cache    │   │ (Hive)   │
                              └─────────┘   └──────────┘   └──────────┘
```

### Error Handling Strategy

```
API Request
    │
    ├─ Success (200-299)
    │   └─ Parse & Cache ──▶ Return Right(Data)
    │
    ├─ Client Error (400-499)
    │   └─ DioHandler ──▶ User-Friendly Message ──▶ Return Left(Error)
    │
    ├─ Server Error (500-599)
    │   └─ Retry Logic ──▶ If 401: Auto-Refresh Token ──▶ Retry
    │
    └─ Network Error
        └─ ConnectivityService ──▶ Show Offline Screen
```

### State Management Architecture

```
(Event-Driven BLoC)
User Action ──▶ Event ──▶ BLoC ──▶ Repository ──▶ API/Cache
                           │                        │
                           │◀──────────────────────┘
                           │
                           ▼
                       State (Immutable)
                           │
                           ▼
                       Listener Re-builds UI

(Method-Driven Cubit)
User Action ──▶ Method ──▶ Repository ──▶ API/Cache
                Cubit        │              │
                           emit()      ◀──┘
                             │
                             ▼
                         State Update
                             │
                             ▼
                        Listener Re-builds UI
```

---

## 🛠 Tech Stack

### 🎨 UI & Framework

| Package | Version | Purpose |
|---------|---------|---------|
| **Flutter** | 3.x | Cross-platform UI framework |
| **Dart** | ^3.9.2 | Programming language |
| **flutter_svg** | ^2.2.1 | SVG asset rendering |
| **google_fonts** | ^6.3.3 | Premium typography |
| **flutter_zoom_drawer** | ^3.2.0 | Animated side drawer |
| **dots_indicator** | ^4.0.1 | Carousel pagination |
| **easy_stepper** | ^0.9.1 | Step-by-step UI |
| **flutter_spinkit** | ^5.2.2 | Loading animations |
| **percent_indicator** | ^4.2.3 | Progress indicators |
| **flutter_rating_bar** | ^4.0.1 | Star rating widget |
| **quickalert** | ^1.1.0 | Beautiful alert dialogs |
| **avatar_glow** | ^3.0.1 | Glowing avatar effects |
| **dotted_border** | ^3.1.0 | Dotted border decoration |
| **infinite_scroll_pagination** | ^5.1.1 | Paginated list views |
| **dropdown_search** | ^6.0.2 | Searchable dropdowns |
| **birth_picker** | ^1.2.0 | Date selection widget |
| **pull_to_refresh_flutter3** | ^2.0.2 | Pull-to-refresh functionality |

### 🧠 State Management & Architecture

| Package | Version | Purpose |
|---------|---------|---------|
| **flutter_bloc** | ^9.1.1 | BLoC state management pattern |
| **get_it** | ^9.0.5 | Service locator / dependency injection |
| **dartz** | ^0.10.1 | Functional programming utilities (Either type) |

### 🌐 Networking & HTTP

| Package | Version | Purpose |
|---------|---------|---------|
| **dio** | ^5.9.0 | Advanced HTTP client |
| **connectivity_plus** | ^7.0.0 | Network status monitoring |

### 💾 Storage & Caching

| Package | Version | Purpose |
|---------|---------|---------|
| **shared_preferences** | ^2.5.3 | Key-value persistent storage |
| **hive** | ^2.2.3 | Fast local NoSQL database |
| **hive_flutter** | ^1.1.0 | Hive Flutter integration |

### 🔥 Firebase & Push Notifications

| Package | Version | Purpose |
|---------|---------|---------|
| **firebase_core** | ^4.2.1 | Firebase SDK initialization |
| **firebase_messaging** | ^16.0.4 | Push notifications (FCM) |
| **flutter_local_notifications** | ^19.5.0 | Local notification display |

### 🎙️ Voice & Media

| Package | Version | Purpose |
|---------|---------|---------|
| **speech_to_text** | ^7.3.0 | Speech recognition engine |
| **flutter_sound** | ^9.2.13 | Audio recording & playback |
| **just_audio** | ^0.9.36 | Professional audio player |
| **siri_wave** | ^2.3.0 | Voice recording waveform animation |
| **image_picker** | ^1.2.1 | Camera & gallery image selection |
| **file_picker** | ^10.3.8 | Document & file selection |

### 🔧 Utilities & Tools

| Package | Version | Purpose |
|---------|---------|---------|
| **flutter_localizations** | SDK | i18n framework |
| **path_provider** | ^2.1.3 | File system paths |
| **permission_handler** | ^12.0.1 | Runtime permissions |
| **device_info_plus** | ^12.3.0 | Device metadata |
| **device_marketing_names** | ^1.1.6 | Device model names |
| **open_filex** | ^4.7.0 | Open files with native apps |
| **url_launcher** | ^6.3.2 | Deep linking & URLs |
| **device_preview** | ^1.3.1 | Multi-device testing |

### 📚 Development & Testing

| Package | Version | Purpose |
|---------|---------|---------|
| **flutter_test** | SDK | Unit & widget testing |
| **flutter_lints** | ^5.0.0 | Dart lint rules |
| **build_runner** | ^2.4.0 | Code generation |
| **hive_generator** | ^2.0.1 | Hive adapter generation |

---

## 📦 Feature Modules (Detailed)

Each module is architected as a self-contained feature with minimal coupling to other features.

### 🔐 Authentication (`auth/`)

Complete user authentication and session management:

**Flows:**
- User Registration → Email OTP Verification → Profile Setup
- User Login → Token Storage → Auto-Token Refresh
- Forgot Password → OTP Verification → Reset Password
- Change Password (authenticated users)

**State Managers:**
- `LoginCubit` — login state & API calls
- `SignupCubit` — registration flow
- `OtpCubit` — OTP verification
- `PasswordRecoveryCubit` — password reset flow
- `UserCubit` — user profile management
- `LogoutCubit` — session logout

**Security:**
- JWT Bearer tokens
- Automatic token refresh on 401
- Secure token storage (SharedPreferences)
- OTP email verification

---

### 🏠 Home (`home/`)

Main app dashboard and navigation hub

**Components:**
- Bottom navigation bar (5+ sections)
- Side drawer menu
- Quick-action buttons
- Order creation shortcuts (search, voice, file)
- Notifications badge
- User profile access

---

### 🔍 Search Product (`search_produict/`)

Advanced pharmaceutical product discovery — **most complex feature**

**Capabilities:**
- Real-time product search with suggestions
- Multi-filter interface:
  - By Supplier
  - By Manufacturer
  - By Warehouse
  - By Category
- Availability cross-check
- Price comparison matrix
- Product detail views
- Reviews & ratings
- Bulk add-to-cart
- Recent searches history
- Favorite products

**State Managers:**
- `SearchProductBloc` — search & filtering
- `SupplierDropdownCubit` — supplier selection
- `ManufacturerCubit` — manufacturer filtering
- `WarehouseCubit` — warehouse selection

---

### 🛒 Cart (`cart/`)

Shopping cart management with warehouse grouping

**Features:**
- Item add/update/delete
- Warehouse-grouped organization
- Quantity adjustments
- Price recalculation
- Clear cart (per warehouse)
- Bulk operations
- Checkout flow
- Cart persistence

**State Manager:**
- `CartBloc` — cart state & operations

---

### 📦 Orders (`orders/`)

Complete order lifecycle management

**Workflows:**
1. **Order Checkout**
   - Confirm items & quantities
   - Select delivery warehouse
   - Apply discounts/promotions
   - Confirm order

2. **Order Tracking**
   - Order list (paginated)
   - Status timeline visualization
   - Order details view
   - Delivery confirmation
   - Rating & reviews

3. **Order History**
   - Filter by status (active, delivered, cancelled)
   - Search by order number
   - Invoice download (PDF/Excel)

**State Managers:**
- `OrdersBloc` — order list & tracking
- `CheckoutBloc` — checkout process

---

### 🏭 Warehouse (`wharehouse/`)

Supplier and warehouse discovery

**Features:**
- Warehouse/supplier browser
- Search & filtering by:
  - Name
  - Product category
  - Manufacturer
- Product catalog per warehouse
- Delivery round information
- Pricing comparison
- Direct warehouse ordering

**State Manager:**
- `WharehouseBloc` — warehouse data & navigation

---

### 👤 Profile (`profile/`)

User account and application settings

**Elements:**
- Personal information display
- Email & phone editing
- Password management
- Language preference (AR/EN)
- Username customization
- Contact us form
- Terms & conditions
- Privacy policy
- About app information

---

### 🔔 Notifications (`notification/`)

Notification center and management

**Features:**
- Paginated notification list
- Mark as read/unread
- Delete individual notifications
- Clear all notifications
- Notification type badges
- Timestamp display
- Firebase integration
- Read statistics

**State Manager:**
- `NotificationBloc` — notification list & operations

---

### ↩️ Returns (`returns_approval/`)

Product return and exchange workflow

**Process:**
1. Select warehouse
2. Choose invoice
3. Select items to return
4. Specify return reason
5. Submit return request
6. Track return status

**State Managers:**
- `ReturnsapprovalBloc` — return processing
- `WarehouseDropdownCubit` — warehouse selection

---

### ⚡ Flash Offers (`flash_offers/`)

Promotional and limited-time deals

**Features:**
- Browse current offers
- View offer details
- Countdown timers
- Quick add-to-cart
- Offer filtering

**State Manager:**
- `FlashOffersBloc` — offer list management

---

### 🌱 Seasonal Items (`Seasonal_items/`)

Seasonal and special pharmaceutical products

**Features:**
- Seasonal product catalog
- Category organization
- Product details
- Pricing & availability

**State Manager:**
- `SeasonalBlocBloc` — seasonal item list

---

### 💎 Top Profitable SKUs (`top_profitable_sKUs/`)

Business intelligence on profitable products

**Analytics:**
- Top-selling products
- Revenue metrics
- Profit margins
- Trend analysis

**State Manager:**
- `TopProfitableSkusBloc` — profitability data

---

### 📊 Quota Items (`couta_items/`)

Quota and allocation management

**Displays:**
- Allocated quota items
- Consumption tracking
- Limits & boundaries

**State Manager:**
- `CoutaBloc` — quota management

---

### 🎤 Voice Order (`create_order_voice/`)

AI-powered voice ordering system

**Technology:**
- Speech-to-text recognition
- Audio waveform visualization
- Voice file upload
- Server-side processing

**State Manager:**
- `CreateOrderVoiceBloc` — voice order handling

---

### 📁 File Order (`Create_order_File/`)

Bulk order creation via files/images

**Supports:**
- PDF file uploads
- Excel spreadsheet imports
- Image capture (camera/gallery)
- OCR processing (server-side)

**State Manager:**
- `CreateOrderFileBloc` — file processing

---

### ☎️ Telesales Call (`telly_sales_call/`)

Request callbacks from telesales team

**Features:**
- Callback request form
- Subject/reason specification
- Preferred time selection
- Request history
- Status tracking

**State Manager:**
- `TellysalesphonecallCubit` — call request management

---

### 📱 Active Devices (`active_devices/`)

Session and device management for security

**Capabilities:**
- View all logged-in devices
- Device name & OS info
- Last activity timestamp
- Revoke individual sessions
- Logout from all devices
- Session monitoring

**State Manager:**
- `ActiveDevicesCubit` — device session management

---

### 📜 Recent Supplies (`recent_supplies/`)

History of received supply orders

**Features:**
- Paginated supply history
- Filter by date range
- Filter by supplier
- Order details quick view

**State Manager:**
- `RecentSuppliesBloc` — supply history list

---

### 🚀 Splash (`Splash/`)

App launch and initialization screen

**Logic:**
- Firebase initialization check
- Token validation
- User session check
- Navigation routing
- 2-second delay for branding

---

### 🎬 Onboarding (`onboarding/`)

First-time user walkthrough experience

**Screens:**
- App feature introduction
- Benefits explanation
- Getting started guide
- Account creation CTA

---

### 📵 No Internet (`no_internet/`)

Offline screen with graceful degradation

**Features:**
- Offline indicator
- Connection status animation
- Retry button
- Offline functionality (where available)

---

## ⚙️ Core Services

### 🌐 API Service (`core/service/Api/`)

Centralized HTTP client with advanced features

**Components:**

1. **ApiService** — Singleton HTTP client
   ```
   Methods: get(), post(), put(), patch(), delete()
   Returns: Either<Errors, T> (Functional programming)
   Handles: Serialization, deserialization, error conversion
   ```

2. **DioInterceptor** — Request/Response interceptor
   ```
   Inbound:
   - Inject Bearer token from cache
   - Add device info headers (Name, OS, Model)
   - Set custom timeout (30 seconds)
   
   Outbound:
   - Analyze response status
   - Convert errors to custom exceptions
   - Auto-refresh token on 401 (hit /api/v1/Auth/refresh)
   - Retry request with new token
   ```

3. **DioHandler** — Exception mapping
   ```
   Network Error → "Check your internet connection"
   Timeout Error → "Request timeout, please try again"
   401 Error → "Unauthorized, please login again"
   500 Error → "Server error, try again later"
   ```

**Error Handling Flow:**

```
API Request
    │
    ├─ Connection Error
    │   └─ ConnectivityService.check()
    │       ├─ Online → Retry
    │       └─ Offline → Show Offline Screen
    │
    ├─ 401 Unauthorized
    │   └─ Auto-Refresh Token
    │       ├─ Success → Retry Original Request
    │       └─ Failure → Show Login Screen
    │
    ├─ Other HTTP Error (4xx, 5xx)
    │   └─ DioHandler.handle()
    │       └─ Convert to User-Friendly Message
    │
    └─ Success (2xx)
        └─ Parse & Cache
            └─ Return Data
```

---

### 💾 Cache Service (`core/service/Locale_storge/`)

Local data persistence and caching

**CacheNetwork Class** — SharedPreferences wrapper
- Token storage & retrieval
- Locale preference persistence
- Generic caching for key-value data
- Secure storage for sensitive data

**Standard Keys:**
```
token → User JWT token
refreshToken → Token refresh credential
locale → App language (ar/en)
deviceId → Unique device identifier
```

---

### 📡 Connectivity Service (`core/service/connectivity/`)

Network status monitoring with debouncing

**Features:**
- Streams connection status changes
- 10-second debounce (prevent spam)
- Singleton pattern
- Graceful offline handling
- Auto-retry on reconnection

**Usage:**
```
connectivityService.connectionStatusStream
    .listen((isConnected) {
        if (!isConnected) {
            Navigator.push(context, NoInternetScreen);
        }
    });
```

---

### 🔔 Notification Services (`core/service/notfications/`)

Push and local notification handling

**Components:**

1. **PushNotifications** — Firebase Cloud Messaging
   - Initialize FCM
   - Request permissions
   - Handle foreground messages
   - Extract token for server

2. **LocalNotificationWithFirebase** — Display notifications
   - Configure notification channels (Android)
   - Handle tap actions
   - Sound & vibration
   - Custom notification icons

3. **LocaleNotifications** — Notification configuration
   - Channel setup
   - Sound mapping
   - Importance levels

---

### 🛡️ Error Handling (`core/errors/`)

Custom exception framework

**Errors Class:**
```dart
class Errors implements Exception {
  final ErroesModles erroesMdeles;
  
  String get message => erroesMdeles.message;
  int? get statusCode => erroesMdeles.status;
}
```

**Error Conversion Pipeline:**
```
DioException
    │
    ├─ Type Identification
    │   ├─ Connection Error
    │   ├─ Timeout Error
    │   ├─ Response Error (HTTP)
    │   └─ Cancel Error
    │
    ├─ User-Friendly Message
    │   └─ Arabic/English Translation
    │
    └─ Wrapped in Errors Class
        └─ Converted to Either<Errors, T>
```

---

### 🔧 Dependency Injection (`core/utils/get_it.dart`)

Service locator pattern using GetIt

**Registration:**
```
Lazy Singletons:
- ApiService
- AuthRepository
- ActiveDevicesRepository

Factories:
- All Cubits (new instance per access)
- State managers
```

**Usage Pattern:**
```dart
final apiService = getIt<ApiService>();
final loginCubit = getIt<LoginCubit>();
```

---

## 🔄 State Management

### BLoC Pattern Architecture

The app implements **event-driven BLoC** and **method-driven Cubit** patterns:

| Strategy | When to Use | Example |
|----------|------------|---------|
| **BLoC (Event-Driven)** | Complex state flows, event sequencing | SearchBloc, OrdersBloc |
| **Cubit (Method-Driven)** | Simple operations, direct method calls | LoginCubit, SignupCubit |

### Global State Managers (Registered in main.dart)

```
MultiBlocProvider(
  providers: [
    // Authentication
    BlocProvider<LoginCubit>(create: (context) => getIt<LoginCubit>()),
    BlocProvider<SignupCubit>(create: (context) => getIt<SignupCubit>()),
    BlocProvider<LogoutCubit>(create: (context) => getIt<LogoutCubit>()),
    
    // Cart & Orders
    BlocProvider<CartBloc>(create: (context) => getIt<CartBloc>()),
    BlocProvider<OrdersBloc>(create: (context) => getIt<OrdersBloc>()),
    BlocProvider<CheckoutBloc>(create: (context) => getIt<CheckoutBloc>()),
    
    // Search & Warehouse
    BlocProvider<SearchProductBloc>(create: (context) => getIt<SearchProductBloc>()),
    BlocProvider<WarehouseBloc>(create: (context) => getIt<WarehouseBloc>()),
    
    // Notifications & Others
    BlocProvider<NotificationBloc>(create: (context) => getIt<NotificationBloc>()),
    // ... 14 more BLoCs
  ],
  child: MaterialApp(...)
)
```

### State Listener Pattern

```dart
// BLoC Usage
BlocListener<SearchProductBloc, SearchProductState>(
  listener: (context, state) {
    if (state is SearchProductLoaded) {
      // Update UI
    } else if (state is SearchProductError) {
      // Show error
    }
  },
  child: BlocBuilder<SearchProductBloc, SearchProductState>(
    builder: (context, state) {
      return buildUI(state);
    }
  )
)

// Cubit Usage
CubitListener<LoginCubit, LoginState>(
  listener: (context, state) {
    if (state.isAuthenticated) {
      Navigator.pushReplacementNamed(context, homeRoute);
    }
  },
  child: CubitBuilder<LoginCubit, LoginState>(
    builder: (context, state) {
      return LoginForm(state: state);
    }
  )
)
```

---

## 🚀 Getting Started

### System Requirements

| Requirement | Version |
|-------------|---------|
| **Flutter SDK** | 3.0.0+ |
| **Dart SDK** | 3.9.2+ |
| **Java Development Kit** | 17+ |
| **Android SDK** | 21+ (API level) |
| **iOS** | 13.0+ |
| **VS Code** / **Android Studio** / **Xcode** | Latest |

### Installation Steps

#### 1️⃣ Clone Repository

```bash
# Clone the project
git clone https://github.com/GODAWA-TECH/flutter---godawa.git

# Navigate to project
cd godawa_app

# Switch to main branch
git checkout main
```

#### 2️⃣ Install Flutter Dependencies

```bash
# Update Flutter
flutter upgrade

# Get all dependencies
flutter pub get

# Download transitive dependencies
flutter pub outdated  # Check for updates (optional)
```

#### 3️⃣ Generate Code

```bash
# Generate localization files (AR/EN)
flutter gen-l10n

# Generate Hive adapters (if using local database)
dart run build_runner build --delete-conflicting-outputs
```

#### 4️⃣ Configure Firebase

```bash
# (Firebase files already present in repo)
# Verify android/app/google-services.json exists
# Verify ios/Runner/GoogleService-Info.plist exists
```

#### 5️⃣ Run on Device/Emulator

```bash
# List available devices
flutter devices

# Run on specific device
flutter run -d <device_id>

# Run with specific flavor (if configured)
flutter run --flavor production

# Run with logs
flutter run -v

# Run with hot reload enabled (default)
flutter run
```

### Build for Release

```bash
# Android APK (single architecture)
flutter build apk --release

# Android App Bundle (recommended for Play Store)
flutter build appbundle --release

# iOS (requires Mac)
flutter build ios --release

# View generated artifacts
# Android: build/app/outputs/flutter-apk/*.apk
# iOS: build/ios/ipa/*.ipa
```

---

## ⚙️ Configuration

### Firebase Configuration

Firebase is pre-configured, but you can update:

**Android:**
- File: `android/app/google-services.json`
- Update with your Firebase project credentials

**iOS:**
- File: `ios/Runner/GoogleService-Info.plist`
- Update with your Firebase project credentials

**Configuration Class:**
```dart
// lib/firebase_options.dart
// Auto-generated by FlutterFire CLI
// Contains platform-specific Firebase config
```

### API Configuration

**Base URL & Constants:**

```dart
// lib/constances.dart
static const String baseurl = "https://instadawa11.azurewebsites.net";
static const String token = "token";
static const String refreshToken = "refreshToken";
static const String locale = "locale";
```

**Custom Base URL:**
1. Update `lib/constances.dart`
2. Update Firebase project config
3. Update Interceptor headers if needed
4. Rebuild app

### Android Signing (Release Builds)

**Keystore File:**
```properties
# android/key.properties
keyAlias=godawa_release
keyPassword=YOUR_PASSWORD
storeFile=/path/to/keystore.jks
storePassword=YOUR_PASSWORD
```

**Generate Keystore:**
```bash
keytool -genkey -v -keystore ~/godawa_keystore.jks \
  -keyalg RSA -keysize 2048 -validity 10000 \
  -alias godawa_release
```

### Environment Variables

Create `.env` file in project root (not in VCS):

```env
# API Configuration
API_BASE_URL=https://instadawa11.azurewebsites.net
API_TIMEOUT=30

# Firebase
FIREBASE_PROJECT_ID=godawa-9b0e9

# Feature Flags
ENABLE_VOICE_ORDERING=true
ENABLE_FILE_ORDERING=true
ENABLE_ANALYTICS=true

# Logging
LOG_LEVEL=info
```

---

## 🌍 Localization (i18n)

### Supported Languages

| Language | Code | Status |
|----------|------|--------|
| **English** | en | ✅ Complete |
| **Arabic** | ar | ✅ Complete (RTL) |

### Configuration

**l10n.yaml** — Localization setup:
```yaml
arb-dir: lib/l10n
template-arb-file: intl_en.arb
output-localization-file: app_localizations.dart
output-class: S
synthetic-locale: false
```

### ARB File Structure

**lib/l10n/intl_en.arb** (English template):
```json
{
  "helloWorld": "Hello World",
  "welcomeMessage": "Welcome to {appName}",
  "@welcomeMessage": {
    "description": "Greeting message",
    "placeholders": {
      "appName": {
        "type": "String"
      }
    }
  }
}
```

**lib/l10n/intl_ar.arb** (Arabic translation):
```json
{
  "helloWorld": "مرحبا بالعالم",
  "welcomeMessage": "أهلا وسهلا في {appName}"
}
```

### Usage in Code

```dart
import 'package:godawa_app/generated/l10n.dart';

// In widgets
Text(S.of(context).helloWorld)

// With parameters
Text(S.of(context).welcomeMessage(appName: 'Go Dawa'))

// Change language
MyApp.of(context).setLocale(Locale('ar'));
```

### Adding New Translations

1. Update `intl_en.arb` with new key
2. Update `intl_ar.arb` with Arabic translation
3. Run: `flutter gen-l10n`
4. New string available in `S.of(context)`

---

## 📡 API Reference

### Base URL

```
https://instadawa11.azurewebsites.net/api/v1
```

### Request Headers

All authenticated requests include:

```http
Authorization: Bearer <jwt_token>
X-Device-Name: <device_name>
X-OS-Name: <os_type>
X-Device-Model: <model_name>
Content-Type: application/json
```

### Authentication Endpoints

| Method | Endpoint | Description | Auth |
|--------|----------|-------------|------|
| `POST` | `/Auth/login` | User login | ❌ |
| `POST` | `/Auth/register` | Register account | ❌ |
| `POST` | `/Auth/verify-otp` | Verify OTP code | ❌ |
| `POST` | `/Auth/forget-password` | Request password reset | ❌ |
| `POST` | `/Auth/verify-reset-otp` | Verify reset OTP | ❌ |
| `POST` | `/Auth/reset-password` | Complete password reset | ❌ |
| `POST` | `/Auth/refresh` | Refresh access token | ✅ |
| `GET` | `/Auth/profile` | Get user profile | ✅ |
| `PUT` | `/Auth/profile` | Update profile | ✅ |
| `PUT` | `/Auth/change-password` | Change password | ✅ |

### Product & Search Endpoints

| Method | Endpoint | Description | Auth |
|--------|----------|-------------|------|
| `GET` | `/Products/search` | Search products | ✅ |
| `GET` | `/Products/{id}` | Get product details | ✅ |
| `GET` | `/Suppliers` | List suppliers | ✅ |
| `GET` | `/Warehouses` | List warehouses | ✅ |
| `GET` | `/Categories` | List categories | ✅ |

### Order Endpoints

| Method | Endpoint | Description | Auth |
|--------|----------|-------------|------|
| `POST` | `/Orders` | Create order | ✅ |
| `GET` | `/Orders` | List user orders | ✅ |
| `GET` | `/Orders/{id}` | Get order details | ✅ |
| `PUT` | `/Orders/{id}/cancel` | Cancel order | ✅ |
| `GET` | `/Orders/{id}/invoice` | Download invoice | ✅ |

### Notification Endpoints

| Method | Endpoint | Description | Auth |
|--------|----------|-------------|------|
| `GET` | `/Notifications` | List notifications | ✅ |
| `PUT` | `/Notifications/{id}/read` | Mark as read | ✅ |
| `DELETE` | `/Notifications/{id}` | Delete notification | ✅ |

### Response Format

**Success Response (200-299):**
```json
{
  "success": true,
  "statusCode": 200,
  "message": "Operation successful",
  "data": {
    "id": "123",
    "name": "Product Name"
  }
}
```

**Error Response (400+):**
```json
{
  "success": false,
  "statusCode": 400,
  "message": "Validation failed",
  "errors": [
    {
      "field": "email",
      "message": "Invalid email format"
    }
  ]
}
```

---

## 🔐 Security & Authentication

### Authentication Flow

```
┌──────────────────────────────────────────────────┐
│              User Authentication Flow             │
└──────────────────────────────────────────────────┘

1. REGISTRATION
   User Input → Validation → POST /Auth/register
   ├─ Response: Success → Send OTP Email
   └─ Response: Error → Show Form Error

2. OTP VERIFICATION
   Check Email → Enter OTP → POST /Auth/verify-otp
   ├─ Response: Success → Auto-login
   └─ Response: Error → Request new OTP

3. LOGIN
   Email + Password → POST /Auth/login
   ├─ Response: Success
   │   ├─ Parse JWT token
   │   ├─ Store in SharedPreferences
   │   ├─ Set Bearer header
   │   └─ Navigate to Home
   └─ Response: Error → Show Login Error

4. TOKEN STORAGE
   SharedPreferences
   ├─ "token" (AccessToken)
   ├─ "refreshToken" (RefreshToken)
   └─ "tokenExpiry" (Timestamp)

5. API REQUESTS
   BLoC → Repository → ApiService
   ├─ DioInterceptor injects Bearer token
   ├─ Sets Device Info headers
   └─ Sends request

6. AUTO-TOKEN REFRESH
   Response: 401 Unauthorized
   ├─ Trigger → POST /Auth/refresh
   ├─ Update token in cache
   ├─ Retry original request
   └─ Response: Success/Redirect to Login

7. LOGOUT
   Post → /Auth/logout
   ├─ Clear tokens from SharedPreferences
   ├─ Clear BLoC state
   └─ Navigate to Splash → Login
```

### Security Features

| Feature | Implementation | Level |
|---------|-----------------|-------|
| **JWT Authentication** | Bearer token in Authorization header | 🔒 High |
| **Auto Token Refresh** | Dio interceptor handles 401 responses | 🔒 High |
| **Device Tracking** | Device Name, OS, Model in headers | 🔒 High |
| **Secure Storage** | SharedPreferences encryption (OS-level) | 🔒 Medium |
| **HTTPS** | All API communication over TLS | 🔒 High |
| **OTP Verification** | Email-based one-time passwords | 🔒 High |
| **Session Management** | Active device tracking & revocation | 🔒 High |
| **Input Validation** | Client-side validation on all forms | 🔒 Medium |

### Token Refresh Mechanism

```dart
// Pseudo-code: DioInterceptor token refresh logic

onResponse(response) {
  if (response.statusCode == 401) {
    // Token expired
    try {
      refreshToken = getFromCache('refreshToken');
      newToken = await apiService.post('/Auth/refresh', {
        refreshToken: refreshToken
      });
      
      // Update cache
      await cache.save('token', newToken);
      
      // Retry original request
      return retryRequest(originalRequest);
      
    } catch (error) {
      // Refresh failed → redirect to login
      navigateTo(LoginScreen);
    }
  }
}
```

---

## 🎨 UI Theme & Design

### Color Palette

| Color | Hex | Usage |
|-------|-----|-------|
| **Primary Purple** | `#4937BB` | Main buttons, headers, appbar |
| **Light Background** | `#F5F7FA` | Page backgrounds |
| **Dark Text** | `#1F2937` | Body text |
| **Light Gray** | `#E5E7EB` | Borders, dividers |
| **Success Green** | `#10B981` | Confirmations, success states |
| **Warning Orange** | `#F59E0B` | Alerts, warnings |
| **Error Red** | `#EF4444` | Errors, destructive actions |

### Typography

- **Font Family**: Google Fonts (customizable)
- **Heading 1**: 32pt, Bold
- **Heading 2**: 24pt, SemiBold
- **Body**: 16pt, Regular
- **Small**: 12pt, Regular

### Component Library

| Component | Purpose | File |
|-----------|---------|------|
| `CustomAppBar` | Standard app header | `core/utils/custom_widgets.dart` |
| `CustomButton` | Styled button | `core/utils/custom_widgets.dart` |
| `CustomTextField` | Form input field | `core/utils/custom_widgets.dart` |
| `LoadingWidget` | Loading animation | `core/utils/custom_widgets.dart` |
| `ErrorWidget` | Error display | `core/utils/custom_widgets.dart` |
| `EmptyStateWidget` | Empty list state | `core/utils/custom_widgets.dart` |

### Responsive Design

```dart
// Using size_config for responsive UI
SizeConfig.isMobilePortrait  // Mobile portrait
SizeConfig.isMobileLandscape // Mobile landscape
SizeConfig.isTablet          // Tablet devices

// Responsive padding
padding: EdgeInsets.all(SizeConfig.defaultSize * 2.0)

// Responsive fonts
fontSize: SizeConfig.defaultSize * 1.8
```

---

## 🧪 Testing

### Testing Strategy

#### Unit Tests
- Test business logic (usecases, repositories)
- Mock external dependencies
- Test error scenarios
- Location: `test/`

#### Widget Tests
- Test UI widgets in isolation
- Test routing
- Test state changes
- Location: `test/`

#### Integration Tests
- Test complete user flows
- Test API integration
- Test state management flows
- Location: `integration_test/`

### Running Tests

```bash
# Run all unit & widget tests
flutter test

# Run specific test file
flutter test test/features/auth/login_test.dart

# Run with coverage
flutter test --coverage

# Run integration tests
flutter drive --target=integration_test/app_test.dart
```

### Example Unit Test

```dart
import 'package:flutter_test/flutter_test.dart';
import 'package:mockito/mockito.dart';

// Setup
late MockAuthRepository mockAuthRepository;
late LoginCubit loginCubit;

setUp(() {
  mockAuthRepository = MockAuthRepository();
  loginCubit = LoginCubit(authRepository: mockAuthRepository);
});

test('LoginCubit emits error on failed login', () async {
  // Arrange
  when(mockAuthRepository.login(email, password))
      .thenThrow(Error('Invalid credentials'));
  
  // Act
  loginCubit.login(email, password);
  
  // Assert
  await expectLater(
    loginCubit.stream,
    emitsInOrder([
      isA<LoginLoading>(),
      isA<LoginError>(),
    ])
  );
});
```

---

## 📊 Project Statistics

| Metric | Value |
|--------|-------|
| **Total Screens** | 25+ |
| **Feature Modules** | 19 |
| **BLoCs/Cubits** | 24 |
| **Dependencies** | 45+  |
| **Lines of Code** | 10,000+ |
| **Code Coverage** | Pending |
| **Min SDK** | 21 (Android), 13 (iOS) |
| **Supported Languages** | 2 (EN, AR) |
| **Firebase Features** | Push Notifications, Analytics |

---

## ❓ Troubleshooting

### Build Issues

**Q: "flutter pub get" fails**
```bash
# Clear cache and retry
flutter clean
rm -rf pubspec.lock
flutter pub get
```

**Q: "Command 'flutter' not found"**
```bash
# Add Flutter to PATH
export PATH="$PATH:/path/to/flutter/bin"

# Or use full path
/path/to/flutter/bin/flutter run
```

### Runtime Issues

**Q: App crashes on startup**
- Check Firebase configuration files
- Verify internet connection
- Check device logs: `flutter logs`
- Clear app data: `adb shell pm clear com.example.godawa_app`

**Q: Push notifications not working**
- Verify Firebase project ID
- Check Firebase Messaging token
- Verify notification permission
- Check notification channel configuration

**Q: Localization not updating**
```bash
# Regenerate i18n files
flutter gen-l10n

# Clean and rebuild
flutter clean
flutter pub get
flutter run
```

### Device Issues

**Q: Can't find connected device**
```bash
# List devices
flutter devices

# Enable developer mode (Android)
# Settings > About > Build Number (tap 7 times) > Developer Options

# Check USB connection
adb devices
```

---

## 🤝 Contributing Guidelines

### Code Style

- Follow Dart conventions
- Use meaningful variable names
- Document public methods with `///`
- Maintain Clean Architecture
- Keep methods under 30 lines

### Commit Convention

```bash
# Format: <type>(<scope>): <message>

git commit -m "feat(auth): implement login with email verification"
git commit -m "fix(search): resolve product filter bug"
git commit -m "refactor(cart): simplify warehouse grouping logic"
git commit -m "docs(readme): update API documentation"
```

**Types**: `feat`, `fix`, `refactor`, `docs`, `test`, `chore`

### Pull Request Process

1. Create feature branch: `git checkout -b feat/feature-name`
2. Implement changes following code style
3. Run tests: `flutter test`
4. Commit changes with conventional messages
5. Push to repository: `git push origin feat/feature-name`
6. Create Pull Request with description
7. Request code review
8. Address review feedback
9. Merge after approval

### Code Review Checklist

- [ ] Follows Clean Architecture
- [ ] Proper error handling
- [ ] Adequate comments/documentation
- [ ] No magic numbers or strings (use constants)
- [ ] Tests written for new features
- [ ] No console.log or debug statements
- [ ] Follows naming conventions
- [ ] No breaking changes

---



<div align="center">

### Made with ❤️ by Go Dawa Team

[Twitter](https://twitter.com) • [LinkedIn](https://linkedin.com) • [Website](https://godawa-pharma.com)

**License**: This project is proprietary software.

**Last Updated**: April 2026

</div>
