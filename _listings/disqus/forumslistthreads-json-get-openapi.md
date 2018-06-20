---
swagger: "2.0"
x-collection-name: Disqus
x-complete: 0
info:
  title: Disqus Forums ListThreads
  description: Forums ListThreads
  termsOfService: https://docs.disqus.com/kb/terms-and-policies/
  version: 1.0.0
host: disqus.com
basePath: api/3.0/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /forumCategories/list.json:
    get:
      summary: ForumCategories List
      description: ForumCategories List
      operationId: forumcategories-list
      x-api-path-slug: forumcategorieslist-json-get
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Categories
      - Forums
  /forums/create.json:
    post:
      summary: Forums Create
      description: Forums Create
      operationId: forums-create
      x-api-path-slug: forumscreate-json-post
      parameters:
      - in: query
        name: adultContent
        description: Defaults to false
        type: string
      - in: query
        name: attach
        description: 'Defaults to []                         Choices: followsForum,
          forumCanDisableAds, forumForumCategory, counters, forumDaysAlive, forumFeatures,
          forumIntegration, forumNewPolicy, forumPermissions'
        type: string
      - in: query
        name: category
        description: 'Defaults to null                         Choices: Tech, Living,
          Style, Business, Entertainment, Celebrity, Sports, Culture, Games, News'
        type: string
      - in: query
        name: commentPolicyLink
        description: Defaults to null                         URL (defined by RFC
          3986)
        type: string
      - in: query
        name: commentPolicyText
        description: Defaults to null
        type: string
      - in: query
        name: description
        description: Defaults to null                         Maximum length of 300
        type: string
      - in: query
        name: forumCategory
        description: Defaults to null                         Looks up a forum category
          by ID
        type: string
      - in: query
        name: guidelines
        description: Defaults to null
        type: string
      - in: query
        name: language
        description: Defaults to en                         Translation Language
        type: string
      - in: query
        name: name
        type: string
      - in: query
        name: short_name
        type: string
      - in: query
        name: website
        description: Defaults to null                         URL (defined by RFC
          3986)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
  /forums/details.json:
    get:
      summary: Forums Details
      description: Forums Details
      operationId: forums-details
      x-api-path-slug: forumsdetails-json-get
      parameters:
      - in: query
        name: attach
        description: 'Defaults to []                         Choices: followsForum,
          forumCanDisableAds, forumForumCategory, counters, forumDaysAlive, forumFeatures,
          forumIntegration, forumNewPolicy, forumPermissions'
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
  /forums/disableAds.json:
    post:
      summary: Forums DisableAds
      description: Forums DisableAds
      operationId: forums-disableads
      x-api-path-slug: forumsdisableads-json-post
      parameters:
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name) You must be a moderator
          on the selected forum
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
      - Advertising
  /forums/fixFavIconsForClassifiedForums.json:
    get:
      summary: Forums FixFavIconsForClassifiedForums
      description: Forums FixFavIconsForClassifiedForums
      operationId: forums-fixfaviconsforclassifiedforums
      x-api-path-slug: forumsfixfaviconsforclassifiedforums-json-get
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
  /forums/follow.json:
    post:
      summary: Forums Follow
      description: Forums Follow
      operationId: forums-follow
      x-api-path-slug: forumsfollow-json-post
      parameters:
      - in: query
        name: target
        description: Looks up a forum by ID (aka short name)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
  /forums/generateInterestingContent.json:
    get:
      summary: Forums GenerateInterestingContent
      description: Forums GenerateInterestingContent
      operationId: forums-generateinterestingcontent
      x-api-path-slug: forumsgenerateinterestingcontent-json-get
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
  /forums/interestingForums.json:
    get:
      summary: Forums InterestingForums
      description: Forums InterestingForums
      operationId: forums-interestingforums
      x-api-path-slug: forumsinterestingforums-json-get
      parameters:
      - in: query
        name: limit
        description: Defaults to 5                         Maximum value of 100
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
  /forums/listThreads.json:
    get:
      summary: Forums ListThreads
      description: Forums ListThreads
      operationId: forums-listthreads
      x-api-path-slug: forumslistthreads-json-get
      parameters:
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: include
        description: 'Defaults to [  open,  closed]                         Choices:
          open, closed, killed'
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: order
        description: 'Defaults to desc                         Choices: asc, desc'
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      - in: query
        name: since
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      - in: query
        name: thread
        description: Defaults to null                         Looks up a thread by
          ID You may pass us the &#39;ident&#39; query type instead of an ID by including
          &#39;forum&#39;
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
      - Lists
x-streamrank:
  polling_total_time_average: "0.32"
  polling_size_download_average: "24075.83"
  streaming_total_time_average: "0.17"
  streaming_size_download_average: "12039.41"
  change_yes: "381"
  change_no: "830"
  time_percentage: "48"
  size_percentage: "50"
  change_percentage: "31"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---