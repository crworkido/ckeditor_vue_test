<template>
  <div class="hello">
    <ckeditor ref="eddy" :editor="editor" v-model="editorData" :config="editorConfig" ></ckeditor>

    <hr/>
    <button @click="showcode">Show code </button>
    <hr/>
    <textarea v-model="editorData" readonly="true"></textarea>
  </div>
</template>

<script> 
//import ClassicEditor from '@ckeditor/ckeditor5-build-classic'
import ClassicEditor from '@ckeditor/ckeditor5-editor-classic/src/classiceditor'


import Essentials from "@ckeditor/ckeditor5-essentials/src/essentials";
//import UploadAdapter from "@ckeditor/ckeditor5-adapter-ckfinder/src/uploadadapter";
import Alignment from "@ckeditor/ckeditor5-alignment/src/alignment";
import Autoformat from "@ckeditor/ckeditor5-autoformat/src/autoformat"
import Bold from "@ckeditor/ckeditor5-basic-styles/src/bold"
import Base64UploadAdapter from "@ckeditor/ckeditor5-upload/src/adapters/base64uploadadapter";
import Italic from "@ckeditor/ckeditor5-basic-styles/src/italic";
import Underline from "@ckeditor/ckeditor5-basic-styles/src/underline";
import Strikethrough from "@ckeditor/ckeditor5-basic-styles/src/strikethrough";
//import CKFinder from "@ckeditor/ckeditor5-ckfinder/src/ckfinder";
import Code from "@ckeditor/ckeditor5-basic-styles/src/code";
import CodeBlock from "@ckeditor/ckeditor5-code-block/src/codeblock";
import Font from "@ckeditor/ckeditor5-font/src/font";
import Subscript from "@ckeditor/ckeditor5-basic-styles/src/subscript";
import Superscript from "@ckeditor/ckeditor5-basic-styles/src/superscript";
import Highlight from "@ckeditor/ckeditor5-highlight/src/highlight";
import Heading from "@ckeditor/ckeditor5-heading/src/heading";
import HorizontalLine from "@ckeditor/ckeditor5-horizontal-line/src/horizontalline";
import Image from "@ckeditor/ckeditor5-image/src/image";
import AutoImage from "@ckeditor/ckeditor5-image/src/autoimage";
import ImageCaption from "@ckeditor/ckeditor5-image/src/imagecaption";
import ImageInsert from "@ckeditor/ckeditor5-image/src/imageinsert";
import ImageStyle from "@ckeditor/ckeditor5-image/src/imagestyle";
import ImageToolbar from "@ckeditor/ckeditor5-image/src/imagetoolbar";
//import ImageUpload from "@ckeditor/ckeditor5-image/src/imageupload";
import ImageResize from "@ckeditor/ckeditor5-image/src/imageresize";
//import EasyImage from "@ckeditor/ckeditor5-easy-image/src/easyimage";
import Indent from "@ckeditor/ckeditor5-indent/src/indent";
import Link from "@ckeditor/ckeditor5-link/src/link";
import IndentBlock from "@ckeditor/ckeditor5-indent/src/indentblock";
import List from "@ckeditor/ckeditor5-list/src/list";
//import MediaEmbed from "@ckeditor/ckeditor5-media-embed/src/mediaembed";
import Paragraph from "@ckeditor/ckeditor5-paragraph/src/paragraph";
import PageBreak from "@ckeditor/ckeditor5-page-break/src/pagebreak";
import PasteFromOffice from "@ckeditor/ckeditor5-paste-from-office/src/pastefromoffice";
import Title from "@ckeditor/ckeditor5-heading/src/title";
import Table from "@ckeditor/ckeditor5-table/src/table";
import TableToolbar from "@ckeditor/ckeditor5-table/src/tabletoolbar";
import TextTransformation from "@ckeditor/ckeditor5-typing/src/texttransformation";
import TodoList from "@ckeditor/ckeditor5-list/src/todolist";
import BlockToolbar from "@ckeditor/ckeditor5-ui/src/toolbar/block/blocktoolbar";
import HeadingButtonsUI from "@ckeditor/ckeditor5-heading/src/headingbuttonsui";
import ParagraphButtonUI from "@ckeditor/ckeditor5-paragraph/src/paragraphbuttonui";



//import FontFamily from '@ckeditor/ckeditor5-font/src/fontfamily.js'
//import FontSize from '@ckeditor/ckeditor5-font/src/fontsize.js'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
//    ckeditor: CKEditor.component
  }, 
  methods: {
    showcode: function() {
      console.log("show me the code")
      console.log(this.$refs.eddy)
    }
  },
  data() {
    return {
      editor: ClassicEditor,
      editorData: '<p>That\'s all foolks!  </p>',
      editorConfig: {
        plugins: [
          Alignment,
          Highlight,
          Essentials,
 //         UploadAdapter,
          Autoformat,
          Bold,
          Base64UploadAdapter,
          Italic,
          Underline,
          Strikethrough,
          Code,
          CodeBlock,
          Font,
          Subscript,
          Superscript,
 //         CKFinder,
          Heading,
          HorizontalLine,
//          EasyImage,
          Image,
          AutoImage,
          ImageCaption,
          ImageInsert,
          ImageStyle,
          ImageToolbar,
//          ImageUpload,
          ImageResize,
          Indent,
          IndentBlock,
          Link,
          List,
//          MediaEmbed,
          Paragraph,
          PasteFromOffice,
          Title,
//          FileRpository,
          Table,
          TableToolbar,
          TextTransformation,
          TodoList,
          BlockToolbar,
          ParagraphButtonUI,
          HeadingButtonsUI,
          PageBreak
	],
        fontFamily: {
          options: [
            'Arial, sans-serif',
            'Times',
            'Courier'
         ]
	},
        toolbar: {
          items:[
           'heading', '|',
        'fontFamily', 'fontsize','fontColor', 'fontBackgroundColor', '|',
        'alignment', 
        'bold', 'italic', 'strikethrough', 'underline', 'subscript', 'superscript', 'horizontalLine', '|',
        'link', '|',
        'outdent', 'indent', '|',
        'bulletedList', 'numberedList', 'todoList', '|',
        'code', 'codeBlock', '|',
        'insertTable', '|',
        'image','imageInsert', 'blockQuote', '|',
        'undo', 'redo' 
          ]
	}
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
