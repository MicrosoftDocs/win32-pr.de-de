---
title: DRV_REMOVE Meldung (MMSYSTEM. h)
description: Benachrichtigt den Treiber, dass er aus dem System entfernt werden soll. Wenn ein Treiber diese Nachricht empfängt, sollte er alle Abschnitte entfernen, die er in der Registrierung erstellt hat.
ms.assetid: e4f6ce7c-29e5-4256-b08a-13571256207c
keywords:
- DRV_REMOVE-Nachricht (Multimedia)
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
ms.openlocfilehash: ccfc94d648f83e618a20323ed7bbe3694616bc06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040989"
---
# <a name="drv_remove-message"></a>DRV- \_ Entfernungs Meldung

Benachrichtigt den Treiber, dass er aus dem System entfernt werden soll. Wenn ein Treiber diese Nachricht empfängt, sollte er alle Abschnitte entfernen, die er in der Registrierung erstellt hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwdriverid*
</dt> <dd>

Der Bezeichner des installierbaren Treibers. Dabei handelt es sich um den gleichen Wert, der zuvor vom Treiber aus der von [**drv \_ geöffneten**](drv-open.md) Nachricht zurückgegeben wurde.

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle der installierbaren Treiber Instanz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die Parameter *lParam1* und *lParam2* werden nicht verwendet.

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

 

 





