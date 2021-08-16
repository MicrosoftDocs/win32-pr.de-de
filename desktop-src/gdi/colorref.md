---
Description: Der COLORREF-Wert wird verwendet, um eine RGB-Farbe anzugeben.
ms.assetid: b87d3de2-7a13-44ef-8253-c6851a75fa54
title: COLORREF (Windef.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 3e51b2a906af5939a5c7a8753e5fcc4fbcfae64590e62bcb6df1da2c2bd8426d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761893"
---
# <a name="colorref"></a>COLORREF

Der COLORREF-Wert wird verwendet, um eine [RGB-Farbe](/windows/desktop/api/Wingdi/nf-wingdi-rgb) anzugeben.


```C++
typedef DWORD COLORREF;
typedef DWORD* LPCOLORREF;
```



## <a name="remarks"></a>Hinweise

Wenn Sie eine explizite [RGB-Farbe](/windows/desktop/api/Wingdi/nf-wingdi-rgb) angeben, weist **der COLORREF-Wert** die folgende Hexadezimalform auf:

`0x00bbggrr`

Das niedrigwertige Byte enthält einen Wert für die relative Intensität von Rot. Das zweite Byte enthält einen Wert für grün. und das dritte Byte enthält einen Wert für blau. Das obere Byte muss 0 (null) sein. Der Höchstwert für ein einzelnes Byte ist 0xFF.

Verwenden Sie das **RGB-Makro,** um einen COLORREF-Farbwert [zu](/windows/desktop/api/Wingdi/nf-wingdi-rgb) erstellen. Um die einzelnen Werte für die roten, grünen und blauen Komponenten eines Farbwerts zu extrahieren, verwenden Sie die Makros [**GetRValue,**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue) [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)und [GetBValue.](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue)

## <a name="example"></a>Beispiel

```cpp
// Color constants.
const COLORREF rgbRed   =  0x000000FF;
const COLORREF rgbGreen =  0x0000FF00;
const COLORREF rgbBlue  =  0x00FF0000;
const COLORREF rgbBlack =  0x00000000;
const COLORREF rgbWhite =  0x00FFFFFF;
```

Beispiel aus [Windows klassischen Beispielen](https://github.com/microsoft/Windows-classic-samples) auf GitHub.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>Windef.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Farben](colors.md)
</dt> <dt>

[Farbstrukturen](color-structures.md)
</dt> <dt>

[GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue)
</dt> <dt>

[GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)
</dt> <dt>

[**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)
</dt> <dt>

[RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb)
</dt> </dl>

 

 




