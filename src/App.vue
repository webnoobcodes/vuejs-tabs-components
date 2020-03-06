<template>
  <div id="app">
    <Tabs>
      <Tab name="description" selected="true">
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dolorum error autem dignissimos nobis illum temporibus 
          voluptate laboriosam eius consequatur! Labore laborum ducimus, culpa sit neque molestias dignissimos natus 
          minima sed recusandae ipsa necessitatibus obcaecati vel eligendi voluptatem, provident in non ad saepe veniam 
          eveniet cumque, fugit unde eaque! Doloribus, iusto?
        </p>
      </Tab>
      <Tab name="list">
        <ul>
          <li>Item 1</li>
          <li>Item 2</li>
          <li>Item 3</li>
          <li>Item 4</li>
          <li>Item 5</li>
        </ul>
      </Tab>
      <Tab name="table">
        <table>
          <tr>
            <th>Name</th>
            <th>Value</th>
          </tr>
          <tr>
            <td>Cheese</td>
            <td>Yellow</td>
          </tr>
          <tr>
            <td>Apple</td>
            <td>Red</td>
          </tr>
        </table>
      </Tab>
    </Tabs>
  </div>
</template>

<script>
  import Tab from '@/components/Tab'
  import Tabs from '@/components/Tabs'

  export default {
    name: 'App',
    components: {
      Tab,
      Tabs
    }
  }
</script>

<style lang="scss">
  body {
    background-color: #45443F;
    color: #fefefe;
  }

  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    font-size: 2rem;  
  }

  th, td {
    padding: 5px;
    border: 1px solid #fefefe;
    text-align: center;
  }
</style>
