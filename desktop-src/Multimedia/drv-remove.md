---
title: DRV_REMOVE (Mmsystem.h)
description: Benachrichtigt den Treiber, dass er aus dem System entfernt werden soll. Wenn ein Treiber diese Meldung empfängt, sollte er alle Abschnitte entfernen, die er in der Registrierung erstellt hat.
ms.assetid: e4f6ce7c-29e5-4256-b08a-13571256207c
keywords:
- DRV_REMOVE-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_REMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c08302d69e934ec77908b247f3c8f6368de8de4eab36809b6102b74858adde5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496420"
---
# <a name="drv_remove-message"></a>\_DRV-REMOVE-Meldung

Benachrichtigt den Treiber, dass er aus dem System entfernt werden soll. Wenn ein Treiber diese Meldung empfängt, sollte er alle Abschnitte entfernen, die er in der Registrierung erstellt hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Bezeichner des installierbaren Treibers. Dies ist der gleiche Wert, der zuvor vom Treiber von der [**DRV \_ OPEN-Nachricht zurückgegeben**](drv-open.md) wurde.

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle der installierbaren Treiberinstanz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die *Parameter lParam1* *und lParam2* werden nicht verwendet.

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

 

 





