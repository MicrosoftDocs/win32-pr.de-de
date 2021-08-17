---
title: DRV_DISABLE (Mmsystem.h)
description: Deaktiviert den Treiber. Der Treiber sollte das entsprechende Gerät in einem inaktiven Zustand platzieren und alle Rückruffunktionen oder Threads beenden.
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- DRV_DISABLE von Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_DISABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d9c5a99414f0b755efbae005365d89665a2b2bc5a4673436101066ec740564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144413"
---
# <a name="drv_disable-message"></a>DRV \_ DISABLE-Meldung

Deaktiviert den Treiber. Der Treiber sollte das entsprechende Gerät in einem inaktiven Zustand platzieren und alle Rückruffunktionen oder Threads beenden.

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

Nach dem Deaktivieren des Treibers sendet das System dem Treiber in der Regel eine [**DRV \_ FREE-Nachricht,**](drv-free.md) bevor der Treiber aus dem Arbeitsspeicher entfernt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Installierbare Treiber](installable-drivers.md)
</dt> <dt>

[Installierbare Treibermeldungen](installable-driver-messages.md)
</dt> </dl>

 

 





