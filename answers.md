## About You.

1. 
I am Fathima Thahasim U, a Full Stack Developer with 1.3 years of experience in Laravel PHP and front-end technologies like HTML, CSS, JavaScript, jQuery, and AJAX. I hold a Master's degree in Computer Application (MCA). My experience includes working on multi-vendor eCommerce platforms, procurement systems, HRMS software, and job management systems. I've also developed third-party API integrations, including Razorpay (payment gateway), Google APIs, and Ecom Express (delivery service).

2. 
OS - Windows 11
IDE - Visual Studio Code(VS Code)
Git - Code Management
MySQL - Database 
Xampp - Local server
Postman & ApiDog - API testing

3.
PHP - Laravel 
JavaScript - jQuery, AJAX
SQL - MySQL
Node.js - for frontend dependencies with npm

4. 
Interested to learn other PHP frameworks like CodeIgniter, Yii. Also frontend frameworks like React.js, Vue.js


## Social Profile

1. Git profile URL - https://github.com/Fthahasim

2. LinkedIn profile - https://www.linkedin.com/in/fathima-thahasim-u

3. NIL


## The Real Stuff

1.

function getArray($num){

    $length = strlen($num);

    $const = 10 ** ($length - 1);
    
    $arr = [];

    while( $num>0 )
    {

        $extracted = (int)($num / $const); 

        $arr[] = $extracted; 

        $num = $num % $const; 

        $const /= 10;  
        
    }

    return $arr;

}






