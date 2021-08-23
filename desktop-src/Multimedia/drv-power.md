---
title: DRV_POWER (Mmsystem.h)
description: Benachrichtigt den Treiber, dass die Stromversorgung des Geräts ein- oder ausgeschaltet wird.
ms.assetid: b3bbd16a-5b90-4127-a1dd-f2ddfd918f0a
keywords:
- DRV_POWER-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_POWER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a6b9f3ddb2c0184337d2f53d73cdda8451a8d8df19229e505b08fedf685f40d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496450"
---
# <a name="drv_power-message"></a>DRV \_ POWER-Nachricht

Benachrichtigt den Treiber, dass die Stromversorgung des Geräts ein- oder ausgeschaltet wird.

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

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück.

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

 

 





