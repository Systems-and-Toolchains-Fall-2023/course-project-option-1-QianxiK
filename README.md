[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/nyeWPUMW)<br>
Name: Qianxi Kong<br>
Video Link: https://drive.google.com/file/d/1KicP7UnC-5fD7INzkZGqAp_LiaT4yxw7/view?usp=drive_link<br>
Cloud Link: <br>
Steps to run my code: There are only two parts of my code: the data folder and jupyter notebook. My code can be easily ran by going over each cell of the jupyter notebook file named"Project_Final"("Project"file is just for checkpoint).<br>

Introduction:This project involves the use of the FIFA Dataset from Kaggle. It has detailed records of male soccer players from 2015 to 2022. The key goal is to dig deep into data analysis, handling things like managing databases and machine learning.<br>

PySpark: Random Forest Regressor and Linear Regression<br>
Random Forest Regressor:<br>
Applicability: <br>
Random forests can capture non-linear relationships without extensive hyperparameter tuning.<br>
Tunable Parameters:<br>
Key parameters : numTrees, maxDepth, and featureSubsetStrategy. These parameters significantly impact model performance and overfitting. A higher number of trees can improve model accuracy but increases computational complexity.<br>
Linear Regression:<br>
Simplicity and Interpretability: <br>
Linear regression is easy to interpret. It works best when there is a linear relationship between features and the target variable.<br>

Tunable Parameters: <br>
Regularization parameters (elasticNetParam, regParam) and the number of iterations can impact the accuracy. Regularization can prevent overfitting in models with many features.<br>
PyTorch: MLP and CNN<br>
MLP (Multi-Layer Perceptron):<br>
Versatility: <br>
MLPs are fundamental neural networks that can capture complex relationships through multiple layers and neurons. They are suitable for a wide range of regression and classification tasks.<br>
Tunable Parameters: <br>
Key parameters include the number of layers, neurons in each layer, learning rate, and activation functions. <br>

CNN (Convolutional Neural Network):<br>
Spatial Data Specialization: <br>
CNNs are chosen for their ability to efficiently process spatial data, like images or data with spatial relationships, through convolutional layers. They can capture spatial hierarchies in data.<br>
Tunable Parameters: <br>
The number and size of convolutional filters, pooling layers, stride, and padding affect model performance, especially in feature extraction. The depth of the network (number of layers) can also influence learning capacity.<br>
Impact of Tunable Parameters on Accuracy<br>
Random Forest Regressor:<br>
Increasing the number of trees improves model accuracy. 
Deeper trees can model complex patterns but risk overfitting.<br>
Linear Regression:<br>
Regularization parameters control the model's complexity, preventing overfitting, especially in high-dimensional data.<br>
MLP:<br>
The number of hidden layers and neurons determines the model's capacity to learn complex patterns. However, too many neurons or layers can lead to overfitting.<br>
The learning rate is crucial for convergence; too high a rate can overshoot minima, and too low a rate can slow down training.<br>
CNN:<br>
The number of filters and their size in convolutional layers directly impact the network's ability to extract features from spatial data.
Pooling layers reduce dimensionality and can help with overfitting but might result in loss of information.
Comparison of Selected Models<br>
Random Forest vs. Linear Regression:<br>
Random Forest is more powerful for capturing complex and non-linear relationships but is computationally more intensive and less interpretable than Linear Regression.
Linear Regression is a good baseline and works well when the linear relationship between features and target.<br>
MLP vs. CNN:<br>
MLP is more general-purpose and suitable for various data types but may perform better than CNN on spatial or image data.
CNNs are specialized for spatial data due to their convolutional layers, making them the preferred choice for image processing tasks.<br>
Cross-framework Comparison:<br>
PySpark models (Random Forest, Linear Regression) are well-suited for large-scale, distributed datasets and offer robustness and simplicity.
PyTorch models (MLP, CNN) are more suited for complex pattern recognition tasks, especially where spatial relationships or deep learning techniques are essential. They require more computational resources but offer greater flexibility and learning capacity.<br>
identify constraints:<br>
1. **sofifa_id:**
   - Constraint: Primary Key, Not Null
   - Description: Unique identifier for each player in the dataset.

2. **player_url:**
   - Constraint: Unique, Not Null
   - Description: URL or link associated with the player's information.

3. **short_name:**
   - Constraint: Not Null
   - Description: Short or abbreviated name of the player.

4. **long_name:**
   - Constraint: Not Null
   - Description: Full name of the player.

5. **player_positions:**
   - Constraint: Not Null
   - Description: Positions the player typically plays in.
     
6. **overall:**
   - Constraint: Not Null, Integer Value (0-100)
   - Description: Player's overall rating based on various attributes and performance.

7. **potential:**
   - Constraint: Not Null, Integer Value (0-100)
   - Description: The potential future rating a player can achieve based on their performance and development.

8. **value_eur:**
   - Constraint: Not Null, Non-negative Value
   - Description: Player's value in euros.

9. **wage_eur:**
   - Constraint: Not Null, Non-negative Value
   - Description: Player's wage in euros.
    
10. **age:**
    - Constraint: Not Null, Non-negative Value
    - Description: Player's age.

11. **dob:**
    - Constraint: Not Null
    - Description: Player's date of birth.

12. **height_cm:**
    - Constraint: Not Null, Non-negative Value
    - Description: Player's height in centimeters.

13. **weight_kg:**
    - Constraint: Not Null, Non-negative Value
    - Description: Player's weight in kilograms.
  
14. **club_team_id:**
    - Constraint: Foreign Key, Not Null
    - Description: Unique identifier for the player's club team.

15. **club_name:**
    - Constraint: Not Null
    - Description: Name of the player's club.

16. **league_name:**
    - Constraint: Not Null
    - Description: Name of the league the player's club belongs to.

17. **league_level:**
    - Constraint: Not Null
    - Description: Level or tier of the league.
    
18. **club_position:**
    - Constraint: Not Null
    - Description: Player's position within their club.
  
19. **club_jersey_number:**
    - Constraint: Not Null, Integer Value (1-99)
    - Description: Player's jersey number in the club.

20. **club_loaned_from:**
    - Constraint: None
    - Description: Club from which the player is loaned.

21. **club_joined:**
    - Constraint: None
    - Description: Date when the player joined the club.

22. **club_contract_valid_until:**
    - Constraint: None
    - Description: Date until the player's contract with the club is valid.

23. **nationality_id:**
    - Constraint: Not Null
    - Description: Unique identifier for the player's nationality.

24. **nationality_name:**
    - Constraint: Not Null
    - Description: Name of the player's nationality.

25. **nation_team_id:**
    - Constraint: Not Null
    - Description: Unique identifier for the player's national team.

26. **nation_position:**
    - Constraint: None
    - Description: Player's position in the national team.

27. **nation_jersey_number:**
    - Constraint: None
    - Description: Player's jersey number in the national team.

28. **preferred_foot:**
    - Constraint: None
    - Description: Player's preferred foot for playing.

29. **weak_foot:**
    - Constraint: None
    - Description: Player's weak foot rating.

30. **skill_moves:**
    - Constraint: None
    - Description: Player's skill moves rating.

31. **international_reputation:**
    - Constraint: None
    - Description: Player's international reputation rating.

32. **work_rate:**
    - Constraint: None
    - Description: Player's work rate.

33. **body_type:**
    - Constraint: None
    - Description: Player's body type.

34. **real_face:**
    - Constraint: None
    - Description: Indicates if the player has a real face in the game.

35. **release_clause_eur:**
    - Constraint: Not Null, Non-negative Value
    - Description: Player's release clause value in euros.

36. **player_tags:**
    - Constraint: None
    - Description: Tags associated with the player.

37. **player_traits:**
    - Constraint: None
    - Description: Traits associated with the player.

38. **pace:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's pace rating.

39. **shooting:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's shooting rating.

40. **passing:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's passing rating.

41. **dribbling:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's dribbling rating.

42. **defending:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's defending rating.

43. **physic:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's physic rating.

44. **attacking_crossing:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's attacking crossing rating.

45. **attacking_finishing:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's attacking finishing rating.

46. **attacking_heading_accuracy:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's attacking heading accuracy rating.

47. **attacking_short_passing:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's attacking short passing rating.

48. **attacking_volleys:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's attacking volleys rating.

49. **skill_dribbling:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's skill dribbling rating.

50. **skill_curve:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's skill curve rating.

51. **skill_fk_accuracy:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's skill free-kick accuracy rating.

52. **skill_long_passing:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's skill long passing rating.

53. **skill_ball_control:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's skill ball control rating.

54. **movement_acceleration:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's movement acceleration rating.

55. **movement_sprint_speed:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's movement sprint speed rating.

56. **movement_agility:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's movement agility rating.

57. **movement_reactions:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's movement reactions rating.

58. **movement_balance:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's movement balance rating.

59. **power_shot_power:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's power shot power rating.

60. **power_jumping:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's power jumping rating.

61. **power_stamina:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's power stamina rating.

62. **power_strength:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's power strength rating.

63. **power_long_shots:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's power long shots rating.

64. **mentality_aggression:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's mentality aggression rating.

65. **mentality_interceptions:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's mentality interceptions rating.

66. **mentality_positioning:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's mentality positioning rating.

67. **mentality_vision:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's mentality vision rating.

68. **mentality_penalties:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's mentality penalties rating.

69. **mentality_composure:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's mentality composure rating.

70. **defending_marking_awareness:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's defending marking awareness rating.

71. **defending_standing_tackle:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's defending standing tackle rating.

72. **defending_sliding_tackle:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's defending sliding tackle rating.

73. **goalkeeping_diving:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's goalkeeping diving rating.

74. **goalkeeping_handling:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's goalkeeping handling rating.

75. **goalkeeping_kicking:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's goalkeeping kicking rating.

76. **goalkeeping_positioning:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's goalkeeping positioning rating.

77. **goalkeeping_reflexes:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's goalkeeping reflexes rating.

78. **goalkeeping_speed:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's goalkeeping speed rating.

79. **ls:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's left striker rating.

80. **st:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's striker rating.

81. **rs:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's right striker rating.

82. **lw:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's left winger rating.

83. **lf:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's left forward rating.

84. **cf:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's center forward rating.

85. **rf:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's right forward rating.

86. **rw:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's right winger rating.

87. **lam:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's left attacking midfielder rating.

88. **cam:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's center attacking midfielder rating.

89. **ram:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's right attacking midfielder rating.

90. **lm:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's left midfielder rating.

91. **lcm:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's left center midfielder rating.

92. **cm:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's center midfielder rating.

93. **rcm:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's right center midfielder rating.

94. **rm:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's right midfielder rating.

95. **lwb:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's left wing back rating.

96. **ldm:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's left defensive midfielder rating.

97. **cdm:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's center defensive midfielder rating.

98. **rdm:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's right defensive midfielder rating.

99. **rwb:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's right wing back rating.

100. **lb:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's left back rating.

101. **lcb:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's left center back rating.

102. **cb:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's center back rating.

103. **rcb:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's right center back rating.

104. **rb:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's right back rating.

105. **gk:**
    - Constraint: Not Null, Integer Value (0-100)
    - Description: Player's goalkeeper rating.

106. **player_face_url:**
    - Constraint: Unique, Not Null
    - Description: URL for the player's face image.

107. **club_logo_url:**
    - Constraint: Unique, Not Null
    - Description: URL for the club's logo.

108. **club_flag_url:**
    - Constraint: Unique, Not Null
    - Description: URL for the club's flag.

109. **nation_logo_url:**
    - Constraint: Unique, Not Null
    - Description: URL for the nation's logo.

110. **nation_flag_url:**
    - Constraint: Unique, Not Null
    - Description: URL for the nation's flag.
     
![image](https://github.com/Systems-and-Toolchains-Fall-2023/course-project-option-1-QianxiK/assets/144309538/0fd379c8-06ca-4da5-9cfb-6a5f297f4e7a)
