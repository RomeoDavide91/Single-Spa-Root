# Root Single Spa #

## Start ##

To launch singlespa root run the command:

```
npm start
```

The application will start on port 9000 of localhost

---
## Config ##

You can add microfrontends in the index.ejs file snippet:

```
<script type="systemjs-importmap">
{
    "imports": {
        "@single-spa/welcome": "https://unpkg.com/single-spa-welcome/dist/single-spa-welcome.js",
        "@single-spa-example/root-config": "//localhost:9000/single-spa-example-root-config.js"
    }
}
</script>
```

---
You can get more information on the following link:

https://medium.com/@romeodavide91/single-spa-framework-ec9a1160f4ad