---
title: DRV_LOAD Meldung (MMSYSTEM. h)
description: Benachrichtigt den Treiber, dass er geladen wurde. Der Treiber sollte sicherstellen, dass Hardware und unterstützende Treiber, die für die ordnungsgemäße Funktion erforderlich sind, vorhanden sind.
ms.assetid: f3642d91-cea8-499d-8d2e-bf01a59a7d72
keywords:
- DRV_LOAD-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7dda950eaa84f924f4845d99d5740e37d6b354
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957165"
---
# <a name="drv_load-message"></a>DRV- \_ Lade Nachricht

Benachrichtigt den Treiber, dass er geladen wurde. Der Treiber sollte sicherstellen, dass Hardware und unterstützende Treiber, die für die ordnungsgemäße Funktion erforderlich sind, vorhanden sind.

## <a name="parameters"></a>Parameter

Der *hdrvr* -Parameter ist immer 0 (null). Die Parameter " *dwdriverid*", " *lParam1*" und " *lParam2* " werden nicht verwendet.

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn erfolgreich, andernfalls

## <a name="remarks"></a>Bemerkungen

Die **drv- \_ Lade** Nachricht ist immer die erste Meldung, die ein Gerätetreiber erhält.

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

 

 





