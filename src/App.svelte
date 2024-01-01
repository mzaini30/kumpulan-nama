<script>
  import Login from "login-zen";
  import { fakerID_ID as faker } from "@faker-js/faker";

  let listNama = [];

  function generateListNama() {
    listNama = [];
    for (let x = 1; x <= 20; x++) {
      listNama = [...listNama, faker.person.fullName()];
    }
  }
  generateListNama();
  setInterval(generateListNama, 10000);
</script>

<svelte:head>
  <title>Kumpulan Nama</title>
</svelte:head>

<Login platform="Kumpulan Nama"></Login>

<div class="p-3">
  <ol>
    {#each listNama as nama}
      <li class="list-decimal ml-5">{nama}</li>
    {/each}
  </ol>
</div>
