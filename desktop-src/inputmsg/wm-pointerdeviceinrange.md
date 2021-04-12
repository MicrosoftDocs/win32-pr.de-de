---
title: WM_POINTERDEVICEINRANGE Meldung
description: Wird an ein Fenster gesendet, wenn ein Zeiger Gerät innerhalb des Bereichs eines eingabedigitalisierers erkannt wird. Diese Meldung enthält Informationen zum Gerät und seiner Nähe.
ms.assetid: 04244758-E662-4FB2-850E-20B4B3D1294A
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERDEVICEINRANGE Nachricht
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEINRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 76ab6ac4f96d1df4e4e29afbcefe86d34b8b602d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518767"
---
# <a name="wm_pointerdeviceinrange-message"></a>WM_POINTERDEVICEINRANGE Meldung

Wird an ein Fenster gesendet, wenn ein Zeiger Gerät innerhalb des Bereichs eines eingabedigitalisierers erkannt wird. Diese Meldung enthält Informationen zum Gerät und seiner Nähe.

> \[! Wichtig\]  
> Desktop-Apps sollten dpi-fähig sein. Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen. Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERDEVICEINRANGE       0X239
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Zusätzliche meldungsspezifische Informationen.

</dd> <dt>

*lParam* 
</dt> <dd>

Zusätzliche meldungsspezifische Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meldungen](messages.md)
</dt> </dl>

 

