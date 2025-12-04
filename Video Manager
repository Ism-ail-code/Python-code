import json
def load_data():
  try:
    with open('text.txt', 'r') as file:
  return json.load(file)                                     // will convert the json object into python object
  except (FileNotFoundError ,json.JSONDecodeError):            
    return []

def savedata(videos):
  with open('text.txt', 'w') as file:
    json.dump(videos, file)


def list_video(videos):
  if videos ==[]:
    print("*" * 64)
    print("The list does not contain any video: ")
    print("*" * 64)
    return
  print("*" * 64)
  for index, video in enumerate(videos, start=1):
    print(f"{index}{video['name']} and its duration is  {video['duration']}")
  print("*" * 64)


def add_video(videos):
  name = input("Enter your video name: ")
  duration = input("Enter your video time duration: ")
  videos.append({"name": name, "duration": duration})
  savedata(videos)


def update_video(videos):
  list_video(videos)
  index = int(input("enter the video you want to update: "))
  if 1 <= index <= len(videos):
    name = input("enter the name for new video: ")
    duration = input("Enter the duration for your video: ")
    videos[index - 1] = {"name": name, "time": duration}
    savedata(videos)


def delete_video(videos):
  list_video(videos)
  index = int(input("enter the video you want to delete"))-1
  if 1 <= index <= len(videos):
    del videos[index]

def exit_app():
  print("*"*72)
  print("App exited sucessfully")
  print("*"*72)
  exit()

videos = load_data()



def main():
  while True:
    print("Youtube Manager: ")
    print("1.List all the Youtube videos: ")
    print("2.Add the Youtube Video: ")
    print("3.Update the Youtube Video: ")
    print("4.Delete a Video: ")
    print("5. Exit the App: ")
    choice = input("Enter your  choice number: ")

    #Conditon for the choices
    if choice == "1":
      list_video(videos)

    elif choice == "2":
      add_video(videos)

    elif choice == "3":
      update_video(videos)

    elif choice == "4":
      delete_video(videos)

    elif choice == "5":
      exit_app()
    else:
      print("enter the valid choice: ")


if __name__ == "__main__":
  main()
