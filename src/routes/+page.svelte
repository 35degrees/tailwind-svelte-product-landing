<script>
  let first = 'Sam3'
  let last = 'Hooker'
  let color = 'blue'
  let hamburger
  let mobileMenu

  $: name = first + ' ' + last

  const toggle = () => {
    hamburger.classList.toggle('open')
    mobileMenu.classList.toggle('flex')
    mobileMenu.classList.toggle('hidden')
    // first = first === 'Sam3' ? 'Stan' : 'Sam3'
    // color = color === 'blue' ? 'red' : 'blue'
    // mobileMenu.classList.toggle('open')
  }
</script>

<!-- navbar  -->
 <nav class="relative container p-6">
  <!-- flex container  -->
   <div class="flex items-center justify-between">
    <!-- logo -->
     <div class="pt-2">
      <img src="src/lib/img/logo.svg" alt="logo">
     </div>

     <!-- menu items  -->
      <div class="hidden md:flex space-x-6">
        <a href="#" class="hover:text-darkGreyishBlue" style="color:{color}">{name}</a>
        <a href="#" class="hover:text-darkGreyishBlue">Product</a>
        <a href="#" class="hover:text-darkGreyishBlue">About Us</a>
        <a href="#" class="hover:text-darkGreyishBlue">Careers</a>
        <a href="#" class="hover:text-darkGreyishBlue">Community</a>
      </div>

      <!-- button  -->
       <a href="#" class="hidden md:block p-3 px-6 pt-2 text-white bg-brightRed rounded-full baseline hover:bg-brightRedLight">Get Started</a>

       <!-- hamburger icon -->
        <button id="menu-btn" bind:this={hamburger} on:click={toggle} class="block hamburger md:hidden focus:outline-none">
          <span class="hamburger-top"></span>
          <span class="hamburger-middle"></span>
          <span class="hamburger-bottom"></span>
        </button>

   </div>

   <!-- mobile menu -->
    <div class="md:hidden">
      <div id="menu" bind:this={mobileMenu} class="absolute flex-col items-center hidden self-end py-8 mt-10 space-y-6 font-bold bg-white sm:w-auto sm:self-center left-6 right-6 drop-shadow-md">
        <a href="#">Pricing</a>
        <a href="#">Product</a>
        <a href="#">About Us</a>
        <a href="#">Careers</a>
        <a href="#">Community</a>
  
      </div>
    </div>
 </nav>


 <!-- HERO SECTION  -->

 <section id="hero">

  <!-- flex container  -->
   <div class="container flex flex-col-reverse md:flex-row items-center px-6 mx-auto mt-10 space-y-0 md:space-y-0">
    <div class="flex flex-col mb-32 space-y-12 md:w-1/2">
      <h1 class="max-w-md text-4xl font-bold text-center md:text-5xl md:text-left">
        Bring everyone together to build better products.
      </h1>
      <p class="max-w-sm text-center text-darkGreyishBlue sm:mx-auto md:mx-0 md:text-left">
        Manage makes it simple for software teams to plan day-to-day tasks while keeping the larger team goals in mind.
      </p>
      <div class="flex justify-center md:justify-start">
        <a href="#" class="p-3 px-6 pt-2 text-white bg-brightRed rounded-full baseline hover:bg-brightRedLight">Get Started</a>
      </div>
    </div>

    <div class="md:w-1/2">
      <img src="src/lib/img/illustration-intro.svg" alt="">
    </div>
   </div>
 </section>


 <!-- features section  -->
  <section id="features">
    <!-- flex container  -->
     <div class="container flex flex-col p-4 mx-auto mt-10 space-y-12 md:space-y-0 md:flex-row">
      <div class="flex flex-col space-y-12 md:w-1/2">
        <!-- whats diff  -->
        <h2 class="max-w-md text-4xl font-bold text-center md:text-left">
          What's different about Manage?
        </h2>
        <p class="max-w-sm text-center text-darkGreyishBlue sm:mx-auto md:mx-0 md:text-left md:text-left">
          Manage provides all the functionality your team needs, without the complexity. Our software is tailor-made for modern digital teams.
        </p>
      </div>

      <div class="flex flex-col space-y-8 md:w-1/2">
        <div class="flex flex-col space-y-3 md:space-y-0 md:space-x-6 md:flex-row">
          <!-- heading -->
           <div class="rounded-l-full bg-brightRedSupLight md:bg-transparent">
            <div class="flex items-center space-x-2">
              <div class="px-4 py-2 text-white rounded-full md:py-1 bg-brightRed">
                01
              </div>
              <h3 class="text-base font-bold md:mb-4 md:hidden">
                Track company-wide progress
              </h3>
            </div>
           </div>
           <div>
            <h3 class="hidden mb-4 text-lg font-bold md:block">
              Track company-wide progress
             </h3>
             <p class="text-darkGreyishBlue">
           Lorem, ipsum dolor sit amet consectetur adipisicing elit. Itaque assumenda tempora pariatur cupiditate quasi est doloribus odio dolore architecto quas sunt sint expedita delectus earum eveniet, ut possimus laborum deleniti laudantium necessitatibus!
             </p>
           </div>
      
        </div>
        <div class="flex flex-col space-y-3 md:space-y-0 md:space-x-6 md:flex-row ">
          <!-- heading -->
           <div class="rounded-l-full bg-brightRedSupLight md:bg-transparent">
            <div class="flex items-center space-x-2">
              <div class="px-4 py-2 text-white rounded-full md:py-1 bg-brightRed">
                02
              </div>
              <h3 class="text-base font-bold md:mb-4 md:hidden">
                Advanced built-in reports
              </h3>
            </div>
           </div>
           <div>
            <h3 class="hidden mb-4 text-lg font-bold md:block">
              Advanced built-in reports
             </h3>
             <p class="text-darkGreyishBlue">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde exercitationem, vero voluptatem explicabo magnam, sapiente adipisci rem inventore nesciunt cumque cupiditate minima? Maiores eius voluptatum, incidunt nesciunt quaerat optio est dolores nihil architecto!
             </p>
           </div>
      
        </div>
        <div class="flex flex-col space-y-3 md:space-y-0 md:space-x-6 md:flex-row ">
          <!-- heading -->
           <div class="rounded-l-full bg-brightRedSupLight md:bg-transparent">
            <div class="flex items-center space-x-2">
              <div class="px-4 py-2 text-white rounded-full md:py-1 bg-brightRed">
                03
              </div>
              <h3 class="text-base font-bold md:mb-4 md:hidden">
                Everything you need in one place
              </h3>
            </div>
           </div>
           <div>
            <h3 class="hidden mb-4 text-lg font-bold md:block">
              Everything you need in one place
             </h3>
             <p class="text-darkGreyishBlue">
           Lorem ipsum dolor sit amet consectetur adipisicing elit. Eligendi eum provident, natus quam, aperiam molestias libero laborum maiores quaerat voluptas atque a necessitatibus autem sapiente deserunt non corporis voluptatem aliquid illum minus possimus modi quae est! Tempora, dignissimos.
             </p>
           </div>
      
        </div>

 
      </div>
     </div>
  </section>

  <!-- TESTIMONIALS  -->
   <section id="testimonials">
    <!-- container to heading  -->
     <div class="max-w-6xl px-5 container mt-20 bg-green-200">
      <!-- heading -->
       <h2 class="text-4xl font-bold text-center">
        What's different about Manage?
       </h2>
       <!-- testimonials container  -->
        <div class="flex flex-col mt-12 md:flex-row md:space-x-6">
          <!-- testimonial 1 -->
           <div class="flex flex-col items-center p-6 space-y-3 rounded-lg md:w-1/3 shadow-[4px_4px_12px_-2px_rgba(0,0,0,0.3)] bg-veryLightGrey">
            <img src="src/lib/img/avatar-anisha.png" class="w-16 -mt-14" alt="anisha">
            <h5 class="text-lg font-bold">Anisha Lee</h5>
            <p class="text-sm text-darkGreyishBlue text-center">
              "Manage has supercharged our team's workflow. The ability to maintain visibilitiy on larger milestones at all times keeps everyone motivated."
            </p>
          </div>
          <!-- testimonial 2 -->
           <div class="hidden md:flex flex-col items-center p-6 space-y-3 rounded-lg bg-veryLightGrey shadow-[4px_4px_12px_-2px_rgba(0,0,0,0.3)] md:w-1/3 ">
            <img src="src/lib/img/avatar-ali.png" class="w-16 -mt-14" alt="anisha">
            <h5 class="text-lg font-bold">Ali Bravo</h5>
            <p class="text-sm text-darkGreyishBlue text-center">
              "We have been able to cancel so many other subscriptions since using Manager. There's no more cross-channel confusion and everyone is focused."
            </p>
          </div>
          <!-- testimonial 3 -->
           <div class="hidden md:flex flex-col items-center p-6 space-y-3 rounded-lg bg-veryLightGrey shadow-[4px_4px_12px_-2px_rgba(0,0,0,0.3)] md:w-1/3">
            <img src="src/lib/img/avatar-richard.png" class="w-16 -mt-14" alt="anisha">
            <h5 class="text-lg font-bold">Richard Watts</h5>
            <p class="text-sm text-darkGreyishBlue text-center">
              "Manage has supercharged our team's workflow. The ability to maintain visibilitiy on larger milestones at all times keeps everyone motivated."
            </p>
          </div>
          
        </div>
        <div class="my-12 text-center">
          <a href="#" class="p-3 px-6 pt-2 text-white mx-auto bg-brightRed rounded-full  hover:bg-brightRedLight">Get Started</a>
        </div>

     </div>
   </section>

   <!-- CTA  -->
    <section id="cta" class="bg-brightRed">
      <!-- flex container  -->
       <div class="container flex flex-col items-center justify-between px-6 py-20 mx-auto space-y-10 md:py-12 md:flex-row md:space-y-0 ">
        <!-- heading -->
         <h2 class="text-5xl font-bold leading-tight text-center text-white md:text-4xl md:max-w-xl md:text-left ">
          Simplify how your team works today.
         </h2>

         <div>
          <a href="#" class="p-3 px-6 pt-2 text-brightRed mx-auto bg-white rounded-full shadow-2xl hover:bg-gray-500">Get Started</a>
        </div>
       </div>
    </section>

    <!-- FOOTER  -->
     <footer class="bg-veryDarkBlue">
      <div class="container flex flex-col-reverse justify-between px-6 py-12 space-y-8 md:flex-row md:space-y-0">
        <!-- logo and social links container -->
         <div class="flex flex-col-reverse items-center justify-between space-y-12 md:flex-col md:space-y-0 md:items-start">
          <div class="mx-auto my-6 text-center text-white md:hidden">
            Copyright &copy; 2024, All rights reserved.
          </div>
          <!-- logo -->
           <div>
            <img src="src/lib/img/logo-white.svg" alt="" class="h-8">
           </div>
           <!-- social links  -->
            <div class="flex justify-center space-x-4">
              <a href="#">
                <img src="src/lib/img/icon-facebook.svg" alt="" class="h-8">
              </a>
              <a href="#">
                <img src="src/lib/img/icon-youtube.svg" alt="" class="h-8">
              </a>
              <a href="#">
                <img src="src/lib/img/icon-twitter.svg" alt="" class="h-8">
              </a>
              <a href="#">
                <img src="src/lib/img/icon-instagram.svg" alt="" class="h-8">
              </a>
              <a href="#">
                <img src="src/lib/img/icon-pinterest.svg" alt="" class="h-8">
              </a>
            </div>
         </div>

         <!-- list container  -->
          <div class="flex justify-around space-x-32">
            <div class="flex flex-col space-y-3 text-white">
              <a href="#" class="hover:text-brightRed">Home</a>
              <a href="#" class="hover:text-brightRed">Pricing</a>
              <a href="#" class="hover:text-brightRed">Products</a>
              <a href="#" class="hover:text-brightRed">About</a>
            </div>
            <div class="flex flex-col space-y-3 text-white">
              <a href="#" class="hover:text-brightRed">Career</a>
              <a href="#" class="hover:text-brightRed">Community</a>
              <a href="#" class="hover:text-brightRed">Privacy Policy</a>
            </div>
          </div>

          <!-- input container -->
           <div class="flex flex-col justify-between">
            <form>
              <div class="flex space-x-3">
                <input type="text" class="flex-1 px-4 rounded-full focus:outline-none" placeholder="Updates in your inbox...">
                <button class="px-6 py-2 text-white rounded-full bg-brightRed hover:bg-brightRedLight focus:outline-none">
                  Go
                </button>
              </div>
            </form>

            <div class="hidden text-white md:block">
              Copyright &copy; 2024, All rights reserved. 
            </div>
           </div>

      </div>
     </footer>

<!-- <script>
  const btn = document.getElementById('menu-btn')
  const nav = document.getElementById('menu')
  console.log(btn);

  // btn.addEventListener('click',() => {
  //   btn?.classList.toggle('open')
  // })
</script> -->