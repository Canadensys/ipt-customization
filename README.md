ipt-customizations
==================

Customize the [Global Biodiversity Information Facility](http://www.gbif.org)'s [Integrated Publishing Toolkit (IPT)](https://github.com/gbif/ipt/releases/tag/ipt-2.3.2) v. 2.3.2 with alternative freemarker, css, and js. A similar set of customized files was produced for IPT v.2.1.1, v. 2.0.5 and v. 2.0.3 and are available from [previous releases](https://github.com/Canadensys/ipt-customization/releases/).

This patch is specific to IPT 2.3.2 and the [Canadensys IPT](http://data.canadensys.net/ipt/) install. It is provided here to illustrate how the Canadensys team coordinates its IPT customization and for its version control.

Copy canadensys_ipt_2.3.2.patch into the Tomcat directory for your IPT (i.e. where you have its META-INF, WEB-INF, images, js, and styles directories). Ensure that git has been initialized for this directory and all files added and committed to its git index, then execute instructions from [https://ariejan.net/2009/10/26/how-to-create-and-apply-a-patch-with-git/](https://ariejan.net/2009/10/26/how-to-create-and-apply-a-patch-with-git/).

This patch was made by David P. Shorthouse.

See LICENSE.
