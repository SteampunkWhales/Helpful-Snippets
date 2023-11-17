<!-- v-for -->
    <!-- the div tag will repeat once for each review in reviews -->
    <!-- you must use v-bind:key with the v-for -->
    <!-- the key must be defined, because of syntax, it exists for Vue managing purposes so it doesn't have to loop through everything. It is performance enhancing-->
    <div class="review" v-for="review in reviews" v-bind:key="review.id"/>
  

<!-- v-for with n -->
    <!-- it will loop for a number -->
    <div class="rating" v-for="n in review.rating" v-bind:key="n">
        <img src="../assets/star.png" />
    </div>

<!-- v-bind -->
    <!-- whenever you need to reactively change an HTML attribute, you must use v-bind-->
    <div class="review" v-bind:class="some-cool-class" />

<!-- v-if -->
    <!-- will not show up on the page or the DOM if false-->
    <!-- v-else does exist, is not as frequently used -->
    <!-- resource: https://www.digitalocean.com/community/tutorials/vuejs-conditional-directives
    -->
    <p v-if="showDescription" class="description">{{ description }}</p>

<!-- v-show -->
    <!-- will not appear on the page, but will show up on the DOM if false-->
    <p v-show="showDescription" class="description">{{ description }}</p>

<!-- Conditional with v-bind -->
<!-- v-bind:attribute="{'value' : boolean condition}" -->
    <h4 v-bind:class="{'verifiedReviewer' : review.verifiedReview}">{{ review.review }}</h4>

<!-- v-model -->
    <!-- 2-Way data binding, will reactively change data if the user form input changes it-->
    <!-- The property does not have to exist, Vue will create it-->
    <input type="text" id="name" v-model="contact.name" />