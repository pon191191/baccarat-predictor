// ข้อความในแต่ละภาษา
const translations = {
  en: {
    title: "Baccarat Analysis",
    start: "Start Analysis",
    select_language: "Select Language"
  },
  th: {
    title: "วิเคราะห์บาคาร่า",
    start: "เริ่มวิเคราะห์",
    select_language: "เลือกภาษา"
  }
};

// ฟังก์ชันเปลี่ยนภาษา
function setLanguage(lang) {
  const t = translations[lang];
  document.getElementById("title").textContent = t.title;
  document.getElementById("startBtn").textContent = t.start;
  document.getElementById("selectLabel").textContent = t.select_language;
}

// โหลดภาษาเริ่มต้น
document.addEventListener("DOMContentLoaded", () => {
  const languageSelector = document.getElementById("languageSelector");

  // ตั้งค่าภาษาเริ่มต้นเป็นอังกฤษ
  setLanguage("en");

  // เมื่อผู้ใช้เปลี่ยนภาษา
  languageSelector.addEventListener("change", (e) => {
    setLanguage(e.target.value);
  });
});
