package main

import (
	"fmt"
	"math/rand"
	"time"
)

func main() {
fmt.Println("***** Игра быки и коровы *****")
  fmt.Println("Я загадываю четырёхзначное число - вы отгадываете. Если цифра угадана, но не на своём месте - это корова. Если цифра угадана и стоит на своём месте - это бык. Число не должно начинаться с нуля и в нём не должны повторяться цифры.")
  fmt.Println("---------")
  fmt.Println("Например, я загадываю 1234. Вы предполагаете, что моё число - 2437. В вашем числе 2 - это корова, т.к. она есть в моём числе, но стоит не на своём месте. А цифра 3 - бык, т.к. угадана верно и находится на своём месте")
  var answer string
  for {
    fmt.Println("Поехали (да/нет)?")
    fmt.Scan(&answer)
    fmt.Println("-----------")
    if answer != "да" && answer != "нет" {
      fmt.Println("Ожидалось да или нет")
      continue
    } 
    if answer == "нет" {
      fmt.Println("Вы не захотели со мной играть. Тогда послушайте хокку:")
      fmt.Println("Печальный мир!")
      fmt.Println("Даже, когда расцветают вишни,")
      fmt.Println("Даже тогда.")
      return
    } else {
      break
    }
  }
  rand.Seed(time.Now().UnixNano())
  var a, b, c, d int // числа, которые загадал компьютер
  for {
    a = rand.Intn(9)
    b = rand.Intn(9)
    c = rand.Intn(9)
    d = rand.Intn(9)
      if a == b || b == c || c == d || d == a || a == c || b == d {
        continue //проверка, чтобы компьютер не загадал число с повторяющимися цифрами
      }
      break
  }
  // fmt.Println("Подсказка: моё число - это", a, b, c, d) //Для понимания в чём заключается игра
  resultII := a * 1000 + b * 100 + c * 10 + d
  var answerUser int
  var a1, b1, c1, d1 int //числа, которые угадывает пользователь
  var bull, cow int
  var numberTry = 1 //число попыток угадать
  fmt.Println("------------")
  for {
    cow, bull = 0, 0
    fmt.Println("У вас попытка №", numberTry, "Попробуйте отгадать моё число:")
    fmt.Scan(&answerUser)
    a1 = answerUser / 1000
    b1 = answerUser / 100 - a1 * 10
    c1 = answerUser / 10 - a1 * 100 - b1 * 10
    d1 = answerUser - a1 * 1000 - b1 * 100 - c1 * 10
    
    if answerUser < 1000 || answerUser > 9999 {
      fmt.Println("Ожидалось четырёхзначное число")
      continue
    }
    fmt.Println("Ваш ответ:", a1, b1, c1, d1)
    if a1 == b1 || b1 == c1 || c1 == d1 || d1 == a1 || a1 == c1 || b1 == d1 {
      fmt.Println("Цифры не должны повторяться")
      continue
    }
    if a1 == a {
      bull++
    }
    if b1 == b {
      bull++
    }
    if c1 == c {
      bull++
    }
    if d1 == d {
      bull++
    }
    if a1 == b || a1 == c || a1 == d {
      cow++
    }
    if b1 == a || b1 == c || b1 == d {
      cow++
    }
    if c1 == a || c1 == b || c1 == d {
      cow++
    }
    if d1 == a || d1 == b || d1 == c {
      cow++
    }
    fmt.Print("В вашем числе быков: ", bull,  ", коров: ", cow, "\n")
    fmt.Println("-------------")
    numberTry++
    if resultII == answerUser {
      break
    } 
  }
fmt.Println("Поздравляю, вы угадали число: ", resultII, " с", numberTry, " попыток \n")
fmt.Println("В награду почитайте гарик:")
fmt.Println("-----------------------------")
fmt.Println("Вовлекаясь во множество дел,")
fmt.Println("Не мечись, как по джунглям ботаник,")
fmt.Println("Не горюй, что не всюду успел,")
fmt.Println("Может ты опоздал на «Титаник»")
}
