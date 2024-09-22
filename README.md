# Dreamer
A UE5 game based on fast paced movement with an open procedural level design.

## Movement System
You are able to run, walk and crouch with one procedural animation. The movement system also includes wall running, jumping/super jump, sliding and dodging.

![ezgif-7-b5b0621a94](https://github.com/user-attachments/assets/7619d05e-b12b-4505-9155-7ed1b8e7c860)
![ezgif-7-ab404f1b81](https://github.com/user-attachments/assets/8570e488-c533-495d-8eec-422bfc4cc3be)
![ezgif-7-d314ac4f7d](https://github.com/user-attachments/assets/c5ce14db-82df-4526-ba53-0cfc68a94095)
![ezgif-7-bfffee9d2f](https://github.com/user-attachments/assets/8747117b-b98e-4579-a648-261311ac5d53)
![ezgif-7-f68d485a07](https://github.com/user-attachments/assets/7dea635b-d4ff-4faf-8ea4-3affd2b5ebd8)
the super jump launches you in which ever direction you are facing


This is the entire logic behind the movement, this includes interupting proccesses (e.g. sliding into walking or super jump)
![Screenshot 2024-09-22 201128](https://github.com/user-attachments/assets/1391eca9-bee2-42e7-8b0d-90c649567679)
![Screenshot 2024-09-22 201203](https://github.com/user-attachments/assets/9663188b-170a-4c13-8993-fb14679af974)
![Screenshot 2024-09-22 201217](https://github.com/user-attachments/assets/1fdb15dc-2bf3-454d-9bbe-d124d348b007)
![Screenshot 2024-09-22 201232](https://github.com/user-attachments/assets/2a54eb7c-797d-4b65-a856-0bdc809ea5a3)

This section moves the camera to avoid it intersecting with a wall, it's also used to create a forward vector for wall running by storing a vector of what side has hit a wall
![Screenshot 2024-09-22 201243](https://github.com/user-attachments/assets/079f4286-aca1-48ba-80fa-d71f1dacce5c)

## Character Customization

 With the character customizer, you can change the shape of your face with morph targets, the colour of you skin and your hair (Head, beard, moustache, eyebrows and lashes)

An example of Changing morphs:
![ezgif-2-9831f5dde4](https://github.com/user-attachments/assets/477c823d-4d62-41d0-8bc9-4616f538badb)


Loading morphs to the character:
![Screenshot 2024-09-22 193540](https://github.com/user-attachments/assets/877e2331-f0b0-4c83-8756-be563c626f79)
If you already have a character made, this changes the sliders to the correct value so that when you change them, everything is correct.


How i change the morph target:
![Screenshot 2024-09-22 193900](https://github.com/user-attachments/assets/07e77130-6888-4ef1-b7c9-6714b474e621)


The widget system is split up into their own sub componants. This allows for easy editing and clarity when making changes
![Screenshot 2024-09-22 194018](https://github.com/user-attachments/assets/399862f3-d975-4cde-a28e-6d5a108180f8)


When it comes to saving, i go through seperate fungtions which writes to a file the values of morph taregets and notes the used hair + its binding, as well as the colours used for skin/hair/eyes
![Screenshot 2024-09-22 194358](https://github.com/user-attachments/assets/a6912f3a-36d5-49b7-b5ee-53801b1c0db5)
![Screenshot 2024-09-22 194223](https://github.com/user-attachments/assets/b5798e8d-91de-4fac-8546-cd7834988557)
![Screenshot 2024-09-22 194528](https://github.com/user-attachments/assets/740d0845-773a-42e2-b8ba-cb1d46d2b203)
![Screenshot 2024-09-22 194555](https://github.com/user-attachments/assets/13adce66-84bc-466f-851e-6476bd176cea)

### Colour Picker
As UE doesn't have a colour picker widget, i had to create my own. I did this by using a 2D slider to give an x and y position, 
using that vector to zoom into a colour spectrum to provide a colour

![Screenshot 2024-09-22 195807](https://github.com/user-attachments/assets/ab4535cd-fb41-4950-994b-9a607e5b4f7e)

The slider the right allows for you to change the brightness of the same colour by adjusting only the y value of the 2D slider


When you select a colour it changes a value of a material parameter. The material parameter isn't used for its colour but because it can be used to store up to 4 values of which we use 3 (r = x, g = y, b = toggle)
![Screenshot 2024-09-22 195435](https://github.com/user-attachments/assets/1867c48f-8399-4e19-9635-7f04c642e1ea)
![Screenshot 2024-09-22 200202](https://github.com/user-attachments/assets/f66f2add-8fa9-40ef-baf4-067a363ef7a1)

Implimenting the colour picker is as simple as putting the material function in and the material parameter that holds the values you want
![Screenshot 2024-09-22 200753](https://github.com/user-attachments/assets/70bcb03f-9802-4d2d-a5bf-c1c4168fbcbf)
