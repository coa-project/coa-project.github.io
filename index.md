#  PyCoA release v2.0 <img src="fig/logo-anime.gif" width="140px" align=top> 
April 2020 - February 2021 

<section id="downloads" class="clearfix">
  <a href="https://github.com/coa-project/pycoa/archive/v2.0.zip" id="download-zip" class="button" target=_blank><span>Download .zip</span></a>
  <a href="https://github.com/coa-project/pycoa/archive/v2.0.tar.gz" id="download-tar-gz" class="button" target=_blank><span>Download .tar.gz</span></a>
  <a href="https://github.com/coa-project/pycoa/tree/v2.0" id="view-on-github" class="button" target=_blank><span>View on GitHub</span></a>
</section>

[<img src="fig/UK.png" height="14px" alt="UK flag"> English  version ](http://pycoa.fr) / 
[ <img src="fig/FR.png" height="14px" alt="FR flag"> Version française ](http://pycoa.fr/index_FR) 

`PyCoA` (Python Covid Analysis) is a Python™ framework which provides:
- a simple access to common Covid-19 databases;
- tools to represent and analyse Covid-19 data such as time series plots and maps.

<img src="fig/pycoa_plot_example.png" height="200px" align=top> <img src="fig/pycoa_map_example.png" height="200px" align=bottom> 

<img src="fig/pycoa_hist_example.png" height="200px" align=top> <img src="fig/pycoa_get_example.png" height="200px" align=top>

It is designed to be accessible to non-specialists: teenagers learning Python™, students, science journalists, even scientists who are not familiar in data access methods. A simple analysis can be performed out of the box, as well as a more complex analysis for people familiar with Python™ programming. As an example, after <a href="https://github.com/coa-project/pycoa/wiki/Install" target=_blank>installing pycoa</a> to your framework, the following few lines of code produce the four figures introducing this short documentation.

```python
import coa.front as cf
cf.plot(where=['France', 'Italy', 'United kingdom'], which='deaths', what='cumul')
cf.map(where=['world'],what='daily',when='01/04/2020')
cf.hist(where='middle africa', which='confirmed',what='cumul')
cf.get(where=['usa'], what='daily', which='recovered',output='pandas')
```

`PyCoA` works currently inside `Jupyter` notebook, over a local install or on online platforms such as <a href="https://colab.research.google.com/" target=_blank>Google Colab</a>.

A basic demo code is available as a notebook on <a href="https://github.com/coa-project/coabook/blob/master/demo_pycoa.ipynb" target=_blank ><img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" height="20" alt="GitHub logo" /> GitHub</a>, on <a href="https://colab.research.google.com/github/coa-project/coabook/blob/master/demo_pycoa.ipynb" target=_blank ><img src="https://colab.research.google.com/img/colab_favicon_256px.png" height="20" alt="Google colab logo" /> Google Colab</a>, or on <a href="https://nbviewer.jupyter.org/github/coa-project/coabook/blob/master/demo_pycoa.ipynb" target=_blank ><img src="https://nbviewer.jupyter.org/static/img/nav_logo.svg" height="20" alt="NbViewer logo" /> Jupyter NbViewer</a>. Other notebooks are providing in our <a href="https://github.com/coa-project/coabook/blob/master/README.md" target=_blank >coabook page</a>.

Full documentation is on <a href="https://github.com/coa-project/pycoa/wiki/Home" target=_blank>the Wiki</a>.

### Authors

* Tristan Beau - [Université de Paris](http://u-paris.fr) - [LPNHE laboratory](http://lpnhe.in2p3.fr/)
* Julien Browaeys - [Université de Paris](http://u-paris.fr) - [MSC laboratory](http://www.msc.univ-paris-diderot.fr/)
* Olivier Dadoun - [CNRS](http://cnrs.fr) - Sorbonne Université](https://www.sorbonne-universite.fr/) - [LPNHE laboratory](http://lpnhe.in2p3.fr/)

### Contact
* [`support@pycoa.fr`](mailto:support@pycoa.fr)
* This page : [`pycoa.fr`](http://pycoa.fr)

<a href="https://twitter.com/pycoa_fr?ref_src=twsrc%5Etfw" class="twitter-follow-button" data-show-count="false">Follow @pycoa_fr</a>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
