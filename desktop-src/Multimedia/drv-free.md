---
title: DRV_FREE (Mmsystem.h)
description: Benachrichtigt den Treiber, dass er aus dem Arbeitsspeicher entfernt wird. Der Treiber sollte arbeitsspeicher- und andere Systemressourcen, die er zugeordnet hat, frei geben.
ms.assetid: 0447f8e9-4c4d-4be5-ab1f-ecd3e8cd2e67
keywords:
- DRV_FREE-Nachricht Windows Multimedia
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
ms.openlocfilehash: 21a558dc7a2c3ece040790b2351ff39dc3054d660eb9368567ed7ce79d40c8a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526210"
---
# <a name="drv_free-message"></a>DRV \_ FREE-Nachricht

Benachrichtigt den Treiber, dass er aus dem Arbeitsspeicher entfernt wird. Der Treiber sollte arbeitsspeicher- und andere Systemressourcen, die er zugeordnet hat, frei geben.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle der installierbaren Treiberinstanz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die *Parameter dwDriverId,* *lParam1* und *lParam2* werden nicht verwendet.

Die **DRV \_ FREE-Nachricht** ist immer die letzte Nachricht, die ein Gerätetreiber empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Installierbare Treiber](installable-drivers.md)
</dt> <dt>

[Installierbare Treibermeldungen](installable-driver-messages.md)
</dt> </dl>

 

 





