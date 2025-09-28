
# **IAM & Microsoft Entra ID – Detailed Notes**

---

## 🔹 IAM (Identity & Access Management)

IAM ka matlab hai **Identity aur Access ka control**.
Har Cloud Provider apna IAM service deta hai:

* **Azure → Microsoft Entra ID**
  (Pehle ise **Azure Active Directory** kehte the).
* **AWS → IAM (Identity & Access Management)**
* **GCP → Cloud IAM (Identity & Access Management)**

👉 Inka kaam ek hi hai: **user ko authenticate karna aur uske role ke hisaab se access dena**.

---

## 🔹 Microsoft Entra ID Basics

1. Jab bhi tum ek **Azure Account** banate ho, uske sath hi ek **Microsoft Entra ID Directory** automatically create ho jaati hai.
2. Ye directory ek **container hai jisme saare users, groups, apps aur permissions manage hote hain**.
3. Har directory ka ek **unique ID hota hai** jise **Tenant ID** bolte hain.

   * Example: `79f4fde6-66f2-4bdd-886e-45f7816be496`
4. Ek default domain bhi milta hai → `abc.onmicrosoft.com`

---

## 🔹 Society Example (Story se samjho)

Socho **Azure ek badi society hai** aur tumhara account us society me ek ghar.

* **Society (Azure Cloud)** → poora Azure environment.
* **Security Room (Entra ID)** → gate jahan guard check karega kaun andar aa raha hai.
* **Malik (Owner/Global Admin)** → society ka malik jo sab kuchh control kar sakta hai.
* **Naye members (Users)** → sirf wahi kaam karenge jo role unhe diya gaya hai.

👉 Jab koi aadmi society ke gate par aata hai:

* **Authentication** = guard check karta hai identity (username, password, OTP).
* **Authorization** = guard check karta hai ki aadmi andar aake sirf parking me jaa sakta hai ya club house bhi use kar sakta hai.

---

## 🔹 Authentication vs Authorization

* **Authentication** = Tum kaun ho? (username + password, MFA, token).
* **Authorization** = Tum kya kar sakte ho? (role ke hisaab se permissions).

---

## 🔹 Entra ID ke Important Roles

1. **Global Administrator** → full control (sab kuchh manage kar sakta hai).
2. **User Administrator** → users aur groups create/update/delete kar sakta hai.
3. **Authentication Administrator** → password reset, MFA registration manage karta hai.
4. **Billing Administrator** → subscription aur billing handle karta hai.
5. **Helpdesk/Password Administrator** → sirf password reset karne ka right.
6. **Application Administrator** → app registrations aur enterprise apps manage.
7. **Cloud Application Administrator** → app configuration aur user consent manage karta hai.
8. **Security Administrator** → security-related settings aur reports manage.
9. **Security Reader** → sirf read-only access deta hai security info ke liye.
10. **Global Reader** → tenant ka poora data read kar sakta hai par koi change nahi kar sakta.
11. **Privileged Role Administrator** → roles assign/remove karne ka right.
12. **Compliance Administrator** → compliance aur audit related kaam.
13. **Reports Reader** → sirf reports aur logs dekhne ka right.

👉 Example:

* Agar tumhe sirf billing dekhni hai → **Billing Admin** role milega.
* Agar tumhe sab kuchh control karna hai → **Global Admin** role milega.

---

## 🔹 Azure Resource Hierarchy

Azure me resources ek **hierarchy** ke hisaab se manage hote hain:

1. **Management Group** → sabse upar, multiple subscriptions ko group karta hai.
2. **Subscription** → billing aur policies apply hoti hain yaha.
3. **Resource Group** → logical container jisme resources rakhe jate hain.
4. **Resources** → VM, Storage, DB, App Services, etc.

👉 Example:

* Ek company ke paas 2 subscriptions ho sakti hain (Production aur Development).
* Dono subscription ek hi Management Group ke under aa sakti hain.

---

## 🔹 Licensing

* Har Azure Account me default **Microsoft Entra ID Free** license milta hai.
* Advanced features ke liye **Premium P1/P2 licenses** available hain.
