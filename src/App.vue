<template>
  <div class="pricing-header px-3 py-3 pt-md-5 pb-md-4 mx-auto text-center">
    <h3 class="display-5">Product Infomation</h3>
    <router-link to="/about">Back</router-link>
</div>

<div class="container">
    <form >
        <div class="form-group row">
        <label for="inputPassword" class="col-sm-3 col-form-label">Product name</label>
        <div class="col-sm-9">
            <input type="text" class="form-control" />
           
        </div>
        </div>
        <div class="form-group row">
            <label for="inputPassword" class="col-sm-3 col-form-label">Product price</label>
            <div class="col-sm-9">
                <input type="text" class="form-control" />
            </div>
        </div>
        <div class="form-group row">
            <label for="inputPassword" class="col-sm-3 col-form-label">Product description</label>
            <div class="col-sm-9">
                <textarea class="form-control" rows="3"></textarea>
            </div>
        </div>
        <div class="form-group row">
            <label for="inputPassword" class="col-sm-3 col-form-label"></label>
            <div class="col-sm-9">
                <button type="submit" class="btn btn-primary">Save</button> &nbsp;
                <button type="reset" class="btn btn-danger">Cancel</button>
            </div>
        </div>
    </form>
</div>
  <!-- <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav> -->
  <!-- <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav> -->
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
