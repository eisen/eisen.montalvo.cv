<script lang="ts">
  $: collapsed = true
  $: msg = ""
  $: bibTeX = `@inproceedings{Bhokare2024,
     author = {Gaurav Bhokare and Eisen Montalvo and Elie Diaz and Cem Yuksel},
     title = {Real-Time Hair Rendering with Hair Meshes},
     booktitle = {SIGGRAPH 2024 Conference Papers},
     series = {SIGGRAPH '24},
     year = {2024},
     month = {07},
     pages = {61:1--61:10},
     articleno = {61},
     numpages = {10},
     location = {Denver, CO, USA},
     isbn = {979-8-4007-0525-0/24/07},
     url = {https://doi.org/10.1145/3641519.3657521},
     doi = {10.1145/3641519.36575214},
     publisher = {ACM Press},
     address = {New York, NY, USA},
  }`

  let CopyBibTeX = async () => {
    try {
      await navigator.clipboard.writeText(bibTeX)
      msg = "BibTeX copied to clipboard!"
      setTimeout(() => (msg = ""), 3_000)
    } catch (err) {
      msg = `Error: copying to clipboard failed! ${err}`
    }
  }
  let ToggleDisplay = () => {
    collapsed = !collapsed
  }
</script>

<template>
  <div class="px-4 py-6 sm:px-6">
    <h3 class="text-base font-semibold leading-7 text-gray-900">
      Publications
    </h3>
    <hr class="mb-2" />
    <div class="flex">
      <div class="pr-4 drop-shadow-md">
        <img
          src="/media/hairmesh_rendering_preview.jpg"
          alt="Hairmesh Rendering Preview"
        />
      </div>
      <div>
        <div class="text-xl">
          <div class="my-2">
            <a
              href="https://www.gauravbhokare.com/"
              class="underline font-normal hover:font-bold"
              target="_blank">Gaurav Bhokare</a
            >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 640 512"
              class="w-6 h-6 inline relative -top-0.5 -left-1"
              ><path
                d="M579.8 267.7c56.5-56.5 56.5-148 0-204.5c-50-50-128.8-56.5-186.3-15.4l-1.6 1.1c-14.4 10.3-17.7 30.3-7.4 44.6s30.3 17.7 44.6 7.4l1.6-1.1c32.1-22.9 76-19.3 103.8 8.6c31.5 31.5 31.5 82.5 0 114L422.3 334.8c-31.5 31.5-82.5 31.5-114 0c-27.9-27.9-31.5-71.8-8.6-103.8l1.1-1.6c10.3-14.4 6.9-34.4-7.4-44.6s-34.4-6.9-44.6 7.4l-1.1 1.6C206.5 251.2 213 330 263 380c56.5 56.5 148 56.5 204.5 0L579.8 267.7zM60.2 244.3c-56.5 56.5-56.5 148 0 204.5c50 50 128.8 56.5 186.3 15.4l1.6-1.1c14.4-10.3 17.7-30.3 7.4-44.6s-30.3-17.7-44.6-7.4l-1.6 1.1c-32.1 22.9-76 19.3-103.8-8.6C74 372 74 321 105.5 289.5L217.7 177.2c31.5-31.5 82.5-31.5 114 0c27.9 27.9 31.5 71.8 8.6 103.9l-1.1 1.6c-10.3 14.4-6.9 34.4 7.4 44.6s34.4 6.9 44.6-7.4l1.1-1.6C433.5 260.8 427 182 377 132c-56.5-56.5-148-56.5-204.5 0L60.2 244.3z"
              /></svg
            >, Eisen Montalvo,
            <a
              href="https://diaz-elie.com/"
              class="underline font-normal hover:font-bold"
              target="_blank">Elie Diaz</a
            >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 640 512"
              class="w-6 h-6 inline relative -top-0.5 -left-1"
              ><path
                d="M579.8 267.7c56.5-56.5 56.5-148 0-204.5c-50-50-128.8-56.5-186.3-15.4l-1.6 1.1c-14.4 10.3-17.7 30.3-7.4 44.6s30.3 17.7 44.6 7.4l1.6-1.1c32.1-22.9 76-19.3 103.8 8.6c31.5 31.5 31.5 82.5 0 114L422.3 334.8c-31.5 31.5-82.5 31.5-114 0c-27.9-27.9-31.5-71.8-8.6-103.8l1.1-1.6c10.3-14.4 6.9-34.4-7.4-44.6s-34.4-6.9-44.6 7.4l-1.1 1.6C206.5 251.2 213 330 263 380c56.5 56.5 148 56.5 204.5 0L579.8 267.7zM60.2 244.3c-56.5 56.5-56.5 148 0 204.5c50 50 128.8 56.5 186.3 15.4l1.6-1.1c14.4-10.3 17.7-30.3 7.4-44.6s-30.3-17.7-44.6-7.4l-1.6 1.1c-32.1 22.9-76 19.3-103.8-8.6C74 372 74 321 105.5 289.5L217.7 177.2c31.5-31.5 82.5-31.5 114 0c27.9 27.9 31.5 71.8 8.6 103.9l-1.1 1.6c-10.3 14.4-6.9 34.4 7.4 44.6s34.4 6.9 44.6-7.4l1.1-1.6C433.5 260.8 427 182 377 132c-56.5-56.5-148-56.5-204.5 0L60.2 244.3z"
              /></svg
            >,
            <a
              href="http://cemyuksel.com"
              class="underline font-normal hover:font-bold"
              target="_blank">Cem Yuksel</a
            >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 640 512"
              class="w-6 h-6 inline relative -top-0.5 -left-1"
              ><path
                d="M579.8 267.7c56.5-56.5 56.5-148 0-204.5c-50-50-128.8-56.5-186.3-15.4l-1.6 1.1c-14.4 10.3-17.7 30.3-7.4 44.6s30.3 17.7 44.6 7.4l1.6-1.1c32.1-22.9 76-19.3 103.8 8.6c31.5 31.5 31.5 82.5 0 114L422.3 334.8c-31.5 31.5-82.5 31.5-114 0c-27.9-27.9-31.5-71.8-8.6-103.8l1.1-1.6c10.3-14.4 6.9-34.4-7.4-44.6s-34.4-6.9-44.6 7.4l-1.1 1.6C206.5 251.2 213 330 263 380c56.5 56.5 148 56.5 204.5 0L579.8 267.7zM60.2 244.3c-56.5 56.5-56.5 148 0 204.5c50 50 128.8 56.5 186.3 15.4l1.6-1.1c14.4-10.3 17.7-30.3 7.4-44.6s-30.3-17.7-44.6-7.4l-1.6 1.1c-32.1 22.9-76 19.3-103.8-8.6C74 372 74 321 105.5 289.5L217.7 177.2c31.5-31.5 82.5-31.5 114 0c27.9 27.9 31.5 71.8 8.6 103.9l-1.1 1.6c-10.3 14.4-6.9 34.4 7.4 44.6s34.4 6.9 44.6-7.4l1.1-1.6C433.5 260.8 427 182 377 132c-56.5-56.5-148-56.5-204.5 0L60.2 244.3z"
              /></svg
            >
          </div>
          <div class="font-bold my-2">
            Real-Time Hair Rendering with Hair Meshes
          </div>
          <div class="italic">SIGGRAPH 2024 Conference Papers</div>
        </div>
        <div class="mt-8">
          <div class="mb-4">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              class="w-8 h-8 inline relative -top-1"
              ><path
                d="M0 64C0 28.7 28.7 0 64 0L224 0l0 128c0 17.7 14.3 32 32 32l128 0 0 144-208 0c-35.3 0-64 28.7-64 64l0 144-48 0c-35.3 0-64-28.7-64-64L0 64zm384 64l-128 0L256 0 384 128zM176 352l32 0c30.9 0 56 25.1 56 56s-25.1 56-56 56l-16 0 0 32c0 8.8-7.2 16-16 16s-16-7.2-16-16l0-48 0-80c0-8.8 7.2-16 16-16zm32 80c13.3 0 24-10.7 24-24s-10.7-24-24-24l-16 0 0 48 16 0zm96-80l32 0c26.5 0 48 21.5 48 48l0 64c0 26.5-21.5 48-48 48l-32 0c-8.8 0-16-7.2-16-16l0-128c0-8.8 7.2-16 16-16zm32 128c8.8 0 16-7.2 16-16l0-64c0-8.8-7.2-16-16-16l-16 0 0 96 16 0zm80-112c0-8.8 7.2-16 16-16l48 0c8.8 0 16 7.2 16 16s-7.2 16-16 16l-32 0 0 32 32 0c8.8 0 16 7.2 16 16s-7.2 16-16 16l-32 0 0 48c0 8.8-7.2 16-16 16s-16-7.2-16-16l0-64 0-64z"
              /></svg
            >
            <a
              class="font-sans text-xl underline hover:font-bold ml-1"
              href="http://cemyuksel.com/research/hairmesh_rendering/Real-Time_Hair_Rendering_with_Hair_Meshes-SIGGRAPH24.pdf"
              >Paper</a
            > - 9.4MB
          </div>
          <div class="mb-4">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              class="w-8 h-8 inline relative -top-1"
              ><path
                d="M0 64C0 28.7 28.7 0 64 0L224 0l0 128c0 17.7 14.3 32 32 32l128 0 0 144-208 0c-35.3 0-64 28.7-64 64l0 144-48 0c-35.3 0-64-28.7-64-64L0 64zm384 64l-128 0L256 0 384 128zM176 352l32 0c30.9 0 56 25.1 56 56s-25.1 56-56 56l-16 0 0 32c0 8.8-7.2 16-16 16s-16-7.2-16-16l0-48 0-80c0-8.8 7.2-16 16-16zm32 80c13.3 0 24-10.7 24-24s-10.7-24-24-24l-16 0 0 48 16 0zm96-80l32 0c26.5 0 48 21.5 48 48l0 64c0 26.5-21.5 48-48 48l-32 0c-8.8 0-16-7.2-16-16l0-128c0-8.8 7.2-16 16-16zm32 128c8.8 0 16-7.2 16-16l0-64c0-8.8-7.2-16-16-16l-16 0 0 96 16 0zm80-112c0-8.8 7.2-16 16-16l48 0c8.8 0 16 7.2 16 16s-7.2 16-16 16l-32 0 0 32 32 0c8.8 0 16 7.2 16 16s-7.2 16-16 16l-32 0 0 48c0 8.8-7.2 16-16 16s-16-7.2-16-16l0-64 0-64z"
              /></svg
            >
            <a
              class="font-sans text-xl underline hover:font-bold ml-1"
              href="http://cemyuksel.com/research/hairmesh_rendering/Real-Time_Hair_Rendering_with_Hair_Meshes-SIGGRAPH24.pdf"
              >Supplemental Document</a
            > - 0.5MB
          </div>
          <div class="mb-4">
            <svg
              version="1.1"
              id="Layer_2_1_"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink"
              x="0px"
              y="0px"
              viewBox="0 0 72 72"
              enable-background="new 0 0 72 72"
              xml:space="preserve"
              class="w-8 h-8 inline relative -top-1"
            >
              <rect
                x="0.127"
                y="64.309"
                fill="#000"
                width="71.873"
                height="7.564"
              />
              <polygon
                fill="#000"
                points="36.063,0 0.127,18.379 0.127,24.338 72,24.338 72,18.379 "
              />
              <polygon
                fill="#000"
                points="22.556,60.57 4.593,60.57 9.098,55.164 9.098,32.655 4.593,28.078 22.556,28.078 17.89,32.655 
      17.89,55.164 "
              />
              <polygon
                fill="#000"
                points="45.045,60.57 27.082,60.57 31.587,55.164 31.587,32.655 27.082,28.078 45.045,28.078 40.379,32.655 
      40.379,55.164 "
              />
              <polygon
                fill="#000"
                points="67.805,60.57 49.842,60.57 54.347,55.164 54.347,32.655 49.842,28.078 67.805,28.078 63.139,32.655 
      63.139,55.164 "
              />
            </svg>
            <a
              class="font-sans text-xl underline hover:font-bold ml-1"
              href="https://doi.org/10.1145/3641519.3657521">Publisher's Page</a
            >
          </div>
          <div class="mb-4">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 576 512"
              class="w-8 h-8 inline relative -top-0.5"
              ><path
                d="M549.7 124.1c-6.3-23.7-24.8-42.3-48.3-48.6C458.8 64 288 64 288 64S117.2 64 74.6 75.5c-23.5 6.3-42 24.9-48.3 48.6-11.4 42.9-11.4 132.3-11.4 132.3s0 89.4 11.4 132.3c6.3 23.7 24.8 41.5 48.3 47.8C117.2 448 288 448 288 448s170.8 0 213.4-11.5c23.5-6.3 42-24.2 48.3-47.8 11.4-42.9 11.4-132.3 11.4-132.3s0-89.4-11.4-132.3zm-317.5 213.5V175.2l142.7 81.2-142.7 81.2z"
              /></svg
            >
            <a
              class="font-sans text-xl underline hover:font-bold ml-1"
              href="https://doi.org/10.1145/3641519.3657521">YouTube Video</a
            >
          </div>
          <div class="mb-2">
            <svg
              version="1.1"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink"
              x="0px"
              y="0px"
              viewBox="0 0 96 96"
              enable-background="new 0 0 96 96"
              xml:space="preserve"
              class="w-8 h-8 inline"
            >
              <g id="Layer_1">
                <path
                  fill="#FFFFFF"
                  stroke="#808080"
                  stroke-width="5"
                  stroke-miterlimit="10"
                  d="M93.118,23.5v65.779
          C55,62.676,53.809,86.103,36.206,88.618c-14.091,2.013-15.882-19.588-33.523-3.53V2.823h69.906L93.118,23.5z"
                />
                <g>
                  <path
                    d="M11.188,64.605V28.759h13.048c4,0,7.074,0.733,9.224,2.2c2.149,1.467,3.225,3.533,3.225,6.199
              c0,1.934-0.654,3.625-1.962,5.074c-1.309,1.45-2.979,2.458-5.012,3.025v0.1c2.549,0.316,4.587,1.258,6.111,2.825
              c1.525,1.566,2.288,3.475,2.288,5.725c0,3.282-1.175,5.887-3.525,7.812c-2.35,1.925-5.558,2.887-9.624,2.887H11.188z
               M19.261,34.708v8.499h3.55c1.666,0,2.979-0.404,3.937-1.212c0.958-0.808,1.438-1.92,1.438-3.337c0-2.633-1.967-3.95-5.899-3.95
              H19.261z M19.261,49.207v9.449h4.375c1.866,0,3.329-0.434,4.387-1.3c1.058-0.866,1.587-2.05,1.587-3.55
              c0-1.433-0.521-2.558-1.563-3.375c-1.042-0.816-2.496-1.225-4.362-1.225H19.261z"
                  />
                  <path
                    d="M47.233,34.958c-1.333,0-2.425-0.396-3.275-1.188c-0.85-0.791-1.274-1.762-1.274-2.912c0-1.183,0.425-2.15,1.274-2.899
              c0.85-0.75,1.941-1.125,3.275-1.125c1.35,0,2.445,0.375,3.287,1.125c0.841,0.75,1.263,1.716,1.263,2.899
              c0,1.2-0.422,2.184-1.263,2.95C49.679,34.575,48.583,34.958,47.233,34.958z M51.133,64.605h-7.899V39.008h7.899V64.605z"
                  />
                  <path
                    d="M65.78,61.63h-0.1v2.975h-7.899V26.709h7.899v16.148h0.1c1.95-2.983,4.725-4.474,8.324-4.474
              c3.3,0,5.841,1.133,7.624,3.399c1.783,2.267,2.675,5.366,2.675,9.299c0,4.267-1.041,7.691-3.124,10.273
              c-2.084,2.584-4.866,3.875-8.35,3.875C69.78,65.23,67.396,64.03,65.78,61.63z M65.556,50.832v2.625c0,1.65,0.475,3.017,1.425,4.1
              s2.166,1.624,3.649,1.624c1.8,0,3.195-0.695,4.188-2.087c0.991-1.392,1.487-3.362,1.487-5.912c0-2.116-0.454-3.771-1.362-4.962
              c-0.909-1.191-2.204-1.788-3.888-1.788c-1.583,0-2.896,0.592-3.937,1.775C66.076,47.391,65.556,48.932,65.556,50.832z"
                  />
                </g>
                <polygon
                  fill="#BEBEBE"
                  stroke="#808080"
                  stroke-width="5"
                  stroke-linejoin="bevel"
                  stroke-miterlimit="10"
                  points="72.512,2.823 
          72.512,23.5 93.113,23.5 	"
                />
              </g>
            </svg>
            <div
              class="font-sans text-xl underline hover:font-bold ml-1 inline cursor-pointer"
              on:click={ToggleDisplay}
            >
              BibTeX
            </div>
            <div class="inline cursor-pointer" on:click={CopyBibTeX}>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 448 512"
                class="w-6 h-6 inline relative -top-1"
                ><path
                  d="M384 336l-192 0c-8.8 0-16-7.2-16-16l0-256c0-8.8 7.2-16 16-16l140.1 0L400 115.9 400 320c0 8.8-7.2 16-16 16zM192 384l192 0c35.3 0 64-28.7 64-64l0-204.1c0-12.7-5.1-24.9-14.1-33.9L366.1 14.1c-9-9-21.2-14.1-33.9-14.1L192 0c-35.3 0-64 28.7-64 64l0 256c0 35.3 28.7 64 64 64zM64 128c-35.3 0-64 28.7-64 64L0 448c0 35.3 28.7 64 64 64l192 0c35.3 0 64-28.7 64-64l0-32-48 0 0 32c0 8.8-7.2 16-16 16L64 464c-8.8 0-16-7.2-16-16l0-256c0-8.8 7.2-16 16-16l32 0 0-48-32 0z"
                /></svg
              >
            </div>
            {#if msg !== ""}
              <div>
                {msg}
              </div>
            {/if}
          </div>
          {#if collapsed === false}
            <div
              class="ml-4 transition-opacity ease-in-out delay-150 duration-300"
            >
              <div>
                @inproceedings{"{"}Bhokare2024,
              </div>
              <div class="ml-8">
                author = {"{"}Gaurav Bhokare and Eisen Montalvo and Elie Diaz
                and Cem Yuksel{"}"},
              </div>
              <div class="ml-8">
                title = {"{"}Real-Time Hair Rendering with Hair Meshes{"}"},
              </div>
              <div class="ml-8">
                booktitle = {"{"}SIGGRAPH 2024 Conference Papers{"}"},
              </div>
              <div class="ml-8">series = {"{"}SIGGRAPH &#39;24{"}"},</div>
              <div class="ml-8">year = {"{"}2024{"}"},</div>
              <div class="ml-8">month = {"{"}07{"}"},</div>
              <div class="ml-8">pages = {"{"}61:1--61:10{"}"},</div>
              <div class="ml-8">articleno = {"{"}61{"}"},</div>
              <div class="ml-8">numpages = {"{"}10{"}"},</div>
              <div class="ml-8">location = {"{"}Denver, CO, USA{"}"},</div>
              <div class="ml-8">isbn = {"{"}979-8-4007-0525-0/24/07{"}"},</div>
              <div class="ml-8">
                url = {"{"}https://doi.org/10.1145/3641519.3657521{"}"},
              </div>
              <div class="ml-8">doi = {"{"}10.1145/3641519.36575214{"}"},</div>
              <div class="ml-8">publisher = {"{"}ACM Press{"}"},</div>
              <div class="ml-8">address = {"{"}New York, NY, USA{"}"},</div>
              {"}"}
            </div>
          {/if}
        </div>
      </div>
    </div>
  </div>
</template>
