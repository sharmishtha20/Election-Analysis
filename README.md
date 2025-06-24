# Election-Analysis
A SQL-based project analyzing the 2024 Indian General Elections. Includes insights on total seats, party-wise wins, alliance classification (NDA, I.N.D.I.A, OTHER), vote types (EVM/postal), top candidates, and state-wise summaries using advanced queries, joins, and window functions.

1.Database Tables
 
     partywise_results
     
     constituencywise_results
     
     constituencywise_details
     
     statewise_results
     
     states.



 2.Features
    ✅ Total seats across states and constituencies
    
    🧮 Party-wise and alliance-wise seat counts (NDA, I.N.D.I.A, OTHER)
    
    🔁 Classification of parties into alliances using UPDATE statements
    
    🥇 Identify winning and runner-up candidates per constituency
    
    🔍 Top 10 candidates with highest EVM votes
    
    🗳️ Comparison of EVM vs Postal votes by constituency
    
    📍 State-specific summaries (e.g., Maharashtra analysis).
  

3.Key Concepts Used

    1.Joins (INNER JOIN)
    Joins were used to merge data from normalized tables like partywise_results, constituencywise_results,
     statewise_results, states, and constituencywise_details. These joins enabled the analysis of vote counts, 
     party affiliations, and state-wise results in a unified view.
    
    2.Aggregate Functions
    SQL functions like COUNT(), SUM(), and MAX() helped calculate total seats, total votes, party-wise wins, and top vote-getters
    in each constituency. These functions were essential for producing summary statistics and ranking results.
    
    3.Window Functions
     The ROW_NUMBER() window function was used to rank candidates within each constituency based on total votes.
     This allowed identification of both winners and runner-up candidates effectively.
     
    4.Common Table Expressions (CTE)
    CTEs provided a clean way to structure complex subqueries, especially when ranking candidates by vote count.
    They improved readability and modularity in queries, such as in the winner vs. runner-up analysis.
    
    5.Conditional Aggregation
    CASE WHEN statements inside aggregation functions helped to compute the number of seats won by different alliances 
    (e.g., NDA, I.N.D.I.A, OTHER) and provided flexibility in segmenting data based on conditions.
    
    6.Data Classification and Transformation
    SQL ALTER TABLE and UPDATE statements were used to add a new column (party_alliance) and populate it by 
    classifying each party into their respective alliance. This was crucial for grouping results by political blocs.
    
    7.Filtering and Sorting
    WHERE, GROUP BY, and ORDER BY clauses were used to focus the analysis on specific states or constituencies, 
    organize the results, and present data in a logical order (e.g., descending by seats won or vote margin).
    
    8.Top-N Queries
    SELECT TOP 10 was used to retrieve the top 10 candidates based on EVM votes across constituencies,
    showcasing leading performers in the election.
