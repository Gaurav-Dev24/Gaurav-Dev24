# 🚀 Web Developer 

## 👋 Hello, I'm Gaurav Dev!

I am a passionate web developer with 1 year of experience in building responsive, interactive, and modern web applications using React, JavaScript, and Tailwind CSS. My mission is to create visually appealing and user-friendly web solutions that enhance user experience and meet business goals.

## 🌟 About Me

- 🌐 **Website:** [Portfolio](https://gdev-portfolio.netlify.app/)
- 💼 **LinkedIn:** [LinkedIn](https://www.linkedin.com/in/gaurav-dev-031a65141/)
- 📧 **Email:** [subhamkr1995dob@gmail.com]

### 🛠️ Technical Skills

- **Frontend:** React, JavaScript (ES6+), HTML5, CSS3, Tailwind CSS
- **State Management:** Redux, Context API
- **Tools & Platforms:** Git, GitHub, VSCode, Netlify, Vercel
- **UI/UX:** Responsive Design, Figma, Adobe XD

## 💼 Projects

### 1. **[Shopping Cart]**

- **Description:** A Shopping Cart, using context API for state management.
- **Tech Stack:** React, JavaScript, Tailwind CSS
- **Features:** Responsive design, dynamic content, API integration, State Management
- **Demo:** [Live Demo](https://gdev-shopping-cart.netlify.app/)
- **Code:** [GitHub Repository](https://github.com/Gaurav-Dev24/Shopping-Cart-Project)

```javascript
import React, { useState, useEffect } from 'react';
import axios from 'axios';
import './App.css';

function App() {
  const [data, setData] = useState([]);

  useEffect(() => {
    axios.get('https://api.example.com/data')
      .then(response => setData(response.data))
      .catch(error => console.error('Error fetching data:', error));
  }, []);

  return (
    <div className="container mx-auto p-4">
      <h1 className="text-4xl font-bold text-center">My Project</h1>
      <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 mt-4">
        {data.map(item => (
          <div key={item.id} className="card p-4 shadow-lg rounded-lg hover:bg-gray-100 transition duration-300">
            <h2 className="text-2xl font-semibold">{item.title}</h2>
            <p>{item.description}</p>
          </div>
        ))}
      </div>
    </div>
  );
}

export default App;

