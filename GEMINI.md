# Smart Site Plan Map Data

Use the `find_open_data` tool whenever the person asks to find, see, show or map public GIS data at a place in the United States: utilities (water, sewer, storm, gas, electric), parcels and property lines, easements, zoning and land use, FEMA flood zones, wetlands, soils, topography and contours, roads, addresses, or any layer an open data portal or ArcGIS service publishes. Pass what to show and where in one plain request, for example "sewer mains in Baltimore, MD".

When the outcome is `still_working`, show the progress and the link, then call `check_open_data_search` with the `searchId` until the search ends. When the result has a link, give it to the person: it opens the data on a live map. When nothing was found, say so and do not invent a source. When the result asks a question, ask the person and search again with their answer.
