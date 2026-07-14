# Smplifai — Test Suite

## Smplifai

### 1. Telefon nömrəsi

New application ucun sorğu yaradılarkən , qeyd olunan telefon nömrəsi yalnış daxil etdikdə keçərli olur.

**Test Case Metadata**

| Field | Value |
|---|---|
| Priority | high |
| Severity | critical |
| Type | functional |
| Behavior | negative |
| Automation | is-not-automated |
| Status | actual |
| Is Flaky | no |
| Layer | e2e |

**Preconditions:**

1.https://appstudentsecret.smplifai.com/auth/login daxil oluruq.

2.Sign in with Google.

3.Sağ yuxarı küncdə **+New application** buttona klik edirik.

**Steps:**

| # | Action | Data | Expected Result |
|---|---|---|---|
| 1 | New application üçün kontakt məlumatları istənilir | İstənilən nömrəni qeyd ediirik (+99411111111) | **Təsdiq edilir (Qeyd olunan nömrə səhvdir bildirisi olmalıdır)** |

---

### 2. Daxil edilən şəxsi sənədlər

Tələbələrin daxil etdikləri sənədlər arasında (Passport , Visa) kimi sənədlər bölməsinə yalnış sənədlər təqdim etdikdə keçərli sayılır.

**Test Case Metadata**

| Field | Value |
|---|---|
| Priority | high |
| Severity | critical |
| Type | functional |
| Behavior | negative |
| Automation | is-not-automated |
| Status | actual |
| Is Flaky | no |
| Layer | e2e |

**Preconditions:**

1.https://appstudentsecret.smplifai.com/auth/login saytda login olduq.

2.Açılan səhifədə **+New** **application** buttona klik edirik.

**Steps:**

| # | Action | Data | Expected Result |
|---|---|---|---|
| 1 | 1.+New application bölməsində təsdiq uçün telefon nömrəsi soruşulur. | +994552011063 | Təsdiq olunur və sənədləri daxil etmək üçün yeni səhifə açılır.<br><br>https://appstudentsecret.smplifai.com/ |
| 2 | Passport bölməsinə klik edirik. | - | **Yalnış sənəd yükləyirik və keçərli sayılır.** |
| 3 | Visa bölməsinə klik edirik. | - | **Yalnış sənəd yükləyirik və keçərli sayılır.** |
| 4 | Yükləndikdən sonra, **Submit document buttonu rəngi dəyişir** və buutton klik etmək üçün hazır olur.Submit document buttonu klik edirik | - | - |
| 5 | **Submit document** buttonu klik edirik | - | My application bölməsində sənədlərin yükləndiyini göstərən qovluq açılır. |

---

### 3. Sənədlərin destkopa yüklənməsi

Passport və Visa bölmələrinə daxil etdiyimiz sənədləri destkopa yükləmək

**Test Case Metadata**

| Field | Value |
|---|---|
| Priority | low |
| Severity | normal |
| Type | functional |
| Behavior | negative |
| Automation | is-not-automated |
| Status | actual |
| Is Flaky | no |
| Layer | e2e |

**Preconditions:**

1.https://appstudentsecret.smplifai.com/# login oluruq.

2.My application bölməsində müqavilə qovluğunu görürük.

**Steps:**

| # | Action | Data | Expected Result |
|---|---|---|---|
| 1 | View buttonuna klik edirik. | - | Təsdiqlənən sənədlər bölməsi açılır. |
| 2 | Hər bir sənədi view buttonuna klik edirik. | - | Klik etdikdə yüklənən sənədlər yeni səhifədə açılır. |
| 3 | Back buttonuna klik edirik. | - | My application bölməsi açılır. |
| 4 | **Download** buttonuna klik edirik. | - | Downloads səhifəsi açılır.**Yüklənən sənədlər görünmür.** |

---

### 4. Tələbə qeydiyyatı

Tələb olunan bölmələrə şəxsi məlumatlar yalnış yazıldıqda belə tələbə qeydiyyatdan keçirilir.

**Test Case Metadata**

| Field | Value |
|---|---|
| Priority | high |
| Severity | critical |
| Type | functional |
| Behavior | negative |
| Automation | is-not-automated |
| Status | actual |
| Is Flaky | no |
| Layer | e2e |

**Preconditions:**

1.https://appstudentsecret.smplifai.com/auth/login Daxil oluruq.

2.Click **Sign up here** button

**Steps:**

| # | Action | Data | Expected Result |
|---|---|---|---|
| 1 | Şəxsi məlumatlar bölməsini doldururuq. | (First name-AAA,Last name Email- elv@gmail.com,Phone- +994111111111,Password-12345678e,Repeat password-12345678e,and accept the terms and conditions | Şəxsi məlumatlar bölmələri uğurla qeyd olunur. |
| 2 | Click **Create account** button | - | Email təsdiqlənməsi bildirişi gəlir və Emailin yoxlanılması soruşulur. |

---
