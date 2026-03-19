最終版使用方式

1. 這版已內建 Firebase 設定
2. 固定共用房號：family-trip
3. 所有人打開同一個網址即可共用
4. 第一次請先在 Firebase Firestore 規則設為：

rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /travelRooms/{roomId} {
      allow read, write: if true;
    }
  }
}

上線方式
- 直接把本資料夾丟到 Netlify Drop
- 或上傳到任何靜態網站空間
