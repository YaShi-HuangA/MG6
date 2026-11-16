# MG6
1.
The entire `for` loop will finish before the `Update()` method finishes. It does not execute one iteration per frame. If the loop takes a really long time to finish, it can make the game lag because Unity has to complete the loop before moving on. It will not automatically continue over multiple frames.

2.One issue I discovered is that the player can sometimes fall through the ground or other objects while jumping. This happens because our logic disables the player's collider whenever the player is moving upward. It disables collisions with everything, not just the platforms. So if the player jumps while underneath another object, the player might pass through it too.
