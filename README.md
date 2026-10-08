# សំបុត្រអញ្ជើញអាពាហ៍ពិពាហ៍ (Wedding Invitation)

គេហទំព័រ HTML ធម្មតា (មិនត្រូវការដំឡើងអ្វីទេ) សម្រាប់ដាក់លើ **GitHub Pages**។

## រចនាសម្ព័ន្ធឯកសារ
```
index.html          ← ទំព័រសំខាន់
.nojekyll           ← ប្រាប់ GitHub កុំដំណើរការ Jekyll
assets/
  song.mp3          ← បទចម្រៀង
  couple.jpg        ← រូបក្នុងស៊ុមពងក្រពើ (ទំព័រទី១)
  gallery-1..4.jpg  ← រូបក្នុងកម្រងរូបភាព (ទំព័រទី២)
```

## របៀប Hosting លើ GitHub Pages (មិនបាច់ប្រើ Git)
1. ចូល https://github.com ហើយចុច **New repository** → ដាក់ឈ្មោះ (ឧ. `wedding`) → ជ្រើស **Public** → **Create repository**។
2. ចុច **uploading an existing file** រួចអូសយក *ខ្លឹមសារទាំងអស់* ក្នុងថត (index.html, .nojekyll និងថត assets) ដាក់ចូល → **Commit changes**។
   (ប្រសិនបើឯកសារ `.nojekyll` មើលមិនឃើញ មិនអីទេ ទំព័រនៅតែដំណើរការ។)
3. ចូល **Settings → Pages** → នៅ **Build and deployment** ជ្រើស **Deploy from a branch** → Branch: **main** / **/(root)** → **Save**។
4. រង់ចាំប្រហែល ១-២ នាទី តំណនឹងបង្ហាញថា៖
   `https://USERNAME.github.io/wedding/`
   (USERNAME = ឈ្មោះគណនី GitHub របស់អ្នក)។

## របៀបប្រើ Git (ជម្រើស)
```bash
git init
git add .
git commit -m "wedding invitation"
git branch -M main
git remote add origin https://github.com/USERNAME/wedding.git
git push -u origin main
```

## កែខ្លឹមសារ
បើក `index.html` ហើយស្វែងរកអក្សរដែលចង់កែ ដូចជា ឈ្មោះ កាលបរិច្ឆេទ កម្មវិធី តំណផែនទី។
- ប្តូររូប៖ ជំនួសឯកសារក្នុង `assets/` ដោយរក្សាឈ្មោះដដែល។
- ប្តូរបទចម្រៀង៖ ជំនួស `assets/song.mp3` (ឬកែ `var SONG='assets/song.mp3'` ក្នុង index.html)។

## ចំណាំ
- ត្រូវមានអ៊ីនធឺណិតដើម្បីផ្ទុកពុម្ពអក្សរខ្មែរពី Google Fonts។
- ដើម្បីឱ្យតំណមានរូបអ្នកទាំងពីរពេលចែករំលែកក្នុង Facebook/Telegram សូមបន្ថែមបន្ទាត់ `og:image` ដូចមានបង្ហាញក្នុងមតិយោបល់ក្នុង `<head>` នៃ index.html។
