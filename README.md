# Dreamer
A UE5 game based on fast paced movement with an open procedural level design.

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
As UE doesn't have a colour picker widget, i had to create my own. I did this by using a 2D slider to give an x and y position, using that vector to zoom into a colour spectrum to provide a colour
![Screenshot 2024-09-22 195807](https://github.com/user-attachments/assets/ab4535cd-fb41-4950-994b-9a607e5b4f7e)
The slider the right allows for you to change the brightness of the same colour by adjusting only the y value of the 2D slider


When you select a colour it changes a value of a material parameter. The material parameter isn't used for its colour but because it can be used to store up to 4 values of which we use 3 (r = x, g = y, b = toggle)
![Screenshot 2024-09-22 195435](https://github.com/user-attachments/assets/1867c48f-8399-4e19-9635-7f04c642e1ea)
![Screenshot 2024-09-22 200202](https://github.com/user-attachments/assets/f66f2add-8fa9-40ef-baf4-067a363ef7a1)
