<template>
  <div class="relative z-10 w-full overflow-y-auto h-full">
    <div class="z-0 absolute pointer-events-none opacity-50">
      <img src="../assets/gradient-bg.png" alt="" />
    </div>
    <!-- Hamburger for Small Screens -->

    <div
      @click="mobileMenu = !mobileMenu"
      class="block sm:hidden text-3xl cursor-pointer absolute right-16 top-20"
      style="color: #4fb34a"
    >
      <i class="far fa-bars"></i>
    </div>
    <div
      v-if="mobileMenu"
      @click="mobileMenu = !mobileMenu"
      class="z-20 fixed inset-0 w-full h-screen"
    >
      <div
        class="bg-white z-30 fixed right-14 top-32 font-medium text-lg rounded-lg"
        style="color: #4fb34a"
      >
        <!--  -->
        <div class="text-center space-y-2 p-4">
          <p>
            <router-link :to="{ path: '/' }">HOME</router-link>
          </p>
          <p>
            <router-link :to="{ path: '/aboutUs' }">ABOUT US</router-link>
          </p>
          <p>
            <router-link :to="{ path: '/ourProducts' }">OUR PRODUCTS</router-link>
          </p>
          <p>
            <router-link :to="{ path: '/contactUs' }">CONTACT US</router-link>
          </p>
        </div>
      </div>
    </div>
    <section class="px-10 lg:px-44 pt-6 font-medium">
      <section id="top" class="flex justify-between" style="font-size: 10px">
        <div class="flex space-x-1 lg:space-x-3 justify-between">
          <!-- For Smaller Screens -->
          <div class="flex justify-between items-center space-x-5">
            <div class="sm:hidden">
              <vs-tooltip bottom>
                <img
                  style="color: #1da737"
                  src="../assets/tel.svg"
                  alt="tel icon"
                  class="pr-2"
                />
                <template #tooltip> +234 814 932 7275, +234 810 950 7030 </template>
              </vs-tooltip>
            </div>

            <div class="sm:hidden">
              <vs-tooltip bottom>
                <img
                  style="color: #1da737"
                  src="../assets/mail.svg"
                  alt="tel icon"
                  class="pr-2"
                />
                <template #tooltip> support@dayspring.com</template>
              </vs-tooltip>
            </div>

            <div class="sm:hidden">
              <vs-tooltip bottom>
                <img
                  style="color: #1da737"
                  src="../assets/location_on.svg"
                  alt="tel icon"
                  class="pr-2"
                />
                <template #tooltip>
                  Plot 24, Oba Onigbanko Way, Amuwo Odofin, Lagos</template
                >
              </vs-tooltip>
            </div>

            <div class="sm:hidden">
              <vs-tooltip bottom>
                <img
                  style="color: #1da737"
                  src="../assets/time.svg"
                  alt="tel icon"
                  class="pr-2"
                />
                <template #tooltip> Mon - Fri: 9:00AM - 5:00PM</template>
              </vs-tooltip>
            </div>

            <!-- For Larger Screens -->

            <a href="tel:+234 814 932 7275" class="sm:flex items-center hidden">
              <img
                style="color: #1da737"
                src="../assets/tel.svg"
                alt="tel icon"
                class="pr-2"
              />
              <p>+234 814 932 7275, +234 810 950 7030</p>
            </a>
          </div>
          <div class="text-center">
            <a href="mailto:support@dayspring.com " class="sm:flex items-center hidden">
              <img
                style="color: #1da737"
                src="../assets/mail.svg"
                alt="tel icon"
                class="pr-2"
              />
              <p>support@dayspring.com</p>
            </a>
          </div>
          <div class="text-center">
            <a
              href="https://www.google.com/maps/place/Amuwo+Odofin+Estate,+Lagos/@6.477648,3.2904734,14z/data=!4m5!3m4!1s0x103b892def871c8b:0xb4250ab791be1ae7!8m2!3d6.4768936!4d3.3137121"
              target="_blank"
              class="sm:flex items-center hidden"
              ><div class="flex">
                <img
                  style="color: #1da737"
                  src="../assets/location_on.svg"
                  alt="tel icon"
                  class="pr-2 flex justify-start"
                />
                <p>Plot 24, Oba Onigbanko Way, Amuwo Odofin, Lagos</p>
              </div></a
            >
          </div>

          <div class="sm:flex items-center hidden">
            <img
              style="color: #1da737"
              src="../assets/time.svg"
              alt="tel icon"
              class="pr-2"
            />
            <p>Mon - Fri: 9:00AM - 5:00PM</p>
          </div>
        </div>
        <div class="flex space-x-8" style="color: #1da737">
          <a href="https://web.facebook.com" target="_blank"
            ><img class="w-4 h-3.5" src="../assets/facebook.svg" alt="facebook" />
          </a>
          <a href="https://twitter.com/" target="_blank"
            ><img class="w-4 h-4" src="../assets/twitter.svg" alt="twitter" />
          </a>
          <a href="https://www.instagram.com/" target="_blank">
            <img class="w-4 h-4" src="../assets/instagram.svg" alt="instagram" />
          </a>
        </div>
      </section>

      <section class="z-30 flex justify-between items-center font-semibold my-7">
        <div>
          <router-link :to="{ path: '/' }">
            <img class="w-20 h-20" src="../assets/logo.svg" alt="Dayspring Logo" />
          </router-link>
        </div>
        <div class="space-x-9 text-lg sm:flex hidden">
          <router-link :to="{ path: '/' }"
            ><span class="cursor-pointer">Home</span></router-link
          >
          <router-link :to="{ name: 'AboutUs' }"
            ><span class="cursor-pointer">About Us</span></router-link
          >
          <router-link :to="{ name: 'OurProducts' }"
            ><span class="cursor-pointer">Our Products</span></router-link
          >
          <router-link :to="{ name: 'ContactUs' }"
            ><span class="cursor-pointer">Contact Us</span></router-link
          >
        </div>
      </section>
      <section class="z-30 pt-28 w-full text-center space-y-9">
        <p class="font-extrabold text-5xl">Your Timeless Financial Service Provider</p>
        <p class="text-base font-semibold">
          We have provided over 300,000 loans to individuals and small businesses in
          Nigeria
        </p>
        <button
          style="background: #1da737"
          class="text-white rounded-md py-3 px-9 text-lg font-semibold"
        >
          See Our Products
        </button>
      </section>
    </section>
    <section
      class="pt-24 px-10 lg:px-44 w-full sm:flex block justify-between space-y-7 sm:space-x-24 space-x-0"
    >
      <div class="space-y-6 font-medium">
        <p class="font-extrabold" style="font-size: 35px">About Us</p>
        <p style="font-size: 14px">
          Dayspring Capital is Nigeria’s fastest growing financial services provider. We
          do this through our website, social media pages and customer experience center.
        </p>
        <p style="font-size: 14px">
          What makes Dayspring Capital unique among the packs of other financial service
          provider is that we also make this service available to individuals who are
          small business owners as it’s our desire to energize the economy through these
          SMEs and provide for their financial needs.
        </p>
        <button
          style="background: #1da737"
          class="text-white rounded-md py-3 px-7 text-base font-semibold"
        >
          Read More
        </button>
      </div>
      <div class="flex justify-center">
        <div class="w-72 h-64">
          <img
            class="w-full h-full inset-0 object-cover rounded-lg"
            src="../assets/aboutus.jpg"
            alt="About Us"
          />
        </div>
      </div>
    </section>
    <section
      class="font-normal pt-10 px-10 lg:px-44 mt-24 mb-10 space-y-6 text-white"
      style="background: #1da737"
    >
      <p style="font-size: 35px" class="font-bold pt-16">Why Dayspring?</p>
      <p style="font-size: 18px">
        Our commitment is to meet our customer’s needs and hand over an unforgettable
        financial service experience within the under listed parameters
      </p>
      <div class="sm:flex justify-between block sm:space-x-8 space-x-0 space-y-4 pb-20">
        <div class="space-y-2">
          <img class="w-7 h-5" src="../assets/payment.svg" alt="Payment" />
          <p class="font-bold" style="font-size: 20px">Flexible Repayment</p>
          <p>
            Our repayment structure is flexible which means you don’t have to break the
            bank to payback
          </p>
        </div>
        <div class="space-y-2">
          <img class="w-5 h-4" src="../assets/rates.svg" alt="Rates" />
          <p class="font-bold" style="font-size: 20px">Great Rates</p>
          <p>
            We have that most competitive interest in the market which makes us top choice
            when it comes to personal and SME lending.
          </p>
        </div>
        <div class="space-y-2">
          <img class="w-5 h-5" src="../assets/customers.svg" alt="Customers" />
          <p class="font-bold" style="font-size: 20px">Happy Customers</p>
          <p>
            Our client testimonial speaks for us, we are not just a credit company we are
            our customer's success partners.
          </p>
        </div>
      </div>
    </section>
    <section class="pt-10 px-10 lg:px-44 mt-14 mb-10 space-y-6 text-black">
      <div>
        <p style="font-size: 35px" class="font-bold mb-2">Our Products</p>
        <div class="sm:flex block sm:space-x-4 space-x-0">
          <div class="sm:w-3/5 w-full mr-7">
            <img src="../assets/dayspring-credit.svg" alt="dayspring credit" />
            <p style="font-size: 18px" class="pt-8 font-normal">
              Dayspring Credit is our platform where we give financial credit to
              Individuals and groups for their financial needs. For this we also target
              credit worthy salary earners who can access this facility. This is available
              between the sum of 100,000- 5 Million based on request. With a 10% interest
              rate, we’ve eased the repayment for customers. This is repaid on a monthly
              basis. The target markets for this are individuals, groups and corporate
              entity.
            </p>
            <button
              style="background: #1da737"
              class="text-white mt-9 rounded-md py-3 px-7 text-base font-semibold"
            >
              Read More
            </button>
          </div>
          <div
            class="sm:w-2/5 w-full text-base font-normal rounded-3xl ml-3 mt-6 py-3 border border-gray-100"
            style="font-size: 18px"
          >
            <div class="px-4">
              <p class="flex text-green-700">
                <img
                  src="../assets//bullet.svg"
                  alt="bullet point"
                  class="pr-4"
                />Dayspring Credit
              </p>
              <p class="border-b border-gray-300 py-2 pt-3">Dayspring Asset Financing</p>
              <p class="border-b border-gray-300 py-2 pt-3">Dayspring Market Money</p>
              <p class="border-b border-gray-300 py-2 pt-3">Dayspring Asset Management</p>
              <p class="border-b border-gray-300 py-2 pt-3">
                Dayspring Equipment Leasing
              </p>
              <p class="border-b border-gray-300 py-2 pt-3">
                Our Foreign Exchange Services
              </p>
              <p class="border-b border-gray-300 py-2 pt-3">FX Brokerage & Transfer</p>
              <p class="border-b border-gray-300 py-2 pt-3">Cash Delivery</p>
              <p class="border-b border-gray-300 py-2 pt-3">
                Business Consultancy Services
              </p>
              <p class="py-2 pt-3">Investment Management</p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section
      class="pt-10 px-10 lg:px-44 mt-24 mb-10 space-y-6 text-white"
      style="background: #1da737"
    >
      <p class="text-4xl font-extrabold">What Our Client's Say</p>
      <p style="font-size: 15px">Dont worry, you're in good hands.</p>
      <div class="sm:flex block sm:space-x-12 space-x-0 pb-10">
        <div class="sm:w-1/2 w-full space-y-3">
          <div class="flex items-center -space-x-20">
            <div class="h-28 w-24">
              <img src="../assets/effect.svg" alt="effect" class="w-full h-full" />
            </div>
            <div class="h-20 w-20">
              <img src="../assets/client1.svg" alt="client1" class="w-full h-full" />
            </div>
          </div>
          <p style="font-size: 20px" class="italic">
            “I was having financial challenges to buy equipment, I requested for a loan
            and I was attended to within 2 hours.
          </p>
          <p style="font-size: 15px" class="font-bold">Paul Oyebanjo</p>
          <p style="font-size: 15px">Sound Engineer</p>
        </div>
        <div class="sm:w-1/2 w-full space-y-3 sm:mt-0 mt-8">
          <div class="flex items-center -space-x-20">
            <div class="h-28 w-24">
              <img src="../assets/effect.svg" alt="effect" class="w-full h-full" />
            </div>
            <div class="h-20 w-20">
              <img src="../assets/client2.svg" alt="client1" class="w-full h-full" />
            </div>
          </div>
          <p class="italic" style="font-size: 20px">
            “I requested for a loan to complete a project, and i was attended to and was
            credited within 30 minutes, after my request was reviewed.The interest is so
            affordable compared to others.They are dependable and reliable.
          </p>
          <p style="font-size: 15px" class="font-bold">Adeniyi Adeyemi</p>
          <p style="font-size: 15px">Architect</p>
        </div>
      </div>
    </section>
    <section class="pt-10 px-10 lg:px-44 mt-14 mb-10 space-y-6">
      <p class="text-4xl font-bold">Send Us A Message</p>
      <p style="font-size: 15px">
        Thank you for your interest in Dayspring Capital. Please fill out the form below
        to ask your questions. We will get back to you within the shortest possible time.
      </p>
      <div class="flex justify-between w-full">
        <div class="w-full flex sm:space-x-12 space-x-0">
          <div class="w-1/3 sm:block hidden mt-1.5">
            <img
              class="w-80 inset-0 object-cover rounded-2xl"
              style="height: 524px"
              src="../assets/message.svg"
              alt="send message"
            />
          </div>
          <div class="sm:w-2/3 w-full space-y-10">
            <div class="w-full flex space-x-4">
              <div class="w-1/2">
                <label for="fname" class="" style="font-size: 15px">First Name</label>
                <br />
                <input
                  type="text"
                  class="border border-gray-100 rounded-xl w-full"
                  placeholder="e.g John"
                />
              </div>

              <div class="w-1/2">
                <label for="sname" class="" style="font-size: 15px">Second Name</label>
                <br />
                <input
                  type="text"
                  class="border border-gray-100 rounded-xl w-full"
                  placeholder="e.g Doe"
                />
              </div>
            </div>

            <div class="w-full flex space-x-4">
              <div class="w-1/2">
                <label for="email" class="" style="font-size: 15px">Email Address</label>
                <br />
                <input
                  type="text"
                  class="border border-gray-100 rounded-xl w-full"
                  placeholder="e.g johndoe@email.com"
                />
              </div>
              <div class="w-1/2">
                <label for="p/no" class="" style="font-size: 15px">Phone Number</label>
                <br />
                <input
                  type="text"
                  class="border border-gray-100 rounded-xl w-full"
                  placeholder="e.g 08023456789"
                />
              </div>
            </div>

            <div class="w-full">
              <label for="message" class="" style="font-size: 15px">Message</label>
              <br />
              <textarea
                name="message"
                id=""
                md:cols="85"
                cols="60"
                rows="10"
                placeholder="Write your message here"
                class="border border-gray-100 rounded-xl w-full"
              >
              </textarea>
            </div>
            <button
              style="background: #f0c603"
              class="rounded-md py-4 px-7 text-xl font-semibold"
            >
              Send Message
            </button>
          </div>
        </div>
      </div>
    </section>
    <section class="pt-10 px-10 lg:px-44 mt-14 pb-10 bg-black text-white">
      <div class="w-full sm:flex block sm:space-x-12">
        <div class="sm:w-1/2 w-full">
          <div>
            <img src="../assets/logo.svg" alt="footer logo" class="w-36 h-36" />
            <div class="ml-6 -mt-10">
              <p style="font-size: 18px" class="font-extrabold">Dayspring</p>
              <p class="mb-3" style="font-size: 8px">Capital Investments Limited</p>
            </div>
          </div>
          <p style="font-size: 13px" class="mb-6">
            Be the first to know! Subscribe to our mailing list to keep up with the latest
            news and offers.
          </p>
          <div class="md:flex items-center block space-x-4 md:space-y-2">
            <div>
              <label for="email" class="">Email Address</label>
              <br />
              <input
                type="text"
                class="border border-gray-100 rounded-xl w-full text-black"
                placeholder="e.g johndoe@email.com"
              />
            </div>
            <div>
              <button
                style="background: #1da737; font-size: 13px; padding: 10px 20px"
                class="text-white rounded-md font-semibold mt-3.5"
              >
                Subscribe
              </button>
            </div>
          </div>
        </div>
        <div class="sm:w-1/2 w-full">
          <div class="md:space-y-8 space-y-6" style="font-size: 13px">
            <div class="">
              <a href="tel:+234 814 932 7275" class="flex">
                <img style="color: #1da737" src="../assets/tel.svg" alt="tel icon" />
                <div class="space-y-2 pl-4 mt-7">
                  <p class="text-extrabold">Phone Number(s)</p>
                  <p>+234 814 932 7275, +234 810 950 7030</p>
                </div>
              </a>
            </div>
            <div class="">
              <a href="mailto:support@dayspring.com " class="flex">
                <img
                  style="color: #1da737"
                  src="../assets/mail.svg"
                  alt="tel icon"
                  class=""
                />
                <div class="space-y-2 pl-4">
                  <p class="text-extrabold">Email Address</p>
                  <p>support@dayspring.com</p>
                </div>
              </a>
            </div>
            <div class="">
              <a
                href="https://www.google.com/maps/place/Amuwo+Odofin+Estate,+Lagos/@6.477648,3.2904734,14z/data=!4m5!3m4!1s0x103b892def871c8b:0xb4250ab791be1ae7!8m2!3d6.4768936!4d3.3137121"
                target="_blank"
                class="flex"
              >
                <img
                  style="color: #1da737"
                  src="../assets/location_on.svg"
                  alt="tel icon"
                  class=""
                />
                <div class="space-y-2 pl-4">
                  <p class="text-extrabold">Address</p>
                  <p>Plot 24, Oba Onigbanko Way, Amuwo Odofin, Lagos</p>
                </div>
              </a>
            </div>

            <div class="flex">
              <img
                style="color: #1da737"
                src="../assets/time.svg"
                alt="tel icon"
                class=""
              />
              <div class="space-y-2 pl-4">
                <p class="text-extrabold">Opening Hours</p>
                <p>Mon - Frid: 9:00AM - 5:00PM</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <hr class="my-10" />
      <div class="flex w-full items-center" style="font-size: 13px">
        <div class="w-2/3">
          <p>&#64;2021 Dayspring Capital RC 1640535. All rights reserved.</p>
        </div>
        <div class="w-1/3 flex justify-around">
          <div class="md:space-x-12 space-x-2 flex" style="color: #1da737">
            <a href="https://web.facebook.com" target="_blank">
              <img class="w-2 h-4" src="../assets/facebook.svg" alt="facebook" />
            </a>
            <a href="https://twitter.com/" target="_blank">
              <img class="w-4 h-3.5" src="../assets/twitter.svg" alt="twitter" />
            </a>
            <a href="https://www.instagram.com/" target="_blank">
              <img class="w-4 h-4" src="../assets/instagram.svg" alt="instagram" />
            </a>
          </div>
          <div class="">
            <a href="/#top" class="flex space-x-2 items-center -mt-1">
              <img
                class="sm:w-3 w-6 sm:h-2 h-4"
                src="../assets/up.svg"
                alt="direction-top"
              />
              <p class="text-xs sm:block hidden">Back to top</p>
            </a>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mobileMenu: false,
    };
  },
};
</script>

<style>
/* .small-font {
  font-size: 10px;
} */
</style>
