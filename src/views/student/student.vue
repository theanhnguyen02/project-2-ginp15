<template>
  <div>

  </div>
</template>

<script>



  export default {
    components: {
      PageTitle,
      Tabs,
      quillEditor,
      ckeditor: CKEditor.component
    },
    data: () => ({
      heading: 'WYSIWYG Editors',
      subheading: 'Need to add formatting to your forms? Use these Vue2 widgets.',
      icon: 'pe-7s-like icon-gradient bg-love-kiss',

      tabs: TABS,
      currentTab: 'tab1',

      editor2: ClassicEditor,
      editorData: '<p>Content of the editor.</p>',
      editorConfig: {
        // The configuration of the editor.
      },

      content: '' +
      '<h1>This is a heading</h1><br><p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.</p>\n' +
      '\n' +
      '<p>Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim. Donec pede justo, fringilla vel, aliquet nec, vulputate eget, arcu.</p>\n' +
      '\n' +
      '<p>In enim justo, rhoncus ut, imperdiet a, venenatis vitae, justo. Nullam dictum felis eu pede mollis pretium. Integer tincidunt. Cras dapibus. Vivamus elementum semper nisi. Aenean vulputate eleifend tellus.</p>\n' +
      '\n' +
      '<p>Vestibulum purus quam, scelerisque ut, mollis sed, nonummy id, metus. Nullam accumsan lorem in dui. Cras ultricies mi eu turpis hendrerit fringilla. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; In ac dui quis mi consectetuer lacinia. Nam pretium turpis et arcu. Duis arcu tortor, suscipit eget, imperdiet nec, imperdiet iac</p>',
      editorOption: {
        // some quill options
      }


    }),

    methods: {
      handleClick(newTab) {
        this.currentTab = newTab;
      },
    },

    computed: {
      editor() {
        return this.$refs.myQuillEditor.quill
      }
    },
  }
  
</script>

<style lang="css">
  @import '~quill/dist/quill.core.css';
  @import '~quill/dist/quill.snow.css';
  @import '~quill/dist/quill.bubble.css';
</style>


