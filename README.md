<!-- ==================================================== HEADER ==================================================== -->

<p align="center">
  <h3 align="center"> Hi, there! 👋🏻 </h3>
  <hr />
</p>

<p align="center">
  <img src="https://github.com/arthurgian/arthurgian/blob/main/Images/Arthur.gif" alt="Animated header">
</p>

<!-- ==================================================== ABOUT ME ================================================== -->
 <hr />
 <h3 align="center"> About me 🧑🏻 </h3>
 <hr />

```jsx
import React, { useState, useRef, useMemo, useEffect } from 'react';

const ArthurGian = ({
  city = "Curitiba, BR",
  languages = ["EN", "PT-BR", "ES"],
  role = "Full Stack Developer",
  specialization = "Building Scalable Web Applications",
  interests = ["AI", "Problem Solving"],
  hobbies = ["Hiking", "Reading"],
  education = "Tech System Analysis and Development"
}) => {
  const [isAvailable] = useState(true);
  const profileRef = useRef(null);

  const weakness = useMemo(() => {
    return "Shyness (overcome with pair programming)";
  }, []);
  
  useEffect(() => {
    console.log("Component ArthurGian mounted!");
    if (profileRef.current) {
      profileRef.current.focus();
    }
  }, []);

  return (
    <div className="developer-profile" ref={profileRef}>
      <h1>ArthurGian Component</h1>
      
      <div className="status-indicator">
        {isAvailable && <div className="availability-badge">🟢 Available for opportunities</div>}
      </div>

      <div className="props-renderer">
        <p>📍 Location: {city}</p>
        <p>🗣️ Languages: {languages.join(' | ')}</p>
        <p>💼 Role: {role}</p>
        <p>🚀 Specialization: {specialization}</p>
        <p>⚡ Main Strength: Adaptability</p>
        <p>⚠️ Working On: {weakness}</p>
      </div>

      <div className="call-to-action">
        <p>💡 {profileRef.current && "Profile loaded and focused!"}</p>
        {interests.map(interest => (
          <span key={interest} className="interest-tag">#{interest}</span>
        ))}
      </div>

      {/*
        * @version 2.1.1 - Hooks edition
        * @component
        * @example
        * <ArthurGian 
        *   collaboration={true}
        *   contact="🔍 See contact cards" 
        * />
        */}
    </div>
  );
};

export default React.memo(ArthurGian);
```
<hr />

<!-- ==================================================== TECHNOLOGIES ================================================== -->

<h3 align="center">Technologies 🤖</h3>
<div align="center">
  <hr />
</div>
<table width="100%" border="0" align="center">
  <tr>
   <td width="270px" align="center">
         <h3 align="center">Programming Languages</h3>
   </td>
   <td width="300px" align="center">
         <h3 align="center">Front-end</h3>
   </td>
   <td width="300px" align="center">
         <h3 align="center">Back-end</h3>
   </td>
   <td width="300px" align="center">
         <h3 align="center">Tools</h3>
   </td>
     </tr>
</table>
<hr />
<table width="100%" border="0" align="center">
  <tr>
    <td width="25%" align="center">
      <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
      <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" />
      <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAyCAYAAAAeP4ixAAAACXBIWXMAAAsTAAALEwEAmpwYAAAEnUlEQVR4nN2aa4hVVRTHf46ZTZlmjpmGpSkkmekQiOUHH4WvUUtLEissCLEs9YNlmIlPFDH90JT0UrGH4SPoaVKhMKZM5iNfUGaTQmmELyIp0xlZ9T+w2Jx7vTP34bnzh8Wce/e55+y1115r/dfaA4VHFxoJngaupxFgPvAEjQA7gbcpcowG6oB1FDG6AH9IkaUUKToDP0kJk+EUIXoBvzklDgFNKTKMAM44JWqBYWnubwm0IkFoAswCLjglTBYG990CPAt8BNQALwLNSAhKgbWBAnWabInuGQR85cb2Aj1JEG4AqmOUqAJaAG2Bz4OxV4HmJAitgN0xSmwFrgV6BE7/L/AMCcMVwOYYJXbIgU2Ouu/PAkNIICbFKPGDtpJhTjA2loTi22Cip5QEIxxyY7b9EovfA0UmurGrlD+isU0kGNVuouc0+QiWF8678T/lM4nEZDfRkzHjVYHF5pFQtA62V3kw3j9Q5C+gPQnFg26i78WMrwmUWUyCscwlu07BWBlwzCnyIwlGiaxhE30lZnyCU8SKLJKuzDJl79AqHZ0ixrmKAlOBDcF3d7oQ3YfLiBbAUOA54DXR9fWqKcpjKj8rou5yn1fIUg+neUd3oFK5qUpb1Fh1TmBb4gPgb7c1TgNPBskvDlENMgp4C+ia4r6rRefNUo8HSfZwrirH72NIYY0S4VCtusltwK3iWW113VOTG6Z20COy4AJglQqs75RrCBjBJ+59tguyxuoYRXIlXwIdUry3j7tvXa5q8JHAu6LnngRmKpZbflWh9SYwDRisZ6fCfblWJISRvtuBB4Dpyg9erN64XxMpFx2JfKU+WOQUmZ0HPf7L0u8ojN6bjxfwf6Q65ayZKkg0GFeKXkQr9bPaOH2Bdims11nWmaDIZb8/APRL8Y4S4DP3jhfIU7vnaAb+EK1mOqmVv9jiRGiiHBU9x3wpb7BVngnsb2CkOg68r8Toi6zm+t4aexvFBAqGG4EKYArwMvC6KPtaEchKFVKWOwa6hkSIa4AZsoDln4LCItIXoueZtDrtyO0xMYKGRLG8oGPQoN4ri0x1YXiamPB6dVJ8/tmqEF4wlAH3KGeM1bU55N05yOq7UkS6COmSZb22zaeKHL7Wrtaeby1n3VPPyR9UVBqUwURXZusvA0S3/QRmKPTGoY1aoE8pmi2SzBPZGycLmnUzxXVi2F9no0hlTLwvZCTp6rqXW7J50EDRD6+Mrc5L+aAKLvwOUej+xzXzsq4kK4Kuh5dflCfmqj06XD7VLk0YbibyeIeoyWhFuDeAbW7ydZKPgW7BM0pj6paMUKpEti3mGC1TORuE6XRSo35X2OCLDlX3aIGzgq32QzoH3KTj5nAVM5VzIo4WFZcorN+c4r29RFvO629eYNn5JpWz/ZVrxkgsIY7XdYXGu4ueXyrslgGPijXUajcszeWxdol6VSMUagcon2SLTlJ2pjJ+1L2/oEPU3uQRLWWB5fKhfaq/VyuHTHcyRRZ6Xj5gNcmH+t3pmG33jX4XNvgKAlPMopH9P5ZxLlvJ7fKFEzpuMJZgfmXXR0RRrFNii2HHd7b9LAzXGxcBVJvnR5MMWnsAAAAASUVORK5CYII=" alt="java-coffee-cup-logo--v1&logoColor=white" />
      <img src="https://img.shields.io/badge/Ruby-CC342D?style=for-the-badge&logo=ruby&logoColor=white" />
      <img src="https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white" />
    </td> 
    <td width="25%" align="center">
      <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" />
      <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" />
      <img src="https://img.shields.io/badge/Sass-CC6699?style=for-the-badge&logo=sass&logoColor=white" />
      <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
      <img src="https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white" />
      <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" />
      <img src="https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white" />
      <img src="https://img.shields.io/badge/styled--components-DB7093?style=for-the-badge&logo=styled-components&logoColor=white" />
      <img src="https://img.shields.io/badge/Material--UI-0081CB?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAwCAYAAABXAvmHAAAACXBIWXMAAAsTAAALEwEAmpwYAAAC2klEQVR4nO2ZsWvbQBSHf3VJa5sOLsWQwUOnDo4Ht/bgoVgYvScJTJaC/oXsnTJ6zZQ9czdD1w7dOmXzlCVToYXWmJYOhRKCbZVrJao4lnwn3ckp+IObIsXvO6F7Pz8DO3bs+P8hoqnjOJ0tltAE8Dnz3cwcMPPScZw3AO6hWE4BLAAECvfUAYxXBf4sIvpORC9hnhcApmHh0ZLBBzC7cX1cIHoazPzW9/37BgovATgDsFwpPpDc9dvXrxGI1sS27ecaiz8AcL6m8GCDQHzXlQTEumbmE8/zHuYofA/AMYCrlOKDlPvTr98gEL0bF0TUy1C8eIKTDYUHxgVCiQURnVmW9Uii8AqAEwBzyeID4wIxkY+O43DKB/YBXCoUHigKzML3IptAbI1t234S+6BaygmjS2Acnkj/SNnpuYTElJnFbhyG3XRTkYuMArMbuy4jII5QcZTKPA3JHb4A0MsgML616zIC4m+dTmePiI6J6CqHwHX4QkdHsapAOmkCEa7rHjDzeQYBcYSuNsPiBQSj0ajkOM4RM/+UEPgVNq91cWQ7AhGu6z4lovcpAh8APEMyeQXqiWlURiB2n8/M32ICPwAcSUTyPAK+TBqVEhBYlrUvkisAsfYl02gWgbpyGoV+ik2j0IfxNHpIRF8MCZhPo4LhcPhYJE2NAippdJYYE/4iLxx/GjmKV0mjYwDxQJhPQOB5Xl0kzQyFq6TRT2K/JP+v3saXgEoaFZIyX4qKE2i320G5XJZNoyqUChEQ78xgMAgajYZMGjXdN9SJn17dbjeoVqtpadR031BnzZehoNVqvWs2mw+20DfU0TAcq2jsG1oFZIZjfc19Q7tA0nCsZqhvqENEr5j5q4TEnIhODfeNbFiWVQvz1FLzFKNYmLnPzJcapxjF0+v1KuLFTRqOpRQ/ydA3zJE0HFOcYmyXdcMxxSnG3SA+HFOcYtwdxO9uzPxaYYqxYwcM8hsw6utur+DIuAAAAABJRU5ErkJggg==" alt="material-ui">
      <img src="https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white" />
    </td>
    <td width="25%" align="center">
      <img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white" />
      <img src="https://img.shields.io/badge/Ruby_on_Rails-CC0000?style=for-the-badge&logo=ruby-on-rails&logoColor=white" />
      <img src="https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white" />  
    </td>
    <td width="25%" align="center">
      <img src="https://img.shields.io/badge/Opencv-8b1df2?style=for-the-badge&logo=Opencv&logoColor=white" />
      <img src="https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white" />
      <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" />
      <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" />
      <img src="https://img.shields.io/badge/Firebase-F29D0C?style=for-the-badge&logo=firebase&logoColor=white" />
      <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
      <img src="https://img.shields.io/badge/Git-E34F26?style=for-the-badge&logo=git&logoColor=white" />
      <img src="https://img.shields.io/badge/Windows-017AD7?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB4AAAAeCAYAAAA7MK6iAAAACXBIWXMAAAsTAAALEwEAmpwYAAAAm0lEQVR4nO3WIQpCQRCA4Q88gc3oHYw2b2Cw2jyBwWx6NxDsFm8geACLxeoBLILJYlqTYHq4zxUV5oeJM/+yDDND8Me00cMIMyyxxamUYIgpFtjgiBtSTRR5dZ0gW3zA9cXkouKUkRziFF8tmit4IgZIipEprx9iO/3eIfCggz7GmGOFHc6fFn/t2GtKC10MMEGFNfa4NK4aeIM7YtebsFbY06oAAAAASUVORK5CYII=" alt="windows-10">
      <img src="https://img.shields.io/badge/Linux-E34F26?style=for-the-badge&logo=linux&logoColor=black" />
    </td>
  </tr>
</table>

<p align="center">
  <hr />
</p>

<!-- ==================================================== PROFESSIONAL EXPERIENCE ========================================== -->

<h3 align="center">Professional Experience 💼</h3>
  <hr />


<img align="left" height="94px" width="94px" alt="Warpnet" src="https://www.go44.co/wp-content/uploads/logo-1.png"/>

**Full Stack Developer (Jr)** \
[**Go44 - Transformação Digital**](https://www.go44.co/) • Full-time \
Languages & Technologies: `Ruby`, `React`, `Typescript`, `JavaScript`, `Cypress`, `Styled Components`\
Projects: [Platform](https://www.go44.co/a-plataforma/)
<br/>

> [!TIP]
> Please, find me in [LinkedIn](https://www.linkedin.com/in/iuricode/) for a more detailed information about professional experiences, education and certifications.
  <hr />
<!-- ==================================================== STATISTICS ========================================== -->

<h3 align="center">GitHub Status 📊</h3>
<div align="center">
  <hr />
</div>

<table border="0" align="center">
  <tr>
    <td width="50%" align="center">
      <img align="center" src="https://github-readme-stats-anuraghazra1.vercel.app/api/top-langs/?username=arthurgian&theme=dark&hide_border=true&no-bg=true&no-frame=true&langs_count=10"/>
    </td> 
    <td width="50%" align="center">
      <img title="Mark Streak" alt="Mark streak" src="https://github-readme-streak-stats.herokuapp.com/?user=arthurgian&theme=dark&hide_border=true" />
      <img align="center" src="https://github-readme-stats.anuraghazra1.vercel.app/api?username=arthurgian&show_icons=true&include_all_commits=true&theme=dark&hide_border=true&no-bg=true&no-frame=true" />
    </td>
  </tr>
</table>

<p align="center">
  <hr />
</p>

<!-- ==================================================== CONTACT ================================================ -->

<img align="right" height="170px" alt="GIF" src="https://github.com/arthurgian/arthurgian/blob/main/Images/Bat.gif" /> 

<h3 align="center"> Contact me! 👨‍💻</h3>
<div align="center">
  <hr />
</div>
<div align=center>
<p align="center">
  <a href="https://www.instagram.com/arthxr.rar/">
    <img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram">
  </a>&nbsp;
  
  <a href="https://www.linkedin.com/in/arthur-gian/">
    <img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAwCAYAAABXAvmHAAAACXBIWXMAAAsTAAALEwEAmpwYAAABaUlEQVR4nO2WP46CUBCHR4sNCQY6LmBiQWn9jMTGU3gHrkCzewAvwQXsrHC3t0VbXCtiS0H4bSQUy5/dFbKRIZkvmYp5j/kyj8cQCYIgcOWDiMAk3rsIgFm0Jl/YNyQCPUPSgQphGGKxWEDXdSilcDqdMKgOKKVKt8NyuRyWgK7rJYHJZDIsATX0DoRhmEvcO+E4Ds7n87AEng2JQIWmOeWR51EUwXVd2LYNTdNgmmZ+FLfbLZIkqb6Gl8DxeIRlWT8OavP5HNfrla/AdDr9c9p0HAdZlvEUeDR2ux1PgfF4nJ///X4P3/exWq0a8zabDU8Bz/NKOWmaYr1e1/JmsxlPgTiOa/sEQVDLMwyDn8BoNEITt9vtodzeBZr2aJNLIlBBOvANkiP0O/IRk9xCkGsUfUP//SMTgWd34HA4oC+C8sTaTYBRtOaTQdEo4tK+fKI3BoWjiNcuAi+FxKXHwqOi+HstgiBQnS/HmtjvrXCGLAAAAABJRU5ErkJggg==" alt="linkedin">
  </a>&nbsp;
  
  <a href="arthur.ogian.kontakt@gmail.com">
    <img src="https://img.shields.io/badge/gmail-%23D14836.svg?&style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>
</p>

</div>


  <hr />



