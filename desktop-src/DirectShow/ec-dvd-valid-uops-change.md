---
description: Signalisiert, dass sich der verfügbare Satz von IDvdControl2-Schnittstellenmethoden geändert hat.
ms.assetid: dfe698b9-abe5-44a7-9844-f408f11fd0ce
title: EC_DVD_VALID_UOPS_CHANGE (Dvdevcode.h)
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
ms.openlocfilehash: fafdbb5443a32a8029ad73d92a2b23c5f05c96d5dfc32375fd05e6d4502484a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051810"
---
# <a name="ec_dvd_valid_uops_change"></a>EC \_ DVD \_ VALID \_ UOPS \_ CHANGE

Signalisiert, dass sich der verfügbare Satz von [**IDvdControl2-Schnittstellenmethoden**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) geändert hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD-Wert,** der eine Kombination aus null oder mehr Flags aus der [**VALID \_ UOP \_ FLAG-Enumeration**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) enthält. Die Bits geben an, welche [**IDvdControl2-Befehle**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) explizit vom DVD-Datenträger deaktiviert wurden.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieses Ereignis gibt nur an, welche Vorgänge vom Inhalt auf dem DVD-Datenträger explizit deaktiviert werden. Es garantiert nicht, dass es gültig ist, Methoden aufzurufen, die nicht deaktiviert sind. Wenn beispielsweise keine Schaltflächen vorhanden sind, funktioniert die [**IDvdControl2::ActivateButton-Methode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) nicht, auch wenn die Methode nicht explizit deaktiviert ist.

Dieses Ereignis wird in allen Domänen ausgelöst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdevcode.h (include Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> <dt>

[DVD-Ereignisbenachrichtigungscodes](dvd-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




