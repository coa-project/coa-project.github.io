[<img src="fig/UK.png" height="14px" alt="UK flag"> English  version ](http://www.pycoa.fr/index) /
[ <img src="fig/FR.png" height="14px" alt="FR flag"> Version française ](http://www.pycoa.fr/index_FR)

<section id="downloads" class="clearfix">
  <a href="https://github.com/coa-project/pycoa/archive/main.zip" id="download-zip" class="button" target=_blank><span><img src="https://upload.wikimedia.org/wikipedia/commons/9/9c/The_Unarchiver_zip.png" height="25px" align="bottom" alt="zip icon from wikipedia">Archive .zip</span></a>
  &nbsp;&nbsp;&nbsp;&nbsp;
  <a href="https://github.com/coa-project/pycoa/archive/main.tar.gz" id="download-tar-gz" class="button" target=_blank><span>
    <img src="https://upload.wikimedia.org/wikipedia/commons/e/e4/Tar_gz_archive_icon.svg" height="25px" align="bottom" alt="targz icon from wikipedia">Archive .tar.gz</span></a>
  &nbsp;&nbsp;&nbsp;&nbsp;
  <a href="https://github.com/coa-project/pycoa/tree/main" id="view-on-github" class="button" target=_blank><span><img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" height="25px" align="bottom" alt="github icon from github">Voir sur GitHub</span></a>
  &nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://gitlab.in2p3.fr/lpnhe/pycoa" id="view-on-gitlab" class="button" target=_blank><span><img src="https://raw.githubusercontent.com/wiki/coa-project/pycoa/figs/gitlab.png" height="25px" align="bottom" alt="github icon from github">Voir sur GitLab IN2P3</span></a>
</section>

<!--center>
<iframe id="mobilehide" height="460" width="580" src="fig/mapFranceVariant.html" frameborder="0"></iframe>
</center-->

`PyCoA` (Python Covid Analysis) est un ensemble de code Python™ qui fournit :
- un accès simple aux bases de données sur la <a href="https://www.who.int/fr/emergencies/diseases/novel-coronavirus-2019/question-and-answers-hub">Covid19</a> ;
- des outils pour représenter et analyser les données de la Covid19, comme des séries temporelles ou des cartes.

Cet environnement est pensé pour être accessible à des non-spécialistes : des lycéen·nes qui apprennent Python™, des étudiant·es, des journalistes scientifiques, voire même des chercheurs et chercheuses qui ne sont pas famillier·es avec l'extraction de données. Des analyses simples peuvent être directement effectuées, et des analyses plus poussées peuvent être produites par les personnes habituées à programmer en Python™.

L'outil `PyCoA` assure l'accès à plusieurs bases de données et fourni un format standardisé pour les données. Il assure par ailleurs une jointure transparente avec des bases concernant géo-localisation (gestion des noms de pays ou de régions, possibilité de jointures sur des bases avec des description différentes, création de cartes). Ces informations de géolocalisation peuvent par ailleurs être utilisées pour d'autres application en dehors des aspects Covid19.

L'outil `PyCoA` est pensé pour être utilisé dans un environnement [jupyter](https://jupyter.org/), installé localement ou bien sur un serveur distant (comme le propose par exemple [google colaboratory](https://colab.research.google.com/) ou [binder](https://mybinder.org/)). Cela en simplifie l'[installation](https://github.com/coa-project/pycoa/wiki/Installation) et assure grâce à la librairie [`Bokeh`](https://bokeh.org/) des sorties graphiques performantes avec très peu de lignes de code pour l'utilisateur comme en attestent les quelques lignes de code suivantes et les sorties associées.

```python
import coa.front as cf
cf.plot(where=['France', 'Italy', 'United kingdom'])
cf.map(where='world',what='daily',when='01/04/2020')
cf.hist(where='middle africa', which='tot_confirmed',what='cumul')
cf.get(where='usa', what='daily', which='tot_recovered',output='pandas')
```
<img src="https://raw.githubusercontent.com/wiki/coa-project/pycoa/figs/pycoa_plot_example.png" height="240" align=top />
<img src="https://raw.githubusercontent.com/wiki/coa-project/pycoa/figs/pycoa_map_example.png" height="240" align=top />
<br/>
<img src="https://raw.githubusercontent.com/wiki/coa-project/pycoa/figs/pycoa_hist_example.png" height="240" align=top />
<img src="https://raw.githubusercontent.com/wiki/coa-project/pycoa/figs/pycoa_get_example.png" height="240" width="300" align=top />

## À propos

Physiciens sur des expériences en physique des particules au [CERN](https://home.cern/) ou en physique de la matière complexe, habitués à la gestion de _big data_, nous avons souhaité partager nos compétences en statistiques et gestion de données au plus grand nombre pour ce qui concerne l'analyse de données liées à la pandémie de la Covid19 au travers le monde.
L'exploration de données et les statistiques devraient pouvoir aider toutes et tous à mieux comprendre un des phénomènes les plus importants de l'histoire récente.

Pour cela nous proposons le projet `PyCoA`, pour _Python™ Covid19 Analysis_, un outil de statistique qui peut s'utiliser en ligne, avec une interface simple et des schémas de modélisation clairs. La version proposée en ligne peut notamment s'utiliser au travers [Google Colaboratory](https://colab.research.google.com/) ou de [Binder](https://mybinder.org/), une infrastructure de notebooks Python™, et ce, sans aucun effort d'installation.
Cela permet en outre un travail collaboratif par le partage de _notebooks_ sur le nuage de `google colab`, ce dernier permettant de plus l'utilisation d'une infrastructure de calcul énorme (incluant aussi des GPU pour de futures analyses de _deep learning_ des données Covid19).

## Origines

Le projet `PyCoA`, initialement désigné `CoCoA`, a vu le jour initialement à partir de la participation en avril 2020 à l'hackathon organisé par [UltraHack.org](https://ultrahack.org/covid-19datahack).
Retenu en phase final mais non sorti vainqueur, le projet se veut libre et gratuit à code source ouvert. Il a continué d'évoluer depuis et a subi une mise à jour majeure lors du [Hackathon Covid19](https://hackathon-covid.fr) animé par la [Direction interministérielle de la transformation publique](https://www.modernisation.gouv.fr/) en avril 2021.

Son code est public ainsi que les `notebooks` et servent de références ou d'exemples d'utilisation lors d'animations ou d'ateliers (lors du [Salon Culture et Jeux Mathématiques 2021](https://salon-math.fr/) ou lors de la [Fête de la Science 2021](https://www.fetedelascience.fr/)).

## `PyCoA`: logiciel générique d'analyses numériques en `Python`
Le projet a été développé à l'origine pour des études épidémiologiques liées à la Covid19. Il pourra cependant être utilisé pour d'autres types d'études.   
Ainsi, des analyses comportant des données avec des séries temporelles associées à des variables numériques et géographiques, pourront utiliser `PyCoA`. Leurs études seront grandement simplifiées et ceux avec des représentations graphiques claires et précises .    


## Licence

Le projet `PyCoA` est sous [licence MIT](https://github.com/coa-project/pycoa/blob/main/LICENSE).

## Auteurs

* Tristan Beau - [Université de Paris](http://u-paris.fr) - [LPNHE laboratory](http://lpnhe.in2p3.fr/)
* Julien Browaeys - [Université de Paris](http://u-paris.fr) - [MSC laboratory](http://www.msc.univ-paris-diderot.fr/)
* Olivier Dadoun - [CNRS](http://cnrs.fr)/[in2p3](https://www.in2p3.cnrs.fr/) - [LPNHE laboratory](http://lpnhe.in2p3.fr/)

## Institutions
<div class="row">
    <img src="https://raw.githubusercontent.com/wiki/coa-project/pycoa/figs/logoCNRS.jpg" alt="CNRS" style="height:45px; padding: 5px;" />
    <img src="https://raw.githubusercontent.com/wiki/coa-project/pycoa/figs/Universite_Paris_logo_horizontal.jpg" alt="UParis" style="height:45px; padding: 5px;" />
    <img src="https://raw.githubusercontent.com/wiki/coa-project/pycoa/figs/logo_sorbonne_U.png" alt="SorbonneU" style="height:45px;" />
    <img src="https://raw.githubusercontent.com/wiki/coa-project/pycoa/figs/logo_LPNHE_web_bleu_2011.gif" alt="LPNHE" style="height:45px; padding: 5px;" />
    <img src="http://www.msc.univ-paris-diderot.fr/plugins/kitcnrs/images/logo_msc.jpg" alt="MSC" style="height:45px; padding: 5px;" />
</div>

***
[ⓒpycoa.fr <img src='https://raw.githubusercontent.com/wiki/coa-project/pycoa/figs/world-wide-web.png' height='25px' />](http://www.pycoa.fr) &nbsp;&nbsp;
[<img src='https://raw.githubusercontent.com/wiki/coa-project/pycoa/figs/email.png' height='25px' align='bottom' />](mailto:support@pycoa.fr) &nbsp;&nbsp;
[<img src='https://raw.githubusercontent.com/wiki/coa-project/pycoa/figs/twitter.png' height='25px' alt='Twitter'  />](https://twitter.com/pycoa_fr) &nbsp;&nbsp;
[<img src='https://raw.githubusercontent.com/wiki/coa-project/pycoa/figs/github.png' height='25px' alt='GitHub' />](https://github.com/coa-project/pycoa) &nbsp;&nbsp;
[<img src='https://raw.githubusercontent.com/wiki/coa-project/pycoa/figs/gitlab.png' height='25px' alt='GitLab' />](https://gitlab.in2p3.fr/lpnhe/pycoa) &nbsp;&nbsp;
[<img src='https://raw.githubusercontent.com/wiki/coa-project/pycoa/figs/information.png' height='25px' alt='User manual' />](https://github.com/coa-project/pycoa/wiki) &nbsp;&nbsp;
[<img src='https://raw.githubusercontent.com/wiki/coa-project/pycoa/figs/manual.png' height='25px' alt='Core documentation' />](https://www.pycoa.fr/doc) &nbsp;&nbsp;
[<img src='https://raw.githubusercontent.com/wiki/coa-project/pycoa/figs/mybinder.png' height='20px' alt='MyBinder launch' />](https://mybinder.org/v2/gh/coa-project/pycoa/dev)&nbsp;&nbsp;
[<img src='https://raw.githubusercontent.com/coa-project/coa-project.github.io/main/doc/pdoc.png' height='30px' alt='Documentation' />](http://pycoa.fr/doc/index.html)

***
### On parle de nous…
* Sur le site [MODCOV19](https://modcov19.math.cnrs.fr/) du [CNRS](https://www.cnrs.fr/) : Modélisation et Covid-19 [PyCoa : Python Covid analysis](https://modcov19.math.cnrs.fr/prepublications/2022_03_11_beau/)
* Dans le journal Acteurs Publics [L’héritage du “Hackathon Covid” passé à la loupe](https://www.acteurspublics.fr/articles/lheritage-du-hackathon-covid-passe-a-la-loupe)
* Dans les actualités du [LPNHE - Laboratoire de Physique Nucléaire et Hautes Énergies](https://lpnhe.in2p3.fr/) (juillet 2021) : [Pycoa, un logiciel pour mieux comprendre la pandémie due à la Covid-19 ](https://lpnhe.in2p3.fr/spip.php?article1596)
* Dans les actualités de [Sorbonne Université](https://www.sorbonne-universite.fr) (juillet 2021) : [PyCoa : un logiciel gratuit d’analyse des données de la Covid-19](https://www.sorbonne-universite.fr/actualites/pycoa-un-logiciel-gratuit-danalyse-des-donnees-de-la-covid-19)
* Dans les actualités de [l'UFR de physique de Université de Paris](https://physique.u-paris.fr) (juillet 2021) : [«Un logiciel pour mieux comprendre la pandémie»](https://physique.u-paris.fr/actualites/un-logiciel-pycoa-pour-mieux-comprendre-la-pandemie)
* Dans les actualités de [Université de Paris](http://u-paris.fr) (juin 2021) : [«Un logiciel pour mieux comprendre la pandémie»](https://u-paris.fr/un-logiciel-pour-mieux-comprendre-la-pandemie/)
* au [22ème salon culture et jeux mathématiques](https://salon-math.fr) (mai 2021) : [`https://salon-math.fr/2021/04/14/pycoa/`](https://salon-math.fr/2021/04/14/pycoa/)
* à l'[hackathon covid - lutter ensemble](https://hackathon-covid.fr) (avril 2021) : [`https://forum.hackathon-covid.fr/t/3a-pycoa-une-analyse-python-des-donnees-covid-pour-tous/251`](https://forum.hackathon-covid.fr/t/3a-pycoa-une-analyse-python-des-donnees-covid-pour-tous/251)
* à l'hackathon [Data Against Covid-19](https://ultrahack.org/covid-19datahack) (avril 2020) : [
