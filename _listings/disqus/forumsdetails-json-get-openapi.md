---
swagger: "2.0"
x-collection-name: Disqus
x-complete: 0
info:
  title: Disqus Forums Details
  description: Forums Details
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
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---