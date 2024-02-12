# HireHive Embed Options

![job postings api](https://raw.githubusercontent.com/hirehive/embed-options/master/images/iframe-job-listing-example.png)

## Introduction

This repository contains documentation and example for the HireHive Embed Option. 
This allows you to display a list of jobs from HireHive on your career page. Potential candidates can see your open roles and apply directly without leaving your site.
If you need any features which are missing or if you find any issues, please email us at
[support@hirehive.com](mailto:support@hirehive.com) or file an issue on this repository.

This is an advanced feature and requires some technical changes to your site.
It is recommended to proceed with this option if you have knowledge of the code running your site. 
All published job postings are also automatically viewable via
`{your sub domain}.hirehive.com`, for example
[AuthenticMedia.hirehive.com](https://AuthenticMedia.hirehive.com)

We also have an API for getting a list of your published jobs. If you wish to display the jobs on your site in a custom format then our API option might suit. [Read more information about our API](https://github.com/hirehive/jobs-api)

### This Option lets you:

- Display open job postings for your company
- Group your postings by `country` or `category`
- View an individual job posting 
- Apply to a job posting via the iframe

Note that all job postings in the `published` state are publically viewable.
These jobs may be scraped by third parties. All other jobs are completely
hidden from the jobs API.

###  Styling

The iframe has a default base styling which you may want to update to suit your company's branding.
Each company gets a dedicated playground page which lets you add your own custom `CSS` to the iframe.
The custom CSS will be injected in all pages in the iframe. ie. Job list, Application page and thanks page.

<img src="https://raw.githubusercontent.com/hirehive/embed-options/master/images/playground.png">

### Examples
[](#examples)

Default job listings

[<img src="https://raw.githubusercontent.com/hirehive/embed-options/master/images/no-grouping.png">](http://codepen.io/)

Job listings grouped by category

[<img src="https://raw.githubusercontent.com/hirehive/embed-options/master/images/category-grouping.png">](http://codepen.io/)

Job listings grouped by country

[<img src="https://raw.githubusercontent.com/hirehive/embed-options/master/images/country-grouping.png">](http://codepen.io/)

### Configuration Options

| Field             | Default Value | Description                   |
| ----------------- | ------------- | ----------------------------- |
| `grouping` | 'none' | Options: `country` or `category` 
| `target` | 'self' | Deprecated: The page url is now automatically updated using the window.history API
| `historyEnabled` | true | When the iframe changes page, the parent page url with automatically update to reflect the job that is being viewed. ?hh_jid will be added so you can share the link directly to a specific job
| `countryCode` | null |  Only display jobs from a certain Country: Two-letter country codes defined in ISO 3166-1. eg 'US', 'IE', 'CA',
| `category` | null | Only display jobs from a certain Category: 'tech', 'sales and marketing'
| `container`| null | CSS selector for the widget container. Use this if displaying multiple widgets in the same page. eg '.sales-jobs' , '#tech'


## Iframe resizing

The embedded iframe uses `window.postMessage` to update the height of the iframe automatically.
No configuration your site should be required for resizing to work.
