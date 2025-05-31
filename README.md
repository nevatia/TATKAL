# IRCTC Tatkal Ticket Booking Automation

This repository provides a semi-automated script to assist in booking Tatkal tickets on [IRCTC](https://www.irctc.co.in) using Google Chrome. The script helps fill in login details, passenger information, and journey details to speed up the booking process. It needs chrome browser.

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

## Steps to Follow
1. First, modify the `login.json` and `passenger_details.json` files as per your requirements.
2. Run the Python file.
3. It will automatically try to log in to the website and ask for CAPTCHA. AFTER YOU SEE CURSOR IN CAPTCHA INPUT FIELD, CLICK IN FIELD AND ENTER CAPTCHA then press ENTER.
4. After entering the correct CAPTCHA, the script will search for your trains and display a list of available options.
5. Wait for 10 AM and click on the desired **CLASS** (AC3/2/1 tier), then select **DATE**, and finally click **BOOK NOW**.
6. All passenger details will be auto-filled, and you will be taken to the **PAYMENT CAPTCHA** page.
7. Check the ticket details and enter the CAPTCHA.
8. Select your desired **payment option** and complete the payment quickly.
9. The program will wait for **3 minutes** and then exit.

## EXE
Also included EXE folder which contains executable file. No need to install python or other libraries. You only need windows with chrome. Update login and passengers file and run exe.

## Disclaimer
This script is intended for educational purposes only. Use at your own risk. We are not responsible for any misuse or violations of IRCTC's terms and conditions.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

