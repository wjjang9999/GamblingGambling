import time
import random
import keyboard

start_time = time.perf_counter()
print("---게임 룰---")
print("1.f키를 눌러 동전 던지기(쿨타임 0.5초)")
print("2.앞면이 나오면 돈 2배 or +10,000원")
print("3.뒷면이 나오면 돈 0.5배 or -10,000원")
print("4.기본자금은 20,000원")
print("5.500만원을 모으면 게임 승")
print("6.돈을 모두 잃으면 게임 끝")
print("7.시간이 매우 자세하게 나오는건 의도된 것이니 신경쓰지마세요...")
print("666.숨겨진 %?^*&@#가 있으니 알아두세요.")
money = 20000
while money < 4999999:
    key = keyboard.read_key()
    if key == "f":
        
        lucky = random.randrange(1,8145061)
        print("                                                                     ",lucky)
        if lucky == 7:
            print("[hidden]떨어진 동전이 세워졌습니다!!")
            money = 5000000
        elif lucky <= 4072530:
            print("앞면!")
            if random.randrange(1,3) == 1:
                money = money*2
                print("현재 보유 돈:",money)
            else:
                money = money+10000
                print("현재 보유 돈:",money)
        else:
            print("뒷면!")
            if random.randrange(1,3) == 1:
                money = money/2
                print("현재 보유 돈:",money)
            else:
                money = money-10000
                print("현재 보유 돈:",money)
        if money <= 0:
            break
        time.sleep(0.7)
end_time = time.perf_counter()
execution_time = end_time - start_time
if lucky == 7:
    print("당신은 814만5060분의 1 이라는 경이로운 확률을 뚫고 동전을 세웠습니다!")
    time.sleep(1)
    print("814만5060분의 1 은 로또 1등 당첨 확률입니다!")
    time.sleep(2)
    print("이딴곳에 운 쓰지 말고 로또 샀으면 1등 당첨이였는데..")
elif money <= 0:
    print("당신은 도박으로 약 2만원을 잃었습니다.")
    time.sleep(2)
    print("하지만 2만원은 가상화폐이기 때문에 당신은 손해를 보지 않았습니다?")
    time.sleep(5)
    print("하지만 약",execution_time,"초의 시간을 손해봤습니다!")
else:
    print("축하합니다!") 
    time.sleep(1)
    print("당신은 도박으로 ",money-20000,"만원을 벌었습니다!")
    time.sleep(3)
    print("하지만 가상화폐니 사용하지 못합니다!")
    time.sleep(3)
    print("오히려 ",execution_time,"초의 시간을 손해봤습니다!")
