[page.htm](https://github.com/user-attachments/files/31177030/page.htm)
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Official Social Hub</title>

    <!-- Google Fonts Premium -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet" />
    
    <!-- Font Awesome 6 (Icons) -->
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
            background: #0b0b0e;
            padding: 24px;
            position: relative;
        }

        /* Background efek glow */
        body::before {
            content: '';
            position: fixed;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(ellipse at 30% 50%, rgba(88, 50, 255, 0.08) 0%, transparent 60%),
                        radial-gradient(ellipse at 70% 80%, rgba(255, 50, 100, 0.06) 0%, transparent 60%);
            z-index: 0;
            pointer-events: none;
        }

        /* ===== CARD UTAMA ===== */
        .hub-card {
            position: relative;
            z-index: 1;
            max-width: 520px;
            width: 100%;
            background: rgba(18, 18, 24, 0.85);
            backdrop-filter: blur(24px);
            -webkit-backdrop-filter: blur(24px);
            border-radius: 48px;
            padding: 44px 36px 36px;
            border: 1px solid rgba(255, 255, 255, 0.06);
            box-shadow: 0 40px 80px rgba(0, 0, 0, 0.7), inset 0 1px 0 rgba(255, 255, 255, 0.04);
            transition: 0.4s ease;
        }

        /* ===== HEADER ===== */
        .brand-header {
            text-align: center;
            margin-bottom: 32px;
        }

        .logo-wrapper {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 14px;
            margin-bottom: 10px;
        }

        .logo-icon {
            width: 52px;
            height: 52px;
            background: linear-gradient(135deg, #7c3aed, #ec4899);
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 26px;
            color: #fff;
            box-shadow: 0 8px 24px rgba(124, 58, 237, 0.3);
        }

        .brand-name {
            font-size: 22px;
            font-weight: 800;
            letter-spacing: -0.5px;
            background: linear-gradient(135deg, #ffffff 60%, rgba(255, 255, 255, 0.6));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .brand-sub {
            color: rgba(255, 255, 255, 0.4);
            font-size: 13px;
            font-weight: 400;
            letter-spacing: 2px;
            text-transform: uppercase;
            margin-top: 2px;
        }

        .divider-glow {
            width: 60px;
            height: 2px;
            margin: 16px auto 0;
            background: linear-gradient(90deg, transparent, rgba(124, 58, 237, 0.5), rgba(236, 72, 153, 0.5), transparent);
            border-radius: 4px;
        }

        /* ===== SECTION LABEL ===== */
        .section-label {
            display: flex;
            align-items: center;
            gap: 12px;
            margin: 28px 0 16px;
            color: rgba(255, 255, 255, 0.3);
            font-size: 11px;
            font-weight: 600;
            letter-spacing: 2.5px;
            text-transform: uppercase;
        }

        .section-label .line {
            flex: 1;
            height: 1px;
            background: linear-gradient(90deg, rgba(255, 255, 255, 0.08), transparent);
        }

        .section-label .line-right {
            flex: 1;
            height: 1px;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.08));
        }

        .section-label i {
            font-size: 14px;
            opacity: 0.6;
        }

        /* ===== TOMBOL SOSMED ===== */
        .social-link {
            display: flex;
            align-items: center;
            gap: 14px;
            padding: 16px 20px;
            margin-bottom: 10px;
            border-radius: 18px;
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.05);
            color: #fff;
            text-decoration: none;
            transition: all 0.3s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            position: relative;
            overflow: hidden;
            cursor: pointer;
        }

        /* Hover efek */
        .social-link::before {
            content: '';
            position: absolute;
            inset: 0;
            border-radius: 18px;
            padding: 1px;
            background: linear-gradient(135deg, rgba(124, 58, 237, 0.2), rgba(236, 72, 153, 0.2));
            -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
            -webkit-mask-composite: xor;
            mask-composite: exclude;
            opacity: 0;
            transition: opacity 0.4s ease;
        }

        .social-link:hover {
            transform: translateY(-2px) scale(1.01);
            background: rgba(255, 255, 255, 0.07);
            border-color: rgba(255, 255, 255, 0.12);
            box-shadow: 0 12px 32px rgba(0, 0, 0, 0.4);
        }

        .social-link:hover::before {
            opacity: 1;
        }

        /* Icon kiri */
        .link-icon {
            width: 40px;
            height: 40px;
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
        }

        .link-icon.fb {
            background: #1877F2;
            color: #fff;
        }

        .link-icon.ig-alt {
            background: linear-gradient(135deg, #833ab4, #fd1d1d, #fcb045);
            color: #fff;
        }

        /* Info tengah */
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
            color: rgba(255, 255, 255, 0.3);
            letter-spacing: 0.5px;
            margin-top: 1px;
        }

        .link-badge i {
            margin-right: 4px;
            font-size: 9px;
        }

        /* Tracking counter di kanan */
        .link-stats {
            font-size: 12px;
            font-weight: 600;
            color: rgba(255, 255, 255, 0.2);
            background: rgba(255, 255, 255, 0.04);
            padding: 4px 12px;
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.04);
            flex-shrink: 0;
            font-variant-numeric: tabular-nums;
            transition: 0.3s;
        }

        .social-link:hover .link-stats {
            color: rgba(255, 255, 255, 0.5);
            border-color: rgba(255, 255, 255, 0.08);
        }

        /* ===== TOMBOL "TAMBAH NANTI" (DISABLED) ===== */
        .social-link.disabled {
            opacity: 0.4;
            cursor: not-allowed;
            filter: grayscale(0.6);
        }

        .social-link.disabled:hover {
            transform: none !important;
            box-shadow: none !important;
            background: rgba(255, 255, 255, 0.03) !important;
            border-color: rgba(255, 255, 255, 0.05) !important;
        }

        .social-link.disabled .link-stats {
            opacity: 0.3;
        }

        .badge-coming {
            font-size: 9px;
            font-weight: 700;
            letter-spacing: 0.8px;
            text-transform: uppercase;
            color: rgba(255, 255, 255, 0.2);
            background: rgba(255, 255, 255, 0.04);
            padding: 2px 10px;
            border-radius: 12px;
            border: 1px solid rgba(255, 255, 255, 0.04);
            margin-left: 6px;
        }

        /* ===== FOOTER ===== */
        .hub-footer {
            margin-top: 32px;
            text-align: center;
            color: rgba(255, 255, 255, 0.15);
            font-size: 11px;
            letter-spacing: 1.5px;
            font-weight: 400;
            border-top: 1px solid rgba(255, 255, 255, 0.03);
            padding-top: 24px;
        }

        .hub-footer span {
            opacity: 0.5;
        }

        /* ===== RESPONSIVE ===== */
        @media (max-width: 480px) {
            .hub-card {
                padding: 28px 20px 24px;
                border-radius: 32px;
            }

            .brand-name {
                font-size: 18px;
            }
            .logo-icon {
                width: 44px;
                height: 44px;
                font-size: 20px;
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
                font-size: 10px;
                margin: 22px 0 12px;
            }
        }

        @media (max-width: 380px) {
            .hub-card {
                padding: 20px 14px 18px;
            }
            .social-link {
                padding: 12px 12px;
                gap: 10px;
                border-radius: 14px;
            }
            .link-icon {
                width: 32px;
                height: 32px;
                font-size: 14px;
            }
            .link-title {
                font-size: 13px;
            }
        }
    </style>
</head>
<body>

    <div class="hub-card">

        <!-- ===== HEADER BRAND ===== -->
        <div class="brand-header">
            <div class="logo-wrapper">
                <div class="logo-icon">
                    <i class="fas fa-bolt"></i>
                </div>
                <span class="brand-name">OFFICIAL</span>
            </div>
            <div class="brand-sub">Social Hub • All Access</div>
            <div class="divider-glow"></div>
        </div>

        <!-- ===== SECTION: INSTAGRAM ===== -->
        <div class="section-label">
            <span class="line"></span>
            <i class="fab fa-instagram" style="color:#E4405F;"></i>
            INSTAGRAM
            <span class="line-right"></span>
        </div>

        <!-- IG 1 -->
        <a href="https://instagram.com/akun1" target="_blank" class="social-link" data-link="ig1">
            <div class="link-icon ig"><i class="fab fa-instagram"></i></div>
            <div class="link-info">
                <div class="link-title">Official Instagram 1</div>
                <div class="link-badge"><i class="fas fa-arrow-right"></i> Kunjungi</div>
            </div>
            <span class="link-stats" id="stats-ig1">0 klik</span>
        </a>

        <!-- IG 2 -->
        <a href="https://instagram.com/akun2" target="_blank" class="social-link" data-link="ig2">
            <div class="link-icon ig-alt"><i class="fab fa-instagram"></i></div>
            <div class="link-info">
                <div class="link-title">Official Instagram 2</div>
                <div class="link-badge"><i class="fas fa-arrow-right"></i> Kunjungi</div>
            </div>
            <span class="link-stats" id="stats-ig2">0 klik</span>
        </a>

        <!-- IG 3 - DISABLED (siap tambah nanti) -->
        <a href="#" class="social-link disabled" onclick="return false;">
            <div class="link-icon ig" style="opacity:0.5;"><i class="fab fa-instagram"></i></div>
            <div class="link-info">
                <div class="link-title">Official Instagram 3</div>
                <div class="link-badge"><span class="badge-coming">⏳ Segera</span></div>
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

        <!-- FB Group 1 -->
        <a href="https://facebook.com/groups/group1" target="_blank" class="social-link" data-link="fb1">
            <div class="link-icon fb"><i class="fab fa-facebook-f"></i></div>
            <div class="link-info">
                <div class="link-title">Official Group 1</div>
                <div class="link-badge"><i class="fas fa-users"></i> Komunitas</div>
            </div>
            <span class="link-stats" id="stats-fb1">0 klik</span>
        </a>

        <!-- FB Group 2 -->
        <a href="https://facebook.com/groups/group2" target="_blank" class="social-link" data-link="fb2">
            <div class="link-icon fb"><i class="fab fa-facebook-f"></i></div>
            <div class="link-info">
                <div class="link-title">Official Group 2</div>
                <div class="link-badge"><i class="fas fa-users"></i> Komunitas</div>
            </div>
            <span class="link-stats" id="stats-fb2">0 klik</span>
        </a>

        <!-- FB Group 3 -->
        <a href="https://facebook.com/groups/group3" target="_blank" class="social-link" data-link="fb3">
            <div class="link-icon fb"><i class="fab fa-facebook-f"></i></div>
            <div class="link-info">
                <div class="link-title">Official Group 3</div>
                <div class="link-badge"><i class="fas fa-users"></i> Komunitas</div>
            </div>
            <span class="link-stats" id="stats-fb3">0 klik</span>
        </a>

        <!-- ===== FOOTER ===== -->
        <div class="hub-footer">
            <span>✦</span> &nbsp; Semua akun resmi dalam satu tempat &nbsp; <span>✦</span>
        </div>

    </div>

    <!-- ===== TRACKING SCRIPT (Local Storage) ===== -->
    <script>
        (function() {
            'use strict';

            // === KONFIGURASI ===
            // Ganti KEY ini kalau mau reset statistik dari nol
            const STORAGE_KEY = 'osh_stats_2026';

            // === LOAD DATA ===
            let stats = {};
            try {
                const saved = localStorage.getItem(STORAGE_KEY);
                if (saved) {
                    stats = JSON.parse(saved);
                }
            } catch (e) {
                stats = {};
            }

            // Pastikan semua link yang aktif punya entry
            const activeLinks = document.querySelectorAll('.social-link:not(.disabled)');
            activeLinks.forEach(el => {
                const key = el.dataset.link;
                if (key && !stats[key]) {
                    stats[key] = 0;
                }
            });

            // === UPDATE TAMPILAN ===
            function updateDisplay() {
                activeLinks.forEach(el => {
                    const key = el.dataset.link;
                    if (key && stats[key] !== undefined) {
                        const counterEl = document.getElementById('stats-' + key);
                        if (counterEl) {
                            const count = stats[key];
                            counterEl.textContent = count + ' klik';
                            // Kalau lebih dari 0, kasih warna biar keliatan
                            if (count > 0) {
                                counterEl.style.color = 'rgba(255,255,255,0.6)';
                                counterEl.style.borderColor = 'rgba(255,255,255,0.1)';
                            }
                        }
                    }
                });
            }

            // === TRACKING KLIK ===
            activeLinks.forEach(el => {
                el.addEventListener('click', function(e) {
                    const key = this.dataset.link;
                    if (!key) return;

                    // Increment
                    if (!stats[key]) stats[key] = 0;
                    stats[key] += 1;

                    // Simpan ke Local Storage
                    try {
                        localStorage.setItem(STORAGE_KEY, JSON.stringify(stats));
                    } catch (e) {
                        // silent
                    }

                    // Update display (biar langsung berubah tanpa refresh)
                    const counterEl = document.getElementById('stats-' + key);
                    if (counterEl) {
                        counterEl.textContent = stats[key] + ' klik';
                        if (stats[key] > 0) {
                            counterEl.style.color = 'rgba(255,255,255,0.6)';
                            counterEl.style.borderColor = 'rgba(255,255,255,0.1)';
                        }
                    }

                    // Link tetap berfungsi normal (redirect ke sosmed)
                    // Karena pakai href asli, gak perlu e.preventDefault()
                });
            });

            // === FIRST LOAD ===
            updateDisplay();

            // === FITUR: RESET STATS (opsional) ===
            // Buka console di browser dan ketik: resetStats()
            window.resetStats = function() {
                if (confirm('Reset semua data klik?')) {
                    stats = {};
                    activeLinks.forEach(el => {
                        const key = el.dataset.link;
                        if (key) stats[key] = 0;
                    });
                    localStorage.setItem(STORAGE_KEY, JSON.stringify(stats));
                    updateDisplay();
                    // Reset warna
                    activeLinks.forEach(el => {
                        const key = el.dataset.link;
                        const counterEl = document.getElementById('stats-' + key);
                        if (counterEl) {
                            counterEl.style.color = 'rgba(255,255,255,0.2)';
                            counterEl.style.borderColor = 'rgba(255,255,255,0.04)';
                        }
                    });
                }
            };

            console.log('✅ Official Social Hub — Tracking siap!');
            console.log('📊 Ketik resetStats() di console untuk reset data.');
        })();
    </script>

</body>
</html>
