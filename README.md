
# Website Documentation

## 🔗 Website link
[youthm01.github.io](https://youthm01.github.io/)


## Overview
The code has been reused from A1 and A1 collectively.
This website, created by Man Yang, showcases my programming skills, projects, and personal journey in the IT sphere. It aims to share my work, insights into programming, and a bit of my personality, hoping to connect with like-minded individuals and potential opportunities in the IT industry.

## Directory Structure

- `/`: Root directory containing the main HTML files.
  - `index.html`: Homepage introducing me, my interests in programming, and a brief about my personality.
  - `projects.html`: Lists various projects with descriptions, technologies used, and their functionalities.
  - `blog.html`: Features articles on coding learnings, tips, and technical viewpoints.
  - `form.html`: Displays a feedback form for the user to give the feedback.

- `/css`: Contains CSS files for styling the website.

- `/img`: Directory for images used across the website.
  - `favicon.ico`: Website favicon.
  - `profile.jpg`: A portrait of Man Yang used in the introduction section.
  - `blog.jpg`: Represents the blog section.
  - `skills.jpg`: Showcases the skillset Man Yang possesses.

### Code Snippets Documentation
#### 1. Navigation Menu
```html
<nav>
    <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="projects.html">Projects</a></li>
        <li><a href="blog.html">Blog</a></li>
        <li><a href="form.html">Feedback form</a></li>

    </ul>
</nav>
```
- **Purpose**: Provides a navigation menu on the website, allowing users to easily navigate to the Home page, Projects page, and Blog section. Placed typically at the top of every page for consistent site navigation. Requires CSS for styling. Embedded within the `<body>` tag of HTML documents.

#### 2. YouTube Video Embed
```html
<iframe width="250" height="140" src="https://www.youtube.com/embed/MZEDpuQdDag" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```
- **Purpose**: Embeds a YouTube video into the webpage, offering a multimedia element to engage visitors. Used to showcase video content related to the site's content, such as a project demo. Can be placed within any section of a webpage where video content is relevant.

#### 3. Footer with Contact Information
```html
<footer>
    <p>Contact me: <a href="mailto:mn932850@dal.ca">mn932850@dal.ca</a></p>
</footer>
```
- **Purpose**: Provides a footer section for the website containing contact information, enhancing website accessibility and user engagement.bPlaced at the bottom of every webpage. Requires CSS for styling.

#### 4. Page Metadata and Favicon
```html
<head>
    <meta charset="UTF-8">
    <title>Home - My Programming Portfolio</title>
    <link rel="icon" href="img/favicon.ico" type="image/x-icon">
</head>
```
- **Purpose**: Sets up the character encoding, page title, and favicon for the website, crucial for web standards and branding. Included within the `<head>` section of each HTML document. The favicon file (`favicon.ico`) needs to be placed in the specified path.

#### 5. Linked Image to External Content
```html
<a href="https://content.techgig.com/technology/top-8-programming-blogs-that-every-software-developer-must-read/articleshow/77672235.cms"><img src="img/skills.jpg" alt="Skills Image" width="100" height="100"></a>
```
- **Purpose**: Provides an image link to external content, in this case, a programming blog, which serves as a resource or further reading. Can be used in blog sections or resources page to link to external authoritative content. Requires the image (`img/skills.jpg`) to be present in the specified path.

#### 6. Video and Audio Embed
```html
<video controls width="250">
    <source src="videos/introduction_video.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
<audio controls>
    <source src="audio/intoduction_audio.mp4" type="audio/mpeg">
    Your browser does not support the audio element.
</audio>
```
- **Purpose**: Embeds video and audio clips into the webpage, providing a rich media experience for the user. Used for introducing the website owner or showcasing multimedia presentations. The video (`introduction_video.mp4`) and audio (`introduction_audio.mp4`) files need to be stored in the specified paths.

#### 7. Profile Image and Projects Table
```html
<img src="img/profile.jpg" alt="Professional Headshot" width="200" height="200">
<table>
    <tr>
        <th>Project Name</th>
        <th>Technologies Used</th>
        <th>Link</th>
    </tr>
    <tr>
        <td>🖥 FRONT END CHALLENGES OR SKILLS</td>
        <td>HTML, CSS</td>
        <td><a href="https://github.com/iamismile/web-dev-resources?tab=readme-ov-file#-front-end-challenges-or-skills">View Project</a></td>
    </tr>
</table>
```
- **Purpose**: Displays a professional headshot and a table listing projects with technologies used and links to view the projects.Utilized in about or portfolio sections to showcase professional image and detailed project information. Requires the profile image (`img/profile.jpg`) to be present in the specified path and CSS for styling the table.

#### 8. Table Color Changer

```html
<div class="text-center mt-4">
    <button id="changeColorButton1" class="btn btn-primary mr-2">Change Color 1</button>
    <button id="changeColorButton2" class="btn btn-primary">Change Color 2</button>
</div>

<script>
    // Function to change the color of the table when 'Change Color 1' button is clicked
    document.getElementById('changeColorButton1').addEventListener('click', function() {
        document.getElementById('projectTable').classList.add('table-color1');
        document.getElementById('projectTable').classList.remove('table-color2');
    });

    // Function to change the color of the table when 'Change Color 2' button is clicked
    document.getElementById('changeColorButton2').addEventListener('click', function() {
        document.getElementById('projectTable').classList.add('table-color2');
        document.getElementById('projectTable').classList.remove('table-color1');
    });
</script>
```
- **Purpose**: This script enables users to dynamically change the color scheme of a table by clicking buttons. This feature enhances user experience and allows customization of visual appearance. When the "Change Color 1" button is clicked, the table's color scheme is changed to the one defined by the table-color1 CSS class. Similarly, clicking the "Change Color 2" button changes the color scheme to that of the table-color2 CSS class.

#### 9. Notifications
```js
Toastify({
                    text: feedbackMessage,
                    duration: 3000,
                    close: false,
                    gravity: "top", 
                    position: "right",
                    stopOnFocus: true, 
                    style: {
                        background: "linear-gradient(to right, #00b09b, #96c93d)",
                    },
                    onClick: function(){}
                }).showToast();
```
- **Purpose**: This code snippet displays a toast notification with specified settings such as text content, duration, position, and styling. The code will display a toast notification with the content specified by feedbackMessage, using a linear gradient background from #00b09b to #96c93d, positioned at the top right corner of the screen, and will disappear after 3000 milliseconds.

#### 10. Limit Character count in Text Area
```js
commentsTextarea.addEventListener('input', function() {
            const remainingChars = 100 - commentsTextarea.value.length;
            charCounter.textContent = remainingChars;
            if (remainingChars === 0) {
                commentsTextarea.setAttribute('maxlength', commentsTextarea.value.length);
                charCounter.textContent = 'Max characters reached';
            }
        });
```
- **Purpose**: This event listener monitors the input in a textarea element (commentsTextarea) and updates a character counter (charCounter). It restricts the input when the maximum character limit (100 characters) is reached and provides feedback to the user. As the user types into the textarea, the character counter updates to display the remaining characters. When the character limit is reached, further input is prevented, and the character counter displays "Max characters reached".

#### 11. Rating Feature
```js
if (form.checkValidity()) {
                const rating = form.querySelector('input[name="rating"]:checked').value;
                let feedbackMessage = "Thank you for your feedback!";
                if (rating >= 4) {
                    feedbackMessage = "We're thrilled to hear you enjoyed it! Feel free to share your experience.";
                } else if (rating == 3) {
                    feedbackMessage = "Thank you! We're always looking to improve.";
                } else {
                    feedbackMessage = "We're sorry to hear that. Please let us know how we can improve.";
                }
                Toastify({
                    text: feedbackMessage,
                    duration: 3000,
                    close: false,
                    gravity: "top", 
                    position: "right",
                    stopOnFocus: true, 
                    style: {
                        background: "linear-gradient(to right, #00b09b, #96c93d)",
                    },
                    onClick: function(){}
                }).showToast();
                form.reset();
            } else {
                alert('Please fill out all required fields correctly.');
            }
```
- **Purpose**: This code snippet handles form submission by validating the form inputs. It retrieves the selected rating from the form and provides feedback to the user based on the rating. 

#### 12. Feedback form
```js
 <form id="exampleForm">
            <!-- Name Input -->
            <div class="form-group">
                <label for="name">Name</label>
                <input type="text" class="form-control" id="name" name="name" required>
            </div>
            <!-- Email Input -->
            <div class="form-group">
                <label for="email">Email</label>
                <input type="email" class="form-control" id="email" name="email" required>
            </div>
            <!-- Age Input -->
            <div class="form-group">
                <label for="age">Age</label>
                <input type="number" class="form-control" id="age" name="age" required>
            </div>
            <!-- Gender Input -->
            <div class="form-group">
                <label for="gender">Gender</label>
                <select class="form-control" id="gender" name="gender" required>
                    <option value="">Select Gender</option>
                    <option value="male">Male</option>
                    <option value="female">Female</option>
                    <option value="other">Other</option>
                </select>
            </div>
            <!-- Star Rating Input -->
            <div class="form-group">
                <label for="rating">Rating</label>
                <div class="star-rating">
                    <input id="star5" name="rating" type="radio" value="5" class="star" />
                    <label for="star5" title="5 star">★</label>
                    <input id="star4" name="rating" type="radio" value="4" class="star" />
                    <label for="star4" title="4 stars">★</label>
                    <input id="star3" name="rating" type="radio" value="3" class="star" />
                    <label for="star3" title="3 stars">★</label>
                    <input id="star2" name="rating" type="radio" value="2" class="star" />
                    <label for="star2" title="2 stars">★</label>
                    <input id="star1" name="rating" type="radio" value="1" class="star" />
                    <label for="star1" title="1 stars">★</label>
                </div>
            </div>
            <!-- Additional Comments -->
            <div class="form-group position-relative">
                <label for="comments">Additional Comments</label>
                <textarea class="form-control" id="comments" name="comments" rows="3" required maxlength="100"></textarea>
                <span class="char-counter">100</span>
            </div>
            <!-- Submit Button -->
            <button type="submit" class="btn btn-primary btn-block">Submit</button>
        </form>
```
- **Purpose**: This HTML form collects information from the user including name, email, age, gender, star rating, and additional comments. It is designed to gather feedback from users and submit it for processing.
Dependent Code Structures. Users can fill out the form fields, including their name, email, age, gender, rating, and additional comments. Upon submission, the form content can be processed to gather feedback.



#### 13. 

## External Sources

[1]	fayefilms. 2023. First day of university and I’m already tired. Retrieved February 9, 2024 from https://www.youtube.com/shorts/MZEDpuQdDag
 	 
[2]	Ismile Hossain. web-dev-resources: The complete web development resources you ever need. More than 150+ resources for your web development.
 	 
[3]	Istockphoto.com. Retrieved February 9, 2024 from https://media.istockphoto.com/id/1318327528/photo/charming-asian-businesswoman-working-with-a-laptop-at-the-office-looking-at-camera.jpg?s=612x612&w=0&k=20&c=t-DTh02iSEXHea_5ZV0hnuw-8KCMz3Z9Ki4slzQkulk=
 	 
[4]	Techgig.com. Retrieved February 9, 2024 from https://contentstatic.techgig.com/photo/77672235/top-8-programming-blogs-that-every-software-developer-must-read.jpg?150543

[5] A. P. Varun. README.md at master · apvarun/toastify-js.

[6] How to create a simple star rating with CSS. W3schools.com. Retrieved April 2, 2024 from https://www.w3schools.com/howto/howto_css_star_rating.asp

[7] HTML forms. W3schools.com. Retrieved April 2, 2024 from https://www.w3schools.com/html/html_forms.asp

[8]JavaScript DOM EventListener. W3schools.com. Retrieved April 2, 2024 from https://www.w3schools.com/js/js_htmldom_eventlistener.asp
 	 
## Contact

Man Yang
Email: mn932850@dal.ca










