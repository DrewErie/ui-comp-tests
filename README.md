A small `webpack` based boilerplate for creating custom Boomi Flow UI components.

## Setup

- Download or clone this repo
- `npm install`

## Usage

Create the custom component in `index.tsx`, or in separate `.tsx` files and import them into `index.tsx`. Any custom styles can
be added in `index.css`.

## Testing

You can start the local development server with `npm run dev`. This will serve the compiled javascript and css at `http://localhost:8080/dist/bundle.js` and `http://localhost:8080/dist/styles.css`.

The easiest way to test a custom component would be to create a custom player then add references to the `bundle.js` and `styles.css`
as custom resources, more information on loading custom resources can be found here: https://docs.manywho.com/adding-custom-javascript-and-stylesheets/

The local development server won't be accessible from `flow.manywho.com`, you can workaround this by using a tunnel like https://ngrok.com/download

Run ngrok with: `ngrok http 8080`

ngrok will provide a url like `https://ad7c2b13.ngrok.io` that will point to `http://localhost:8080`, for example you would add the following as custom resources in a player:

```
https://ad7c2b13.ngrok.io/dist/bundle.js,
https://ad7c2b13.ngrok.io/dist/styles.css
```