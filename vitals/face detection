import face_recognition
import PIL.Image
import PIL.ImageDraw

input_image = face_recognition.load_image_file("")

face_landmarks = face_recognition.face_landmarks(input_image)
print(face_landmarks[0])

output_image = PIL.Image.fromarray(input_image)
draw = PIL.ImageDraw.Draw(output_image)

landmark = face_landmarks[0].get("left_eye")
for loc in landmark:
    x,y = loc
    draw.rectangle((x, y, x+2, y+2), outline = "blue")

output_image.show()
