# DSWorkCES
Data Science Work for Career Exploration Office &amp; Rutgers as part of my senior thesis, along with best practices and helper functions to use going forward when spreading the data for further use among the university.

# Layout of code

Layout of code:

1. Imports
2. Data import/cleaning
3. Visualizations
    1. **Part 1:** General visualizations [bold are biggest metrics to track]
        1. **Graph 1: What % replied yes/no to satisfaction**
        2. **Graph 2: % in each post_grad_status by year and semester**
        3. Graph 3/4: Post grad status counts and % satisfied by status
        4. Graph 5: Number of experiences
        5. Graph 6: % satisfaction by # of experiences
        6. Graph 7: What do unsatisfied prefer
        7. Graph 8/9: What % of those who did experience _ were satisfied, and counts of yes/no per experience
        8. Graph 10: How did people get their position
        9. Graph 11: How many of each actvitiy are seeking employment
        10. Graph 12: % satisfaction by survey semester and year
        11. Graph 13/14: 10 happiest and least happy majors
        12. Graph 15: Top 10 % seeking employment majors
        13. Graph 16: Bottom 10% seeking employment majors
        14. Graph 17: Top 10 majors with ratio of grad school competitiveness
        15. Graph 18: Bottom 10 majors by graduate school competitiveness (i.e. ratio of wanting to go vs being in)
        16. Graph 19: Reasons not doing any experience
        17. Graph 20: Majors with biggest counts of the top 10 reasons for not doing any experience
    2. **Part 2:** Specific visualizations
        1. Graph 21: Make major groups using same majors as in part 1 of my thesis and plot by % satisfaction
        2. Graph 22: Plot each college in Rutgers by % satisfied
        3. Graph 23-28: Showing each college and the % of people in that college in each status
        4. Table 29: Showing each experience and the count of those who did those experiences in each post_grad_status and the experiences that have the highest who did them fully employed, in grad school versus want to, and seeking employment.
    3. **Part 3:** Models: Note that since 2/3 of the data has post_grad_choice=Yes, it’s an imbalanced dataset since our prediction should include 2/3 as one class over another. As a result, all 5 models can predict around 66% accuracy just by predicting all satisfied, so the models are all balanced. ********************************************[bold are most useful]********************************************
        1. Split into regular training and testing
            1. **Model 1: Status**
            2. Model 2: Experiences
            3. Model 3: Majors
            4. Model 4: Majors & Experiences
            5. Model 5: Status & Majors & Experiences
        2. Using synthetic training data
            1. Model 1.2: Status
            2. Model 2.2: Experiences
            3. Model 3.2: Majors
            4. **Model 4.2: Majors & Experiences**
            5. Model 5.2: Status & Majors & Experiences
        3. Decision Tree
            1. **Model 6: Decision tree**
        4. PCA: Principal Component analysis shows which of the independent variables explains most of the variance in the dependent variable. Since it’s categorical variables (even one hot encoded as numerical variables) it isn’t very useful, but shows that few of the majors contribute to the variance whereas mostly it’s certain experiences and statuses.
            1. Model 7: PCA
    4. ****************Part 4:**************** Helper functions
        1. Majors
            1. Helper 1: Pick a major. Find the % satisfaction.
        2. Experiences
            1. Helper 2: Pick an experience. Find the 10 majors who did it the most.
        3. Status
            1. Helper 3: Pick a major. Find the post_grad_status breakdown
            2. Helper 4: Pick a major. Find how satisfied those from that major were in different statuses.
            3. Helper 5: Pick a major. Shows a table of what status those in that major who did each experience are in.
        5. Intro to helper 6: Investigating graph 8 as to why Field Placements aren't more effective to satisfaction than doing no experience.
            1. Helper 6.1: Investigate how much doing an experience led to satisfaction for a major.
            2. Helper 6.2: Investigate the effectiveness of an experience on a major for satisfaction versus other majors.
            3. Helper 6.3: Investigate the effectiveness of an experience on a major for ending up in a status versus other majors.
    5. ****************Part 5:**************** Appendix functions
        1. Appendix 1: Graph to show post_grad_status by experiences done by those in that status
        2. Appendix 2: Investigating duplicate experiences
        3. Appendix 3: Hard coded typo checks
        4. Appendix 4: Checking people who replied satisfied yet had preferred - what were their preferred?