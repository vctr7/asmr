# Generate ASMR audio file using WaveGAN

  Since audio file is time series data, it has lots of frames per second(44100/sec) and each frame has a huge scope of amplitude(2^16). Furthermore, sound in real life has a cycle, which needs substantial length of frames, therefore it is required to handle the long range of data. As a result, the existing LSTM or RNN model in machine learning libraries are not proper to train the music data.
  
  To overcome these problems, the large receptive fields have to be applied. I could found some methods that use this technic, Google Deepmind's [Wavenet](https://deepmind.com/blog/article/wavenet-generative-model-raw-audio) and [WaveGAN](https://arxiv.org/pdf/1802.04208.pdf). Wavenet is based on CNN and WaveGAN used transformation of DCGAN.
  
  Of the two options, I chose the latter one. And I could generate asmr files by referencing the [paper](https://arxiv.org/pdf/1802.04208.pdf) and the writer's Github [code](https://github.com/chrisdonahue/wavegan).
  
  If you process the whole procedures in your local environment, it'll take a huge amount of time for each file. To train multiple dataset fastly, I used on-premise MLass [NSML](https://nsml.navercorp.com/). By referencing [NSML Document](https://pages.oss.navercorp.com/nsml/docs.nsml/_build/html/ko_KR/index.html) and [NSML examples](https://oss.navercorp.com/nsml/nsml-examples), you could port your code on NSML then it'll allocate GPU resources to you.
  

## Details

- [PPT](https://github.com/vctr7/asmr/blob/master/ppt/WaveGAN.pdf)

## List

### Non-ASMR

  1. Chopin - Ballades(Krystian Zimerman)
  
     [Dataset](https://www.youtube.com/watch?v=Nhd9ymDZ8L0) 
     
     [Output](https://soundcloud.com/pzlambhjdu8z/mix-by-audio-joiner-com-5)
    

  2. Bach - Goldberg Variations(Glenn Gould)

      [Dataset](https://www.youtube.com/watch?v=Ah392lnFHxM) 
   
      [Output](https://soundcloud.com/pzlambhjdu8z/mix-by-audio-joiner-com-2)
  
  3. Sergei Rachmaninov - Piano Concerto No.1 1st mov
   
      [Dataset](https://www.youtube.com/watch?v=PSJdLkN8Ki4)
      
      [Output](https://soundcloud.com/pzlambhjdu8z/mix-by-audio-joiner-618814755)
 
  4. Lala Land OST(insturments)
  
      [Dataset](https://vibe.naver.com/album/1772995) 
     
      [Output](https://soundcloud.com/pzlambhjdu8z/mix-by-audio-joiner-com-1)
      
  
  5. Philip Glass - Opening
     
      [Dataset](https://www.youtube.com/watch?v=_2vRbNehGB0)
      
      [Output](https://soundcloud.com/pzlambhjdu8z/mix-by-audio-joiner-722086615)
      
      
  6. Antonio Carlos Jobim - Wave
  
      [Dataset](https://www.youtube.com/watch?v=a6KDpB6skA4)
      
      [Output](https://soundcloud.com/pzlambhjdu8z/mix-by-audio-joiner-com-7)
  
  
### ASMR
  
  1. Autumn leaves
  
      [Dataset](https://vibe.naver.com/search/tracks?query=%EB%82%99%EC%97%BD%20asmr)
      
      [Output](https://soundcloud.com/pzlambhjdu8z/mix-by-audio-joiner-com-6)
  
  2. Bird
  
      [Dataset](https://vibe.naver.com/search/tracks?query=%EC%83%88%20%EC%86%8C%EB%A6%AC)
      
      [Output](https://soundcloud.com/pzlambhjdu8z/mix-by-audio-joiner-com-4)
  
  3. La Seine
  
      [Dataset](https://www.youtube.com/watch?v=tQHWKK2spyg)
      
      [Output](https://soundcloud.com/pzlambhjdu8z/mix-by-audio-joiner-192132364)
  
  4. NYC
  
      [Dataset](https://www.youtube.com/watch?v=Mnx7-I-nv5E)
      
      [Output](https://soundcloud.com/pzlambhjdu8z/mix-by-audio-joiner-37923293)
  
  5. Cutting
  
      [Dataset](https://www.youtube.com/watch?v=IHfLqOto_50)
      
      [Output](https://soundcloud.com/pzlambhjdu8z/mix-by-audio-joiner-755274620)
  
  6. Tropical wave
  
      [Dataset](https://www.youtube.com/watch?v=-eXfXTA1P2M)
     
      [Output](https://soundcloud.com/pzlambhjdu8z/mix-by-audio-joiner-com-8)
      
  7. Barber shop
  
      [Dataset](https://www.youtube.com/watch?v=XgRnPbKA7ug)
       
      [Output](https://soundcloud.com/pzlambhjdu8z/mix-by-audio-joiner-833706113)
      
  8. Trafalgar square
  
      [Dataset](https://vibe.naver.com/track/27343933)
      
      [Output](https://soundcloud.com/pzlambhjdu8z/mix-by-audio-joiner-com-9)
  
  9. Fry
  
      [Dataset](https://www.youtube.com/watch?v=DDjqDaqV-Wc)
      
      [Output](https://soundcloud.com/pzlambhjdu8z/mix-by-audio-joiner-333615183)
      
  10. Le Café
  
      [Dataset](https://vibe.naver.com/album/3381589)
      
      [Output](https://soundcloud.com/pzlambhjdu8z/mix-by-audio-joiner-com-3)

  11. Yamanote Line
    
      [Dataset](https://www.youtube.com/watch?v=Rrg9tM6s80o) 
   
      [Output](https://soundcloud.com/pzlambhjdu8z/mix-by-audio-joiner-com)
      
      
  ## Referneces
  
  - [https://github.com/chrisdonahue/wavegan](https://github.com/chrisdonahue/wavegan)
  
  - [https://n-clair.github.io/vision-docs/_build/html/ko_KR/index.html](https://n-clair.github.io/vision-docs/_build/html/ko_KR/index.html)
