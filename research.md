---
layout: page
permalink: /research/
elements:
  - content
  - css
  - formatting
  - html
  - markup  

---

<style>
  summary {
    font-weight: bold;
    cursor: pointer;
    padding: 10px;
    background-color: #2a5866; /* Navy background */
    color: white; /* White text */
    border: 1px solid #001f3f;
    border-radius: 5px;
    width: fit-content;
  }

  summary:hover {
    background-color: #001a35; /* Slightly darker navy on hover */
  }

  details {
    margin-bottom: 15px;
  }

  details[open] summary {
    background-color: #001a35; /* Change background when open */
  }

  .text-justify {
    text-align: justify;
    padding: 10px;
    background-color: #f9f9f9;
    border-left: 4px solid #ccc;
    margin-top: 10px;
    border-radius: 3px;
  }

  /* Ensures buttons (details) are aligned side by side */
  .button-container {
    display: flex;
    gap: 10px; /* Adds spacing between buttons */
    flex-wrap: wrap; /* Allows buttons to wrap if the screen is small */
  }

  /* Optional: Adjust for smaller screens */
  @media (max-width: 600px) {
    .button-container {
      flex-direction: column;
    }
  }

/* Add vertical spacing before h1 */
h1 {
    margin-top: 40px; /* Adds vertical spacing before h1 */
}
	/* Add margin to a specific div or section containing the header */
section {
    margin-top: 40px; /* Adds space before sections */
}

/* Center the specific page title with a class */
.page-title {
    text-align: center; /* Centers the title */
    font-style: normal; /* Removes the italic style */
}

 .jmp-container {
    display: flex;
    align-items: flex-start;
    gap: 20px;
  }

  .jmp-content {
    flex: 2; /* Content takes up more space */
  }

  .jmp-carousel {
    flex: 1; /* Carousel takes up less space */
  }

.carousel {
  position: relative;
  max-width: 600px; /* Define the maximum width of the carousel */
  margin: 0 auto; /* Center the carousel */
  overflow: hidden;
  border: 1px solid #ddd;
  border-radius: 8px;
  background: #f9f9f9; /* Optional: Add a background for visibility */
}

.carousel-images {
  display: flex;
  transition: transform 0.5s ease-in-out;
}

.carousel img {
  width: 100%; /* Ensures images scale with the carousel width */
  flex-shrink: 0;
}

.carousel-buttons {
  position: absolute;
  top: 50%; /* Vertically center the buttons */
  width: 100%; /* The buttons span the entire carousel width */
  display: flex;
  justify-content: space-between; /* Position buttons to the left and right */
  transform: translateY(-50%); /* Align with the middle of the carousel */
  pointer-events: none; /* Prevent the buttons from blocking image clicks */
}

.carousel-button {
  background: rgba(0, 0, 0, 0.6); /* Semi-transparent background for buttons */
  color: white;
  border: none;
  padding: 15px;
  cursor: pointer;
  pointer-events: auto; /* Allow buttons to be clickable */
  border-radius: 50%;
  z-index: 2; /* Ensure buttons are above images */
}

.carousel-button.prev {
  margin-left: 10px; /* Slight space from the left edge */
}

.carousel-button.next {
  margin-right: 10px; /* Slight space from the right edge */
}

.carousel-button:hover {
  background: rgba(0, 0, 0, 0.8); /* Darker background on hover */
}



</style>


	
# Publication

---------------------------------------------------------------------------------------------------------------------------------------------------------------

<div class="jmp-container">
  
<!-- Left-hand side: Markdown content -->
<div class="jmp-content">

    <h3><em><a href="https://www.sciencedirect.com/science/article/pii/S0927537124000022">Male and female selection effects on gender wage gaps in three countries</a></em></h3>

    <h5>Published at Labour Economics - <a href="https://doi.org/10.1016/j.labeco.2024.102506">https://doi.org/10.1016/j.labeco.2024.102506</a></h5>

<div class="button-container">
<details>
  <summary>Abstract</summary>
    <p class="text-justify">
    A vast literature on gender wage gaps has examined the importance of selection into employment. However, most analyses have focused only on female labour force participation and gaps at the median. The Great Recession questions this approach because of the major shift in male employment that it implied. This paper uses the methodology proposed by Arellano and Bonhomme (2017) to estimate a quantile selection model over the period 2007–2018. Using a tax and benefit microsimulation model, I compute an instrument capturing both male and female decisions to participate in the labour market: the potential out-of-work income. Since my instrument is crucially determined by the welfare state, I consider three countries with notably different benefit systems – the UK, France, and Finland. My results imply different selection patterns across countries and a sizeable male selection in France and the UK. Correction for selection bias lowers the gender wage gap and reveals a substantial glass ceiling with different magnitudes. Findings suggest that disparities between these countries are driven by occupational segregation and public spending on families.
  </p>
</details>

 
<details>
  <summary>Presentations</summary>
Presentations: EALE 2023, LAGV 2023, Ninth ECINEQ Meeting of The Society for the Study of Economic Inequality, ECINEQ PhD Workshop participants at the London School of Economics, 14th Workshop on Labour Economics (IAAEU), the 4th QMUL Economics Workshop for PhD and Post-doctoral Students, the 2022 French Stata conference, PhD seminar at the Aix-Marseille School of Economics, Labour Chair seminar at the Paris School of Economics
</details>
</div>


</div>

<!-- Right-hand side: Carousel -->
<div class="jmp-carousel">

<div class="carousel">
  <div class="carousel-images">
    <img src="https://raw.githubusercontent.com/elasskenza/website/main/assets/selection/1.png" alt="Slide sel1">
    <img src="https://raw.githubusercontent.com/elasskenza/website/main/assets/selection/2.png" alt="Slide sel2">
    <img src="https://raw.githubusercontent.com/elasskenza/website/main/assets/selection/3.png" alt="Slide sel3">
    <img src="https://raw.githubusercontent.com/elasskenza/website/main/assets/selection/4.png" alt="Slide sel4">
  </div>
  <div class="carousel-buttons">
    <button class="carousel-button prev">❮</button>
    <button class="carousel-button next">❯</button>
  </div>
</div>

</div>
</div>

<script>
document.querySelectorAll('.carousel').forEach((carousel) => {
  const carouselImages = carousel.querySelector('.carousel-images');
  const images = carousel.querySelectorAll('.carousel img');
  const prevButton = carousel.querySelector('.carousel-button.prev');
  const nextButton = carousel.querySelector('.carousel-button.next');

  let currentIndex = 0;

  function updateCarousel() {
    const width = images[0].clientWidth;
    carouselImages.style.transform = `translateX(-${currentIndex * width}px)`;
  }

  function nextImage() {
    currentIndex = (currentIndex + 1) % images.length;
    updateCarousel();
  }

  function prevImage() {
    currentIndex = (currentIndex - 1 + images.length) % images.length;
    updateCarousel();
  }

  nextButton.addEventListener('click', nextImage);
  prevButton.addEventListener('click', prevImage);

  // Auto-rotate every 10 seconds
  setInterval(nextImage, 10000);
});

</script>


# Working Papers

---------------------------------------------------------------------------------------------------------------------------------------------------------------


<div class="jmp-container">
  
<!-- Left-hand side: Markdown content -->
<div class="jmp-content">

    <h3><em>Automating Inequality: Gender Bias in AI-mediated Labor Markets</em></h3>
 With Germain Gauthier (Bocconi University), Debora Nozza (Bocconi University) & Paola Profeta (Bocconi University) - <a href="https://www.socialscienceregistry.org/trials/13538/history/220793">Link to the AEA Pre-analysis Plan</a>, Previously "Generative AI & Labor Market Discrimination"  
    <br>
	 <br> 
	 
     <h4>
<p style="color: #237ecf;">
  Revise & Resubmit at
  <a href="https://www.pnas.org/" style="font-weight: bold; color: #237ecf;">
    PNAS (Proceedings of the National Academy of Sciences)
  </a> 
</p>
</h4> 

    
     <h5>Working paper available upon request
    </h5>
<br>
  <div class="button-container">
<details>
  <summary>Abstract</summary>
    <p class="text-justify">
	The rise of Generative Artificial Intelligence (GenAI) has led to the widespread adoption of automated CV generation services for job seekers and CV screening services for employers. We study the consequences of using GenAI for such tasks. We find that GenAI systematically reproduces and can even amplify gender biases. It generates gender-stereotyped CVs and recommends lower earnings for female job seekers. We also run a series of online experiments inspired by classical correspondence studies, which measure hiring discrimination by comparing employer responses to equivalent CVs that differ only by gender. Our results show that GenAI penalizes female candidates during CV screening in male-dominated occupations. These patterns persist even when models are explicitly instructed to remain gender-neutral. Our findings provide the first direct evidence that GenAI can reinforce structural labor market inequalities, potentially disadvantaging women at every stage of the job search. 
  </p>
</details>

<details>
  <summary>Presentations</summary>
   TASKS VII Conference: The Economic Impacts of AI on Work and Labor Markets, 4th Workshop on Field Experiments in Economics and Business, 10th CEPR Text-As-Data Workshop,  2025 Workshop in Gender Economics at ENS de Lyon, 5th Discrimination and Diversity Workshop, LAGV 2025, Dondena AI and Society Initiative Seminar at Bocconi University, Advanced AI Methods Workshop, CREM Seminar at Rennes University, Applied Economics Lunch Seminar of the Paris School of Economics, Gender Inequality Workshop at the London School of Economics, Discrimination and the Inequalities in the Age of AI Workshop at Sciences Po
  </details>
</div>

<p><em>Supported by the <a href="https://dauphine.psl.eu/en/women-and-science">Women and Science</a> Chair Grant</em></p>


</div>  
</div>  




---------------------------------------------------------------------------------------------------------------------------------------------------------------



<div class="jmp-container">
  
<!-- Left-hand side: Markdown content -->
<div class="jmp-content">


    <h3><em>What do women want in a job? Household constraints, gender-biased decisions and the reservation wage </em></h3>
    <h4>
<p style="color: #237ecf;">
  This paper was awarded the 
  <a href="https://www.siepweb.it/siep/wp/en/en/premio-etta-chiuri/" style="font-weight: bold; color: #237ecf;">
    Etta Chiuri Prize 2025
  </a> 
  by the Italian Society of Public Economics.
</p>
</h4>
    <h5>Draft available here: 
      <a href="https://www.dropbox.com/scl/fi/vcikrhj1dvwrig3jwfnvj/JMP_Kenza_Elass.pdf?rlkey=kncf3g3ofj1zgbz53vc098nuh&st=e6poxbut&dl=0">Dropbox link</a>
    </h5>

<div class="button-container">
<details>
  <summary>Abstract</summary>
    <p class="text-justify">
 Recent explanations of the gender wage gap emphasize the role of gender differences in job search, yet the role of childcare constraints remains underexplored. This paper uses French administrative data to investigate how childcare constraints shape women’s reservation wage and job search strategies. First, I assess the types of occupations that men and women apply for and the implications for the reservation wage gap. Using text analysis, I create a novel dataset classifying occupations based on amenities and job content. Quantile decomposition methods allow me to document an unequal gap in reservation wage, intensifying along the distribution, partially explained by gender biased choices in the temporal flexibility associated with the desired job.  Given that gender differences in targeted amenities may be shaped by childcare constraints, could a reduction in childcare costs change women's job search strategies? To address this question, I assess to which extent a 2018 reform, which increased childcare benefits for single-parent households by 30%, influenced the reservation wage and job-search strategies of women. Using a difference-in-differences strategy and spatial variation in childcare service availability, results indicate that the reduction in childcare costs led women to lower their reservation wages. However, I also find that more affordable access to flexible childcare increases the likelihood of targeting occupations requiring greater temporal flexibility and the desired maximum commute, thereby enabling them to secure more stable jobs and improve their reemployment outcomes. Lastly, I show that policies of childcare cost reduction are only truly effective when combined with childcare services availability.
  </p>
</details>

<details>
  <summary>Presentations</summary>
  <ul>
    <li>  Bank of Italy Gender Economics Workshop*,  SIEP 2025 Conference, ECONtribute and C-SEB Design & Behavior Seminar at Cologne University, Areena JMC Symposium, EEA-ESEM 2024, EALE 2024, Junior Economist Meeting 2024, 2024 Junior Research Day at College de France, Afépop 2024, ADRES 2023, AFSE 2023, European Association of Labour Economists (EALE) Conference 2022, International Association for Applied Econometrics (IAAE) Conference 2022, LAGV 2022, JMA 2022, Food for Thought seminar at Bocconi University, Labour Chair Seminar at the Paris School of Economics, Firms and market seminar at CREST, Core Brown Bag Seminar at Louvain University, ADRES 2023 and PhD seminar at the Aix Marseille School of Economics </li>
  </ul>
</details>
</div>

<details>
  <summary>Paper</summary>
  <div style="overflow: auto; -webkit-overflow-scrolling: touch; margin-top: 10px;">
    <iframe src="../assets/JMP_Kenza_Elass.pdf" style="width: 100%; height: 80vh;" frameborder="0">
        This browser does not support PDFs. Please download the PDF to view it: 
        <a href="../assets/JMP_Kenza_Elass.pdf">Download PDF</a>.
    </iframe>
  </div>
</details>

</div>

<!-- Right-hand side: Carousel -->
<div class="jmp-carousel">

<div class="carousel">
  <div class="carousel-images">
    <img src="https://raw.githubusercontent.com/elasskenza/website/main/assets/JMP/figure_2.png" alt="Slide 1">
    <img src="https://raw.githubusercontent.com/elasskenza/website/main/assets/JMP/figure_4.png" alt="Slide 2">
    <img src="https://raw.githubusercontent.com/elasskenza/website/main/assets/JMP/figure_5.png" alt="Slide 3">
    <img src="https://raw.githubusercontent.com/elasskenza/website/main/assets/JMP/figure_6.png" alt="Slide 4">
    <img src="https://raw.githubusercontent.com/elasskenza/website/main/assets/JMP/figure_8.png" alt="Slide 5">
    <img src="https://raw.githubusercontent.com/elasskenza/website/main/assets/JMP/figure_9.png" alt="Slide 6">
    <img src="https://raw.githubusercontent.com/elasskenza/website/main/assets/JMP/figure_10.png" alt="Slide 7">
    <img src="https://raw.githubusercontent.com/elasskenza/website/main/assets/JMP/figure_11.png" alt="Slide 8">
  </div>
  <div class="carousel-buttons">
    <button class="carousel-button prev">❮</button>
    <button class="carousel-button next">❯</button>
  </div>
</div>

</div>
</div>

<script>
document.querySelectorAll('.carousel').forEach((carousel) => {
  const carouselImages = carousel.querySelector('.carousel-images');
  const images = carousel.querySelectorAll('.carousel img');
  const prevButton = carousel.querySelector('.carousel-button.prev');
  const nextButton = carousel.querySelector('.carousel-button.next');

  let currentIndex = 0;

  function updateCarousel() {
    const width = images[0].clientWidth;
    carouselImages.style.transform = `translateX(-${currentIndex * width}px)`;
  }

  function nextImage() {
    currentIndex = (currentIndex + 1) % images.length;
    updateCarousel();
  }

  function prevImage() {
    currentIndex = (currentIndex - 1 + images.length) % images.length;
    updateCarousel();
  }

  nextButton.addEventListener('click', nextImage);
  prevButton.addEventListener('click', prevImage);

  // Auto-rotate every 10 seconds
  setInterval(nextImage, 10000);
});

</script>

---------------------------------------------------------------------------------------------------------------------------------------------------------------


<div class="jmp-container">
  
<!-- Left-hand side: Markdown content -->
<div class="jmp-content">

    <h3><em>Gender gaps in the urban wage premium</em></h3>
	
 With Cecilia García-Peñalosa (AMSE, CNRS, EHESS) & Christian Schluter (AMSE) -
 <a href="https://cepr.org/publications/dp19592">Link to the CEPR Working Paper</a> - 
      <a href="https://www.cesifo.org/en/publications/2024/working-paper/gender-gaps-urban-wage-premium">Link to the CESifo Working Paper</a> - 
	  <a href="https://drive.google.com/file/d/1XK1jeGmbXEah44l8Fp0DoNe3CYC6LRDc/view">Appendix</a>  
   <br>
    <br>
   
    <h5> Under Review
    </h5>  

<br>
<div class="button-container">
<details>
  <summary>Abstract</summary>
    <p class="text-justify">
	We examine the economic geography of gender wage gaps to understand the role that location plays in gender earning differences. Using panelised administrative data for the universe of French workers, our findings indicate that women benefit relatively more from density than men, with an urban wage premium (return to urban density) 48% higher than for men. We identify a number of factors that explain this gap, with a large share being explained by the structure of the local labour market, notably, the extent of occupational segregation. Another important factor is commuting patterns, while childcare availability plays only a moderate role.
  </p>
</details>

<details>
  <summary>Presentations</summary>
  King’s Junior Research Day 2023, ADRES 2023, GRAPE 2023 Gender Gaps Conference, Bocconi Food for Thought seminar, PhD seminar at the Aix Marseille School of Economics, Paris School of Economics Labour Chair seminar; COSME workshop, 3rd Workshop on Public Policies, Urban Economics Association Conference 2024, IAAE Conference 2024, <a href="https://cepr.org/events/third-middle-east-spatial-and-international-economics-conference-mesie" target="_blank">CEPR MESIE Conference</a>
  </details>
</div>

<h6>Communication: <p><a href="https://nadaesgratis.es/admin/la-geografia-de-las-desigualdades-salariales-entre-mujeres-y-hombres" target="_blank">Nada es Gratis</a></p> </h6>

</div>

<!-- Right-hand side: Carousel -->
<div class="jmp-carousel">

<div class="carousel">
  <div class="carousel-images">
    <img src="https://raw.githubusercontent.com/elasskenza/website/main/assets/uwp/1.png" alt="Slide 1">
    <img src="https://raw.githubusercontent.com/elasskenza/website/main/assets/uwp/2.png" alt="Slide 2">
    <img src="https://raw.githubusercontent.com/elasskenza/website/main/assets/uwp/3.png" alt="Slide 3">
  </div>
  <div class="carousel-buttons">
    <button class="carousel-button prev">❮</button>
    <button class="carousel-button next">❯</button>
  </div>
</div>

</div>
</div>

<script>
document.querySelectorAll('.carousel').forEach((carousel) => {
  const carouselImages = carousel.querySelector('.carousel-images');
  const images = carousel.querySelectorAll('.carousel img');
  const prevButton = carousel.querySelector('.carousel-button.prev');
  const nextButton = carousel.querySelector('.carousel-button.next');

  let currentIndex = 0;

  function updateCarousel() {
    const width = images[0].clientWidth;
    carouselImages.style.transform = `translateX(-${currentIndex * width}px)`;
  }

  function nextImage() {
    currentIndex = (currentIndex + 1) % images.length;
    updateCarousel();
  }

  function prevImage() {
    currentIndex = (currentIndex - 1 + images.length) % images.length;
    updateCarousel();
  }

  nextButton.addEventListener('click', nextImage);
  prevButton.addEventListener('click', prevImage);

  // Auto-rotate every 10 seconds
  setInterval(nextImage, 10000);
});

</script>





<br>
<br>

# Selected work in progress 

---------------------------------------------------------------------------------------------------------------------------------------------------------------

  *  **_Gender Norms and Child Development_**, with Hélène Le Forner (CREM) 
  * **_Changing the media narrative: the role of social movements_**, with Caroline Coly (IEB) and Mahima Vasishth (Bocconi University)
  * **_Is artificial intelligence turning the tables on gender wage inequality?_**, With Fabien Petit (UCL, University of Barcelona) and Paola Profeta (Bocconi University) 

<br>
<br>


<section>
  <h2>Other Writing - General Audience</h2>
  <h3><i>Threat or opportunity? The impact of AI on women</i></h3>
  <p>With Paola Profeta (Bocconi University)</p>

  <div class="button-container">
    <details>
      <summary>Abstract</summary>
      <p class="text-justify">
        The adoption of AI in various sectors has led to changes that present both opportunities and challenges for gender equality. Although AI appears to be less biased than human decision-makers, the literature also suggests it perpetuates stereotypes and inequalities between men and women. The unequal use of AI tools, combined with existing disparities in education and employment, may further disadvantage women in the labour market. In addition, AI's influence on employment, wage inequality and gender bias in healthcare has not been sufficiently studied, raising ethical questions about the fairness and transparency of these technologies. Addressing these challenges involves an increase in diversity in data-science teams, diverse and representative datasets, and promoting gender-inclusive training programs. Ultimately, the impact of AI on gender equality will depend on today's initiatives to neutralize the effects of AI.
      </p>
    </details>

    <details>
      <summary>Paper</summary>
      <div>
        <iframe src="../assets/pdf/Elass_profeta_AI_Gender.pdf" style="width: 100%; height: 80vh;" frameborder="0">
          This browser does not support PDFs. Please download the PDF to view it:
          <a href="../assets/pdf/Elass_profeta_AI_Gender.pdf">Download PDF</a>.
        </iframe>
      </div>
    </details>
  </div>

  <div>
    <h4>Communication</h4>
    <p>
      <a href="https://www.repubblica.it/dossier/economia/top-story/2024/11/11/news/ia_opportunita_e_minaccia_per_l_uguaglianza_di_genere-423611448/" target="_blank">
        La Repubblica
      </a>
    </p>
  </div>
</section>

