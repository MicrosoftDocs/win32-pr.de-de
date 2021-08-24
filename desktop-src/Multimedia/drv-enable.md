---
title: DRV_ENABLE (Mmsystem.h)
description: Aktiviert den Treiber. Der Treiber sollte alle Variablen initialisieren und Geräte mit der Eingabe- und Ausgabeschnittstelle (E/A) suchen.
ms.assetid: 8aa36f3d-b36c-4460-859c-108a7a450ae5
keywords:
- DRV_ENABLE-Nachricht Windows Multimedia
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
ms.openlocfilehash: e7ab74abf08380db97a15da22fa99d58d72b6aba124a430cad665f65bc94e26c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526280"
---
# <a name="drv_enable-message"></a>DRV \_ ENABLE-Meldung

Aktiviert den Treiber. Der Treiber sollte alle Variablen initialisieren und Geräte mit der Eingabe- und Ausgabeschnittstelle (E/A) suchen.

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

Treiber gelten ab dem Zeitpunkt, zu dem sie diese Nachricht erhalten, als aktiviert, bis sie mithilfe der [**DRV \_ DISABLE-Meldung deaktiviert**](drv-disable.md) werden.

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

 

 





