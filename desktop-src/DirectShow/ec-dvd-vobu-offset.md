---
description: 'EC_DVD_VOBU_Offset: Wird gesendet, wenn der DVD-Navigator ein PCI-Paket analysiert.'
ms.assetid: e2e65007-7c34-4be4-86b9-9491061891e5
title: EC_DVD_VOBU_Offset (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Offset
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 9223f2d5bb25d7b950dba8fb19c152cf3184af93
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119768"
---
# <a name="ec_dvd_vobu_offset"></a>EC \_ DVD \_ VOBU \_ Offset

Wird gesendet, wenn [der DVD-Navigator](dvd-navigator-filter.md) ein PCI-Paket analysiert.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Der Blockoffset der letzten Videoobjekteinheit (VOBU).

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Die aktuelle Anzahl von Videotiteln (VTSN).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis ist standardmäßig deaktiviert. Um dieses Ereignis zu aktivieren, rufen Sie [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) auf, und legen Sie die **Option DVD \_ EnableLoggingEvents** auf **TRUE fest.**

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
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

 

 




