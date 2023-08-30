import random

def number_guessing_game(language):
    target_number = random.randint(1, 100)
    guess_attempts = 5

    if language == "tr":
        print("1 ile 100 arasında bir sayı seçildi. Tahmin edin!")
    elif language == "en":
        print("A number between 1 and 100 has been selected. Guess it!")
    # Diğer diller için benzer if blokları eklenebilir.

    while guess_attempts > 0:
        guess = int(input("Tahmininiz: "))
        guess_attempts -= 1

        if guess < target_number:
            if language == "tr":
                print("Daha yüksek bir sayı tahmin edin.")
            elif language == "en":
                print("Guess a higher number.")
            # Diğer diller için benzer if blokları eklenebilir.
        elif guess > target_number:
            if language == "tr":
                print("Daha düşük bir sayı tahmin edin.")
            elif language == "en":
                print("Guess a lower number.")
            # Diğer diller için benzer if blokları eklenebilir.
        else:
            if language == "tr":
                print("Tebrikler! Doğru tahmin ettiniz. Seçilen sayı:", target_number)
            elif language == "en":
                print("Congratulations! You guessed it right. The chosen number is:", target_number)
            # Diğer diller için benzer if blokları eklenebilir.
            break

        if guess_attempts > 0:
            if language == "tr":
                print("Kalan tahmin hakkınız:", guess_attempts)
            elif language == "en":
                print("Remaining guess attempts:", guess_attempts)
            # Diğer diller için benzer if blokları eklenebilir.
        else:
            if language == "tr":
                print("Tahmin hakkınız kalmadı. Doğru cevap:", target_number)
            elif language == "en":
                print("No more guess attempts left. The correct answer is:", target_number)
            # Diğer diller için benzer if blokları eklenebilir.
