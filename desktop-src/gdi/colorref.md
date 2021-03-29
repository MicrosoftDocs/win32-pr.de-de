---
Description: Der COLORREF-Wert wird verwendet, um eine RGB-Farbe anzugeben.
ms.assetid: b87d3de2-7a13-44ef-8253-c6851a75fa54
title: COLORREF (WINDEF. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 6836cfcc1b18d0b20d5e347fb83206551b27de06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996458"
---
# <a name="colorref"></a>COLORREF

Der COLORREF-Wert wird verwendet, um eine [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) -Farbe anzugeben.


```C++
typedef DWORD COLORREF;
typedef DWORD* LPCOLORREF;
```



## <a name="remarks"></a>Bemerkungen

Beim Angeben einer expliziten [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) -Farbe hat der **COLORREF** -Wert die folgende hexadezimale Form:

`0x00bbggrr`

Das nieder wertige Byte enthält einen Wert für die relative Intensität von rot. Das zweite Byte enthält einen Wert für grün; Das dritte Byte enthält einen Wert für blau. Das höchst wertige Byte muss NULL sein. Der maximale Wert für ein einzelnes Byte ist 0xFF.

Um einen **COLORREF** -Farbwert zu erstellen, verwenden Sie das [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) -Makro. Um die einzelnen Werte für die roten, grünen und blauen Komponenten eines Farbwerts zu extrahieren, verwenden Sie die Makros [**getrvalue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [getgvalue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)und [getbvalue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) .

## <a name="example"></a>Beispiel

```cpp
// Color constants.
const COLORREF rgbRed   =  0x000000FF;
const COLORREF rgbGreen =  0x0000FF00;
const COLORREF rgbBlue  =  0x00FF0000;
const COLORREF rgbBlack =  0x00000000;
const COLORREF rgbWhite =  0x00FFFFFF;
```

Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples) auf GitHub.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>WINDEF. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Farben](colors.md)
</dt> <dt>

[Farbstrukturen](color-structures.md)
</dt> <dt>

[Getbvalue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue)
</dt> <dt>

[Getgvalue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)
</dt> <dt>

[**Getrvalue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)
</dt> <dt>

[RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb)
</dt> </dl>

 

 




