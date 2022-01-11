<template>
  <div class="about mt-5 pt-5 container">
    <h1>Création d'une catégorie</h1>
    <div v-if="confirm">
      Catégorie ajoutée avec succès !
    </div>
    <div>
      <label class="form-label" for="libelle">Libellé</label>
      <input class="form-control" type="text" name="libelle" v-model="libelle"  id="libelle"/>
    </div>
    <br>
    <div>
      <label class="form-label" for="couleur">Couleur</label>
      <input class="form-control" type="text" name="couleur" v-model="couleur"  id="couleur"/>
    </div>
    <br>
    <div>
      <button class="btn btn-primary" @click="ajoutCategorie">Ajouter</button>
    </div>
    <br>
    <a class="btn btn-info float-start" href="/messages">Retour</a>
  </div>
</template>

<script>

import {postCategorie} from '../api/categorie'

export default {
  name: 'NouvellesCategorie',
  data () {
    return {
      couleur: '',
      libelle: '',
      confirm: false
    }
  },
  methods: {
    async ajoutCategorie() {
      await postCategorie({
        couleur: this.couleur,
        libelle: this.libelle
      }).then((reponse) => {
        console.log(reponse)
        //this.confirm = true //activation d'un bandeau de confirmation
        this.$router.push('/categories') //redirection
      })
    }
  }
}

</script>
