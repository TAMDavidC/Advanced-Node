# Notes

## Sending an HTML File to the Browser

~~~ javascript
// set header content type
res.setHeader(`Content-Type`, `text/html`);

// snd an html file
fs.readFile(`./views/index.html`, (err, data) => {
    if (err){
        console.log(err);
        res.end();
    }
    else{
        res.write(data);
        res.end();
    }
})
~~~

## Sending HTML to The Browser

~~~ Javascript
// set header content type
res.setHeader(`Content-Type`, `text/html`);

res.write(`<head><link rel="styleshet href="#></head>`);
res.write(`<p>Hello, ninjas</p>`);
res.write(`<p>Hello again, ninjas</p>`);
res.end();
~~~
