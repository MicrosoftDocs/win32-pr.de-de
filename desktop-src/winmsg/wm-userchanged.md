---
description: Wird an alle Fenster gesendet, nachdem sich der Benutzer angemeldet hat. Wenn sich der Benutzer anmeldet oder anmeldet, aktualisiert das System die benutzerspezifischen Einstellungen. Das System sendet diese Nachricht sofort nach dem Aktualisieren der Einstellungen.
title: WM_USERCHANGED Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_userchanged.htm
api_name:
- WM_USERCHANGED
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14458bdafa0bbf4421c67db8102491db4e1fe6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960656"
---
# <a name="wm_userchanged-message"></a>WM \_ userchanged-Meldung

Wird an alle Fenster gesendet, nachdem sich der Benutzer angemeldet hat. Wenn sich der Benutzer anmeldet oder anmeldet, aktualisiert das System die benutzerspezifischen Einstellungen. Das System sendet diese Nachricht sofort nach dem Aktualisieren der Einstellungen.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.

> [!Note]  
> Diese Meldung wird ab Windows Vista nicht unterstützt.

 


```C++
#define WM_USERCHANGED                  0x0054
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

Typ: **LRESULT**

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über Windows](windows.md)
</dt> </dl>

 

 
