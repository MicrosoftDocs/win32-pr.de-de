---
title: DRV_QUERYCONFIGURE Meldung (MMSYSTEM. h)
description: Weist den Treiber an, anzugeben, ob die benutzerdefinierte Konfiguration unterstützt wird.
ms.assetid: fb2e36a7-8d6b-4b08-b2d7-e128ca7082dc
keywords:
- DRV_QUERYCONFIGURE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_QUERYCONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66780106fdd42364d247db534a838842f25dc16a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213738"
---
# <a name="drv_queryconfigure-message"></a>DRV- \_ queryconfigure-Meldung

Weist den Treiber an, anzugeben, ob die benutzerdefinierte Konfiguration unterstützt wird.

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

Gibt einen Wert ungleich 0 (null) zurück, wenn der Treiber ein Konfigurations Dialogfeld anzeigen kann, andernfalls NULL.

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

 

 





