# vite-heliosweb-template-main-ui
Example of Helios-Web project using Vite with additional changes for helios-web-ui.

# Setup:
1. Install nodejs/npm
2. Ensure helios-web-ui bundled components (drawer-component.es, drawer-component.umd) are located in the dist folder
3. Include a div in index.html for the drawer component

   ```
   <div id="drawer-container"></div>
   ```
   
5. In main.js:
     1. Import react and the drawer component:

         ```
         import React from 'react';
         import ReactDOM from 'react-dom/client';
         import DrawerComponent from './dist/drawer-component.es';
         ```

     2. Declare drawer props to send the helios object and render the drawer component:
  
        ```
          const drawerProps = {
            helios,
          };

          const root = ReactDOM.createRoot(document.getElementById('drawer-container'));
          root.render(
            React.createElement(DrawerComponent, drawerProps)
          );
        ```
        
6. npm install
7. npm run dev
