<template>
  <div class="resume">
    
    <custom-nav />
    <b-container class="bv-example-row">
    <b-card title="NEW RESUME" tag="article">
    
    
    <h5 style="text-align: left;">ICON</h5>
    <b-form-input v-model="icon"
                  type="text"
                  placeholder="http"></b-form-input>
    
    <h5 style="text-align: left;">BANNER</h5>
    <b-form-input v-model="banner"
                  type="text"
                  placeholder="http"></b-form-input>

    <h5 style="text-align: left;">SUMMARY</h5>
    <b-form-textarea id="summary"
                     v-model="summary"
                     placeholder="Write the summary"
                     :rows="3"
                     :max-rows="6">
    </b-form-textarea>
    
    <h5 style="text-align: left;">SKILLS</h5>
    <b-form-textarea id="skills"
                     v-model="skills"
                     placeholder="Java, Python, ..."
                     :rows="3"
                     :max-rows="6">
    </b-form-textarea>
    
    <h5 style="text-align: left;">EXPERIENCE</h5>
    <b-form-textarea id="history"
                     v-model="history"
                     placeholder="Software developer in Dyamsoft"
                     :rows="3"
                     :max-rows="6">
    </b-form-textarea>

    <h5 style="text-align: left;">EDUCATION</h5>
    <b-form-textarea id="hobbies"
                     v-model="education"
                     placeholder="Software developer in UMSS"
                     :rows="3"
                     :max-rows="6">
    </b-form-textarea>
    
    <h5 style="text-align: left;">ADDICTIONAL ACTIVITIES</h5>
    <b-form-textarea id="hobbies"
                     v-model="hobbies"
                     placeholder="Football, Running, ..."
                     :rows="3"
                     :max-rows="6">
    </b-form-textarea>
  
    <b-button v-on:click="save">Save</b-button>
  </b-card>
  </b-container>
  </div>
</template>

<script>

export default {
  name: 'ResumeCreate',
  data () {
    return {
      icon: '',
      banner: '',
      summary: '',
      skills: '',
      education: '',
      history: '',
      hobbies: ''
    }
  },
  methods: {
    save: function (event) {
      this.$router.push('/Resume/' + (Math.floor(Math.random() * (6 - 1 + 1)) + 1))
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
