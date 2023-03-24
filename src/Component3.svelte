<script>
  export let headers;
  export let data;
</script>

<body>
  <table>
    <thead>
      {#each headers as columnHeading}
        <th>{columnHeading}</th>
      {/each}
    </thead>
    <tbody>
      {#each data as row}
        <tr>
          {#each Object.values(row) as cell}
            <td>{cell}</td>
          {/each}
        </tr>
      {/each}
    </tbody>
  </table>
</body>

<style>
  table {
    margin: 0px auto;
    width: 80%;
    border-collapse: collapse;
    font-size: 20px;
    text-align: left;
  }
  thead {
    background-color: rgb(216, 216, 216);
  }
  th {
    padding: 5px;
  }
  tr,
  td {
    padding: 5px;
    margin: 50px;
    background-color: rgb(238, 238, 238);
    border-bottom: 1px solid rgb(228, 227, 227);
  }
</style>
