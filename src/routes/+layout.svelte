<script lang="ts">
  import "../app.postcss"
  import { ComplexCode, Email } from "$icons"

  const defaultStyle =
    "text-gray-300 hover:bg-gray-700 hover:text-white rounded-md px-3 py-2 text-sm font-medium"

  $: show = false

  const ToggleMenu = () => (show = !show)
  const HideMenu = () => (show = false)
</script>

<div class="min-h-full">
  <nav class="bg-gray-800">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="flex h-16 items-center justify-between">
        <div class="flex items-center">
          <div class="flex-shrink-0">
            <a href="/" on:click={HideMenu}>
              <div class="h-8 w-8 fill-white">
                <ComplexCode />
              </div>
            </a>
          </div>
          <div class="hidden md:block">
            <div class="ml-10 flex items-baseline space-x-4">
              <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
              <a href="#education" class={defaultStyle}> Education </a>
              <a href="#employment" class={defaultStyle}> Employment </a>
              <a href="#teaching" class={defaultStyle}> Teaching </a>
              <a href="#publications" class={defaultStyle}> Publications </a>
              <a href="#affiliations" class={defaultStyle}> Affiliations </a>
              <a href="#languages" class={defaultStyle}> Languages </a>
            </div>
          </div>
        </div>
        <div class="-mr-2 flex md:hidden">
          <!-- Mobile menu button -->
          <button
            type="button"
            class="inline-flex items-center justify-center rounded-md bg-gray-800 p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-gray-800"
            aria-controls="mobile-menu"
            aria-expanded="false"
            on:click={ToggleMenu}
          >
            <span class="sr-only">Open main menu</span>
            <!-- Menu open: "hidden", Menu closed: "block" -->
            <svg
              class:block={!show}
              class:hidden={show}
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
              />
            </svg>
            <!-- Menu open: "block", Menu closed: "hidden" -->
            <svg
              class:block={show}
              class:hidden={!show}
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile menu, show/hide based on menu state. -->
    <div class="md:hidden absolute left-0 right-0 bg-gray-800" id="mobile-menu">
      {#if show}
        <div class="space-y-1 px-2 pb-3 pt-2 sm:px-3 flex flex-col">
          <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
          <a href="#education" class={defaultStyle}> Education </a>
          <a href="#employment" class={defaultStyle}> Employment </a>
          <a href="#teaching" class={defaultStyle}> Teaching </a>
          <a href="#publications" class={defaultStyle}> Publications </a>
          <a href="#affiliations" class={defaultStyle}> Affiliations </a>
          <a href="#languages" class={defaultStyle}> Languages </a>
        </div>
      {/if}
    </div>
  </nav>

  <header class="bg-white">
    <main>
      <div class="mx-auto pb-6">
        <div>
          <div>
            <img
              class="h-32 w-full object-cover lg:h-48"
              src="/media/banner.jpeg"
              alt=""
            />
          </div>
          <div class="mx-auto max-w-5xl px-4 sm:px-6 lg:px-8">
            <div class="-mt-12 sm:-mt-16 sm:flex sm:items-end sm:space-x-5">
              <div class="flex">
                <img
                  class="h-24 w-24 rounded-full ring-4 ring-white sm:h-32 sm:w-32"
                  src="/media/profile.png"
                  alt=""
                />
              </div>
              <div
                class="mt-6 sm:flex sm:min-w-0 sm:flex-1 sm:items-center sm:justify-end sm:space-x-6 sm:pb-1"
              >
                <div class="mt-6 min-w-0 flex-1 sm:hidden md:block">
                  <h1 class="truncate text-2xl font-bold text-gray-900">
                    Eisen Montalvo
                  </h1>
                  <h2>Principal Computer Engineer</h2>
                </div>
                <div class="flex mt-6">
                  <div class="h-8 w-8 fill-indigo-500 mr-0">
                    <Email />
                  </div>
                  <div class="ml-3 relative top-1">
                    contact@eisen.montalvo.cv
                  </div>
                </div>
              </div>
            </div>
            <div class="mt-6 hidden min-w-0 flex-1 sm:block md:hidden">
              <h1 class="truncate text-2xl font-bold text-gray-900">
                Eisen Montalvo
              </h1>
              <h2>Principal Computer Engineer</h2>
            </div>
          </div>
        </div>
      </div>
    </main>
  </header>
</div>

<div class="px-4 py-5 sm:p-6 max-w-7xl mx-auto">
  <slot />
</div>
