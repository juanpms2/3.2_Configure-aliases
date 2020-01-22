# Path mapping en Webpack y TypeScript

Lo que conseguimos con el path mapping o alias es mapear las rutas de nuestros archivos para unas importaciones más limpias y con menos probabilidad de cometer un fallo.

### Webpack.config

Añadimos el siguiente código con nuestras rutas

    resolve: {
        alias: {
            api: path.resolve(__dirname, './src/api/'),
            assets: path.resolve(__dirname, './src/assets/'),
            img: path.resolve(__dirname, './src/assets/img'),
            imgGalery: path.resolve(__dirname, './src/assets/img-galery'),      
            layout: path.resolve(__dirname, './src/layout/'),
            scss: path.resolve(__dirname, './src/scss/'),
        },
        extensions: [".js", ".ts", ".jsx", ".tsx"]
    },

### tsconfig.json

En la configuración de TypeScript también añadimos nuestras rutas. Es probable que tengas que reiniciar el servidor de TypeScrip o Visual Studio Code si es el editor que usas.

    "compilerOptions": {
        "moduleResolution": "node",
        "baseUrl": "src",
        "paths": {
            "api": ["api"],
            "assets": ["assets"],
            "img": ["img"],
            "imgGalery": ["imgGalery"],
            "layout": ["layout"],
            "scss": ["scss"]
        }
    },

Para más información:
    - https://www.basefactor.com/configuring-aliases-in-webpack-vs-code-typescript-jest
    - https://medium.com/@insomniocode/typescript-path-mapping-22459288d3db
<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

