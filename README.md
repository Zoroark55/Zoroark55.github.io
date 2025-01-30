<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GameAccount Bazaar</title>
    <style>
        /* Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', sans-serif;
        }

        body {
            background: #0f0f1a;
            color: white;
        }

        /* Header */
        .header {
            background: linear-gradient(45deg, #2a2a4a, #1a1a2f);
            padding: 1rem;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: #6c5ce7;
        }

        /* Game Sections */
        .game-section {
            padding: 4rem 2rem;
            margin-top: 60px;
        }

        .game-card {
            background: #1e1e2f;
            border-radius: 10px;
            padding: 1rem;
            margin: 1rem 0;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1rem;
        }

        .account-card {
            background: #2a2a4a;
            border-radius: 8px;
            padding: 1rem;
            margin: 0.5rem;
            transition: transform 0.3s;
        }

        .account-card:hover {
            transform: translateY(-5px);
        }

        /* Image Gallery */
        .image-gallery {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 0.5rem;
            margin: 1rem 0;
        }

        .gallery-img {
            width: 100%;
            height: 100px;
            object-fit: cover;
            border-radius: 4px;
        }

        /* Z-Points System */
        .wallet {
            position: fixed;
            top: 70px;
            right: 20px;
            background: #6c5ce7;
            padding: 0.5rem 1rem;
            border-radius: 20px;
            display: flex;
            align-items: center;
        }

        /* Login/Sell Modal */
        .modal {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: #1e1e2f;
            padding: 2rem;
            border-radius: 10px;
            width: 90%;
            max-width: 400px;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .game-card {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <nav class="nav">
            <div class="logo">GameAccount Bazaar</div>
            <div class="wallet">
                <span>Z-Points: 0</span>
            </div>
        </nav>
    </header>

    <!-- Game Sections -->
    <section class="game-section" id="pubg">
        <h2>PUBG Accounts</h2>
        <div class="game-card">
            <!-- Sample Account Card -->
            <div class="account-card">
                <h3>Conqueror Account</h3>
                <div class="image-gallery">
                    <img src="placeholder.jpg" class="gallery-img" alt="Account Preview">
                    <img src="placeholder.jpg" class="gallery-img" alt="Account Preview">
                    <img src="placeholder.jpg" class="gallery-img" alt="Account Preview">
                </div>
                <p>Price: 5000 Z-Points</p>
                <button class="buy-btn">Buy Now</button>
            </div>
            <!-- More account cards -->
        </div>
    </section>

    <!-- Repeat similar sections for MLBB, Clash of Clans, Free Fire -->

    <!-- Login/Signup Modal -->
    <div class="modal" id="loginModal">
        <h2>Login with Google</h2>
        <button id="googleLogin">Continue with Google</button>
    </div>

    <!-- Sell Account Form -->
    <div class="modal" id="sellModal">
        <h2>Sell Your Account</h2>
        <form id="sellForm">
            <input type="email" placeholder="Account Email" required>
            <input type="password" placeholder="Account Password" required>
            <input type="number" placeholder="Price in Z-Points" required>
            <div class="image-upload">
                <input type="file" accept="image/*" multiple>
            </div>
            <button type="submit">List Account</button>
        </form>
    </div>

    <script>
        // Basic Frontend Interactions
        document.querySelectorAll('.buy-btn').forEach(btn => {
            btn.addEventListener('click', () => {
                document.getElementById('loginModal').style.display = 'block';
            });
        });

        // Google Auth (Requires Firebase Integration)
        document.getElementById('googleLogin').addEventListener('click', () => {
            // Implement Firebase Google Auth
        });
    </script>
</body>
</html>
