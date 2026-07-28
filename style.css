// 1. 地図の初期化（四国の中心あたりを表示するように設定）
const map = L.map('map').setView([33.8, 133.5], 8);

// 2. 地図の背景タイル（OpenStreetMap）を設定
L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
  attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
}).addTo(map);

// 3. 映画館のデータリスト
const cinemas = [
  // --- イオンシネマ ---
  {
    name: "イオンシネマ 高松",
    address: "香川県高松市福岡町3-8-5 イオンタウン高松1F",
    url: "https://www.aeoncinema.com/cinema/takamatsu/",
    lat: 34.3468,
    lng: 134.0682
  },
  {
    name: "イオンシネマ 綾川",
    address: "香川県綾歌郡綾川町萱原822-1 イオンモール綾川3F",
    url: "https://www.aeoncinema.com/cinema/ayagawa/",
    lat: 34.2289,
    lng: 133.9262
  },
  {
    name: "イオンシネマ 徳島",
    address: "徳島県徳島市南末広町4-1 イオンモール徳島5F",
    url: "https://www.aeoncinema.com/cinema/tokushima/",
    lat: 34.0617,
    lng: 134.5768
  },
  {
    name: "イオンシネマ 今治新食田",
    address: "愛媛県今治市にぎわい広場1-1 イオンモール今治新食田2F",
    url: "https://www.aeoncinema.com/cinema/imabari/",
    lat: 34.0361,
    lng: 133.0102
  },

  // --- シネマサンシャイン ---
  {
    name: "シネマサンシャイン衣山",
    address: "愛媛県松山市衣山1-188 パルティ・フジ衣山3F",
    url: "https://www.cinemasunshine.co.jp/theater/kinuyama/",
    lat: 33.8553,
    lng: 132.7485
  },
  {
    name: "シネマサンシャイン重信",
    address: "愛媛県東温市野田3-1-13 フジグラン重信3F",
    url: "https://www.cinemasunshine.co.jp/theater/shigenobu/",
    lat: 33.7997,
    lng: 132.8465
  },
  {
    name: "シネマサンシャインエミフルMASAKI",
    address: "愛媛県伊予郡松前町筒井850 エミフルMASAKI 2F",
    url: "https://www.cinemasunshine.co.jp/theater/masaki/",
    lat: 33.7892,
    lng: 132.7128
  },
  {
    name: "シネマサンシャイン北島",
    address: "徳島県板野郡北島町高房字川田15-1 フジグラン北島3F",
    url: "https://www.cinemasunshine.co.jp/theater/kitajima/",
    lat: 34.1205,
    lng: 134.5481
  },

  // --- TOHOシネマズ ---
  {
    name: "TOHOシネマズ 高知",
    address: "高知県高知市秦南町1-4-8 イオンモール高知3F",
    url: "https://hlo.tohocinemas.jp/net/theater/017/inst_top.do",
    lat: 33.5786,
    lng: 133.5385
  }
];

// 4. データをもとにピン（マーカー）と吹き出し（ポップアップ）を地図に追加
cinemas.forEach(cinema => {
  // ピンを作成
  const marker = L.marker([cinema.lat, cinema.lng]).addTo(map);

  // クリックした時に出る吹き出しの見た目を作成
  const popupHtml = `
    <div class="popup-content">
      <h3>${cinema.name}</h3>
      <p>📍 ${cinema.address}</p>
      <a href="${cinema.url}" target="_blank" rel="noopener noreferrer">公式サイトを見る ↗</a>
    </div>
  `;

  // マーカーに吹き出しをセット
  marker.bindPopup(popupHtml);
});
