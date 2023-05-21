# NFL Win Total Data (2003 - 2022)
NFL win total odds, implied pre-season ratings, and observed results

This dataset contains data on how each team was projected to do based on pre-season win total odds and how well they actually did based on wins and SRS (simple rating system) derived from game margins.

### Data Sources ###
Win total odds come from Lee Sharpe's nflgamedata dataset from 2003 to 2020. Odds from 2021 to 2022 come from CBS sports news articles.
All observed data is derived from Lee Sharpe's nflgamedata file
QB adjustments are made from 538's QB Elo ratings

### Data Dictionary ###
* line_adj is the pre-season win total line adjusted for hold derived from the over and under odds numbers
* wt_ratings are the team strengths implied by the line_adj win totals. These are calculated by running the combining schedule with line_adj and solving for wt_rating using an optimizer
* sos is the projected strength of schedule use wt_ratings. This number represents the average points the team's average opponent is expected to win by against an average team. The greater the number, the harder the schedule
* srs stands for "Simple Rating System" and is the observed rating of the team from the actual game results. The higher the number the better the team
* observed_sos is the the actual strength of schedule faced by the team using srs to determine opponent strength
* observed_sos_w_qb_adj is the actual strength of schedule faced by the team, but also accounts for QB injuries that may have made the schedule easier or harder than would be implied based on srs alone

