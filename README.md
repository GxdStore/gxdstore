<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GxD Store — Tibia Coins & Gaming Premium</title>
<meta name="description" content="GxD Store — Tecnologia, Tibia Coins, Mouses, Teclados, Headsets e muito mais.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&family=Outfit:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#05050f;
  --bg2:#0a0a1a;
  --bg3:#0f0f25;
  --surface:#12122a;
  --surface2:#1a1a38;
  --glass:rgba(255,255,255,0.04);
  --glass-border:rgba(255,255,255,0.08);
  --purple:#7c3aed;
  --purple2:#a855f7;
  --purple3:#d8b4fe;
  --blue:#2563eb;
  --blue2:#3b82f6;
  --blue3:#93c5fd;
  --neon:#00d4ff;
  --neon2:#7df9ff;
  --pink:#e879f9;
  --white:#ffffff;
  --gray:#94a3b8;
  --gray2:#64748b;
  --border:rgba(124,58,237,0.2);
  --shadow:0 0 40px rgba(124,58,237,0.15);
  --font-display:'Rajdhani',sans-serif;
  --font-body:'Outfit',sans-serif;
}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--white);font-family:var(--font-body);overflow-x:hidden;line-height:1.6}
a{color:inherit;text-decoration:none}
button{cursor:pointer;font-family:var(--font-body);border:none;outline:none}
input{font-family:var(--font-body)}

/* ─── SCROLLBAR ─── */
::-webkit-scrollbar{width:6px}
::-webkit-scrollbar-track{background:var(--bg)}
::-webkit-scrollbar-thumb{background:var(--purple);border-radius:3px}

/* ─── NOISE OVERLAY ─── */
body::before{
  content:'';position:fixed;inset:0;
  background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E");
  pointer-events:none;z-index:0;opacity:0.4;
}

/* ─── GLOW ORBS ─── */
.orb{position:fixed;border-radius:50%;filter:blur(80px);pointer-events:none;z-index:0}
.orb1{width:500px;height:500px;background:rgba(124,58,237,0.12);top:-100px;left:-100px}
.orb2{width:400px;height:400px;background:rgba(37,99,235,0.1);top:40%;right:-100px}
.orb3{width:300px;height:300px;background:rgba(0,212,255,0.06);bottom:20%;left:30%}

/* ─── PROMO BAR ─── */
#promo-bar{
  background:linear-gradient(90deg,var(--purple),var(--blue),var(--neon),var(--purple));
  background-size:300% 100%;
  animation:gradShift 4s linear infinite;
  text-align:center;padding:8px 16px;font-size:13px;font-weight:600;
  letter-spacing:0.05em;position:relative;z-index:100
}
#promo-bar span{margin:0 12px}
@keyframes gradShift{0%{background-position:0% 50%}100%{background-position:300% 50%}}

/* ─── HEADER ─── */
header{
  position:sticky;top:0;z-index:99;
  background:rgba(5,5,15,0.85);
  backdrop-filter:blur(20px);
  border-bottom:1px solid var(--glass-border);
  padding:0 24px;
}
.header-inner{
  max-width:1400px;margin:0 auto;
  display:flex;align-items:center;gap:16px;height:68px;
}
.logo{
  font-family:var(--font-display);font-size:26px;font-weight:700;
  background:linear-gradient(135deg,var(--purple2),var(--neon));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;
  white-space:nowrap;flex-shrink:0;letter-spacing:1px;
}
.logo span{color:var(--neon);-webkit-text-fill-color:var(--neon)}

nav{display:flex;gap:4px;flex:1;justify-content:center}
nav a{
  padding:6px 14px;border-radius:8px;font-size:14px;font-weight:500;
  color:var(--gray);transition:all .2s;white-space:nowrap;
}
nav a:hover,nav a.active{color:var(--white);background:var(--glass)}
nav a.active{color:var(--purple3)}

.search-wrap{
  display:flex;align-items:center;gap:8px;
  background:var(--glass);border:1px solid var(--glass-border);
  border-radius:10px;padding:8px 14px;width:220px;transition:all .3s;
}
.search-wrap:focus-within{border-color:var(--purple);box-shadow:0 0 0 3px rgba(124,58,237,0.15);width:260px}
.search-wrap input{background:none;border:none;outline:none;color:var(--white);font-size:14px;width:100%}
.search-wrap input::placeholder{color:var(--gray2)}
.search-wrap svg{width:16px;height:16px;color:var(--gray2);flex-shrink:0}

.header-actions{display:flex;gap:8px;align-items:center}
.icon-btn{
  width:40px;height:40px;border-radius:10px;
  background:var(--glass);border:1px solid var(--glass-border);
  display:flex;align-items:center;justify-content:center;
  color:var(--gray);transition:all .2s;position:relative;
}
.icon-btn:hover{color:var(--white);border-color:var(--purple);background:rgba(124,58,237,0.15)}
.badge{
  position:absolute;top:-4px;right:-4px;
  background:var(--purple);color:#fff;
  font-size:10px;font-weight:700;width:18px;height:18px;
  border-radius:50%;display:flex;align-items:center;justify-content:center;
}
.hamburger{display:none;width:40px;height:40px;border-radius:10px;background:var(--glass);border:1px solid var(--glass-border);align-items:center;justify-content:center;color:var(--gray)}

/* ─── HERO BANNER ─── */
.hero-slider{position:relative;overflow:hidden;height:520px;z-index:1}
.slide{
  position:absolute;inset:0;display:flex;align-items:center;
  opacity:0;transition:opacity .8s;pointer-events:none;
}
.slide.active{opacity:1;pointer-events:auto}
.slide-bg{
  position:absolute;inset:0;
  background-size:cover;background-position:center;
}
.slide-bg::after{
  content:'';position:absolute;inset:0;
  background:linear-gradient(90deg,rgba(5,5,15,0.9) 40%,transparent);
}
.slide-content{
  position:relative;z-index:2;max-width:1400px;
  margin:0 auto;padding:0 40px;
}
.slide-tag{
  display:inline-block;background:rgba(124,58,237,0.3);
  border:1px solid var(--purple);color:var(--purple3);
  font-size:11px;font-weight:700;letter-spacing:2px;text-transform:uppercase;
  padding:4px 12px;border-radius:20px;margin-bottom:16px;
}
.slide-title{
  font-family:var(--font-display);font-size:clamp(32px,5vw,64px);
  font-weight:700;line-height:1.1;margin-bottom:16px;
}
.slide-title .hl{
  background:linear-gradient(135deg,var(--purple2),var(--neon));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;
}
.slide-sub{font-size:16px;color:var(--gray);margin-bottom:28px;max-width:480px}
.slide-btns{display:flex;gap:12px;flex-wrap:wrap}

.btn-primary{
  padding:12px 28px;border-radius:10px;font-weight:600;font-size:15px;
  background:linear-gradient(135deg,var(--purple),var(--blue));
  color:#fff;border:none;transition:all .3s;
  box-shadow:0 4px 20px rgba(124,58,237,0.4);
}
.btn-primary:hover{transform:translateY(-2px);box-shadow:0 8px 30px rgba(124,58,237,0.5)}

.btn-outline{
  padding:12px 28px;border-radius:10px;font-weight:600;font-size:15px;
  background:transparent;border:1px solid var(--purple);color:var(--purple3);
  transition:all .3s;
}
.btn-outline:hover{background:rgba(124,58,237,0.15);transform:translateY(-2px)}

.slider-dots{
  position:absolute;bottom:24px;left:50%;transform:translateX(-50%);
  display:flex;gap:8px;z-index:3;
}
.dot{width:8px;height:8px;border-radius:4px;background:rgba(255,255,255,0.3);cursor:pointer;transition:all .3s}
.dot.active{background:var(--purple2);width:24px}

.slider-arrow{
  position:absolute;top:50%;transform:translateY(-50%);z-index:3;
  width:44px;height:44px;border-radius:50%;
  background:rgba(255,255,255,0.08);border:1px solid rgba(255,255,255,0.15);
  color:#fff;display:flex;align-items:center;justify-content:center;
  cursor:pointer;transition:all .2s;
}
.slider-arrow:hover{background:var(--purple);border-color:var(--purple)}
.slider-arrow.prev{left:20px}
.slider-arrow.next{right:20px}

/* ─── SECTIONS ─── */
section{position:relative;z-index:1}
.container{max-width:1400px;margin:0 auto;padding:0 24px}
.section-header{text-align:center;margin-bottom:48px}
.section-label{
  display:inline-block;font-size:11px;font-weight:700;letter-spacing:3px;
  text-transform:uppercase;color:var(--purple3);margin-bottom:12px;
}
.section-title{
  font-family:var(--font-display);font-size:clamp(28px,4vw,44px);
  font-weight:700;line-height:1.1;
}
.section-title .hl{
  background:linear-gradient(135deg,var(--purple2),var(--neon));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;
}
.section-sub{color:var(--gray);font-size:16px;margin-top:10px}

/* ─── CATEGORIES ─── */
.cats-section{padding:60px 0 40px}
.cats-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(120px,1fr));gap:16px}
.cat-card{
  display:flex;flex-direction:column;align-items:center;gap:10px;
  padding:20px 12px;border-radius:16px;
  background:var(--glass);border:1px solid var(--glass-border);
  cursor:pointer;transition:all .3s;text-align:center;
}
.cat-card:hover,.cat-card.active{
  border-color:var(--purple);background:rgba(124,58,237,0.12);
  transform:translateY(-4px);
}
.cat-icon{
  width:48px;height:48px;border-radius:12px;
  background:linear-gradient(135deg,var(--purple),var(--blue));
  display:flex;align-items:center;justify-content:center;font-size:22px;
}
.cat-name{font-size:13px;font-weight:600;color:var(--white)}
.cat-count{font-size:11px;color:var(--gray2)}

/* ─── FILTERS ─── */
.filters-bar{
  display:flex;align-items:center;gap:12px;
  padding:16px 0;flex-wrap:wrap;
  border-bottom:1px solid var(--glass-border);
  margin-bottom:32px;
}
.filter-btn{
  padding:7px 16px;border-radius:8px;font-size:13px;font-weight:500;
  background:var(--glass);border:1px solid var(--glass-border);
  color:var(--gray);transition:all .2s;display:flex;align-items:center;gap:6px;
}
.filter-btn:hover,.filter-btn.active{
  border-color:var(--purple);color:var(--purple3);background:rgba(124,58,237,0.1)
}
.filter-select{
  padding:7px 14px;border-radius:8px;font-size:13px;
  background:var(--glass);border:1px solid var(--glass-border);
  color:var(--white);outline:none;cursor:pointer;
}
.filter-select option{background:var(--surface)}
.sort-wrap{margin-left:auto;display:flex;align-items:center;gap:8px}
.sort-label{font-size:13px;color:var(--gray)}

/* ─── PRODUCT GRID ─── */
.products-section{padding:32px 0 80px}
.products-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(240px,1fr));gap:24px}

/* ─── PRODUCT CARD ─── */
.product-card{
  border-radius:20px;overflow:hidden;
  background:var(--surface);border:1px solid var(--glass-border);
  transition:all .3s;position:relative;cursor:pointer;
}
.product-card:hover{
  transform:translateY(-6px);
  border-color:rgba(124,58,237,0.4);
  box-shadow:0 16px 40px rgba(124,58,237,0.2);
}
.card-img{
  position:relative;overflow:hidden;height:200px;
  background:var(--bg3);display:flex;align-items:center;justify-content:center;
}
.card-img img{
  width:100%;height:100%;object-fit:contain;padding:24px;
  transition:transform .4s;
}
.product-card:hover .card-img img{transform:scale(1.06)}
.card-badges{position:absolute;top:12px;left:12px;display:flex;flex-direction:column;gap:6px}
.badge-discount{
  background:linear-gradient(135deg,#ef4444,#dc2626);
  color:#fff;font-size:11px;font-weight:700;padding:3px 8px;border-radius:6px;
}
.badge-new{
  background:linear-gradient(135deg,var(--neon),var(--blue2));
  color:#000;font-size:11px;font-weight:700;padding:3px 8px;border-radius:6px;
}
.badge-hot{
  background:linear-gradient(135deg,#f97316,#ef4444);
  color:#fff;font-size:11px;font-weight:700;padding:3px 8px;border-radius:6px;
}
.wishlist-btn{
  position:absolute;top:12px;right:12px;width:32px;height:32px;
  border-radius:8px;background:rgba(5,5,15,0.6);border:1px solid var(--glass-border);
  display:flex;align-items:center;justify-content:center;color:var(--gray);
  transition:all .2s;
}
.wishlist-btn:hover,.wishlist-btn.active{color:#e879f9;border-color:#e879f9;background:rgba(232,121,249,0.1)}
.card-body{padding:16px}
.card-cat{font-size:11px;color:var(--gray2);font-weight:600;letter-spacing:1px;text-transform:uppercase;margin-bottom:6px}
.card-name{font-size:15px;font-weight:600;color:var(--white);margin-bottom:8px;line-height:1.3}
.card-stars{display:flex;align-items:center;gap:4px;margin-bottom:10px}
.stars{color:#f59e0b;font-size:13px;letter-spacing:1px}
.review-count{font-size:12px;color:var(--gray2)}
.card-price{display:flex;align-items:baseline;gap:8px;margin-bottom:14px}
.price-old{font-size:13px;color:var(--gray2);text-decoration:line-through}
.price-new{font-size:22px;font-weight:700;color:var(--white)}
.price-new small{font-size:13px;font-weight:400}
.card-actions{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.btn-buy{
  padding:9px 0;border-radius:8px;font-size:13px;font-weight:600;
  background:linear-gradient(135deg,var(--purple),var(--blue));
  color:#fff;transition:all .2s;text-align:center;
}
.btn-buy:hover{opacity:0.85;transform:scale(0.98)}
.btn-cart{
  padding:9px 0;border-radius:8px;font-size:13px;font-weight:600;
  background:var(--glass);border:1px solid var(--glass-border);
  color:var(--white);transition:all .2s;text-align:center;display:flex;
  align-items:center;justify-content:center;gap:6px;
}
.btn-cart:hover{border-color:var(--purple);color:var(--purple3);background:rgba(124,58,237,0.1)}

/* ─── HIGHLIGHTS SECTION ─── */
.highlights-section{padding:60px 0;background:var(--bg2)}
.highlights-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:16px}
.highlight-card{
  padding:24px;border-radius:16px;
  background:var(--glass);border:1px solid var(--glass-border);
  display:flex;flex-direction:column;align-items:center;text-align:center;gap:12px;
  transition:all .3s;
}
.highlight-card:hover{border-color:var(--purple);transform:translateY(-4px)}
.hl-icon{
  width:52px;height:52px;border-radius:14px;font-size:24px;
  display:flex;align-items:center;justify-content:center;
}
.hl-title{font-size:14px;font-weight:700;color:var(--white)}
.hl-sub{font-size:12px;color:var(--gray2)}

/* ─── TIBIA SECTION ─── */
.tibia-section{padding:60px 0}
.tibia-grid{display:grid;grid-template-columns:1fr 1fr;gap:32px;align-items:center}
.tibia-visual{
  border-radius:24px;overflow:hidden;
  border:1px solid rgba(168,85,247,0.3);
  background:var(--surface);padding:40px;
  display:flex;flex-direction:column;align-items:center;gap:20px;
  position:relative;
}
.tibia-visual::before{
  content:'';position:absolute;inset:0;
  background:radial-gradient(circle at center,rgba(124,58,237,0.15),transparent 70%);
}
.tibia-logo{
  font-family:var(--font-display);font-size:48px;font-weight:700;
  background:linear-gradient(135deg,#f59e0b,#ef4444);
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;
  position:relative;z-index:1;
}
.coin-count{
  font-family:var(--font-display);font-size:22px;font-weight:700;
  background:linear-gradient(135deg,var(--purple2),var(--neon));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;
  position:relative;z-index:1;
}
.tibia-coins-grid{
  display:grid;grid-template-columns:repeat(2,1fr);gap:12px;
  position:relative;z-index:1;width:100%;
}
.coin-pack{
  padding:16px;border-radius:12px;
  background:rgba(255,255,255,0.05);border:1px solid rgba(255,255,255,0.1);
  text-align:center;cursor:pointer;transition:all .3s;
}
.coin-pack:hover{border-color:var(--purple);background:rgba(124,58,237,0.15);transform:scale(1.02)}
.coin-pack-amount{font-family:var(--font-display);font-size:18px;font-weight:700;color:#f59e0b}
.coin-pack-price{font-size:13px;color:var(--white);font-weight:600}
.coin-pack-old{font-size:11px;color:var(--gray2);text-decoration:line-through}
.tibia-text{display:flex;flex-direction:column;gap:20px}
.tibia-text h2{
  font-family:var(--font-display);font-size:clamp(28px,3.5vw,44px);
  font-weight:700;line-height:1.1;
}
.tibia-text p{color:var(--gray);font-size:15px;line-height:1.7}
.tibia-features{display:flex;flex-direction:column;gap:10px}
.tibia-feat{display:flex;align-items:center;gap:10px;font-size:14px;color:var(--gray)}
.tibia-feat span{width:22px;height:22px;border-radius:6px;background:rgba(124,58,237,0.2);border:1px solid var(--purple);display:flex;align-items:center;justify-content:center;font-size:12px;flex-shrink:0}

/* ─── CART SIDEBAR ─── */
.cart-overlay{
  position:fixed;inset:0;background:rgba(0,0,0,0.7);z-index:200;
  opacity:0;pointer-events:none;transition:opacity .3s;
}
.cart-overlay.open{opacity:1;pointer-events:auto}
.cart-sidebar{
  position:fixed;right:0;top:0;bottom:0;width:420px;max-width:100vw;
  background:var(--bg2);border-left:1px solid var(--glass-border);
  transform:translateX(100%);transition:transform .4s cubic-bezier(0.4,0,0.2,1);
  z-index:201;display:flex;flex-direction:column;
}
.cart-sidebar.open{transform:translateX(0)}
.cart-header{
  padding:24px;border-bottom:1px solid var(--glass-border);
  display:flex;align-items:center;justify-content:space-between;
}
.cart-title{font-family:var(--font-display);font-size:24px;font-weight:700}
.cart-close{
  width:36px;height:36px;border-radius:8px;
  background:var(--glass);border:1px solid var(--glass-border);
  display:flex;align-items:center;justify-content:center;
  color:var(--gray);cursor:pointer;transition:all .2s;
}
.cart-close:hover{color:var(--white);border-color:var(--purple)}
.cart-items{flex:1;overflow-y:auto;padding:16px 24px;display:flex;flex-direction:column;gap:16px}
.cart-empty{
  flex:1;display:flex;flex-direction:column;align-items:center;
  justify-content:center;gap:16px;text-align:center;color:var(--gray);
}
.cart-empty .empty-icon{font-size:64px;opacity:0.3}
.cart-item{
  display:flex;gap:12px;padding:14px;border-radius:14px;
  background:var(--glass);border:1px solid var(--glass-border);
}
.cart-item-img{
  width:70px;height:70px;border-radius:10px;
  background:var(--surface);object-fit:contain;padding:8px;flex-shrink:0;
}
.cart-item-info{flex:1;min-width:0}
.cart-item-name{font-size:14px;font-weight:600;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.cart-item-cat{font-size:11px;color:var(--gray2);margin-bottom:6px}
.cart-item-price{font-size:16px;font-weight:700;color:var(--purple3)}
.cart-item-qty{display:flex;align-items:center;gap:8px;margin-top:8px}
.qty-btn{
  width:26px;height:26px;border-radius:6px;
  background:var(--glass);border:1px solid var(--glass-border);
  color:var(--white);font-size:15px;font-weight:700;
  display:flex;align-items:center;justify-content:center;cursor:pointer;
  transition:all .2s;
}
.qty-btn:hover{border-color:var(--purple);color:var(--purple3)}
.qty-num{font-size:14px;font-weight:600;min-width:20px;text-align:center}
.cart-del{
  align-self:flex-start;width:28px;height:28px;border-radius:6px;
  background:rgba(239,68,68,0.1);border:1px solid rgba(239,68,68,0.2);
  color:#ef4444;display:flex;align-items:center;justify-content:center;
  cursor:pointer;font-size:14px;transition:all .2s;
}
.cart-del:hover{background:rgba(239,68,68,0.2)}
.cart-footer{padding:20px 24px;border-top:1px solid var(--glass-border)}
.coupon-row{display:flex;gap:8px;margin-bottom:16px}
.coupon-input{
  flex:1;background:var(--glass);border:1px solid var(--glass-border);
  border-radius:8px;padding:10px 14px;color:var(--white);font-size:13px;outline:none;
}
.coupon-input::placeholder{color:var(--gray2)}
.coupon-input:focus{border-color:var(--purple)}
.coupon-btn{
  padding:10px 16px;border-radius:8px;background:var(--purple);
  color:#fff;font-size:13px;font-weight:600;cursor:pointer;
  border:none;transition:all .2s;
}
.coupon-btn:hover{opacity:0.85}
.tibia-char-row{margin-bottom:16px}
.tibia-char-label{font-size:12px;color:var(--gray);margin-bottom:6px;display:flex;align-items:center;gap:6px}
.tibia-char-input{
  width:100%;background:var(--glass);border:1px solid var(--glass-border);
  border-radius:8px;padding:10px 14px;color:var(--white);font-size:13px;outline:none;
}
.tibia-char-input::placeholder{color:var(--gray2)}
.tibia-char-input:focus{border-color:var(--purple)}
.char-info{
  margin-top:8px;padding:10px 12px;border-radius:8px;
  background:rgba(124,58,237,0.1);border:1px solid rgba(124,58,237,0.2);
  font-size:12px;color:var(--purple3);display:none;
}
.char-info.show{display:block}
.total-row{display:flex;justify-content:space-between;align-items:center;margin-bottom:8px}
.total-label{font-size:14px;color:var(--gray)}
.total-val{font-size:14px;font-weight:600}
.total-final{font-size:20px;font-weight:700;color:var(--white)}
.checkout-btn{
  width:100%;padding:14px;border-radius:10px;font-size:15px;font-weight:700;
  background:linear-gradient(135deg,var(--purple),var(--blue));
  color:#fff;border:none;cursor:pointer;transition:all .3s;margin-top:14px;
  box-shadow:0 4px 20px rgba(124,58,237,0.4);
}
.checkout-btn:hover{opacity:0.9;transform:translateY(-2px)}

/* ─── PRODUCT MODAL ─── */
.modal-overlay{
  position:fixed;inset:0;background:rgba(0,0,0,0.8);z-index:300;
  opacity:0;pointer-events:none;transition:opacity .3s;
  display:flex;align-items:center;justify-content:center;padding:20px;
}
.modal-overlay.open{opacity:1;pointer-events:auto}
.product-modal{
  background:var(--bg2);border:1px solid var(--glass-border);
  border-radius:24px;width:900px;max-width:100%;max-height:90vh;
  overflow-y:auto;transform:scale(0.9);transition:transform .3s;
}
.modal-overlay.open .product-modal{transform:scale(1)}
.modal-inner{padding:40px}
.modal-grid{display:grid;grid-template-columns:1fr 1fr;gap:40px;align-items:start}
.modal-img-main{
  aspect-ratio:1;border-radius:16px;background:var(--surface);
  display:flex;align-items:center;justify-content:center;overflow:hidden;
  margin-bottom:12px;
}
.modal-img-main img{width:100%;height:100%;object-fit:contain;padding:32px;transition:transform .4s}
.modal-img-main:hover img{transform:scale(1.1)}
.modal-thumbs{display:flex;gap:8px}
.modal-thumb{
  width:60px;height:60px;border-radius:10px;background:var(--surface);
  border:2px solid transparent;cursor:pointer;overflow:hidden;
  display:flex;align-items:center;justify-content:center;transition:all .2s;
}
.modal-thumb.active,.modal-thumb:hover{border-color:var(--purple)}
.modal-thumb img{width:100%;height:100%;object-fit:contain;padding:8px}
.modal-info{display:flex;flex-direction:column;gap:16px}
.modal-cat{font-size:11px;color:var(--gray2);letter-spacing:2px;text-transform:uppercase}
.modal-name{font-family:var(--font-display);font-size:28px;font-weight:700;line-height:1.2}
.modal-rating{display:flex;align-items:center;gap:8px}
.modal-price-block{padding:16px;border-radius:12px;background:var(--glass);border:1px solid var(--glass-border)}
.modal-price-old{font-size:14px;color:var(--gray2);text-decoration:line-through}
.modal-price-new{font-size:32px;font-weight:700}
.modal-desc{font-size:14px;color:var(--gray);line-height:1.7}
.specs-table{width:100%;border-collapse:collapse}
.specs-table td{padding:8px 0;font-size:13px;border-bottom:1px solid var(--glass-border)}
.specs-table td:first-child{color:var(--gray2);width:40%}
.specs-table td:last-child{color:var(--white);font-weight:500}
.modal-actions{display:flex;flex-direction:column;gap:10px}
.modal-actions .btn-primary{width:100%;padding:14px;font-size:15px}
.modal-actions .btn-cart{width:100%;padding:14px;font-size:15px;background:var(--glass);border:1px solid var(--glass-border);color:var(--white);border-radius:10px;display:flex;align-items:center;justify-content:center;gap:8px;font-weight:600;transition:all .2s}
.modal-actions .btn-cart:hover{border-color:var(--purple);color:var(--purple3)}
.modal-close{
  position:absolute;top:16px;right:16px;width:36px;height:36px;
  border-radius:8px;background:var(--glass);border:1px solid var(--glass-border);
  display:flex;align-items:center;justify-content:center;color:var(--gray);
  cursor:pointer;font-size:18px;transition:all .2s;
}
.modal-close:hover{color:var(--white);border-color:var(--purple)}
.product-modal{position:relative}

/* ─── TOAST ─── */
.toast-container{position:fixed;bottom:24px;right:24px;z-index:400;display:flex;flex-direction:column;gap:8px}
.toast{
  background:var(--surface2);border:1px solid var(--glass-border);
  border-radius:12px;padding:14px 18px;font-size:14px;font-weight:500;
  display:flex;align-items:center;gap:10px;min-width:280px;
  animation:slideIn .3s ease;box-shadow:0 8px 32px rgba(0,0,0,0.4);
}
.toast.success{border-color:rgba(16,185,129,0.3);color:#6ee7b7}
.toast.success .ti{color:#10b981}
@keyframes slideIn{from{transform:translateX(100%);opacity:0}to{transform:translateX(0);opacity:1}}
@keyframes slideOut{from{transform:translateX(0);opacity:1}to{transform:translateX(100%);opacity:0}}

/* ─── FOOTER ─── */
footer{background:var(--bg2);border-top:1px solid var(--glass-border);padding:60px 0 0;position:relative;z-index:1}
.footer-grid{display:grid;grid-template-columns:2fr 1fr 1fr 1fr;gap:40px;margin-bottom:48px}
.footer-brand{}
.footer-logo{font-family:var(--font-display);font-size:28px;font-weight:700;margin-bottom:12px;background:linear-gradient(135deg,var(--purple2),var(--neon));-webkit-background-clip:text;-webkit-text-fill-color:transparent}
.footer-desc{font-size:14px;color:var(--gray);line-height:1.7;margin-bottom:20px}
.social-links{display:flex;gap:10px}
.social-link{
  width:38px;height:38px;border-radius:10px;
  background:var(--glass);border:1px solid var(--glass-border);
  display:flex;align-items:center;justify-content:center;font-size:16px;
  color:var(--gray);transition:all .2s;
}
.social-link:hover{color:var(--white);border-color:var(--purple);background:rgba(124,58,237,0.15)}
.footer-col h4{font-size:14px;font-weight:700;color:var(--white);margin-bottom:16px;letter-spacing:1px;text-transform:uppercase}
.footer-links{display:flex;flex-direction:column;gap:10px}
.footer-links a{font-size:14px;color:var(--gray);transition:color .2s}
.footer-links a:hover{color:var(--purple3)}
.footer-bottom{
  border-top:1px solid var(--glass-border);
  padding:20px 0;display:flex;align-items:center;justify-content:space-between;
  flex-wrap:wrap;gap:12px;
}
.footer-copy{font-size:13px;color:var(--gray2)}
.payment-icons{display:flex;gap:8px;flex-wrap:wrap}
.pay-icon{
  padding:6px 12px;border-radius:6px;
  background:var(--glass);border:1px solid var(--glass-border);
  font-size:12px;font-weight:700;color:var(--gray);
}
.newsletter-wrap{margin-bottom:48px}
.newsletter-inner{
  border-radius:20px;padding:40px;
  background:linear-gradient(135deg,rgba(124,58,237,0.15),rgba(37,99,235,0.1));
  border:1px solid rgba(124,58,237,0.2);
  display:flex;align-items:center;justify-content:space-between;gap:24px;flex-wrap:wrap;
}
.newsletter-text h3{font-family:var(--font-display);font-size:26px;font-weight:700;margin-bottom:8px}
.newsletter-text p{font-size:14px;color:var(--gray)}
.newsletter-form{display:flex;gap:10px;flex:1;max-width:420px}
.newsletter-form input{
  flex:1;background:rgba(255,255,255,0.07);border:1px solid var(--glass-border);
  border-radius:10px;padding:12px 16px;color:var(--white);font-size:14px;outline:none;
}
.newsletter-form input::placeholder{color:var(--gray2)}
.newsletter-form input:focus{border-color:var(--purple)}
.newsletter-form button{
  padding:12px 20px;border-radius:10px;
  background:linear-gradient(135deg,var(--purple),var(--blue));
  color:#fff;font-size:14px;font-weight:600;white-space:nowrap;
}
.newsletter-form button:hover{opacity:0.9}

/* ─── MOBILE NAV ─── */
.mobile-nav{
  position:fixed;bottom:0;left:0;right:0;
  background:rgba(10,10,26,0.95);backdrop-filter:blur(20px);
  border-top:1px solid var(--glass-border);
  display:none;z-index:99;
}
.mobile-nav-inner{
  display:flex;justify-content:space-around;padding:8px 0;max-width:480px;margin:0 auto;
}
.mobile-nav-btn{
  display:flex;flex-direction:column;align-items:center;gap:4px;
  padding:8px 16px;color:var(--gray);cursor:pointer;transition:color .2s;font-size:11px;
  background:none;border:none;
}
.mobile-nav-btn.active,.mobile-nav-btn:hover{color:var(--purple3)}
.mobile-nav-btn svg{width:22px;height:22px}

/* ─── LOADER ─── */
.page-loader{
  position:fixed;inset:0;background:var(--bg);z-index:500;
  display:flex;align-items:center;justify-content:center;flex-direction:column;gap:16px;
  transition:opacity .5s;
}
.page-loader.hidden{opacity:0;pointer-events:none}
.loader-logo{font-family:var(--font-display);font-size:40px;font-weight:700;background:linear-gradient(135deg,var(--purple2),var(--neon));-webkit-background-clip:text;-webkit-text-fill-color:transparent;animation:pulse 1s infinite}
.loader-bar{width:200px;height:3px;background:rgba(255,255,255,0.1);border-radius:2px;overflow:hidden}
.loader-fill{height:100%;background:linear-gradient(90deg,var(--purple),var(--neon));border-radius:2px;animation:load 1.5s ease forwards}
@keyframes load{from{width:0}to{width:100%}}
@keyframes pulse{0%,100%{opacity:1}50%{opacity:0.5}}

/* ─── RESPONSIVE ─── */
@media(max-width:1100px){
  nav{display:none}
  .tibia-grid{grid-template-columns:1fr}
  .footer-grid{grid-template-columns:1fr 1fr}
}
@media(max-width:768px){
  .hamburger{display:flex}
  .search-wrap{width:160px}
  .hero-slider{height:400px}
  .slide-content{padding:0 24px}
  .modal-grid{grid-template-columns:1fr}
  .product-modal{border-radius:16px}
  .modal-inner{padding:24px}
  .footer-grid{grid-template-columns:1fr}
  .mobile-nav{display:block}
  body{padding-bottom:70px}
  .newsletter-inner{flex-direction:column}
  .newsletter-form{max-width:100%;width:100%}
  .cart-sidebar{width:100vw}
}
@media(max-width:480px){
  .search-wrap{display:none}
  .header-inner{gap:10px}
  .products-grid{grid-template-columns:repeat(auto-fill,minmax(180px,1fr));gap:16px}
}
</style>
</head>
<body>

<!-- Loader -->
<div class="page-loader" id="loader">
  <div class="loader-logo">GXD STORE</div>
  <div class="loader-bar"><div class="loader-fill"></div></div>
  <p style="font-size:13px;color:var(--gray2);letter-spacing:2px">CARREGANDO...</p>
</div>

<!-- Glow Orbs -->
<div class="orb orb1"></div>
<div class="orb orb2"></div>
<div class="orb orb3"></div>

<!-- Promo Bar -->
<div id="promo-bar" style="position:relative;z-index:100">
  <span>🔥 FRETE GRÁTIS acima de R$ 299</span>
  <span>⚡ PIX com 5% de desconto</span>
  <span>🎮 Tibia Coins entrega imediata</span>
  <span>🔥 FRETE GRÁTIS acima de R$ 299</span>
  <span>⚡ PIX com 5% de desconto</span>
</div>

<!-- Header -->
<header>
  <div class="header-inner">
    <div class="logo">GXD<span>STORE</span></div>
    <nav>
      <a href="#" class="active">Home</a>
      <a href="#products">Produtos</a>
      <a href="#tibia">Tibia</a>
      <a href="#" onclick="filterCat('Mouses')">Periféricos</a>
      <a href="#" onclick="filterCat('Gadgets')">Gadgets</a>
      <a href="#" onclick="filterCat('Promoções')">Promoções</a>
    </nav>
    <div class="search-wrap">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg>
      <input type="text" placeholder="Buscar produtos..." id="search-input" oninput="handleSearch(this.value)">
    </div>
    <div class="header-actions">
      <button class="icon-btn" onclick="toggleWishlist()" title="Lista de Desejos">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z"/></svg>
        <span class="badge" id="wish-count" style="display:none">0</span>
      </button>
      <button class="icon-btn" onclick="openCart()" title="Carrinho">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="9" cy="21" r="1"/><circle cx="20" cy="21" r="1"/><path d="M1 1h4l2.68 13.39a2 2 0 0 0 2 1.61h9.72a2 2 0 0 0 2-1.61L23 6H6"/></svg>
        <span class="badge" id="cart-count">0</span>
      </button>
      <button class="icon-btn" title="Conta">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"/><circle cx="12" cy="7" r="4"/></svg>
      </button>
      <button class="hamburger icon-btn">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="3" y1="6" x2="21" y2="6"/><line x1="3" y1="12" x2="21" y2="12"/><line x1="3" y1="18" x2="21" y2="18"/></svg>
      </button>
    </div>
  </div>
</header>

<!-- Hero Slider -->
<div class="hero-slider" id="hero">
  <div class="slide active">
    <div class="slide-bg" style="background:linear-gradient(135deg,#0f0030 0%,#050015 100%)">
      <div style="position:absolute;right:0;top:0;bottom:0;width:55%;background:radial-gradient(ellipse at 70% 50%,rgba(124,58,237,0.3),transparent 70%);display:flex;align-items:center;justify-content:center;font-size:200px;opacity:0.15">🖱️</div>
    </div>
    <div class="slide-content" style="width:100%">
      <div class="slide-tag">⚡ Novo Lançamento</div>
      <div class="slide-title">Tecnologia, <span class="hl">Performance</span><br>e Inovação.</div>
      <p class="slide-sub">Os melhores periféricos gaming e gadgets em um só lugar. Entrega rápida para todo o Brasil.</p>
      <div class="slide-btns">
        <button class="btn-primary" onclick="document.getElementById('products').scrollIntoView({behavior:'smooth'})">Ver Produtos</button>
        <button class="btn-outline" onclick="filterCat('Promoções')">Promoções</button>
      </div>
    </div>
  </div>
  <div class="slide">
    <div class="slide-bg" style="background:linear-gradient(135deg,#001830 0%,#000a15 100%)">
      <div style="position:absolute;right:0;top:0;bottom:0;width:55%;background:radial-gradient(ellipse at 70% 50%,rgba(37,99,235,0.3),transparent 70%);display:flex;align-items:center;justify-content:center;font-size:180px;opacity:0.15">⌨️</div>
    </div>
    <div class="slide-content" style="width:100%">
      <div class="slide-tag">🎮 Gamer Setup</div>
      <div class="slide-title">Sua <span class="hl">Setup</span><br>dos Sonhos.</div>
      <p class="slide-sub">Teclados mecânicos, headsets premium e muito mais. Monte a setup perfeita com os melhores produtos.</p>
      <div class="slide-btns">
        <button class="btn-primary" onclick="filterCat('Teclados')">Ver Teclados</button>
        <button class="btn-outline" onclick="filterCat('Headsets')">Ver Headsets</button>
      </div>
    </div>
  </div>
  <div class="slide">
    <div class="slide-bg" style="background:linear-gradient(135deg,#1a0030 0%,#0a0020 100%)">
      <div style="position:absolute;right:0;top:0;bottom:0;width:55%;background:radial-gradient(ellipse at 70% 50%,rgba(168,85,247,0.35),transparent 70%);display:flex;align-items:center;justify-content:center;font-size:180px;opacity:0.2">🪙</div>
    </div>
    <div class="slide-content" style="width:100%">
      <div class="slide-tag">🎮 Tibia Official</div>
      <div class="slide-title">Tibia <span class="hl">Coins</span><br>Entrega Imediata.</div>
      <p class="slide-sub">Compre Tibia Coins com segurança. Pagamento via PIX, cartão e boleto. Entrega em minutos.</p>
      <div class="slide-btns">
        <button class="btn-primary" onclick="document.getElementById('tibia').scrollIntoView({behavior:'smooth'})">Comprar Coins</button>
        <button class="btn-outline" onclick="filterCat('Itens Tibia')">Ver Itens</button>
      </div>
    </div>
  </div>
  <button class="slider-arrow prev" onclick="changeSlide(-1)">‹</button>
  <button class="slider-arrow next" onclick="changeSlide(1)">›</button>
  <div class="slider-dots">
    <div class="dot active" onclick="goSlide(0)"></div>
    <div class="dot" onclick="goSlide(1)"></div>
    <div class="dot" onclick="goSlide(2)"></div>
  </div>
</div>

<!-- Highlights -->
<div class="highlights-section">
  <div class="container">
    <div class="highlights-grid">
      <div class="highlight-card">
        <div class="hl-icon" style="background:linear-gradient(135deg,rgba(124,58,237,0.3),rgba(37,99,235,0.3))">🚚</div>
        <div class="hl-title">Frete Grátis</div>
        <div class="hl-sub">Compras acima de R$ 299</div>
      </div>
      <div class="highlight-card">
        <div class="hl-icon" style="background:linear-gradient(135deg,rgba(16,185,129,0.3),rgba(5,150,105,0.3))">💳</div>
        <div class="hl-title">12x Sem Juros</div>
        <div class="hl-sub">Em todos os produtos</div>
      </div>
      <div class="highlight-card">
        <div class="hl-icon" style="background:linear-gradient(135deg,rgba(245,158,11,0.3),rgba(234,88,12,0.3))">⚡</div>
        <div class="hl-title">PIX com 5% OFF</div>
        <div class="hl-sub">Desconto na hora</div>
      </div>
      <div class="highlight-card">
        <div class="hl-icon" style="background:linear-gradient(135deg,rgba(239,68,68,0.3),rgba(220,38,38,0.3))">🔒</div>
        <div class="hl-title">Compra Segura</div>
        <div class="hl-sub">SSL & Certificado</div>
      </div>
      <div class="highlight-card">
        <div class="hl-icon" style="background:linear-gradient(135deg,rgba(0,212,255,0.2),rgba(37,99,235,0.2))">📦</div>
        <div class="hl-title">Troca Fácil</div>
        <div class="hl-sub">30 dias garantidos</div>
      </div>
    </div>
  </div>
</div>

<!-- Categories -->
<section class="cats-section">
  <div class="container">
    <div class="section-header">
      <div class="section-label">Explorar</div>
      <h2 class="section-title">Nossas <span class="hl">Categorias</span></h2>
    </div>
    <div class="cats-grid" id="cats-grid"></div>
  </div>
</section>

<!-- Products Section -->
<section class="products-section" id="products">
  <div class="container">
    <div class="section-header">
      <div class="section-label">Catálogo</div>
      <h2 class="section-title">Produtos em <span class="hl">Destaque</span></h2>
      <p class="section-sub">Os melhores periféricos, gadgets e itens gaming do mercado</p>
    </div>
    <div class="filters-bar" id="filters-bar"></div>
    <div class="products-grid" id="products-grid"></div>
  </div>
</section>

<!-- Tibia Section -->
<section class="tibia-section" id="tibia">
  <div class="container">
    <div class="tibia-grid">
      <div class="tibia-visual">
        <div class="tibia-logo">⚔️ TIBIA</div>
        <div class="coin-count">🪙 Tibia Coins — Entrega Rápida</div>
        <div class="tibia-coins-grid" id="tibia-packs"></div>
      </div>
      <div class="tibia-text">
        <div class="section-label">Tibia Store</div>
        <h2 class="section-title"><span class="hl">Tibia Coins</span><br>& Itens do Jogo</h2>
        <p>Compre Tibia Coins com segurança e praticidade. Aceitamos PIX, cartão de crédito/débito e boleto bancário. Entrega imediata após confirmação do pagamento.</p>
        <div class="tibia-features">
          <div class="tibia-feat"><span>✓</span> Entrega em até 5 minutos após pagamento</div>
          <div class="tibia-feat"><span>✓</span> Verificação do personagem via TibiaData API</div>
          <div class="tibia-feat"><span>✓</span> Suporte via WhatsApp 24/7</div>
          <div class="tibia-feat"><span>✓</span> Todos os mundos Tibia disponíveis</div>
          <div class="tibia-feat"><span>✓</span> Pagamento 100% seguro e criptografado</div>
        </div>
        <button class="btn-primary" onclick="filterCat('Tibia Coins');document.getElementById('products').scrollIntoView({behavior:'smooth'})">Ver Todos os Pacotes</button>
      </div>
    </div>
  </div>
</section>

<!-- Newsletter -->
<div class="container" style="padding-top:20px;padding-bottom:60px">
  <div class="newsletter-wrap">
    <div class="newsletter-inner">
      <div class="newsletter-text">
        <h3>Fique por <span style="background:linear-gradient(135deg,var(--purple2),var(--neon));-webkit-background-clip:text;-webkit-text-fill-color:transparent">dentro</span> das ofertas</h3>
        <p>Receba promoções exclusivas e lançamentos no seu e-mail</p>
      </div>
      <div class="newsletter-form">
        <input type="email" placeholder="Seu melhor e-mail">
        <button onclick="showToast('✅ Inscrito com sucesso! Bem-vindo(a)!')">Inscrever</button>
      </div>
    </div>
  </div>
</div>

<!-- Footer -->
<footer>
  <div class="container">
    <div class="footer-grid">
      <div class="footer-brand">
        <div class="footer-logo">GXD STORE</div>
        <p class="footer-desc">Sua loja de tecnologia, gaming e Tibia. Os melhores produtos com preços competitivos e entrega rápida para todo o Brasil.</p>
        <div class="social-links">
          <a href="#" class="social-link">📘</a>
          <a href="#" class="social-link">📸</a>
          <a href="#" class="social-link">🎵</a>
          <a href="#" class="social-link">💬</a>
          <a href="#" class="social-link">🎮</a>
        </div>
      </div>
      <div class="footer-col">
        <h4>Categorias</h4>
        <div class="footer-links">
          <a href="#">Mouses Gamer</a>
          <a href="#">Teclados Mecânicos</a>
          <a href="#">Headsets</a>
          <a href="#">Tibia Coins</a>
          <a href="#">Gadgets</a>
          <a href="#">Promoções</a>
        </div>
      </div>
      <div class="footer-col">
        <h4>Institucional</h4>
        <div class="footer-links">
          <a href="#">Sobre Nós</a>
          <a href="#">Política de Privacidade</a>
          <a href="#">Termos de Uso</a>
          <a href="#">Política de Troca</a>
          <a href="#">Vender Tibia Coins</a>
        </div>
      </div>
      <div class="footer-col">
        <h4>Suporte</h4>
        <div class="footer-links">
          <a href="#">Central de Ajuda</a>
          <a href="#">Rastrear Pedido</a>
          <a href="#">WhatsApp</a>
          <a href="#">Fale Conosco</a>
          <a href="#">FAQ</a>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <div class="footer-copy">© 2026 GXD Store — Todos os direitos reservados. CNPJ: 67.069.614/0001-09 — E-mail: sac@gxdstore.fun</div>
      <div class="payment-icons">
        <div class="pay-icon">PIX</div>
        <div class="pay-icon">Visa</div>
        <div class="pay-icon">Master</div>
        <div class="pay-icon">Elo</div>
        <div class="pay-icon">Boleto</div>
      </div>
    </div>
  </div>
</footer>

<!-- Cart Overlay & Sidebar -->
<div class="cart-overlay" id="cart-overlay" onclick="closeCart()"></div>
<div class="cart-sidebar" id="cart-sidebar">
  <div class="cart-header">
    <div class="cart-title">🛒 Carrinho</div>
    <button class="cart-close" onclick="closeCart()">✕</button>
  </div>
  <div class="cart-items" id="cart-items"></div>
  <div class="cart-footer" id="cart-footer" style="display:none">
    <div class="coupon-row">
      <input class="coupon-input" placeholder="Código do cupom" id="coupon-input">
      <button class="coupon-btn" onclick="applyCoupon()">Aplicar</button>
    </div>
    <div class="tibia-char-row" id="tibia-char-section" style="display:none">
      <div class="tibia-char-label">🎮 Nome do Personagem Tibia</div>
      <input class="tibia-char-input" placeholder="Ex: Garotinho Knight" id="char-name-input" oninput="lookupChar(this.value)">
      <div class="char-info" id="char-info"></div>
    </div>
    <div class="total-row"><span class="total-label">Subtotal</span><span class="total-val" id="subtotal-val">R$ 0,00</span></div>
    <div class="total-row" id="discount-row" style="display:none"><span class="total-label" style="color:#6ee7b7">Desconto</span><span class="total-val" style="color:#6ee7b7" id="discount-val">-R$ 0,00</span></div>
    <div class="total-row"><span class="total-label">Frete</span><span class="total-val" id="frete-val">Calcular</span></div>
    <div class="total-row" style="margin-top:8px;padding-top:8px;border-top:1px solid var(--glass-border)"><span style="font-size:16px;font-weight:700">Total</span><span class="total-final" id="total-val">R$ 0,00</span></div>
    <button class="checkout-btn" onclick="checkout()">Finalizar Compra →</button>
  </div>
</div>

<!-- Product Modal -->
<div class="modal-overlay" id="modal-overlay" onclick="closeModal(event)">
  <div class="product-modal" id="product-modal">
    <button class="modal-close" onclick="closeModalDirect()">✕</button>
    <div class="modal-inner" id="modal-inner"></div>
  </div>
</div>

<!-- Toast Container -->
<div class="toast-container" id="toast-container"></div>

<!-- Mobile Nav -->
<nav class="mobile-nav">
  <div class="mobile-nav-inner">
    <button class="mobile-nav-btn active" onclick="scrollTop()">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="m3 9 9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/></svg>
      Home
    </button>
    <button class="mobile-nav-btn" onclick="document.getElementById('products').scrollIntoView({behavior:'smooth'})">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="3" width="20" height="14" rx="2"/><line x1="8" y1="21" x2="16" y2="21"/><line x1="12" y1="17" x2="12" y2="21"/></svg>
      Produtos
    </button>
    <button class="mobile-nav-btn" onclick="document.getElementById('tibia').scrollIntoView({behavior:'smooth'})">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="M12 8v4l3 3"/></svg>
      Tibia
    </button>
    <button class="mobile-nav-btn" onclick="openCart()">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="9" cy="21" r="1"/><circle cx="20" cy="21" r="1"/><path d="M1 1h4l2.68 13.39a2 2 0 0 0 2 1.61h9.72a2 2 0 0 0 2-1.61L23 6H6"/></svg>
      Carrinho
    </button>
  </div>
</nav>

<script>
// ─── DATA ───────────────────────────────────────────────
const CATS=[
  {name:'Mouses',icon:'🖱️',count:18},
  {name:'Teclados',icon:'⌨️',count:12},
  {name:'Headsets',icon:'🎧',count:15},
  {name:'Tibia Coins',icon:'🪙',count:8},
  {name:'Itens Tibia',icon:'⚔️',count:24},
  {name:'Gadgets',icon:'📱',count:20},
  {name:'Promoções',icon:'🔥',count:35},
  {name:'Todos',icon:'🛍️',count:132},
];

const imgs={
  mouse:'https://images.unsplash.com/photo-1527814050087-3793815479db?w=300&h=300&fit=crop',
  keyboard:'https://images.unsplash.com/photo-1587829741301-dc798b83add3?w=300&h=300&fit=crop',
  headset:'https://images.unsplash.com/photo-1505740420928-5e560c06d30e?w=300&h=300&fit=crop',
  gadget:'https://images.unsplash.com/photo-1523275335684-37898b6baf30?w=300&h=300&fit=crop',
  coin:'https://images.unsplash.com/photo-1633158829585-23ba8f7c8caf?w=300&h=300&fit=crop',
  item:'https://images.unsplash.com/photo-1511512578047-dfb367046420?w=300&h=300&fit=crop',
};

const PRODUCTS=[
  {id:1,name:'Mouse Gamer HyperX Pulsefire FPS',cat:'Mouses',img:imgs.mouse,price:189.90,oldPrice:239.90,rating:4.8,reviews:312,badge:'discount',badgeText:'-21%',desc:'Mouse gamer de alta precisão com sensor óptico de 16.000 DPI, iluminação RGB e design ergonômico para longas sessões de jogo.',specs:{DPI:'200 - 16.000',Botões:'6 programáveis',Peso:'95g',Cabo:'1.8m trançado',Conexão:'USB'}},
  {id:2,name:'Teclado Mecânico Redragon K530',cat:'Teclados',img:imgs.keyboard,price:299.90,oldPrice:399.90,rating:4.7,reviews:198,badge:'hot',badgeText:'🔥 Top',desc:'Teclado mecânico compacto 60% com switches Red lineares, iluminação RGB por tecla e construção em alumínio premium.',specs:{Layout:'60% ABNT2',Switch:'Red Linear',Iluminação:'RGB por tecla','N-Key Rollover':'Sim',Material:'Alumínio + ABS'}},
  {id:3,name:'Headset Gamer JBL Quantum 100',cat:'Headsets',img:imgs.headset,price:1490,oldPrice:1990,rating:4.6,reviews:445,badge:'discount',badgeText:'-25%',desc:'Headset com som surround 7.1, microfone flip-up com cancelamento de ruído e almofadas memory foam.',specs:{Driver:'50mm',Frequência:'20Hz-20kHz',Microfone:'Flip-up',Cabo:'1.5m',Compatibilidade:'PC/PS/Xbox/Switch'}},
  {id:4,name:'Tibia Coins 250 TC',cat:'Tibia Coins',img:imgs.coin,price:51.90,oldPrice:56.90,rating:5.0,reviews:821,badge:'discount',badgeText:'-9%',desc:'Pacote de 250 Tibia Coins. Entrega instantânea no personagem informado. Válido para todos os mundos.',specs:{Quantidade:'250 TC',Entrega:'Instantânea',Mundos:'Todos',Pagamento:'PIX/Cartão/Boleto',Garantia:'100%'}},
  {id:5,name:'Tibia Coins 750 TC',cat:'Tibia Coins',img:imgs.coin,price:149.90,oldPrice:170.70,rating:5.0,reviews:634,badge:'hot',badgeText:'🎮 Popular',desc:'Pacote com 750 Tibia Coins com desconto especial. Melhor custo-benefício para jogadores frequentes.',specs:{Quantidade:'750 TC',Entrega:'Instantânea',Mundos:'Todos',Pagamento:'PIX/Cartão/Boleto',Bonus:'+5% de bônus'}},
  {id:6,name:'Gadget Smart Watch Serie 8',cat:'Gadgets',img:imgs.gadget,price:389.90,oldPrice:499.90,rating:4.5,reviews:267,badge:'new',badgeText:'Novo',desc:'Smartwatch com monitor cardíaco, GPS integrado, 18 modos esportivos e bateria de 36h.',specs:{Tela:'1.9" AMOLED',GPS:'Sim','Bateria':'36 horas',Resistência:'5ATM',Compatibilidade:'Android/iOS'}},
  {id:7,name:'Mouse Pad XL RGB 900x400',cat:'Gadgets',img:imgs.mouse,price:89.90,oldPrice:129.90,rating:4.7,reviews:189,badge:'discount',badgeText:'-31%',desc:'Mouse pad extra grande com iluminação RGB nas bordas, superfície de controle premium e base antiderrapante.',specs:{Dimensões:'900x400x4mm',Superfície:'Tecido premium',Iluminação:'RGB 16M cores',Base:'Borracha antiderrapante',USB:'Sim'}},
  {id:8,name:'Espada Excalibur — Item Tibia',cat:'Itens Tibia',img:imgs.item,price:79.90,oldPrice:null,rating:4.9,reviews:156,badge:'new',badgeText:'Item',desc:'Item raro do jogo Tibia. Atk+45 Def+25. Entrega direta para o personagem via Trade segura.',specs:{Ataque:'45',Defesa:'25',Tipo:'Espada','Nível Req.':'100',Vocação:'Knights'}},
  {id:9,name:'Headset Logitech G435',cat:'Headsets',img:imgs.headset,price:279.90,oldPrice:349.90,rating:4.8,reviews:203,badge:'discount',badgeText:'-20%',desc:'Headset sem fio leve com 18h de bateria, compatível com Dolby Atmos e microfone beamforming.',specs:{Tipo:'Sem Fio',Bateria:'18 horas',Driver:'40mm',Peso:'165g',Microfone:'Beamforming'}},
  {id:10,name:'Teclado HyperX Alloy Origins',cat:'Teclados',img:imgs.keyboard,price:449.90,oldPrice:549.90,rating:4.9,reviews:387,badge:'hot',badgeText:'🔥 Hot',desc:'Teclado mecânico full-size com switches HyperX Red, corpo em alumínio e iluminação RGB individual.',specs:{Layout:'Full-Size',Switch:'HyperX Red',Frame:'Alumínio avião',Backlight:'RGB individual',USB:'Type-C detachável'}},
  {id:11,name:'Tibia Coins 1500 TC',cat:'Tibia Coins',img:imgs.coin,price:289.90,oldPrice:341.10,rating:5.0,reviews:412,badge:'hot',badgeText:'🔥 Melhor',desc:'Maior pacote disponível — 1500 Tibia Coins com maior economia por TC. Ideal para garantir seu itens&treino.',specs:{Quantidade:'1500 TC',Entrega:'Instantânea',Mundos:'Todos',Economia:'15% por TC',Bonus:'+10% de bônus'}},
  {id:12,name:'Webcam Logitech C920 HD',cat:'Gadgets',img:imgs.gadget,price:329.90,oldPrice:399.90,rating:4.7,reviews:241,badge:'discount',badgeText:'-18%',desc:'Webcam Full HD 1080p/30fps com foco automático, microfone duplo estéreo e compatível com OBS.',specs:{Resolução:'1080p/30fps',Foco:'Automático',Microfone:'Duplo estéreo',FOV:'78°',Interface:'USB-A'}},
];

const TIBIA_PACKS=[
  {amount:'250 TC',price:'R$ 51,90',old:'R$ 56,90'},
  {amount:'500 TC',price:'R$ 99,90',old:'R$ 113,80'},
  {amount:'750 TC',price:'R$ 149,90',old:'R$ 170,70'},
  {amount:'1500 TC',price:'R$ 289,90',old:'R$ 341,10'},
];

// ─── STATE ─────────────────────────────────────────────
let cart=[];
let wishlist=new Set();
let currentCat='Todos';
let currentSort='featured';
let searchQ='';
let discount=0;
let currentProduct=null;
let slideIdx=0;
let slideTimer;

// ─── SLIDER ────────────────────────────────────────────
function startSlider(){
  slideTimer=setInterval(()=>changeSlide(1),5000);
}
function changeSlide(d){
  const slides=document.querySelectorAll('.slide');
  const dots=document.querySelectorAll('.dot');
  slides[slideIdx].classList.remove('active');
  dots[slideIdx].classList.remove('active');
  slideIdx=(slideIdx+d+slides.length)%slides.length;
  slides[slideIdx].classList.add('active');
  dots[slideIdx].classList.add('active');
  clearInterval(slideTimer);startSlider();
}
function goSlide(i){
  const slides=document.querySelectorAll('.slide');
  const dots=document.querySelectorAll('.dot');
  slides[slideIdx].classList.remove('active');
  dots[slideIdx].classList.remove('active');
  slideIdx=i;
  slides[slideIdx].classList.add('active');
  dots[slideIdx].classList.add('active');
  clearInterval(slideTimer);startSlider();
}

// ─── CATEGORIES ────────────────────────────────────────
function renderCats(){
  const g=document.getElementById('cats-grid');
  g.innerHTML=CATS.map(c=>`
    <div class="cat-card ${currentCat===c.name?'active':''}" onclick="filterCat('${c.name}')">
      <div class="cat-icon">${c.icon}</div>
      <div class="cat-name">${c.name}</div>
      <div class="cat-count">${c.count} produtos</div>
    </div>
  `).join('');
}

function filterCat(cat){
  currentCat=cat;
  renderCats();
  renderProducts();
  document.getElementById('products').scrollIntoView({behavior:'smooth'});
}

// ─── FILTERS ────────────────────────────────────────────
function renderFilters(){
  const f=document.getElementById('filters-bar');
  const sorts=[
    {v:'featured',l:'Destaques'},
    {v:'price_asc',l:'Menor Preço'},
    {v:'price_desc',l:'Maior Preço'},
    {v:'rating',l:'Avaliação'},
    {v:'reviews',l:'Mais Vendidos'},
  ];
  f.innerHTML=`
    ${CATS.slice(0,7).map(c=>`
      <button class="filter-btn ${currentCat===c.name?'active':''}" onclick="filterCat('${c.name}')">
        ${c.icon} ${c.name}
      </button>
    `).join('')}
    <div class="sort-wrap">
      <span class="sort-label">Ordenar:</span>
      <select class="filter-select" onchange="setSort(this.value)">
        ${sorts.map(s=>`<option value="${s.v}" ${currentSort===s.v?'selected':''}>${s.l}</option>`).join('')}
      </select>
    </div>
  `;
}

function setSort(v){currentSort=v;renderProducts()}

// ─── PRODUCTS ────────────────────────────────────────────
function getFiltered(){
  let p=[...PRODUCTS];
  if(currentCat!=='Todos')p=p.filter(x=>x.cat===currentCat);
  if(currentCat==='Promoções')p=PRODUCTS.filter(x=>x.oldPrice);
  if(searchQ)p=p.filter(x=>x.name.toLowerCase().includes(searchQ.toLowerCase())||x.cat.toLowerCase().includes(searchQ.toLowerCase()));
  if(currentSort==='price_asc')p.sort((a,b)=>a.price-b.price);
  else if(currentSort==='price_desc')p.sort((a,b)=>b.price-a.price);
  else if(currentSort==='rating')p.sort((a,b)=>b.rating-a.rating);
  else if(currentSort==='reviews')p.sort((a,b)=>b.reviews-a.reviews);
  return p;
}

function renderProducts(){
  renderFilters();
  const p=getFiltered();
  const g=document.getElementById('products-grid');
  if(!p.length){
    g.innerHTML=`<div style="grid-column:1/-1;text-align:center;padding:60px;color:var(--gray)"><div style="font-size:48px;margin-bottom:16px">🔍</div><p>Nenhum produto encontrado para "${searchQ||currentCat}"</p></div>`;
    return;
  }
  g.innerHTML=p.map(prod=>cardHTML(prod)).join('');
}

function stars(r){
  const f=Math.floor(r);
  const h=r%1>=0.5?1:0;
  return '★'.repeat(f)+(h?'½':'')+'☆'.repeat(5-f-h);
}

function fmtPrice(v){return'R$ '+v.toFixed(2).replace('.',',').replace(/\B(?=(\d{3})+(?!\d))/g,'.')}

function cardHTML(p){
  const discount=p.oldPrice?Math.round((1-p.price/p.oldPrice)*100):0;
  return`
  <div class="product-card" onclick="openProduct(${p.id})">
    <div class="card-img">
      <img src="${p.img}" alt="${p.name}" loading="lazy">
      <div class="card-badges">
        ${p.badge==='discount'?`<span class="badge-discount">-${discount}%</span>`:''}
        ${p.badge==='new'?`<span class="badge-new">NOVO</span>`:''}
        ${p.badge==='hot'?`<span class="badge-hot">${p.badgeText||'HOT'}</span>`:''}
      </div>
      <button class="wishlist-btn ${wishlist.has(p.id)?'active':''}" onclick="event.stopPropagation();toggleWishItem(${p.id})" title="Lista de desejos">
        ${wishlist.has(p.id)?'❤️':'🤍'}
      </button>
    </div>
    <div class="card-body">
      <div class="card-cat">${p.cat}</div>
      <div class="card-name">${p.name}</div>
      <div class="card-stars">
        <span class="stars">${'★'.repeat(Math.round(p.rating))}</span>
        <span class="review-count">(${p.reviews})</span>
      </div>
      <div class="card-price">
        ${p.oldPrice?`<span class="price-old">${fmtPrice(p.oldPrice)}</span>`:''}
        <span class="price-new"><small>R$</small> ${p.price.toFixed(2).replace('.',',')}</span>
      </div>
      <div class="card-actions" onclick="event.stopPropagation()">
        <button class="btn-buy" onclick="buyNow(${p.id})">Comprar</button>
        <button class="btn-cart" onclick="addToCart(${p.id})">
          <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="9" cy="21" r="1"/><circle cx="20" cy="21" r="1"/><path d="M1 1h4l2.68 13.39a2 2 0 0 0 2 1.61h9.72a2 2 0 0 0 2-1.61L23 6H6"/></svg>
          Carrinho
        </button>
      </div>
    </div>
  </div>`;
}

// ─── TIBIA PACKS ────────────────────────────────────────
function renderTibiaPacks(){
  const g=document.getElementById('tibia-packs');
  g.innerHTML=TIBIA_PACKS.map(p=>`
    <div class="coin-pack" onclick="addCoinPack('${p.amount}','${p.price}')">
      <div class="coin-pack-amount">🪙 ${p.amount}</div>
      <div class="coin-pack-price">${p.price}</div>
      <div class="coin-pack-old">${p.old}</div>
    </div>
  `).join('');
}

function addCoinPack(amount,price){
  const p=price.replace('R$ ','').replace(',','.');
  const prod={id:'tc_'+Date.now(),name:'Tibia Coins '+amount,cat:'Tibia Coins',img:imgs.coin,price:parseFloat(p)};
  addCartItem(prod);
  showToast('🪙 '+amount+' adicionado ao carrinho!');
  openCart();
}

// ─── CART ───────────────────────────────────────────────
function addToCart(id){
  const p=PRODUCTS.find(x=>x.id===id);
  addCartItem(p);
  showToast('✅ '+p.name+' adicionado!');
  document.getElementById('cart-count').textContent=cart.reduce((a,x)=>a+x.qty,0);
}

function buyNow(id){
  addToCart(id);
  openCart();
}

function addCartItem(prod){
  const ex=cart.find(x=>x.id===prod.id);
  if(ex)ex.qty++;
  else cart.push({...prod,qty:1});
  updateCartCount();
  renderCart();
}

function removeFromCart(id){
  cart=cart.filter(x=>x.id!==id);
  updateCartCount();
  renderCart();
}

function updateQty(id,d){
  const item=cart.find(x=>x.id===id);
  if(!item)return;
  item.qty+=d;
  if(item.qty<=0)cart=cart.filter(x=>x.id!==id);
  updateCartCount();
  renderCart();
}

function updateCartCount(){
  const total=cart.reduce((a,x)=>a+x.qty,0);
  document.getElementById('cart-count').textContent=total;
}

function renderCart(){
  const ci=document.getElementById('cart-items');
  const cf=document.getElementById('cart-footer');
  const tibiaSection=document.getElementById('tibia-char-section');
  if(!cart.length){
    ci.innerHTML=`<div class="cart-empty"><div class="empty-icon">🛒</div><p style="font-weight:600">Seu carrinho está vazio</p><p style="font-size:13px">Adicione produtos para continuar</p><button class="btn-primary" onclick="closeCart()" style="margin-top:8px">Ver Produtos</button></div>`;
    cf.style.display='none';return;
  }
  cf.style.display='block';
  const hasTibia=cart.some(x=>x.cat&&x.cat.toLowerCase().includes('tibia'));
  tibiaSection.style.display=hasTibia?'block':'none';
  ci.innerHTML=cart.map(item=>`
    <div class="cart-item">
      <img class="cart-item-img" src="${item.img}" alt="${item.name}">
      <div class="cart-item-info">
        <div class="cart-item-name">${item.name}</div>
        <div class="cart-item-cat">${item.cat}</div>
        <div class="cart-item-price">${fmtPrice(item.price)}</div>
        <div class="cart-item-qty">
          <button class="qty-btn" onclick="updateQty('${item.id}',-1)">−</button>
          <span class="qty-num">${item.qty}</span>
          <button class="qty-btn" onclick="updateQty('${item.id}',1)">+</button>
        </div>
      </div>
      <button class="cart-del" onclick="removeFromCart('${item.id}')" title="Remover">✕</button>
    </div>
  `).join('');
  updateTotals();
}

function updateTotals(){
  const sub=cart.reduce((a,x)=>a+x.price*x.qty,0);
  const disc=sub*discount;
  const total=sub-disc;
  document.getElementById('subtotal-val').textContent=fmtPrice(sub);
  document.getElementById('total-val').textContent=fmtPrice(total);
  if(disc>0){
    document.getElementById('discount-row').style.display='flex';
    document.getElementById('discount-val').textContent='-'+fmtPrice(disc);
  }
  const frete=sub>=299?'GRÁTIS':'A calcular';
  document.getElementById('frete-val').textContent=frete;
  if(frete==='GRÁTIS')document.getElementById('frete-val').style.color='#6ee7b7';
}

function applyCoupon(){
  const code=document.getElementById('coupon-input').value.toUpperCase().trim();
  if(code==='GAROTIIN10'){discount=0.1;showToast('🎉 Cupom aplicado! 10% de desconto!')}
  else if(code==='TIBIA5'){discount=0.05;showToast('🎉 Cupom Tibia! 5% de desconto!')}
  else{showToast('❌ Cupom inválido');return}
  updateTotals();
}

function openCart(){
  document.getElementById('cart-overlay').classList.add('open');
  document.getElementById('cart-sidebar').classList.add('open');
  renderCart();
}
function closeCart(){
  document.getElementById('cart-overlay').classList.remove('open');
  document.getElementById('cart-sidebar').classList.remove('open');
}

function checkout(){
  if(!cart.length)return;
  showToast('🎉 Pedido realizado! Redirecionando para pagamento...');
  setTimeout(()=>{cart=[];updateCartCount();renderCart();closeCart();},2000);
}

// ─── WISHLIST ───────────────────────────────────────────
function toggleWishItem(id){
  if(wishlist.has(id)){wishlist.delete(id);showToast('Removido da lista de desejos')}
  else{wishlist.add(id);showToast('❤️ Adicionado à lista de desejos!')}
  const wc=document.getElementById('wish-count');
  wc.textContent=wishlist.size;
  wc.style.display=wishlist.size?'flex':'none';
  renderProducts();
}
function toggleWishlist(){
  if(wishlist.size)showToast('❤️ Você tem '+wishlist.size+' item(s) na lista de desejos');
  else showToast('Sua lista de desejos está vazia');
}

// ─── PRODUCT MODAL ──────────────────────────────────────
function openProduct(id){
  const p=PRODUCTS.find(x=>x.id===id);
  if(!p)return;
  currentProduct=p;
  const specs=p.specs?Object.entries(p.specs).map(([k,v])=>`<tr><td>${k}</td><td>${v}</td></tr>`).join(''):'';
  document.getElementById('modal-inner').innerHTML=`
    <div class="modal-grid">
      <div>
        <div class="modal-img-main">
          <img src="${p.img}" alt="${p.name}" id="modal-main-img">
        </div>
        <div class="modal-thumbs">
          ${[p.img,p.img,p.img].map((img,i)=>`
            <div class="modal-thumb ${i===0?'active':''}" onclick="setMainImg('${img}',this)">
              <img src="${img}" alt="">
            </div>
          `).join('')}
        </div>
      </div>
      <div class="modal-info">
        <div class="modal-cat">${p.cat}</div>
        <div class="modal-name">${p.name}</div>
        <div class="modal-rating">
          <span style="color:#f59e0b;font-size:16px">${'★'.repeat(Math.round(p.rating))}</span>
          <span style="font-size:13px;color:var(--gray)">${p.rating} (${p.reviews} avaliações)</span>
        </div>
        <div class="modal-price-block">
          ${p.oldPrice?`<div class="modal-price-old">${fmtPrice(p.oldPrice)}</div>`:''}
          <div class="modal-price-new" style="background:linear-gradient(135deg,var(--purple2),var(--neon));-webkit-background-clip:text;-webkit-text-fill-color:transparent">${fmtPrice(p.price)}</div>
          <div style="font-size:12px;color:var(--gray);margin-top:4px">ou 12x de ${fmtPrice(p.price/12)} sem juros</div>
        </div>
        <div class="modal-desc">${p.desc}</div>
        ${specs?`
          <div>
            <div style="font-size:13px;font-weight:700;color:var(--gray2);letter-spacing:1px;text-transform:uppercase;margin-bottom:8px">Especificações</div>
            <table class="specs-table">${specs}</table>
          </div>
        `:''}
        <div class="modal-actions">
          <button class="btn-primary" onclick="buyNow(${p.id});closeModalDirect()">⚡ Comprar Agora</button>
          <button class="btn-cart" onclick="addToCart(${p.id})">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="9" cy="21" r="1"/><circle cx="20" cy="21" r="1"/><path d="M1 1h4l2.68 13.39a2 2 0 0 0 2 1.61h9.72a2 2 0 0 0 2-1.61L23 6H6"/></svg>
            Adicionar ao Carrinho
          </button>
        </div>
      </div>
    </div>
  `;
  document.getElementById('modal-overlay').classList.add('open');
  document.body.style.overflow='hidden';
}

function setMainImg(src,el){
  document.getElementById('modal-main-img').src=src;
  document.querySelectorAll('.modal-thumb').forEach(t=>t.classList.remove('active'));
  el.classList.add('active');
}

function closeModal(e){
  if(e.target===document.getElementById('modal-overlay'))closeModalDirect();
}
function closeModalDirect(){
  document.getElementById('modal-overlay').classList.remove('open');
  document.body.style.overflow='';
}

// ─── TIBIA CHAR LOOKUP ──────────────────────────────────
let charTimer;
function lookupChar(name){
  clearTimeout(charTimer);
  const info=document.getElementById('char-info');
  if(!name||name.length<3){info.classList.remove('show');return}
  charTimer=setTimeout(async()=>{
    info.classList.add('show');
    info.textContent='🔍 Buscando personagem...';
    try{
      const r=await fetch(`https://api.tibiadata.com/v4/character/${encodeURIComponent(name)}`);
      const d=await r.json();
      if(d.character&&d.character.character){
        const c=d.character.character;
        info.innerHTML=`✅ <strong>${c.name}</strong> — ${c.vocation} Nível ${c.level} — Mundo: ${c.world}`;
      }else{
        info.innerHTML='❌ Personagem não encontrado';
      }
    }catch{
      info.innerHTML='⚠️ Não foi possível verificar o personagem';
    }
  },800);
}

// ─── SEARCH ─────────────────────────────────────────────
function handleSearch(v){
  searchQ=v;
  currentCat='Todos';
  renderCats();
  renderProducts();
  if(v)document.getElementById('products').scrollIntoView({behavior:'smooth'});
}

// ─── TOAST ─────────────────────────────────────────────
function showToast(msg){
  const c=document.getElementById('toast-container');
  const t=document.createElement('div');
  t.className='toast success';
  t.innerHTML=msg;
  c.appendChild(t);
  setTimeout(()=>{
    t.style.animation='slideOut .3s ease forwards';
    setTimeout(()=>t.remove(),300);
  },3000);
}

// ─── MISC ───────────────────────────────────────────────
function scrollTop(){window.scrollTo({top:0,behavior:'smooth'})}

// ─── INIT ───────────────────────────────────────────────
document.addEventListener('DOMContentLoaded',()=>{
  renderCats();
  renderFilters();
  renderProducts();
  renderTibiaPacks();
  startSlider();
  setTimeout(()=>{
    document.getElementById('loader').classList.add('hidden');
  },1600);
  // initial cart count
  document.getElementById('cart-count').textContent='0';
});
</script>
</body>
</html>
