<script>
  let contacts = [
    {
      type: "Email",
      icon: "mail",
      item: "joey.h.bellerose@gmail.com",
      method: "mailto:joey.h.bellerose@gmail.com"
    },
    {
      type: "LinkedIn",
      icon: "linkedin",
      item: "https://linkedin.com/in/joey-bellerose-707271139/",
      method: "https://linkedin.com/in/joey-bellerose-707271139/"
    },
    {
      type: "Github",
      icon: "github",
      item: "https://github.com/joeybellerose",
      method: "https://github.com/joeybellerose"
    }
  ];
  let tools = [
    { name: "R", amount: 90 },
    { name: "Excel", amount: 85 },
    { name: "Python", amount: 75 },
    { name: "HTML", amount: 75 },
    { name: "Tableau", amount: 75 },
    { name: "Javascript", amount: 50 }
  ];
  let jobs = [
    {
      employer: "NAVAIR",
      date: "2012-Present",
      list: [
        { description: "Obtained Top Secret clearance" },
        {
          description:
            "Started and led analytics teams on multiple billion dollar programs"
        },
        {
          description:
            "Developed data-driven model to enable proposel-less negotiations and reduce time to award by ~18 months"
        },
        {
          description:
            "Reduced contract cost by ~25% from proposed resulting in ~$220M in cost avoidance"
        },
        {
          description:
            "Created vision for data analytics implementation within PEO-U&W"
        },
        {
          description: "Created digital strategy between DCMA and PMA-280"
        },
        {
          description:
            "Leveraged big data from contractor to provide new insights into duplicate proposing due to concurrent programs"
        },
        {
          description:
            "Built analytical tools to enable deep-dive into contractor proposals"
        },
        {
          description:
            "Developed in-house models for Learning Curves, Budget Phasing Projections and Staffing Profiles"
        },
        {
          description:
            "Built machine learning algorithm to project future aircraft development costs"
        },
        {
          description: "Beta-tester for new Data Science OpenShift Plaform"
        }
      ]
    },
    {
      employer: "Tecolote",
      date: "2009-2012",
      list: [
        { description: "Obtained Secret clearence" },
        {
          description:
            "Led development and coordination of cost models and data collection on multiple projects within PMA-281"
        },
        {
          description:
            "Developed Cost models useing Excel, ACEIT, PRICE S, COCOMO II and NEMO"
        },
        {
          description:
            "Identified major cost and programatic risk drivers using Monte-Carlo and Latin-Hypercube techniques"
        }
      ]
    }
  ];
</script>

<style>
  #side {
    background-color: #000080;
    color: white;
  }
  #side h3 {
    color: white;
  }
  #side a {
    color: white;
  }
  #side h1,
  h5 {
    color: white;
  }
</style>

<div class="uk-grid-match" uk-grid>
  <div id="side" class="uk-width-1-4">
    <div class="">
      <!-- <img data-src="testpic.jpg" width="" height="" alt="" uk-img /> -->
      <h1 class="uk-title">Joey Bellerose</h1>
      <br />
      <h3>Data Science/Operations Research</h3>

    </div>
    <div class="uk-card">
      <h3 class="uk-card-title">About</h3>
      <p>Helping people automate decisions and explore options</p>
    </div>
    <div class="uk-section">
      <h3 class="uk-card-title">Contact</h3>
      {#each contacts as contact}
        <span uk-icon={contact.icon} />
        <a href={contact.method}>{contact.item}</a>
        <br />
      {/each}
    </div>
    <div class="uk-card">
      <h3 class="uk-card-title">Tools</h3>
      {#each tools as tool}
        <span>{tool.name}</span>
        <div class="uk-margin-right">
          <progress class="uk-progress" value={tool.amount} max="100" />
        </div>
      {/each}
    </div>

  </div>
  <div id="main" class="uk-width-3-4" uk-grid>
    <div class="uk-card uk-card-body uk-card-default uk-card-hover">
      <h3 class="uk-card-title">Objective</h3>
      <p>
        To build a world class team that drives out the complexities of modern
        decision making in order to simplify running an organization.
      </p>
    </div>
    <div class="uk-card uk-card-body uk-card-default uk-card-hover">
      <h3 class="uk-card-title">Work</h3>
      <div uk-grid>
        {#each jobs as { employer, date, list }}
          <div class="uk-width-3-4">
            <h5 class="uk-text-primary">{employer}</h5>
          </div>
          <div class="uk-width-1-4">
            <h5 class="uk-text-primary uk-text-right">{date}</h5>
          </div>
          <ul>
            {#each list as task}
              <li class="uk-width-1 uk-margin-small">{task.description}</li>
            {/each}
          </ul>
        {/each}
      </div>
    </div>
    <div class="uk-card uk-card-body uk-card-default uk-card-hover">
      <h3 class="uk-card-title">School</h3>
      <h5 class="uk-text-primary">St. Mary's College of Maryland</h5>
      <div uk-grid>
        <div class="uk-width-3-5">
          <p>Bachelors of Arts - B.A, Economics</p>
        </div>
        <div class="uk-width-2-5">
          <p class="uk-text-right">December 2008</p>
        </div>
      </div>
    </div>
    <div class="uk-card uk-card-body uk-card-default uk-card-hover">
      <h3 class="uk-card-title">Awards</h3>
      <div uk-grid>
        <div class="uk-width-3-5">
          <p>PMA-281 Letter of Commendation</p>
        </div>
        <div class="uk-width-2-5">
          <p>December 2012</p>
        </div>
      </div>
    </div>
  </div>
</div>

<svelte:head>
  <!-- UIkit CSS -->
  <link rel="stylesheet" href="uikit.css" />

  <!-- UIkit JS -->
  <script src="uikit.js">

  </script>
  <script src="uikit-icons.js">

  </script>
</svelte:head>
