<script>
    import dayjs from 'dayjs'

    const number_of_gurudeva_portraits = 3


    let image_number = 1
    $: current_gurudeva_portrait = `/gurudeva${image_number}.jpg`

    setInterval(() => {
        if (image_number == number_of_gurudeva_portraits){
            image_number = 1
        } else {
            image_number+=1;
        }
    }, 5000)

</script>

<!-- <div style="background-image: url({current_gurudeva_portrait})" class="background" >
</div> -->
<img src={current_gurudeva_portrait} alt="gurudeva"/>

<style>
    img {
        /* background-color: blue; */
        background-size: cover;
        height:100vh;
        width: 100vw;
        margin: 0;
    }
</style>
