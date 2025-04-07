
# 📘 Méthode Merise — تعریف و توضیح کامل

---

## 🔷 مقدمه

**Méthode Merise** یک متدولوژی مدلسازی سیستم‌های اطلاعاتی است که در دهه 1980 در فرانسه توسعه یافت. هدف اصلی Merise، **جدا کردن داده‌ها از فرایندها** و **استفاده از چندین سطح مدل‌سازی** برای طراحی منظم، دقیق و ساخت‌یافته سیستم‌های اطلاعاتی است.

---

## 🧩 سطوح اصلی در Merise

Merise شامل سه سطح برای تحلیل داده‌ها و فرایندها است:

| سطح | داده‌ها | فرایندها |
|------|---------|-----------|
| سطح مفهومی | MCD (Modèle Conceptuel de Données) | MCT (Modèle Conceptuel des Traitements) |
| سطح منطقی | MLD (Modèle Logique de Données) | MOT (Modèle Organisationnel des Traitements) |
| سطح فیزیکی | MPD (Modèle Physique de Données) | MDT (Modèle des Traitements Détaillés) |

---

## 🔶 1. MCD – Modèle Conceptuel de Données

### 🎯 هدف:
تحلیل نیازهای داده‌ای کاربران بدون در نظر گرفتن جزئیات فنی.

### ✅ عناصر اصلی:
- **Entité (موجودیت):** مانند `Client`, `Produit`, `Commande`
- **Attribut (ویژگی):** ویژگی‌هایی مانند `nom`, `email`
- **Association (ارتباط):** روابط بین موجودیت‌ها مانند `passe commande`
- **Cardinalité:** تعداد عناصر مجاز در رابطه (مانند `1`, `N`)

---

## 🔷 2. MLD – Modèle Logique de Données

### 🎯 هدف:
تبدیل MCD به ساختار قابل پیاده‌سازی در پایگاه‌ داده رابطه‌ای.

### ✅ مشخصات:
- موجودیت‌ها تبدیل به **جداول** می‌شوند.
- تعیین **کلیدهای اصلی** و **خارجی**.
- تعریف روابط با استفاده از **جدول‌های واسط**.

### 🛠 مثال:
```sql
TABLE Client (
  id_client INT PRIMARY KEY,
  nom VARCHAR(100)
)
```

---

## 🔷 3. MPD – Modèle Physique de Données

### 🎯 هدف:
پیاده‌سازی پایگاه‌داده در یک سیستم مدیریت پایگاه‌داده خاص (مثل MySQL).

### ✅ مشخصات:
- تعیین نوع داده‌ها: `VARCHAR`, `INT`, `DATE`, ...
- تعریف constraints، index، collation و ...

---

## 🔷 4. MCT – Modèle Conceptuel des Traitements

### 🎯 هدف:
مدلسازی فعالیت‌هایی که کاربران با سیستم انجام می‌دهند.

### ✅ ابزارها:
- **DFD (Data Flow Diagram)**
- عملیات: ایجاد، جستجو، بروزرسانی، حذف

---

## 🔷 5. MOT – Modèle Organisationnel des Traitements

### 🎯 هدف:
مدیریت اجرای فرایندها بر اساس ساختار سازمانی.

### ✅ کاربرد:
- تعیین مسئول هر فعالیت
- توزیع وظایف بین واحدها

---

## 🔷 6. MDT – Modèle des Traitements Détaillés

### 🎯 هدف:
توضیح دقیق و فنی چگونگی اجرای فرایندها با الگوریتم‌ها و ترتیب گام‌ها.

---

## ✅ مزایای Merise

- جداسازی ساختار داده و فرایندها
- تسهیل همکاری تیمی بین تحلیل‌گران و توسعه‌دهندگان
- امکان مدیریت بهتر تغییرات
- مناسب برای پروژه‌های بزرگ و پیچیده

---

## 🛠 ابزارهای مورد استفاده در Merise

- **Looping**: طراحی MCD و تولید MLD/MPD
- **Win'Design**
- **PowerAMC / PowerDesigner**

---