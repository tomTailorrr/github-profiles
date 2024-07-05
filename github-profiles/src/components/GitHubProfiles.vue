<template>
  <div class="profiles">
    <h2>GitHub профили</h2>
    <div class="profile-cards">
      <div class="profile-card" v-for="profile in profiles" :key="profile.name">
        <img :src="profile.image" alt="profile picture" />
        <div class="profile-info">
          <h3>{{ profile.name }}</h3>
          <p>{{ profile.joinDate }}</p>
          <p>{{ profile.description }}</p>
          <p>{{ profile.friends }} Друзья</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      profiles: [
        {
          name: 'Daniel Kelly',
          joinDate: 'Зарегистрирован: 2014-05-19T20:55:29Z',
          description: '',
          friends: '398',
          image: 'https://wpapers.ru/wallpapers/avto/Dodge/426/download/1600x1200_Dodge-Challenger.jpg' 
        },
        {
          name: 'Alex Kyriakidis',
          joinDate: 'Зарегистрирован: 2013-12-10T02:45:44Z',
          description: 'Developer - Teacher - Author - Consultant',
          friends: '1299',
          image: 'https://img.goodfon.com/original/1600x1200/0/ff/panorama-gorod-mosty-most.jpg'
        },
        {
          name: 'Rolf Haug',
          joinDate: 'Зарегистрирован: 2010-06-16T16:36:05Z',
          description: 'Educator and web developer. Co-founder of Vue School',
          friends: '163',
          image: 'https://priroda-foto.ucoz.ru/_ph/5/988290684.jpg'
        },
        {
          name: 'Guillaume Chau',
          joinDate: 'Зарегистрирован: 2012-11-14T11:18:54Z',
          description: 'Web & JavaScript enthusiast. @vuejs core team.',
          friends: '4998',
          image: 'https://www.1zoom.ru/big/66/44719-740.jpg'
        }
      ]
    };
  }
};
</script>

<style scoped>
.profiles {
  padding: 20px;
}

.profile-cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}

.profile-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  border: 1px solid #ccc;
  border-radius: 10px;
  padding: 10px;
  margin: 10px;
  max-width: 200px;
}

.profile-card img {
  border-radius: 50%;
  width: 100px;
  height: 100px;
}

.profile-info {
  text-align: center;
}
</style>
