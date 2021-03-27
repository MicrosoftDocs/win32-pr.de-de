---
description: Die WM \_ paletteischanging-Nachricht informiert Anwendungen darüber, dass eine Anwendung ihre logische Palette erkennen wird.
ms.assetid: 64ec1042-0ab5-496f-9a88-2f293b412704
title: WM_PALETTEISCHANGING Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2127dc9c682bba1fc4cea4e10b2b96ecc92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757878"
---
# <a name="wm_paletteischanging-message"></a>WM \_ paletteischanging-Meldung

Die **WM \_ paletteischanging** -Nachricht informiert Anwendungen darüber, dass eine Anwendung ihre logische Palette erkennen wird.

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

Ein Handle für das Fenster, in dem die logische Palette erkannt wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Die Anwendung, die die Palette ändert, wartet nicht auf die Bestätigung dieser Nachricht, bevor die Palette geändert und die [**WM \_ palettechanged**](wm-palettechanged.md) -Nachricht gesendet wird. Folglich wird die Palette möglicherweise bereits geändert, wenn eine Anwendung diese Nachricht empfängt.

Wenn die Anwendung diese Nachricht ignoriert oder nicht verarbeitet, und eine zweite Anwendung ihre Palette erkennt, während die erste Palette-Indizes verwendet, besteht die Möglichkeit, dass der Benutzer bei nachfolgenden Zeichnungs Vorgängen unerwartete Farben erkennt.

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

[**WM \_ querynewpalette**](wm-querynewpalette.md)
</dt> </dl>

 

 
