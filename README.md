# Exam-Motivation-bot
print("Title of program: Exam motivation bot")
print()
while True:
  description = input("Could you describe how you feel in a sentence?")

  list_of_words = description.split()

  feelings_list = []
  encouragement_list = []
  counter = 0
  
  for each_word in list_of_words:
    
    if each_word == "bored":
      feelings_list.append("bored")
      encouragement_list.append("revise your studies")
      counter += 1
    if each_word == "enjoying":
      feelings_list.append("enjoying")
      encouragement_list.append("keep up the good work")
      counter += 1
    if each_word == "results":
      feelings_list.append("results")
      encouragement_list.append("do your best")
      counter += 1
    if each_word == "stuck":
      feelings_list.append("stuck")
      encouragement_list.append("consult a teacher or your friends")
      counter += 1
    if each_word == "tired":
      feelings_list.append("tired")
      encouragement_list.append("take a short break")
      counter += 1
    if each_word == "stressed":
      feelings_list.append("stressed")
      encouragement_list.append("calm down and take a short break")
      counter += 1
    if each_word == "worried":
      feelings_list.append("worried")
      encouragement_list.append("do your best")
      counter += 1

  if counter == 0:
    
      output = "Sorry I don't really understand. Please use different words?"

  elif counter == 1:
    
      output = "It seems that you are feeling quite " + feelings_list[0] + ". However, do remember to "+ encouragement_list[0] + "! Hope you feel better :)"  

  else:

    feelings = ""    
    for i in range(len(feelings_list)-1):
      feelings += feelings_list[i] + ", "
    feelings += "and " + feelings_list[-1]
    
    encouragement = ""    
    for j in range(len(encouragement_list)-1):
      encouragement += encouragement_list[i] + ", "
    encouragement += "and " + encouragement_list[-1]

    output = "It seems that you are feeling quite " + feelings + ". Please always remember "+ encouragement + "! Hope you feel better :)"

  print()
  print(output)
  print()
