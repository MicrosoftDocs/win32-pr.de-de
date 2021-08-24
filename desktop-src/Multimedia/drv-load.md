---
title: DRV_LOAD (Mmsystem.h)
description: Benachrichtigt den Treiber, dass er geladen wurde. Der Treiber sollte sicherstellen, dass alle Hardware- und unterstützenden Treiber vorhanden sind, die er benötigt, um ordnungsgemäß zu funktionieren.
ms.assetid: f3642d91-cea8-499d-8d2e-bf01a59a7d72
keywords:
- DRV_LOAD-Nachricht Windows Multimedia
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
ms.openlocfilehash: d74b8d0663e96f0dc700739c7b8b5f9304d478ed02bf9493f24d03a506c14a61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678710"
---
# <a name="drv_load-message"></a>DRV \_ LOAD-Nachricht

Benachrichtigt den Treiber, dass er geladen wurde. Der Treiber sollte sicherstellen, dass alle Hardware- und unterstützenden Treiber vorhanden sind, die er benötigt, um ordnungsgemäß zu funktionieren.

## <a name="parameters"></a>Parameter

Der *hdrvr-Parameter* ist immer 0 (null). Die *Parameter dwDriverId,* *lParam1* und *lParam2* werden nicht verwendet.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Die **DRV \_ LOAD-Nachricht** ist immer die erste Nachricht, die ein Gerätetreiber empfängt.

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

 

 





