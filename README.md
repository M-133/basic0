هذه مسائل مناسبة لمن درس ( المتغيرات - والشروط - والحلقات - والمصفوفات - الدوال )


بالطبع! فيما يلي مجموعة من المشاكل البرمجية المخصصة للمبتدئين في لغة C++. سأقدم لك كل مشكلة مع تفاصيل واضحة حول ما يجب القيام به دون تقديم الحل:

---

### **1. حساب متوسط ثلاثة أرقام**
**الوصف:**
قم بكتابة برنامج يطلب من المستخدم إدخال ثلاثة أرقام، ثم يقوم بحساب المتوسط الحسابي لهذه الأرقام وعرض النتيجة.

**التفاصيل:**
- قم بإنشاء متغيرات لتخزين الأرقام الثلاثة.
- استخدم دالة `cin` لأخذ القيم من المستخدم.
- احسب المتوسط باستخدام الصيغة: `(عدد1 + عدد2 + عدد3) / 3`.
- عرض النتيجة باستخدام دالة `cout`.


الحل

	double x, y, z;

	cout << "Enter 3 Num " << endl; 
	cout << "=========== " << endl;
	
	cout << "Enter Num 1 : ";
	cin >> x;
	cout << "Enter Num 2 : ";
	cin >> y;
	cout << "Enter Num 3 : ";
	cin >> z;

	double Average = (x + y + z) / 3;

	cout << "Average = " << Average << endl;


---

### **2. تحديد أكبر رقم بين رقمين**
**الوصف:**
قم بكتابة برنامج يطلب من المستخدم إدخال رقمين، ثم يحدد الرقم الأكبر بينهما ويقوم بطباعته.

**التفاصيل:**
- قم بإنشاء متغيرين لتخزين الرقمين.
- استخدم دالة `cin` لأخذ القيم من المستخدم.
- استخدم بنية if-else لمقارنة القيمتين.
- إذا كان الرقم الأول أكبر، قم بطباعته. وإذا كان الرقم الثاني أكبر، قم بطباعته.
  
الحل ب if

	
	double x, y;
	cout << "Enter First Number: ";
	cin >> x;
	cout << "Enter Sacand Number: ";
	cin >> y;


	if (x > y) {
		cout << "The Largest Number is: " << x << endl;
	}
	else if (x < y) {
		cout << "The Largest Number is: " << y << endl;
	}
	else {
		cout << "The Two Numbers are Equal" << endl;
	}
 
 الحل ب ال function
 ```
using namespace std;

static double Max(double x, double y) {
	return (x > y) ? x : y;
}

int main() {

	double x, y;
	cout << "Enter First Number: ";
	cin >> x;
	cout << "Enter Sacand Number: ";
	cin >> y;

	cout << "The Max Is : " << Max(x, y);

}
```

---

### **3. التحقق مما إذا كان الرقم زوجيًا أم فرديًا**
**الوصف:**
قم بكتابة برنامج يطلب من المستخدم إدخال رقم، ثم يتحقق مما إذا كان الرقم زوجيًا أم فرديًا.

**التفاصيل:**
- قم بإنشاء متغير لتخزين الرقم.
- استخدم دالة `cin` لأخذ الرقم من المستخدم.
- استخدم العملية `%` (modulo) للتحقق مما إذا كان الرقم قابلًا للقسمة على 2 بدون باقي.
- إذا كانت النتيجة صفرًا، فإن الرقم زوجي. وإلا فهو فردي.
- عرض النتيجة باستخدام دالة `cout`.

الحل
```
int main() {
	
	int x;

	cout << "Type Number : ";
	
	cin >> x;

	if (x % 2 == 0) {
		cout << "The number is even. " << endl;
	}
	else if (x % 2 == 1) {
		cout << "The number is odd. " << endl;
	}

}
```

---

### **4. حساب مساحة مستطيل**
**الوصف:**
قم بكتابة برنامج يطلب من المستخدم إدخال طول وعرض مستطيل، ثم يقوم بحساب مساحته.

**التفاصيل:**
- قم بإنشاء متغيرين لتخزين الطول والعرض.
- استخدم دالة `cin` لأخذ القيم من المستخدم.
- احسب المساحة باستخدام الصيغة: `مساحة = الطول * العرض`.
- عرض النتيجة باستخدام دالة `cout`.

```
static double Area(double x, double y) {
	return x * y;
}

int main() {
	
	double x , y;

	cout << "Type height : ";
	cin >> x;

	cout << "Type width : ";
	cin >> y;

	cout << "The Area is : " << Area(x,y) << endl;

}
```

---

### **5. تحويل درجات الحرارة من مئوي إلى فهرنهايت**
**الوصف:**
قم بكتابة برنامج يطلب من المستخدم إدخال درجة حرارة بالمئوية، ثم يقوم بتحويلها إلى درجة حرارة بمقاييس فهرنهايت.

**التفاصيل:**
- قم بإنشاء متغير لتخزين الدرجة المئوية.
- استخدم دالة `cin` لأخذ القيمة من المستخدم.
- استخدم الصيغة التالية للتحويل: `فهرنهايت = (9/5) * المئوية + 32`.
- عرض النتيجة باستخدام دالة `cout`.

الحل 
```
int main() {
	
	double x;

	cout << "Enter the Celsius temperature : ";
	cin >> x;

	double f = x * 1.8;

	cout << f + 32 << " degrees Fahrenheit." << endl;

}
```

---

### **6. جدول الضرب**
**الوصف:**
قم بكتابة برنامج يعرض جدول ضرب لأي رقم يدخله المستخدم.

**التفاصيل:**
- قم بإنشاء متغير لتخزين الرقم الذي سيستخدم لإنشاء جدول الضرب.
- استخدم دالة `cin` لأخذ الرقم من المستخدم.
- استخدم حلقة `for` لتكرار العمليات من 1 إلى 10.
- لكل تكرار، احسب الناتج باستخدام الصيغة: `الرقم * i` (حيث `i` هو العدد الحالي في الحلقة).
- عرض النتائج بشكل مرتب.

---

### **7. معرفة إذا كان الرقم موجبًا، سالبًا أم صفر**
**الوصف:**
قم بكتابة برنامج يطلب من المستخدم إدخال رقم، ثم يحدد إذا كان الرقم موجبًا، سالبًا أم صفر.

**التفاصيل:**
- قم بإنشاء متغير لتخزين الرقم.
- استخدم دالة `cin` لأخذ الرقم من المستخدم.
- استخدم بنية if-else-if للتحقق من الشروط التالية:
  - إذا كان الرقم أكبر من صفر، فهو موجب.
  - إذا كان الرقم أقل من صفر، فهو سالب.
  - إذا كان الرقم يساوي صفرًا، فهو صفر.
- عرض النتيجة باستخدام دالة `cout`.

---

### **8. حساب مجموع الأرقام من 1 إلى n**
**الوصف:**
قم بكتابة برنامج يطلب من المستخدم إدخال رقم `n`، ثم يقوم بحساب مجموع جميع الأرقام من 1 إلى `n`.

**التفاصيل:**
- قم بإنشاء متغير لتخزين الرقم `n`.
- استخدم دالة `cin` لأخذ الرقم من المستخدم.
- استخدم حلقة `for` أو `while` لجمع الأرقام من 1 إلى `n`.
- قم بإنشاء متغير لتخزين المجموع وابدأه بـ 0.
- في كل تكرار، أضف الرقم الحالي إلى المتغير الخاص بالمجموع.
- عرض النتيجة باستخدام دالة `cout`.

---

### **9. عكس رقم**
**الوصف:**
قم بكتابة برنامج يطلب من المستخدم إدخال رقم، ثم يقوم بعكس أرقامه.

**التفاصيل:**
- قم بإنشاء متغير لتخزين الرقم الأصلي.
- استخدم دالة `cin` لأخذ الرقم من المستخدم.
- قم بإنشاء متغير آخر لتخزين الرقم المعكوس وابدأه بـ 0.
- استخدم حلقة while لاستخراج الأرقام واحدة تلو الأخرى باستخدام العمليات `%` و `/`.
- في كل تكرار، أضف الرقم الأخير إلى الرقم المعكوس بعد ضربه في 10.
- عرض الرقم المعكوس باستخدام دالة `cout`.

---

### **10. تحديد إذا كان الرقم أوليًا أم لا**
**الوصف:**
قم بكتابة برنامج يطلب من المستخدم إدخال رقم، ثم يحدد إذا كان الرقم أوليًا أم لا.

**التفاصيل:**
- قم بإنشاء متغير لتخزين الرقم.
- استخدم دالة `cin` لأخذ الرقم من المستخدم.
- استخدم حلقة `for` للتحقق مما إذا كان الرقم قابلًا للقسمة على أي رقم بين 2 و `sqrt(الرقم)`.
- إذا تم العثور على قاسم، فإن الرقم ليس أوليًا.
- إذا لم يتم العثور على أي قاسم، فإن الرقم أولي.
- عرض النتيجة باستخدام دالة `cout`.

---

هذه المشاكل مناسبة للمبتدئين وتغطي الأساسيات مثل الدوال، الحلقات، الشرطيات، والعمليات الحسابية. يمكنك البدء بحلها خطوة بخطوة لتحسين مهاراتك في البرمجة بلغة C++.
