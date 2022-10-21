# StopWatch
## This is the proffetional watch wich can be used in reffeering the game because it show properly every details it used in basketball because it can be stopped and start at the same  time 

this is the starting point of this app

![image](https://user-images.githubusercontent.com/103323625/185907800-9197e771-b7d5-49d1-aa49-570c4b576ad7.png)


after clicking the starting button

![image](https://user-images.githubusercontent.com/103323625/185908076-daa3f422-d284-4ae9-a624-9be73593ba08.png)


and the Stop button stop the working of watch till we decide to starting again and the good think here is that after starting again we dont start from zero ,we start from 

where we stopped

![image](https://user-images.githubusercontent.com/103323625/185909162-de800717-079b-4308-b1b0-fa6ab35ed24c.png)
### Link
https://exquisite-axolotl-209544.netlify.app/

### code

```javascript

let seconds = 0
let tens = 0
const displayTens = document.getElementById('tens')
const displaySeconds = document.getElementById('seconds')
const buttonStart = document.getElementById('button-start')
const buttonStop = document.getElementById('button-stop')
const buttonReset = document.getElementById('button-reset')
let interval


buttonStart.onclick = () => {
  clearInterval(interval)
  interval = setInterval(timer, 10)
}

buttonStop.onclick = () => {
  clearInterval(interval)
}

buttonReset.onclick = () => {
  clearInterval(interval)
  tens = 0
  seconds = 0
  displayTens.innerHTML = `0${tens}`
  displaySeconds.innerHTML = `0${seconds}`
}

const timer = () => {
  tens++

  if (Number(tens) <= 9) {
    displayTens.innerHTML = `0${tens}`
  }

  if (Number(tens) > 9) {
    displayTens.innerHTML = tens
  }

  if (Number(tens) > 99) {
    console.log('seconds')
    seconds++
    displaySeconds.innerHTML = `0${seconds}`
    tens = 0
    displayTens.innerHTML = `0${tens}`
  }

  if (Number(seconds) > 9) {
    displaySeconds.innerHTML = seconds
  }
}


```
