<script>
// @ts-nocheck

    import logo from '../lib/images/logo-paper.svg'
    export let dark
    export let darkMode
</script>
<nav class="flex p-5 gap-12 justify-between text-sm dark:bg-slate-900 {darkMode}">
    <div class="flex gap-10 my-2">
        <img src={logo} alt="paper-logo">
        <div class="flex gap-12 ">
            <div class="flex flex-col gap-1 items-center group">
                <i class="fa-solid fa-chart-simple"></i>
                <h1 class="group-hover:underline decoration-green-400 underline-offset-8">Dashboard</h1>
            </div>
            <div class="group flex flex-col gap-1 items-center">
                <i class="fa-solid fa-chalkboard-user"></i>
                <h1 class="group-hover:underline decoration-green-400 underline-offset-8">Chat</h1>
            </div>
            <div class="group flex flex-col gap-1 items-center">
                <i class="fa-sharp fa-solid fa-paper-plane"></i>
                <h1 class="group-hover:underline decoration-green-400 underline-offset-8">Review Center</h1>
            </div>
        </div>
    </div>
    <div class="flex gap-12 my-1 mx-5">
        <div>
            <input bind:checked = {dark}  type="checkbox" class="checkbox" id="checkbox">
          <label for="checkbox" class="label">
            <i class="fas fa-moon"></i>
            <i class='fas fa-sun'></i>
            <div class='ball'>
          </label>
        </div>
        <div class="py-2 px-3 bg-blue-500 rounded-md text">
            <i class="fa-regular fa-calendar text-xl"></i>
        </div>
        
        <h1 class="my-1 font-bold">Tutor Name Menu</h1>
    </div>
</nav>

<style>
.checkbox {
  opacity: 0;
  position: absolute;
}

.label {
  width: 50px;
  height: 26px;
  background-color:blue;
  display: flex;
  border-radius:50px;
  align-items: center;
  justify-content: space-between;
  padding: 5px;
  position: relative;
  transform: scale(1.5);
}

.ball {
  width: 20px;
  height: 20px;
  background-color: white;
  position: absolute;
  top: 2px;
  left: 2px;
  border-radius: 50%;
  transition: transform 0.2s linear;
}

/*  target the elemenent after the label*/
.checkbox:checked + .label .ball{
  transform: translateX(24px);
}

.fa-moon {
  color: pink;
}

.fa-sun {
  color: yellow;
}
</style>