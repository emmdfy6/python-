import random
import os

def clear():
    os.system('cls' if os.name == 'nt' else 'clear')

def print_header(text):
    print("\n" + "=" * 50)
    print(f"🎮 {text} 🎮")
    print("=" * 50)

def game_guess():
    clear()
    num = random.randint(1, 20)
    tries = 0
    print_header("حدس عدد")
    print("💡 بین 1 تا 20 حدس بزن")
    while True:
        guess = input("👉 عددت رو بگو (یا 'خروج'): ")
        if guess == "خروج":
            break
        try:
            guess = int(guess)
        except:
            print("❌ فقط عدد وارد کن!")
            continue
        tries += 1
        if guess == num:
            print(f"🎉 برنده شدی در {tries} تلاش!")
            input("\n🔹 Enter بزن تا برگردی...")
            break
        elif guess < num:
            print("📈 برو بالا")
        else:
            print("📉 بیا پایین")

def game_rps():
    clear()
    choices = ["سنگ", "کاغذ", "قیچی"]
    score_user = 0
    score_pc = 0
    print_header("سنگ-کاغذ-قیچی")
    while True:
        pc = random.choice(choices)
        user = input("\n👉 انتخاب کن (سنگ/کاغذ/قیچی یا 'خروج'): ")
        if user == "خروج":
            print(f"\n🏆 امتیاز نهایی: تو {score_user} - کامپیوتر {score_pc}")
            input("\n🔹 Enter بزن تا برگردی...")
            break
        if user not in choices:
            print("❌ فقط سنگ/کاغذ/قیچی بنویس!")
            continue
        print(f"\n🧑 تو: {user}  |  💻 کامپیوتر: {pc}")
        if user == pc:
            print("🤝 مساوی!")
        elif (user == "سنگ" and pc == "قیچی") or \
             (user == "کاغذ" and pc == "سنگ") or \
             (user == "قیچی" and pc == "کاغذ"):
            print("✅ برنده شدی! +1 امتیاز")
            score_user += 1
        else:
            print("❌ باختی! کامپیوتر +1 امتیاز")
            score_pc += 1

# منوی اصلی
while True:
    clear()
    print("\n" + "🌟" * 25)
    print("🎮  خوش آمدی به بازی‌های پایتون  🎮")
    print("🌟" * 25)
    print("\n📌 1️⃣  حدس عدد")
    print("📌 2️⃣  سنگ-کاغذ-قیچی")
    print("📌 3️⃣  خروج از بازی")
    print("\n" + "-" * 50)
    
    choice = input("👉 شماره بازی رو انتخاب کن: ")
    
    if choice == "1":
        game_guess()
    elif choice == "2":
        game_rps()
    elif choice == "3":
        clear()
        print("\n" + "❤️" * 20)
        print("🙋 خدانگهدار! موفق باشی!")
        print("❤️" * 20 + "\n")
        break
    else:
        print("❌ فقط 1، 2 یا 3 وارد کن!")
        input("🔹 Enter بزن تا دوباره تلاش کنی...")