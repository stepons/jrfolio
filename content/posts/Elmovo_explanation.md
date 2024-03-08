---
title: "Electric delivery moped rentals"
date: 2023-05-02T16:58:25+01:00
draft: false
---

### Abstract

An analysis of the performance of electric delivery mopeds and how the battery life affects rider behaviour. The data is from the company Elmovo that operated in London in 2019-20.

Rental duration and distance are plotted by rental location and the results analysed in the context of the different geographies around the rental stations. 

Then rental start times are plotted by days of the week to show the demand patterns for the service and corresponding utilisation of the mopeds.

It is clear that battery life limits the duration of the 6-hour rentals and booking patterns further suggest that rentals of longer than 6-hours would be desirable.

### Rider choices dictated by battery capacity

I was co-founder of a gig-economy focused electric moped rental service, the USP of which was to match bike rentals to the times the riders work, whether that was every day or just once or twice a week. Riders could book and pick up a bike from one of our locations, do a shift and return the bike.

The main constraint on the service was the range of the bikes and therefore, how long a rider could use the bike before running out of charge. We estimated that the batteries should last 6 hours including time waiting for deliveries and set standard rental length to that. We subsequently introduced 3-hour rentals based on rider feedback.

{{< gist stepons 9b52946639af905e3dd0f4ba9e0e7513 >}}

We had complaints that bikes did not last the full 6-hour rental period – and this is evident from the box plots for the four branches. 

![targets](/img/el_fig1.png)

The 75th percentile at all locations is below the 6-hour mark and the medians are closer to, and in one case below, 5 hours. With 3-hour rentals the 75th percentiles are at or above 3 hours and the distributions are also negatively skewed, meaning that a greater proportion of rentals finished at, or close to, the 3-hour period. The pattern is likely to have been similar for the 6-hour rentals without the battery range issue. Cambridge Heath Road (CHR) shows some of the longest rentals for both 3 and 6-hour sessions which is due to the area being quieter for food deliveries resulting in riders spending more time waiting.

The Swiss Cottage (SC) location fared worse than the the others on 6-hour rentals finishing early and there is one principal reason for this: the branch was based at a Deliveroo kitchen which closed at 11pm when a gate was locked, so there was a hard cut-off for bikes to be returned whatever the rental start time. 

We had also thought that it might be because the site served Hampstead, which meant a lot of hills that drained the batteries more quickly. However looking at the distance covered during rentals tells a different story.

![targets](/img/el_fig2.png)

The interquartile range shows Swiss Cottage to have the greatest distances for the majority of rentals. The reason for this is two-fold: there was charging available for the mopeds which the riders could use while they were waiting for the next delivery, so the hills caused no reduction in overall range – and also they could fit more deliveries into the shorter rental period because the bikes were stored at the busy kitchen, meaning reduced waiting times for pickups.

Comparing the other 2 locations we have distance data for, Devonshire Row Mews (DRM) had longer rental durations than Wandsworth Road (WR), however the distance covered during rentals was greater at WR. This is due to the geography of the 2 locations. DRM is in W1, just south of Regent’s Park, in a dense urban area. WR is more suburban, with riders reporting having had to ride several miles to some delivery locations.

A note on the number of outliers. There are a large number at the shorter time-scales as we had some technical issues which meant that we had to manually end rentals and restart them with a new moped and there were booking mistakes by riders that had to be corrected. There are a greater number at DRM as that was by far the most popular location with the greatest number of rentals overall. Rentals below an hour long have been removed from the dataset as they do not reflect the performance of the mopeds.

Looking at a violin plot of all rentals by start time, the evening peak is very pronounced, as is the preference for 6-hour rentals. The peak for 3-hour rentals is later than for 6-hour rentals, which suggests the 3-hour sessions were being used to keep working later in the evening after a 6-hour rental, which reinforces that riders would like to rent for longer work shifts than the batteries allow. What is clear is that the mopeds are underutilised outside mealtimes. The plan had been to increase utilisation rates by renting to non-food couriers during the working day when rental rates were lower, however the onset of the pandemic stopped progress at an early stage.

![targets](/img/el_fig3a_.png)

The hard cut-off of the plots of some days at the end of the evening are cause by the start time data being saved by hour only and not minutes. Therefore on quieter days like Monday and Wednesday there are no rentals past 9pm and all rentals during the previous hour are given a start time of 8pm exactly.

The pattern of rental start times has to be looked at in combination with the average daily numbers of rentals at each hour which shows just how popular the early evening 6-hour rentals are and the differential in demand overall between the two durations.

![targets](/img/el_fig3b_.png)