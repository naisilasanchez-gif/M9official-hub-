<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Official Hub — M9WIN · PETIR19 · POKERBOLA</title>

    <!-- Google Fonts Premium -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800;14..32,900&display=swap" rel="stylesheet" />
    
    <!-- Font Awesome 6 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />

    <style>
        /* ===== RESET & BASE ===== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: #0a0808;
            padding: 24px;
            position: relative;
        }

        /* Background efek mewah */
        body::before {
            content: '';
            position: fixed;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: 
                radial-gradient(ellipse at 20% 30%, rgba(200, 20, 30, 0.06) 0%, transparent 50%),
                radial-gradient(ellipse at 80% 70%, rgba(255, 215, 0, 0.04) 0%, transparent 50%),
                radial-gradient(ellipse at 50% 100%, rgba(120, 10, 20, 0.05) 0%, transparent 40%);
            z-index: 0;
            pointer-events: none;
        }

        /* ===== CARD UTAMA ===== */
        .hub-card {
            position: relative;
            z-index: 1;
            max-width: 540px;
            width: 100%;
            background: rgba(12, 10, 10, 0.94);
            backdrop-filter: blur(24px);
            -webkit-backdrop-filter: blur(24px);
            border-radius: 48px;
            padding: 44px 36px 36px;
            border: 1px solid rgba(255, 215, 0, 0.06);
            box-shadow: 0 40px 80px rgba(0, 0, 0, 0.9), 
                        inset 0 1px 0 rgba(255, 215, 0, 0.04),
                        0 0 80px rgba(200, 20, 30, 0.02);
            transition: 0.4s ease;
        }

        /* ===== HEADER ===== */
        .brand-header {
            text-align: center;
            margin-bottom: 32px;
        }

        .logo-wrapper {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 8px;
            margin-bottom: 6px;
        }

        /* Logo area dengan efek emas */
        .logo-main {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            flex-wrap: wrap;
        }

        .brand-name {
            font-size: 32px;
            font-weight: 900;
            letter-spacing: -0.5px;
            background: linear-gradient(135deg, #ffd700 0%, #f5a623 40%, #ffd700 70%, #f5a623 100%);
            background-size: 200% 200%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: shimmer-gold 4s ease-in-out infinite;
        }

        @keyframes shimmer-gold {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }

        /* Sub-brand di bawah M9WIN */
        .sub-brands {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 16px;
            margin-top: 2px;
            flex-wrap: wrap;
        }

        .sub-brand {
            font-size: 13px;
            font-weight: 700;
            letter-spacing: 1.5px;
            color: rgba(255, 255, 255, 0.3);
            text-transform: uppercase;
            position: relative;
        }

        .sub-brand.petir {
            color: rgba(255, 215, 0, 0.5);
        }

        .sub-brand.poker {
            color: rgba(255, 255, 255, 0.3);
        }

        .sub-brand .dot {
            display: inline-block;
            width: 4px;
            height: 4px;
            border-radius: 50%;
            background: rgba(255, 215, 0, 0.2);
            margin: 0 6px;
            vertical-align: middle;
        }

        /* Tagline */
        .tagline {
            font-size: 10px;
            font-weight: 400;
            letter-spacing: 2px;
            color: rgba(255, 215, 0, 0.15);
            margin-top: 8px;
            text-transform: uppercase;
        }

        .tagline span {
            color: rgba(200, 20, 30, 0.3);
            font-weight: 600;
        }

        .divider-glow {
            width: 80px;
            height: 2px;
            margin: 14px auto 0;
            background: linear-gradient(90deg, transparent, rgba(255, 215, 0, 0.2), rgba(200, 20, 30, 0.2), transparent);
            border-radius: 4px;
        }

        /* ===== SECTION LABEL ===== */
        .section-label {
            display: flex;
            align-items: center;
            gap: 12px;
            margin: 28px 0 16px;
            color: rgba(255, 255, 255, 0.15);
            font-size: 10px;
            font-weight: 700;
            letter-spacing: 3px;
            text-transform: uppercase;
        }

        .section-label .line {
            flex: 1;
            height: 1px;
            background: linear-gradient(90deg, rgba(255, 215, 0, 0.06), transparent);
        }

        .section-label .line-right {
            flex: 1;
            height: 1px;
            background: linear-gradient(90deg, transparent, rgba(255, 215, 0, 0.06));
        }

        .section-label i {
            font-size: 14px;
            opacity: 0.5;
        }

        /* ===== TOMBOL SOSMED ===== */
        .social-link {
            display: flex;
            align-items: center;
            gap: 14px;
            padding: 16px 20px;
            margin-bottom: 10px;
            border-radius: 18px;
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 215, 0, 0.04);
            color: #fff;
            text-decoration: none;
            transition: all 0.35s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            position: relative;
            overflow: hidden;
            cursor: pointer;
        }

        .social-link::before {
            content: '';
            position: absolute;
            inset: 0;
            border-radius: 18px;
            padding: 1px;
            background: linear-gradient(135deg, rgba(255, 215, 0, 0.12), rgba(200, 20, 30, 0.06));
            -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
            -webkit-mask-composite: xor;
            mask-composite: exclude;
            opacity: 0;
            transition: opacity 0.4s ease;
        }

        .social-link:hover {
            transform: translateY(-2px) scale(1.01);
            background: rgba(255, 215, 0, 0.03);
            border-color: rgba(255, 215, 0, 0.1);
            box-shadow: 0 12px 32px rgba(0, 0, 0, 0.5);
        }

        .social-link:hover::before {
            opacity: 1;
        }

        /* Icon kiri */
        .link-icon {
            width: 42px;
            height: 42px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            flex-shrink: 0;
            transition: 0.3s;
        }

        .link-icon.ig {
            background: linear-gradient(135deg, #f09433, #e6683c, #dc2743, #cc2366, #bc1888);
            color: #fff;
            box-shadow: 0 4px 16px rgba(225, 48, 108, 0.15);
        }

        .link-icon.ig-alt {
            background: linear-gradient(135deg, #833ab4, #fd1d1d, #fcb045);
            color: #fff;
            box-shadow: 0 4px 16px rgba(253, 29, 29, 0.15);
        }

        .link-icon.fb {
            background: #1877F2;
            color: #fff;
            box-shadow: 0 4px 16px rgba(24, 119, 242, 0.15);
        }

        .link-icon.fb-alt {
            background: linear-gradient(135deg, #1877F2, #0d65d9);
            color: #fff;
            box-shadow: 0 4px 16px rgba(24, 119, 242, 0.15);
        }

        /* Brand badge kecil di tombol */
        .brand-tag {
            font-size: 8px;
            font-weight: 700;
            letter-spacing: 0.8px;
            padding: 2px 8px;
            border-radius: 10px;
            background: rgba(255, 215, 0, 0.06);
            border: 1px solid rgba(255, 215, 0, 0.04);
            color: rgba(255, 215, 0, 0.2);
            text-transform: uppercase;
            margin-left: 6px;
        }

        .brand-tag.m9 {
            color: rgba(255, 215, 0, 0.25);
            border-color: rgba(255, 215, 0, 0.06);
        }

        .brand-tag.petir {
            color: rgba(255, 215, 0, 0.3);
            border-color: rgba(255, 215, 0, 0.08);
        }

        .brand-tag.poker {
            color: rgba(255, 255, 255, 0.15);
            border-color: rgba(255, 255, 255, 0.04);
        }

        .link-info {
            flex: 1;
            min-width: 0;
        }

        .link-title {
            font-size: 15px;
            font-weight: 600;
            color: #fff;
            letter-spacing: -0.2px;
        }

        .link-badge {
            font-size: 10px;
            font-weight: 500;
            color: rgba(255, 215, 0, 0.2);
            letter-spacing: 0.5px;
            margin-top: 2px;
        }

        .link-badge i {
            margin-right: 4px;
            font-size: 9px;
        }

        /* Tracking counter */
        .link-stats {
            font-size: 12px;
            font-weight: 600;
            color: rgba(255, 215, 0, 0.12);
            background: rgba(255, 215, 0, 0.02);
            padding: 4px 12px;
            border-radius: 20px;
            border: 1px solid rgba(255, 215, 0, 0.03);
            flex-shrink: 0;
            font-variant-numeric: tabular-nums;
            transition: 0.3s;
        }

        .social-link:hover .link-stats {
            color: rgba(255, 215, 0, 0.3);
            border-color: rgba(255, 215, 0, 0.06);
        }

        /* ===== TOMBOL DISABLED ===== */
        .social-link.disabled {
            opacity: 0.3;
            cursor: not-allowed;
            filter: grayscale(0.6);
        }

        .social-link.disabled:hover {
            transform: none !important;
            box-shadow: none !important;
            background: rgba(255, 255, 255, 0.02) !important;
            border-color: rgba(255, 215, 0, 0.04) !important;
        }

        .badge-coming {
            font-size: 8px;
            font-weight: 700;
            letter-spacing: 1px;
            text-transform: uppercase;
            color: rgba(255, 215, 0, 0.15);
            background: rgba(255, 215, 0, 0.03);
            padding: 2px 10px;
            border-radius: 12px;
            border: 1px solid rgba(255, 215, 0, 0.03);
            margin-left: 6px;
        }

        /* ===== FOOTER ===== */
        .hub-footer {
            margin-top: 32px;
            text-align: center;
            color: rgba(255, 215, 0, 0.06);
            font-size: 9px;
            letter-spacing: 2.5px;
            font-weight: 400;
            border-top: 1px solid rgba(255, 215, 0, 0.02);
            padding-top: 24px;
            text-transform: uppercase;
        }

        .hub-footer .powered {
            color: rgba(255, 215, 0, 0.08);
        }

        .hub-footer .powered strong {
            color: rgba(255, 215, 0, 0.12);
            font-weight: 700;
        }

        /* ===== RESPONSIVE ===== */
        @media (max-width: 480px) {
            .hub-card {
                padding: 28px 20px 24px;
                border-radius: 32px;
            }

            .brand-name {
                font-size: 26px;
            }
            .sub-brand {
                font-size: 11px;
            }
            .sub-brands {
                gap: 10px;
            }

            .social-link {
                padding: 14px 16px;
                gap: 12px;
            }
            .link-icon {
                width: 36px;
                height: 36px;
                font-size: 16px;
                border-radius: 10px;
            }
            .link-title {
                font-size: 14px;
            }
            .link-stats {
                font-size: 11px;
                padding: 3px 10px;
            }
            .section-label {
                font-size: 9px;
                margin: 22px 0 12px;
            }
            .brand-tag {
                font-size: 7px;
                padding: 1px 6px;
            }
        }
    </style>
</head>
<body>

    <div class="hub-card">

        <!-- ===== HEADER BRAND ===== -->
        <div class="brand-header">
            <div class="logo-wrapper">
                <div class="logo-main">
                    <span class="brand-name">M9WIN</span>
                </div>
                <div class="sub-brands">
                    <span class="sub-brand petir">⚡ PETIR19</span>
                    <span class="sub-brand"><span class="dot"></span></span>
                    <span class="sub-brand poker">♠ POKERBOLA</span>
                </div>
                <div class="tagline">
                    <span>formerly branded by M8WIN</span>
                </div>
            </div>
            <div class="divider-glow"></div>
        </div>

        <!-- ===== SECTION: INSTAGRAM ===== -->
        <div class="section-label">
            <span class="line"></span>
            <i class="fab fa-instagram" style="color:#E4405F;"></i>
            INSTAGRAM
            <span class="line-right"></span>
        </div>

        <!-- IG: Petir19 Official VIP -->
        <a href="https://www.instagram.com/petir19_official_vip/" target="_blank" class="social-link" data-link="ig1">
            <div class="link-icon ig"><i class="fab fa-instagram"></i></div>
            <div class="link-info">
                <div class="link-title">
                    Petir19 Official VIP
                    <span class="brand-tag petir">⚡ PETIR</span>
                </div>
                <div class="link-badge"><i class="fas fa-bolt"></i> Official Instagram</div>
            </div>
            <span class="link-stats" id="stats-ig1">0 klik</span>
        </a>

        <!-- IG: Official M9Win -->
        <a href="https://www.instagram.com/officialm9win/" target="_blank" class="social-link" data-link="ig2">
            <div class="link-icon ig-alt"><i class="fab fa-instagram"></i></div>
            <div class="link-info">
                <div class="link-title">
                    Official M9Win
                    <span class="brand-tag m9">M9</span>
                </div>
                <div class="link-badge"><i class="fas fa-bolt"></i> Official Instagram</div>
            </div>
            <span class="link-stats" id="stats-ig2">0 klik</span>
        </a>

        <!-- IG 3 - DISABLED -->
        <a href="#" class="social-link disabled" onclick="return false;">
            <div class="link-icon ig" style="opacity:0.3;"><i class="fab fa-instagram"></i></div>
            <div class="link-info">
                <div class="link-title">
                    Instagram 3
                    <span class="badge-coming">⏳ Segera</span>
                </div>
                <div class="link-badge">—</div>
            </div>
            <span class="link-stats">—</span>
        </a>

        <!-- ===== SECTION: FACEBOOK GROUP ===== -->
        <div class="section-label" style="margin-top: 32px;">
            <span class="line"></span>
            <i class="fab fa-facebook" style="color:#1877F2;"></i>
            FACEBOOK GROUP
            <span class="line-right"></span>
        </div>

        <!-- FB: Petir19 -->
        <a href="https://www.facebook.com/groups/petir19" target="_blank" class="social-link" data-link="fb1">
            <div class="link-icon fb"><i class="fab fa-facebook-f"></i></div>
            <div class="link-info">
                <div class="link-title">
                    Petir19
                    <span class="brand-tag petir">⚡ PETIR</span>
                </div>
                <div class="link-badge"><i class="fas fa-users"></i> Komunitas Facebook</div>
            </div>
            <span class="link-stats" id="stats-fb1">0 klik</span>
        </a>

        <!-- FB: Official M9Win -->
        <a href="https://www.facebook.com/groups/officialm9win" target="_blank" class="social-link" data-link="fb2">
            <div class="link-icon fb-alt"><i class="fab fa-facebook-f"></i></div>
            <div class="link-info">
                <div class="link-title">
                    Official M9Win
                    <span class="brand-tag m9">M9</span>
                </div>
                <div class="link-badge"><i class="fas fa-users"></i> Komunitas Facebook</div>
            </div>
            <span class="link-stats" id="stats-fb2">0 klik</span>
        </a>

        <!-- FB: PokerBola Official -->
        <a href="https://www.facebook.com/groups/pokerbolaofficial" target="_blank" class="social-link" data-link="fb3">
            <div class="link-icon fb"><i class="fab fa-facebook-f"></i></div>
            <div class="link-info">
                <div class="link-title">
                    PokerBola Official
                    <span class="brand-tag poker">♠ POKER</span>
                </div>
                <div class="link-badge"><i class="fas fa-users"></i> Komunitas Facebook</div>
            </div>
            <span class="link-stats" id="stats-fb3">0 klik</span>
        </a>

        <!-- ===== FOOTER ===== -->
        <div class="hub-footer">
            <div class="powered">
                <span>✦</span> &nbsp; <strong>POWERED BY M9WIN</strong> &nbsp; <span>✦</span>
            </div>
        </div>

    </div>

    <!-- ===== TRACKING SCRIPT ===== -->
    <script>
        (function() {
            'use strict';

            const STORAGE_KEY = 'osh_stats_2026';

            let stats = {};
            try {
                const saved = localStorage.getItem(STORAGE_KEY);
                if (saved) stats = JSON.parse(saved);
            } catch (e) { stats = {}; }

            const activeLinks = document.querySelectorAll('.social-link:not(.disabled)');
            activeLinks.forEach(el => {
                const key = el.dataset.link;
                if (key && !stats[key]) stats[key] = 0;
            });

            function updateDisplay() {
                activeLinks.forEach(el => {
                    const key = el.dataset.link;
                    if (key && stats[key] !== undefined) {
                        const counterEl = document.getElementById('stats-' + key);
                        if (counterEl) {
                            const count = stats[key];
                            counterEl.textContent = count + ' klik';
                            if (count > 0) {
                                counterEl.style.color = 'rgba(255,215,0,0.4)';
                                counterEl.style.borderColor = 'rgba(255,215,0,0.06)';
                            }
                        }
                    }
                });
            }

            activeLinks.forEach(el => {
                el.addEventListener('click', function(e) {
                    const key = this.dataset.link;
                    if (!key) return;

                    if (!stats[key]) stats[key] = 0;
                    stats[key] += 1;

                    try {
                        localStorage.setItem(STORAGE_KEY, JSON.stringify(stats));
                    } catch (e) {}

                    const counterEl = document.getElementById('stats-' + key);
                    if (counterEl) {
                        counterEl.textContent = stats[key] + ' klik';
                        if (stats[key] > 0) {
                            counterEl.style.color = 'rgba(255,215,0,0.4)';
                            counterEl.style.borderColor = 'rgba(255,215,0,0.06)';
                        }
                    }
                });
            });

            updateDisplay();

            window.resetStats = function() {
                if (confirm('Reset semua data klik?')) {
                    stats = {};
                    activeLinks.forEach(el => {
                        const key = el.dataset.link;
                        if (key) stats[key] = 0;
                    });
                    localStorage.setItem(STORAGE_KEY, JSON.stringify(stats));
                    updateDisplay();
                    activeLinks.forEach(el => {
                        const key = el.dataset.link;
                        const counterEl = document.getElementById('stats-' + key);
                        if (counterEl) {
                            counterEl.style.color = 'rgba(255,215,0,0.12)';
                            counterEl.style.borderColor = 'rgba(255,215,0,0.03)';
                        }
                    });
                }
            };

            console.log('⚡ M9WIN · PETIR19 · POKERBOLA — Official Hub siap!');
            console.log('📊 Ketik resetStats() di console untuk reset data.');
        })();
    </script>

</body>
</html>
