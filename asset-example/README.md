# Asset Example

So you want to serve you're own images using the Kibana server. It's as easy as creating a basic plugin using the example code in this directory.

1. Copy `asset-example` to `KIBANA/installedPlugins/assets`
2. Put your images into `KIBANA/installedPlugins/assets/public`
3. Now you can refrence your images using the following path prefix `/plugins/assets/`

This can be useful if you want to have a library of images that you want to use in conjunction with a field formater. Let's say your had a field named `status` and you wanted to display `red.png`, `green.png`, or `yellow.png` instead of the `status` value. 

1. Create a `Url` field formater for the `status` field
2. Set `type` to `image`
3. Set `Url Template` to `/plugins/assets/{{value}}.png` 
4. Profit!
