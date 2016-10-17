---
title: Ember.js 2.8-LTS, 2.9 Stable, and 2.10 Beta Released
author: Matthew Beale
tags: Releases
---

Today, the Ember core team is happy to announce three new Ember.js releases.

* Ember.js 2.8-LTS, a long-term support release that will receive critical
  bugfixes for the next 6 release cycles (until roughly June 2017) and security
  patches for the next 10 release cycles (until roughly February 2018).
* Ember.js 2.9, a stable minor release suitable for production. This branch contains
  the same rendering engine as Ember 2.8.
* Ember.js 2.10-beta, the branch of Ember.js that will become stable in six
  weeks. This branch includes the new Glimmer2 rendering engine.

## Ember.js 2.8-LTS

2.8-LTS marks the second long-term support release of Ember.js. The designation
of this LTS release comes six weeks after 2.8.0 was released, ensuring the
2.8.2 has already been adopted in production by many apps for real-world
testing. We
encourage users on the previous LTS (2.4) to begin the upgrade process if they
haven't already.

For applications that have removed their use of legacy 1.x
`View`, `ArrayController`, and `ObjectController` APIs the upgrade process
is expected to be straightforward. Applications still using those APIs via the
[ember-legacy-views](https://github.com/emberjs/ember-legacy-views) or
[ember-legacy-controllers](https://github.com/emberjs/ember-legacy-controllers)
addons will need to refactor away from those deprecated addons before they can
upgrade. See the
[1.13 deprecation
guide](http://emberjs.com/deprecations/v1.x/#toc_deprecations-added-in-1-13)
for migration strategies away from legacy controller and view APIs.

For a full list of features that were introduced with Ember.js 2.8, [see the
2.8 stable release post](http://emberjs.com/blog/2016/09/08/ember-2-8-and-2-9-beta-released.html#toc_ember-js-2-8).

For more details on changes in Ember 2.8 since 2.8.0 was released, review the
[Ember.js 2.8.2 CHANGELOG](https://github.com/emberjs/ember.js/blob/v2.8.2/CHANGELOG.md).

## Ember.js 2.9

Initial releases of Ember.js 2.9-beta ([announced in
September](http://emberjs.com/blog/2016/09/08/ember-2-8-and-2-9-beta-released.html#toc_ember-js-2-9-beta))
included the new Glimmer2 rendering engine. Although the late betas with
Glimmer2 were considered quite stable and backwards compatible (several
apps are using them in production), we uncovered several minor
incompatibilities with earlier 2.x releases late in the beta process. **To ensure
the upgrade path to Glimmer2 is as smooth as possible for all users, 2.9 stable
is shipping today with the same rendering engine as earlier 2.x releases.**
Ember.js 2.10 beta releases include the Glimmer2 rendering engine, and we look
forward to addressing the few known issues in the next six-week cycle.

Because of the late decision to defer Glimmer2 into Ember.js 2.10, 2.9 is
basically a fork of the 2.8 stable branch. There are no new features or
deprecations over those in 2.8.2.

For more details on changes landing in 2.9 stable, review the
[Ember.js 2.9.0 CHANGELOG](https://github.com/emberjs/ember.js/blob/v2.9.0/CHANGELOG.md).

## Ember.js 2.10 beta

Ember.js 2.10 beta is released today, and continues to focus on integration
of the Glimmer2 rendering engine into Ember. Our focus is to resolve several
minor compatibility issues raised during the integration effort:

* [emberjs/ember.js#14413](https://github.com/emberjs/ember.js/issues/14413) - Block params
  should always "win" during property value lookup.
* [emberjs/ember.js#14401](https://github.com/emberjs/ember.js/issues/14351) - Class-based
  helpers can trigger "infinite loop" error when using `recompute`.
* [emberjs/ember.js#14339](https://github.com/emberjs/ember.js/issues/14335) - Closure actions
  cause excessively expensive re-renders.
* [emberjs/ember.js#14326](https://github.com/emberjs/ember.js/issues/14326) - Change in
  behavior of the `{{#with}}` helper when `null` or `undefined` is a value
  in a property chain.
* [emberjs/ember.js#14293](https://github.com/emberjs/ember.js/pull/14293) - Change in when
  warnings are raised for bindings to `style`.
* [tildeio/glimmer#334](https://github.com/tildeio/glimmer/pull/334) - Improve
  Glimmer2 support for
  [ember-wormhole](https://github.com/yapplabs/ember-wormhole) and
  [flexi](https://github.com/html-next/flexi).

For more details on changes landing in 2.10 beta, review the
[Ember.js 2.10.0-beta.1 CHANGELOG](https://github.com/emberjs/ember.js/blob/v2.10.0-beta.1/CHANGELOG.md).
