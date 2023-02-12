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
        "@single-spa/mf-contact": "http://localhost:4201/main.js",
        "@single-spa-example/root-config": "//localhost:9000/single-spa-example-root-config.js"
    }
}
</script>
```

And add import frontend route in layout html (microfrontend-layout.html)

```
<single-spa-router>
  <main>
    <route default>
      <application name="@single-spa/welcome"></application>
    </route>
    <route path="contact">
      <application name="@single-spa/mf-contact"></application>
    </route>
  </main>
</single-spa-router>
```
---
You can get more information on the following link:

https://medium.com/@romeodavide91/single-spa-framework-ec9a1160f4ad