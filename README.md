# Generate ASMR audio file using WaveGAN
  오디오는 시계열이지만 초당 프레임이 많고 진폭도 커서 기존의 LSTM을 이용하면 원하는 결과가 나오지 않음. 이를 보완한 것이 대표적으로 Google의 Wavenet임.
  그 외에도 DCGAN을 변형한 WaveGAN을 이용하여 오디오 음원을 합성, 생성할 수 있음. [WaveGAN 논문](https://arxiv.org/pdf/1802.04208.pdf) [WaveGAN Github](https://github.com/chrisdonahue/wavegan)를 참조했다.
  
  학습을 로컬에서 진행할 시 시간이 상당히 소요될 뿐더러 한번에 여러 데이터셋을 훈련시킬 수 없다. 다양한 데이터셋을 빠른 속도로 훈련시키기 위해 사내 MLaas인 [NSML](https://nsml.navercorp.com/)을 이용한다. [NSML Document](https://pages.oss.navercorp.com/nsml/docs.nsml/_build/html/ko_KR/index.html)와 [NSML 예제](https://oss.navercorp.com/nsml/nsml-examples)들을 참고하여 포팅하면 세션별로 GPU를 할당받을 수 있다. 이렇게 되면 로컬이 아닌 환경에서 빠른 속도로 모델 학습이 가능하다.


## List

### Non-ASMR

  1. Chopin Ballades(Krystian Zimerman)
  
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
     
      [Output]()
      
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
