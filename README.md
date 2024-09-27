# Main-flow
This is a contact form..


for html codes
  index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Interactive Webpage</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="gfd">
    <div class="abc">
    <h1>ADDI'S.IN</h1>

    <!-- Contact Form -->
    <h2>FILL THE FORM TO ENHANCE YOUR SKILL</h2>
    <form id="contactForm">
        <input type="text" id="name" placeholder="Name" required>
        <input type="email" id="email" placeholder="Email" required>
        <input type="phone" id="phone" placeholder="Phone no" required>
        <textarea id="message" placeholder="Message" required></textarea>
        <button type="submit">Submit</button>
    </form>
    <div id="formMessage"></div>

    <!-- Image Slideshow -->
    <h2>OUR TEAM MEMBERS</h2>
    <img id="slide" src="WhatsApp Image 2024-09-27 at 07.43.23_4dd8ff60.jpg">
    <button onclick="nextSlide()">Next</button>


    <p>To join our community this form is compulsory,make your carrier enhance yourself with us..</p>


    <!-- Toggle Content -->
    <h2>Toggle Content</h2>
    <button onclick="toggleContent()">Toggle Info</button>
    <div id="toggleDiv" style="display:none;">
        <p>This is additional info.</p>
    </div>

    <script src="script.js"></script>
    </div>
    </div>
</body>
</html>

           for Css codes
            styles.css
            .gfd{
    padding-left:500px;
}
.abc{
    text-align: center;
    width:400px;

}
body {
    font-family: Arial, sans-serif;
    margin: 20px;
    padding: 20px;
    background-color: #f4f4f4;
}

h1 {
    color: #333;
}

h2 {
    color: #555;
}

form {
    margin-bottom: 20px;
}

input, textarea {
    width: 100%;
    padding: 10px;
    margin: 5px 0;
    border: 1px solid #ccc;
    border-radius: 5px;
}

button {
    padding: 10px 15px;
    background-color: #28a745;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #218838;
}

#formMessage {
    margin-top: 10px;
    color: green;
}

#toggleDiv {
    margin-top: 10px;
    background-color: #e9ecef;
    padding: 10px;
    border-radius: 5px;
}
#slide{
    width:200px;
    height:150px;
}

   for javascript codes
         scripts.js
         // Slideshow
let currentSlide = 0;
const images = ["WhatsApp Image 2024-09-27 at 07.32.38_39bc5566.jpg", "WhatsApp Image 2024-09-27 at 07.32.38_78df0b1a.jpg", "WhatsApp Image 2024-09-27 at 07.33.32_a22b6d14.jpg"]; // Your images

function nextSlide() {
    currentSlide = (currentSlide + 1) % images.length;
    document.getElementById("slide").src = images[currentSlide];
}

// Form Validation
document.getElementById("contactForm").addEventListener("submit", function(event) {
    event.preventDefault();
    const name = document.getElementById("name").value;
    const email = document.getElementById("email").value;
    const message = document.getElementById("message").value;

    if (name && email && message) {
        document.getElementById("formMessage").innerText = "Thank you!";
        this.reset();
    } else {
        document.getElementById("formMessage").innerText = "Please fill all fields.";
    }
});

// Toggle Content
function toggleContent() {
    const toggleDiv = document.getElementById("toggleDiv");
    toggleDiv.style.display = toggleDiv.style.display === "none" ? "block" : "none";
}
