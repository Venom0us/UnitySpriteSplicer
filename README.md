# UnitySpriteSplicer
Slices a sprite into multiple square sprites, supports positioning, rotation and scaling.
PPU must be the same as the width/height of the sprite.
So for example: 64x64 : PPU: 64

# Usage
```csharp
public void Start()
{
    var renderer = gameObject.GetComponent<SpriteRenderer>();
  
    // Spawn spliced gameobject on top of current game object
    const int slices = 4;
    var spliced = SpriteSplicer.Splice(renderer, slices, transform.position, transform.localScale, transform.rotation);

    // Destroy current gameeobject
    Destroy(gameObject);
}
```
You should see visually no difference, but your object will be sliced in a grid.
