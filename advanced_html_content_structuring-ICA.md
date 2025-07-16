# Lesson 3: In-Class Assignments
## Advanced HTML & Content Structuring

---

## **Assignment 1: Build a Blog Article Page** ⏰ 15 minutes

### **Objective**
Create a semantic blog article page using advanced HTML5 elements and accessibility features.

### **Setup Instructions**
1. **Create a new HTML file** called `blog-article.html`
2. **Open your project folder** in VS Code (File → Open Folder)
3. **Start with basic HTML5 structure** (use `!` + Tab for quick setup)

### **Requirements**
1. **Header section** with:
   - Site title
   - Navigation menu with at least 3 links
   - ARIA roles for accessibility

2. **Main article** with:
   - Article header (title, date, author)
   - At least 2 content sections
   - One figure with image and caption
   - Aside with related content

3. **Footer** with:
   - Contact information using `<address>` element

4. **Accessibility features:**
   - Skip link for keyboard navigation
   - Proper ARIA roles
   - Semantic HTML elements

### **HTML Structure Template**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Add meta tags and title here -->
</head>
<body>
    <!-- Add skip link here -->
    
    <header role="banner">
        <!-- Add site title and navigation here -->
    </header>

    <main id="main-content" role="main">
        <article>
            <header>
                <!-- Add article title, date, and author here -->
            </header>

            <section>
                <!-- Add first content section here -->
                <!-- Include a figure with image and caption -->
            </section>

            <section>
                <!-- Add second content section here -->
            </section>

            <aside role="complementary">
                <!-- Add related content here -->
            </aside>
        </article>
    </main>

    <footer role="contentinfo">
        <!-- Add contact information with address element -->
    </footer>
</body>
</html>
```

### **HTML Elements You'll Need**
- **Semantic structure:** `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<aside>`, `<footer>`
- **Content elements:** `<h1>`, `<h2>`, `<h3>`, `<p>`, `<ul>`, `<li>`, `<a>`
- **Advanced elements:** `<figure>`, `<figcaption>`, `<time>`, `<address>`
- **ARIA attributes:** `role`, `aria-label`

### **Success Criteria**
- [ ] Uses semantic HTML5 elements correctly
- [ ] Includes proper article structure
- [ ] Has skip link for accessibility
- [ ] Figure and figcaption work together
- [ ] ARIA roles enhance accessibility
- [ ] Proper heading hierarchy (h1 → h2 → h3)

### **Bonus Challenges** (if you finish early)
- Add a definition list (`<dl>`, `<dt>`, `<dd>`) for technical terms
- Include details/summary element for expandable content
- Add more ARIA attributes (`aria-describedby`, `aria-labelledby`)
- Include proper meta tags for SEO

---

## **Assignment 2: Create Registration Form** ⏰ 20 minutes

### **Objective**
Build a comprehensive registration form with various input types, proper validation, and accessibility features.

### **Setup Instructions**
- **Create new file:** `registration-form.html` 
- **Use your blog-article.html** as a starting template for the basic structure
- **Focus on the main content area** for your form

### **Form Requirements**

#### **1. Personal Information Section**
- Full name (text input with pattern validation)
- Email address (email input, required)
- Phone number (tel input with pattern)
- Date of birth (date input)

#### **2. Experience Section**
- Years of experience (number input with min/max)
- Skill level (radio buttons)
- Areas of interest (multi-select dropdown)
- Personal website (URL input)

#### **3. Preferences Section**
- Communication preferences (checkboxes)
- Course format preference (radio buttons)

#### **4. Form Controls**
- Reset button
- Submit button

### **HTML Structure Template**
```html
<main id="main-content" role="main">
    <h1>Course Registration</h1>
    
    <form action="/submit" method="POST" novalidate>
        <fieldset>
            <legend>Personal Information</legend>
            
            <!-- Add name, email, phone, birth date inputs here -->
            
        </fieldset>

        <fieldset>
            <legend>Experience & Skills</legend>
            
            <!-- Add experience inputs here -->
            <!-- Add skill level radio buttons here -->
            <!-- Add interests multi-select here -->
            <!-- Add website URL input here -->
            
        </fieldset>

        <fieldset>
            <legend>Preferences</legend>
            
            <!-- Add communication checkboxes here -->
            <!-- Add course format radio buttons here -->
            
        </fieldset>

        <div class="form-controls">
            <!-- Add reset and submit buttons here -->
        </div>
    </form>
</main>
```

### **Form Elements You'll Need**
- **Form structure:** `<form>`, `<fieldset>`, `<legend>`
- **Input types:** `text`, `email`, `tel`, `date`, `number`, `url`
- **Selection:** `<select>`, `<optgroup>`, `<option>`
- **Radio/Checkbox:** `input type="radio"`, `input type="checkbox"`
- **Labels:** `<label for="id">`, `id` on inputs
- **Help text:** `<small>`, `aria-describedby`
- **Buttons:** `<button type="submit">`, `<button type="reset">`

### **Accessibility Requirements**
- **Proper label associations:** Use `for` and `id` attributes
- **Fieldset grouping:** Group related form controls
- **Help text:** Link help text with `aria-describedby`
- **Required indicators:** Mark required fields clearly
- **Validation attributes:** `required`, `pattern`, `min`, `max`

### **Success Criteria**
- [ ] All form sections properly structured with fieldset/legend
- [ ] Every input has an associated label
- [ ] Uses appropriate input types for each field
- [ ] Includes validation attributes
- [ ] Help text is properly linked to inputs
- [ ] Form is keyboard accessible

### **Sample Input Examples**
```html
<!-- Text with pattern validation -->
<div class="form-group">
    <label for="fullname">Full Name *</label>
    <input type="text" 
           id="fullname" 
           name="fullname" 
           required 
           pattern="[A-Za-z ]{2,50}"
           aria-describedby="name-help">
    <small id="name-help">Enter first and last name (2-50 characters)</small>
</div>

<!-- Email input -->
<div class="form-group">
    <label for="email">Email Address *</label>
    <input type="email" 
           id="email" 
           name="email" 
           required
           autocomplete="email">
</div>

<!-- Radio button group -->
<fieldset>
    <legend>Experience Level</legend>
    
    <div class="radio-group">
        <input type="radio" id="beginner" name="level" value="beginner">
        <label for="beginner">Beginner (0-1 years)</label>
    </div>
    
    <div class="radio-group">
        <input type="radio" id="intermediate" name="level" value="intermediate">
        <label for="intermediate">Intermediate (2-5 years)</label>
    </div>
</fieldset>
```

---

## **Assignment 3: Portfolio Enhancement with Git** ⏰ 10 minutes
This Project will be based off of your portfolio from yesterday's inclass assignment/Homework

### **Objective**
Use Git feature branches to enhance your portfolio with advanced HTML features.

### **⭐ Git Workflow Tip**
**Remember:** Always open VS Code directly to your project folder (File → Open Folder) to make Git commands work properly in the integrated terminal.

### **Git Setup Instructions**
1. **Navigate to your portfolio project** (the folder with your previous HTML files)
2. **Open integrated terminal** in VS Code (Terminal → New Terminal)
3. **Verify you're in the right location:** Run `ls` (Mac/Linux) or `dir` (Windows) to see your HTML files

### **Step 1: Create Feature Branch** ⏰ 2 minutes

**Commands to run:**
```bash
# Make sure you're on main branch and up to date
git checkout main
git pull origin main

# Create and switch to feature branch
git checkout -b feature/portfolio-enhancement
```

**Verification:**
- [ ] Terminal shows you're on the new branch
- [ ] No error messages

### **Step 2: Add Enhancement Features** ⏰ 6 minutes

**Choose 2-3 enhancements to add to your existing portfolio:**

#### **Option A: Skills Table**
Add a table showing your skills and experience levels:
```html
<section id="skills-table">
    <h2>Skills & Experience</h2>
    <table>
        <caption>Technical Skills Assessment</caption>
        <thead>
            <tr>
                <th scope="col">Skill</th>
                <th scope="col">Experience Level</th>
                <th scope="col">Years</th>
            </tr>
        </thead>
        <tbody>
            <!-- Add your skills here -->
        </tbody>
    </table>
</section>
```

#### **Option B: Multimedia Section**
Add video or audio elements:
```html
<section id="multimedia">
    <h2>My Work</h2>
    
    <!-- Video element -->
    <video controls width="640" height="360">
        <source src="demo-video.mp4" type="video/mp4">
        <p>Your browser doesn't support video. 
           <a href="demo-video.mp4">Download the video</a> instead.</p>
    </video>
    
    <!-- Or audio element -->
    <audio controls>
        <source src="interview.mp3" type="audio/mpeg">
        <p>Your browser doesn't support audio. 
           <a href="interview.mp3">Download the audio</a> instead.</p>
    </audio>
</section>
```

#### **Option C: Enhanced Contact Form**
Improve your existing contact form with new input types:
```html
<!-- Add these to your existing form -->
<div class="form-group">
    <label for="phone">Phone Number</label>
    <input type="tel" 
           id="phone" 
           name="phone"
           pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}"
           placeholder="123-456-7890">
</div>

<div class="form-group">
    <label for="website">Your Website</label>
    <input type="url" 
           id="website" 
           name="website"
           placeholder="https://example.com">
</div>
```

#### **Option D: Accessibility Improvements**
Enhance accessibility features:
```html
<!-- Add skip link at top of body -->
<a href="#main-content" class="skip-link">Skip to main content</a>

<!-- Add ARIA roles -->
<header role="banner">
<nav role="navigation" aria-label="Main navigation">
<main id="main-content" role="main">
<footer role="contentinfo">
```

### **Step 3: Commit and Push** ⏰ 2 minutes

**Commands to run:**
```bash
# Check what files have changed
git status

# Add all changes
git add .

# Commit with descriptive message
git commit -m "Add [describe your enhancements] to portfolio"

# Push feature branch to GitHub
git push origin feature/portfolio-enhancement
```

**Verification:**
- [ ] Commit successful
- [ ] Branch pushed to GitHub
- [ ] Can see your changes on GitHub website

### **Git Commands Reference**
```bash
# Check current status
git status

# Check current branch
git branch

# Add files to staging area
git add filename.html        # Add specific file
git add .                    # Add all files

# Commit changes
git commit -m "Your descriptive message here"

# Push to GitHub
git push origin branch-name

# Switch between branches
git checkout branch-name
```

### **Troubleshooting Common Issues**

**"Branch already exists" error:**
- Use a different branch name: `git checkout -b feature/portfolio-v2`

**"Working directory not clean" error:**
- Commit current changes first: `git add . && git commit -m "Save current work"`

**"No changes to commit" message:**
- Make sure you saved your HTML files
- Check you're in the right directory

### **Optional: Create Pull Request**
**If you finish early:**
1. Go to your GitHub repository
2. Click "Compare & pull request" button
3. Write a description of your changes
4. Create the pull request (don't merge yet)

---

## **Assignment Completion Checklist**

### **By the end of class, you should have:**

#### **Assignment 1:**
- [ ] Blog article with semantic structure
- [ ] Proper ARIA roles and accessibility features
- [ ] Figure, time, and address elements used correctly
- [ ] Skip link for keyboard navigation

#### **Assignment 2:**
- [ ] Complete registration form with multiple sections
- [ ] Various input types (text, email, tel, date, number, url)
- [ ] Proper form accessibility (labels, fieldsets, ARIA)
- [ ] Selection controls (radio, checkbox, select)

#### **Assignment 3:**
- [ ] Git feature branch created
- [ ] Portfolio enhanced with 2-3 new features
- [ ] Changes committed with clear messages
- [ ] Feature branch pushed to GitHub

### **Homework for Next Week:**
1. **Complete portfolio enhancement** by merging feature branch
2. **Test accessibility** using browser developer tools
3. **Validate HTML** at [validator.w3.org](https://validator.w3.org/)
4. **Read CSS basics tutorial** (link will be provided)
5. **Practice Git branching** with additional features

---

## **Need Help? Ask These Questions:**

1. **"My semantic elements aren't working"**
   - Check for proper nesting and closing tags
   - Verify you're using appropriate elements for content type
   - Make sure ARIA roles match the element's purpose

2. **"Form inputs aren't accessible"**
   - Verify every input has a matching label
   - Check `for` and `id` attributes match exactly
   - Ensure fieldset and legend are properly used

3. **"Git branch commands aren't working"**
   - Confirm you're in the right directory (should see your HTML files)
   - Check if you have unsaved changes with `git status`
   - Make sure you committed current work before creating new branch

4. **"Table structure is confusing"**
   - Start with basic table (table, tr, th, td)
   - Add semantic sections (thead, tbody, tfoot) gradually
   - Use scope attribute on header cells

5. **"Multimedia elements won't display"**
   - Check file paths are correct
   - Ensure file formats are supported
   - Always include fallback content
   - Test in different browsers

**Remember:** Focus on semantic meaning and accessibility. The visual styling will come in our next lesson with CSS! 🎨📱 
