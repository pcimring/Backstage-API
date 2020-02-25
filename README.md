# Backstage-API

## DEPRECATION NOTICE - FEBRUARY 25, 2020

The *documentation* in this Git Repo has been *retired*.

Going forward, please use the docs available *online*: https://developers.taboola.com/backstage-api/reference

## Table of Contents
1. [Authentication and General API Usage](#1-authentication-and-general-api-usage)
2. [Campaign Items](#2-campaign-items)
3. [Campaigns](#3-campaigns)
4. [Dictionary](#4-dictionary)
5. [Errors](#5-errors)
6. [Reports](#6-reports)
7. [Targeting](#7-targeting)
8. [Users](#8-users)
9. [API Libraries](#9-api-libraries)



## 1. Authentication and General API Usage
Taboola uses [OAuth2](https://oauth.net/2/) for authentication.
The idea is simple - request an Access Token from the Authorization Server, then attach the obtained Access Token as an HTTP header when making requests to the API.
All requests to the API must include an Authorization HTTP header, with its value containing the retrieved Access Token.

There are four possible ways to retrieve an Access Token, all detailed in the document.



## 2. Campaign Items
Relevant only for advertisers.


The following operations are available via the API:
1. Fetch a List of Items for a specific Campaign.
2. Fetch a Single Item from a Campaign.
3. Create a new Item in a specific Campaign.
4. Update an existing Item.
5. Delete (Stop) an Item.
6. Fetch Children Items of an RSS Item
7. Fetch a specific Child Item of an RSS Item
8. Update a child of an RSS Item



## 3. Campaigns
Relevant only for advertisers.


The following operations are available via the API:
1. Fetch a List of Campaigns.
2. Fetch a Single Campaign.
3. Create a Campaign.
4. Update a Campaign.

## 4. Dictionary
The dictionary allows to get from Taboola lists of possible values and their meaning in various contexts (enum’s and their relevant codes). This is used in order to get predefined allowed values to be selected by the user. 

For example, if the user would like to target specific countries, the dictionary will allow to get the possible country values supported in Taboola and display them as selectable options to the user.

The following dictionaries are available via the API:
1. **Generic dictionaries:**
  * Get a list of dictionaries.
  * Get a list of supported countries and regions.
  * Get a list of supported platforms.
2. **Resource specific dictionaries:**
  * Get a list of possible enum values that relate to campaigns.
  * Get a list of possible enum values that relate to items.

## 5. Errors
The Backstage API returns errors in a JSON format. The response body will contain an object with several fields, and the HTTP status will be set appropriately.
This document details the different errors you can get and their meanings.

## 6. Reports
The document details the different reports you can pull using the API, including supported dimensions and filters.

**Advertiser reports available through the API:**
* **Campaign Summary** - This report provides general campaign metrics such as impressions, clicks, conversions, spend, as well as performance metrics such as CTR, CPC, CPM, CPA. The report can be broken down by date, campaign, referring site, country or platform.
* **Top Campaign Content** - This report lists the top 500 Items of a Campaign. The report allows fetching the top 500 Items for all Campaigns of an Account, or filter the results to include only the Items of a specific Campaign.

**Publisher reports available through the API:**
* **Revenue Summary** - This report provides general revenue information, as well as revenue performance statistics such as RPM, CPC and CTR. This report allows breaking down revenue performance metrics by site, page type, placement, platform and country.
* **Visit Value** - This report provides revenue and engagement metrics for an entire visit, allowing to deduce the value of a visitor. This report allows breaking down that value by referral source, visit landing page, platform and country.
* **Recirculation Summary** - This report provides organic content performance information such as Page Views and CTR.  This report allows breaking down organic (recirculation) performance metrics by date, page type, publisher, country and platform.

## 7. Targeting
Targeting   your   campaigns   to   the   right   segment   helps   you   get   the   most   out   of   your campaigns.   In   the   following   document   you   will   find   information   regarding   the   targeting abilities   supported   by   the   API.
The   supported   targeting   options   are:
1. Geo  Targeting  -  You  can  target  specific  geographic  areas  -  like  countries  or
regions   within   a   specific   country.   You   can   also   target   more   granularly   -   by   postal code.   For   example,   you   can   run   your   local   store   campaigns   only   in   places   you have   physical   stores,   helping   you   spend   your   budget   wisely   and   attract   relevant customers.
2. Platform  Targeting  (include  only)  -  You  can  choose  on  which  devices  your campaign   items   will   appear.   Platform   targeting   can   be   useful   if   you   have   different product   or   service   offerings   for   users   that   browse   from   different   platforms.   For example,   if   you’re   offering   a   mobile   app,   it   would   make   sense   to   target   mobile devices   only.
3. Publisher  Targeting  (exclude  only)  -  You  can  block  specific  publishers  from serving   your   campaign.

## 8. Users
The API enables you to fetch a list of the user's allowed Accounts.

## 9. API Libraries

1. [Java Library](https://github.com/taboola/backstage-api-java-client)
