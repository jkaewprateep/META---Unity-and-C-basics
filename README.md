# META - Unity and C# basics
META - Unity and C# basics

<p align="center" width="100%">
    <img width="45%" src="https://github.com/jkaewprateep/META---Unity-and-C-basics/blob/main/AR%20instructors.png">
    <img width="17.5%" src="https://github.com/jkaewprateep/META---Unity-and-C-basics/blob/main/versus.jpg">  
    <img width="13.2%" src="https://github.com/jkaewprateep/META---Unity-and-C-basics/blob/main/image22.jpg">  
    <img width="16.1%" src="https://github.com/jkaewprateep/META---Unity-and-C-basics/blob/main/kid_24.jpg"> </br>
    <b> Pictures from the Internet </b> </br>
</p>

[.NET FullStack Developer Specialization ]( https://github.com/jkaewprateep/Portfolio/blob/main/Coursera%206DRYK7YS79ZT.pdf ) </br>
[Meta AR Developer Professional Certificate]( https://github.com/jkaewprateep/Portfolio/blob/main/Coursera%20T9ZTYYSXGY5H.pdf ) </br>
[Google UX Design Specialization]( https://coursera.org/share/15f48b13d33cefb8686c2bcca579d6a8 ) </br>

### PlayerController.cs ###

```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlayerController : MonoBehaviour
{
    // Private Variables
    private float speed = 5.0f; 
    private float turnSpeed = 25.0f;
    private float horizontalInput; 
    private float forwardInput;
    // Start is called before the first frame update
    void Start()
    {

    }

    // Update is called once per frame
    void Update()
    {
        // This is where we get player input
        horizontalInput = Input.GetAxis("Horizontal");
        forwardInput = Input.GetAxis("Vertical");
        // We move the vehicle forward
        transform. Translate (Vector3. forward * Time.deltaTime * speed * forwardInput);
        // We turn the vehicle
        transform.Rotate(Vector3.up, Time.deltaTime * turnSpeed * horizontalInput);
    }
}
```

### PlayerController.cs - time delta ###

```
public class PlayerController2 : MonoBehaviour
{
    // Update is called once per frame
    void Update()
    {
        transform.Translate(Vector3.forward * Time.deltaTime * 21);        
    }
}
```

### PlayerController.cs - parameterizes ###

```
public class PlayerController3 : MonoBehaviour
{
    public GameObject player;
    private Vector3 Offset = new Vector3(0, 5, -7);

    // Update is called once per frame
    void Update()
    {
        // Offset the camera behide the player by adding the player locations;
        transform.position = player.transform.position + Offset;
    }
}
```

### Rotation.cs - custom action - vector ###

```
public class PlatformRotate : MonoBehaviour { 

    public Vector3 rotateChange;

    // Start is called before the first frame update
    void Start()
    {
    
    }

    // Update is called once per frame
    void Update()
    {
        transform.Rotate (rotateChange); 
    }
}
```

### Default.cs - custom action - position ###

```
public class TrackPosition : MonoBehaviour {
    
    public Vector3 positionChange;

    // Start is called before the first frame update
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        transform.position += positionChange;
    }
}
```

### AlignObjects.cs - custom action - transform position ###

```
public class AlignObjects: MonoBehaviour
{
    public GameObject[] objectsToAlign; 
    public float spacing = 1;

    // Start is called before the first frame update
    void Start()
	{
        for (var i = 0; i < objectsToAlign.Length; i++)
            {
                objectsToAlign[i].transform.position = new Vector3(i* spacing, 0, 0);
            }
    }
}
```

### BulletCreator.cs - custom action - key space ###

```
public class BulletCreator : MonoBehaviour
{
    public GameObject bullet;

    void Start()
    {
        Invoke("ShootBullet", 2);
    }
    void ShootBullet()
    {
        var newBullet = Instantiate(bullet);
        newBullet.transform.position = new Vector3(0, 10, 0);
        Destroy(newBullet, 5);
    }
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space))
        {
            ShootBullet();
        }
    }
}
```

### DestroyOnClick.cs - custom action - destroy object - key space ###

```
public class DestroyOnClick : MonoBehaviour
{
    void OnMouseDown()
    {
        Destroy(gameObject);
    }
}
```

### ExampleBehaviourScript.cs - custom action - change property - key space ###

```
public class ExampleBehaviourScript : MonoBehaviour
{
    // Update is called once per frame
    void Update()
    {
        {
            if (Input.GetKeyDown(KeyCode.R))
            {
                GetComponent<Renderer>().material.color = Color.red;
            }
            if (Input.GetKeyDown(KeyCode.G))
            {
                GetComponent<Renderer>().material.color = Color.green;
            }
            if (Input.GetKeyDown(KeyCode.B))
            {
                GetComponent<Renderer>().material.color = Color.blue;
            }
        }
    }
}
```

### Movement.cs - custom action - change position - key space ###

```
public class Movement : MonoBehaviour
{
    public float speed;

    // Update is called once per frame
    void Update()
    {
        var pos = transform.position;

        if (Input.GetKey(KeyCode.LeftArrow))
        {
            pos.x = pos.x - speed * Time.deltaTime;
        }
        if (Input.GetKey(KeyCode.RightArrow))
        {
            pos.x = pos.x + speed * Time.deltaTime;
        }
        if (Input.GetKey(KeyCode.UpArrow))
        {
            pos.y = pos.y + speed * Time.deltaTime;
        }
        if (Input.GetKey(KeyCode.DownArrow))
        {
            pos.y = pos.y - speed * Time.deltaTime;
        }

        transform.position = pos;
    }
}
```
