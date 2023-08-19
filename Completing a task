def add_contact():
    surname = input("Введите фамилию: ")
    name = input("Введите имя: ")
    patronymic = input("Введите отчество: ")
    organization = input("Введите название организации: ")
    work_phone = input("Введите рабочий телефон: ")
    personal_phone = input("Введите личный телефон: ")

    with open("address_book.txt", "a") as file:
        file.write(f"{surname},{name},{patronymic},{organization},{work_phone},{personal_phone}\n")

    print("Контакт успешно добавлен!")

def search_contacts():
    search_term = input("Введите фамилию, имя или организацию для поиска: ")

    with open("address_book.txt", "r") as file:
        contacts = file.readlines()

    found_contacts = []
    for contact in contacts:
        if search_term.lower() in contact.lower():
            found_contacts.append(contact)

    if found_contacts:
        print("Результаты поиска:")
        for found_contact in found_contacts:
            print(found_contact)
    else:
        print("Контакты не найдены.")

def display_contacts():
    with open("address_book.txt", "r") as file:
        contacts = file.readlines()

    if contacts:
        print("Список контактов:")
        for contact in contacts:
            print(contact)
    else:
        print("Справочник пуст.")

def menu():
    while True:
        print("\n-- Адресная книга --")
        print("1. Добавить контакт")
        print("2. Поиск контактов")
        print("3. Показать все контакты")
        print("4. Выйти")

        choice = input("Выберите пункт меню: ")

        if choice == "1":
            add_contact()
        elif choice == "2":
            search_contacts()
        elif choice == "3":
            display_contacts()
        elif choice == "4":
            break
        else:
            print("Неверный выбор. Попробуйте снова.")

menu()
