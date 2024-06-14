* {
  margin: 0;
  padding: 0;
  border: 0;
  box-sizing: border-box;
  color: #ffffff;
  text-decoration: none;
  list-style: none;
}
body {
  width: 100%;
  height: 100vh;
  background: #141414;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
:root {
  --clr: #ff006a;
  --clr1: #006eff;
}
.text {
  display: flex;
  position: relative;
  font-size: 30px;
  font-weight: bold;
  font-style: italic;
  color: var(--clr);
  
}
.text::after {
  content: '';
  width: 100%;
  height: 50px;
  background: #ff00ea;
  position: absolute;
  top: 100%;
  transform: perspective(1em) rotateX(40deg) scale(1.0, 0.5);
  filter: blur(1em);
}
.image {
  display: flex;
}
.image img {
  width: 100px;
  height: 100px;
}
#loading {
  width: 400px;
  height: 400px;
  display: flex;
  position: relative;
  justify-content: center;
  align-items: center;
  animation: scale 5s linear infinite;
}
#loading span {
  width: 100%;
  height: 100%;
  position: absolute;
  border-left: 3px solid rgb(47, 0, 255);
  border-right: 3px solid rgb(255, 0, 21);
  border-radius: 37% 61% 63% 35% / 42% 34% 64% 56%;
  animation: rotate 3s linear infinite;
}
#loading span:nth-child(1) {
  animation: rotate 6s linear infinite reverse;
}
#loading span:nth-child(2) {
  animation: rotate 9s linear infinite;
}
#loading span:nth-child(3) {
  animation: rotate 12s linear infinite reverse;
}
@keyframes rotate {
  0% {
    transform: rotate(0);
  }
  100% {
    transform: rotate(360deg);
  }
}
@keyframes scale {
  0% {
    width: 400px;
    height: 400px;
  }
  50% {
    width: 600px;
    height: 600px;
  }
  100% {
    width: 400px;
    height: 400px;
  }
}
