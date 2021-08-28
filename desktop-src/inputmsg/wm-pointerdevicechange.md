---
title: WM_POINTERDEVICECHANGE Meldung
description: Wird an ein Fenster gesendet, wenn sich die Einstellungen eines Monitors ändern, an den ein Digitizer angefügt ist. Diese Meldung enthält Informationen zur Skalierung des Anzeigemodus.
ms.assetid: 9ED01D4C-58B4-4A21-B510-784281F9A909
keywords:
- WM_POINTERDEVICECHANGE Der Nachrichteneingabenachrichten und -benachrichtigungen
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
ms.openlocfilehash: 6d75a5afa245303952c5c6b1814b2f1ce77cd03da7c789d34bda2500c6bffee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829580"
---
# <a name="wm_pointerdevicechange-message"></a>WM_POINTERDEVICECHANGE Meldung

Wird an ein Fenster gesendet, wenn sich die Einstellungen eines Monitors ändern, an den ein Digitizer angefügt ist. Diese Meldung enthält Informationen zur Skalierung des Anzeigemodus.

> \[! Wichtig\]  
> Desktop-Apps sollten DPI-fähige Apps sein. Wenn Ihre App nicht DPI-bewusst ist, können Bildschirmkoordinaten, die in Zeigermeldungen und zugehörigen Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von Win32-Anwendungen mit hohem DPI-Anteil.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERDEVICECHANGE       0X238
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält einen Wert aus [**Zeigergeräteänderungskonstanten.**](pointer-device-change-constants.md)

</dd> <dt>

*lParam* 
</dt> <dd>

Zusätzliche meldungsspezifische Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte sie [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Meldungen](messages.md)
</dt> </dl>

 

