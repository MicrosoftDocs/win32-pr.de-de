---
description: Die Meldung "WM \_ Display Change" wird an alle Fenster gesendet, wenn sich die Bildschirmauflösung geändert hat.
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: WM_DISPLAYCHANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 682612529fd40b22481612bb26a954bec45e3901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215642"
---
# <a name="wm_displaychange-message"></a>WM \_ Display Change-Meldung

Die Meldung " **WM \_ Display Change** " wird an alle Fenster gesendet, wenn sich die Bildschirmauflösung geändert hat.

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

Die neue Bildtiefe der Anzeige in Bits pro Pixel.

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort gibt die horizontale Auflösung des Bildschirms an.

Das höchst wertige Wort gibt die vertikale Auflösung des Bildschirms an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird nur an Fenster der obersten Ebene gesendet. Für alle anderen Fenster wird Sie gepostet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über das Zeichnen und zeichnen](painting-and-drawing.md)
</dt> <dt>

[Zeichnen und Zeichnen von Nachrichten](painting-and-drawing-messages.md)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

 
