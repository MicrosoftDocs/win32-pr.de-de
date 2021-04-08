---
title: DRV_FREE Meldung (MMSYSTEM. h)
description: Benachrichtigt den Treiber, dass er aus dem Arbeitsspeicher entfernt wird. Der Treiber sollte jeglichen Arbeitsspeicher und andere Systemressourcen freigeben, die er zugewiesen hat.
ms.assetid: 0447f8e9-4c4d-4be5-ab1f-ecd3e8cd2e67
keywords:
- DRV_FREE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_FREE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb9d70d269cb84e0d6ef0881618b67cfef11068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957167"
---
# <a name="drv_free-message"></a>Freie drv- \_ Nachricht

Benachrichtigt den Treiber, dass er aus dem Arbeitsspeicher entfernt wird. Der Treiber sollte jeglichen Arbeitsspeicher und andere Systemressourcen freigeben, die er zugewiesen hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle der installierbaren Treiber Instanz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die Parameter " *dwdriverid*", " *lParam1*" und " *lParam2* " werden nicht verwendet.

Die **\_ freie drv** -Nachricht ist immer die letzte Nachricht, die ein Gerätetreiber erhält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Installierbare Treiber](installable-drivers.md)
</dt> <dt>

[Installierbare Treiber Meldungen](installable-driver-messages.md)
</dt> </dl>

 

 





