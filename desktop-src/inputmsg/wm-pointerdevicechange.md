---
title: WM_POINTERDEVICECHANGE Meldung
description: Wird an ein Fenster gesendet, wenn eine Änderung in den Einstellungen eines Monitors vorliegt, dem ein Digitalisierer angefügt ist. Diese Meldung enthält Informationen zur Skalierung des Anzeigemodus.
ms.assetid: 9ED01D4C-58B4-4A21-B510-784281F9A909
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERDEVICECHANGE Nachricht
topic_type:
- apiref
api_name:
- WM_POINTERDEVICECHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 38f570059f374f64e393e960a8458e605983d6c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340353"
---
# <a name="wm_pointerdevicechange-message"></a>WM_POINTERDEVICECHANGE Meldung

Wird an ein Fenster gesendet, wenn eine Änderung in den Einstellungen eines Monitors vorliegt, dem ein Digitalisierer angefügt ist. Diese Meldung enthält Informationen zur Skalierung des Anzeigemodus.

> \[! Wichtig\]  
> Desktop-Apps sollten dpi-fähig sein. Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen. Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERDEVICECHANGE       0X238
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält einen Wert aus [**Zeiger-Geräte Änderungs Konstanten**](pointer-device-change-constants.md).

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

 

