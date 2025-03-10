---
title: GitHub Discussions Documentation
beta_product: true
shortTitle: GitHub Discussions
intro: '{% data variables.product.prodname_discussions %} is a collaborative communication forum for the community around an open source project. Community members can ask and answer questions, share updates, have open-ended conversations, and follow along on decisions affecting the community''s way of working.'
introLinks:
  quickstart: /discussions/quickstart
featuredLinks:
  guides:
    - /discussions/collaborating-with-your-community-using-discussions/about-discussions
    - /discussions/collaborating-with-your-community-using-discussions/participating-in-a-discussion
    - /discussions/managing-discussions-for-your-community/moderating-discussions
  gettingStarted:
    - /discussions/quickstart
  guideCards:
    - /discussions/collaborating-with-your-community-using-discussions/about-discussions
    - /discussions/collaborating-with-your-community-using-discussions/participating-in-a-discussion
    - /discussions/managing-discussions-for-your-community/moderating-discussions
  popular:
    - /discussions/guides/granting-higher-permissions-to-top-contributors
    - /discussions/guides/best-practices-for-community-conversations-on-github
    - /discussions/guides/finding-discussions-across-multiple-repositories
    - /discussions/collaborating-with-your-community-using-discussions/collaborating-with-maintainers-using-discussions
    - /discussions/managing-discussions-for-your-community/managing-categories-for-discussions-in-your-repository
changelog:
  label: 'discussions'
product_video: https://www.youtube-nocookie.com/embed/IpBw2SJkFyk
layout: product-landing
versions:
  free-pro-team: '*'
---

<!-- {% link_with_intro /quickstart %} -->
<!-- {% link_with_intro /discussions-guides %} -->
<!-- {% link_with_intro /collaborating-with-your-community-using-discussions %} -->
<!-- {% link_with_intro /managing-discussions-for-your-community %} -->

<!-- Community examples -->
{% assign discussionsCommunityExamples = site.data.variables.discussions_community_examples %}
{% if discussionsCommunityExamples %}
<div class="my-6 pt-6">
  <h2 class="mb-2 font-mktg h1">Communities using discussions</h2>

  <div class="d-flex flex-wrap gutter">
    {% render discussions-community-card for discussionsCommunityExamples as example %}
  </div>
  {% if discussionsCommunityExamples.length > 6 %}
    <button class="js-filter-card-show-more btn btn-outline float-right" data-js-filter-card-max="6">Show more {% octicon "arrow-right" %}</button>
  {% endif %}
  <div class="js-filter-card-no-results d-none py-4 text-center color-text-secondary font-mktg">
    <div class="mb-3">{% octicon "search" width="24" %}</div>
    <h3 class="text-normal">Sorry, there is no result for <strong class="js-filter-card-value"></strong></h3>
    <p class="my-3 f4">It looks like we don't have an example that fits your filter.<br>Try another filter or add your code example</p>
    <a href="https://github.com/github/docs/blob/main/data/variables/discussions_community_examples.yml">Add your community {% octicon "arrow-right" %}</a>
  </div>
</div>
{% endif %}
