---
description: Signalisiert eine DVD-Fehlerbedingung.
ms.assetid: 2cd3e0c4-e2b7-4aa1-9f3c-9003eabfb08a
title: EC_DVD_ERROR (dvdevcode. h)
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
ms.openlocfilehash: 3b338889836bf78a334784ea66c0e346e9f6b672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369477"
---
# <a name="ec_dvd_error"></a>EC- \_ DVD- \_ Fehler

Signalisiert eine DVD-Fehlerbedingung.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD** -Wert, der den Fehlerzustand angibt. Member des enumerierten Datentyps des [**DVD- \_ Fehlers**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Bedeutung hängt vom Wert von *lParam1* ab. Weitere Informationen finden Sie unter [**DVD- \_ Fehler**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) .

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

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

 

 




