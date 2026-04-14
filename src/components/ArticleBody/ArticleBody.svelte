<!-- 
@component
### ArticleBody component
This is a general workspace illustrating what an article body might look like if you use only the components included in this template.  
ArticleBody doesn't accept any props. All contents will need to be hand-placed by a designer directly inside this component.  
In this example, Grid and GridRow help establish the width of the article body's contents. 
Documentation included with those components and accessed by VSCode tooltip explains each component in greater detail.

#### State in this component
- innerWidth: int - pixel width of the viewport.
- isMobile: boolean - derived from innerWidth, true if less than 768 pixels
- isTablet: boolean - derived from innerWidth, true if between 768 pixels inclusive and 1160 pixels exclusive
- isDesktop: boolean - derived from innerWidth, true if greater than 1160 pixels inclusive

#### Using state in this component
You can use any of the three derived states to render different variants of a GridRow component reactively.
The following example uses a ternary to render an image edge-to-edge on mobile but inline otherwise.

#### Example
```svelte
  <GridRow
    variant={isMobile ? "fullBleed" : "inline"}
  >
    <Image
      src="https://arc.stimg.co/startribunemedia/4SPNT7DI36ANT2SOB5N5EJAIJU.jpg"
      alt="Descriptive alt text"
      caption="Caption tk tk tk"
    />
  </GridRow>
```
-->

<script>
  import Grid from "../Grid/Grid.svelte";
  import GridRow from "../Grid/_GridRow.svelte";
  import Subhead from "./_Subhead.svelte";
  import Paragraph from "./_Paragraph.svelte";
  import Dropcap from "./_Dropcap.svelte";
  import Image from "../Image/Image.svelte";
  import Gallery from "../Image/Gallery.svelte";
  import ScrollySection from "../Scrolly/ScrollySection.svelte";
  import JWPlayer from "../Video/JWPlayer.svelte";


  let innerWidth = $state(0);
  let isMobile = $derived(innerWidth < 768);
  let isTablet = $derived(innerWidth >= 768 && innerWidth < 1160);
  let isDesktop = $derived(innerWidth >= 1160);
</script>

<svelte:window bind:innerWidth />
<Grid additionalClasses={"gap-y-5 pb-4"}>
  <GridRow variant={"inline"} additionalClasses={"gap-y-5"}>

<Paragraph>  <h2 class="w-full  font-editorial-non-news-heading-03 font-regular leading-[1.1] text-left mx-auto mt-0 xs:mt-10 pb-2 text-primary xl:text-[1.75rem] lg:text-[1.5rem] md:text-2xl xs:text-[24px]">NBA veteran Mike Conley has a personal greeting for teammates, friends and staffers that requires a lot of muscle memory.</h2></Paragraph>

<Paragraph>
    <div class="byline rt-Box col-span-full flex items-center gap-x-2 flex-wrap mx-auto font-utility-label-reg-02 pb-4">
      <div class="rt-Box col-span-full flex items-center gap-x-2 flex-wrap">
        <div class="rt-Box w-full mb-3 flex items-center gap-x-2">
          <div class="rt-Box flex flex-col gap-y-0.5">
            <div class="rt-Box flex items-center">
                <p class="rt-Text font-utility-label-bold-02 text-text-primary relative mr-2">By <a class="!no-underline" href="https://www.startribune.com/author/chris-hine/6370609" target="_blank">Chris Hine</a> <br>Photos and video by <a class="!no-underline" href="https://www.startribune.com/author/carlos-gonzalez/6370603" target="_blank">Carlos Gonzalez</a></p>
                
            </div>
            <span class="rt-Text text-text-secondary font-utility-label-reg-02">The Minnesota Star Tribune</span>
          </div>
        </div>
        <div class="rt-Flex flex rt-r-display-flex rt-r-jc-start">
          <span class="rt-Text font-utility-label-reg-caps-03 text-text-secondary !text-[.6875rem] pb-8">April 15, 2026</span>
        </div>
      </div>
    </div>
  </Paragraph>


  <Paragraph>
    A smiling Mike Conley walked back to the Timberwolves bench after hitting a clinching three-pointer.
    </Paragraph>
    
    <Paragraph>
    Teammates were lined up to greet him in the late November victory over San Antonio.
    </Paragraph>
    
    <Paragraph>
    One by one, they congratulated Conley with the unique handshakes: A couple back-and-forth handslaps with Donte DiVincenzo; a slap, then interlocking fingers with Anthony Edwards; some hand pats, then interlocking arms with Rudy Gobert.
    </Paragraph>
    
    <Paragraph>
    On down the line Conley went, never breaking stride or hesitating on the moves required to execute over a dozen different handshakes before he got to sit down on the bench.
    </Paragraph>
    
    <Paragraph>
    How does he remember them all?
    </Paragraph>
    
    <Paragraph>
    “It’s on cruise control. It really is,” Conley said. “Maybe all the guys don’t have handshakes with other people, but they all have one with me. So when they see me, they can almost lead the dance.”
    </Paragraph>
    
    <Paragraph>
    Across his 19 seasons in the league, Conley has committed dozens of these “dances” to memory. He is renowned for being one of the best teammates in the NBA. He won the Joe Dumars Sportsmanship Award four times and the Twyman-Stokes Teammate of the Year twice.
    </Paragraph>
    
    <Paragraph>
    One of the ways Conley built that reputation is through his handshakes, which are his way of forming a unique connection with teammates, coaches and staffers who pass through what can be a transient business.
    </Paragraph>
    
</GridRow>


<GridRow additionalClasses={"pt-8 pb-4"}>
    <picture style="display: contents;"><source media="(max-width: 767px)" srcset="https://arc.stimg.co/startribunemedia/XIPXOHVWYBDMNLTG5D3VBAQ3A4.jpg?&amp;w=390" style="display: contents;"><source media="(min-width: 768px) and (max-width: 1159px)" srcset="https://arc.stimg.co/startribunemedia/XIPXOHVWYBDMNLTG5D3VBAQ3A4.jpg?&amp;w=720" style="display: contents;"><img data-testid="InLineImage" alt="" data-chromatic="ignore" loading="lazy" width="0" height="0" decoding="async" data-nimg="1" class="object-cover h-auto w-full" src="https://arc.stimg.co/startribunemedia/XIPXOHVWYBDMNLTG5D3VBAQ3A4.jpg?&amp;w=1080" style=""></picture><div class="text-[14px] w-full max-w-[575px] mx-auto text-center leading-[125%] pt-2 pb-4">Timberwolves guard Mike Conley, left, shares custom handshakes with teammates including Anthony Edwards. It's something he's done throughout his 19 seasons in the NBA and helped him become one of the most well-regarded locker room assets in the league. “I’ve always felt that it’s a way to personally connect to people that’s beyond the game,” Conley said.</div>
    </GridRow>
    
    
    <GridRow variant={"inline"} additionalClasses={"gap-y-5"}>
    <Paragraph>
    In all, Conley estimates he has over 100 handshakes stored in his brain, all ready to come out upon seeing someone.
    </Paragraph>
    
    <Paragraph>
    Teammate Jaden McDaniels didn’t quite believe it when told Conley has that many.
    </Paragraph>
    
    <Paragraph>
    “Sometimes people just be talking to talk,” McDaniels said in a deadpan delivery. But then he thought for a moment. “He might though.”
    </Paragraph>
    
    <Paragraph>
    Even if years have passed and Conley hasn’t seen the person in a while, the handshake comes out just as naturally as saying hello.
    </Paragraph>
    
    <Paragraph>
    “It reminds me of just like a great song that you love when you were a kid,” Conley said. “Maybe you don’t hear for five, six years, and it pops up like, ‘Man, I really enjoy that. And you start singing along. How do I remember that song? It’s kind of like the same way. …
    </Paragraph>
    
    <Paragraph>
    “By the time you’ve done it thousands of times you’re talking about you don’t see each other for a year, it’s just like clockwork, picking up from where you left off.”
    </Paragraph>
    </GridRow>


    <GridRow additionalClasses={"pt-8 pb-4"}>
    <link rel="stylesheet" href="https://static.startribune.com/news/tools/embeds/video-player/css/video-iframe_070125.css">
  <div class="video-embed default">
	<div class="video-inner">
		<iframe src="https://static.startribune.com/news/tools/embeds/video-player/player-no-ads.html?url=https://d2rhwptr68oefh.cloudfront.net/wp-startribunemedia/Carlos_Gonazalez/20260406/69d44223ef096c66f498cf3b/t_05c973f411ef4562bb0160aa8cf5c482_name_HANDSHAKES_Bones_16X9/file_1920x1080-5400-v4.mp4&amp;shape=default&amp;thumbnail=https://arc-goldfish-startribunemedia-thumbnails.s3.amazonaws.com/04-06-2026/t_807abc84fd07436fbab54fe6770a4c2d_name_file_1920x1080_5400_v4_.jpg" scrolling="no" marginheight="0" frameborder="0" allowfullscreen="false" loop="" autoplay="" mute="true"></iframe>

	</div>

</div>
<div class="text-[14px] w-full max-w-[575px] mx-auto text-center leading-[125%] pt-2 pb-4">Timberwolves players Mike Conley and Bones Hyland get hyped up pregame with their custom handshake — one of the dozens Conley has committed to memory throughout his long NBA career.</div>
</GridRow>



<GridRow variant={"inline"} additionalClasses={"gap-y-5"}>
    
    <Paragraph>
    There’s no specific method for coming up with a handshake. Sometimes they are just born out of spontaneity.
    </Paragraph>
    
    <Paragraph>
    Guard Bones Hyland said Conley told him to come up with something this season, and Hyland said their handshake took “literally two minutes” to create.
    </Paragraph>
    
    <Paragraph>
    “I went with the flow, I said, bet, I got you. … and we just got it. I swear to God, he don’t forget it. It’s crazy,” Hyland said.
    </Paragraph>
    
    <Paragraph>
    While every handshake is like a snowflake, unique in its design and patterns, Conley prefers if a handshake has a “solid” similar foundation.
    </Paragraph>
    
    <Paragraph>
    “So like the first three contacts have to be consistent … to start it off,” Conley said. “You can’t have too many different things going on at the beginning of it, but if you can start it all kind of similar, then you can pick up on who you’re having the handshake with.”
    </Paragraph>
    
    <Paragraph>
    Those motions are like quick claps or pats, and then those can segue into something a little more complicated.
    </Paragraph>
    
    <Paragraph>
    The most intricate handshake he has is with someone who Conley is on his third stint with as a teammate, Kyle Anderson. Anderson, 32, and Conley, 38, were together in Memphis and now twice with the Wolves.
    </Paragraph>
    
    <Paragraph>
    The irony is even though Anderson and Conley have been teammates off and on since 2018, they only just now came up with their own handshake.
    </Paragraph>
    
    <Paragraph>
    “I was like, ‘Man, I don’t know how that happened, but we got to change that.’” Conley said.
    </Paragraph>
    
    <Paragraph>
    At first, Anderson said he didn’t like what Conley came up with for them. Then he went scrolling through social media and got some inspiration.
    </Paragraph>
    
    <Paragraph>
    “I was just watching a TikTok of some dance and I just threw a little piece of the TikTok in there,” Anderson said. “It’s two old guys using TikTok.”
    </Paragraph>
    
    <Paragraph>
    When you watch Conley interact with his teammates, it’s rare they don’t smile when he walks up to them. He’s quick with a joke or a helpful word. When he was away from the team for a while after getting traded twice, teammates and coach Chris Finch joked they didn’t know who was going to break down their huddles with “one, two, three, Wolves” because that was always Conley.
    </Paragraph>
    
    <Paragraph>
    He, along with Hyland, also handle the pregame dances that get everybody loose just before tipoff. Before he breaks it down, though, Conley goes through most of his teammates and greets them with a handshake at the end of the lineup line.
    </Paragraph>
    
    <Paragraph>
    “You see him, it’s something you do and it might change your mood that day, depending what your handshake is,” McDaniels said.
    </Paragraph>
    
    <Paragraph>
    Added Anderson: “When you’re in the heat of battle, and you see how cool and collected he is, he’s ready to help guys calm down so they can deliver. He’s awesome.”
    </Paragraph>
    
  </GridRow>


  <GridRow  additionalClasses={"pt-8 pb-4"}>
    <picture style="display: contents;"><source media="(max-width: 767px)" srcset="https://arc.stimg.co/startribunemedia/ES2SB7H2BREZVILFTJJ2LCNE74.jpg?&amp;w=390" style="display: contents;"><source media="(min-width: 768px) and (max-width: 1159px)" srcset="https://arc.stimg.co/startribunemedia/ES2SB7H2BREZVILFTJJ2LCNE74.jpg?&amp;w=720" style="display: contents;"><img data-testid="InLineImage" alt="" data-chromatic="ignore" loading="lazy" width="0" height="0" decoding="async" data-nimg="1" class="object-cover h-auto w-full" src="https://arc.stimg.co/startribunemedia/ES2SB7H2BREZVILFTJJ2LCNE74.jpg?&amp;w=1080" style="color: transparent;"></picture><div class="text-[14px] w-full max-w-[575px] mx-auto text-center leading-[125%] pt-2 pb-4">Every handshake Mike Conley, left, shares with a teammate, like Rudy Gobert, is unique and memorized but starts in a similar way with claps or pats. “You can’t have too many different things going on at the beginning of it, but if you can start it all kind of similar, then you can pick up on who you’re having the handshake with," Conley said.</div>
    </GridRow>
    
    
    <GridRow variant={"inline"} additionalClasses={"gap-y-5"}>
    
      <Subhead>A way to connect</Subhead>

    <Paragraph>
    For Conley, the handshake is a special way to connect with not just teammates, but staff members and family. Well, except for one family member: his wife, Mary.
    </Paragraph>
    
    <Paragraph>
    “No handshake with Mary,” Conley said. “That’s a regular hug and a kiss.”
    </Paragraph>
    
    <Paragraph>
    Conley said he really started making handshakes a regular feature of his daily life in high school, and they just expanded from there, his way of finding a distinctive way to bond with people who come in and out of his orbit during his career.
    </Paragraph>
    
    <Paragraph>
    “I’ve always felt that it’s a way to personally connect to people that’s beyond the game,” Conley said. “It’s just a way that when I see you, you see me. The fact that we can remember this handshake every time after seeing each other, maybe not for like, a week or a month or a year, and the first thing you do is the handshake, it just symbolizes something deeper than just passing through, working alongside you.”
    </Paragraph>
    
    <Paragraph>
    Case and point: in that San Antonio game, a number of the teammates Conley exchanged handshakes with on his way to the bench, like Rob Dillingham, Leonard Miller and Johnny Juzang, are no longer on the team. He and Juzang formalized their handshake just weeks before Conley was traded twice (before ending up back with the Wolves) and the team waived Juzang after the All-Star break.
    </Paragraph>
    
    <Paragraph>
    “Something happened in a game where I came out and I did like a beat on my chest, he hit his chest and, then like slapped his hand,” Conley said. “I was like, that might be it. Just random how it happens, but I think that’s the beauty of it, it’s just so organic.”
    </Paragraph>
    
    <Paragraph>
    They’ll always have their handshake, and Conley isn’t going to forget it.
    </Paragraph>
    
    <Paragraph>
    “I look at the person, and as soon as I see who it is it just clicks, your body takes over and you’re back to it,” Conley said.
    </Paragraph>
    
    <Paragraph>
    “I got handshakes from guys with old teams, see them once or twice a year and I see them and I’m like I don’t know how I remember this, but it’s just how it goes.”
    </Paragraph>
    </GridRow>
</Grid>

<style>
  a {
    text-decoration-line: underline;
    text-decoration-color: #00854b;
    text-underline-offset: 2px;
  }

  a:hover {
    color: #00854b;
  }
</style>
