# לוח מעקב כלכלי - הפעלה פרטית ב-Vercel

## שלב 1: להעלות ל-GitHub
1. פתח טרמינל בתיקייה הזו
2. `git init`
3. `git add .`
4. `git commit -m "לוח מעקב כלכלי - גרסה ראשונה"`
5. צור repo חדש ב-GitHub (ציבורי, אין בו סודות - הסיסמה לא נשמרת בקוד)
6. `git remote add origin <כתובת ה-repo שלך>`
7. `git push -u origin main`

## שלב 2: לחבר ל-Vercel
1. היכנס ל-vercel.com (עם החשבון שכבר יש לך)
2. New Project -> Import מה-repo שיצרת
3. לפני הדיפלוי הראשון, לך ל-Settings -> Environment Variables והוסף:
   - BASIC_AUTH_USER = השם משתמש שתבחר (למשל ben)
   - BASIC_AUTH_PASSWORD = סיסמה חזקה שרק אתה יודע
4. לחץ Deploy

## שלב 3: שימוש
- האתר יהיה בכתובת כמו https://ben-finance-dashboard.vercel.app
- בכל כניסה תתבקש שם משתמש+סיסמה (Basic Auth ברמת השרת - Claude ואף אחד אחר לא רואה את זה)
- הנתונים שתזין נשמרים ב-localStorage של הדפדפן שלך, וישארו שם גם אחרי שנעדכן את הקוד - כי הכתובת קבועה

## עדכונים עתידיים
כשתרצה גרסה משודרגת של הדשבורד - Claude יכין לך קובץ dashboard.html חדש,
אתה פשוט מחליף את הקובץ ב-public/dashboard.html, git commit, git push -
Vercel יעדכן אוטומטית תוך שניות, והנתונים השמורים בדפדפן לא יימחקו.
