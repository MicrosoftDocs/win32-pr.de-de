---
description: Gibt die neue Domäne des DVD-Players an.
ms.assetid: 4faa46d6-2ba2-44a3-b237-acac3b32f8b1
title: EC_DVD_DOMAIN_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DOMAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: a43c44e779d8ad64852b673fb053467687c50daec85acb9bc87999675200d5f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965660"
---
# <a name="ec_dvd_domain_change"></a>\_ÄNDERUNG DER EC-DVD-DOMÄNE \_ \_

Gibt die neue Domäne des DVD-Players an.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD-Wert,** der die neue Domäne angibt. Member des [**aufzählten DVD \_ DOMAIN-Datentyps.**](/windows/win32/api/strmif/ne-strmif-dvd_domain)

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der DVD-Player signalisiert dieses Ereignis, wenn er Domänen ändert.

Dieses Ereignis wird in allen DVD-Domänen ausgelöst.

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

 

 




