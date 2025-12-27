```md
# MinLib — простая минималистичная UI‑либа

Эта библиотека позволяет быстро создавать минимальные и аккуратные интерфейсы для Roblox‑скриптов.

---

## Подключение

```lua
local MinimalLib = loadstring(game:HttpGet("ВАША_ССЫЛКА"))()
```

---

## Создание окна

```lua
local Window = MinimalLib:MakeWindow({
    Name = "Название окна",
    SaveConfig = true,          -- сохранять значения
    ConfigFolder = "MyConfig",  -- папка для сохранений
})
```

---

## Создание таба

```lua
local Tab = Window:MakeTab({
    Name = "Главная"
})
```

---

## Label (текст)

```lua
Tab:AddLabel("Пример текста")
```

---

## Button (кнопка)

```lua
Tab:AddButton({
    Name = "Нажми меня",
    Callback = function()
        print("Кнопка нажата")
    end
})
```

---

## Toggle (переключатель)

```lua
Tab:AddToggle({
    Name = "Тоггл",
    Default = false,
    Flag = "MyToggle",
    Save = true,
    Callback = function(state)
        print("Состояние:", state)
    end
})
```

---

## Slider (ползунок)

```lua
Tab:AddSlider({
    Name = "Громкость",
    Min = 0,
    Max = 100,
    Default = 50,
    Increment = 1,
    ValueName = "%",
    Flag = "Volume",
    Save = true,
    Callback = function(value)
        print("Громкость:", value)
    end
})
```

---

## Textbox (поле ввода)

```lua
Tab:AddTextbox({
    Name = "Введите текст",
    Default = "",
    TextDisappear = false,
    Callback = function(text)
        print("Введено:", text)
    end
})
```

---

## Инициализация сохранений

```lua
MinimalLib:Init()
```

---

## Уничтожение UI

```lua
MinimalLib:Destroy()
```

---
