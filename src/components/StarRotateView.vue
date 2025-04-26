<template>
    <div class="badge" href="#">
        <!-- v2.7 -->
        <span></span>
    </div>

</template>

<style >
.badge {
  position: relative;
}

.badge span {
  width: 25px;
  height: 25px;
  position: absolute;
  top: -12px;
  right: -2px;
  transform: rotate(-20deg);
  filter: blur(0.5px);
  display: flex;
  align-items: center;
  justify-content: center;
}

.badge span:before,
.badge span:after {
  content: "";
  position: absolute;
}

.badge span:before {
  width: 1px;
  height: 100%;
  left: 12px;
  background: linear-gradient(
    to bottom,
    transparent,
    rgba(255, 255, 255, 0.7),
    transparent
  );
}
span:after {
  width: 100%;
  height: 1px;
  top: 12px;
  background: linear-gradient(
    to left,
    transparent,
    rgba(255, 255, 255, 0.7),
    transparent
  );
}
span:after {
  display: block;
  animation: rotate 3s linear infinite; /* Adjust timing as needed */
}
span::before {
  display: block;
  animation: rotate 3s linear infinite; /* Adjust timing as needed */
}

@keyframes rotate {
  0% {
    transform: rotate(0deg) scale(1);
  }
  50% {
    transform: rotate(180deg) scale(1.8);
  }
  100% {
    transform: rotate(360deg) scale(1);
  }
}


</style>