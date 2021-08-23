---
description: Die WM \_ PALETTEISCHANGING-Nachricht informiert Anwendungen darüber, dass eine Anwendung ihre logische Palette umsetzen wird.
ms.assetid: 64ec1042-0ab5-496f-9a88-2f293b412704
title: WM_PALETTEISCHANGING Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b0de17e7957e4b03c0a8fb942e7c0e4f94a3329e53cb039ce1d7f0a8c33aa89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717680"
---
# <a name="wm_paletteischanging-message"></a>WM \_ PALETTEISCHANGING-Meldung

Die **WM \_ PALETTEISCHANGING-Nachricht** informiert Anwendungen darüber, dass eine Anwendung ihre logische Palette umsetzen wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Ein Handle für das Fenster, das seine logische Palette realisiert.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Die Anwendung, die ihre Palette ändert, wartet nicht auf die Bestätigung dieser Nachricht, bevor sie die Palette ändert und die [**WM \_ PALETTECHANGED-Nachricht**](wm-palettechanged.md) sendet. Daher kann die Palette bereits geändert werden, wenn eine Anwendung diese Nachricht empfängt.

Wenn die Anwendung diese Nachricht entweder ignoriert oder nicht verarbeitet und eine zweite Anwendung ihre Palette erkennt, während die erste Palettenindizes verwendet, besteht die starke Möglichkeit, dass dem Benutzer bei nachfolgenden Zeichnungsvorgängen unerwartete Farben angezeigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Farben](colors.md)
</dt> <dt>

[Farbmeldungen](color-messages.md)
</dt> <dt>

[**WM \_ PALETTECHANGED**](wm-palettechanged.md)
</dt> <dt>

[**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md)
</dt> </dl>

 

 
