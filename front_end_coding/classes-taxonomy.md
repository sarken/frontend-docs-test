---
layout: page
title: Class Taxonomy
parent: Classes
---
# Class Taxonomy
{: .no_toc }

Concrete classes are used in the HTML; you can look at the code and find them used in `class` attributes on at least one page. Abstract classes never appear in the HTML, but influence how we group our styles either mentally or in the stylesheets.

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
* TOC
{:toc}
</details>

## Supertypes

There are four concrete supertype classes and one abstract supertype class.

* [.region](#region)
* [.group](#group)
* [.zone](#zone)
* [.actions](#actions)
* [.interactions](#interactions) (abstract)

### .region

* #header
* #dashboard
* #main
* #footer

### .group

* [.index](/patterns/indexes)
* [.listbox](/patterns/listbox)
* [.meta](/patterns/meta)
* [.blurb](/patterns/blurb)
* [.preface](/patterns/preface)
* [.comments](/patterns/comments)
* [.stats](/patterns/stats)

### .zone

* .system
  * .splash
  * .sessions
  * .docs
  * .feedbacks
  * .faq
  * .tos
  * .tos_faq
  * #tos_prompt
  * #proxy-notice
* .home
  * [objects](#object)
* .searchbrowse (abstract)
  * .filters
  * .search
* .tags
* .translation

### .actions

* .navigation
* .pagination
* .action

### .interactions

* .post (create or edit something, combine with .create)
* .search (find something)
* .destroy (delete a record)
* .manage (edit preferences, manage inbox)
* .filter (remove this in favor of .searchbrowse .filters)
* .review (tag set nominations)
* .update (tag edit)
* .widget (abstract)
  * .character_counter
  * .LV_* (live validation does not have an overarching class, but all of its classes begin with the prefix LV)
  * .autocomplete
  * .ui-sortable and .ui-draggable
  * .ui-datepicker and .ui-timepicker
  * .qtip (tooltips)
  * #modal
* .ajax (abstract)
  * .ajax-remove
  * .ajax-create-destroy

### Nulls

There are also these nulls, set in `types-groups.css`, which are .groups and #regions, but do not have patterns or a lot of layout. They can be useful for skins.

* .module
* .wrapper
* #outer
* #inner

## Types

We can divide types into two abstract classes:

* [object](#object)
* [data](#data)

### object

The abstract class `.object` encompasses classes that correspond with database records. These are typically a *type* of record that corresponds with a model name, such as `.work` or `.user`, but sometimes they're *specific* records, such as the `.rating-teen` class that correspondes with the [rating tag Teen and Up Audiences](https://archiveofourown.org/tags/Teen%20And%20Up%20Audiences).

* .user
* .work
  * .chapter
* .series
* .bookmark
  * .rec (a state [modifier](#modifiers) specific to bookmarks)
* .skin
* .tags
  * .tag
    * .freeform
    * .required-tags
      * .rating
        * .rating-general-audience
        * .rating-teen
        * .rating-mature
        * .rating-explicit
        * .rating-notrated
      * .category
        * .category-femslash
        * .category-gen
        * .category-het
        * .category-slash
        * .category-multi
        * .category-other
        * .category-none
      * .warnings
        * .warning-yes
        * .warning-no
        * .warning-choosenotto
        * .external-work (.warnings becomes an abstract)
      * .iswip (a state [modifier](#modifiers) presented as part of the `.required-tags` block in [blurbs](/patterns/blurb))
        * .complete-yes
        * .complete-no
* .tagset
  * .nomination
* .collection
  * .prompt
  * .item
  * .signup

### data

The abstract class `.data` encompasses classes that describe the type or format of the information it's applied to.

* .heading
* .title
* .byline
* .datetime
* .news
* .notes
* .footnote
* .summary
* .toc
* .faq
* .intro
* .count
* [.status](#modifiers)
* .notice
* .error
* .icon
* .symbol
  * .help
  * .question
* .alphabet
  * .letter
* .media
  * .medium

## Modifiers

Modifiers can be grouped into these abstract classes:

* roles
* states
* contexts
* abilities
* modes

Let's expand those abstracts and list the concrete classes we have in the codebase:

* roles
  * .wrangler
  * .translator
  * .user
  * .visitor
  * .admin
  * .participant also .member also .requester also pos .prompter \[IN REVIEW\]
  * .pinch-hitter
  * .mod
  * .owner
* states
  * [.current](/patterns/actions)
  * .hidden
  * .public
  * .private
  * .mystery
  * .important
  * .caution
  * .required
  * .latest (.recent on bookmarks)
  * .open
  * .closed
  * abstract "pending"
    * draft
    * preview
    * unreviewed
    * unread
    * unfulfilled
    * unwrangled
  * abstract "completed"
    * reviewed
    * read
    * replied
    * claimed
    * posted
  * abstract "relationship"
    * .child
    * .parent
    * .synonym
    * .meta (tag)
    * .canonical
    * .own
* contexts
  * .dashboard
  * .primary
  * .secondary
  * .tertiary
  * .start
  * .end
* abilities (interactions)
  * .draggable
  * .droppable
  * .sortable
  * .dynamic
  * .expandable
* modes (interactions)
  * .single
  * .simple
  * .verbose

## Travellers

Index is the most used example of the polyvalent "types or states of groups"

    * .index
    * .tree
    * .cloud

    * * *
