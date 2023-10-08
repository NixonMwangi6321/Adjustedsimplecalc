# Adjustedsimplecalc
#SCT211-0698/2022
#NIXON MWANGI GITONGA

import datetime

def calculate_age(birth_year, birth_month, birth_day):
    today = datetime.date.today()
    birthdate = datetime.date(birth_year, birth_month, birth_day)

    age = today - birthdate

    years = age.days // 365
    remaining_days = age.days % 365
    months = remaining_days // 30
    days = remaining_days % 30

    return years, months, days

def age_calculator():
    print("Thisis our adjusted Age Calculator")
    
    user_name = input("Enter your name: ")
    birth_year = int(input("Enter your year of birth: "))
    birth_month = int(input("Enter your birth month (1-12): "))
    birth_day = int(input("Enter your birth day (1-31): "))

    years, months, days = calculate_age(birth_year, birth_month, birth_day)

    print(f"Hello, {user_name}!")
    print(f"Your current age is {years} years, {months} months, and {days} days.")

if __name__ == "__main__":
    age_calculator()

