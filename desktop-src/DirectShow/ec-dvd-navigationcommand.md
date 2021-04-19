---
description: Wird gesendet, wenn der DVD-Navigator einen DVD-Navigations Befehl verarbeitet.
ms.assetid: 95e502b6-330f-4bc7-8adc-851913987370
title: EC_DVD_NavigationCommand (dvdevcode. h)
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
ms.openlocfilehash: e81dbf108868cbaec4c44a436f2c8271bb5f282a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370629"
---
# <a name="ec_dvd_navigationcommand"></a>EC \_ DVD \_ navigationcommand

Wird gesendet, wenn der [DVD-Navigator](dvd-navigator-filter.md) einen DVD-Navigations Befehl verarbeitet.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Die unteren 32 Bits des rohnavigations Befehls.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Die oberen 32 Bits des rohnavigations Befehls.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis ist standardmäßig deaktiviert. Um dieses Ereignis zu aktivieren, müssen Sie [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) aufrufen und die Option " **DVD \_ enableloggingevents** " auf " **true**" festlegen.

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

 

 




