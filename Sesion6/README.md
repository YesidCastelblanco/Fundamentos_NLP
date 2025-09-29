# Consideraciones para la ejecución del Proyecto en Kaggle

Este proyecto utiliza la librería **Hugging Face** y requiere autenticación mediante un token personal.  
Para garantizar la seguridad, el token **no está incluido en este repositorio** y debe configurarse en **Kaggle** antes de ejecutar el notebook.

---
## 🔑 1. Generar un Token en Hugging Face
1. Ingrese a [Hugging Face Settings → Tokens](https://hf.co/settings/tokens).  
2. Haga clic en **New Token**.  
3. Seleccione permisos con rol `read` (solo lectura).  
4. Copie el valor del token generado y guárdelo en un lugar seguro.  

---

## 🔐 2. Configurar un Secreto en Kaggle
1. Vaya a [Kaggle → Add-ons] 
2. Desplácese hasta la sección **Secrets**.  
3. En el apartado **Secrets**, haga clic en **“Create New Secret”**.  
4. Complete el formulario:  
   - **Label:** `HF_TOKEN`  
   - **Value:** (pegue aquí su token de Hugging Face).  
5. Guarde los cambios.  

A partir de este momento, Kaggle inyectará automáticamente el valor del token en la variable de entorno `HF_TOKEN` cada vez que se ejecute este notebook.

---
