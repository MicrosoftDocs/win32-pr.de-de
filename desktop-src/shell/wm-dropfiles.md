---
description: Wird gesendet, wenn der Benutzer eine Datei im Fenster einer Anwendung löscht, die sich selbst als Empfänger von gelöschten Dateien registriert hat.
ms.assetid: 07dc2df7-4699-4e9c-b1a5-4ce877116268
title: WM_DROPFILES Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8362bfa746eaab519cdfc34d2cdf7757105fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979465"
---
# <a name="wm_dropfiles-message"></a>WM \_ dropfiles-Meldung

Wird gesendet, wenn der Benutzer eine Datei im Fenster einer Anwendung löscht, die sich selbst als Empfänger von gelöschten Dateien registriert hat.


```C++
PostMessage(
    (HWND) hWndControl,   // handle to destination control
    (UINT) WM_DROPFILES,  // message ID
    (WPARAM) wParam,      // = (WPARAM) (HDROP) hDrop;
    (LPARAM) lParam       // = 0; not used, must be zero 
);          
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDrop* 
</dt> <dd>

Ein Handle für eine interne-Struktur, die die gelöschten Dateien beschreibt. Übergeben Sie das Handle [**dragfinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**dragqueryfile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea)oder [**dragquerypoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) , um Informationen zu den gelöschten Dateien abzurufen.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Das HDROP-Handle wird in shellapi. h deklariert. Sie müssen diesen Header in Ihren Build einschließen, um **WM \_ dropfiles** zu verwenden. Weitere Informationen zur Verwendung von Drag & amp; Drop zum Übertragen von shelldaten finden Sie unter über [tragen von shelldaten per Drag & Drop oder Zwischenablage](dragdrop.md).

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**DragAcceptFiles**](/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles)
</dt> </dl>

 

 
