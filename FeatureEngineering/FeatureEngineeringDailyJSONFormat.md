**Feature Engineering Daily JSON Format**
==============================

### Overview
--------

This document provides a detailed explanation of the JSON format used in the daily data cleaning process. It includes information on the columns, their data types, and the structure of the dataset.

### Structure of the JSON
---------------------

The JSON consists of an array of objects, where each object represents a specific video along with its associated channel data. Below is a breakdown of the individual columns and their descriptions:

### Columns

| Column Name | Description | Data Type |
| --- | --- | --- |
| `channelId` | Unique identifier for the channel | String |
| `channelName` | Name of the YouTube channel | String |
| `videoId` | Unique identifier for the video | String |
| `videoTitle` | Title of the video | String |
| `videoPublishYear` | Year when the video was published | Integer |
| `videoPublishMonth` | Month when the video was published | Integer |
| `videoPublishDay` | Day when the video was published | Integer |
| `videoPublishTime` | Time when the video was published (in HH:MM:SS format) | String |
| `videoPublishedOn` | Full timestamp of when the video was published (ISO 8601 format) | String |
| `videoPublishedOnInSeconds` | Timestamp in seconds when the video was published | Integer |
| `videoViewCount` | Total number of views on the video | Integer |
| `videoLikeCount` | Total number of likes on the video | Integer |
| `videoCommentCount` | Total number of comments on the video | Integer |
| `videoCategoryId` | Identifier for the video’s category (e.g., 27 for Education) | Integer |
| `videoDefaultAudioLanguage` | Default language for the video audio (e.g., 'en' for English) | String |
| `videoDuration` | Duration of the video in ISO 8601 format (e.g., PT2H46M15S) | String |
| `videoDurationInSeconds` | Duration of the video in seconds | Integer |
| `videoContentType` | Type of content in the video (e.g., 'Video') | String |
| `videoDimension` | Video dimension type (e.g., '2d') | String |
| `videoDefinition` | Video quality (e.g., 'hd') | String |
| `videoCaption` | Indicates if the video has captions (e.g., 'true') | Boolean |
| `videoLicensedContent` | Indicates if the video has licensed content (e.g., 'true') | Boolean |
| `videoProjection` | The projection type of the video (e.g., 'rectangular') | String |
| `channelCustomUrl` | Custom URL for the channel | String |
| `channelPublishYear` | Year when the channel was published | Integer |
| `channelPublishMonth` | Month when the channel was published | Integer |
| `channelPublishDay` | Day when the channel was published | Integer |
| `channelPublishTime` | Time when the channel was published (in HH:MM:SS format) | String |
| `channelPublishedOn` | Full timestamp of when the channel was published (ISO 8601 format) | String |
| `channelPublishedOnInSeconds` | Timestamp in seconds when the channel was published | Integer |
| `channelCountry` | Country of origin for the channel | String |
| `channelViewCount` | Total number of views across the channel | Integer |
| `channelSubscriberCount` | Total number of subscribers for the channel | Integer |
| `channelVideoCount` | Total number of videos uploaded to the channel | Integer |
| `videoPublishedWeekDay` | Day of the week when the video was published (e.g., 'Wednesday') | String |
| `videoDurationClassification` | Classification of the video’s duration (e.g., 'Extended') | String |
| `channelAgeInYears` | Age of the channel in years (calculated based on `channelPublishedOn`) | Float |
| `channelNormalizedViewCount` | Normalized value of the channel view count | Float |
| `channelNormalizedSubscriberCount` | Normalized value of the channel subscriber count | Float |
| `channelNormalizedVideoCount` | Normalized value of the channel video count | Float |
| `channelNormalizedChannelAge` | Normalized value of the channel's age in years | Float |
| `channelGrowthScore` | A score representing the growth of the channel based on multiple factors | Float |
| `videoAgeInDays` | Age of the video in days (calculated based on `videoPublishedOn`) | Float |
| `videoViewsPerDay` | Average number of views per day for the video | Float |
| `videoLikeToViewRatio` | Ratio of likes to views for the video | Float |
| `videoCommentToViewRatio` | Ratio of comments to views for the video | Float |
| `videoEngagementScore` | A score representing the engagement of the video | Float |
| `channelGrowthScoreRank` | Rank of the channel based on the growth score | Float |
| `videoEngagementScoreRank` | Rank of the video based on the engagement score | Float |
| `country_code` | Country code for the channel’s country | String |
| `country_name` | Full country name for the channel’s country | String |
| `continent` | Continent where the channel’s country is located | String |
| `continent_code` | Continent code (e.g., 'EU' for Europe) | String |
| `it_hub_country` | Indicator if the country is considered a major IT hub (e.g., 'Yes' or 'No') | String |

### Data Types
----------

The following are the main data types used in this dataset:

- **String**: Textual data (e.g., `channelId`, `channelName`, `videoTitle`).
- **Integer**: Whole numbers (e.g., `videoViewCount`, `channelSubscriberCount`).
- **Float**: Decimal numbers (e.g., `channelAgeInYears`, `channelGrowthScore`).
- **Boolean**: True/False values (e.g., `videoCaption`, `videoLicensedContent`).
- **DateTime (String)**: Timestamp data in ISO 8601 format (e.g., `videoPublishedOn`, `channelPublishedOn`).

### Example JSON Object
-------------------

Below is an example of the JSON structure for one record:

```json
{
  "channelId": "UCdngmbVKX1Tgre699-XLlUA",
  "channelName": "TechWorld with Nana",
  "videoId": "3c-iBn73dDE",
  "videoTitle": "Docker Tutorial for Beginners [FULL COURSE in 3 Hours]",
  "videoPublishYear": 2020,
  "videoPublishMonth": 10,
  "videoPublishDay": 21,
  "videoPublishTime": "19:26:53",
  "videoPublishedOn": "2020-10-21T19:26:53Z",
  "videoPublishedOnInSeconds": 1603308413,
  "videoViewCount": 5486402,
  "videoLikeCount": 93213,
  "videoCommentCount": 4545,
  "videoCategoryId": 27,
  "videoDefaultAudioLanguage": "en",
  "videoDuration": "PT2H46M15S",
  "videoDurationInSeconds": 9975,
  "videoContentType": "Video",
  "videoDimension": "2d",
  "videoDefinition": "hd",
  "videoCaption": true,
  "videoLicensedContent": true,
  "videoProjection": "rectangular",
  "channelCustomUrl": "@techworldwithnana",
  "channelPublishYear": 2019,
  "channelPublishMonth": 10,
  "channelPublishDay": 6,
  "channelPublishTime": "08:50:17",
  "channelPublishedOn": "2019-10-06T08:50:17Z",
  "channelPublishedOnInSeconds": 1570351817,
  "channelCountry": "AT",
  "channelViewCount": 64400244,
  "channelSubscriberCount": 1200000,
  "channelVideoCount": 126,
  "videoPublishedWeekDay": "Wednesday",
  "videoDurationClassification": "Extended",
  "channelAgeInYears": 5.34,
  "channelNormalizedViewCount": 0.0776,
  "channelNormalizedSubscriberCount": 0.1043,
  "channelNormalizedVideoCount": 0.0071,
  "channelNormalizedChannelAge": 0.2533,
  "channelGrowthScore": 0.2824,
  "videoAgeInDays": 1567.28,
  "videoViewsPerDay": 3500.59,
  "videoLikeToViewRatio": 0.017,
  "videoCommentToViewRatio": 0.00083,
  "videoEngagementScore": 1750.82,
  "channelGrowthScoreRank": 355.0,
  "videoEngagementScoreRank": 411.0,
  "country_code": "AT",
  "country_name": "Austria",
  "continent": "Europe",
  "continent_code": "EU",
  "it_hub_country": "No"
}
```
