# Ex06-Redirecting-the-Scene
## Aim:
To Redirecting the scene in the unity engine.

## Algorithm:
### Step 1: 
To open the unity engine.

### Step 2: 
Create a new 3D project.

### Step 3: 
Create plane and name it as ground and create cube and name it as player.

### Step 4: 
Add WinText in Hierarchy.

### Step 5: 
Create a C# Script and name it as playercontroller and add the script to player.

### Step 6: 
Use the R button to change the level2

### Step 7:
Print the Output and end the program.

## Program:
Name: Vinush.CV

Reg no: 212222230176

```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class playercontroller : MonoBehaviour
{
    // Start is called before the first frame update
    Rigidbody rb;
    public GameObject WinText;
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("Level2");
        }
    }
    private void OnMouseDown()
    {
        Destroy(gameObject);
    }
    private void OnCollisionEnter(Collision collision)
    {
        if (collision.gameObject.tag == "sphere")
        {
            Destroy(collision.gameObject);
            WinText.SetActive(true);
        }
    }
}
```
## OUTPUT:
![image](https://github.com/vinushcv/Ex06-Redirecting-the-Scene/assets/113975318/21584574-acc0-432d-ad9c-dfe49a191836)



![image](https://github.com/vinushcv/Ex06-Redirecting-the-Scene/assets/113975318/808900f4-da9d-43b2-a9eb-03912582bb14)


## RESULT:
The above C# coding is successfully redirecting the scene in the unity engine.

