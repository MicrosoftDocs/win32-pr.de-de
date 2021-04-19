---
description: Signalisiert eine DVD-Warnungs Bedingung.
ms.assetid: d7221e8a-089f-4eaf-a193-548709c14336
title: EC_DVD_WARNING (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_WARNING
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 7f25d4565c2afeb4619f7832f6d5742e07dcca0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373657"
---
# <a name="ec_dvd_warning"></a>EC- \_ DVD- \_ Warnung

Signalisiert eine DVD-Warnungs Bedingung.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD** -Wert, der die Warnungs Bedingung angibt. Member des enumerierten Datentyps der [**DVD- \_ Warnung**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Wenn *pParam1* den Wert "DVD \_ Warning \_ Open", "DVD \_ Warning Seek" oder " \_ DVD \_ Warning Read" \_ aufweist, enthält *lParam2* den letzten von " **GetLastError**" zurückgegebenen Fehlercode.

</dd> </dl>

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

 

 




