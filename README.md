import random


def guess_number_game():
    number_to_guess = random.randint(1, 100)

    guesses = 0

    print("欢迎来到猜数字游戏！")
    print("我已经想好了一个1到100之间的数字，你能猜到吗？")

    while True:
        guess = input("请输入你的猜测：")

        if not guess.isdigit():
            print("请输入一个有效的数字！")
            continue

        guess = int(guess)

        guesses += 1

        if guess < number_to_guess:
            print("太小了！再试一次。")
        elif guess > number_to_guess:
            print("太大了！再试一次。")
        else:
            print(f"恭喜你，你猜对了！数字是 {number_to_guess}。")
            print(f"你一共猜了 {guesses} 次。")
            break
