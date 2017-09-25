# TV-Shows-Web-Scraping-and-Modeling
Originally a project at General Assembly

## Summary of Findings

**Proposed Question and Sample:**

In an attempt to predict the next successful TV show, I built a model using intrinsic traits of a show to predict the show’s IMDB rating. While IMDB rating is not the only measure of a show’s success, a high score with a large voting sample is a good indicator of a popular show. Since TV is a rapidly changing medium, our sample is contained to shows that premiered since 2013. Since our company produces shows in the United State, our sample is also limited to shows with US origin. Finally, a show must have a minimum of 2500 ratings to be included in our sample to ensure we are only analyzing shows with a minimum threshold of popularity. 405 shows met the criteria listed above.

**Show Features and Assumptions:**

Using IMDB and TV Maze, we were able to retrieve information on the sample of shows. One of our primary goals for the model is to predict based on a show’s initial properties, not based on it’s achieved success. For example, we can’t know how many seasons a show will run during creation, therefore it would be inappropriate to use that information in our model. With that assumption in mind, our features include: show’s network or web channel, genre, members of the cast and crew, episode runtime, season length (by episodes), show type (scripted/reality/etc), premiere month and show summary. Show summary is the only feature that is not self-explanatory. Essentially, the show summary reads like an initial press release synopsis of the show.

**Target and Results:**

After reviewing the ratings, 404 (one outlier was removed) shows centered around a median rating of 7.5. Therefore the modeling goal was to predict whether a show would be above or below that threshold. After setting that marker, our shows broke down in 52% below and 48% above. Unfortunately, we were not able to produce a model that consistently predicted success. At our best, we were about to predict about 58% above our 52% baseline, however these results were fairly inconsistent. The results were equally unsuccessful when attempting to model elite shows rated 8.1 or above.

**Next Steps:**

Ultimately, our data was not able to determine the criteria for a successful show. However we have been provided some guidance toward further research that can be done to hopefully better accomplish the task.
* Cast and crew seemingly had little impact on the feature importance. While this can't be conclusive for future models, we should focus elsewhere.
* Summary was slightly more promising and there deeper analysis available to look for underlying patterns.
* If you expand the scope to more years, time series analysis might prove useful to see changes or trends over time.
* Are there fundamental differences between network and online hosted shows?
* Lastly, IMDB rating is only one proxy of success, perhaps other metrics would prove easier to predict.
