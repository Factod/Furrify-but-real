import keyboard
import random
# change the phwases if  meow :3 you want...
fur_suffixes = [" rawr~", " mrrrph~~", " meow :3", " uwu", " >w<", " OwO", " *blushes*", " -w-"]

# speaking fow  *blushes* it sewf
replacements_en = {
    'r': 'w', 'R': 'W', 
    'l': 'w', 'L': 'W'
}

extra_mode = False

def toggle_extra():
    global extra_mode
    extra_mode = not extra_mode
    print(f"phrases :3 : {'onnn owo' if extra_mode else 'off TwT'}")

keyboard.add_hotkey('ctrl+i', toggle_extra)

def on_key(event):
    # wepwacments
    if event.name in replacements_en and not keyboard.is_pressed('ctrl'):
        keyboard.press_and_release('backspace')
        keyboard.write(replacements_en[event.name])
    
    # adding phwasses
    elif event.name in ['space', 'enter'] and extra_mode:
        if random.random() < 0.25:
            if event.name == 'enter':
                keyboard.press_and_release('backspace')
                keyboard.write(random.choice(fur_suffixes))
                keyboard.press_and_release('enter')
            else:
                keyboard.write(random.choice(fur_suffixes) + " ")

keyboard.on_press(on_key)
print("mewooo :3 (Ctrl+I for phrases)")
keyboard.wait()
