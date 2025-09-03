
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ZariAura - Men's Fashion</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Global Styles */
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --success: #27ae60;
            --warning: #f39c12;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f8f9fa;
            color: #333;
            line-height: 1.6;
            padding-bottom: 80px; /* Space for WhatsApp button */
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        /* Header Styles */
        header {
            background-color: var(--primary);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: var(--shadow);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: white;
            text-decoration: none;
        }

        .logo span {
            color: var(--secondary);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 1.5rem;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            transition: var(--transition);
            font-weight: 500;
        }

        nav ul li a:hover {
            color: var(--secondary);
        }

        .cart-icon {
            position: relative;
            cursor: pointer;
        }

        .cart-count {
            position: absolute;
            top: -10px;
            right: -10px;
            background-color: var(--accent);
            color: white;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
            font-weight: bold;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1483985988355-763728e1935b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 5rem 0;
            text-align: center;
            margin-bottom: 2rem;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
        }

        .btn {
            display: inline-block;
            padding: 0.8rem 1.5rem;
            background-color: var(--secondary);
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
        }

        .btn:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
        }

        .btn-accent {
            background-color: var(--accent);
        }

        .btn-accent:hover {
            background-color: #c0392b;
        }

        .btn-success {
            background-color: var(--success);
        }

        .btn-success:hover {
            background-color: #219653;
        }

        /* Products Grid */
        .section-title {
            text-align: center;
            margin: 3rem 0 2rem;
            color: var(--dark);
            position: relative;
        }

        .section-title:after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background-color: var(--secondary);
            margin: 0.5rem auto;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .product-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
        }

        .product-image {
            height: 200px;
            width: 100%;
            object-fit: cover;
        }

        .product-info {
            padding: 1.5rem;
        }

        .product-name {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            color: var(--dark);
        }

        .product-price {
            font-size: 1.3rem;
            font-weight: bold;
            color: var(--accent);
            margin-bottom: 1rem;
        }

        .product-sizes {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }

        .size-pill {
            padding: 0.3rem 0.6rem;
            background-color: var(--light);
            border-radius: 4px;
            font-size: 0.8rem;
            font-weight: 500;
        }

        .size-pill.out-of-stock {
            background-color: #f5f5f5;
            color: #bbb;
            text-decoration: line-through;
        }

        .product-actions {
            display: flex;
            gap: 0.5rem;
        }

        /* Admin Panel */
        .admin-panel {
            display: none;
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: var(--shadow);
            margin: 2rem 0;
        }

        .admin-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid #eee;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }

        .form-control {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
        }

        textarea.form-control {
            min-height: 100px;
            resize: vertical;
        }

        .size-inputs {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-bottom: 1rem;
        }

        .size-input {
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .image-preview {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 1rem;
        }

        .preview-image {
            width: 100px;
            height: 100px;
            object-fit: cover;
            border-radius: 4px;
            border: 1px solid #ddd;
        }

        /* Cart Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 1000;
            align-items: center;
            justify-content: center;
        }

        .modal-content {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            width: 90%;
            max-width: 600px;
            max-height: 80vh;
            overflow-y: auto;
        }

        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid #eee;
        }

        .close-modal {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: #777;
        }

        .cart-items {
            margin-bottom: 1.5rem;
        }

        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
            border-bottom: 1px solid #eee;
        }

        .cart-item-info {
            flex: 1;
        }

        .cart-item-name {
            font-weight: 500;
            margin-bottom: 0.3rem;
        }

        .cart-item-details {
            font-size: 0.9rem;
            color: #777;
        }

        .cart-item-price {
            font-weight: bold;
            color: var(--accent);
        }

        .cart-item-actions {
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .quantity-btn {
            width: 30px;
            height: 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: var(--light);
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        .cart-total {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
            font-size: 1.2rem;
            font-weight: bold;
            border-top: 2px solid #eee;
        }

        /* Checkout Form */
        .checkout-form {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
        }

        .checkout-form .form-group.full-width {
            grid-column: 1 / -1;
        }

        .payment-options {
            display: flex;
            gap: 1rem;
            margin-bottom: 1rem;
        }

        .payment-option {
            flex: 1;
            text-align: center;
            padding: 1rem;
            border: 2px solid #ddd;
            border-radius: 8px;
            cursor: pointer;
            transition: var(--transition);
        }

        .payment-option.selected {
            border-color: var(--secondary);
            background-color: rgba(52, 152, 219, 0.1);
        }

        /* Toast Notifications */
        .toast-container {
            position: fixed;
            top: 20px;
            right: 20px;
            z-index: 1100;
        }

        .toast {
            padding: 1rem 1.5rem;
            margin-bottom: 1rem;
            border-radius: 4px;
            color: white;
            display: flex;
            align-items: center;
            justify-content: space-between;
            min-width: 300px;
            box-shadow: var(--shadow);
            animation: slideIn 0.3s ease;
        }

        .toast.success {
            background-color: var(--success);
        }

        .toast.error {
            background-color: var(--accent);
        }

        .close-toast {
            background: none;
            border: none;
            color: white;
            cursor: pointer;
            font-size: 1.2rem;
        }

        @keyframes slideIn {
            from {
                transform: translateX(100%);
                opacity: 0;
            }
            to {
                transform: translateX(0);
                opacity: 1;
            }
        }

        /* WhatsApp Help Button */
        .whatsapp-help {
            position: fixed;
            bottom: 20px;
            right: 20px;
            width: 60px;
            height: 60px;
            background-color: #25D366;
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            box-shadow: var(--shadow);
            z-index: 100;
            cursor: pointer;
            transition: var(--transition);
        }

        .whatsapp-help:hover {
            transform: scale(1.1);
        }

        /* Admin Login */
        .admin-login {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: var(--shadow);
            max-width: 400px;
            margin: 5rem auto;
        }

        .admin-login h2 {
            text-align: center;
            margin-bottom: 1.5rem;
            color: var(--dark);
        }

        /* Responsive Styles */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 1rem;
            }

            nav ul {
                gap: 1rem;
            }

            nav ul li {
                margin-left: 0;
            }

            .hero h1 {
                font-size: 2.2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .checkout-form {
                grid-template-columns: 1fr;
            }

            .payment-options {
                flex-direction: column;
            }
        }

        /* Empty State */
        .empty-state {
            text-align: center;
            padding: 3rem;
            color: #777;
        }

        .empty-state i {
            font-size: 3rem;
            margin-bottom: 1rem;
            color: #ddd;
        }

        /* Tabs for Admin */
        .admin-tabs {
            display: flex;
            border-bottom: 1px solid #ddd;
            margin-bottom: 1.5rem;
        }

        .admin-tab {
            padding: 0.8rem 1.5rem;
            cursor: pointer;
            border-bottom: 3px solid transparent;
        }

        .admin-tab.active {
            border-bottom: 3px solid var(--secondary);
            font-weight: bold;
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
        }

        /* Payment Confirmation */
        .payment-confirmation {
            background-color: #f8f9fa;
            padding: 1.5rem;
            border-radius: 8px;
            margin-top: 1rem;
            text-align: center;
        }

        .payment-status {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }

        .payment-status i {
            font-size: 2rem;
        }

        .payment-status.success i {
            color: var(--success);
        }

        .payment-status.pending i {
            color: var(--warning);
        }
    </style>
</head>
<body>
    <!-- WhatsApp Help Button -->
    <div class="whatsapp-help" onclick="openWhatsAppHelp()">
        <i class="fab fa-whatsapp"></i>
    </div>

    <!-- Header -->
    <header>
        <div class="container header-content">
            <a href="#" class="logo">Zari<span>Aura</span></a>
            <nav>
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#products">Products</a></li>
                    <li><a href="#" onclick="openAdminLogin()">Admin</a></li>
                    <li class="cart-icon" onclick="openCart()">
                        <i class="fas fa-shopping-cart"></i>
                        <span class="cart-count" id="cartCount">0</span>
                    </li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>Elevate Your Style</h1>
            <p>Discover premium men's fashion that combines quality, comfort, and sophistication for the modern gentleman.</p>
            <a href="#products" class="btn">Shop Now</a>
        </div>
    </section>

    <!-- Products Section -->
    <section id="products">
        <div class="container">
            <h2 class="section-title">Our Collection</h2>
            <div class="products-grid" id="productsGrid">
                <!-- Products will be dynamically added here -->
                <div class="empty-state" id="emptyProducts">
                    <i class="fas fa-tshirt"></i>
                    <h3>No products available</h3>
                    <p>Admin can add products using the Admin panel</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Admin Login Modal -->
    <div class="modal" id="adminLoginModal">
        <div class="modal-content">
            <div class="modal-header">
                <h2>Admin Login</h2>
                <button class="close-modal" onclick="closeModal('adminLoginModal')">&times;</button>
            </div>
            <div class="admin-login">
                <div class="form-group">
                    <label for="adminPassword">Password</label>
                    <input type="password" id="adminPassword" class="form-control" placeholder="Enter admin password">
                </div>
                <button class="btn" onclick="loginAdmin()">Login</button>
            </div>
        </div>
    </div>

    <!-- Admin Panel -->
    <div class="container">
        <div class="admin-panel" id="adminPanel">
            <div class="admin-header">
                <h2>Admin Panel</h2>
                <button class="btn btn-accent" onclick="logoutAdmin()">Logout</button>
            </div>

            <div class="admin-tabs">
                <div class="admin-tab active" onclick="switchTab('addProductTab')">Add Product</div>
                <div class="admin-tab" onclick="switchTab('manageProductsTab')">Manage Products</div>
            </div>

            <div id="addProductTab" class="tab-content active">
                <h3>Add New Product</h3>
                <form id="productForm">
                    <div class="form-group">
                        <label for="productName">Product Name *</label>
                        <input type="text" id="productName" class="form-control" required>
                    </div>

                    <div class="form-group">
                        <label for="productDescription">Description *</label>
                        <textarea id="productDescription" class="form-control" required></textarea>
                    </div>

                    <div class="form-group">
                        <label for="productPrice">Price (INR) *</label>
                        <input type="number" id="productPrice" class="form-control" min="1" required>
                    </div>

                    <div class="form-group">
                        <label for="productSizes">Sizes (comma separated, e.g., S,M,L,XL) *</label>
                        <input type="text" id="productSizes" class="form-control" required>
                    </div>

                    <div class="form-group">
                        <label for="productImages">Product Images (1-6 images) *</label>
                        <input type="file" id="productImages" class="form-control" multiple accept="image/*" required>
                        <div class="image-preview" id="imagePreview"></div>
                    </div>

                    <button type="button" class="btn" onclick="addProduct()">Add Product</button>
                </form>
            </div>

            <div id="manageProductsTab" class="tab-content">
                <h3>Manage Products</h3>
                <div id="adminProductsList">
                    <!-- Admin product list will be added here -->
                </div>
            </div>
        </div>
    </div>

    <!-- Cart Modal -->
    <div class="modal" id="cartModal">
        <div class="modal-content">
            <div class="modal-header">
                <h2>Your Cart</h2>
                <button class="close-modal" onclick="closeModal('cartModal')">&times;</button>
            </div>

            <div class="cart-items" id="cartItems">
                <!-- Cart items will be added here -->
                <div class="empty-state">
                    <i class="fas fa-shopping-cart"></i>
                    <h3>Your cart is empty</h3>
                    <p>Add some products to your cart</p>
                </div>
            </div>

            <div class="cart-total">
                <span>Total:</span>
                <span id="cartTotal">₹0</span>
            </div>

            <button class="btn btn-accent" style="width: 100%;" onclick="openCheckout()">Proceed to Checkout</button>
        </div>
    </div>

    <!-- Checkout Modal -->
    <div class="modal" id="checkoutModal">
        <div class="modal-content">
            <div class="modal-header">
                <h2>Checkout</h2>
                <button class="close-modal" onclick="closeModal('checkoutModal')">&times;</button>
            </div>

            <form id="checkoutForm">
                <div class="checkout-form">
                    <div class="form-group full-width">
                        <h3>Customer Information</h3>
                    </div>

                    <div class="form-group">
                        <label for="customerName">Full Name *</label>
                        <input type="text" id="customerName" class="form-control" required>
                    </div>

                    <div class="form-group">
                        <label for="customerPhone">Phone *</label>
                        <input type="tel" id="customerPhone" class="form-control" pattern="[0-9]{10}" required>
                    </div>

                    <div class="form-group full-width">
                        <label for="customerAddress">Full Address *</label>
                        <textarea id="customerAddress" class="form-control" required></textarea>
                    </div>

                    <div class="form-group">
                        <label for="customerCity">City *</label>
                        <input type="text" id="customerCity" class="form-control" required>
                    </div>

                    <div class="form-group">
                        <label for="customerState">State *</label>
                        <input type="text" id="customerState" class="form-control" required>
                    </div>

                    <div class="form-group">
                        <label for="customerPincode">Pincode *</label>
                        <input type="text" id="customerPincode" class="form-control" pattern="[0-9]{6}" required>
                    </div>

                    <div class="form-group full-width">
                        <h3>Payment Method</h3>
                        <div class="payment-options">
                            <div class="payment-option selected" onclick="selectPayment('cod')">
                                <i class="fas fa-money-bill-wave"></i>
                                <p>Cash on Delivery</p>
                            </div>
                            <div class="payment-option" onclick="selectPayment('upi')">
                                <i class="fas fa-mobile-alt"></i>
                                <p>UPI Payment</p>
                            </div>
                        </div>
                        <input type="hidden" id="paymentMethod" value="cod" required>
                    </div>

                    <div class="form-group full-width" id="upiInstructions" style="display: none;">
                        <div style="background-color: #f8f9fa; padding: 1rem; border-radius: 4px;">
                            <p><strong>UPI ID: 7428443169@fam</strong></p>
                            <p>Please make the payment to this UPI ID and confirm after completing the payment.</p>
                            <button type="button" class="btn" onclick="openUPIApp()">Open UPI App</button>
                            <button type="button" class="btn" onclick="copyUPIID()">Copy UPI ID</button>
                        </div>
                    </div>

                    <div class="form-group full-width" id="paymentConfirmation" style="display: none;">
                        <div class="payment-confirmation">
                            <div class="payment-status pending">
                                <i class="fas fa-clock"></i>
                                <span>Payment Pending</span>
                            </div>
                            <p>Please complete the payment and then confirm below.</p>
                            <button type="button" class="btn btn-success" onclick="confirmPayment()">I Have Made the Payment</button>
                        </div>
                    </div>
                </div>

                <button type="button" class="btn btn-accent" style="width: 100%; margin-top: 1rem;" onclick="processOrder()" id="placeOrderBtn">Place Order</button>
            </form>
        </div>
    </div>

    <!-- Order Success Modal -->
    <div class="modal" id="orderSuccessModal">
        <div class="modal-content">
            <div class="modal-header">
                <h2>Order Successful!</h2>
                <button class="close-modal" onclick="closeModal('orderSuccessModal')">&times;</button>
            </div>
            <div style="text-align: center; padding: 2rem;">
                <div style="font-size: 4rem; color: var(--success); margin-bottom: 1rem;">
                    <i class="fas fa-check-circle"></i>
                </div>
                <h3>Thank You for Your Order</h3>
                <p>Your order has been successfully placed and sent to the seller via WhatsApp.</p>
                <p>The seller will contact you shortly to confirm your order.</p>
                <button class="btn" onclick="closeModal('orderSuccessModal')">Continue Shopping</button>
            </div>
        </div>
    </div>

    <!-- Toast Container -->
    <div class="toast-container" id="toastContainer"></div>

    <script>
        // README: 
        // This is a client-side e-commerce prototype for a men's fashion store.
        // 
        // STORAGE & PERSISTENCE:
        // - All data (products, cart) is stored in the browser's localStorage
        // - Product images are stored as Base64 strings (not efficient for production)
        // - Data persists across page reloads but is limited to the current browser/device
        //
        // LIMITATIONS:
        // - Client-side storage has size limitations (usually 5-10MB)
        // - Base64 images consume about 33% more space than binary images
        // - Data is not synced across devices or browsers
        //
        // PRODUCTION RECOMMENDATIONS:
        // - Use a backend server with a proper database (MySQL, MongoDB, etc.)
        // - Store images in cloud storage (AWS S3, Cloudinary, etc.)
        // - Implement server-side authentication (not client-side password check)
        // - Use a payment gateway with webhooks for payment verification
        //
        // UPI & WHATSAPP FLOWS:
        // - UPI payments require manual confirmation from the user
        // - Orders are sent to WhatsApp as messages (no order storage in admin)
        // - Admin receives orders via WhatsApp, not through the admin panel

        // Global variables
        let cart = [];
        let products = [];
        const ADMIN_PASSWORD = 'Rahul@7428';
        const UPI_ID = '7428443169@fam';
        const WHATSAPP_NUMBER = '917428443169';
        let paymentConfirmed = false;
        let currentOrderData = null;

        // Initialize the application
        document.addEventListener('DOMContentLoaded', function() {
            loadProducts();
            loadCart();
            updateCartUI();
            
            // Add event listener for image preview
            document.getElementById('productImages').addEventListener('change', handleImagePreview);
        });

        // Product management functions
        function loadProducts() {
            const storedProducts = localStorage.getItem('products');
            if (storedProducts) {
                products = JSON.parse(storedProducts);
                renderProducts();
                renderAdminProducts();
            }
        }

        function saveProducts() {
            localStorage.setItem('products', JSON.stringify(products));
        }

        function renderProducts() {
            const productsGrid = document.getElementById('productsGrid');
            const emptyProducts = document.getElementById('emptyProducts');
            
            if (products.length === 0) {
                emptyProducts.style.display = 'block';
                productsGrid.innerHTML = '';
                productsGrid.appendChild(emptyProducts);
                return;
            }
            
            emptyProducts.style.display = 'none';
            productsGrid.innerHTML = '';
            
            products.forEach((product, index) => {
                const productCard = document.createElement('div');
                productCard.className = 'product-card';
                
                // Use the first image as the thumbnail
                const thumbnail = product.images[0];
                
                productCard.innerHTML = `
                    <img src="${thumbnail}" alt="${product.name}" class="product-image">
                    <div class="product-info">
                        <h3 class="product-name">${product.name}</h3>
                        <p class="product-price">₹${product.price}</p>
                        <div class="product-sizes">
                            ${product.sizes.map(size => 
                                `<span class="size-pill">${size}</span>`
                            ).join('')}
                        </div>
                        <div class="product-actions">
                            <button class="btn" onclick="addToCart(${index})">Add to Cart</button>
                            <button class="btn btn-accent" onclick="buyNow(${index})">Buy Now</button>
                        </div>
                    </div>
                `;
                
                productsGrid.appendChild(productCard);
            });
        }

        function renderAdminProducts() {
            const adminProductsList = document.getElementById('adminProductsList');
            adminProductsList.innerHTML = '';
            
            if (products.length === 0) {
                adminProductsList.innerHTML = '<p>No products added yet.</p>';
                return;
            }
            
            products.forEach((product, index) => {
                const productItem = document.createElement('div');
                productItem.className = 'product-item';
                productItem.style.cssText = 'border: 1px solid #ddd; padding: 1rem; margin-bottom: 1rem; border-radius: 4px;';
                
                productItem.innerHTML = `
                    <div style="display: flex; justify-content: space-between; align-items: center;">
                        <div>
                            <h4>${product.name}</h4>
                            <p>₹${product.price} | Sizes: ${product.sizes.join(', ')}</p>
                        </div>
                        <div>
                            <button class="btn btn-accent" onclick="deleteProduct(${index})">Delete</button>
                        </div>
                    </div>
                `;
                
                adminProductsList.appendChild(productItem);
            });
        }

        function addProduct() {
            const name = document.getElementById('productName').value;
            const description = document.getElementById('productDescription').value;
            const price = document.getElementById('productPrice').value;
            const sizesInput = document.getElementById('productSizes').value;
            const imagesInput = document.getElementById('productImages');
            
            // Validate inputs
            if (!name || !description || !price || !sizesInput || imagesInput.files.length === 0) {
                showToast('Please fill all required fields', 'error');
                return;
            }
            
            if (imagesInput.files.length > 6) {
                showToast('Maximum 6 images allowed', 'error');
                return;
            }
            
            // Process sizes
            const sizes = sizesInput.split(',').map(size => size.trim()).filter(size => size);
            
            // Process images
            const imagePromises = [];
            for (let i = 0; i < imagesInput.files.length; i++) {
                imagePromises.push(readFileAsDataURL(imagesInput.files[i]));
            }
            
            Promise.all(imagePromises)
                .then(images => {
                    // Create product object
                    const product = {
                        id: Date.now(), // Unique ID
                        name,
                        description,
                        price: parseInt(price),
                        sizes,
                        images
                    };
                    
                    // Add to products array
                    products.push(product);
                    
                    // Save and update UI
                    saveProducts();
                    renderProducts();
                    renderAdminProducts();
                    
                    // Reset form
                    document.getElementById('productForm').reset();
                    document.getElementById('imagePreview').innerHTML = '';
                    
                    showToast('Product added successfully', 'success');
                })
                .catch(error => {
                    console.error('Error reading images:', error);
                    showToast('Error processing images', 'error');
                });
        }

        function readFileAsDataURL(file) {
            return new Promise((resolve, reject) => {
                const reader = new FileReader();
                reader.onload = () => resolve(reader.result);
                reader.onerror = reject;
                reader.readAsDataURL(file);
            });
        }

        function deleteProduct(index) {
            if (confirm('Are you sure you want to delete this product?')) {
                products.splice(index, 1);
                saveProducts();
                renderProducts();
                renderAdminProducts();
                showToast('Product deleted successfully', 'success');
            }
        }

        function handleImagePreview() {
            const input = document.getElementById('productImages');
            const preview = document.getElementById('imagePreview');
            preview.innerHTML = '';
            
            if (input.files) {
                Array.from(input.files).forEach(file => {
                    const reader = new FileReader();
                    reader.onload = function(e) {
                        const img = document.createElement('img');
                        img.src = e.target.result;
                        img.className = 'preview-image';
                        preview.appendChild(img);
                    };
                    reader.readAsDataURL(file);
                });
            }
        }

        // Cart management functions
        function loadCart() {
            const storedCart = localStorage.getItem('cart');
            if (storedCart) {
                cart = JSON.parse(storedCart);
            }
        }

        function saveCart() {
            localStorage.setItem('cart', JSON.stringify(cart));
        }

        function updateCartUI() {
            const cartCount = document.getElementById('cartCount');
            cartCount.textContent = cart.reduce((total, item) => total + item.quantity, 0);
        }

        function addToCart(productIndex) {
            const product = products[productIndex];
            const existingItem = cart.find(item => item.productId === product.id);
            
            if (existingItem) {
                existingItem.quantity += 1;
            } else {
                cart.push({
                    productId: product.id,
                    name: product.name,
                    price: product.price,
                    size: product.sizes[0], // Default to first size
                    quantity: 1,
                    image: product.images[0]
                });
            }
            
            saveCart();
            updateCartUI();
            showToast('Product added to cart', 'success');
        }

        function buyNow(productIndex) {
            addToCart(productIndex);
            openCart();
        }

        function openCart() {
            const cartModal = document.getElementById('cartModal');
            const cartItems = document.getElementById('cartItems');
            
            if (cart.length === 0) {
                cartItems.innerHTML = `
                    <div class="empty-state">
                        <i class="fas fa-shopping-cart"></i>
                        <h3>Your cart is empty</h3>
                        <p>Add some products to your cart</p>
                    </div>
                `;
                document.getElementById('cartTotal').textContent = '₹0';
            } else {
                cartItems.innerHTML = '';
                let total = 0;
                
                cart.forEach((item, index) => {
                    const itemTotal = item.price * item.quantity;
                    total += itemTotal;
                    
                    const cartItem = document.createElement('div');
                    cartItem.className = 'cart-item';
                    cartItem.innerHTML = `
                        <div class="cart-item-info">
                            <h4 class="cart-item-name">${item.name}</h4>
                            <p class="cart-item-details">Size: ${item.size} | ₹${item.price} x ${item.quantity}</p>
                        </div>
                        <div class="cart-item-price">₹${itemTotal}</div>
                        <div class="cart-item-actions">
                            <button class="quantity-btn" onclick="updateCartItemQuantity(${index}, ${item.quantity - 1})">-</button>
                            <span>${item.quantity}</span>
                            <button class="quantity-btn" onclick="updateCartItemQuantity(${index}, ${item.quantity + 1})">+</button>
                            <button class="btn btn-accent" style="margin-left: 10px;" onclick="removeCartItem(${index})">Remove</button>
                        </div>
                    `;
                    
                    cartItems.appendChild(cartItem);
                });
                
                document.getElementById('cartTotal').textContent = `₹${total}`;
            }
            
            cartModal.style.display = 'flex';
        }

        function updateCartItemQuantity(index, newQuantity) {
            if (newQuantity < 1) {
                removeCartItem(index);
                return;
            }
            
            cart[index].quantity = newQuantity;
            saveCart();
            updateCartUI();
            openCart(); // Refresh cart view
        }

        function removeCartItem(index) {
            cart.splice(index, 1);
            saveCart();
            updateCartUI();
            openCart(); // Refresh cart view
            showToast('Item removed from cart', 'success');
        }

        function openCheckout() {
            if (cart.length === 0) {
                showToast('Your cart is empty', 'error');
                return;
            }
            
            closeModal('cartModal');
            document.getElementById('checkoutForm').reset();
            document.getElementById('paymentMethod').value = 'cod';
            document.getElementById('upiInstructions').style.display = 'none';
            document.getElementById('paymentConfirmation').style.display = 'none';
            document.getElementById('placeOrderBtn').style.display = 'block';
            
            // Reset payment option UI
            document.querySelectorAll('.payment-option').forEach(option => {
                option.classList.remove('selected');
            });
            document.querySelector('.payment-option:first-child').classList.add('selected');
            
            // Reset payment status
            paymentConfirmed = false;
            
            const checkoutModal = document.getElementById('checkoutModal');
            checkoutModal.style.display = 'flex';
        }

        function selectPayment(method) {
            document.getElementById('paymentMethod').value = method;
            document.getElementById('upiInstructions').style.display = method === 'upi' ? 'block' : 'none';
            document.getElementById('paymentConfirmation').style.display = method === 'upi' ? 'block' : 'none';
            
            if (method === 'upi') {
                document.getElementById('placeOrderBtn').style.display = 'none';
                paymentConfirmed = false;
            } else {
                document.getElementById('placeOrderBtn').style.display = 'block';
            }
            
            // Update UI
            document.querySelectorAll('.payment-option').forEach(option => {
                option.classList.remove('selected');
            });
            event.currentTarget.classList.add('selected');
        }

        function openUPIApp() {
            const total = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
            const orderId = 'ORD' + Date.now();
            const upiLink = `upi://pay?pa=${UPI_ID}&pn=ZariAura&am=${total}&cu=INR&tn=Order%20${orderId}`;
            
            window.open(upiLink, '_blank');
        }

        function copyUPIID() {
            navigator.clipboard.writeText(UPI_ID)
                .then(() => {
                    showToast('UPI ID copied to clipboard', 'success');
                })
                .catch(err => {
                    showToast('Failed to copy UPI ID', 'error');
                });
        }

        function confirmPayment() {
            paymentConfirmed = true;
            document.getElementById('placeOrderBtn').style.display = 'block';
            document.querySelector('.payment-status').innerHTML = '<i class="fas fa-check-circle" style="color: var(--success);"></i><span>Payment Confirmed</span>';
            showToast('Payment confirmed. You can now place your order.', 'success');
        }

        function processOrder() {
            const paymentMethod = document.getElementById('paymentMethod').value;
            
            // For UPI payments, check if payment is confirmed
            if (paymentMethod === 'upi' && !paymentConfirmed) {
                showToast('Please confirm your payment first', 'error');
                return;
            }
            
            // Validate form
            const form = document.getElementById('checkoutForm');
            if (!form.checkValidity()) {
                form.reportValidity();
                return;
            }
            
            // Collect customer info
            const customer = {
                name: document.getElementById('customerName').value,
                phone: document.getElementById('customerPhone').value,
                address: document.getElementById('customerAddress').value,
                city: document.getElementById('customerCity').value,
                state: document.getElementById('customerState').value,
                pincode: document.getElementById('customerPincode').value
            };
            
            const total = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
            const orderId = 'ORD' + Date.now();
            
            // Store order data for WhatsApp message
            currentOrderData = {
                customer,
                paymentMethod,
                total,
                orderId,
                cart: [...cart]
            };
            
            // Generate WhatsApp message
            let message = `New Order Received:%0A`;
            message += `Name: ${customer.name}%0A`;
            message += `Phone: ${customer.phone}%0A`;
            message += `Address: ${customer.address}, ${customer.city}, ${customer.state} - ${customer.pincode}%0A`;
            message += `%0AOrder Details:%0A`;
            
            cart.forEach(item => {
                message += `- ${item.name} (Size: ${item.size}, Qty: ${item.quantity}) - ₹${item.price * item.quantity}%0A`;
            });
            
            message += `%0ATotal: ₹${total}%0A`;
            message += `Payment: ${paymentMethod.toUpperCase()}%0A`;
            message += `Order ID: ${orderId}`;
            
            if (paymentMethod === 'upi') {
                message += '%0A%0AUPI Payment: Confirmed by customer';
            }
            
            // Open WhatsApp
            const whatsappURL = `https://wa.me/${WHATSAPP_NUMBER}?text=${message}`;
            window.open(whatsappURL, '_blank');
            
            // Show success modal
            closeModal('checkoutModal');
            document.getElementById('orderSuccessModal').style.display = 'flex';
            
            // Clear cart
            cart = [];
            saveCart();
            updateCartUI();
            
            // Reset payment status
            paymentConfirmed = false;
        }

        // Admin functions
        function openAdminLogin() {
            document.getElementById('adminLoginModal').style.display = 'flex';
        }

        function loginAdmin() {
            const password = document.getElementById('adminPassword').value;
            
            if (password === ADMIN_PASSWORD) {
                document.getElementById('adminPanel').style.display = 'block';
                closeModal('adminLoginModal');
                showToast('Admin login successful', 'success');
            } else {
                showToast('Incorrect password', 'error');
            }
        }

        function logoutAdmin() {
            document.getElementById('adminPanel').style.display = 'none';
            showToast('Admin logged out', 'success');
        }

        function switchTab(tabId) {
            // Hide all tabs
            document.querySelectorAll('.tab-content').forEach(tab => {
                tab.classList.remove('active');
            });
            
            // Deactivate all tab buttons
            document.querySelectorAll('.admin-tab').forEach(tab => {
                tab.classList.remove('active');
            });
            
            // Activate selected tab
            document.getElementById(tabId).classList.add('active');
            event.currentTarget.classList.add('active');
        }

        // UI helper functions
        function closeModal(modalId) {
            document.getElementById(modalId).style.display = 'none';
        }

        function showToast(message, type) {
            const toastContainer = document.getElementById('toastContainer');
            const toast = document.createElement('div');
            toast.className = `toast ${type}`;
            toast.innerHTML = `
                <span>${message}</span>
                <button class="close-toast" onclick="this.parentElement.remove()">&times;</button>
            `;
            
            toastContainer.appendChild(toast);
            
            // Auto remove after 5 seconds
            setTimeout(() => {
                if (toast.parentElement) {
                    toast.remove();
                }
            }, 5000);
        }

        function openWhatsAppHelp() {
            const message = 'Hi%20I%20need%20help%20with%20my%20order.';
            window.open(`https://wa.me/${WHATSAPP_NUMBER}?text=${message}`, '_blank');
        }
    </script>
</body>
</html>
