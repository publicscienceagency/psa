---
published_at: 11.30.2016 02:00
image: hosny.gif
description: Economic simulation and game for speculating alternative economies
process:
    - 3D design
    - Simulation design
    - Game design
links:
    Research: https://www.tumblr.com/blog/humansofsimulatedny
    Source: https://github.com/frnsys/hosny
    Writeup: http://spaceandtim.es/projects/hosny
top_image: /assets/posts/hosny.gif
intro:
    - "HOSNY is a participative agent-based simulation built to speculate alternative economies. It asks how world-building as interactive gameplay creates the opportunity for a better and more complete understanding of the complex relationships that make up the systems of our world."
    - "Players set a virtual model of New York with simulated citizens, built using data based on the U.S. Census and agent-based modeling, according to their preferences of how the world should function. They are then assigned a character from this simulated pool and given the chance to steer the future of the city through a simple democracy: players take turns voting on important issues at the end of each play session."
tools:
    System Designer (SYD):
        url: https://github.com/frnsys/system_designer
        description: "A simple agent-based modeling framework, supporting distributed computation"
        images:
            - /assets/posts/syd01.gif
            - /assets/posts/syd02.gif
            - /assets/posts/syd03.gif
            - /assets/posts/syd04.gif
---

# Humans of Simulated New York

HOSNY is an initial exploration into accessible and narrative economic simulation, inspired by projects such as [Cybersyn](https://www.jacobinmag.com/2015/04/allende-chile-beer-medina-cybersyn/) and [Dwarf Fortress](http://www.nytimes.com/2011/07/24/magazine/the-brilliance-of-dwarf-fortress.html) and early attempts to answer Frederic Jameson's call in _Postmodernism_ for "a situational representation on the part of the individual subject to that vaster and properly unrepresentable totality which is the ensemble of society's structures as a whole" and Nick Srineck's similar sentiment in his _Accelerationism - Epistemic, Economic, Political_ essay (emphasis added):

> So this is one thing that can help out in the current conjuncture: economic models which adopt the programme of epistemic accelerationism, which reduce the complexity of the world into aesthetic representations, which offer pragmatic purchase on manipulating the world, and which are all oriented toward the political accelerationist goals of building and expanding rational freedom. __These can provide both navigational tools for the current world, and representational tools for a future world.__

We generated "plausible" simulated citizens from a model learned from New York City American Community Survey (ACS) data spanning 2005-2014 (see below for specific data sources). Using [agent-based simulation](https://en.wikipedia.org/wiki/Agent-based_model), citizens go about their days, starting businesses (if they can afford it) or working (if they can get hired), and try to live as satisfying a life as possible.

Their activity is reflected through a 3D city which ebbs according to the businesses that form the economy. Weaving through the city are avatars of the citizens, coded according to race and socioeconomic status so that the structure of the economy is laid bare.

[![](/assets/work/hosny/disparity.gif)](/assets/work/hosny/disparity.gif)

Parameters for the simulation are, where possible, derived from data. For example, a citizen's success at finding a job is based on the ACS data, so structural inequality is captured by the simulation.

[![](/assets/work/hosny/setup.png)](/assets/work/hosny/setup.png)

Other parameters are defined by the players which allow them to play in worlds alternate to our own. They can, for instance, see what happens in a society where a blight has wiped out most agriculture or a society where high levels of automation are present.

[![](/assets/work/hosny/player.png)](/assets/work/hosny/player.png)

Players are randomly assigned a citizen and can periodically propose and vote on new legislation to affect the outcome of the city. Their "success" is conveyed through a variety of indices displayed behind the city.

[![](/assets/work/hosny/vote.png)](/assets/work/hosny/vote.png)

## Design

This graphic provides an overview of how we designed the simulation components.

[![](/assets/work/hosny/design.png)](/assets/work/hosny/design.png)

## Data

- [Frequently Occurring Surnames from the Census 2000](http://www.census.gov/topics/population/genealogy/data/2000_surnames.html). Surnames occurring >= 100 more times in the 2000 census. ([details here](http://www2.census.gov/topics/genealogy/2000surnames/surnames.pdf))
- [Female/male first names from the Census 1990](http://deron.meranda.us/data/)
- Household and individual IPUMS data for 2005-2014, retrieved from [IPUMS USA, Minnesota Population Center, University of Minnesota](https://usa.ipums.org/usa/index.shtml)
- PUMS network map of NY, hand-compiled from the [NYC PUMA map](http://www.nyc.gov/html/dcp/pdf/census/puma_cd_map.pdf)
- NYC unemployment data was retrieved from [New York State Department of Labor](https://labor.ny.gov/stats/laus.asp)
- S&P500 data was retrieved from Open Knowledge's [Standard and Poor's (S&P) 500 Index Data including Dividend, Earnings and P/E Ratio](http://data.okfn.org/data/core/s-and-p-500)
- Friendship model parameters were taken from [Social Distance in the United States: Sex, Race, Religion, Age, and Education Homophily among Confidants, 1985 to 2004](http://digitalcommons.unl.edu/cgi/viewcontent.cgi?article=1254&context=sociologyfacpub). Jeffrey A. Smith, Miller McPherson, Lynn Smith-Lovin. University of Nebraska - Lincoln. 2014.
- Annual expenses calculated from [Living Wage Calculator](http://livingwage.mit.medu/counties/36061) (Amy K. Glasmeier, Carey Anne Nadeau, Eric Schultheis, 2014).
