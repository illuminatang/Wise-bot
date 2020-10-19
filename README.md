# Wise-bot
print("Title of program: Wise bot")
print()
while True:
  description = input("Could you describe how you feel in a sentence?")

  list_of_words = description.split()

  feelings_list = []
  encouragement_list = []
  counter = 0
  
  for each_word in list_of_words:
    
    if each_word == "sad":
      feelings_list.append("sad")
      encouragement_list.append("You should not ignore this. Normally, negative emotion is a reminder of what you lack at, instead of looking at the bright side, try to look for your own doubts, doubts about emotions, doubts about life. Sadness, its a important feedback mechanism in life, slowly, your life can improve, not only does hapiness stems from solving problems, but you also improve yourself, learning from your past mistakes, and that is where true learning comes.")
      counter += 1
    if each_word == "happy":
      feelings_list.append("happy")
      encouragement_list.append("Happiness. It comes from solving problems, therefore, it is a form of activity. It is a problem. What we feel is pleasure, a side effect of happiness, pleasure itself is just a form of high, a high that we take to avoid problems. Happiness, it is a consant work in progress, since it is the human nature to be discontented, happiness was never a destiny, but it is part of our struggle. We struggle to achieve happiness, it builds the foundation of our next day problems.")
      counter += 1
    if each_word == "tired":
      feelings_list.append("tired")
      encouragement_list.append("you are stronger than you think")
      counter += 1

  if counter == 0:
    
      output = "Sorry I don't really understand. Please use different words?"

  elif counter == 1:
    
      output = "It seems that you are feeling quite " + feelings_list[0] + ". However, do remember that "+ encouragement_list[0] + "! Hope you feel better :)"  

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
