<template>
  <v-app>

    <v-container>
      <v-row>
        <words-component 
        :leveling="'start'" 
        :wordsArr="tagText"
        :size="'18'"/>
      </v-row>
      <v-row>
        <words-component 
        :leveling="'justify'" 
        :wordsArr="tagText"
        :size="'18'"/>
      </v-row>
      <v-row cols="12" class="px-0">
        <v-col>
          <words-component 
          :leveling="'start'" 
          :wordsArr="tagText"
          :size="'16'"/>
        </v-col>
        <v-col>
          <words-component 
          :leveling="'justify'" 
          :wordsArr="tagText"
          :size="'16'"/>
        </v-col>
        <v-col cols="2">
          <words-component 
          :leveling="'justify'" 
          :wordsArr="tagText"
          :size="'12'"/>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
import WordsComponent from './components/WordsComponent';

export default {
  name: 'App',

  components: {
    WordsComponent,
  },

  data: () => ({
    tagText: [
      {
        text: 'Таким образом дальнейшее развитие различных форм деятельности представляет собой интересный эксперимент проверки новых предложений. Идейные соображения высшего порядка, а также постоянный количественный рост и сфера нашей активности обеспечивает широкому кругу (специалистов) участие в формировании новых предложений. Разнообразный и богатый опыт укрепление и развитие структуры требуют от нас анализа новых предложений. Значимость этих проблем настолько очевидна, что консультация с широким активом обеспечивает широкому кругу (специалистов) участие в формировании систем массового участия.',
      },
      {
        text: 'Не следует, однако забывать, что дальнейшее развитие различных форм деятельности требуют определения и уточнения позиций, занимаемых участниками в отношении поставленных задач.',
        icon: 'mdiCircleSmall',
      },
    ]
  }),
};
</script>
