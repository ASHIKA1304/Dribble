# Project Responsive Web Design using Bootstrap
## Date:13-05-25

## AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.


## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

### Step 5:
Create a HTML file and include the needed Bootstrap components.

### Step 6:
Publish the website in the LocalHost.

## PROGRAM :
## project.html
```
@import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');

body {
    font-family: 'Pacifico', cursive;
    margin: 0;
    padding: 0;
    background-color: #bcd4d4; /* Soft teal background */
    color: #2c3e50; /* Dark, contrasting text */
}

/* Navbar Customization */
.navbar {
    background-color: #00695c; /* Dark teal background */
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1); /* Slight shadow */
}

.navbar-brand, .navbar-nav .nav-link {
    color: #ffffff !important;
}

.navbar-nav {
    flex-direction: row;
}

.navbar-nav .nav-link {
    padding: 0 15px;
}

.nav-item .btn-primary {
    background-color: #ff7043; /* Coral for buttons */
    border-color: #ff7043;
}

.nav-item .btn-primary:hover {
    background-color: #d84315; /* Darker coral on hover */
    border-color: #d84315;
}

/* Header Section */
.header-section h3 {
    font-weight: bold;
    color: #00695c; /* Dark teal */
}

.header-section p {
    font-size: 1.2em;
    color: #37474f; /* Darker, readable text */
}

/* Gallery and Card adjustments */
.gallery-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 20px;
    padding: 20px;
}

/* Card Styling */
.card {
    background-color: #ffffff;
    border: 1px solid #cfd8dc;
    border-radius: 10px;
    box-shadow: 0px 6px 12px rgba(0, 0, 0, 0.08); /* Light shadow */
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 0; /* No padding around card */
    margin-bottom: 20px;
}

.card:hover {
    transform: translateY(-5px); /* Lift effect */
    box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.15); /* Stronger shadow on hover */
}

/* Adjusted Card Image Styling */
.gallery-img {
    width: 100%;
    height: 180px;
    object-fit: cover;
    border-radius: 10px 10px 0 0; /* Rounded top corners only */
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    margin-bottom: 0; /* No bottom margin */
}

.card:hover .gallery-img {
    transform: scale(1.05); /* Zoom effect on hover */
    box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.25); /* Subtle shadow on hover */
}

/* Card Content */
.card-title {
    font-weight: bold;
    font-size: 1.1rem;
    color: #00695c; /* Dark teal for titles */
    text-align: center;
    margin-top: 15px;
}

.card-body {
    padding: 20px;
    text-align: center;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

/* Footer */
footer {
    background-color: #00695c;
    color: #ffffff;
    text-align: center;
    padding: 25px;
    font-size: 0.9em;
    margin-top: 40px;
    box-shadow: 0px -2px 5px rgba(0, 0, 0, 0.1); /* Shadow above footer */
}

/* Responsive Design */
@media (max-width: 768px) {
    .navbar-nav {
        flex-direction: column;
        text-align: center;
        padding: 10px 0;
    }

    .gallery-section {
        margin-top: 20px;
    }

    .card-body {
        padding: 10px;
    }
}

@media (max-width: 480px) {
    .header-section h3 {
        font-size: 1.5em;
    }

    .header-section p {
        font-size: 1em;
    }
}
```

## project.css
```
@import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');

body {
    font-family: 'Pacifico', cursive;
    margin: 0;
    padding: 0;
    background-color: #bcd4d4; /* Soft teal background */
    color: #2c3e50; /* Dark, contrasting text */
}

/* Navbar Customization */
.navbar {
    background-color: #00695c; /* Dark teal background */
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1); /* Slight shadow */
}

.navbar-brand, .navbar-nav .nav-link {
    color: #ffffff !important;
}

.navbar-nav {
    flex-direction: row;
}

.navbar-nav .nav-link {
    padding: 0 15px;
}

.nav-item .btn-primary {
    background-color: #ff7043; /* Coral for buttons */
    border-color: #ff7043;
}

.nav-item .btn-primary:hover {
    background-color: #d84315; /* Darker coral on hover */
    border-color: #d84315;
}

/* Header Section */
.header-section h3 {
    font-weight: bold;
    color: #00695c; /* Dark teal */
}

.header-section p {
    font-size: 1.2em;
    color: #37474f; /* Darker, readable text */
}

/* Gallery and Card adjustments */
.gallery-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 20px;
    padding: 20px;
}

/* Card Styling */
.card {
    background-color: #ffffff;
    border: 1px solid #cfd8dc;
    border-radius: 10px;
    box-shadow: 0px 6px 12px rgba(0, 0, 0, 0.08); /* Light shadow */
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 0; /* No padding around card */
    margin-bottom: 20px;
}

.card:hover {
    transform: translateY(-5px); /* Lift effect */
    box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.15); /* Stronger shadow on hover */
}

/* Adjusted Card Image Styling */
.gallery-img {
    width: 100%;
    height: 180px;
    object-fit: cover;
    border-radius: 10px 10px 0 0; /* Rounded top corners only */
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    margin-bottom: 0; /* No bottom margin */
}

.card:hover .gallery-img {
    transform: scale(1.05); /* Zoom effect on hover */
    box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.25); /* Subtle shadow on hover */
}

/* Card Content */
.card-title {
    font-weight: bold;
    font-size: 1.1rem;
    color: #00695c; /* Dark teal for titles */
    text-align: center;
    margin-top: 15px;
}

.card-body {
    padding: 20px;
    text-align: center;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

/* Footer */
footer {
    background-color: #00695c;
    color: #ffffff;
    text-align: center;
    padding: 25px;
    font-size: 0.9em;
    margin-top: 40px;
    box-shadow: 0px -2px 5px rgba(0, 0, 0, 0.1); /* Shadow above footer */
}

/* Responsive Design */
@media (max-width: 768px) {
    .navbar-nav {
        flex-direction: column;
        text-align: center;
        padding: 10px 0;
    }

    .gallery-section {
        margin-top: 20px;
    }

    .card-body {
        padding: 10px;
    }
}

@media (max-width: 480px) {
    .header-section h3 {
        font-size: 1.5em;
    }

    .header-section p {
        font-size: 1em;
    }
}
```


## OUTPUT:
![Screenshot 2025-05-13 233822](https://github.com/user-attachments/assets/ecf602c2-2074-4e85-bc56-d12aeb1e13eb)



## RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
