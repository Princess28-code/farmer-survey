<!DOCTYPE html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Farmer Logistics Survey</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

```
    body {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        min-height: 100vh;
        padding: 20px;
    }
    
    .container {
        max-width: 800px;
        margin: 0 auto;
        background: white;
        border-radius: 20px;
        box-shadow: 0 20px 60px rgba(0,0,0,0.3);
        overflow: hidden;
        margin-bottom: 40px;
    }
    
    .header {
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        color: white;
        padding: 40px 30px;
        text-align: center;
    }
    
    .header h1 {
        font-size: 28px;
        margin-bottom: 10px;
    }
    
    .header p {
        font-size: 16px;
        opacity: 0.9;
        line-height: 1.6;
    }
    
    .form-content {
        padding: 40px 30px;
    }
    
    .section {
        margin-bottom: 40px;
    }
    
    .section-title {
        font-size: 22px;
        color: #667eea;
        margin-bottom: 20px;
        padding-bottom: 10px;
        border-bottom: 3px solid #667eea;
        font-weight: bold;
    }
    
    .question {
        margin-bottom: 30px;
    }
    
    .question-label {
        display: block;
        font-size: 16px;
        font-weight: 600;
        color: #2d3748;
        margin-bottom: 12px;
    }
    
    .required {
        color: #e53e3e;
    }
    
    .radio-group, .checkbox-group {
        display: flex;
        flex-direction: column;
        gap: 10px;
    }
    
    .radio-option, .checkbox-option {
        display: flex;
        align-items: center;
        padding: 12px 15px;
        background: #f7fafc;
        border-radius: 8px;
        cursor: pointer;
        transition: all 0.3s ease;
        border: 2px solid transparent;
    }
    
    .radio-option:hover, .checkbox-option:hover {
        background: #edf2f7;
        border-color: #667eea;
    }
    
    .radio-option input, .checkbox-option input {
        margin-right: 12px;
        cursor: pointer;
        width: 18px;
        height: 18px;
    }
    
    .radio-option label, .checkbox-option label {
        cursor: pointer;
        flex: 1;
        font-size: 15px;
    }
    
    .rank-group {
        display: flex;
        flex-direction: column;
        gap: 15px;
    }
    
    .rank-item {
        display: flex;
        align-items: center;
        gap: 15px;
        padding: 15px;
        background: #f7fafc;
        border-radius: 8px;
    }
    
    .rank-item label {
        flex: 1;
        font-size: 15px;
    }
    
    .rank-item select {
        padding: 8px 12px;
        border: 2px solid #e2e8f0;
        border-radius: 6px;
        font-size: 14px;
        cursor: pointer;
        background: white;
    }
    
    .submit-section {
        text-align: center;
        padding: 30px 0;
        border-top: 2px solid #e2e8f0;
    }
    
    .submit-btn {
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        color: white;
        border: none;
        padding: 15px 60px;
        font-size: 18px;
        font-weight: bold;
        border-radius: 50px;
        cursor: pointer;
        transition: transform 0.3s ease;
        box-shadow: 0 4px 15px rgba(102, 126, 234, 0.4);
    }
    
    .submit-btn:hover {
        transform: translateY(-2px);
    }
    
    .success-message {
        display: none;
        background: #48bb78;
        color: white;
        padding: 20px;
        border-radius: 10px;
        margin-top: 20px;
        text-align: center;
        font-size: 18px;
    }
    
    .success-message.show {
        display: block;
    }
    
    @media (max-width: 600px) {
        .header h1 { font-size: 24px; }
        .form-content { padding: 30px 20px; }
        .submit-btn { padding: 12px 40px; font-size: 16px; }
    }
</style>
```

</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🌾 Buying Intention Survey</h1>
            <p>Shared Logistics Platform for Small Farmers</p>
            <p style="margin-top: 15px; font-size: 14px;">This survey aims to understand the logistics challenges faced by small-scale farmers and assess their interest in a shared logistics platform.</p>
        </div>

```
    <div class="form-content">
        <form id="surveyForm">
            <div class="section">
                <h2 class="section-title">Section A: Background Information</h2>
                
                <div class="question">
                    <label class="question-label">1. Farm Size <span class="required">*</span></label>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" name="farmSize" value="Less than 5 acres" id="farm1" required>
                            <label for="farm1">Less than 5 acres</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="farmSize" value="5-20 acres" id="farm2">
                            <label for="farm2">5-20 acres</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="farmSize" value="20-50 acres" id="farm3">
                            <label for="farm3">20-50 acres</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="farmSize" value="More than 50 acres" id="farm4">
                            <label for="farm4">More than 50 acres</label>
                        </div>
                    </div>
                </div>
                
                <div class="question">
                    <label class="question-label">2. Type of Crops <span class="required">*</span></label>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" name="cropType" value="Vegetables" id="crop1" required>
                            <label for="crop1">Vegetables</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="cropType" value="Fruits" id="crop2">
                            <label for="crop2">Fruits</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="cropType" value="Organic produce" id="crop3">
                            <label for="crop3">Organic produce</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="cropType" value="Mixed farming" id="crop4">
                            <label for="crop4">Mixed farming</label>
                        </div>
                    </div>
                </div>
                
                <div class="question">
                    <label class="question-label">3. Current Monthly Logistics Cost <span class="required">*</span></label>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" name="logisticsCost" value="Less than $500" id="cost1" required>
                            <label for="cost1">Less than $500</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="logisticsCost" value="$500-$1,000" id="cost2">
                            <label for="cost2">$500-$1,000</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="logisticsCost" value="$1,000-$2,000" id="cost3">
                            <label for="cost3">$1,000-$2,000</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="logisticsCost" value="More than $2,000" id="cost4">
                            <label for="cost4">More than $2,000</label>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title">Section B: Current Challenges</h2>
                
                <div class="question">
                    <label class="question-label">4. What are your biggest logistics challenges? (Select all that apply) <span class="required">*</span></label>
                    <div class="checkbox-group">
                        <div class="checkbox-option">
                            <input type="checkbox" name="challenges" value="High transportation costs" id="chal1">
                            <label for="chal1">High transportation costs</label>
                        </div>
                        <div class="checkbox-option">
                            <input type="checkbox" name="challenges" value="Lack of refrigerated storage" id="chal2">
                            <label for="chal2">Lack of refrigerated storage</label>
                        </div>
                        <div class="checkbox-option">
                            <input type="checkbox" name="challenges" value="Difficulty accessing markets" id="chal3">
                            <label for="chal3">Difficulty accessing markets</label>
                        </div>
                        <div class="checkbox-option">
                            <input type="checkbox" name="challenges" value="Product spoilage during transport" id="chal4">
                            <label for="chal4">Product spoilage during transport</label>
                        </div>
                        <div class="checkbox-option">
                            <input type="checkbox" name="challenges" value="Unpredictable delivery schedules" id="chal5">
                            <label for="chal5">Unpredictable delivery schedules</label>
                        </div>
                    </div>
                </div>
                
                <div class="question">
                    <label class="question-label">5. How often do you lose products due to poor logistics? <span class="required">*</span></label>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" name="productLoss" value="Never" id="loss1" required>
                            <label for="loss1">Never</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="productLoss" value="Rarely (less than 5%)" id="loss2">
                            <label for="loss2">Rarely (less than 5%)</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="productLoss" value="Sometimes (5-15%)" id="loss3">
                            <label for="loss3">Sometimes (5-15%)</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="productLoss" value="Often (more than 15%)" id="loss4">
                            <label for="loss4">Often (more than 15%)</label>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title">Section C: Platform Interest</h2>
                
                <div class="question">
                    <label class="question-label">6. Would you use a shared logistics platform that reduces costs by 40-60%? <span class="required">*</span></label>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" name="willingness" value="Definitely yes" id="will1" required>
                            <label for="will1">Definitely yes</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="willingness" value="Probably yes" id="will2">
                            <label for="will2">Probably yes</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="willingness" value="Not sure" id="will3">
                            <label for="will3">Not sure</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="willingness" value="Probably no" id="will4">
                            <label for="will4">Probably no</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="willingness" value="Definitely no" id="will5">
                            <label for="will5">Definitely no</label>
                        </div>
                    </div>
                </div>
                
                <div class="question">
                    <label class="question-label">7. How much would you pay monthly for shared logistics services? <span class="required">*</span></label>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" name="payment" value="$50-$150" id="pay1" required>
                            <label for="pay1">$50-$150</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="payment" value="$150-$300" id="pay2">
                            <label for="pay2">$150-$300</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="payment" value="$300-$500" id="pay3">
                            <label for="pay3">$300-$500</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="payment" value="More than $500" id="pay4">
                            <label for="pay4">More than $500</label>
                        </div>
                    </div>
                </div>
                
                <div class="question">
                    <label class="question-label">8. Rank features by importance (1=Most Important, 5=Least Important) <span class="required">*</span></label>
                    <div class="rank-group">
                        <div class="rank-item">
                            <label>Refrigerated transportation</label>
                            <select name="rank_refrigerated" required>
                                <option value="">-</option>
                                <option value="1">1</option>
                                <option value="2">2</option>
                                <option value="3">3</option>
                                <option value="4">4</option>
                                <option value="5">5</option>
                            </select>
                        </div>
                        <div class="rank-item">
                            <label>Shared warehouse storage</label>
                            <select name="rank_warehouse" required>
                                <option value="">-</option>
                                <option value="1">1</option>
                                <option value="2">2</option>
                                <option value="3">3</option>
                                <option value="4">4</option>
                                <option value="5">5</option>
                            </select>
                        </div>
                        <div class="rank-item">
                            <label>Direct market access</label>
                            <select name="rank_market" required>
                                <option value="">-</option>
                                <option value="1">1</option>
                                <option value="2">2</option>
                                <option value="3">3</option>
                                <option value="4">4</option>
                                <option value="5">5</option>
                            </select>
                        </div>
                        <div class="rank-item">
                            <label>Real-time tracking</label>
                            <select name="rank_tracking" required>
                                <option value="">-</option>
                                <option value="1">1</option>
                                <option value="2">2</option>
                                <option value="3">3</option>
                                <option value="4">4</option>
                                <option value="5">5</option>
                            </select>
                        </div>
                        <div class="rank-item">
                            <label>Quality certification</label>
                            <select name="rank_quality" required>
                                <option value="">-</option>
                                <option value="1">1</option>
                                <option value="2">2</option>
                                <option value="3">3</option>
                                <option value="4">4</option>
                                <option value="5">5</option>
                            </select>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title">Section D: Buying Intention</h2>
                
                <div class="question">
                    <label class="question-label">9. If this platform launched next month, would you sign up? <span class="required">*</span></label>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" name="signup" value="Yes, immediately" id="sign1" required>
                            <label for="sign1">Yes, immediately</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="signup" value="Yes, within 3 months" id="sign2">
                            <label for="sign2">Yes, within 3 months</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="signup" value="Yes, within 6 months" id="sign3">
                            <label for="sign3">Yes, within 6 months</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="signup" value="Maybe, need more information" id="sign4">
                            <label for="sign4">Maybe, need more information</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" name="signup" value="No" id="sign5">
                            <label for="sign5">No</label>
                        </div>
                    </div>
                </div>
                
                <div class="question">
                    <label class="question-label">10. What concerns would prevent you from using this service? (Select all that apply) <span class="required">*</span></label>
                    <div class="checkbox-group">
                        <div class="checkbox-option">
                            <input type="checkbox" name="concerns" value="Trust issues with other farmers" id="con1">
                            <label for="con1">Trust issues with other farmers</label>
                        </div>
                        <div class="checkbox-option">
                            <input type="checkbox" name="concerns" value="Technology barriers" id="con2">
                            <label for="con2">Technology barriers</label>
                        </div>
                        <div class="checkbox-option">
                            <input type="checkbox" name="concerns" value="Cost concerns" id="con3">
                            <label for="con3">Cost concerns</label>
                        </div>
                        <div class="checkbox-option">
                            <input type="checkbox" name="concerns" value="Lack of flexibility" id="con4">
                            <label for="con4">Lack of flexibility</label>
                        </div>
                        <div class="checkbox-option">
                            <input type="checkbox" name="concerns" value="Other" id="con5">
                            <label for="con5">Other</label>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="submit-section">
                <button type="submit" class="submit-btn">📩 Submit Survey</button>
            </div>
        </form>
        
        <div class="success-message" id="successMessage">
            ✅ Thank you! Your response has been recorded successfully.
        </div>
    </div>
</div>

<script>
    document.getElementById('surveyForm').addEventListener('submit', function(e) {
        e.preventDefault();
        document.getElementById('successMessage').classList.add('show');
        this.style.display = 'none';
        window.scrollTo({ top: 0, behavior: 'smooth' });
    });
</script>
```

</body>
</html>
