---
description: Wird gesendet, nachdem ein Fenster verschoben wurde.
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: WM_MOVE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56004ec47266a50bf2ac82a828b9046c84a8ebfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363480"
---
# <a name="wm_move-message"></a>WM-Verschiebungs \_ Meldung

Wird gesendet, nachdem ein Fenster verschoben wurde.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) -Funktion.


```C++
#define WM_MOVE                         0x0003
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Die x-und y-Koordinaten der oberen linken Ecke des Client Bereichs des Fensters. Das nieder wertige Wort enthält die x-Koordinate, während das Haupt Wort die y-Koordinate enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Die Parameter werden in Bildschirm Koordinaten für überlappende und Popup Fenster sowie in den übergeordneten Client Koordinaten für untergeordnete Fenster angegeben.

Im folgenden Beispiel wird veranschaulicht, wie die Position aus dem *LPARAM* -Parameter abgerufen wird.


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



Sie können auch das [**makepoints**](/windows/win32/api/wingdi/nf-wingdi-makepoints) -Makro verwenden, um den *LPARAM* -Parameter in eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur zu konvertieren.

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion sendet die **WM- \_ Größe** und die WM-Verschiebungs Nachricht, wenn Sie die [**WM- \_ windowposchge**](wm-windowposchanged.md) -Nachricht verarbeitet. **\_**
Die **WM- \_ Größe** und die WM-Verschiebungs Nachricht werden nicht gesendet, wenn eine Anwendung die **WM- \_ windowposchangsnachricht** verarbeitet, ohne **defwindowproc** Aufrufs. **\_**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM-Windows-Server \_**](wm-windowposchanged.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Makepoints**](/windows/win32/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punkt**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

 
