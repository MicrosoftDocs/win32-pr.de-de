---
description: Die WM \_ DISPLAYCHANGE-Meldung wird an alle Fenster gesendet, wenn sich die Anzeigeauflösung geändert hat.
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: WM_DISPLAYCHANGE (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d28f5708618ada0d766b140f01ff81a9427f443abb89cf41ba2c743223fbc70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037438"
---
# <a name="wm_displaychange-message"></a>WM \_ DISPLAYCHANGE-Meldung

Die **WM \_ DISPLAYCHANGE-Meldung** wird an alle Fenster gesendet, wenn sich die Anzeigeauflösung geändert hat.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Die neue Bildtiefe der Anzeige in Bits pro Pixel.

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort in niedriger Reihenfolge gibt die horizontale Auflösung des Bildschirms an.

Das obere Wort gibt die vertikale Auflösung des Bildschirms an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Meldung wird nur an Fenster der obersten Ebene gesendet. Für alle anderen Fenster wird sie veröffentlicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Das Zeichnen und Zeichnen](painting-and-drawing.md)
</dt> <dt>

[Zeichnen und Zeichnen von Nachrichten](painting-and-drawing-messages.md)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

 
