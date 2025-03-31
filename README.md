# IRCTC Tatkal Ticket Booking Automation

This repository provides a semi-automated script to assist in booking Tatkal tickets on [IRCTC](https://www.irctc.co.in) using Google Chrome. The script helps fill in login details, passenger information, and journey details to speed up the booking process.

## Features
- Auto-fills login credentials.
- Auto-fills passenger details.
- Reduces manual input time during Tatkal booking.

## Limitations
- **Not fully automated**: You will need to manually solve the Captcha, select the train, and complete the payment process.

## Prerequisites
- Google Chrome browser installed.
- ChromeDriver corresponding to your Chrome version.
- Python installed with the required dependencies.

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/nevatia/TATKAL.git
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Set up login credentials in `login.json`:
   ```json
   {
       "USERNAME": "xxxxxxxxxxx",
       "PASSWORD": "xxxxxxxxx"
   }
   ```
4. Enter passenger and travel details in `passenger_details.json`:
   4. Enter passenger and travel details in `passenger_details.json`:
   ```json
   {
       "TRAVEL_DATE": "01/04/2025",
       "SOURCE_STATION": "NDLS",
       "DESTINATION_STATION": "HWH",
       "MOBILE": "9898989898",
       "PASSENGER_DETAILS": [
           {
               "NAME": "VIRAT KOHLI",
               "AGE": 40,
               "GENDER": "Male",
               "SEAT": "No Preference",
               "FOOD": "No Food"
           },
           {
               "NAME": "ANUSHKA KOHLI",
               "AGE": 36,
               "GENDER": "Female",
               "SEAT": "No Preference",
               "FOOD": "No Food"
           }
       ],
       "__valid_coaches__": "SL | 2A | 3A | 3E | 1A | CC | EC | 2S",
       "__valid_seats__": "Lower | Middle | Upper | Side Lower | Side Upper | Window Side | No Preference",
       "__valid_genders__": "Male | Female | Transgender",
       "__valid_food_choices__": "Veg | Non Veg | No Food"
   }
   ```


## Usage
1. Run the script:
   ```sh
   python sanju_Tatkal_booking.py
   ```
2. The script will open Chrome, navigate to IRCTC, and fill in login details.
3. Manually solve the Captcha and select the train.
4. The script will auto-fill passenger details.
5. Manually proceed with payment to complete the booking.

## Disclaimer
This script is intended for educational purposes only. Use at your own risk. We are not responsible for any misuse or violations of IRCTC's terms and conditions.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

