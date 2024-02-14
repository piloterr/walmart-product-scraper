# Walmart Porudct Information Retrieval Script

## Overview

This Python script is designed to retrieve information about Walmart products using their slugs. It makes use of the Piloterr API to fetch data and stores the results in a JSON file. The script utilizes concurrent programming for efficient processing and includes error handling mechanisms to handle HTTP and request errors.

## Prerequisites

Before running the script, make sure to set up the following:

- Python environment
- Required Python packages: `dotenv`, `requests`, `tqdm`, `termcolor`
- API Token: Obtain an API token from Piloterr and set it in the `.env` file.

## Usage

1. Install the required packages:

```bash
pip install dotenv requests tqdm termcolor
```

2. Set up the API token:

- Create a `.env` file in the script directory.
- Add the following line with your Piloterr API token:

```plaintext
API_TOKEN=your_api_token_here
```

- Change the `MAX_WORKERS` variable in the script to set the number of concurrent workers.
- Save the file.

3. Prepare the CSV file:

- Create a CSV file named `extract.csv` with a column containing Walmart product page slugs.

4. Run the script:

```bash
python walmart_product.py
```

## Results

The script outputs the retrieved products information in a JSON file named `results.json`.

```json
{
  "https://www.walmart.com/ip/RENPHO-HEPA-Air-Purifier-Home-Large-Room-600-Sq-ft-H13-True-Filter-Cleaner-Pet-Hair-Allergies-99-97-Smokers-Odors-Dust-Pollen-Odor-Eliminators-Bedroo/960917788": {
    "sku": "960917788",
    "name": "RENPHO HEPA Air Purifier for Home Large Room up to 600 Sq.ft, H13 True HEPA Filter Air Cleaner for Pet Hair, Allergies, 99.97% Smokers, Odors, Dust, Pollen, Odor Eliminators for Bedroom",
    "brand": {
      "name": "Renpho"
    },
    "image": "https://i5.walmartimages.com/seo/RENPHO-HEPA-Air-Purifier-Home-Large-Room-600-Sq-ft-H13-True-Filter-Cleaner-Pet-Hair-Allergies-99-97-Smokers-Odors-Dust-Pollen-Odor-Eliminators-Bedroo_1d90be16-914c-43df-a124-978e7b2b3e45.b43e82ed35acf4af4609f83f12e05d03.jpeg",
    "model": "RP-AP088B",
    "gtin13": null,
    "offers": {
      "url": "https://www.walmart.com/ip/RENPHO-HEPA-Air-Purifier-Home-Large-Room-600-Sq-ft-H13-True-Filter-Cleaner-Pet-Hair-Allergies-99-97-Smokers-Odors-Dust-Pollen-Odor-Eliminators-Bedroo/960917788",
      "price": 65.99,
      "availability": "https://schema.org/InStock",
      "item_condition": "https://schema.org/NewCondition",
      "price_currency": "USD",
      "available_delivery_method": "https://schema.org/OnSitePickup"
    },
    "review": [
      {
        "name": "Great value",
        "author": {
          "name": "Junebug"
        },
        "review_body": "Very easy to change filter and seems to be keeping our camper space dust free! Love the lighting on it. Great nightlight. The fan speed options work well for us.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "September 30, 2023"
      },
      {
        "name": "Air Purifier",
        "author": {
          "name": "Rosalie"
        },
        "review_body": "I have been looking at air purifiers because my living area always seems to have a smell, I came across this one and it seemed to be good value so thought I'd give it a try.  It says it covers 240 sq.ft which is perfect for my living room. It has 3 different fan speeds, which is nice for different times of the day where you need it more or less. It has a timer and sleep mode which are super convenient so you don't have to think about it. I have noticed that it has helped a alot with the smell in my living room. My shower has been starting to grow mold so needs to be remodeled obviously, but in the mean time this has worked great to put in my bathroom also to clear out the air and mold smell. I would definitely recommend this air purifier and I think I'm gonna have to get me another one!",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "May 10, 2021"
      },
      {
        "name": "Clean air!",
        "author": {
          "name": "Fran"
        },
        "review_body": "So far so good! I'm totally liking my air purifier! All you have to do is unbox, take the filter out of the plastic, insert and turn it on! It doesn't get easier than that!",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "September 24, 2023"
      },
      {
        "name": "First time purifier user and it's amazing",
        "author": {
          "name": "defaultForRating"
        },
        "review_body": "I have moderate to severe allergies and I live in a household that amplifies it. I'm talking watery, itchy AND dry eyes, sinus pressure, which makes it impossible to breathe and sleep, a cough and sore throat, I could go on. Medicine helps, as well as household cleaning, but I have pets, smokers in the house, old furniture... It's just a disaster inside and outside with the pollen. Needless to say, this machine was desperately needed. Set up was easy peasy and it comes with everything. I was cautious about the radio wave disruptions, but when I researched it, they say just put it out of range if anything occurs. I didn't have anything happen at all even when right next to it, though. After setup, it really was just the waiting game. I don't know why it took me so long to get one, because this purifier is wonderful. It blows out all the cool, fresh air, and sucks up the bad stuff. Part of me can't wait to see what it looks like when I change my filter, but I know it'll probably be gross, lol. My hay fever is so bad that it debilitates me and my air quality is not good normally, but I actually feel a difference when this is on and running, which I was sooo skeptical about. It's not like I'm breathing dust and pollen anymore right after I clean or come from outside. It's not loud, either, which wasn't a worry of mine, but that's cool. The buttons are easy enough to use, too. I am just so glad I notice a difference in the air quality. It's almost as if I was breathing into a dusty, smoky, hairy mask at any given moment without this. I'm shocked at how much better it makes my life. It's awesome.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "May 23, 2021"
      },
      {
        "name": null,
        "author": {
          "name": "Debra"
        },
        "review_body": "I love this humidifier I can smell the a difference inside my house I recommend for everyone to buy one! Well let's just say invest in one I will be ordering a second one for my bedroom.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "September 6, 2023"
      },
      {
        "name": "A GREAT BUY!!",
        "author": {
          "name": "Alberto"
        },
        "review_body": "I have a dog and live in a nyc railroad apt I've had the air purifier about 3 days now and I love it I love how it had a timer %26 3 different speeds and how the light changes as well lol",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "December 6, 2023"
      },
      {
        "name": "It works well.",
        "author": {
          "name": "Eddie"
        },
        "review_body": "It works quite well for the size of the room that it cleans.  The air is cleared of smoke and food odors in a few minutes.  And, i think it helps our many plants to stay and look crisp and healthy.  I also like the color display that it offers.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "November 13, 2022"
      },
      {
        "name": "Great product",
        "author": {
          "name": "Erica"
        },
        "review_body": "You can visibly see on the unit where it sucks in the regular air! I was amazed. I do recommend cleaning the outside if you do see that film; I wouldn't let it build up. Works great though.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "October 11, 2023"
      },
      {
        "name": "Air purifier",
        "author": {
          "name": "susan"
        },
        "review_body": "I love mine! Great for allergen sufferers and anyone wanting cleaner air. I noticed the difference within the few minutes of using it!",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "December 30, 2023"
      },
      {
        "name": "Great Device",
        "author": {
          "name": "defaultForRating"
        },
        "review_body": "Its very quiet and works very well in cleaning the air in my bedroom.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "February 5, 2024"
      }
    ],
    "description": "<strong>RENPHO air purifier for allergy &amp; asthma, H13 HEPA filter air purifier with 5-stage filtration provides 360° purification for your indoor air.</strong><br>\n<strong>This air purifier can improve your indoor air quality and help your family breathe better while keeping your household healthier.</strong><br>\n<strong>The air cleaner is especially well-suited for those who have babies, the elderly, and pet owners who suffer from allergies.</strong><br>\n<br>\n<strong>Air purifier adopts the TRUE HEPA H13 filter and can help capture and reduce ultra-tiny particles as small as 0.3 microns, eliminate airborne such as:</strong><br>\nAllergy Symptoms: allergic to dust mites, seasonal allergy, chronic allergies, asthmatic, coughing, sneezing, sinusitis, sinus congestion, allergens.<br>\nParticles: pollen, dust, large dust particles.<br>\nFrom Pets: odors, hair, fur, lint.<br>\nSmell: cigarette smoke, kitchen cooking fumes, weed smell, wildfire, perfumes.<br>\n<br>\n<strong>3 Adjustable Fan Speeds</strong><br>\nSimply press the speed button to choose from Low, Medium, or High fan speeds based on the air quality around you. When the air purifier turns on, the default fan speed is Medium.<br>\n<br>\n<strong>Sleep Mode with Whisper Quiet Operation</strong><br>\nGreat for sleeping, this air purifier?s sleep mode runs quietly at 26dB. About the level of whispering, it allows you to sleep while purifying your air.<br>\n<br>\n<strong>Timer and Lock Function</strong><br>\nConveniently set an auto-off timer for 2 hours, 4 hours, or 8 hours, which helps save money and energy. Press Lock button to activate the keylock mode to avoid errors operation caused by children or pets.<br>\n<br>\n<strong>Filter Replacement Indicator</strong><br>\nThe air purifier's filter replacement indicator will flash automatically when you need to change to a new filter. It should be replaced every 6-8 months. Please use the official filter model.<br>\n<br>\n<strong>Specifications:</strong><br>\nPower Supply: AC 120V 60Hz<br>\nCoverage Area: Up to 240 sq.ft / 22㎡<br>\nNoise Level: 26-52dB<br>\nDimensions: 8.5 x 8.5 x 14.25 in<br>\n<br>\n<strong>What's In The Box?</strong><br>\n1 x RENPHO Air Purifier<br>\n1 x True HEPA Filter ( Pre-Installed)<br>\n1 x User Manual<br>\n<br>\n<strong>Warm Tips:</strong><br>\nPlease remove the packaging material of the air filter before first use.<br>\nPlease reset the filter after replacing the filter to make sure the air cleaner to calculate the filter's lifetime.<br>\nWe suggest you replace the air filter every 6-8 months. However, you may change the air filter based on how clean your area is and how often you use it.<br>\n<br>\n<strong>Original Replacement Filter: </strong><br>\nfor pet allergy, Genuine, 1 Pack <a rel=\"nofollow\" href=\"https://www.walmart.com/ip/seort/304235467\"> Click me</a><br>\nfor moist conditions , Genuine, 1 Pack <a rel=\"nofollow\" href=\"https://www.walmart.com/ip/seort/388838587\">Click me</a>",
    "aggregate_rating": {
      "best_rating": 5,
      "rating_value": 4.7,
      "review_count": 2929
    },
    "item_list_element": [
      {
        "item": {
          "@id": "https://www.walmart.com/cp/home-improvement/1072864",
          "name": "Home Improvement"
        },
        "position": 1
      },
      {
        "item": {
          "@id": "https://www.walmart.com/cp/heating-cooling-air-quality/133032",
          "name": "Heating, Cooling, & Air Quality"
        },
        "position": 2
      },
      {
        "item": {
          "@id": "https://www.walmart.com/cp/air-quality/1231459",
          "name": "Air Quality"
        },
        "position": 3
      },
      {
        "item": {
          "@id": "https://www.walmart.com/browse/home-improvement/air-purifiers/1072864_133032_1231459_46324",
          "name": "Air Purifiers"
        },
        "position": 4
      },
      {
        "item": {
          "@id": "https://www.walmart.com/browse/home-improvement/air-purifiers/1072864_133032_1231459_46324",
          "name": "All Air Purifiers"
        },
        "position": 5
      }
    ]
  },
  "https://www.walmart.com/ip/COOPLUS-Women-s-Athletic-Ankle-Socks-Women-s-Sock-Size-9-11-Female-Cushioned-Color-Socks-6-Pairs/940014996": {
    "sku": "940014996",
    "name": "COOPLUS Women's Athletic Ankle Socks Women's Sock Size 9-11 Female Cushioned Color Socks 6 Pairs",
    "brand": {
      "name": "Cooplus"
    },
    "image": "https://i5.walmartimages.com/seo/COOPLUS-Women-s-Athletic-Ankle-Socks-Women-s-Sock-Size-9-11-Female-Cushioned-Color-Socks-6-Pairs_2be83d28-ffb2-498d-912a-6ee8bf55c441.33a1b0761e7dcf491159b9d5ba5d5345.jpeg",
    "model": null,
    "gtin13": "768634164498",
    "offers": {
      "url": "https://www.walmart.com/ip/COOPLUS-Women-s-Athletic-Ankle-Socks-Women-s-Sock-Size-9-11-Female-Cushioned-Color-Socks-6-Pairs/940014996",
      "price": 12.48,
      "availability": "https://schema.org/InStock",
      "item_condition": "https://schema.org/NewCondition",
      "price_currency": "USD",
      "available_delivery_method": "https://schema.org/OnSitePickup"
    },
    "review": [
      {
        "name": "Great socks",
        "author": {
          "name": "Cathy"
        },
        "review_body": "Love these socks toe and heel are thick gives you more padding for walking and jogging. They stay where they need to. They don't bunch up in your shoes.  Great product",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "February 4, 2024"
      },
      {
        "name": "The best socks ever.",
        "author": {
          "name": "Miranda"
        },
        "review_body": "I was concerned when the socks arrived about the thickness, I always wear thin socks.  I made a point to wear them and they are the most comfortable socks that I have worn.  They stay in place and I love the way they feel so soft and comfy.  I also love the bright colors.  I would recommend these socks to anyone.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "January 4, 2024"
      },
      {
        "name": "Great quality",
        "author": {
          "name": "JudyLasVegas"
        },
        "review_body": "Well worth the price and the price is very reasonable too. Very comfortable. These are thick quality but not so thick your shoes are uncomfortable. The colors are bright and pretty. I bought other brands that are very thin and didn't hold up. These are high quality. The seams do not hurt my feet. These do not roll down off my feet. They stay in place but are not too tight.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "January 30, 2024"
      },
      {
        "name": "I ordered Lg size and they fit me.\n(Man) s",
        "author": {
          "name": "defaultForRating"
        },
        "review_body": "These are made really nice. They're very comfortable and fit perfectly.      I never knew that women's socks were so much better than men's socks. Lol.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "November 14, 2023"
      },
      {
        "name": "cushioned socks black\\neon",
        "author": {
          "name": "Susan"
        },
        "review_body": "they came early, they are the most comfortable shock I have ever put on my foot, fit perfectly they were actually the size they said they were.  the colors are kind of cute my sister wanted to sit still a pair. very good value for the money high quality",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "December 27, 2023"
      },
      {
        "name": "Great fitting, comfy",
        "author": {
          "name": "Sissy"
        },
        "review_body": "Socks fit nicely, elastic hugs my feet without squeezing too much.  Heels stay in place and do not slide down into shoes.  Would definitely buy again.  Wish I could pick the colors- the pack of six pairs of different colors included yellow and orange (not my favorites).  But the other four colors were great.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "December 20, 2023"
      },
      {
        "name": "pleasantly pleased",
        "author": {
          "name": "Y"
        },
        "review_body": "Great socks! My feet are super sensitive, so it's hard for me to find comfortable socks. I have had to return many. I bought these, liked them and bought some more. My feet are  very happy!! There are quite a few of these socks. I had to make sure they said Eallco across the toes.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "February 3, 2024"
      },
      {
        "name": "Happy Feet",
        "author": {
          "name": "terrivanilla"
        },
        "review_body": "Great quality sock. They are a bit thick but feel like cushions when you walk. They have a seen band that sits around the mid area of your foot. Great support. I love that the back has a bit of extra fabric so that the back of your gym shoe doesn’t rub agains the back of your ankle. Definitely would buy again. My feet are super happy.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "March 3, 2023"
      },
      {
        "name": null,
        "author": {
          "name": "tamara"
        },
        "review_body": "Soft, nice and cushiony. I wear a size 11w. They are stretch and do not roll down. They stay in place. The down side is the fuzz badly after the first wash!",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 3,
          "worst_rating": 1
        },
        "date_published": "November 5, 2022"
      },
      {
        "name": null,
        "author": {
          "name": "Deb"
        },
        "review_body": "They look like someone had open the socks. There wasn't any label wrath's around them or what size they are.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 3,
          "worst_rating": 1
        },
        "date_published": "August 26, 2023"
      }
    ],
    "description": "<p><strong>Women's Athletic Ankle Cushioned Socks</strong></p><p><strong>COOPLUS Socks Features: Moisture wicking; Arch support; Cushioned sole;Good stretch;Breathable</strong></p><p><strong>Suitable for Casual/dress/sport/running/work/athletic shoes</strong></p><p><strong>6 Pairs Per Suit</strong></p><p><strong>Fit for Female Shoe Size 6-10; Sock Size 9-11</strong></p><p><strong>Washing Instruction: Machine Wash &amp; Hand Wash(Suggest using wash bag). Tumble Dry &amp; Air Dry. Don't iron. Don't bleach. Don't soak socks in hot water or suds for a long time.</strong></p>",
    "aggregate_rating": {
      "best_rating": 5,
      "rating_value": 4.8,
      "review_count": 909
    },
    "item_list_element": [
      {
        "item": {
          "@id": "https://www.walmart.com/cp/clothing/5438",
          "name": "Clothing"
        },
        "position": 1
      },
      {
        "item": {
          "@id": "https://www.walmart.com/cp/womens-clothing/133162",
          "name": "Womens Clothing"
        },
        "position": 2
      },
      {
        "item": {
          "@id": "https://www.walmart.com/browse/clothing/womens-socks-hosiery-tights/5438_133162_5155182_7615574",
          "name": "Womens Socks, Hosiery & Tights"
        },
        "position": 3
      },
      {
        "item": {
          "@id": "https://www.walmart.com/browse/clothing/womens-socks/5438_133162_5155182_8388637_1228577",
          "name": "Womens Socks"
        },
        "position": 4
      },
      {
        "item": {
          "@id": "https://www.walmart.com/browse/clothing/womens-socks/5438_133162_5155182_8388637_1228577",
          "name": "Womens Socks"
        },
        "position": 5
      }
    ]
  },
  "https://www.walmart.com/ip/AMITOFO-Robes-for-Women-Satin-Silk-Pajamas-Set-4pcs-Lace-Trim-Cami-Sexy-Lingerie-Sleepwear-Underwear/3517206463": {
    "sku": "3517206463",
    "name": "AMITOFO Robes for Women Satin Silk Pajamas Set 4pcs Lace Trim Cami Sexy Lingerie Sleepwear Underwear",
    "brand": {
      "name": "AMITOFO"
    },
    "image": "https://i5.walmartimages.com/seo/AMITOFO-Robes-for-Women-Satin-Silk-Pajamas-Set-4pcs-Lace-Trim-Cami-Sexy-Lingerie-Sleepwear-Underwear_19d7d19d-9b99-4c8a-a49f-ac688873ab20.954ae9819680bbab7c72e4d899ff50cd.jpeg",
    "model": null,
    "gtin13": "657381108926",
    "offers": {
      "url": "https://www.walmart.com/ip/AMITOFO-Robes-for-Women-Satin-Silk-Pajamas-Set-4pcs-Lace-Trim-Cami-Sexy-Lingerie-Sleepwear-Underwear/3517206463",
      "price": 14.99,
      "availability": "https://schema.org/InStock",
      "item_condition": "https://schema.org/NewCondition",
      "price_currency": "USD",
      "available_delivery_method": "https://schema.org/OnSitePickup"
    },
    "review": [
      {
        "name": "amazing",
        "author": {
          "name": "Michael"
        },
        "review_body": "my wife is a full figure woman and looks incredible in this ❤️",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "January 22, 2024"
      },
      {
        "name": "Like this made well for price and really cute",
        "author": {
          "name": "Tina"
        },
        "review_body": "Made well great price will recommend seller %26 items",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "January 13, 2024"
      },
      {
        "name": "WIFE LOVES IT",
        "author": {
          "name": "Damien"
        },
        "review_body": "was a gift its beautiful yet sexy, sleek and smooth i recommend as gifts and personal purchases!",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "December 23, 2023"
      },
      {
        "name": "Incredibly alluring!",
        "author": {
          "name": "Charli"
        },
        "review_body": "I mainly wear it around the house during relaxed days, so it's comfortable. The robe is particularly handy for quickly covering up if I need to answer the door or something. Everything fits just right.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "October 16, 2023"
      },
      {
        "name": "A charming and enticing satin lingerie set.",
        "author": {
          "name": "Jenn"
        },
        "review_body": "I absolutely love this cute and sexy 4-piece lingerie set! It includes a super sexy crop lace top with matching lace panties. The silky material feels wonderful, and the fit is incredibly comfortable. The set also comes with satin pajama shorts and a robe with a sash.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "July 8, 2023"
      },
      {
        "name": "A fantastic little set.",
        "author": {
          "name": "Kaylie"
        },
        "review_body": "This set is a fantastic choice if you're seeking affordable lingerie. It fits perfectly and true to size, so there's no need to go up or down a size. However, be aware that if you have a larger chest, the top might fit somewhat oddly, but it still works. My husband was quite a fan, and I'm pleased to have found something both sexy and comfortable, which is always my goal. It's a great discovery.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 4,
          "worst_rating": 1
        },
        "date_published": "August 3, 2023"
      },
      {
        "name": "A bit challenging to put on.",
        "author": {
          "name": "Riley"
        },
        "review_body": "The bra portion proved to be quite challenging to put on, constantly twisting at the back regardless of how I attempted to wear it. Some other reviewers mentioned that the top lacked stretch, but I found it to have just the right amount. With a height of 5'4\", weighing 128 lbs, and wearing a 36C bra size, I opted for a size medium. Although I was worried it might tear if mishandled, fortunately, it didn't. Nonetheless, I decided to return it because it didn't fit me well, especially disliking how the shorts sagged.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 3,
          "worst_rating": 1
        },
        "date_published": "September 13, 2023"
      },
      {
        "name": "Cheap quality, runs small",
        "author": {
          "name": "Vanessa"
        },
        "review_body": "The quality of this set feels very thin and cheap. I ordered a 2XL and it fit like a L, This is not true to size I sized one up for my usual size when it arrived it was 2sizes too small. The underwear alone had to be a about a size M-L",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 2,
          "worst_rating": 1
        },
        "date_published": "January 14, 2024"
      },
      {
        "name": "Runs very small",
        "author": {
          "name": "Amanda"
        },
        "review_body": "My normal size is an XL. I got an XL and it's too small. The XL is closer to a Medium",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 1,
          "worst_rating": 1
        },
        "date_published": "November 8, 2023"
      },
      {
        "name": null,
        "author": {
          "name": "joanna"
        },
        "review_body": "i dislike the make of the products",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 1,
          "worst_rating": 1
        },
        "date_published": "December 29, 2023"
      }
    ],
    "description": "<p>Women's Satin Pajamas Sets 4 Pieces Sexy Silk Lingerie Lace Sleepwear Cami Shorts with Robe</p>\n<p></p>\n<p>Women's 4 piece silk pajama set matching sexy lace tank top , elastic band shorts and satin comfy robes. Floral lace, satin, long sleeve, elastic waist, bra and shorts lingerie set and a belted robe are included, keeps you nice all night</p>\n<p></p>\n<p>Soft fabric</p>\n<p>Hand wash or machine wash. Do not bleach.</p>\n<p></p>\n<p>Fabric: Made of satin and lace material, skin-friendly, breathable, and soft fabric that takes care of your skin. Easy to put on and take off，keep you nice and comfortable all day.</p>\n<p></p>\n<p>Features: 4 PCS sleepwear set, include lace lingerie, satin night robe with belt, and sleep shorts. Comfy Pajama Set for a relaxing day or night.The sexy V neck strap is adjustable.</p>\n<p></p>\n<p>Occasions: This silk pajama set for women is not only suitable for daily home wear, but also role-playing,pajama party, girls day, bridal party and other sleepwear activity.</p>\n<p></p>\n<p>Material: 95% polyester 5% spandex</p>\n<p></p>\n<p>Package Include:4 PCS sleepwear set</p>",
    "aggregate_rating": {
      "best_rating": 5,
      "rating_value": 4,
      "review_count": 63
    },
    "item_list_element": [
      {
        "item": {
          "@id": "https://www.walmart.com/cp/clothing/5438",
          "name": "Clothing"
        },
        "position": 1
      },
      {
        "item": {
          "@id": "https://www.walmart.com/cp/womens-clothing/133162",
          "name": "Womens Clothing"
        },
        "position": 2
      },
      {
        "item": {
          "@id": "https://www.walmart.com/cp/womens-bras-panties-lingerie/3523459",
          "name": "Womens Bras, Panties & Lingerie"
        },
        "position": 3
      },
      {
        "item": {
          "@id": "https://www.walmart.com/browse/clothing/womens-lingerie/5438_133162_3523459_4248599_7492439",
          "name": "Womens Lingerie"
        },
        "position": 4
      },
      {
        "item": {
          "@id": "https://www.walmart.com/browse/clothing/womens-lingerie/5438_133162_3523459_4248599_7492439",
          "name": "Womens Lingerie"
        },
        "position": 5
      }
    ]
  },
  "https://www.walmart.com/ip/Carote-Nonstick-Pots-and-Pans-Set-8-Pcs-Induction-Kitchen-Cookware-Sets-Beige-Granite/513536386": {
    "sku": "513536386",
    "name": "Carote Nonstick Pots and Pans Set, 8 Pcs Induction Kitchen Cookware Sets (Beige Granite)",
    "brand": {
      "name": "Carote"
    },
    "image": "https://i5.walmartimages.com/seo/Carote-Nonstick-Pots-and-Pans-Set-8-Pcs-Induction-Kitchen-Cookware-Sets-Beige-Granite_e4183757-3e78-4321-a9ad-3123804e77ad.98cb62d1e47bdc84f235cbdcfafac1db.png",
    "model": "S-ICE10",
    "gtin13": "888316705754",
    "offers": {
      "url": "https://www.walmart.com/ip/Carote-Nonstick-Pots-and-Pans-Set-8-Pcs-Induction-Kitchen-Cookware-Sets-Beige-Granite/513536386",
      "price": 64.98,
      "availability": "https://schema.org/InStock",
      "item_condition": "https://schema.org/NewCondition",
      "price_currency": "USD",
      "available_delivery_method": "https://schema.org/OnSitePickup"
    },
    "review": [
      {
        "name": "Absolutely love ! Must buy!",
        "author": {
          "name": "Nessa"
        },
        "review_body": "They are the most high quality pots ! Im impressed with the non stick results, they have no weird smells! I feel better knowing these arent toxic and I will have for years to come! The price was unbelievable!",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "February 2, 2024"
      },
      {
        "name": "Had for 4 months",
        "author": {
          "name": "Jacquelyne"
        },
        "review_body": "I've had these pots and pans for about 4 months now and am very impressed. I have no complaints so far. I've purchased nonstick pans in the past, and they've alway come up short, so always been pretty weary of the phrase from past experiences. My husband however fell for it and purchased these as a gift; though I objected, he went ahead and bought them and I am so glad he did! They're truly nonstick and have become my everyday pans. I make Korean pancakes and it's a nightmare cooking them on my other pans. With these, they don't stick at all and they come out crispy and perfect. To top it off they're very pretty to look at. Very happy with this buy and would definitely recommend to anyone.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "February 5, 2024"
      },
      {
        "name": "Will Buy a Second Set",
        "author": {
          "name": "Deina"
        },
        "review_body": "Beautiful love them. Used everyday for a week now. Have held up nicely. I hand wash them after, no dishwasher so far.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "March 27, 2023"
      },
      {
        "name": "Perfect heat distribution, beautiful, non stick.",
        "author": {
          "name": "defaultForRating"
        },
        "review_body": "It's an excellent set of pans. Beautiful one. I was afraid to have my collection with stains and spots during the first days (due to some reviews), but it didn't happen. I use it often, and now I retired my stainless steel set. It has an excellent heat distribution and definitely doesn't stick to food. I cook all sort of foods, usually handwashing, because it's pretty easy, almost remove the fat with a soft sponge. So far, after nearly one year, neither stains nor cracks.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 5,
          "worst_rating": 1
        },
        "date_published": "January 13, 2024"
      },
      {
        "name": "Alright",
        "author": {
          "name": "Marlene"
        },
        "review_body": "I love the way the set looks but unfortunately they stained really easily and scratched easily, hopefully this problem get fixed someday…",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 3,
          "worst_rating": 1
        },
        "date_published": "February 24, 2023"
      },
      {
        "name": "Not for cooking—-decor items",
        "author": {
          "name": "Cole"
        },
        "review_body": "The color of the pans are pretty. However, after multiple uses the color distorts due to heat causing the color to turn brown. Water gets into the handles when cleaning causing the “wood” handles to expand, resulting in the handles to bubble %26 becomes hot. It's more of a decor aesthetic.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 2,
          "worst_rating": 1
        },
        "date_published": "November 19, 2023"
      },
      {
        "name": "Came stained and scratched so easy",
        "author": {
          "name": "CHRISTIAN"
        },
        "review_body": "I never use metal anything, only wooden or plastic but there are deep groves which makes no sense. The paint from the inner protectant is bubbled on one of the pans and one of these looked like it had soot on one when I opened. With all that being said that are some good pots of the rest didn’t happen.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 2,
          "worst_rating": 1
        },
        "date_published": "March 27, 2023"
      },
      {
        "name": "Love pots and pans. Hate customer service.",
        "author": {
          "name": "Rod"
        },
        "review_body": "we do like the pans, although when we received them one of the handle's was broke. on several occasions contacted customer service but our complaint was ignored. we throughly enjoy the pots, except the one thats broken, but customer service is non-existing. As of today, we still haven't heard back from them, to get a replacement handle.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 2,
          "worst_rating": 1
        },
        "date_published": "March 14, 2023"
      },
      {
        "name": "Pretty but Scratches easily",
        "author": {
          "name": "Stephanie"
        },
        "review_body": "This is a pretty set but it scratches very easily. I only use silicone utensils on it and always wash them by hand and they are still all scratched. One came scratched but I was too lazy to do anything about it, but probably should have taken that as a sign to return them. Wouldn't recommend, I'd stick to a good stainless steel set or cast iron.",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 1,
          "worst_rating": 1
        },
        "date_published": "December 27, 2023"
      },
      {
        "name": null,
        "author": {
          "name": "Omi"
        },
        "review_body": "I love the pots and pans, the reason for the 1 star is that the big pot has handles that heat up just like the pot itself. I burned myself and almost dropped it on my glass stove top. I wrote to the Company and never heard back from them. this was my second set, the first one has different handles that dont get hot. So this one here is a bad one to use. I added pictures of both to see the difference. If it wasnt for that handles on the pot on the left this would deserve a 5 star. Since I have not gotten any return message or call from Manufacturers I say Customer service is a -0",
        "review_rating": {
          "best_rating": 5,
          "rating_value": 1,
          "worst_rating": 1
        },
        "date_published": "January 9, 2024"
      }
    ],
    "description": "Carote Nonstick Pots and Pans Set, 8 Pcs Non Stick Cookware Set, Induction Stone Cookware Kitchen Cooking Set (Beige Granite)<br>",
    "aggregate_rating": {
      "best_rating": 5,
      "rating_value": 4.7,
      "review_count": 6518
    },
    "item_list_element": [
      {
        "item": {
          "@id": "https://www.walmart.com/cp/home/4044",
          "name": "Home"
        },
        "position": 1
      },
      {
        "item": {
          "@id": "https://www.walmart.com/cp/kitchen-dining/623679",
          "name": "Kitchen & Dining"
        },
        "position": 2
      },
      {
        "item": {
          "@id": "https://www.walmart.com/browse/home/shop-pots-pans/4044_623679_8140341_4666314",
          "name": "Pots & Pans"
        },
        "position": 3
      },
      {
        "item": {
          "@id": "https://www.walmart.com/browse/home/cookware-sets/4044_623679_8140341_599265",
          "name": "Cookware Sets"
        },
        "position": 4
      }
    ]
  }
}
```

Additionally, it maintains a record of failed rows in `failed_rows.txt` for reprocessing in subsequent runs.

## Contributing

Feel free to contribute by submitting issues or pull requests. Your feedback and improvements are welcome!