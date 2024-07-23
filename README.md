# Free Rugby API

The **Rugby API** provides a comprehensive suite of data for rugby enthusiasts and developers, offering real-time updates, player statistics, team information, and more. This API is designed to deliver detailed insights into rugby matches, player performance, and team statistics, enhancing applications and services related to rugby. This API can be found on RapidAPI, [Click here to open](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/rugby-live-data-complete)

## Key Features

- **Live Match Data**: Access real-time updates during rugby matches, including scores, match events, and player statistics.
- **Player Statistics**: Retrieve detailed performance metrics for rugby players, including tries, tackles, and other key statistics.
- **Team Information**: Get information on rugby teams, including rosters, rankings, and performance metrics.
- **Match Schedules**: View upcoming matches, including dates, venues, and fixture details.
- **Historical Data**: Access past match results and player statistics for thorough analysis and historical comparisons.

## Getting Started

1. **Sign Up**: Create an account on RapidAPI.
2. **Subscribe**: Choose a subscription plan that fits your needs.
3. **API Key**: Obtain your unique API key to begin making requests.
4. **Documentation**: For detailed usage instructions, visit the [Rugby API Documentation](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/rugby-live-data-complete).


## Endpoint: Retrieve League IDs

### URL

`GET /leagueIds`

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing a list of league IDs and their corresponding names.

  ```json
  {
      "leagueIds": {
          "164205": "Rugby World Cup",
          "180659": "Six Nations",
          "244293": "Rugby Championship",
          "271937": "European Rugby Champions Cup",
          "267979": "Premiership Rugby",
          "270557": "United Rugby Championship",
          "2009": "URBA Top 12",
          "242041": "Super Rugby Pacific",
          "270555": "Currie Cup",
          "270563": "National Provence Championship",
          "256449": "Pacific Nations Cup",
          "282": "Olympic Men's 7s",
          "283": "Olympic Women's Rugby Sevens",
          "289237": "Women's Rugby World Cup"
      }
  }


## Endpoint: Retrieve Game BoxScore

### URL

`GET /boxscore`

### Query Parameters

- `gameId` (string, optional): The unique identifier for the game. Default value is `'597223'`.
- `leagueId` (string, optional): The unique identifier for the league. Default value is `'242041'`.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing the box score of the specified game.
  
  ```json
  {
      // Example response format
      "team1": {
          "score": 100,
          "players": [
              // player details
          ]
      },
      "team2": {
          "score": 95,
          "players": [
              // player details
          ]
      }
  }


## Endpoint: Retrieve Game Information

### URL

`GET /gameInfo`

### Query Parameters

- `gameId` (string, optional): The unique identifier for the game. Default value is `'597223'`.
- `leagueId` (string, optional): The unique identifier for the league. Default value is `'242041'`.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing the game information of the specified game.
  
  ```json
  {
      // Example response format
      "gameDetails": {
          "date": "2023-07-23",
          "location": "Stadium Name",
          "teams": {
              "home": "Team A",
              "away": "Team B"
          },
          "score": {
              "home": 100,
              "away": 95
          }
      }
  }

## Endpoint: Retrieve Last Five Games

### URL

`GET /last-five-games`

### Query Parameters

- `gameId` (string, optional): The unique identifier for the game. Default value is `'597223'`.
- `leagueId` (string, optional): The unique identifier for the league. Default value is `'242041'`.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing the details of the last five games related to the specified game.

  ```json
  {
      // Example response format
      "lastFiveGames": [
          {
              "date": "2023-07-18",
              "opponent": "Team X",
              "score": {
                  "home": 95,
                  "away": 88
              }
          },
          {
              "date": "2023-07-15",
              "opponent": "Team Y",
              "score": {
                  "home": 100,
                  "away": 102
              }
          },
          // more games
      ]
  }


## Endpoint: Retrieve Game Summary

### URL

`GET /game-summary`

### Query Parameters

- `gameId` (string, optional): The unique identifier for the game. Default value is `'597388'`.
- `league` (string, optional): The unique identifier for the league.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing the summary of the specified game.
  
  ```json
  {
      // Example response format
      "summary": {
          "gameId": "597388",
          "league": "League Name",
          "date": "2023-07-23",
          "location": "Stadium Name",

## Endpoint: Retrieve Game Head to Head

### URL

`GET /head-to-head`

### Query Parameters

- `gameId` (string, optional): The unique identifier for the game. Default value is `'597223'`.
- `leagueId` (string, optional): The unique identifier for the league. Default value is `'242041'`.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing the head-to-head comparison for the specified game.

  ```json
  {
      // Example response format
      "headToHead": {
          "team1": {
              "name": "Team A",
              "wins": 5,
              "losses": 3
          },
          "team2": {
              "name": "Team B",
              "wins": 3,
              "losses": 5
          },
          "recentMeetings": [
              {
                  "date": "2023-07-18",
                  "score": {
                      "team1": 100,
                      "team2": 95
                  }
              },
              {
                  "date": "2023-06-15",
                  "score": {
                      "team1": 98,
                      "team2": 101
                  }
              }
          ]
      }
  }


## Endpoint: Retrieve Game Odds

### URL

`GET /odds`

### Query Parameters

- `gameId` (string, optional): The unique identifier for the game. Default value is `'597223'`.
- `leagueId` (string, optional): The unique identifier for the league. Default value is `'242041'`.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing the odds for the specified game.

  ```json
  {
      // Example response format
      "odds": {
          "team1": {
              "name": "Team A",
              "odds": 1.5
          },
          "team2": {
              "name": "Team B",
              "odds": 2.5
          }
      }
  }


## Endpoint: Retrieve Game Roster

### URL

`GET /rosters`

### Query Parameters

- `gameId` (string, optional): The unique identifier for the game. Default value is `'597223'`.
- `leagueId` (string, optional): The unique identifier for the league. Default value is `'242041'`.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing the rosters for the specified game.
  
  ```json
  {
      // Example response format
      "team1": {
          "name": "Team A",
          "roster": [
              {
                  "playerId": "123",
                  "name": "Player One",
                  "position": "Forward",
                  "number": 10
              },
              // more players
          ]
      },
      "team2": {
          "name": "Team B",
          "roster": [
              {
                  "playerId": "456",
                  "name": "Player Two",
                  "position": "Guard",
                  "number": 12
              },
              // more players
          ]
      }
  }


## Endpoint: Retrieve Standings by Games

### URL

`GET /standings-by-games`

### Query Parameters

- `gameId` (string, optional): The unique identifier for the game. Default value is `'597223'`.
- `leagueId` (string, optional): The unique identifier for the league. Default value is `'242041'`.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing the standings based on games for the specified league and game.

  ```json
  {
      // Example response format
      "standings": [
          {
              "team": "Team A",
              "wins": 10,
              "losses": 5
          },
          {
              "team": "Team B",
              "wins": 8,
              "losses": 7
          },
          // more teams
      ]
  }

## Endpoint: Retrieve Scoreboard Data

### URL

`GET /scoreboard`

### Query Parameters

- `league` (string, optional): The unique identifier for the league. Default value is `'242041'`.
- `year` (number, optional): The year for which the scoreboard data is being requested. Default value is `2023`.
- `month` (number, optional): The month for which the scoreboard data is being requested. Default value is `null`.
- `day` (number, optional): The day for which the scoreboard data is being requested. Default value is `null`.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing the scoreboard data for the specified league, year, month, and day.

  ```json
  {
      // Example response format
      "scoreboard": [
          {
              "date": "2023-07-23",
              "games": [
                  {
                      "gameId": "597388",
                      "teams": {
                          "home": "Team A",
                          "away": "Team B"
                      },
                      "score": {
                          "home": 100,
                          "away": 95
                      },
                      "status": "Final"
                  },
                  // more games
              ]
          }
      ]
  }


## Endpoint: Retrieve Schedule Data

### URL

`GET /fixture`

### Query Parameters

- `year` (number, required): The year for which the schedule data is being requested.
- `month` (number, required): The month for which the schedule data is being requested.
- `day` (number, required): The day for which the schedule data is being requested.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing the schedule data for the specified date.

  ```json
  {
      "fixture": {
          // Example response format
          "games": [
              {
                  "gameId": "597388",
                  "teams": {
                      "home": "Team A",
                      "away": "Team B"
                  },
                  "date": "2023-07-23",
                  "time": "15:00",
                  "location": "Stadium Name"
              },
              // more games
          ]
      }
  }

## Endpoint: Retrieve Schedule Data by League

### URL

`GET /fixture-by-league`

### Query Parameters

- `year` (number, required): The year for which the schedule data is being requested.
- `month` (number, required): The month for which the schedule data is being requested.
- `day` (number, required): The day for which the schedule data is being requested.
- `leagueId` (string, required): The unique identifier for the league.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing the schedule data for the specified date and league.

  ```json
  {
      "fixture": {
          // Example response format
          "games": [
              {
                  "gameId": "597388",
                  "teams": {
                      "home": "Team A",
                      "away": "Team B"
                  },
                  "date": "2024-03-12",
                  "time": "15:00",
                  "location": "Stadium Name"
              },
              // more games
          ]
      }
  }

## Endpoint: Retrieve Standings

### URL

`GET /standings`

### Query Parameters

- `year` (number, optional): The year for which the standings data is being requested. Default value is `2024`.
- `leagueId` (string, required): The unique identifier for the league.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing the standings data for the specified year and league.

  ```json
  {
      // Example response format
      "standings": [
          {
              "team": "Team A",
              "wins": 15,
              "losses": 3,
              "draws": 2,
              "points": 47
          },
          {
              "team": "Team B",
              "wins": 12,
              "losses": 6,
              "draws": 2,
              "points": 38
          },
          // more teams
      ]
  }

## Endpoint: Retrieve Lineups

### URL

`GET /lineups`

### Query Parameters

- `gameId` (string, optional): The unique identifier for the game. Default value is `'597223'`.
- `leagueId` (string, optional): The unique identifier for the league. Default value is `'242041'`.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing the lineups data for the specified game and league.

  ```json
  {
      // Example response format
      "lineups": {
          "homeTeam": {
              "players": [
                  {
                      "playerId": "123",
                      "name": "Player A",
                      "position": "Forward"
                  },
                  {
                      "playerId": "124",
                      "name": "Player B",
                      "position": "Back"
                  }
                  // more players
              ]
          },
          "awayTeam": {
              "players": [
                  {
                      "playerId": "125",
                      "name": "Player C",
                      "position": "Forward"
                  },
                  {
                      "playerId": "126",
                      "name": "Player D",
                      "position": "Back"
                  }
                  // more players
              ]
          }
      }
  }

## Endpoint: Retrieve News

### URL

`GET /news`

### Query Parameters

- `limit` (number, optional): The maximum number of news items to return. Default value is `15`.
- `league` (string, optional): The unique identifier for the league. Default value is `'271937'`.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing the news data for the specified league and limit.

  ```json
  {
      "news": [
          {
              "id": "1",
              "headline": "Team A Wins Championship",
              "date": "2024-07-23",
              "summary": "Team A clinched the championship title with a decisive victory over Team B."
          },
          {
              "id": "2",
              "headline": "Player X Transfers to New Team",
              "date": "2024-07-22",
              "summary": "Player X has signed with Team C after a successful season with Team D."
          }
          // more news items
      ]
  }

## Endpoint: Retrieve Teams Information

### URL

`GET /teamsInfo`

### Query Parameters

- `leagueId` (string, optional): The unique identifier for the league. Default value is `'242041'`.
- `teamId` (string, optional): The unique identifier for the team. Default value is `'25936'`.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing information about the specified team and league.

  ```json
  {
      "teamInfo": {
          "teamId": "25936",
          "name": "Team A",
          "leagueId": "242041",
          "leagueName": "Premier League",
          "players": [
              {
                  "playerId": "123",
                  "name": "Player A",
                  "position": "Forward"
              },
              {
                  "playerId": "124",
                  "name": "Player B",
                  "position": "Back"
              }
              // more players
          ],
          "coach": "Coach A",
          "stadium": "Stadium Name"
      }
  }


## Commonly Asked Questions

### 1. What kind of data can I access through the Rugby API?
You can access live match data, player statistics, team information, match schedules, and historical data.

### 2. How do I authenticate my API requests?
You need to include your API key in the headers of your requests as detailed in the API documentation.

### 3. Are there usage limits for the API?
Yes, usage limits vary depending on your subscription plan. Check the RapidAPI dashboard for specifics.

### 4. Can I filter data by specific matches, teams, or players?
Yes, the API allows filtering to retrieve data for specific matches, teams, or players.

### 5. Is historical data available for past matches?
Yes, the Rugby API includes historical data for past matches, allowing for detailed analysis and comparisons.

### 6. How frequently is the data updated?
The data is updated in real-time during live matches and periodically for historical data and schedules.

### 7. Can I access data for international and domestic rugby leagues?
Yes, the API provides data for both international and domestic rugby leagues and tournaments.

### 8. What formats does the API support for data responses?
The API supports data responses in JSON format, making it easy to integrate into various applications.

### 9. Are there specific endpoints for different types of data (e.g., scores, player stats)?
Yes, the API includes specific endpoints for various types of data, such as match scores, player statistics, and team information.

### 10. How can I stay updated on changes to the API?
You can stay informed about updates and changes by checking the API documentation and RapidAPI dashboard regularly.

For more information and to start using the Rugby API, visit [Rugby API on RapidAPI](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/rugby-live-data-complete).





