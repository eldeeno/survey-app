<template>
  <div>
    <img alt="Workflow" class="mx-auto h-12 w-auto"
         src="https://tailwindui.com/img/logos/workflow-mark-indigo-600.svg"/>
    <h2 class="mt-6 text-center text-3xl font-extrabold text-gray-900">Sign in to your account</h2>
    <p class="mt-2 text-center text-sm text-gray-600">
      Or
      {{ ' ' }}
      <router-link :to="{ name: 'Login' }" class="font-medium text-indigo-600 hover:text-indigo-500"> login to your
        account
      </router-link>
    </p>
  </div>
  <form action="#" class="mt-8 space-y-6" method="POST">
    <input name="remember" type="hidden" value="true"/>
    <div class="rounded-md shadow-sm -space-y-px">
      <div>
        <label class="sr-only" for="fullname">Email address</label>
        <input id="fullname" autocomplete="fullname"
               class="appearance-none rounded-none relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-t-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm"
               name="fullname" placeholder="Full name"
               required=""
               type="text"/>
      </div>
      <div>
        <label class="sr-only" for="email-address">Email address</label>
        <input id="email-address" autocomplete="email"
               class="appearance-none rounded-none relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm"
               name="email" placeholder="Email address"
               required=""
               type="email"/>
      </div>
      <div>
        <label class="sr-only" for="password">Password</label>
        <input id="password" autocomplete="current-password"
               class="appearance-none rounded-none relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-b-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm"
               name="password" placeholder="Password"
               required=""
               type="password"/>
      </div>
    </div>

    <div>
      <button
        class="group relative w-full flex justify-center py-2 px-4 border border-transparent text-sm font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
        type="submit">
            <span class="absolute left-0 inset-y-0 flex items-center pl-3">
              <LockClosedIcon aria-hidden="true" class="h-5 w-5 text-indigo-500 group-hover:text-indigo-400"/>
            </span>
        Sign up
      </button>
    </div>
  </form>
</template>

<script>
import {LockClosedIcon} from '@heroicons/vue/solid'

export default {
  components: {
    LockClosedIcon,
  },
}
</script>
