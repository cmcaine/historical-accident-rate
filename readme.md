# Historical accident rate

Use stats19 and historic travel data (HTD) to establish where possible an accident rate.

This is useful because mode share and overall traffic on routes has changed non-uniformly across the country -- otherwise we could just do something based on the deviation from the mean for each time interval.

Method:

MVP:

- stats19 is easy with Robin's package, so work on the historical travel data
- Identify time resolution of HTD
   - Casweb: "We provide access to England, Wales, and Scotland 2001, 1991, 1981, 1971 data"
- Identify spatial resolution of HTD for each time interval
   - If all the same: done
   - If not work it out
- split stats19 by polygons derived from last step
- split again by time intervals
- collision rate = number of collisions / number of journeys
- plot chloropleth of collision rate per mode

Later:

- fit a linear model to predict collision rate from number of journeys/modeshare/urban-rural/demographic data
- Cluster census areas by the same variables (for the module. No hypothesis yet)

Issues:

- What intervals should I use?
   - 10 years centered on each census year seems sensible.

Hypotheses:

- The rate of cyclist injury will be negatively correlated with cycle mode share, after correcting for other factors
   - May be impossible to isolate cycle mode share from e.g. how urban the area is.
- Areas with greater investment in cycling and walking infrastructure will have lower collision rates for those modes
- Areas with greater investment in cycling and walking infrastructure will have lower collision rates for all modes
- There will be no relation between controlling political party of local government and collision rate, after adjusting for other factors.
