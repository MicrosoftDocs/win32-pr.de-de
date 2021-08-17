---
title: DM_POINTERHITTEST-Nachricht
description: Wird an ein Fenster gesendet, wenn die Zeigereingabe zum ersten Mal erkannt wird, um das wahrscheinlichste Eingabeziel für die direkte Bearbeitung zu bestimmen.
ms.assetid: E4CE60F0-0C2A-440A-8F64-B070867A1572
keywords:
- 'DM_POINTERHITTEST-Nachricht: Eingabemeldungen und Benachrichtigungen'
topic_type:
- apiref
api_name:
- DM_POINTERHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9fda57a0c7084ae0c6ab85514244ed531a182108ec5dce7aae7794de2c38c903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482471"
---
# <a name="dm_pointerhittest-message"></a>DM_POINTERHITTEST-Nachricht

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Wird an ein Fenster gesendet, wenn die Zeigereingabe zum ersten Mal erkannt wird, um das wahrscheinlichste Eingabeziel für die direkte [Bearbeitung zu bestimmen.](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)

> \[! Wichtig\]  
> Desktop-Apps sollten DPI-bewusst sein. Wenn Ihre App keine DPI-Unterstützung hat, können Bildschirmkoordinaten, die in Zeigermeldungen und verwandten Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Writing High-DPI Win32 Applications ( Schreiben von Win32-Anwendungen mit hohem DPI-Code).](/previous-versions//dd464660(v=vs.85))

 


```C++
#define DM_POINTERHITTEST       0x0250
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

NULL

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Meldungen](messages.md)
</dt> </dl>

 

