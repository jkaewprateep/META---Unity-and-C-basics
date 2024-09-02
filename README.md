# META - Unity and C# basics
META - Unity and C# basics

<p align="center" width="100%">
    <img width="45%" src="https://github.com/jkaewprateep/META---Unity-and-C-basics/blob/main/AR%20instructors.png">
    <img width="17.5%" src="https://github.com/jkaewprateep/META---Unity-and-C-basics/blob/main/versus.jpg">  
    <img width="13.2%" src="https://github.com/jkaewprateep/META---Unity-and-C-basics/blob/main/image22.jpg">  
    <img width="16.1%" src="https://github.com/jkaewprateep/META---Unity-and-C-basics/blob/main/kid_24.jpg"> </br>
    <b> Pictures from the Internet </b> </br>
</p>

</br>

[.NET FullStack Developer Specialization ]( https://github.com/jkaewprateep/Portfolio/blob/main/Coursera%206DRYK7YS79ZT.pdf ) </br>
[Meta AR Developer Professional Certificate]( https://github.com/jkaewprateep/Portfolio/blob/main/Coursera%20T9ZTYYSXGY5H.pdf ) </br>
[Google UX Design Specialization]( https://coursera.org/share/15f48b13d33cefb8686c2bcca579d6a8 ) </br>

</br>

🧸💬 Similar to model and data visualization augmented reality is one technology for transferring learning knowledge, experience, entertainment, and user interaction feedback into reachable and adaptive media. In image processing and data science, augmented reality utilizes the same data by applying augment functions to make it similar or different and have good effects on machine learning or learners. In AR, the object or model can be applied by the mathematical function to create a visualization experience and better effects in communications and entertainment. </br>
👧💬 🎈 If the data model generates of vector image then data augmenting is to create rotation, scales, axis and alignment, colours, similarity and contrast, and physical property of the vector image applied by scales that provide good effects for the learner. In the lesson, we will see examples of rendering models with materials property and physical property applying custom functions to create effects of physical location change, collision effects, bouncing, random spawns, change in property and instance, and removing objects with provided effects and entertainments. </br>

<p align="center" width="100%">
    <img width="45%" src="https://github.com/jkaewprateep/META---Unity-and-C-basics/blob/main/web01.png">
    <img width="45%" src="https://github.com/jkaewprateep/META---Unity-and-C-basics/blob/main/web02.png">
    <img width="45%" src="https://github.com/jkaewprateep/META---Unity-and-C-basics/blob/main/web03.png">
    <img width="45%" src="https://github.com/jkaewprateep/META---Unity-and-C-basics/blob/main/web04.png"> </br>
</p>

🐑💬 ➰ Heart beating with physical property and creating games using AR by Unity program possible with the provided tools and C# programming languages but you need to know the basics of class inheritance programming styles because the AR development platform will utilize of user create objects and render for the same screen rendering. </br>
🐐💬 Applying effects, gravity and boundary of the image or collisions creates games and simulation development environments where you can specific mass, position, and axis of the object to start the collision effects when there are one or more objects in the same screen aligned or pass-though the target collision axes and position. </br>

### PlayerController.cs ###

🐑💬 ➰ By the public variable allows parameters for the class variable to reuse the same variable inside the class and utilize the effects, private variables are similar to the same rules and ```C# language programming``` . </br>
🦭💬 There are rotation axis measurements and similar axis measurements for object description and Unity provided ```transform functions``` to perform rotation axis and similar axis. Continuous movement can use a time ticker or physical force apply. </br>
🧸💬 The rotation axis is easy to use with an angle while the symmetric axis is easy to use with the position then the ```transform functions``` is very useful you can work without converting values between these two axises. </br>

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

🐑💬 ➰ Continuous movement by ```time delta``` and the ```speed``` effects on the rotation axis forward, make the object model rotate moving forward with the speed effect provided and the class can change the direction of the object ```forward``` and ```backward``` . </br>
🧸💬 The ```time delta``` is a good object for continuous actions, Unity allows to use of the time delta anywhere or from import reference and instance but as a symmetric axis and original source on the screen the object they are working on the same time scalings. </br>
🦭💬 The ```Vector3``` is a vector-like property of the object and contains useful functions where you can work with communication words forward, backward, rotation etc. </br>

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

🐑💬 ➰ By ```GameObject``` is related to the object of the script or the custom class of action assigned to and simply applies the new position by using the ```transform functions``` . </br>
🐯💬 The ```Offset``` is one way to apply the effects and you can create multiple Offset values and make them as matrix apply for the same type of effects and share between objects or create a script file of the effect that can be reused in the project. There is ```traditional INFO``` where the same type of object behavior is the same as in the project and ```culture INFO``` where a similar type of object provides the same effects as import components and the object can be reused overall the projects. </br>
🦁💬 Effects of the object same as class property and materials property are protected the same as the object and its effects within the same and outside domain. Applying the same object in different projects or domains may create different effects but the ```original domain effects``` are the most potential of the object property even the development domain creates wider effects. </br>
🐐💬 When there are multiple domains the model object is also the same as the data model we determine the effect of the original domain but if there is a specialization of the different domains that is significant that is individual domain effects. As the ```individual domain effects``` properties are preserved but the effects is selected by the domain controller and designer to use and normally bug and effects enchantment will work on the original domain and if updated, and create wider effects that need to be performed on specific domains separately. Copied of the object model to run in a specific domain that is not original is not covered by the design but protected by the original idea. Copied of the programming running on the target-specific domain that the program owner had intentionally built, they are hardworking but intentionally only when it ```works on a specific domain``` . ( Working on the specific version of the program or fixing bugs then ```ES - essential patch``` is sometimes called intentional and do not mess with the sentence we apply intentionally. It does not mean we create bugs to fix. </br>

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

🐑💬 ➰ Rotation action on the rotation domain is applied ```degrees``` or ```angular degrees``` by its method otherwise uses a transformation function. </br> 
🧸💬 Working with drawings subject object rotation on itself is easy just by the ```rotation function``` but object rotation by axis requires a bit of technique by creating a new coordinate and transforming to the new coordinate. </br> 
🦭💬 In programming when referring to data models or data model objects you can reference a larger data model and specify the specific property the same as the object you merge as the model object internally used within the project. The project will easily apply external program logic or simulation problems because they support both symmetric axis and rotation axis, input as the matrix can be converted using the transform function to the vector object as required by the objective. ```Machine learning```, ```feedback systems```, and ```data communications``` project communication protocols provide output signalings as numerics in matrixes sizes specific or logits shape that is the adaptive method to create simulation from the output of the process same as ```PyGame```, ```Gyms```, and other ```simulation environment``` for machine learning and games. </br> 

```
public class PlatformRotate : MonoBehaviour { 

    public Vector3 rotateChange;

    // Update is called once per frame
    void Update()
    {
        transform.Rotate (rotateChange); 
    }
}
```

### Default.cs - custom action - position ###

🐑💬 ➰ Position axis action by incremental of the position value by its symmetric domain. </br> 
👧💬 🎈 Incremental support when testing the object is originals by the environment using the games environment functions without opening into the class method working is create the incremental function when they are a response to the same environment input and they are limited their action into the boundary, not distracted or create none aligned of reference in the game's environment and they are not left of the environment by the extreme functions they can contain within the environment. ```Objects need to be contained within the environment``` . </br> 
🐯💬 Visually are the objects aligned with the ```traditional-INFO as references``` object in the environment⁉️ </br> 
🦁💬 By the object of the environment, source of light, and provided in the science, vertical and horizontal axis we can create a function to determine object enter into the environment. If the object is not aligned with the environment can create effects on users or users create an effect that considers a material object. </br> 
👧💬 🎈 Example cheating items in-game environment does it prohibited⁉️ </br> 
🦁💬 Needs to be decided by the game admin and users because that is not aligned with the game's story and the game's tradition. </br> 

```
public class TrackPosition : MonoBehaviour {
    
    public Vector3 positionChange;

    // Update is called once per frame
    void Update()
    {
        transform.position += positionChange;
    }
}
```

### AlignObjects.cs - custom action - transform position ###

🐑💬 ➰ Transformation is the application of the simple input objects and their effects. </br> 
🦭💬 Array-like property support for the object of the game helps about create programming iteration or programming logic application apply and support of array-like object property is dedicated collection property and create support inheritance method as using ```C# language``` . </br> 
🐯💬 Working ```APIs``` level ```culture-INFO``` need to provide an inherited class-like object that supports collections method, references description, numeric data and description, and function return and ops-codes to submitted. </br> 
🦁💬 That is because users have many levels and they need to access the same resources, the API needs to create and handle support to them with possible methods designed by the API and working function algorithms. </br> 

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

🐑💬 ➰ Create functions for the model object effects that can recall overall the project. </br> 
🧸💬 Collection of actions or effects can create as a method function when it can call from an application or working process class object that can save the actions method as they are named as function name or you can name them like ```snowflakes``` or ```ShootBullet``` .</br> 

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

🐑💬 ➰ Remove the object from the domain. </br>
🐐💬 ➰ Unity build function Destroy for the AR object then you do not need to dispose or create a dedicated function, AR works well in the visualization object and priority tasks ordering even using a bit of computation power. </br>
🦭💬 There is a hidden truth about the programming we are reading the object on the scene and interacting or directly applying effects we create and need visualization update the ```destroy``` function is a create function that helps update render object results that are faster than iterations update by each item on the scene that is some examples of create function useful from AR. </br>

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

🐑💬 ➰ Accepted the key press and performed actions by its conditions to create better effects, change of the object property and render display determined by the ```user key press interactions``` . </br>
🐯💬 Touch and absolute colours that is a working item. </br>
🦭💬 It is ready to use, and they need to have behavior when needed or like ```m&M``` they are selling by the software application working when needed and the function will not automatically call by the assignment logic same as the snacks candy. </br>

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

🐑💬 ➰ Keypress conditions apply position effect with time and velocity speed, parameterized speed variable. </br>
🦭💬 The ```Rational buttom``` is add 0.5 dimension by the delay-time pressing work widely and famous and at the beginning of smart mobile phones introduce the games created to support rational button control that makes for the smaller mobile device is a good user experience that they need to create a desire to the action and many games released to the support of the same idea and application when competitive platform define of full control set of user input that is for working as computer plam on hand. </br>
🦭💬 It is rational because it provides ```signals with amplitude``` and famous encapsulated into a range number decimal and float for computing and communication processes. </br>

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

### Movement.cs - custom action - visibility - key space ###

🐑💬 ➰ Visibility affects application from user keypress interactions. </br>
👧💬 🎈 Visibility is one tool because we use observation for the objects or players when they have visibility and observation at the same level we can make objects visible they can interact or they can observe makes us different than users where we are not created of new object and balance of the game tradition. </br>
🐯💬 Monster visibility can be both monster observation ranges and player observation ranges but not over ```spawn rates```. Outscope player observation is none game ```tradition-INFO``` because humans are the game players. </br>
👧💬 🎈 Sometimes I will need to observe the monster ```observation ranges``` to determine as the game's detective they should not see the player or the player should have ```collection items``` drop from the spawns and observation range if they are human. </br>

```
public class RendererEnabler : MonoBehaviour
{
    // Update is called once per frame
    void Update()
    {   
        if (Input.GetKeyDown(KeyCode.Space))
        {
            var renderer = GetComponent<Renderer>();
            renderer.enabled = !renderer.enabled;
        }
    }
}
```

### SphereMaker.cs - custom action - create object - key space ###

🐑💬 ➰ Duplicate object for same property object created with target position on the same domain, ```random function``` create distribution effects of the objects created by this function. </br>

```
public class SphereMaker : MonoBehaviour
{
    public GameObject sphere;
    public int numberOfSpheres = 4;

    // Start is called before the first frame update
    void Start()
    {
        for (int i = 0; i < numberOfSpheres; i = i + 1)
        {
            var duplicateSphere = GameObject.Instantiate(sphere);
            duplicateSphere.transform.position = new Vector3(i, 0, 0);
        }
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetMouseButtonDown(1))
        {
            var duplicateSphere = GameObject.Instantiate(sphere);
            duplicateSphere.transform.position = new Vector3(Random.Range(-4, 4), Random.Range(-4, 4), 0);
            Camera.main.transform.LookAt(duplicateSphere.transform);
        }
    }
}
```

### TestScript.cs - custom action - camera tracking ###

🐑💬 ➰ Camera tracking scripts for object observation or velocity object access the primary object. </br>

```
public class TestScript : MonoBehaviour
{
    public float torque;
    public float velocity;
    public Rigidbody rb;

    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    void FixedUpdate()
    {
        float turn = Input.GetAxis("Horizontal");
        rb.AddTorque(Vector3.up * torque * turn);

        var vertical = Input.GetAxis("Vertical");

        // float turn = Input.GetAxis("Horizontal");
        // rb. AddTorque(Vector3.up * torque * turn);
        // rb.AddForce(Vector3.forward * velocity * vertical);
        rb.AddForce(Camera.main.transform.forward * velocity * vertical);
        rb.AddForce(Camera.main.transform.up * velocity * vertical);
        // rb.AddForce(Camera.main.transform.up * velocity * vertical) 
        // rb.AddForce(Camera.main.transform.forward * velocity * vertical); 
    }
}
```

### ColorChanger.cs - custom action - property change - collisions ###

🐑💬 ➰ The ```collision``` enter effects method by object property changes and rendering. </br>

```
public class ColorChanger : MonoBehaviour
{
    public GameObject spherePrefab;

    void OnCollisionEnter(Collision collision)
    {
        foreach (ContactPoint contact in collision.contacts)
        {
            // var collision_colour = contact.color;
            var collision_point = contact.point;
            var collision_type = contact.normal;
            // var collision_sphere = contact.collider;          
            
            GameObject duplicateSphere = GameObject.Instantiate(spherePrefab);
            //
            var shpere = duplicateSphere.GetComponent<Collider>();
            duplicateSphere.GetComponent<Renderer>().material.color = Color.red;
            // duplicateSphere.collider = collision.collider;


            var colour_code = Random.Range(0, 3);
            switch(colour_code)
            {
                case 0 : GetComponent<Renderer>().material.color = Color.red;
                    break;
                case 1 : GetComponent<Renderer>().material.color = Color.blue;
                    break;
                case 2 : GetComponent<Renderer>().material.color = Color.green;
                    break;
                case 3 : GetComponent<Renderer>().material.color = Color.red;
                    break;
            }        

            // Debug.DrawRay(contact.point, contact.normal, Color.white);
        }
        // if (collision.relativeVelocity.magnitude > 2)
        //     audioSource.Play();
    }
}
```

### DestroyOutOfBounds.cs - custom action - game environment scopes ###

🐑💬 ➰ Range position effects. </br>

```
public class DestroyOutOfBounds : MonoBehaviour
{
    private float topBound = 10;
    private float lowerBound = -10;

    // Update is called once per frame
    void Update()
    {
        if(transfrom.position.z > topBound)
        {
            Destroy(gameObject);
        }

        if(transfrom.position.z < lowerBound)
        {
            Destroy(gameObject);
            Debug.log("Game Over!!!");
        }
    }
}
```

### DetectCollisionsn.cs - custom action - destroy object - collisions ###

🐑💬 ➰ On ```Collider``` event trigger. </br>

```
public class DetectCollisions : MonoBehaviour
{
    private void onTriggerEnter(Collider other)
    {
        Destroy(gameObject);
        Destroy(other.gameObject);
    }
}
```

### MoveForward.cs - custom action - initial speed - parameterizes ###

🐑💬 ➰ Create instance velocity speed movement effects for the assigning object. </br>

```
public class MoveForward : MonoBehaviour
{
    public float speed = 40.0f;

    // Update is called once per frame
    void Update()
    {
        transform.Translate( Vector3.forward * Time.deltaTime * speed );
    }
}
```

### PlayerController.cs - custom action - position transform - parameterizes ###

🐑💬 ➰ Apply the effects of position and rotation. </br>

```
public class PlayerController : MonoBehaviour
{
    public float horizointalInput;
    public float speed = 10.0f;
    public float xRange = 10.0f;
    private float topBound = 10;
    private float lowerBound = -10;

    public GameObject projectilePrefab;

    // Update is called once per frame
    void Update()
    {
        if (transform.position.x < - xRange)
        {
            transform.position = new Vector3( -xRange, transform.position.y, transform.position.z );
        }

        if (transform.position.x > xRange)
        {
            transform.position = new Vector3( xRange, transform.position.y, transform.position.z );
        } 

        horizointalInput = Input.GetAxis("Horizontal");
        transform.Translate(Vector3.right * horizointalInput * Time.deltaTime * speed );
    }
}

```

### SpawnManager.cs - custom action - spawn range positions - parameterizes ###

🐑💬 ➰ Spawn in range of the object animation, rotation, and delay. </br>

```
public class SpawnManager : MonoBehaviour
{
    public GameObject[] animalPrefebs;
    // public int animalIndex;
    private float spawnRangeX = 20;
    private float spawnPosZ = 20;
    private float startDelay = 2;
    private float spawnInterval = 1.5f;

    // Start is called before the first frame update
    void Start()
    {
        InvokeRepeating("SpawnRandomAnimal", startDelay, spawnInterval);
    }

    void SpawnRandomAnimal()
    {
        int animalIndex = Random.Range(0, animalPrefebs.length);
        Vector3 spawnPos = new Vector3(Random.Range(-spawnRangeX, spawnRangeX), 0, spawnPosZ);

        Instantiate(animalPrefebs[animalIndex], spawnPos, animalPrefebs[animalIndex].transform.rotation);
    }
}
```

---

<p align="center" width="100%">
    <img width="30%" src="https://github.com/jkaewprateep/advanced_mysql_topics_notes/blob/main/custom_dataset.png">
    <img width="30%" src="https://github.com/jkaewprateep/advanced_mysql_topics_notes/blob/main/custom_dataset_2.png"> </br>
    <b> 🥺💬 รับจ้างเขียน functions </b> </br>
</p>
