---
description: Signalisiert, dass sich die Anzahl der DVD-Menü Schaltflächen geändert hat oder dass sich die Schaltflächen Auswahl geändert hat.
ms.assetid: af6c841d-ca06-4535-b418-14409fa78c81
title: EC_DVD_BUTTON_CHANGE (dvdevcode. h)
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
ms.openlocfilehash: 8647c1100e5cca6897e2068b2a20119a8f047396
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370259"
---
# <a name="ec_dvd_button_change"></a>EC- \_ DVD- \_ Schaltflächen \_ Änderung

Signalisiert, dass sich die Anzahl der DVD-Menü Schaltflächen geändert hat oder dass sich die Schaltflächen Auswahl geändert hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD** -Wert, der die Anzahl der verfügbaren Schaltflächen angibt.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**DWORD** -Wert, der die aktuell ausgewählte Schaltflächen Nummer angibt. Die ausgewählte Schaltflächen Nummer 0 bedeutet, dass keine Schaltfläche ausgewählt ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Schaltflächen Nummern liegen zwischen 1 und 36.

Die aktuell ausgewählte Schaltfläche kann sich automatisch ändern, wenn ein Navigations Befehl auf der Festplatte und mithilfe der [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -Schnittstelle auf der Festplatte erstellt wurde.

Dieses Ereignis kann allen verfügbaren Schaltflächen Nummern signalisieren. Diese Zahlen entsprechen nicht immer den für [**IDvdControl2:: selectandactivatebutton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) verwendeten Schaltflächen Nummern, da von dieser Methode nur eine Teilmenge der Schaltflächen aktiviert werden kann.

Dieses Ereignis wird in allen Domänen ausgelöst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdevcode. h (Include DShow. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> <dt>

[DVD-Ereignis Benachrichtigungs Codes](dvd-notification-codes.md)
</dt> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




