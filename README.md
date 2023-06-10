# Redirecting-the-scene

## Aim:
To Redirecting the scene in the unity engine.

## Algorithm:
Step 1:
To open the unity engine.

Step 2:
Create a new plane and create a cube and give color for the cube.

Step 3:
Next create sphere in the orgin and change the z-axis and Give the color for the sphere.

Step 4:
Create a tag for the Sphere and Make the sphere and cube as a Rigidbodies and Make the sphere use Gravity.

Step 5:
Create the C# script file in the Assets and write the Coding for the Redirecting to the page2 after hit the sphere to cube.

Step 6:
Next Create a another new scene named as page2.

Step 7
In File->Build settings and drop the both first scene and page2 scene in the Scenes in build setting.

Step 8:
Click the Build and run button in the Build settings and run the scene.

Step 9:
The Sphere after touching the cube it will disappeared and Press the key [R] the redircting to the new scene that is page2.
## Program:
~~~
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;
public class hello : MonoBehaviour
{
    Rigidbody rb;
    // Start is called before the first frame update
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }
    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("lev2");
        }
    }
    private void OnCollisionEnter(Collision collision)
    {
        if (collision.gameObject.tag == "sphere") ;
            Destroy(collision.gameObject);
    }
}
~~~

## Output:
## Scene before Ball hits the Cube:
![image](https://user-images.githubusercontent.com/94187572/204089884-aecceecb-fe28-4619-aeff-8efdf56d3190.png)
## Scene after the Ball hits the Cube:
![image](https://user-images.githubusercontent.com/94187572/204089901-f5b2c3f5-2b49-4952-8b90-a966de11c9f4.png)
## Redirected Scene:
![image](https://user-images.githubusercontent.com/94187572/204089920-64749301-1e9c-4a08-9709-fe20558eb8fb.png)




## Result:
The above C# coding is successfully redirecting the scene in the unity engine.
