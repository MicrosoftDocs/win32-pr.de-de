---
description: Signalisiert eine DVD-Fehlerbedingung.
ms.assetid: 2cd3e0c4-e2b7-4aa1-9f3c-9003eabfb08a
title: EC_DVD_ERROR (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ERROR
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c0afa9ce750016001ddbe054d8cb9a589a2c68d8856e8e4db5c59043eb881129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820527"
---
# <a name="ec_dvd_error"></a>\_ \_ EC-DVD-FEHLER

Signalisiert eine DVD-Fehlerbedingung.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD-Wert,** der die Fehlerbedingung angibt. Member des [**\_ aufzählten DVD**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) ERROR-Datentyps.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Die Bedeutung hängt vom Wert von *lParam1 ab.* Weitere Informationen finden Sie unter [**\_ DVD-FEHLER.**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error)

</dd> </dl>

## <a name="remarks"></a>Hinweise

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

 

 




