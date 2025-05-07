
# بررسی لیست مخازن YUM در CentOS 7

در این مستند نحوه بررسی و مدیریت مخازن YUM در سیستم‌عامل CentOS 7 آموزش داده می‌شود.

---

## 🧭 مسیر لیست مخازن فعال

برای مشاهده لیست مخازن فعال YUM، از دستور زیر استفاده کنید:

```bash
yum repolist
```

### خروجی نمونه:

```text
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: mirror.ir.co
 * extras: mirror.ir.co
 * updates: mirror.ir.co
repo id               repo name                            status
base/7/x86_64         CentOS-7 - Base                      10,070
extras/7/x86_64       CentOS-7 - Extras                      500
updates/7/x86_64      CentOS-7 - Updates                   1,250
repolist: 11,820
```

---

## 📁 محل فایل‌های تنظیمات مخزن

فایل‌های مخزن در مسیر زیر قرار دارند:

```bash
/etc/yum.repos.d/
```

در این مسیر می‌توانید فایل‌های `.repo` مربوط به هر مخزن را مشاهده و ویرایش کنید.

---

## ⚙️ بررسی جزئیات مخازن

برای مشاهده جزئیات بیشتر از هر مخزن:

```bash
yum repoinfo
```

---

## 🔄 بروزرسانی لیست مخازن

برای بروزرسانی کش YUM:

```bash
yum clean all
yum makecache
```

---

## 🚫 غیرفعال کردن یک مخزن خاص

برای غیرفعال کردن یک مخزن، فایل مربوط به آن را در مسیر `/etc/yum.repos.d/` باز کرده و مقدار `enabled=1` را به `enabled=0` تغییر دهید.

---

**نکته:** مطمئن شوید که اتصال اینترنت برقرار است و DNS به درستی کار می‌کند تا لیست مخازن به درستی بارگذاری شود.

## آخرین فایل های به روز شده رو میتونید از همینجا دانلود کنید
