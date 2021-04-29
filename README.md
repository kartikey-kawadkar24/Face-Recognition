The main aim of this project is not only to identify the faces but also give labels
associated with it while reading the same face again in real-time after training the
model.

Face Recognition systems have many applications but the most commonly used application
is the attendence system used in manufacturing plants/companies.

So, here we have used a simple "Face Recognition" library developed by Google.
Instead of taking some pre-defined dataset, we can create our own dataset by reading the
faces and storing it in a pickle file along with its label name. This works as a key-value
pair dictionary where key is the face stored in one file and value is the label associated
with it stored in other file.

The faces are read at different angles so while testing the model on real time data base,
if the face is tilted or shifeted by a few degrees, then the offset should not create any
issue while detection.

Once the faces at different angles are captured, we try to find the location and outline
of the faces to extract the co-ordinates of each face.

These features or co-ordinates obtainted are encoded so it can be compared with the other
faces to see if it matches or not.

Hence we have 2 files, one with the information of face like encodings, locations,
co-ordinates and angles and other with label and index value to differentiate the label
from one face to another.

So, finally when we show a face to the camera, the library tries to read the co-ordinates, 
compares them with the stored data, and tries to match with it. If the compared information
matches then the face is bounded with a box with the label assigned to it.
