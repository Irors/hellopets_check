import requests

with open("wallets.txt") as wallet:
    wallets = wallet.readlines()

for adresss in wallets:
    params = {
        'address': f'{adresss[:-1]}',
        'activityId': '0',
    }

    if adresss == wallets[-1]:
        response = requests.get('https://api.hellopets.world/api/v1/activity/reward', params=params)
        if int(response.json()['data']['totalReward']) != 0:
            print(f"{response.json()['data']['address']} rewards - {response.json()['data']['totalReward']}")


    else:
        response = requests.get('https://api.hellopets.world/api/v1/activity/reward', params=params)
        if int(response.json()['data']['totalReward']) != 0:
            print(f"{response.json()['data']['address']} rewards - {response.json()['data']['totalReward']}")


