---
title: MCIWNDM_SETINACTIVETIMER Meldung (VFW. h)
description: Die mciwndm \_ setinactivetimer-Nachricht legt den von mciwnd verwendeten Aktualisierungs Zeitraum fest, um die TrackBar im mciwnd-Fenster zu aktualisieren, Positionsinformationen zu aktualisieren, die in der Fenstertitelleiste angezeigt werden, und Benachrichtigungs Meldungen an das übergeordnete Fenster zu senden, wenn das mciwnd-Fenster inaktiv ist. Sie können diese Nachricht explizit oder mithilfe des Makros "mciwndsegtinactivetimer" senden.
ms.assetid: 8900c372-0493-4a63-a027-ef6ecf8f8254
keywords:
- MCIWNDM_SETINACTIVETIMER-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4504d84b254dfb67616568f5f97bba8e3bc2e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518251"
---
# <a name="mciwndm_setinactivetimer-message"></a>Mciwndm * \_ tinactivetimer-Nachricht

Die **mciwndm \_ setinactivetimer** -Nachricht legt den von mciwnd verwendeten Aktualisierungs Zeitraum fest, um die TrackBar im mciwnd-Fenster zu aktualisieren, Positionsinformationen zu aktualisieren, die in der Fenstertitelleiste angezeigt werden, und Benachrichtigungs Meldungen an das übergeordnete Fenster zu senden, wenn das mciwnd-Fenster inaktiv ist. Sie können diese Nachricht explizit oder mithilfe des Makros " [**mciwndsegtinactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) " senden.


```C++
MCIWNDM_SETINACTIVETIMER 
wParam = (WPARAM) (UINT) inactive; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*VSTE*
</dt> <dd>

Aktualisierungs Zeitraum in Millisekunden. Der Standardwert ist 2000 Millisekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndstitinactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
</dt> </dl>

 

 





