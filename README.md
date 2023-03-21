## Notes

#### Current React Version

```
"react": "^18.2.0",
"react-dom": "^18.2.0",
"react-scripts": "5.0.1"
```

## About Project

#### .env vars

```
-REACT_APP_AUTH_DOMAIN=
-REACT_APP_AUTH_CLIENT_ID=
-REACT_APP_STRIPE_PUBLIC_KEY=
-REACT_APP_STRIPE_SECRET_KEY=

```

#### Colors

- get shades from tailwind.css

- [tailwind color shades] (https://tailwindcss.com/docs/customizing-colors#color-palette-reference)

```css
:root {
  /* dark shades of primary color*/
  --clr-primary-1: #0c4a6e;
  --clr-primary-2: #075985;
  --clr-primary-3: #0369a1;
  --clr-primary-4: #0284c7;
  /* primary/main color */
  --clr-primary-5: #0ea5e9;
  /* lighter shades of primary color */
  --clr-primary-6: #38bdf8;
  --clr-primary-7: #7dd3fc;
  --clr-primary-8: #bae6fd;
  --clr-primary-9: #e0f2fe;
  --clr-primary-10: #f0f9ff;
  /* darkest grey - used for headings */
  --clr-grey-1: #0f172a;
  --clr-grey-2: #1e293b;
  --clr-grey-3: #334155;
  --clr-grey-4: #475569;
  /* grey used for paragraphs */
  --clr-grey-5: #64748b;
  --clr-grey-6: #94a3b8;
  --clr-grey-7: #cbd5e1;
  --clr-grey-8: #e2e8f0;
  --clr-grey-9: #f1f5f9;
  --clr-grey-10: #f8fafc;
  --clr-white: #fff;
}
```

#### Logo

- Figma
- Code Version
- create Logo.js

components/Logo

```js
import styled from "styled-components";
const Logo = () => {
  return (
    <Wrapper>
      <span>Furni</span>Mart
    </Wrapper>
  );
};
const Wrapper = styled.h3`
  margin-bottom: 0;
  color: var(--clr-grey-1);
  span {
    color: var(--clr-primary-5);
  }
`;

export default Logo;
```

- replace in Navbar and Sidebar

#### Favicon

- [favicon.io](https://favicon.io/)
- I used primary-5 color value
- replace favicon.ico in public

#### Main Images - First Approach

- get images, go with pexels
- [pexels](https://www.pexels.com/)
- replace in src/assets
- hero-bcg.jpeg
- hero-bcg-2.jpeg

#### Main Images - Second Approach

- [undraw](https://undraw.co/illustrations)
- use primary color
- hero-bcg.svg

components/Hero

```js
<article className="img-container">
  <img src={heroBcg} alt="nice table" className="main-img" />
</article>
```

```css
gap: 2rem;
```

#### Serverless Functions

- in functions create
- products.js
- single-product.js

```js
exports.handler = async (event, context, cb) => {
  return {
    statusCode: 200,
    body: "products route",
  };
};
```

- restart the server "npm run dev"
