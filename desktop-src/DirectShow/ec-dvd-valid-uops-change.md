---
description: Signalisiert, dass sich der verfügbare Satz von IDvdControl2-Schnittstellen Methoden geändert hat.
ms.assetid: dfe698b9-abe5-44a7-9844-f408f11fd0ce
title: EC_DVD_VALID_UOPS_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VALID_UOPS_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 26ab0674b504fac3fe374247f47ca20496b22ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366005"
---
# <a name="ec_dvd_valid_uops_change"></a>\_ \_ gültige \_ UOPs- \_ Änderung für EC-DVD

Signalisiert, dass sich der verfügbare Satz von [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -Schnittstellen Methoden geändert hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD** -Wert, der eine Kombination aus null oder mehr Flags aus der [**gültigen \_ UOP- \_ Flag**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) -Enumeration enthält. Die Bits geben an, welche [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -Befehle von der DVD-CD explizit deaktiviert wurden.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis gibt nur an, welche Vorgänge durch den Inhalt auf der DVD-CD explizit deaktiviert werden. Es ist nicht sichergestellt, dass es zulässig ist, nicht deaktivierte Methoden aufzurufen. Wenn z. b. keine Schaltflächen vorhanden sind, funktioniert die [**IDvdControl2:: activatebutton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) -Methode nicht, obwohl die Methode nicht explizit deaktiviert ist.

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

 

 




