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


2.

$text = 'Join with yellowfish';  

$vowels = ['a','e','i','o','u','A','E','I','O','U'];

$pigLatinText = $this->toPigLatin($text,$vowels);

$reversePigLatin = $this->reversePigLatin($pigLatinText,$vowels);

echo $text,$pigLatinText,$reversePigLatin;

public function toPigLatin($text,$vowels) // to pig latin
{
    $words = explode(" ", $text);

    $pigLatin = [];

    foreach ($words as $word) {

        $firstLetter = substr($word, 0, 1); // 1st letter
        $remainingWord = substr($word, 1); // remaining 

        if (ctype_alpha($word)) { 
            if(in_array($firstLetter,$vowels)){
                $pigLatin[] = $word . 'ay';
            }else{
                $pigLatin[] = $remainingWord . $firstLetter . 'ay';
            }
        } else {
            $pigLatin[] = $word; 
        }
        
    }

    $pigLatinText = implode(" ", $pigLatin);

    return $pigLatinText;
}


public function reversePigLatin($pigLatinText,$vowels) // reverse pig latin
{
    
    $words = explode(" ", $pigLatinText);

    $reversed = [];

    foreach ($words as $word) {

        $initial = substr($word, -3, 1);  // 3rd last
        $last2letter = substr($word, -2); // ay

        $vowelSuffix = substr($word, 0, -2); // remove last 2
        $consonantSuffix = substr($word, 0, -3); // remove last 3

        if(ctype_alpha($word) && $last2letter === 'ay'){
            if(in_array($initial,$vowels)){
                $reversed[] = $vowelSuffix;
            }else{
                $reversed[] = $initial.$consonantSuffix;
            }
        }else{
            $reversed[] = $word;
        }
    }

    $pigLatinBack = implode(" ", $reversed);

    return $pigLatinBack;
}



3.

$k = 2;
$arr = [1, 2, 3, 4, 5, 6];

$result = $this->rotateArray($arr, $k);

echo $result;

public function rotateArray($arr, $k) { 
    $n = count($arr);
    $k = $k % $n; 

    $arr = $this->reverse($arr, 0, $k - 1); // reverse first k 
    $arr = $this->reverse($arr, $k, $n - 1); // reverse remaining
    $arr = $this->reverse($arr, 0, $n - 1); // reverse whole

    return $arr; 
}

public function reverse($arr, $start, $end) { 
    while ($start < $end) {
        list($arr[$start], $arr[$end]) = [$arr[$end], $arr[$start]];
        $start++;
        $end--;
    }
    return $arr; 
}