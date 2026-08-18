# Mahob Khmer — គេហទំព័រភោជនីយដ្ឋាន (React + Firebase)

គម្រោងនេះសាងសង់ដោយ **React (Vite)** សម្រាប់ Frontend និង **Firebase** សម្រាប់ Backend (Authentication + Firestore Database)។

## មុខងារដែលមាន

- ទំព័រដើម, អំពីយើង, ទំនាក់ទំនង, មុខម្ហូប (Home, About, Contact, Services)
- ចូលគណនី / ចុះឈ្មោះ / ភ្លេចពាក្យសម្ងាត់ (Login / Register / Forgot Password) — ប្រើ Firebase Authentication
- Admin Dashboard សម្រាប់បន្ថែម / កែប្រែ / លុប មុខម្ហូប (CRUD) — ប្រើ Firestore Database
- ការការពារទំព័រ Admin (Protected Route) — ត្រូវ login សិនទើបចូលបាន

## របៀបដំណើរការនៅលើកុំព្យូទ័ររបស់អ្នក

### ជំហានទី ១៖ តំឡើង dependencies

```bash
npm install
```

### ជំហានទី ២៖ Setup Firebase (ចាំបាច់)

1. ចូលទៅ [https://console.firebase.google.com/](https://console.firebase.google.com/)
2. ចុច **Add project** ហើយបង្កើត project ថ្មី (ឧ. `mahob-khmer`)
3. នៅក្នុង project, ចុច **Web icon (`</>`)** ដើម្បីបន្ថែម Web App
4. ចម្លង `firebaseConfig` object ដែលបង្ហាញមក
5. បើកឯកសារ `src/firebase.js` ហើយជំនួសតម្លៃទាំងអស់ (`YOUR_API_KEY`...) ដោយតម្លៃពិតរបស់អ្នក
6. ក្នុង Firebase Console:
   - ចូល **Authentication → Sign-in method → Email/Password → Enable**
   - ចូល **Firestore Database → Create database → Start in test mode**

### ជំហានទី ៣៖ ដំណើរការ

```bash
npm run dev
```

បើកកម្មវិធីរុករកតាម URL ដែលបង្ហាញ (ជាធម្មតា `http://localhost:5173`)

### ជំហានទី ៤៖ Build សម្រាប់ដាក់ Production

```bash
npm run build
```

ឯកសារ build នឹងស្ថិតនៅក្នុង folder `dist/`

## រចនាសម្ព័ន្ធ Project

```
src/
  firebase.js          → Firebase configuration
  context/
    AuthContext.jsx     → គ្រប់គ្រង login state ទាំងមូល
  components/
    Navbar.jsx / .css
    Footer.jsx / .css
    ProtectedRoute.jsx  → ការពារទំព័រ Admin
  pages/
    Home.jsx            → ទំព័រដើម
    About.jsx           → អំពីយើង
    Contact.jsx          → ទំនាក់ទំនង
    Services.jsx         → មុខម្ហូប (ទាញពី Firestore)
    Login.jsx
    Register.jsx
    ForgotPassword.jsx
    AdminDashboard.jsx  → CRUD មុខម្ហូប
  App.jsx                → Routes ទាំងអស់
  main.jsx               → Entry point
```

## ជំហានបន្ថែម (សម្រាប់ Assignment)

តាមខ្លឹមសារក្នុង slide របស់អ្នក (Introduction, Literature Review, Methodology, Result/Demo,
Discussion, Conclusion) សូមថត screenshot នៃមុខងារនីមួយៗ (Home, Login, Admin Dashboard CRUD)
ដើម្បីដាក់ក្នុងផ្នែក **Result/Demo** នៃរបាយការណ៍របស់អ្នក។
