{
  "info": {
    "name": "WMATA Rail Station Information XML - Parking Information",
    "_postman_id": "16ad6295-2b77-41cd-b824-6a344cda8534",
    "description": "Description\n\nReturns parking information at a station based on a given StationCode. Omit\nthe StationCode to return parking information for all stations.\n\nIf a station has no parking, the StationsParking element will contain no\nchild elements.\n\nResponse Elements\n\n\n\n\nElement\n\nDescription\n\n\n\n\n\nStationsParking\n\n\nArray containing station parking information (StationParking).\n\n\n\n\n\n\nStationParking\nElements\n\n\n\n\n\nCode\n\nStation code. Useful when returning parking information for all\nstations. Use this value in other rail-related APIs to retrieve\ndata about a station.\n\n\n\nNotes\n\nWhen not NULL, provides additional parking resources such as\nnearby lots.\n\n\n\nAllDayParking\n\n\nStructure describing all-day\nparking options.\n\n\n\n\nShortTermParking\n\n\nStructure describing short-term\nparking options.\n\n\n\n\n\n\nAllDayParking\nElements\n\n\n\n\n\nTotalCount\n\nNumber of all-day parking spots available at a station.\n\n\n\nRiderCost\n\nAll-day cost per day (weekday) for Metro riders. NULL when no all-day\nspots are available. For most stations, this value is identical to\nthe NonRiderCost.\n\nFor cases where the NonRiderCost is different, the lower cost per\nday requires a valid rail trip using a SmarTrip&reg; card\noriginating from a station other than the one where the patron\nparked. To receive this lower rate, patrons must pay for their\nparking with the same SmarTrip&reg; card used to enter/exit\nMetrorail, and must exit the parking lot within two hours of\nexiting Metrorail.\n\n\n\nNonRiderCost\n\nAll-day cost per day (weekday) for non-Metro riders. NULL when no all-day\nspots are available.\n\n\n\n\n\nShortTermParking Elements\n\n\n\n\n\nSaturdayRiderCost\n\nSimilar to RiderCost, except denoting Saturday prices.\n\n\n\nSaturdayNonRiderCost\n\nSimilar to NonRiderCost, except denoting Saturday prices.\n\n\n\nTotalCount\n\nNumber of short-term parking spots available at a station\n(parking meters).\n\n\n\nNotes\n\nMisc. information relating to short-term parking. NULL when no\nshort-term spots are available.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Transit",
      "item": [
        {
          "id": "f6117211-d35e-486d-b1b3-8e883676f05f",
          "name": "getJsonJstationparking",
          "request": {
            "url": "http://api.wmata.com/Rail.svc/json/jStationParking?StationCode=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Description\n\nReturns parking information at a station based on a given StationCode. Omit\nthe StationCode to return parking information for all stations.\n\nIf a station has no parking, the StationsParking element will contain no\nchild elements.\n\nResponse Elements\n\n\n\n\nElement\n\nDescription\n\n\n\n\n\nStationsParking\n\n\nArray containing station parking information (StationParking).\n\n\n\n\n\n\nStationParking\nElements\n\n\n\n\n\nCode\n\nStation code. Useful when returning parking information for all\nstations. Use this value in other rail-related APIs to retrieve\ndata about a station.\n\n\n\nNotes\n\nWhen not NULL, provides additional parking resources such as\nnearby lots.\n\n\n\nAllDayParking\n\n\nStructure describing all-day\nparking options.\n\n\n\n\nShortTermParking\n\n\nStructure describing short-term\nparking options.\n\n\n\n\n\n\nAllDayParking\nElements\n\n\n\n\n\nTotalCount\n\nNumber of all-day parking spots available at a station.\n\n\n\nRiderCost\n\nAll-day cost per day (weekday) for Metro riders. NULL when no all-day\nspots are available. For most stations, this value is identical to\nthe NonRiderCost.\n\nFor cases where the NonRiderCost is different, the lower cost per\nday requires a valid rail trip using a SmarTrip&reg; card\noriginating from a station other than the one where the patron\nparked. To receive this lower rate, patrons must pay for their\nparking with the same SmarTrip&reg; card used to enter/exit\nMetrorail, and must exit the parking lot within two hours of\nexiting Metrorail.\n\n\n\nNonRiderCost\n\nAll-day cost per day (weekday) for non-Metro riders. NULL when no all-day\nspots are available.\n\n\n\n\n\nShortTermParking Elements\n\n\n\n\n\nSaturdayRiderCost\n\nSimilar to RiderCost, except denoting Saturday prices.\n\n\n\nSaturdayNonRiderCost\n\nSimilar to NonRiderCost, except denoting Saturday prices.\n\n\n\nTotalCount\n\nNumber of short-term parking spots available at a station\n(parking meters).\n\n\n\nNotes\n\nMisc. information relating to short-term parking. NULL when no\nshort-term spots are available."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7b70450c-6769-47f4-b949-effb6e21e2fc"
            }
          ]
        },
        {
          "id": "488f848b-29dd-4cba-9b2a-ff29d266050e",
          "name": "getJsonJstationentrances",
          "request": {
            "url": "http://api.wmata.com/Rail.svc/json/jStationEntrances?Lat=%7B%7D&Lon=%7B%7D&Radius=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Description\r\n\r\nReturns a list of nearby station entrances based on latitude, longitude, and\r\nradius (meters). Omit search parameters to return all station entrances.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nEntrances\r\n\r\n\r\nArray containing detailed information about station entrances\r\n(StationEntrance).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStationEntrance Elements\r\n\r\n\r\n\r\n\r\n\r\nDescription\r\n\r\nAdditional information for the entrance, if available.\r\nCurrently available data usually shows the same value as the Name\r\nelement.\r\n\r\n\r\n\r\nID\r\n\r\nDeprecated.\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nName\r\n\r\nName of the entrance (usually the station name and nearest\r\nintersection).\r\n\r\n\r\n\r\nStationCode1\r\n\r\nThe station code associated with this entrance. Use this value\r\nin other rail-related APIs to retrieve data about a station.\r\n\r\n\r\n\r\nStationCode2\r\n\r\nFor stations containing multiple platforms (e.g.: Gallery\r\nPlace, Fort Totten, L'Enfant Plaza, and Metro Center), the other\r\nstation code."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7bfce070-013c-4933-83da-87a124cd50b9"
            }
          ]
        },
        {
          "id": "2502df28-cc14-473c-b5bc-a7f72b009dab",
          "name": "getJsonJstationinfo",
          "request": {
            "url": "http://api.wmata.com/Rail.svc/json/jStationInfo?StationCode=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Description\r\n\r\nReturns station location and address information based on a given\r\nStationCode.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nAddress\r\n\r\n\r\nStructure describing address information.\r\n\r\n\r\n\r\n\r\nCode\r\n\r\nStation code. Repeated from input.\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLineCode1\r\n\r\nTwo-letter abbreviation for the line (e.g.: RD, BL, YL, OR, GR,\r\nor SV) served by this station.\r\n\r\n\r\n\r\nLineCode2\r\n\r\nAdditional line served by this station. This is often the case\r\nwhen stations have multiple platforms (e.g.: Gallery Place, Fort\r\nTotten, L'Enfant Plaza, and Metro Center).\r\n\r\n\r\n\r\nLineCode3\r\n\r\nSimilar to function as LineCodeX.\r\n\r\n\r\n\r\nLineCode4\r\n\r\nSimilar to function as LineCodeX. Currently not in use.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nName\r\n\r\nStation name.\r\n\r\n\r\n\r\nStationTogether1\r\n\r\nFor stations with multiple platforms (e.g.: Gallery Place, Fort\r\nTotten, L'Enfant Plaza, and Metro Center), the additional\r\nStationCode will be listed here.\r\n\r\n\r\n\r\nStationTogether2\r\n\r\nSimilar in function to StationTogether2. Currently not in\r\nuse.\r\n\r\n\r\n\r\n\r\n\r\nAddress Elements\r\n\r\n\r\n\r\n\r\n\r\nCity\r\n\r\nCity.\r\n\r\n\r\n\r\nState\r\n\r\nState (abbreviated).\r\n\r\n\r\n\r\nStreet\r\n\r\nStreet address (for GPS use).\r\n\r\n\r\n\r\nZip\r\n\r\nZip code."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "62817695-fc02-4261-896c-b3eb87f18086"
            }
          ]
        },
        {
          "id": "d63f8585-f821-4ca7-8a6e-054a3d8259ae",
          "name": "getJsonJstations",
          "request": {
            "url": "http://api.wmata.com/Rail.svc/json/jStations?LineCode=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Description\r\n\r\nReturns a list of station location and address information based on a given\r\nLineCode. Omit the LineCode to return all stations. The response is an array of\r\nobjects identical to those returned in the Station Information method.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nStations\r\n\r\n\r\nArray containing station information (Station).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStation Elements\r\n\r\n\r\n\r\n\r\n\r\nAddress\r\n\r\n\r\nStructure describing address information.\r\n\r\n\r\n\r\n\r\nCode\r\n\r\nStation code. Repeated from input.\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLineCode1\r\n\r\nTwo-letter abbreviation for the line (e.g.: RD, BL, YL, OR, GR,\r\nor SV) served by this station.\r\n\r\n\r\n\r\nLineCode2\r\n\r\nAdditional line served by this station. This is often the case\r\nwhen stations have multiple platforms (e.g.: Gallery Place, Fort\r\nTotten, L'Enfant Plaza, and Metro Center).\r\n\r\n\r\n\r\nLineCode3\r\n\r\nSimilar to function as LineCodeX.\r\n\r\n\r\n\r\nLineCode4\r\n\r\nSimilar to function as LineCodeX. Currently not in use.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nName\r\n\r\nStation name.\r\n\r\n\r\n\r\nStationTogether1\r\n\r\nFor stations with multiple platforms (e.g.: Gallery Place, Fort\r\nTotten, L'Enfant Plaza, and Metro Center), the additional\r\nStationCode will be listed here.\r\n\r\n\r\n\r\nStationTogether2\r\n\r\nSimilar in function to StationTogether2. Currently not in\r\nuse.\r\n\r\n\r\n\r\n\r\n\r\nAddress Elements\r\n\r\n\r\n\r\n\r\n\r\nCity\r\n\r\nCity.\r\n\r\n\r\n\r\nState\r\n\r\nState (abbreviated).\r\n\r\n\r\n\r\nStreet\r\n\r\nStreet address (for GPS use).\r\n\r\n\r\n\r\nZip\r\n\r\nZip code."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "debdb1fc-b6fd-499e-8196-e642aab5ef98"
            }
          ]
        },
        {
          "id": "5473c304-ae3e-4207-90be-b74579e4644d",
          "name": "getJsonJstationtimes",
          "request": {
            "url": "http://api.wmata.com/Rail.svc/json/jStationTimes?StationCode=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Description\r\n\r\nReturns opening and scheduled first/last train times based on a given\r\nStationCode. Omit the StationCode to return timing information for all\r\nstations.\r\n\r\nNote that for stations with multiple platforms (e.g.: Metro Center, L'Enfant\r\nPlaza, etc.), a distinct call is required for each StationCode to retrieve the\r\nfull set of train times at such stations.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nStationTimes\r\n\r\n\r\nArray containing station timing information (StationTime).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStationTime\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nCode\r\n\r\nStation code for this station. Use this value in other\r\nrail-related APIs to retrieve data about a station.\r\n\r\n\r\n\r\nStationName\r\n\r\nFull name of the station.\r\n\r\n\r\n\r\n*Day Elements\r\n\r\n\r\nContainer elements containing timing information based on\r\nday of the week.\r\n\r\n\r\n\r\n\r\n\r\n\r\nMonday/Tuesday/Wednesday/etc.\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nOpeningTime\r\n\r\nStation opening time. Format is HH:mm.\r\n\r\n\r\n\r\nFirstTrains\r\n\r\n\r\nStructure containing first train\r\ninformation.\r\n\r\n\r\n\r\n\r\nLastTrains\r\n\r\n\r\nStructure containing last train\r\ninformation.\r\n\r\n\r\n\r\n\r\n\r\n\r\nFirstTrains Elements\r\n\r\n\r\n\r\n\r\n\r\nTime\r\n\r\nFirst train leaves the station at this time. Format is\r\nHH:mm.\r\n\r\n\r\n\r\nDestinationStation\r\n\r\nStation code for the train's destination. Use this value in\r\nother rail-related APIs to retrieve data about a station.\r\n\r\n\r\n\r\n\r\n\r\nLastTrains Elements\r\n\r\n\r\n\r\n\r\n\r\nTime\r\n\r\nLast train leaves the station at this time. Format is HH:mm.\r\nNote that when the time is AM, it signifies the next day. For\r\nexample, a value of 02:30 under a Saturday element means the last\r\ntrain leaves on Sunday at 2:30 AM.\r\n\r\n\r\n\r\nDestinationStation\r\n\r\nStation code for the train's destination. Use this value in\r\nother rail-related APIs to retrieve data about a station."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7b9d0323-0e8e-471e-881a-c8eb8faf642d"
            }
          ]
        },
        {
          "id": "c67f7772-3b6e-47ab-9cb2-b27dccd25aa7",
          "name": "getJsonJsrcstationtodststationinfo",
          "request": {
            "url": "http://api.wmata.com/Rail.svc/json/jSrcStationToDstStationInfo?FromStationCode=%7B%7D&ToStationCode=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Description\r\n\r\nReturns a distance, fare information, and estimated travel time between any\r\ntwo stations, including those on different lines. Omit both parameters to\r\nretrieve data for all stations.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nStationToStationInfos\r\n\r\n\r\nArray containing station to station information (StationToStationInfo).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStationToStationInfo Elements\r\n\r\n\r\n\r\n\r\n\r\nCompositeMiles\r\n\r\nDistance in miles from the source to destination station.\r\n\r\n\r\n\r\nDestinationStation\r\n\r\nDestination station code. Use this value in other rail-related\r\nAPIs to retrieve data about a station.\r\n\r\n\r\n\r\nRailFare\r\n\r\n\r\nStructure containing fare information.\r\n\r\n\r\n\r\n\r\nRailTime\r\n\r\nEstimated travel time (schedule time) in minutes between the source and\r\ndestination station. This is not correlated to minutes (Min) in Real-Time Rail Predictions.\r\n\r\n\r\n\r\nSourceStation\r\n\r\nOrigin station code. Use this value in other rail-related APIs\r\nto retrieve data about a station.\r\n\r\n\r\n\r\n\r\n\r\nRailFare Elements\r\n\r\n\r\n\r\n\r\n\r\nOffPeakTime\r\n\r\nFare during off-peak times (times other than the ones described\r\nbelow).\r\n\r\n\r\n\r\nPeakTime\r\n\r\nFare during peak times (weekdays from opening to 9:30 AM and\r\n3-7 PM, and weekends from midnight to closing).\r\n\r\n\r\n\r\nSeniorDisabled\r\n\r\n\r\nReduced fare for senior citizens or\r\npeople with disabilities."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bceeeb98-39da-406a-8f0c-4ae8c30a6aba"
            }
          ]
        },
        {
          "id": "a2edc036-67e0-42a1-9e0f-508fda19ebad",
          "name": "getStationparking",
          "request": {
            "url": "http://api.wmata.com/Rail.svc/StationParking?StationCode=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Description\n\nReturns parking information at a station based on a given StationCode. Omit\nthe StationCode to return parking information for all stations.\n\nIf a station has no parking, the StationsParking element will contain no\nchild elements.\n\nResponse Elements\n\n\n\n\nElement\n\nDescription\n\n\n\n\n\nStationsParking\n\n\nArray containing station parking information (StationParking).\n\n\n\n\n\n\nStationParking\nElements\n\n\n\n\n\nCode\n\nStation code. Useful when returning parking information for all\nstations. Use this value in other rail-related APIs to retrieve\ndata about a station.\n\n\n\nNotes\n\nWhen not NULL, provides additional parking resources such as\nnearby lots.\n\n\n\nAllDayParking\n\n\nStructure describing all-day\nparking options.\n\n\n\n\nShortTermParking\n\n\nStructure describing short-term\nparking options.\n\n\n\n\n\n\nAllDayParking\nElements\n\n\n\n\n\nTotalCount\n\nNumber of all-day parking spots available at a station.\n\n\n\nRiderCost\n\nAll-day cost per day (weekday) for Metro riders. NULL when no all-day\nspots are available. For most stations, this value is identical to\nthe NonRiderCost.\n\nFor cases where the NonRiderCost is different, the lower cost per\nday requires a valid rail trip using a SmarTrip&reg; card\noriginating from a station other than the one where the patron\nparked. To receive this lower rate, patrons must pay for their\nparking with the same SmarTrip&reg; card used to enter/exit\nMetrorail, and must exit the parking lot within two hours of\nexiting Metrorail.\n\n\n\nNonRiderCost\n\nAll-day cost per day (weekday) for non-Metro riders. NULL when no all-day\nspots are available.\n\n\n\n\n\nShortTermParking Elements\n\n\n\n\n\nSaturdayRiderCost\n\nSimilar to RiderCost, except denoting Saturday prices.\n\n\n\nSaturdayNonRiderCost\n\nSimilar to NonRiderCost, except denoting Saturday prices.\n\n\n\nTotalCount\n\nNumber of short-term parking spots available at a station\n(parking meters).\n\n\n\nNotes\n\nMisc. information relating to short-term parking. NULL when no\nshort-term spots are available."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2762830c-359a-4f84-af83-928e2142031b"
            }
          ]
        }
      ]
    }
  ]
}