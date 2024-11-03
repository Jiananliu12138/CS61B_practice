# tilt
1. Firstly, set the direction and reverse the image according to the input direction, with the aim of using true north as the direction for all image operations, making it easy to operate.
2. The first big loop is to find the first non null Tile element in each column, and then search downwards for lowerTile.
- If the values of lowerTile and Tile are equal, the move method in Board is used to merge them, calculate the score, and the subsequent search starts from the lowerTile row downwards (the move method clears the value of lowerTile here), while avoiding multiple merges as mentioned in the rule.
- If the values of lowerTile and Tile are not equal, jump out of the loop and search for new tiles in the remaining rows of this column.
3. Our array has now completed merging and score calculation according to the game rules, but there are many null values in the middle of our array. The goal of the second large loop is to fill these null values so that our values are closely aligned and achieve the game effect.
4. The final step is to flip the image back to its original state, with the main purpose of making all up, down, left, and right movements turn into upward movements.