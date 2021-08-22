---
description: Wird gesendet, wenn der DVD-Navigator einen DVD-Navigationsbefehl verarbeitet.
ms.assetid: 95e502b6-330f-4bc7-8adc-851913987370
title: EC_DVD_NavigationCommand (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_NavigationCommand
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 6fbca42d3a9f0056bfd040b49e1426275a71bd7e6aaa8a71032389ab636f4cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119303360"
---
# <a name="ec_dvd_navigationcommand"></a>EC \_ DVD \_ NavigationCommand

Wird gesendet, wenn [der DVD-Navigator](dvd-navigator-filter.md) einen DVD-Navigationsbefehl verarbeitet.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Die unteren 32 Bits des unformatten Navigationsbefehls.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Die oberen 32 Bits des unformatten Navigationsbefehls.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieses Ereignis ist standardmäßig deaktiviert. Um dieses Ereignis zu aktivieren, rufen Sie [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) auf, und legen Sie die **Option DVD \_ EnableLoggingEvents** auf **TRUE fest.**

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

 

 




