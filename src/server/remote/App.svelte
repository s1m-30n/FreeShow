<script lang="ts">
  import Center from "../common/components/Center.svelte"
  import Error from "../common/components/Error.svelte"
  import Auth from "./components/Auth.svelte"
  import Main from "./components/Main.svelte"
  import { translate } from "./util/helpers"
  import { initSocket } from "./util/socket"
  import { dictionary, errors, isConnected, password } from "./util/stores"

  initSocket()

  // test API actions
  // send("API:get_playlists")
</script>

<Error errors={$errors} />

{#if $isConnected}
  <Main />
{:else if $password.required}
  <Auth />
{:else}
  <Center>
    {translate("remote.loading", $dictionary)}
  </Center>
{/if}

<svelte:head>
<<<<<<< HEAD
  <style>
    :root {
      --primary: #292c36;
      --primary-lighter: #363945;
      --primary-darker: #191923;
      --primary-darkest: #12121c;
      --text: #f0f0ff;
      --textInvert: #131313;
      --secondary: #27a8f5;
      --secondary-opacity: #27a9f55e;
      --secondary-text: #f0f0ff;
=======
    <style>
        :root {
            --primary: #242832;
            --primary-lighter: #2f3542;
            --primary-darker: #191923;
            --primary-darkest: #12121c;
            --text: #f0f0ff;
            --textInvert: #131313;
            --secondary: #f0008c;
            --secondary-opacity: rgba(240, 0, 140, 0.5);
            --secondary-text: #f0f0ff;
            --transparent: #232530;

            --accent: #90caf9;

            --connected: #27a827;
            --disconnected: #a82727;

            --red: rgb(255 0 0 / 0.25);
>>>>>>> 1e60c9d2e7c3a6d9b5b111651132670e59b9d90c

      --hover: rgb(255 255 255 / 0.05);
      --focus: rgb(255 255 255 / 0.1);
      /* --active: rgb(230 52 156 / .8); */

<<<<<<< HEAD
      /* --navigation-width: 18vw; */
      --navigation-width: 300px;
    }
=======
            /* --navigation-width: 18vw; */
            --navigation-width: 300px;

            --font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen-Sans, Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
            --font-size: 1em;
        }
>>>>>>> 1e60c9d2e7c3a6d9b5b111651132670e59b9d90c

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      user-select: none;

      outline-offset: -4px;
      outline-color: var(--secondary);
    }

<<<<<<< HEAD
    html {
      height: 100%;
    }

    body {
      background-color: var(--primary);
      color: var(--text);
      /* transition: background-color 0.5s; */

      font-family: sans-serif;
      font-size: 1.5em;

      height: 100%;
      /* width: 100vw;
height: 100vh; */
    }
=======
        html {
            height: 100%;
            font-family: var(--font-family);
            font-size: var(--font-size);
        }

        body {
            background-color: var(--primary);
            color: var(--text);
            transition: background-color 0.5s;

            font-family: inherit;
            font-size: inherit;

            height: 100%;
            display: flex;
            flex-direction: column;
            touch-action: manipulation;
        }

        /* Match FreeShow main app scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
            height: 8px;
        }
        ::-webkit-scrollbar-track,
        ::-webkit-scrollbar-corner {
            background: rgb(255 255 255 / 0.05);
        }
        ::-webkit-scrollbar-thumb {
            background: rgb(255 255 255 / 0.3);
            border-radius: 8px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: rgb(255 255 255 / 0.5);
        }

        /* Firefox scrollbar */
        * {
            scrollbar-width: thin;
            scrollbar-color: rgb(255 255 255 / 0.3) rgb(255 255 255 / 0.05);
        }
>>>>>>> 1e60c9d2e7c3a6d9b5b111651132670e59b9d90c

    h1 {
      color: var(--secondary);
      text-align: center;
      padding-bottom: 20px;
    }

<<<<<<< HEAD
    h2 {
      color: var(--secondary);
      text-align: center;
      font-size: 1.3em;
      padding: 0.2em 0.8em;
      width: 100%;
      overflow: hidden;
      text-overflow: ellipsis;
      white-space: nowrap;
    }
=======
        h2 {
            color: var(--secondary);
            text-align: center;
            font-size: 1.3em;
            padding: 0;
            width: 100%;
            overflow: hidden;
            text-overflow: ellipsis;
            white-space: nowrap;
            margin: 0;
        }
>>>>>>> 1e60c9d2e7c3a6d9b5b111651132670e59b9d90c

    .header {
      display: flex;
      justify-content: center;
      align-items: center;

      background-color: var(--primary-darker);
      color: var(--text);
      width: 100%;

<<<<<<< HEAD
      padding: 0.2em 0.8em;
      font-weight: 600;
      font-size: 0.9em;
    }
=======
            height: 56px; /* Match show item height */
            font-weight: 600;
            font-size: 1.05em;
        }
>>>>>>> 1e60c9d2e7c3a6d9b5b111651132670e59b9d90c

    /* CHECKERED */

    .checkered {
      /* background-color: var(--transparent); */
      background: repeating-conic-gradient(
          rgba(70, 70, 80, 0.1) 0% 25%,
          transparent 0% 50%
        )
        50% / 26px 26px;
    }
  </style>
</svelte:head>
