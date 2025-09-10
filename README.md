# temp

# Program to process a sentence, store results, and read them back

def main():
    # Step 1: Accept a sentence from the user
    sentence = input("Enter a sentence: ")

    # Step 2: Split into words and store in a list
    words_list = sentence.split()

    # Step 3: Convert all words to uppercase and store in a tuple
    words_tuple = tuple(word.upper() for word in words_list)

    # Step 4: Save list and tuple into a file
    with open("sentence_data.txt", "w") as f:
        f.write("List: " + str(words_list) + "\n")
        f.write("Tuple: " + str(words_tuple) + "\n")

    # Step 5: Read back and display
    print("\nData read from file:")
    with open("sentence_data.txt", "r") as f:
        content = f.read()
        print(content)


if __name__ == "__main__":
    main()
