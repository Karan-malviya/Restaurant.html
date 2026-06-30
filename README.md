# Restaurant.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Restaurant Food Feedback</title>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif; }
        
        body {
            background-color: #f4f7f6;
            display: flex;
            justify-content: center;
            padding: 40px 20px;
            color: #333;
        }

        .feedback-form {
            background: #ffffff;
            max-width: 600px;
            width: 100%;
            padding: 35px;
            border-radius: 12px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
        }

        .form-header {
            margin-bottom: 25px;
            text-align: center;
        }

        .form-header h2 { font-size: 1.6rem; color: #1a1a1a; margin-bottom: 6px; }
        .form-header p { color: #666; font-size: 0.95rem; }

        fieldset {
            border: none;
            margin-bottom: 25px;
        }
  
        legend {
            font-weight: 700;
            color: #2c3e50;
            font-size: 1.1rem;
            border-bottom: 2px solid #e67e22;
            padding-bottom: 6px;
            margin-bottom: 16px;
            width: 100%;
        }

        .form-group { margin-bottom: 18px; }

        label.field-label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            font-size: 0.9rem;
        }

        input[type="text"],
        input[type="email"],
        select,
        textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #d1d5db;
            border-radius: 6px;
            font-size: 0.95rem;
            transition: border-color 0.2s;
        }

        input:focus, select:focus, textarea:focus {
            outline: none;
            border-color: #e67e22;
        }

        textarea { resize: vertical; min-height: 90px; }

        .radio-grid {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .radio-option {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
            cursor: pointer;
            background: #f9fafb;
            padding: 8px 14px;
            border-radius: 6px;
            border: 1px solid #e5e7eb;
        }

        .radio-option:hover { background: #f3f4f6; }

        .submit-btn {
            width: 100%;
            background-color: #e67e22;
            color: white;
            border: none;
            padding: 14px;
            font-size: 1rem;
            font-weight: bold;
            border-radius: 6px;
            cursor: pointer;
            transition: background 0.2s;
        }

        .submit-btn:hover { background-color: #d35400; }
    </style>
</head>
<body>

<form class="feedback-form" action="#" method="POST">
    
    <div class="form-header">
        <h2>🍽️. Food Feedback</h2>
        <p>Help us improve our kitchen by sharing your experience.</p>
    </div>

    <!-- Section 1: Visit Context -->
    <fieldset>
        <legend>1. Order Details</legend>
        
        <div class="form-group">
            <label class="field-label" for="order-type">Dining Option</label>
            <select id="order-type" name="order_type" required>
                <option value="dine-in">Dine-In</option>
                <option value="takeout">Takeout / Pickup</option>
                <option value="delivery">Delivery</option>
            </select>
        </div>

        <div class="form-group">
            <label class="field-label" for="dish-ordered">What was your main dish?</label>
            <input type="text" id="dish-ordered" name="dish_ordered" placeholder="e.g. Truffle Garlic Pasta">
        </div>
    </fieldset>

    <!-- Section 2: The Food -->
    <fieldset>
        <legend>2. Food Quality</legend>
        
        <div class="form-group">
            <label class="field-label">Overall Taste & Quality *</label>
            <div class="radio-grid">
                <label class="radio-option"><input type="radio" name="quality" value="5" required> Excellent</label>
                <label class="radio-option"><input type="radio" name="quality" value="4"> Good</label>
                <label class="radio-option"><input type="radio" name="quality" value="3"> Average</label>
                <label class="radio-option"><input type="radio" name="quality" value="2"> Poor</label>
            </div>
        </div>

        <div class="form-group">
            <label class="field-label">Food Temperature *</label>
            <div class="radio-grid">
                <label class="radio-option"><input type="radio" name="temp" value="hot" required> Served Hot/Fresh</label>
                <label class="radio-option"><input type="radio" name="temp" value="warm"> Acceptable</label>
                <label class="radio-option"><input type="radio" name="temp" value="cold"> Too Cold</label>
            </div>
        </div>

        <div class="form-group">
            <label class="field-label">Portion Size</label>
            <div class="radio-grid">
                <label class="radio-option"><input type="radio" name="portion" value="small"> Too Small</label>
                <label class="radio-option"><input type="radio" name="portion" value="perfect" checked> Just Right</label>
                <label class="radio-option"><input type="radio" name="portion" value="large"> Too Large</label>
            </div>
        </div>
    </fieldset>

    <!-- Section 3: Open Thoughts -->
    <fieldset>
        <legend>3. Comments & Guest Info</legend>
        
        <div class="form-group">
            <label class="field-label" for="comments">Any notes for the Chef?</label>
            <textarea id="comments" name="comments" placeholder="Was the seasoning right? Anything we should add to the menu?"></textarea>
        </div>

        <div class="form-group">
            <label class="field-label" for="guest-name">Your Name (Optional)</label>
            <input type="text" id="guest-name" name="guest_name" placeholder="Jane Doe">
        </div>

        <div class="form-group">
            <label class="field-label" for="guest-email">Email Address (Optional)</label>
            <input type="email" id="guest-email" name="guest_email" placeholder="jane@example.com">
        </div>
    </fieldset>

    <button type="submit" class="submit-btn">Send Feedback</button>

</form>

</body>
</html>
