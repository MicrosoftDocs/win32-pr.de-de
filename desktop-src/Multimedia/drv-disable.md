---
title: DRV_DISABLE Meldung (MMSYSTEM. h)
description: Deaktiviert den Treiber. Der Treiber sollte das entsprechende Gerät (sofern vorhanden) in einen inaktiven Zustand versetzen und alle Rückruf Funktionen oder Threads beenden.
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- DRV_DISABLE-Nachricht (Multimedia)
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
ms.openlocfilehash: b512e90612a02681008474c7f1323f17304422d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957168"
---
# <a name="drv_disable-message"></a>DRV-Deaktivierungs \_ Meldung

Deaktiviert den Treiber. Der Treiber sollte das entsprechende Gerät (sofern vorhanden) in einen inaktiven Zustand versetzen und alle Rückruf Funktionen oder Threads beenden.

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

Nach der Deaktivierung des Treibers sendet das System in der Regel eine [**drv- \_ freie drv**](drv-free.md) -Nachricht, bevor der Treiber aus dem Arbeitsspeicher entfernt wird.

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

 

 





