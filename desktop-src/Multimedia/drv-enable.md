---
title: DRV_ENABLE Meldung (MMSYSTEM. h)
description: Aktiviert den Treiber. Der Treiber sollte alle Variablen initialisieren und Geräte mit der Eingabe-und Ausgabeschnittstelle (e/a) suchen.
ms.assetid: 8aa36f3d-b36c-4460-859c-108a7a450ae5
keywords:
- DRV_ENABLE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_ENABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569b4ca5f3d0dc5f439b1e2b0e25887ffd1da4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957170"
---
# <a name="drv_enable-message"></a>DRV- \_ Aktivierungs Nachricht

Aktiviert den Treiber. Der Treiber sollte alle Variablen initialisieren und Geräte mit der Eingabe-und Ausgabeschnittstelle (e/a) suchen.

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

Treiber werden ab dem Zeitpunkt, an dem Sie diese Nachricht empfangen, als aktiviert eingestuft, bis Sie mithilfe der [**drv- \_**](drv-disable.md) Deaktivierungs Nachricht deaktiviert werden.

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

 

 





