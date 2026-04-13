<!--
@component
### Hero component 
Renders a visual replica of the Immersive Template hero. 

#### Optional properties
- sectionLabel: string;
- headline: string;
- timestamp: string;
- heroImageUrl: string;
- heroImageCaption: string;
- heroImageAltText: string;
- dek: string;
- authorName: string;
- authorBioUrl: string;

#### Example
```svelte
<Hero
  sectionLabel = "Section label",
  headline = "Lorem ipsum dolor sit amet consectetur adipiscing elit",
  timestamp = "Dec. 1, 1977",
  heroImageUrl = "https://arc.stimg.co/startribunemedia/4SPNT7DI36ANT2SOB5N5EJAIJU.jpg",
  heroImageCaption = "",
  heroImageAltText = "",
  dek = "Lorem ipsum dolor sit amet consectetur adipiscing elit, fusce sociis at montes vitae tempor enim, venenatis tristique feugiat arcu dis ridiculus.",
  authorName = "Bryan Brussee",
  authorBioUrl = "https://www.startribune.com/bryan-brussee/8455834",
>
```
-->

<script>
  import Grid from "../Grid/Grid.svelte";
  import GridRow from "../Grid/_GridRow.svelte";
  import SectionLabel from "./_SectionLabel.svelte";
  import Headline from "./_Headline.svelte";
  import Timestamp from "./_Timestamp.svelte";
  import Image from "../Image/Image.svelte";
  import Dek from "./_Dek.svelte";
  import Byline from "./_Byline.svelte";

  /** @type {{sectionLabel?: string; headline?: string; timestamp?: string; heroImageUrl?: string; heroImageCaption?: string; heroImageAltText?: string; dek?: string; authorName?: string; authorBioUrl?: string;}} */
  let {
    sectionLabel = "",
    headline = "",
    timestamp = "",
    heroImageUrl = "",
    heroImageCaption = "",
    heroImageAltText = "",
    dek = "",
    authorName = "",
    authorBioUrl = "",
  } = $props();
</script>





<Grid additionalClasses="gap-y-8 md:gap-y-10">


    <GridRow variant={"fullBleed"}>
      <div class="relative flex items-center justify-center h-screen mb-4 overflow-hidden bg-[white] xl:max-h-[1000px] lg:max-h-[900px] md:max-h-[800px] xs:max-h-[650px]">
        <div class="absolute left-8 bottom-4 md:min-w-[800px] xs:min-w-[95%] xs:left-2 xs:top-2 z-30 xl:p-6 lg:p-4 md:p-4 xs:p-2 text-2xl !text-[white] text-left font-editorial-news-heading-01 max-w-[700px] mt-auto drop-shadow-md">

            <div class="xs:hidden md:block absolute bottom-0 xl:text-[3.5rem] lg:text-[3.5rem] md:text-[2.75rem] xs:text-[2rem] bg-[#0c2340] p-4"><h1>Timberwolves guard Mike Conley<br>is a man of 1,000 handshakes.</h1><h1 class="pt-6">Well, close.</h1></div>


            <div class="xs:block md:hidden absolute bottom-0 xs:text-[2rem] bg-[#0c2340] p-4"><h1>Timberwolves guard<br>Mike Conley is a man<br>of 1,000 handshakes.</h1><h1 class="pt-6">Well, close.</h1></div>


        </div>
        <video autoplay="" loop="" muted="true" class="object-cover absolute h-full w-full">
            <source src="https://static.startribune.com/news/projects/all/2026-WOLVES-HANDSHAKE/video%20assets/HANDSHAKES_HERO_16X9%20%281%29.mp4" type="video/mp4">Your browser does not support the video tag.
        </video>
    </div>
    </GridRow>

</Grid>
