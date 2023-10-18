<template>
  <ejs-pdfviewer
    ref="pdfViewer"
    :serviceUrl="serviceUrl"
    :documentPath="documentPath">
  </ejs-pdfviewer>
</template>

<script setup>

import { provide } from 'vue';
import { PdfViewerComponent as EjsPdfviewer, Toolbar, Magnification, Navigation, LinkAnnotation, BookmarkView, 
  ThumbnailView, Print, TextSelection, TextSearch, Annotation, FormDesigner, FormFields } from '@syncfusion/ej2-vue-pdfviewer';

const serviceUrl = 'https://localhost:44309/pdfviewer';
const documentPath = 'PDF_Succinctly.pdf';
const pdfViewer = null;

provide('PdfViewer', [ Toolbar, Magnification, Navigation, LinkAnnotation, BookmarkView, ThumbnailView, 
                       Print, TextSelection, TextSearch, Annotation, FormDesigner, FormFields]);
</script>

<style>

  @import './node_modules/@syncfusion/ej2-base/styles/material.css';  
  @import './node_modules/@syncfusion/ej2-buttons/styles/material.css';
  @import './node_modules/@syncfusion/ej2-dropdowns/styles/material.css';  
  @import './node_modules/@syncfusion/ej2-inputs/styles/material.css';  
  @import './node_modules/@syncfusion/ej2-navigations/styles/material.css';
  @import './node_modules/@syncfusion/ej2-popups/styles/material.css';
  @import './node_modules/@syncfusion/ej2-splitbuttons/styles/material.css';
  @import './node_modules/@syncfusion/ej2-lists/styles/material.css';
  @import './node_modules/@syncfusion/ej2-vue-pdfviewer/styles/material.css';
  #pdfViewer {
    height: 640px;
  } 

</style>