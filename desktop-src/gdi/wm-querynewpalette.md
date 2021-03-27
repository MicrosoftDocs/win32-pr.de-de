---
description: Die WM- \_ Abfrage "querynewpalette" informiert ein Fenster darüber, dass es im Begriff ist, den Tastaturfokus zu erhalten, sodass das Fenster seine logische Palette erkennen kann, wenn es den Fokus erhält.
ms.assetid: bc9f76ca-62af-4f0b-8791-49269a1b23d1
title: WM_QUERYNEWPALETTE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ca664bbb6fb30a0508f9429dd62af489c092db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979353"
---
# <a name="wm_querynewpalette-message"></a>WM \_ querynewpalette-Meldung

Die **WM- \_ Abfrage "querynewpalette** " informiert ein Fenster darüber, dass es im Begriff ist, den Tastaturfokus zu erhalten, sodass das Fenster seine logische Palette erkennen kann, wenn es den Fokus erhält.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn das Fenster seine logische Palette erkennt, muss es **true** zurückgeben. Andernfalls muss Sie **false** zurückgeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Farben](colors.md)
</dt> <dt>

[Farb Meldungen](color-messages.md)
</dt> <dt>

[**WM \_ palettechanged**](wm-palettechanged.md)
</dt> <dt>

[**WM- \_ paletteischanging**](wm-paletteischanging.md)
</dt> </dl>

 

 
