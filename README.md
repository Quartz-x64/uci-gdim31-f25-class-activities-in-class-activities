# in-class-activities
## Devlogs
### W1
When I moved the Camera GameObject off of the Cat GameObject, the camera stopped moving with the cat. This is because the Camera was moving with the cat because of the parent-child relationship, where the cat parent GameObject was carrying the camera child GameObject.
https://quartz-x64.itch.io/w1

### W2
r, g, and b variables are not true or false questions, so they're not bool. They are not names or dialogues, so they're not string. They can be decimal, so they are float but not int.
_bounce variable is not true or false question, so it's not bool. It's not name or dialogue, so it's not string. It can be integer but cannot be decimal, so it's int but not float.
Its semicolon is missing.

### W3
1.Table #: 13
GetResponse
- Parameters: int friendshipLevel, bool knowsSecret
- Return type: string
- Reason: This method uses the player’s friendship level and whether they know the character’s secret to return a dialogue response.
SetLightDimness
- Parameter: float sanityLevel
- Return type: void
- Reason: This method adjusts the light’s brightness based on the player’s sanity level and does not need to return a value.
DidPlayerHitBeat
- Parameter: float keyPressTime
- Return type: bool
- Reason: This method checks whether the player’s key press timing matches the beat and returns true or fals.
2.A class is like a blueprint for a Component: it describes what each instance can be and do. Member variables are its traits, while methods are the actions it can perform. Each Component made from the class has its own trait values.
3.Each fast bounce multiplies the ball’s current color by 1.5, so the brightness grows exponentially instead of resetting. After many bounces, the color values can exceed their normal range, making the balls look extremely bright, especially with HDR or Bloom enabled.

### W4
I added Rigidbody components to the Cat and the SoccerBall. The Cat needs one so its jump force works and it can collide with the ball and walls. The ball needs one so it can respond to the Cat’s kick and bounce off the walls.
I checked Is Trigger only on the Goal’s BoxCollider. That lets the game detect when the ball enters the goal area while allowing the ball to pass through. The Cat’s CapsuleCollider and the SoccerBall’s SphereCollider remain solid so they can collide with walls and each other.
The Cat fell over after adding its Rigidbody, I freeze its rotation on the X and Z axes in Rigidbody Constraints. I also check that CatW4’s Rigidbody field references the Cat’s Rigidbody; if it still shows None, jumping may cause an error or fail.

## Open-Source Assets
### W1
- Animals: https://assetstore.unity.com/packages/3d/characters/animals/animals-free-animated-low-poly-3d-models-260727 
- Low-poly environment: https://assetstore.unity.com/packages/3d/environments/landscapes/low-poly-simple-nature-pack-162153 
