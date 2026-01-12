### INTRODUCTION 
Climate plays a pivotal role in shaping terrestrial ecosystems on both regional and global scales ([Delire et al. 2011]), with the intricate nature of vegetation cover serving as a vivid reflection of the fragility and instability inherent in these ecosystems ([De Graff 2018]). Notably, in East Africa, the economy relies heavily on the exploitation of natural resources, contributing directly to the observed abnormal changes in climate ([Huq & Reid 2005]). In contemporary research, satellite sensors have evolved into indispensable tools for investigating vegetation dynamics and trends at a regional to global scale ([Ssemmanda et al. 2014]; [Cao et al. 2018]). Notable works have been done to deepen into the relations of vegetation and its environment ([Walther et al. 2002]; [Zhou et al. 2014]). [Plisnier et al.] delved into the intricate web of tele-connections between El Niño Southern Oscillation (ENSO) and ecosystems, utilizing NDVI and ENSO indices, and climate data (2020). Their findings validated the considerable influence of ENSO on climate and ecological fluctuations. Examining the NDVI anomaly in East (South) Africa from 1997 to 2000 revealed a significant reversal associated with precipitation patterns, indicating a transition from El Niño to La Niña conditions. [Landmann & Dubovyk] integrated NDVI data with rainfall records from the Tropical Rainfall Measuring Mission covering the period of 2001–2011 in East Africa (2014). Their results uncovered declining yields attributed to both vegetation degradation and human-induced alterations to the land. Given the current state of research in the region of interest, the aim of this study is to describe climatological patterns of cloud coverage for a long-term period and to assess the impact of the cloud coverage values over regional NDVI values.

### AREA STUDY AND DATA 
The Juba-Shabelle basin is places between the Ethiopian highlands at an altitude of about 4 230 m a.s.l. and the Mount Kenya (5 195 m a.s.l.). The total catchment area is 796 600 Km2. The Shabelle river joins the Juba River when rain is exceptional, otherwise it ends in Somalian sand depression areas. The average annual rainfall in the mountains is 1 500-1 600 mm and 200 mm downstream ([Abdullahy, 2013]). 
We have used the NOAA Climate Data Record (CDR) of AVHRR Normalized Difference Vegetation Index (NDVI) Version 5 and VIIRS Normalized Difference Vegetation Index (NDVI) Version 1 at a spatial resolution of 0.05° and a daily temporal resolution. The datasets were retrieved from https://noaa-cdr-ndvi-pds.s3.amazonaws.com/index.html#data/ from 1991 to 2020 to illustrate a long-record climatology. In the dataset of the NDVI products, from the two sensors, there are two main variables that we used for the purpose of the work: NDVI and QA, where QA is the variable that indicates if the NDVI values for each grid-point have a technical noise or if it is affected by the clouds or their shadows. The NDVI is used to monitor the changes in vegetation coverage, and its values range from -1.0 to +1.0, where high values (approximately 0.6 to 0.9)  correspond to dense vegetation and negative values correspond to bare soil and water bodies. Sparse vegetation such as shrubs and grasslands or senescing crops may result in moderate NDVI values (approximately 0.2 to 0.5) ([Schneider, 2013] ; [Albarakat, 2019]). 

### METHODS
The data mainly consists of daily netCDF files. We combined the data to check homogeneous metadata to future array operations and clip the extension using a vector file of our study area so the data weights less and can be treated locally. The cloud-mask property corresponds to the state of cloud coverage, which at the same time depends on the stability of the troposphere at different levels and its thermodynamic processes. Two applications can be derived by this advantage: to create a cloud coverage record and to assess its impact on the NDVI regional values by its distribution and quantity as lost data (NDVI must be superficial). Once the daily data is cleaned from cloud-contaminated pixels, it is ready to have a preliminary monthly reduction. This step helps to fill pixels and to create representative values in the case of overlapping existing values from different days of the month. Regional NDVI for the basin was created using the median to create intermonthly variation of monthly mean NDVI. Now, this is a key point in the study as we have not done interpolations or other technique to fill the persisting missing values despite the monthly averages; in that sense we can estimate not only how much data is lost by seasonal effect, but where it is and how it is distributed. So, a count of monthly null values is done to go along with the regional NDVI which is supposed to be affected in a negative way.
In assessing the association of the percentage of lost pixels per month as the independent variable with its respective regional NDVI (which is to be imperfect as it comes from considerable lack of pixels), we used a linear regression model ([Ghebrezgabher et al. 2020]; [Al-Kindi et al. 2023]). The slope of the regression indicates the average change of the regional NDVI by the number of lost pixels by cloud occurrence and a negative value would mean a decreasing trend and a positive one, an increasing trend. A monthly plot of missing values is done by a monthly to-grid accumulation of missing values during the climatology period. That is, how the climatology of cloud draws over the region of study insistently, because it means cloud activity every available day in the monthly composition ([Yaringaño 2022]; [Armitage et al. 2013]). 

### RESULTS AND DISCUSSIONS
Figure A shows the intermonthly variation of monthly mean NDVI and percentage of lost pixels by insistence of clouds in bars. The time series has the NDVI fixed in between 0 and 0.6 (dimensionless NDVI-value), while the bars are set between 0 and 50% of the area with missing values. Both variables act seasonally. More pixels are lost in the rainy seasons of boreal spring and summer (April to September) due to the cloud coverage. Despite having done a monthly composition of the daily available data, some regions lack information due to constant convective activity. There are two apparent peaks in a year found in April (early spring) and november (mid-autumn) going through gradually low NDVI values in winter and summer. In general, in the East Africa region NDVI values gradually rise from spring to rainy season and fall steadily from autumn to winter.
It is evident also that from 2014 on the values in each variable contrast in magnitude. The NDVI values, that range between 0.2 and 0.4 through the year, change to 0.25 to 0.45. However, each sensor has different orbital characteristics and product generation corrective algorithms, and because of that there is a difference in values of NDVI and the range that oscillates ([Miura et al. 2013]). Also, the VIIRS series works with more bits, which allows representativeness of the NDVI values, which can be observed in a lower percentage of lost pixels after 2014.
In section B we plot the accumulation of missing pixels over the long-term series, by month, to aboard the cloud patterns in a spatial perspective. Constant cloud coverage/missing pixels concentrates in the high region of the study area above 1000 m a.s.l., and the low region-near the Indian Ocean in the Banaadir coast. The white areas indicate low monthly cloud occurrence where the reduction could be constructed with 25 values out of 30. The gray areas represent the pixels that had 16 to 66% of the data gone by cloud coverage. The black areas show an important void of values which is consistent despite the monthly reductions that represent the most probable places for rain activity thence higher NDVI. Surface reflectance can not be found, for example, in July near the ethiopian mountains almost for any year as they are climatological regions for convective cloud formation activated by the summer conditions. 
Figure C shows a resulting negative correlation between percentage and regional NDVI in which the high NDVI values are more likely to be found in a complete array of monthly values, and low NDVI values as the lost pixels increase. In complete arrays we can get 0.4 to 0.5. The coefficient is approximately -0.21, which despite being small, is a significant negative correlation; the R-squared 0.04, and the p-value of the regression way less than the significance level (0.05), meaning that we have enough evidence to reject the null hypothesis. This could explain the decreased NDVI values between summer and autumn corresponding to the transition between the length of both growing seasons which rests as an average to the lowest and highest NDVI values from winter and spring ([Ghebrezgabher et al. 2020]). 
The spatial distribution of the 30-year averaged monthly NDVI over the area of study is presented in Figure D. We take advantage of elevation dashed lines to see the association of the geography with the concentration of forest lands. The predominant vegetation cover types in the Juba-Shabelle basin are grasslands, woodlands, and agricultural lands (croplands) with the NDVI values that correspond to the range of 0.2-0.6. Values greater than 0.7 are in the forest area in the Ethiopian Highlands and Ahmar Mountains, northeast near the basin border ([Kalisa et al. 2019]). Unlike the other areas, these values are reached because of an annual precipitation of 850 mm ([Ghebrezgabher et al. 2020]). 

### CONCLUSIONS AND RECOMMENDATIONS 
Vegetation is concentrated along the coast of Somalia and the Ahmar mountain range because of orographic rainfall with decreased vegetation distribution and deserts in the northeast and central regions of the basin. Additionally, an increase in monthly NDVI across the basin appears to be related to a decrease in lost pixels. This is due to cloud coverage predominantly occurring over more vegetated regions. It is important to consider the impact of this lost information because of cloud coverage. Expectedly, this impact reaches a maximum during boreal summer months. As such, regional NDVI calculations may be particularly underestimated during this timeframe. A potential method for reducing the impact of cloud coverage on NDVI calculations would be spatial and temporal interpolation. Another next step is to determine the lag correlation between El Nino events and impact on NDVI. This would allow for the improvement of predictions, which are useful for food security in the region.


### REFERENCES

Abdullahi Elmi Mohamed (2013). Managing Shared Basins in the Horn of Africa – Ethiopian Projects on the Juba and Shabelle Rivers and Downstream Effects in Somalia. Natural Resources and Conservation, 1(2), 35 - 49.
https://doi.org/10.13189/nrc.2013.010203

Alfieri, L., Libertino, A., Campo, L., Dottori, F., Gabellani, S., Ghizzoni, T., Masoero, A., Rossi, L., Rudari, R., Testa, N., Trasforini, E., Amdihun, A., Ouma, J., Rossi, L., Tramblay, Y., Wu, H., and Massabò, M. (2023)  Impact-based flood forecasting in the Greater Horn of Africa, EGUsphere [preprint], https://doi.org/10.5194/egusphere-2023-804  

Al-Kindi, K.M.; Al Nadhairi, R.; Al Akhzami, S. (2023). Dynamic Change in Normalised Vegetation Index (NDVI) from 2015 to 2021 in Dhofar, Southern Oman in Response to the Climate Change. Agriculture 2023, 13, 592. 
https://doi.org/10.3390/agriculture13030592 

Andrea Ficchì, Hannah Cloke, Claudia Neves, Steve Woolnough, Erin Coughlan de Perez, Ervin Zsoter, Izidine Pinto, Arlindo Meque, Elisabeth Stephens: Beyond El Niño: Unsung climate modes drive African floods, Weather and Climate Extremes, Volume 33, 2021, 100345, ISSN 2212-0947, https://doi.org/10.1016/j.wace.2021.100345.

Armitage, R. P., Alberto Ramirez, F., Mark Danson, F., & Ogunbadewa, E. Y. (2013). Probability cloud-free observation conditions across Great Britain estimated using MODIS cloud mask. Remote Sensing Letters, 4(5), 427-435.
http://dx.doi.org/10.1080/2150704X.2012.744486  

Cao, Z., Li, Y., Liu, Y., Chen, Y. & Wang, Y. (2018). When and where did the Loess Plateau turn “green”? Analysis of the tendency and breakpoints of the normalized difference vegetation index. Land Degradation & Development 29, 162–175,  https://doi.org/10.1002/ ldr.2852 

Delire, C., Nathalie, D. N. D., Sima, A. & Gouirand, I. (2011). Vegetation Dynamics Enhancing Long-Term Climate Variability Confirmed by Two Models. Journal of Climate 24, 2238–2257, https://doi.org/10.1175/2010JCLI3664.1 

De Graff, J. V. Vegetation Cover. In: Bobrowsky P. T., Marker B. (eds) Encyclopedia of Engineering Geology. Encyclopedia of Earth Sciences Series. Springer, Cham, https://doi.org/10.1007/978-3-319-73568-9_288 

Fan, X., & Liu, Y. (2016). A global study of NDVI difference among moderate-resolution satellite sensors. ISPRS Journal of Photogrammetry and Remote Sensing, 121, 177–191. https://doi.org/10.1016/j.isprsjprs.2016.09.008 

Huq, S. & Reid, H. Climate Change and Development A Regional Report. International Institute for Environmental and Development, 3 Endsleigh Street, London WC1H 0DD, UK, 1–20. (2005).

Kalisa, W., Igbawua, T., Henchiri, M., Ali, S., Zhang, S., Bai, Y., & Zhang, J. (2019). Assessment of climate impact on vegetation dynamics over East Africa from 1982 to 2015. Scientific Reports, 9(1). https://doi.org/10.1038/s41598-019-53150-0 

Landmann, T. & Dubovyk, O. (2014). Spatial analysis of human-induced vegetation productivity decline over eastern Africa using a decade (2001–2011) of medium resolution MODIS time-series data. International Journal of Applied Earth Observation and Geoinformation. 33, 76–82, https://doi.org/10.1016/j.jag.2014.04.020

Mihretab G. Ghebrezgabher, Taibao Yang, Xuemei Yang, Temesghen Eyassu Sereke. (2020). Assessment of NDVI variations in responses to climate change in the Horn of Africa, The Egyptian Journal of Remote Sensing and Space Science, Volume 23, Issue 3, 2020, Pages 249-261, ISSN 1110-9823.
https://doi.org/10.1016/j.ejrs.2020.08.003 

Miura, T., Turner, J. P., & Huete, A. R. (2013). Spectral compatibility of the NDVI across VIIRS, MODIS, and AVHRR: An analysis of atmospheric effects using EO-1 hyperion. IEEE Transactions on Geoscience and Remote Sensing, 51(3), 1349–1359. 
https://doi.org/10.1109/TGRS.2012.2224118 

Plisnier, P. D., Serneels, S. & Lambin, E. F. (2000). Impact of ENSO on East African Ecosystems: A Multivariate Analysis Based on Climate and Remote Sensing Data. Global Ecology & Biogeography 9, 481–497, https://doi.org/10.1046/j.1365-2699.2000.00208.x 

Serdeczny, O., Adams, S., Baarsch, F. et al. Climate change impacts in Sub-Saharan Africa: from physical changes to their social repercussions. Reg Environ Change 17, 1585–1600 (2017). https://doi.org/10.1007/s10113-015-0910-2

Ssemmanda, I., Gelorini, V. & Verschuren, D. (2014). Sensitivity of East African savannah vegetation to historical moisture-balance variation. Climate of the Past 10, 2067–2080, https://doi.org/10.5194/cp-10-2067-2014

Walther, G. R. et al. (2002). Ecological responses to recent climate change. Nature 416, 389–395, https://doi.org/10.1038/416389a 

Yaringaño, K. (2022). VARIACIÓN ESPACIO-TEMPORAL DE LA NUBOSIDAD USANDO
EL PRODUCTO MÁSCARA DE NUBES MODIS SOBRE EL PERÚ [undergraduate thesis, Universidad Nacional Agraria La Molina]. Repositorio Institucional UNALM. https://repositorio.lamolina.edu.pe/handle/20.500.12996/5227 

Zhou, L. et al. (2014) Widespread decline of Congo rainforest greenness in the past decade. Nature 509, 86–90, https://doi.org/10.1038/ nature13265 

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [Serdeczny et al. 2017]: <https://doi.org/10.1007/s10113-015-0910-2>
   [Delire et al. 2011]: <https://doi.org/10.1175/2010JCLI3664.1>
   [De Graff 2018]: <https://doi.org/10.1007/978-3-319-73568-9_288>
   [Huq & Reid 2005]: <https://www.researchgate.net/publication/45182806_Climate_Change_and_Development_Links>
   [Ssemmanda et al. 2014]: <https://doi.org/10.5194/cp-10-2067-2014>
   [Cao et al. 2018]: <https://doi.org/10.1002/ldr.2852>
   [Walther et al. 2002]: <https://doi.org/10.1038/416389a>
   [Zhou et al. 2014]: <https://doi.org/10.1038/nature13265>
   [Plisnier et al.]: <https://doi.org/10.1046/j.1365-2699.2000.00208.x>
   [Landmann & Dubovyk]: <https://doi.org/10.1016/j.jag.2014.04.020>
   [Ghebrezgabher et al. 2020]: <https://doi.org/10.1016/j.ejrs.2020.08.003>
   [Al-Kindi et al. 2023]: <https://doi.org/10.3390/agriculture13030592>
   [Armitage et al. 2013]: <http://dx.doi.org/10.1080/2150704X.2012.744486>
   [Yaringaño 2022]: <https://repositorio.lamolina.edu.pe/handle/20.500.12996/5227>
   [Fan & Liu 2016]: <https://doi.org/10.1016/j.isprsjprs.2016.09.008>
   [Miura et al. 2013]: <https://doi.org/10.1109/TGRS.2012.2224118>
   [Kalisa et al. 2019]: <https://doi.org/10.1038/s41598-019-53150-0>
   [Alfieri et al. 2023]: <https://doi.org/10.5194/egusphere-2023-804>
   [Ficchì et al. 2021]: <https://doi.org/10.1016/j.wace.2021.100345>
   [Abdullahy, 2013]: <https://doi.org/10.13189/nrc.2013.010203>
