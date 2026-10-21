
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<meta name="description"
content="COSIS Township Lahore - College of Sharia and Islamic Sciences">

<title>COSIS Township Lahore | College of Shariah & Islamic Sciences</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Inter:wght@300;400;500;600;700;800&display=swap"
rel="stylesheet">

<style>

/* =========================================================
   ROOT
========================================================= */

:root{
    --green:#0c5135;
    --dark-green:#063524;
    --deep-green:#03291d;
    --gold:#c79a35;
    --light-gold:#ead18a;
    --cream:#f8f7f2;
    --white:#ffffff;
    --gray:#68736d;
    --light-green:#eef5f0;
    --border:#e4e9e5;
    --shadow:0 20px 60px rgba(0,0,0,.10);
}

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:"Inter",sans-serif;
    background:var(--cream);
    color:#17251d;
    line-height:1.6;
    overflow-x:hidden;
}

body::selection{
    background:var(--gold);
    color:white;
}

a{
    text-decoration:none;
}

img{
    max-width:100%;
    display:block;
}

button,
input,
textarea,
select{
    font-family:inherit;
}

/* =========================================================
   SCROLL PROGRESS
========================================================= */

.scroll-progress{
    position:fixed;
    top:0;
    left:0;
    height:4px;
    width:0%;
    background:linear-gradient(90deg,var(--gold),var(--light-gold));
    z-index:99999;
}

/* =========================================================
   NAVBAR
========================================================= */

nav{
    height:82px;
    padding:0 7%;
    background:rgba(255,255,255,.94);
    backdrop-filter:blur(18px);
    -webkit-backdrop-filter:blur(18px);

    display:flex;
    justify-content:space-between;
    align-items:center;

    position:sticky;
    top:0;
    z-index:1000;

    border-bottom:1px solid rgba(199,154,53,.12);
    box-shadow:0 5px 30px rgba(0,0,0,.06);

    animation:navDrop .8s ease;
}

@keyframes navDrop{
    from{
        opacity:0;
        transform:translateY(-30px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}

.brand{
    display:flex;
    align-items:center;
    gap:14px;
}

.logo{
    width:55px;
    height:55px;
    border-radius:50%;
    background:white;
    border:2px solid rgba(199,154,53,.25);
    padding:4px;
    display:flex;
    align-items:center;
    justify-content:center;
    overflow:hidden;
    box-shadow:0 8px 25px rgba(12,81,53,.12);
    animation:logoFloat 3s ease-in-out infinite;
}

.logo img{
    width:100%;
    height:100%;
    object-fit:contain;
    border-radius:50%;
}

@keyframes logoFloat{
    0%,100%{transform:translateY(0)}
    50%{transform:translateY(-5px)}
}

.brand-text strong{
    display:block;
    color:var(--green);
    font-size:12px;
    letter-spacing:.7px;
}

.brand-text span{
    color:#777;
    font-size:11px;
}

nav ul{
    display:flex;
    gap:27px;
    list-style:none;
    align-items:center;
}

nav ul a{
    position:relative;
    color:#26342d;
    font-size:14px;
    font-weight:600;
    transition:.3s;
}

nav ul a:not(.admission-btn)::after{
    content:"";
    position:absolute;
    left:0;
    bottom:-8px;
    width:0;
    height:2px;
    background:var(--gold);
    transition:.3s;
}

nav ul a:hover{
    color:var(--gold);
}

nav ul a:hover::after{
    width:100%;
}

.admission-btn{
    background:linear-gradient(135deg,var(--gold),#a97d1e);
    color:white!important;
    padding:12px 20px;
    border-radius:6px;
    box-shadow:0 8px 20px rgba(199,154,53,.25);
}

.admission-btn:hover{
    background:var(--green);
    transform:translateY(-2px);
}

.menu-btn{
    display:none;
    font-size:27px;
    color:var(--green);
    cursor:pointer;
}

/* =========================================================
   HERO
========================================================= */

.hero{
    min-height:680px;

    background:
        linear-gradient(
            90deg,
            rgba(3,39,25,.97),
            rgba(7,67,43,.82),
            rgba(5,54,35,.62)
        ),
        url("./oipnjc.jpg");

    background-size:cover;
    background-position:center;

    display:flex;
    align-items:center;

    color:white;
    padding:100px 7%;

    position:relative;
    overflow:hidden;
}

.hero::before{
    content:"";
    position:absolute;
    width:600px;
    height:600px;
    border:1px solid rgba(234,209,138,.18);
    border-radius:50%;
    right:-230px;
    top:30px;
    animation:circleRotate 15s linear infinite;
}

.hero::after{
    content:"";
    position:absolute;
    width:350px;
    height:350px;
    border:1px solid rgba(234,209,138,.12);
    border-radius:50%;
    right:-100px;
    top:160px;
    animation:circleRotate 10s linear infinite reverse;
}

@keyframes circleRotate{
    from{transform:rotate(0deg)}
    to{transform:rotate(360deg)}
}

.hero-content{
    max-width:850px;
    position:relative;
    z-index:2;
    animation:heroReveal 1.2s ease;
}

@keyframes heroReveal{
    from{
        opacity:0;
        transform:translateX(-70px);
    }
    to{
        opacity:1;
        transform:translateX(0);
    }
}

.hero-label{
    color:var(--light-gold);
    text-transform:uppercase;
    letter-spacing:4px;
    font-size:17px;
    font-weight:700;
    margin-bottom:20px;
}

.hero h1{
    font-family:"Amiri",serif;
    font-size:clamp(50px,7vw,82px);
    line-height:1.05;
    margin-bottom:22px;
}

.hero h1 span{
    background:linear-gradient(
        90deg,
        white,
        var(--light-gold)
    );
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
}

.hero p{
    max-width:680px;
    color:#e4ebe7;
    font-size:18px;
    line-height:1.9;
    margin-bottom:35px;
}

.hero-buttons{
    display:flex;
    gap:14px;
    flex-wrap:wrap;
}

.btn{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    padding:14px 27px;
    border-radius:6px;
    font-weight:700;
    transition:.35s;
    position:relative;
    overflow:hidden;
}

.btn-primary{
    background:linear-gradient(
        135deg,
        var(--gold),
        #a97d1e
    );
    color:white;
    box-shadow:0 10px 30px rgba(199,154,53,.25);
}

.btn-primary:hover{
    transform:translateY(-4px);
    background:white;
    color:var(--green);
    box-shadow:0 15px 35px rgba(0,0,0,.18);
}

.btn-outline{
    border:1px solid rgba(255,255,255,.55);
    color:white;
    background:rgba(255,255,255,.03);
    backdrop-filter:blur(10px);
}

.btn-outline:hover{
    background:white;
    color:var(--green);
    transform:translateY(-4px);
}

/* =========================================================
   QUICK INFO
========================================================= */

.quick-info{
    margin:-50px auto 0;
    position:relative;
    z-index:5;
    width:86%;

    display:grid;
    grid-template-columns:repeat(3,1fr);

    background:rgba(255,255,255,.95);
    backdrop-filter:blur(15px);

    box-shadow:0 20px 60px rgba(0,0,0,.12);
    border-radius:12px;
    overflow:hidden;

    border:1px solid rgba(255,255,255,.7);
}

.quick-item{
    padding:30px;
    display:flex;
    gap:18px;
    align-items:center;
    border-right:1px solid #eee;
    transition:.4s;
}

.quick-item:last-child{
    border-right:none;
}

.quick-item:hover{
    background:#f4f8f5;
    transform:translateY(-5px);
}

.quick-icon{
    width:55px;
    height:55px;
    flex-shrink:0;
    display:flex;
    align-items:center;
    justify-content:center;
    border-radius:50%;
    background:#edf5ef;
    font-size:27px;
    transition:.4s;
}

.quick-item:hover .quick-icon{
    background:var(--gold);
    transform:scale(1.1) rotate(8deg);
}

.quick-item h4{
    color:var(--green);
    margin-bottom:4px;
}

.quick-item p{
    color:var(--gray);
    font-size:13px;
}

/* =========================================================
   GENERAL SECTION
========================================================= */

section{
    padding:105px 7%;
}

.section-heading{
    text-align:center;
    margin-bottom:55px;
}

.section-heading small{
    color:var(--gold);
    text-transform:uppercase;
    letter-spacing:3px;
    font-weight:700;
    font-size:11px;
}

.section-heading h2{
    color:var(--green);
    font-family:"Amiri",serif;
    font-size:48px;
    margin-top:8px;
}

.section-heading p{
    max-width:650px;
    margin:10px auto 0;
    color:var(--gray);
}

/* =========================================================
   ABOUT
========================================================= */

#about{
    position:relative;
}

.marquee{
    background:linear-gradient(
        135deg,
        var(--dark-green),
        var(--green)
    );
    color:var(--light-gold);
    padding:25px 10px;
    overflow:hidden;
    white-space:nowrap;
    font-size:38px;
    margin:40px auto;
    border-radius:12px;
    box-shadow:0 15px 40px rgba(6,53,36,.18);
}

.marquee-text{
    display:inline-block;
    animation:marqueeMove 15s linear infinite;
}

@keyframes marqueeMove{
    from{transform:translateX(100%)}
    to{transform:translateX(-100%)}
}

/* =========================================================
   CAROUSEL
========================================================= */

.carousel{
    width:1000px;
    max-width:100%;
    margin:45px auto 60px;
    position:relative;
    overflow:hidden;
    height:550px;
    border-radius:18px;
    box-shadow:0 25px 70px rgba(0,0,0,.18);
    background:#063524;
}

.slides{
    display:flex;
    height:100%;
    transition:transform .7s cubic-bezier(.77,0,.18,1);
}

.slides img{
    width:100%;
    height:100%;
    flex-shrink:0;
    display:block;
    object-fit:cover;
}

.carousel button{
    position:absolute;
    top:50%;
    transform:translateY(-50%);
    width:52px;
    height:52px;
    border:none;
    border-radius:50%;
    background:rgba(0,0,0,.38);
    backdrop-filter:blur(10px);
    color:white;
    font-size:24px;
    cursor:pointer;
    z-index:5;
    transition:.3s;
}

.carousel button:hover{
    background:var(--gold);
    transform:translateY(-50%) scale(1.1);
}

.prev{
    left:20px;
}

.next{
    right:20px;
}

.carousel-dots{
    position:absolute;
    bottom:18px;
    left:50%;
    transform:translateX(-50%);
    display:flex;
    gap:7px;
    z-index:5;
}

.carousel-dot{
    width:8px;
    height:8px;
    border-radius:50%;
    background:rgba(255,255,255,.5);
    cursor:pointer;
    transition:.3s;
}

.carousel-dot.active{
    width:25px;
    border-radius:10px;
    background:var(--gold);
}

/* =========================================================
   ABOUT CONTENT
========================================================= */

.about-content{
    max-width:1000px;
    margin:auto;
    padding:50px;
    border-radius:18px;
    background:white;
    box-shadow:0 15px 50px rgba(0,0,0,.07);
    border:1px solid var(--border);
}

.about-content h3{
    font-family:"Amiri",serif;
    font-size:40px;
    color:var(--green);
    margin-bottom:18px;
}

.about-content p{
    color:var(--gray);
    margin-bottom:17px;
    line-height:1.9;
}

.check-list{
    margin:25px 0;
    list-style:none;
}

.check-list li{
    margin:13px 0;
    color:#435048;
}

.check-list li::before{
    content:"✓";
    color:var(--gold);
    font-weight:bold;
    margin-right:12px;
}

/* =========================================================
   PROGRAMS
========================================================= */

.programs{
    background:#eef3ef;
    position:relative;
}

.programs::before{
    content:"";
    position:absolute;
    width:300px;
    height:300px;
    border-radius:50%;
    background:rgba(199,154,53,.06);
    top:80px;
    left:-150px;
}

.program-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:25px;
    position:relative;
}

.program-card{
    background:white;
    padding:35px;
    border-radius:12px;
    border:1px solid transparent;
    border-top:4px solid var(--green);
    box-shadow:0 8px 35px rgba(0,0,0,.05);
    transition:.4s;
    position:relative;
    overflow:hidden;
}

.program-card::after{
    content:"";
    position:absolute;
    width:100px;
    height:100px;
    border-radius:50%;
    background:rgba(199,154,53,.06);
    right:-45px;
    bottom:-45px;
    transition:.4s;
}

.program-card:hover{
    transform:translateY(-10px);
    border-color:rgba(199,154,53,.25);
    border-top-color:var(--gold);
    box-shadow:0 25px 55px rgba(0,0,0,.11);
}

.program-card:hover::after{
    transform:scale(2);
}

.program-number{
    color:var(--gold);
    font-weight:800;
    font-size:13px;
    letter-spacing:1px;
}

.program-card h3{
    color:var(--green);
    font-family:"Amiri",serif;
    font-size:28px;
    margin:18px 0 10px;
}

.program-card p{
    color:var(--gray);
    line-height:1.8;
}

.program-link{
    display:inline-block;
    margin-top:22px;
    color:var(--green);
    font-weight:700;
    font-size:13px;
    transition:.3s;
}

.program-link:hover{
    color:var(--gold);
    transform:translateX(5px);
}

/* =========================================================
   QUOTE
========================================================= */

.quote{
    background:
        linear-gradient(
            135deg,
            var(--dark-green),
            var(--green)
        );
    color:white;
    text-align:center;
    padding:110px 20px;
    position:relative;
    overflow:hidden;
}

.quote::before,
.quote::after{
    content:"";
    position:absolute;
    border:1px solid rgba(234,209,138,.15);
    border-radius:50%;
}

.quote::before{
    width:350px;
    height:350px;
    left:-180px;
    top:-150px;
}

.quote::after{
    width:450px;
    height:450px;
    right:-230px;
    bottom:-250px;
}

.quote .arabic{
    font-family:"Amiri",serif;
    color:var(--light-gold);
    font-size:45px;
    margin-bottom:20px;
}

.quote p{
    max-width:800px;
    margin:auto;
    font-family:"Amiri",serif;
    font-size:27px;
    line-height:1.8;
}

/* =========================================================
   WHY COSIS
========================================================= */

.features-section{
    background:white;
}

.feature-grid{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:20px;
}

.feature{
    text-align:center;
    padding:35px 20px;
    background:white;
    border:1px solid #e5e8e5;
    border-radius:12px;
    transition:.4s;
}

.feature:hover{
    border-color:var(--gold);
    transform:translateY(-10px);
    box-shadow:0 20px 45px rgba(0,0,0,.08);
}

.feature-icon{
    width:65px;
    height:65px;
    margin:auto;
    border-radius:50%;
    background:#edf5ef;
    color:var(--green);
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:27px;
    transition:.5s;
}

.feature:hover .feature-icon{
    transform:rotateY(360deg);
    background:var(--gold);
    color:white;
}

.feature h3{
    color:var(--green);
    margin:17px 0 8px;
    font-size:17px;
}

.feature p{
    color:var(--gray);
    font-size:13px;
}

/* =========================================================
   EVENTS
========================================================= */

.events{
    background:#fafafa;
}

.event-list{
    max-width:1000px;
    margin:auto;
}

.event{
    background:white;
    border-left:5px solid var(--gold);
    padding:25px 30px;
    margin-bottom:18px;
    display:grid;
    grid-template-columns:100px 1fr auto;
    gap:25px;
    align-items:center;
    box-shadow:0 5px 20px rgba(0,0,0,.05);
    border-radius:0 10px 10px 0;
    transition:.4s;
}

.event:hover{
    transform:translateX(8px);
    box-shadow:0 20px 40px rgba(0,0,0,.1);
}

.event-date{
    text-align:center;
    color:var(--green);
    font-weight:800;
}

.event-date strong{
    display:block;
    font-size:30px;
    transition:.3s;
}

.event:hover .event-date strong{
    color:var(--gold);
    transform:scale(1.15);
}

.event h3{
    color:var(--green);
    margin-bottom:5px;
}

.event p{
    color:var(--gray);
    font-size:13px;
}

.event-tag{
    color:var(--gold);
    font-size:12px;
    font-weight:700;
}

/* =========================================================
   CTA
========================================================= */

.cta{
    margin:0 7% 100px;
    padding:70px;
    border-radius:18px;
    background:
        linear-gradient(
            135deg,
            var(--dark-green),
            var(--green)
        );
    color:white;
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:30px;
    overflow:hidden;
    position:relative;
    box-shadow:0 25px 60px rgba(6,53,36,.2);
}

.cta::before{
    content:"";
    position:absolute;
    width:350px;
    height:350px;
    border:1px solid rgba(255,255,255,.13);
    border-radius:50%;
    right:-130px;
    top:-150px;
    animation:ctaFloat 7s ease-in-out infinite;
}

@keyframes ctaFloat{
    0%,100%{transform:scale(1)}
    50%{transform:scale(1.2)}
}

.cta h2{
    font-family:"Amiri",serif;
    font-size:42px;
}

.cta p{
    color:#cbd9d1;
    margin-top:8px;
}

/* =========================================================
   CONTACT
========================================================= */

.contact{
    display:grid;
    grid-template-columns:.8fr 1.2fr;
    gap:60px;
}

.contact-info h3{
    color:var(--green);
    font-family:"Amiri",serif;
    font-size:36px;
    margin-bottom:15px;
}

.contact-info > p{
    color:var(--gray);
    line-height:1.8;
    margin-bottom:30px;
}

.contact-item{
    display:flex;
    gap:15px;
    margin:20px 0;
}

.contact-item-icon{
    color:var(--gold);
    font-size:22px;
}

.contact-item strong{
    display:block;
    color:var(--green);
}

.contact-item strong a{
    color:var(--green);
}

.contact-item strong a:hover{
    color:var(--gold);
}

.contact-item span{
    color:var(--gray);
    font-size:14px;
}

.contact-form{
    background:white;
    padding:35px;
    border-radius:14px;
    box-shadow:0 10px 40px rgba(0,0,0,.07);
    transition:.4s;
}

.contact-form:hover{
    transform:translateY(-8px);
    box-shadow:0 20px 50px rgba(0,0,0,.12);
}

.form-row{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:15px;
}

input,
textarea,
select{
    width:100%;
    padding:15px;
    margin-bottom:15px;
    border:1px solid #dfe4e0;
    border-radius:6px;
    outline:none;
    background:#fbfcfb;
    transition:.3s;
}

input:focus,
textarea:focus,
select:focus{
    border-color:var(--gold);
    box-shadow:0 5px 15px rgba(199,154,53,.12);
    transform:translateY(-2px);
}

textarea{
    height:140px;
    resize:vertical;
}

/* =========================================================
   FAQ
========================================================= */

.faq-section{
    background:#eef3ef;
}

.faq-container{
    max-width:900px;
    margin:auto;
}

.faq{
    background:white;
    margin-bottom:12px;
    border-radius:8px;
    overflow:hidden;
    border:1px solid #e3e8e4;
}

.faq-question{
    padding:20px 25px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    cursor:pointer;
    color:var(--green);
    font-weight:700;
}

.faq-question span{
    color:var(--gold);
    font-size:22px;
}

.faq-answer{
    max-height:0;
    overflow:hidden;
    transition:.4s ease;
}

.faq-answer p{
    padding:0 25px 20px;
    color:var(--gray);
    font-size:14px;
}

.faq.active .faq-answer{
    max-height:200px;
}

/* =========================================================
   FOOTER
========================================================= */

footer{
    background:#062d1f;
    color:white;
    padding:65px 7% 25px;
}

.footer-grid{
    display:grid;
    grid-template-columns:1.4fr 1fr 1fr 1fr;
    gap:45px;
    padding-bottom:45px;
}

footer h3{
    color:var(--light-gold);
    margin-bottom:18px;
}

footer p,
footer a{
    color:#aebeb5;
    font-size:13px;
    line-height:1.9;
}

footer a{
    display:block;
    margin:7px 0;
    transition:.3s;
}

footer a:hover{
    color:white;
    padding-left:6px;
}

.footer-logo{
    font-family:"Amiri",serif;
    font-size:30px;
    color:var(--light-gold);
    margin-bottom:12px;
}

.copyright{
    border-top:1px solid rgba(255,255,255,.1);
    padding-top:22px;
    color:#8fa096;
    font-size:12px;
    text-align:center;
}

/* =========================================================
   SCROLL TOP
========================================================= */

#scrollTop{
    position:fixed;
    right:25px;
    bottom:25px;
    width:50px;
    height:50px;
    border-radius:50%;
    background:var(--gold);
    color:white;
    border:none;
    font-size:22px;
    cursor:pointer;
    z-index:9999;
    opacity:0;
    visibility:hidden;
    transform:translateY(20px);
    transition:.4s;
    box-shadow:0 8px 25px rgba(0,0,0,.2);
}

#scrollTop.show{
    opacity:1;
    visibility:visible;
    transform:translateY(0);
}

#scrollTop:hover{
    background:var(--green);
    transform:translateY(-5px);
}

/* =========================================================
   REVEAL ANIMATION
========================================================= */

.reveal{
    opacity:0;
    transform:translateY(45px);
    transition:all .8s ease;
}

.reveal.show{
    opacity:1;
    transform:translateY(0);
}

/* =========================================================
   RESPONSIVE
========================================================= */

@media(max-width:950px){

    nav ul{
        display:none;
    }

    .menu-btn{
        display:block;
    }

    nav ul.mobile-open{
        display:flex;
        position:absolute;
        top:82px;
        right:0;
        width:100%;
        background:white;
        padding:25px;
        flex-direction:column;
        gap:20px;
        box-shadow:0 20px 30px rgba(0,0,0,.1);
    }

    .quick-info{
        grid-template-columns:1fr;
    }

    .quick-item{
        border-right:none;
        border-bottom:1px solid #eee;
    }

    .quick-item:last-child{
        border-bottom:none;
    }

    .program-grid{
        grid-template-columns:1fr 1fr;
    }

    .feature-grid{
        grid-template-columns:1fr 1fr;
    }

    .contact{
        grid-template-columns:1fr;
    }

    .footer-grid{
        grid-template-columns:1fr 1fr;
    }

    .cta{
        flex-direction:column;
        align-items:flex-start;
    }
}

@media(max-width:600px){

    nav{
        height:70px;
        padding:0 5%;
    }

    nav ul.mobile-open{
        top:70px;
    }

    .logo{
        width:45px;
        height:45px;
    }

    .brand-text strong{
        font-size:11px;
    }

    .brand-text span{
        font-size:9px;
    }

    .hero{
        min-height:650px;
        padding:90px 6%;
    }

    .hero-label{
        font-size:12px;
        letter-spacing:2px;
    }

    .hero h1{
        font-size:48px;
    }

    .hero p{
        font-size:15px;
    }

    .hero-buttons{
        flex-direction:column;
        align-items:stretch;
    }

    .btn{
        text-align:center;
    }

    .quick-info{
        width:88%;
    }

    section{
        padding:75px 6%;
    }

    .section-heading h2{
        font-size:38px;
    }

    .marquee{
        font-size:25px;
        padding:22px 10px;
    }

    .carousel{
        height:320px;
        border-radius:12px;
    }

    .carousel button{
        width:42px;
        height:42px;
        font-size:18px;
    }

    .prev{
        left:10px;
    }

    .next{
        right:10px;
    }

    .about-content{
        padding:28px;
    }

    .about-content h3{
        font-size:34px;
    }

    .program-grid,
    .feature-grid{
        grid-template-columns:1fr;
    }

    .event{
        grid-template-columns:70px 1fr;
        gap:15px;
        padding:20px;
    }

    .event-tag{
        display:none;
    }

    .form-row{
        grid-template-columns:1fr;
    }

    .cta{
        margin:0 6% 70px;
        padding:40px 25px;
    }

    .cta h2{
        font-size:34px;
    }

    .quote .arabic{
        font-size:30px;
    }

    .quote p{
        font-size:20px;
    }

    .footer-grid{
        grid-template-columns:1fr;
    }
}

/* =========================================================
   REDUCED MOTION
========================================================= */

@media(prefers-reduced-motion:reduce){

    *,
    *::before,
    *::after{
        animation-duration:.01ms!important;
        animation-iteration-count:1!important;
        transition-duration:.01ms!important;
        scroll-behavior:auto!important;
    }
}

</style>
</head>

<body>

<div class="scroll-progress" id="scrollProgress"></div>

<!-- =======================================================
     NAVIGATION
======================================================= -->

<nav>

    <div class="brand">

        <div class="logo">
            <img src="OIP.webp" alt="COSIS Logo">
        </div>

        <div class="brand-text">
            <strong>COSIS TOWNSHIP</strong>

            <span>
                College of Shariah & Islamic Sciences
            </span>
        </div>

    </div>

    <div class="menu-btn" onclick="toggleMenu()">
        ☰
    </div>

    <ul id="navMenu">

        <li>
            <a href="#home">Home</a>
        </li>

        <li>
            <a href="#about">About</a>
        </li>

        <li>
            <a href="#programs">Programs</a>
        </li>

        <li>
            <a href="#events">Events</a>
        </li>

        <li>
            <a href="#contact">Contact</a>
        </li>

        <li>
            <a class="admission-btn"
               href="admission .html">
                Admissions
            </a>
        </li>

    </ul>

</nav>


<!-- =======================================================
     HERO
======================================================= -->

<section class="hero" id="home">

    <div class="hero-content">

        <div class="hero-label">
            College of Shariah & Islamic Sciences
        </div>

        <h1>
            <span>
                Knowledge.<br>
                Character.<br>
                Leadership.
            </span>
        </h1>

        <p>
            Welcome to COSIS Township Lahore — a center
            dedicated to learning, Islamic scholarship,
            character development and the preparation of
            students for meaningful service to society.
        </p>

        <div class="hero-buttons">

            <a href="#programs" class="btn btn-primary">
                Explore Programs
            </a>

            <a href="#contact" class="btn btn-outline">
                Contact Us
            </a>

        </div>

    </div>

</section>


<!-- =======================================================
     QUICK INFORMATION
======================================================= -->

<div class="quick-info">

    <div class="quick-item">

        <div class="quick-icon">
            🎓
        </div>

        <div>
            <h4>Quality Education</h4>

            <p>
                Islamic and academic learning
            </p>
        </div>

    </div>


    <div class="quick-item">

        <div class="quick-icon">
            📚
        </div>

        <div>
            <h4>Islamic Scholarship</h4>

            <p>
                Knowledge rooted in Islamic tradition
            </p>
        </div>

    </div>


    <div class="quick-item">

        <div class="quick-icon">
            🌱
        </div>

        <div>
            <h4>Student Development</h4>

            <p>
                Character, leadership and growth
            </p>
        </div>

    </div>

</div>


<!-- =======================================================
     ABOUT
======================================================= -->

<section id="about">

    <div class="section-heading reveal">

        <small>
            About COSIS
        </small>

        <h2>
            A Center of Learning
        </h2>

        <p>
            Developing knowledgeable, principled and
            capable individuals through education and training.
        </p>

    </div>


    <div class="marquee reveal">

        <div class="marquee-text">
            Welcome to College of shariyah and islamic Sciences Township Lahore
        </div>

    </div>


    <!-- CAROUSEL -->

    <div class="carousel reveal">

        <div class="slides">

            <img src="oipjndhfkfvjn.jpg" alt="Slide 1">

            <img src="oipbghdvybdumd.jpg" alt="Slide 2">

            <img src="oipbg.jpg" alt="Slide 3">

            <img src="oipbgdgd.jpg" alt="Slide 4">

            <img src="puisdkjbhvhr.jpg" alt="Slide 8">

            <img src="oipmhjvbfgbg.jpg" alt="Slide 9">

            <img src="oipnvsdvdsdv.jpg" alt="Slide 10">

            <img src="oipnjc.jpg" alt="Slide 11">
            
            <img src="oipmvgbnhmj.jpg" alt="Slide 12">

        </div>

        <button class="prev"
                onclick="previousSlide()"
                aria-label="Previous slide">
            ❮
        </button>

        <button class="next"
                onclick="nextSlide()"
                aria-label="Next slide">
            ❯
        </button>

        <div class="carousel-dots" id="carouselDots"></div>

    </div>


    <div class="about-content reveal">

        <h3>
            Education With Purpose
        </h3>

        <p>
            The College of Sharia and Islamic Sciences
            (COSIS) is an institution associated with
            Minhaj University Lahore and has a long
            history of Islamic and academic education.
        </p>

        <p>
            The institution seeks to combine Islamic
            scholarship with contemporary educational
            approaches and develop students intellectually,
            spiritually and personally.
        </p>

        <ul class="check-list">

            <li>
                Islamic Studies and Shariah
            </li>

            <li>
                Qur'an and Islamic learning
            </li>

            <li>
                Character and moral development
            </li>

            <li>
                Academic and intellectual growth
            </li>

            <li>
                Leadership and community service
            </li>

        </ul>

        <a href="http://www.cosis.edu.pk/english/index.html"
           target="_blank"
           class="btn btn-primary">

            Visit Official Website

        </a>

    </div>

</section>


<!-- =======================================================
     PROGRAMS
======================================================= -->

<section class="programs" id="programs">

    <div class="section-heading reveal">

        <small>
            Education
        </small>

        <h2>
            Programs & Learning
        </h2>

        <p>
            Explore the areas of learning and training
            offered through COSIS.
        </p>

    </div>


    <div class="program-grid">

        <div class="program-card reveal">

            <div class="program-number">
                PROGRAM 01
            </div>

            <h3>
                Shariah & Islamic Sciences
            </h3>

            <p>
                Study Islamic knowledge, ics and
                related areas of Islamic sciences.
            </p>

            <a href="#contact" class="program-link">
                Learn More →
            </a>

        </div>


        <div class="program-card reveal">

            <div class="program-number">
                PROGRAM 02
            </div>

            <h3>
                Islamic Training Courses
            </h3>

            <p>
                Arabic course and english language
                course and many computer courses
            </p>

            <a href="#contact" class="program-link">
                Learn More →
            </a>

        </div>


        <div class="program-card reveal">

            <div class="program-number">
                PROGRAM 03
            </div>

            <h3>
                Qur'anic Learning
            </h3>

            <p>
                Learning opportunities covering Qur'anic
                understanding, translation, recitation
                and related subjects.
            </p>

            <a href="#contact" class="program-link">
                Learn More →
            </a>

        </div>


        <div class="program-card reveal">

            <div class="program-number">
                PROGRAM 04
            </div>

            <h3>
                Islamic Ethics
            </h3>

            <p>
                Developing character, manners and responsible
                conduct through Islamic teachings.
            </p>

            <a href="#contact" class="program-link">
                Learn More →
            </a>

        </div>


        <div class="program-card reveal">

            <div class="program-number">
                PROGRAM 05
            </div>

            <h3>
                Research & Scholarship
            </h3>

            <p>
                Encouraging academic thinking, research,
                intellectual development and scholarly work.
            </p>

            <a href="#contact" class="program-link">
                Learn More →
            </a>

        </div>


        <div class="program-card reveal">

            <div class="program-number">
                PROGRAM 06
            </div>

            <h3>
                Student Development
            </h3>

            <p>
                Activities and lectures supporting students'
                personal, intellectual and leadership development.
            </p>

            <a href="#contact" class="program-link">
                Learn More →
            </a>

        </div>

    </div>

</section>


<!-- =======================================================
     QUOTE
======================================================= -->

<section class="quote">

    <div class="arabic">
        وَقُلْ رَبِّ زِدْنِي عِلْمًا
    </div>

    <p>
        “And say: My Lord, increase me in knowledge.”
    </p>

</section>


<!-- =======================================================
     WHY COSIS
======================================================= -->

<section class="features-section">

    <div class="section-heading reveal">

        <small>
            Why COSIS
        </small>

        <h2>
            Learning Beyond Books
        </h2>

        <p>
            Building knowledge, character and confidence
            for meaningful service to society.
        </p>

    </div>


    <div class="feature-grid">

        <div class="feature reveal">

            <div class="feature-icon">
                📖
            </div>

            <h3>
                Islamic Learning
            </h3>

            <p>
                Knowledge rooted in Islamic tradition.
            </p>

        </div>


        <div class="feature reveal">

            <div class="feature-icon">
                🎓
            </div>

            <h3>
                Academic Growth
            </h3>

            <p>
                Encouraging intellectual development.
            </p>

        </div>


        <div class="feature reveal">

            <div class="feature-icon">
                🌱
            </div>

            <h3>
                Character Building
            </h3>

            <p>
                Developing responsible and principled individuals.
            </p>

        </div>


        <div class="feature reveal">

            <div class="feature-icon">
                ⭐
            </div>

            <h3>
                Leadership
            </h3>

            <p>
                Preparing students for meaningful service.
            </p>

        </div>

    </div>

</section>


<!-- =======================================================
     EVENTS
======================================================= -->

<section class="events" id="events">

    <div class="section-heading reveal">

        <small>
            Campus Life
        </small>

        <h2>
            News & Events
        </h2>

        <p>
            Keep students and visitors informed about
            educational activities and campus events.
        </p>

    </div>


    <div class="event-list">

        <div class="event reveal">

            <div class="event-date">

                <strong>
                    01
                </strong>

                EVENT

            </div>

            <div>

                <h3>
                    Guest Lecture Series
                </h3>

                <p>
                    Educational talks and sessions featuring
                    distinguished speakers and resource persons.
                </p>

            </div>

            <div class="event-tag">
                EDUCATION
            </div>

        </div>


        <div class="event reveal">

            <div class="event-date">

                <strong>
                    02
                </strong>

                EVENT

            </div>

            <div>

                <h3>
                    Student Training
                </h3>

                <p>
                    Training activities focused on personal,
                    intellectual and spiritual development.
                </p>

            </div>

            <div class="event-tag">
                TRAINING
            </div>

        </div>


        <div class="event reveal">

            <div class="event-date">

                <strong>
                    03
                </strong>

                EVENT

            </div>

            <div>

                <h3>
                    Academic & Award Ceremonies
                </h3>

                <p>
                    Celebrating student achievement and
                    academic excellence.
                </p>

            </div>

            <div class="event-tag">
                CAMPUS
            </div>

        </div>

    </div>

</section>


<!-- =======================================================
     ADMISSIONS CTA
======================================================= -->

<section id="admissions">

    <div class="cta">

        <div>

            <h2>
                Begin Your Educational Journey
            </h2>

            <p>
                Contact COSIS for current admission,
                program and course information.
            </p>

        </div>

        <a href="#contact" class="btn btn-primary">
            Admission Inquiry
        </a>

    </div>

</section>


<!-- =======================================================
     CONTACT
======================================================= -->

<section id="contact">

    <div class="section-heading reveal">

        <small>
            Contact
        </small>

        <h2>
            Get In Touch
        </h2>

        <p>
            Have a question about admissions,
            programs or courses? Send us a message.
        </p>

    </div>


    <div class="contact">

        <div class="contact-info reveal">

            <h3>
                Contact COSIS
            </h3>

            <p>
                For the most current information regarding
                admissions, courses, schedules and official
                announcements, please verify details through
                the official COSIS website.
            </p>


            <div class="contact-item">

                <div class="contact-item-icon">
                    📍
                </div>

                <div>

                    <strong>
                        <a href="https://www.google.com/maps/place/College+of+Shariah+and+Islamic+Sciences/@31.4446346,74.3153251,18z"
                           target="_blank">
                            Location
                        </a>
                    </strong>

                    <span>
                        Township, Lahore, Pakistan
                    </span>

                </div>

            </div>


            <div class="contact-item">

                <div class="contact-item-icon">
                    🌐
                </div>

                <div>

                    <strong>
                        <a href="http://www.cosis.edu.pk/english/index.html"
                           target="_blank">
                            Official Website
                        </a>
                    </strong>

                    <span>
                        cosis Township.pk
                    </span>

                </div>

            </div>


            <div class="contact-item">

                <div class="contact-item-icon">
                    🎓
                </div>

                <div>

                    <strong>
                        <a href="https://www.facebook.com/cosistownship/"
                           target="_blank">
                            Institution
                        </a>
                    </strong>

                    <span>
                        College of Shariah & Islamic Sciences
                    </span>

                </div>

            </div>

        </div>


        <div class="contact-form reveal">

            <form onsubmit="submitForm(event)">

                <div class="form-row">

                    <input
                        type="text"
                        id="name"
                        placeholder="Your Name"
                        required
                    >

                    <input
                        type="email"
                        id="email"
                        placeholder="Your Email"
                        required
                    >

                </div>


                <select id="subject" required>

                    <option value="">
                        Select Inquiry
                    </option>

                    <option>
                        Admissions
                    </option>

                    <option>
                        Programs
                    </option>

                    <option>
                        Courses
                    </option>

                    <option>
                        General Information
                    </option>

                </select>


                <textarea
                    id="message"
                    placeholder="Write your message..."
                    required></textarea>


                <button type="submit"
                        class="btn btn-primary">
                    Send Inquiry →
                </button>

            </form>

        </div>

    </div>

</section>


<!-- =======================================================
     FAQ
======================================================= -->

<section class="faq-section">

    <div class="section-heading reveal">

        <small>
            Information
        </small>

        <h2>
            Frequently Asked Questions
        </h2>

        <p>
            Find answers to common questions about COSIS.
        </p>

    </div>


    <div class="faq-container">

        <div class="faq reveal">

            <div class="faq-question"
                 onclick="toggleFAQ(this)">

                <span>
                    What is COSIS?
                </span>

                <span>+</span>

            </div>

            <div class="faq-answer">

                <p>
                    The College of Sharia and Islamic Sciences
                    (COSIS) is an institution associated with
                    Minhaj University Lahore and has a long
                    history of Islamic and academic education.
                </p>

            </div>

        </div>


        <div class="faq reveal">

            <div class="faq-question"
                 onclick="toggleFAQ(this)">

                <span>
                    What programs are available?
                </span>

                <span>+</span>

            </div>

            <div class="faq-answer">

                <p>
                    COSIS offers learning opportunities covering
                    Shariah and Islamic Sciences, Islamic training,
                    Qur'anic learning, ethics, research and
                    student development.
                </p>

            </div>

        </div>


        <div class="faq reveal">

            <div class="faq-question"
                 onclick="toggleFAQ(this)">

                <span>
                    How can I contact COSIS?
                </span>

                <span>+</span>

            </div>

            <div class="faq-answer">

                <p>
                    You can use the contact information and
                    official website provided on this page
                    for current information.
                </p>

            </div>

        </div>


        <div class="faq reveal">

            <div class="faq-question"
                 onclick="toggleFAQ(this)">

                <span>
                    Where is COSIS located?
                </span>

                <span>+</span>

            </div>

            <div class="faq-answer">

                <p>
                    COSIS is located in Township, Lahore, Pakistan.
                </p>

            </div>

        </div>

    </div>

</section>


<!-- =======================================================
     FOOTER
======================================================= -->

<footer>

    <div class="footer-grid">

        <div>

            <div class="footer-logo">
                COSIS Township
            </div>

            <p>
                College of Shariah and Islamic Sciences.
                A center of Islamic learning, education
                and student development.
            </p>

        </div>


        <div>

            <h3>
                Quick Links
            </h3>

            <a href="#home">
                Home
            </a>

            <a href="#about">
                About
            </a>

            <a href="#programs">
                Programs
            </a>

            <a href="#events">
                Events
            </a>

        </div>


        <div>

            <h3>
                Students
            </h3>

            <a href="#admissions">
                Admissions
            </a>

            <a href="#programs">
                Courses
            </a>

            <a href="https://www.instagram.com/cosis_township_/"
               target="_blank">
                Instagram
            </a>

        </div>


        <div>

            <h3>
                Official website
            </h3>

            <a href="https://www.cosis.pk/"
               target="_blank">
                COSIS Website
            </a>

            <a href="https://mul.edu.pk/"
               target="_blank">
                Minhaj University Lahore
            </a>

        </div>

    </div>


    <div class="copyright">

        © 2026 COSIS Township Lahore.
        Website concept created for educational/informational use.

    </div>

</footer>


<button id="scrollTop"
        aria-label="Scroll to top">
    ↑
</button>


<script>

/* =========================================================
   CAROUSEL
========================================================= */

let currentSlide = 0;

const slides = document.querySelector(".slides");
const slideImages = document.querySelectorAll(".slides img");
const totalSlides = slideImages.length;
const dotsContainer = document.getElementById("carouselDots");

function createDots(){

    if(!dotsContainer) return;

    dotsContainer.innerHTML = "";

    slideImages.forEach((_, index) => {

        const dot = document.createElement("div");

        dot.className = "carousel-dot";

        if(index === 0){
            dot.classList.add("active");
        }

        dot.addEventListener("click", () => {

            currentSlide = index;

            showSlide();

        });

        dotsContainer.appendChild(dot);

    });

}

function showSlide(){

    if(!slides || totalSlides === 0) return;

    slides.style.transform =
        `translateX(-${currentSlide * 100}%)`;

    document
        .querySelectorAll(".carousel-dot")
        .forEach((dot,index)=>{

            dot.classList.toggle(
                "active",
                index === currentSlide
            );

        });
}

function nextSlide(){

    currentSlide++;

    if(currentSlide >= totalSlides){
        currentSlide = 0;
    }

    showSlide();

}

function previousSlide(){

    currentSlide--;

    if(currentSlide < 0){
        currentSlide = totalSlides - 1;
    }

    showSlide();

}

createDots();
showSlide();


/* =========================================================
   AUTO SLIDER
========================================================= */

let autoSlide =
    setInterval(nextSlide,4000);

const carousel =
    document.querySelector(".carousel");

if(carousel){

    carousel.addEventListener("mouseenter",()=>{

        clearInterval(autoSlide);

    });

    carousel.addEventListener("mouseleave",()=>{

        autoSlide =
            setInterval(nextSlide,4000);

    });

}


/* =========================================================
   MOBILE MENU
========================================================= */

function toggleMenu(){

    const menu =
        document.getElementById("navMenu");

    if(!menu) return;

    menu.classList.toggle("mobile-open");

}


/* Close mobile menu */

document
.querySelectorAll("#navMenu a")
.forEach(link=>{

    link.addEventListener("click",()=>{

        const menu =
            document.getElementById("navMenu");

        menu.classList.remove("mobile-open");

    });

});


/* =========================================================
   SCROLL REVEAL
========================================================= */

const revealElements =
    document.querySelectorAll(".reveal");

const revealObserver =
    new IntersectionObserver(

        entries=>{

            entries.forEach(entry=>{

                if(entry.isIntersecting){

                    entry.target.classList.add("show");

                    revealObserver
                        .unobserve(entry.target);

                }

            });

        },

        {
            threshold:.12
        }

    );

revealElements.forEach(element=>{

    revealObserver.observe(element);

});


/* =========================================================
   CONTACT FORM
========================================================= */

function submitForm(event){

    event.preventDefault();

    const name =
        document.getElementById("name").value;

    const subject =
        document.getElementById("subject").value;

    alert(
        "Thank you, " +
        name +
        "!\n\n" +
        "Your " +
        subject +
        " inquiry has been recorded in this demo."
    );

    event.target.reset();

}


/* =========================================================
   FAQ
========================================================= */

function toggleFAQ(element){

    const faq =
        element.parentElement;

    document
        .querySelectorAll(".faq")
        .forEach(item=>{

            if(item !== faq){
                item.classList.remove("active");

                const icon =
                    item.querySelector(
                        ".faq-question span:last-child"
                    );

                if(icon){
                    icon.textContent = "+";
                }
            }

        });

    faq.classList.toggle("active");

    const icon =
        element.querySelector(
            "span:last-child"
        );

    if(icon){

        icon.textContent =
            faq.classList.contains("active")
            ? "−"
            : "+";

    }

}


/* =========================================================
   SCROLL TO TOP
========================================================= */

const topButton =
    document.getElementById("scrollTop");

window.addEventListener("scroll",()=>{

    if(window.scrollY > 500){

        topButton.classList.add("show");

    }else{

        topButton.classList.remove("show");

    }

});

topButton.addEventListener("click",()=>{

    window.scrollTo({

        top:0,

        behavior:"smooth"

    });

});


/* =========================================================
   SCROLL PROGRESS
========================================================= */

window.addEventListener("scroll",()=>{

    const scrollTop =
        window.scrollY;

    const documentHeight =
        document.documentElement.scrollHeight
        - window.innerHeight;

    const percentage =
        (scrollTop / documentHeight) * 100;

    document.getElementById(
        "scrollProgress"
    ).style.width =
        percentage + "%";

});


/* =========================================================
   HERO PARALLAX
========================================================= */

window.addEventListener("scroll",()=>{

    const hero =
        document.querySelector(".hero");

    if(!hero) return;

    if(window.scrollY < 700){

        hero.style.backgroundPosition =
            `center ${window.scrollY * .18}px`;

    }

});


/* =========================================================
   KEYBOARD CAROUSEL
========================================================= */

document.addEventListener("keydown",event=>{

    if(event.key === "ArrowRight"){

        nextSlide();

    }

    if(event.key === "ArrowLeft"){

        previousSlide();

    }

});


/* =========================================================
   TOUCH SWIPE CAROUSEL
========================================================= */

let touchStartX = 0;
let touchEndX = 0;

if(carousel){

    carousel.addEventListener("touchstart",event=>{

        touchStartX =
            event.changedTouches[0].screenX;

    });

    carousel.addEventListener("touchend",event=>{

        touchEndX =
            event.changedTouches[0].screenX;

        if(touchEndX < touchStartX - 50){

            nextSlide();

        }

        if(touchEndX > touchStartX + 50){

            previousSlide();

        }

    });

}


/* =========================================================
   ESC CLOSE MOBILE MENU
========================================================= */

document.addEventListener("keydown",event=>{

    if(event.key === "Escape"){

        document
            .getElementById("navMenu")
            .classList.remove("mobile-open");

    }

});

</script>

</body>
</html>
