---
title: MCIWNDM_SETACTIVETIMER Meldung (VFW. h)
description: Die mciwndm \_ setactivetimer-Nachricht legt den Update Zeitraum fest, der von mciwnd zum Aktualisieren der TrackBar im mciwnd-Fenster, Aktualisieren der Positionsinformationen, die in der Fenstertitelleiste angezeigt werden, und Senden von Benachrichtigungs Meldungen an das übergeordnete Fenster, wenn das mciwnd-Fenster aktiv ist. Sie können diese Nachricht explizit oder mit dem mciwndabtactivetimer-Makro senden.
ms.assetid: a30c0091-d9bb-44a3-a7b0-d1be30adcd9c
keywords:
- MCIWNDM_SETACTIVETIMER-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1924a991f0627009a8e622c8f8be086b2e045635
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104714"
---
# <a name="mciwndm_setactivetimer-message"></a>Mciwndm- \_ Nachricht

Die **mciwndm \_ setactivetimer** -Nachricht legt den Update Zeitraum fest, der von mciwnd zum Aktualisieren der TrackBar im mciwnd-Fenster, Aktualisieren der Positionsinformationen, die in der Fenstertitelleiste angezeigt werden, und Senden von Benachrichtigungs Meldungen an das übergeordnete Fenster, wenn das mciwnd-Fenster aktiv ist. Sie können diese Nachricht explizit oder mit dem [**mciwndabtactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) -Makro senden.


```C++
MCIWNDM_SETACTIVETIMER 
wParam = (WPARAM) (UINT) active; 
lParam = 0L; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*enden*
</dt> <dd>

Aktualisierungs Zeitraum in Millisekunden. Der Standardwert ist 500 Millisekunden.

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

[**Mciwndabtactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
</dt> </dl>

 

 





