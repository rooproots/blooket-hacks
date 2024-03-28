

// This code multiplies the points earned in Blooket games by a specified factor.
const multiplier = 2; // Change this value to set the multiplier factor

const originalAddPointsFunction = BlooketGame.prototype.addPoints;
BlooketGame.prototype.addPoints = function(points) {
    points *= multiplier;
    originalAddPointsFunction.call(this, points);
};
