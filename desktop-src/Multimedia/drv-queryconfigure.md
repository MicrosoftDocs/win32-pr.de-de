---
title: DRV_QUERYCONFIGURE (Mmsystem.h)
description: Leitet den Treiber an anzugeben, ob er benutzerdefinierte Konfiguration unterstützt.
ms.assetid: fb2e36a7-8d6b-4b08-b2d7-e128ca7082dc
keywords:
- DRV_QUERYCONFIGURE von Windows Multimedia
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
ms.openlocfilehash: 22c49ec54d1822bbc9ddc4d2606f8905a21c5193322a12df335549074dacdea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691570"
---
# <a name="drv_queryconfigure-message"></a>DRV \_ QUERYCONFIGURE-Meldung

Leitet den Treiber an anzugeben, ob er benutzerdefinierte Konfiguration unterstützt.

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

Gibt einen Wert ungleich 0 (null) zurück, wenn der Treiber ein Konfigurationsdialogfeld anzeigen kann, andernfalls 0 (null).

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

 

 





