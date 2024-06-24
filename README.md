<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Contact Page</title>
  <script>
    function validateForm() {
      let fullName = document.getElementById("FullName").value;
      let email = document.getElementById("Email").value;
      let phoneNumber = document.getElementById("number").value;
      let subject = document.getElementById("subject").value;
      let message = document.getElementById("Address").value;

      if (fullName === "") {
        alert("Please enter your full name");
        return false;
      }

      if (email === "") {
        alert("Please enter your email address");
        return false;
      }

      if (!validateEmail(email)) {
        alert("Invalid email address");
        return false;
      }

      if (phoneNumber === ""||phoneNumber.length<10) {
        alert("Please enter a valid phone number");
        return false;
      }

      if (subject === "") {
        alert("Please enter a subject");
        return false;
      }

      if (message === "") {
        alert("Please enter a message");
        return false;
      }

      return true;
    }

    function validateEmail(email) {
      const re = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;
      return re.test(email);
    }
  </script>
</head>
<body>
  <h2 style="color: brown; font-style: italic;">CONTACT US</h2>

  <h3 style="color: indianred;">Address:</h3>
  <p>SDM College of Engineering and Technology,
  Kalaghatagi Road, Dharwad 580002</p>
  <P> Tel-No: 0836–2447465</P>
  <p>Helpline: (0836) 2255619/2464699</p>
  Management Quota: 9611637191
  CET/COMED-K: 7019853531
  <p>Email:principal@sdmcet.ac.in</p>

  <form action="Verifylogin.php" method="post" onsubmit="return validateForm()">
    <img src="C:\Users\siris\OneDrive\Pictures\download (2).jpg" style="float: left;">
    <h3 style="color: brown; font-style: italic;"> Fill the below form to get in touch 
    with us: </h3>
    <table>
      <tr>
        <td>
          <td><input type="text" id="FullName" placeholder="Full Name:" 
          required/></td>
        </td>
      </tr>
      <tr>
        <td>
          <td><input type="email" id="Email" placeholder="E-mail Address:" 
          required/></td>
        </td>
      </tr>
      <tr>
        <td>
          <td><input type="number" id="number" placeholder="Phone Number:" 
          required/></td>
        </td>
      </tr>
      <tr>
        <td>
          <td><input type="text" id="subject" placeholder="Subject:" 
          required/></td>
        </td>
      </tr>

      <tr>
        <td>
          <td><textarea type="text" id="Address" 
          placeholder="Message:"></textarea></td>
        </td>
      </tr>
    </table>
    <p>
      <td><input type="submit" value="Submit" name="btnsubmit" style="color: 
      brown; "></td>
    </p>
  </form>
  <p>
    <a href="MainPage.html">Back</a>
  </p>
</body>
</html>
