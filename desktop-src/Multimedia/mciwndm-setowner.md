---
title: MCIWNDM_SETOWNER Meldung (VFW. h)
description: Die mciwndm \_ SetOwner-Nachricht legt das Fenster fest, um dem mciwnd-Fenster zugeordnete Benachrichtigungs Meldungen zu empfangen. Sie können diese Nachricht explizit oder mit dem mciwndltowner-Makro senden.
ms.assetid: c2d0f9d5-bf60-4036-a613-65ba1ed83110
keywords:
- MCIWNDM_SETOWNER-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETOWNER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3989632e83a65cda5e805bd91da3f502ca387d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104720"
---
# <a name="mciwndm_setowner-message"></a>Mciwndm- \_ Abmeldung

Die **mciwndm \_ SetOwner** -Nachricht legt das Fenster fest, um dem mciwnd-Fenster zugeordnete Benachrichtigungs Meldungen zu empfangen. Sie können diese Nachricht explizit oder mit dem [**mciwndltowner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) -Makro senden.


```C++
MCIWNDM_SETOWNER 
wParam = (WPARAM) hwndP; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*hwndp*
</dt> <dd>

Handle für das Fenster, um die Benachrichtigungs Meldungen zu empfangen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndseetowner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner)
</dt> </dl>

 

 





