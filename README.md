ipt-customizations
==================

Customize the [Global Biodiversity Information Facility](http://www.gbif.org)'s [Integrated Publishing Toolkit (IPT)](https://github.com/gbif/ipt/releases/tag/ipt-2.3.5) v. 2.3.5 with alternative freemarker, css, and js. A similar set of customized files was produced for IPT v.2.3.2, v.2.1.1, v. 2.0.5 and v. 2.0.3 and are available from [previous releases](https://github.com/Canadensys/ipt-customization/releases/).

This patch is specific to IPT 2.3.5 and the [Canadensys IPT](http://data.canadensys.net/ipt/) install. It is provided here to illustrate how the Canadensys team coordinates its IPT customization and for its version control.

Copy canadensys_ipt_2.3.5.patch into the Tomcat directory for your IPT (i.e. where you have its META-INF, WEB-INF, images, js, and styles directories). Ensure that git has been initialized for this directory and all files added and committed to its git index, then execute instructions from [https://ariejan.net/2009/10/26/how-to-create-and-apply-a-patch-with-git/](https://ariejan.net/2009/10/26/how-to-create-and-apply-a-patch-with-git/).

Resume steps to create:

0. ``$ git clone https://github.com/gbif/ipt.git``
1. ``$ cd ipt``
2. Create a branch: ``$ git checkout -b canadensys_ipt_x.x.x``
3. Create your modifications and commit them on the new branch
4. Create your patch: ``$ git format-patch master --stdout > canadensys_ipt_x.x.x.patch``

Resume steps to apply:

0. Go to your ipt deployed website then initiate a git repository: ``# git init``
1. Create first commit: ``# git add -A && git commit -m "IPT first commit"``
2. ``# git apply --stat canadensys_ipt_x.x.x.patch``
3. ``# git apply --check canadensys_ipt_x.x.x.patch``
4. Apply the patch``# git am --signoff < fix_empty_poster.patch``

(Thanks to ARIEJAN DE VROOM)

All images, css, or JS are now on [Canadensys Layout common](https://github.com/Canadensys/canadensys-layout)

This patch was made by following David P. Shorthouse recommendations.

See LICENSE.
