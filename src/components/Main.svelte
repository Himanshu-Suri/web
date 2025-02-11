<script>
     import Step from "./Step.svelte";
        let steps = [
            {name: 'fps', icon: 'fa-solid fa-gun'},
            {name: 'ham' , icon: 'fa-solid fa-walkie-talkie' },
            {name: 'web dev' , icon: 'fa-solid fa-wifi' }
        ]
        
        let benefits = [
        {
            metric: "10x",
            name: "a self taught developer",
            description:
                "I taught myself to code using online resources. Starting of with JavaScript, HTML & CSS and evolving my knowledge base to include JavaScript frameworks with base level profeciency in c , c++ and python.",
        },
        {
            name: "I love to innovate",
            description:
                "I love to think of challenging ways to tackle a problem.",
        },
        {
            name: "an excellent communicator",
            description:
                "Communication is key. I believe in transparency and constructive communication above all else. This helps me develop deep relationships and ensures my effectiveness and productivity in any work space with any team.",
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4">
 <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm-py-14">
    <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8">
        <h2 class ="font-semibold text-4xl sm:text-5xl md:text-6xl">
            Hi! I am <span text-coilet-400>Himanshu Suri</span> an aspiring dev!
        </h2>
        <p class="text-base sm:text-lg md:text-xl">
            I am currently learning web dev using tailwind and svelte!
        </p>
        <a class="blueshadow mx-auto lg:mr-auto text-base sm:text-base sm:text-lg md:text-xl relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950" href="#">Get in touch</a>
        <div class="relative shadow-2xl grid place-items-center ">
            <img src="/assets/images/img.png" alt="profile image" class="object-cover z-[2] max-h-[70vh] rounded-full center">

        </div>
 </section>
 <section id ="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h3 class="text-xl Roboto">
                A few of my intrests 
            </h3>
            <div class="grid grid-cols-1 mt-10 lg:grid-cols-3 gap-12 lg:gap-10">
                <Step step={steps[0]}>
                <p>
                   I love playing fps such as <strong
                        class="text-violet-400"
                        >TF2</strong>                 
            </p>
            </Step>
                <Step step={steps[1]} >  <p>
                    I have experience in <strong
                         class="text-violet-400"
                         > wireless communication</strong>                 
             </p></Step>
                <Step step={steps[2]}> 
                    <p>
                        I am enjoying learning <strong
                             class="text-violet-400"
                             >web dev</strong>                 
                 </p>
                </Step>
                
            </div>
        </div>

 </section>

    <section
    id="about"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
    <div
        class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
        <h6 class="text-large sm:text-xl md:text-2xl">
            Want to know more?
        </h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            A bit <span class="poppins text-violet-400">about</span> me.
        </h3>
    </div>
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
        I am . . .
    </p>
    <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
        {#each benefits as benefit, index}
           
            <div class="flex gap-6 sm:gap-8">
                <p
                    class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                >
                    0{index + 1}
                </p>
                <div class="flex flex-col gap-6 sm:gap-8">
                    <h3 class="text-2xl sm:text-3xl md:text-5xl">
                        {benefit.name}
                    </h3>
                    <p>{benefit.description}</p>
                </div>
            </div>
        {/each}
    </div>
</section>
 
</main>