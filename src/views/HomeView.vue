<template>
  <div class="container">
    <!-- Espaço para a foto -->
    <img src="@/assets/profile2.jpg" alt="Profile Photo" class="profile-photo"/>

    <!-- Informação principal (nome, título, website) -->
    <Info title="Jules Winnfield" text="Hitman"/>
    <p class="website">juleswinnfield.website</p>

    <!-- Botões de contato -->
    <div class="buttons">
      <button class="email-button">
        <i class="fas fa-envelope"></i> Email
      </button>
      <a href="https://www.linkedin.com/in/henrique-pimenta-souza-643b25202/" target="_blank" class="linkedin-link">
        <button class="linkedin-button">
          <i class="fab fa-linkedin"></i> LinkedIn
        </button>
      </a>
    </div>

    <Contact />

    <Socials />
  </div>
</template>

<script>
import Info from '@/components/info.vue';
import Contact from '@/components/contact.vue';
import Socials from '@/components/socials.vue';

export default {
  name: 'Home',
  components: {
    Info,
    Contact,
    Socials
  }
}
</script>

<style scoped>
.container {
  background-color: var(--neutral-neutral-600); /* Usando a cor do cartão */
  max-width: 400px;
  margin: 0 auto;
  padding: 0px;
  border-radius: 8px;
  text-align: center;
  color: var(--neutral-text);
}


.profile-photo {
  width: 100%;
  margin-bottom: 20px;
  border-top-left-radius: 8px;
  border-top-right-radius: 8px;
}

.website {
  font-size: 12px;
  margin-top: -10px;
  margin-bottom: 20px;
  color: var(--neutral-text);
}

.buttons {
  display: flex;
  justify-content: center;
  gap: 19px;
  margin-bottom: 20px;
}

.email-button, .linkedin-button {
  padding: 12px 24px; 
  width: 140px; 
  height: 36px;
  border: none;
  border-radius: 6px;
  color: var(--neutral-text); 
  cursor: pointer;
  font-size: 14px;
  transition: background-color 0.3s ease, transform 0.2s ease; 
  display: flex; 
  align-items: center;
  justify-content: center;
}

.email-button {
  background-color: var(--button-email-bg); 
  color: var(--button-text-dark); 
}

.linkedin-button {
  background-color: var(--button-linkedin-bg); 
}

.email-button i, .linkedin-button i {
  margin-right: 8px; 
}

.linkedin-link {
  text-decoration: none; 
}
</style>
