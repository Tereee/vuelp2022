<!--<script>-->

<!--import {deleteCategorie, getCategorie} from '../api/categorie'-->

<!--export default {-->
<!--  name: 'CategorieDelete',-->
<!--  data () {-->
<!--    return {-->
<!--      id: ''-->
<!--    }-->
<!--  },-->
<!--  async mounted() {-->
<!--    this.id = this.$route.params.id-->
<!--    await getCategorie(this.id)-->
<!--  },-->
<!--  methods: {-->
<!--    async mounted() {-->
<!--      await deleteCategorie(this.id).then((reponse) => {-->
<!--        console.log(reponse)-->
<!--        //this.confirm = true //activation d'un bandeau de confirmation-->
<!--        this.$router.push('/categories') //redirection-->
<!--      })-->
<!--    }-->
<!--  }-->
<!--}-->

<!--</script>-->