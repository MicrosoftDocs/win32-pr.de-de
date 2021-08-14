---
description: Signalisiert, dass sich die Anzahl der DVD-Menüschaltflächen geändert hat oder dass sich die Schaltflächenauswahl geändert hat.
ms.assetid: af6c841d-ca06-4535-b418-14409fa78c81
title: EC_DVD_BUTTON_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 61e74a967df18d5ba105eda1609a72c0db9770868bbd967c7a90f5e920dc954d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652746"
---
# <a name="ec_dvd_button_change"></a>\_ÄNDERUNG DER EC-DVD-SCHALTFLÄCHE \_ \_

Signalisiert, dass sich die Anzahl der DVD-Menüschaltflächen geändert hat oder dass sich die Schaltflächenauswahl geändert hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD-Wert,** der die Anzahl der verfügbaren Schaltflächen angibt.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**DWORD-Wert,** der die aktuell ausgewählte Schaltflächennummer angibt. Die ausgewählte Schaltflächennummer 0 bedeutet, dass keine Schaltfläche ausgewählt ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Schaltflächennummern liegen zwischen 1 und 36.

Die aktuell ausgewählte Schaltfläche kann mit einem navigationsbefehl, der auf dem Datenträger erstellt wurde, sowie über die Anwendungssteuerung mithilfe der [**IDvdControl2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) automatisch geändert werden.

Dieses Ereignis kann alle verfügbaren Schaltflächennummern signalisieren. Diese Zahlen entsprechen nicht immer schaltflächennummern, die für [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) verwendet werden, da diese Methode nur eine Teilmenge der Schaltflächen aktivieren kann.

Dieses Ereignis wird in allen Domänen ausgelöst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdevcode.h (include Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> <dt>

[DVD-Ereignisbenachrichtigungscodes](dvd-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




