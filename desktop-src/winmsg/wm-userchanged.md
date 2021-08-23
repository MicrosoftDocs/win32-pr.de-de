---
description: Wird an alle Fenster gesendet, nachdem sich der Benutzer angemeldet oder deaktiviert hat. Wenn sich der Benutzer anmeldet oder deaktiviert, aktualisiert das System die benutzerspezifischen Einstellungen. Das System sendet diese Meldung unmittelbar nach dem Aktualisieren der Einstellungen.
title: WM_USERCHANGED (Winuser.h)
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
ms.openlocfilehash: 2bb466e80070fe1be5cd7af7889fc5727c81f8caad89ad60c48c7a105b688fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705700"
---
# <a name="wm_userchanged-message"></a>WM \_ USERCHANGED-Nachricht

Wird an alle Fenster gesendet, nachdem sich der Benutzer angemeldet oder deaktiviert hat. Wenn sich der Benutzer anmeldet oder deaktiviert, aktualisiert das System die benutzerspezifischen Einstellungen. Das System sendet diese Meldung unmittelbar nach dem Aktualisieren der Einstellungen.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> [!Note]  
> Diese Meldung wird ab dem 1. Windows Vista nicht mehr unterstützt.

 


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

Eine Anwendung sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Windows Übersicht](windows.md)
</dt> </dl>

 

 
