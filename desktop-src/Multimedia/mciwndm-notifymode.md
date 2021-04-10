---
title: MCIWNDM_NOTIFYMODE Meldung (VFW. h)
description: Die mciwndm \_ notifymode-Meldung benachrichtigt das übergeordnete Fenster einer Anwendung, dass sich der Betriebsmodus des MCI-Geräts geändert hat.
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- MCIWNDM_NOTIFYMODE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe75048a53023dab67bef4048d6149438ad54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040074"
---
# <a name="mciwndm_notifymode-message"></a>Mciwndm \_ notifymode-Meldung

Die **mciwndm \_ notifymode** -Meldung benachrichtigt das übergeordnete Fenster einer Anwendung, dass sich der Betriebsmodus des MCI-Geräts geändert hat.


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle für das mciwnd-Fenster.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*Spar*
</dt> <dd>

Eine Ganzzahl, die dem MCI-Modus entspricht.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können Benachrichtigungen über Änderungen im Modus eines MCI-Geräts aktivieren, indem Sie den mciwndf- \_ Fenster Stil "notifymode" angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





