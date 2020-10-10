Web Counter 
---

Build

  docker build --no-cache --tag webcounter:0.1 .
  docker run -itd --rm --name was -p 80:80 webcounter:0.1
  docker stop was && docker rmi webcounter:0.1
