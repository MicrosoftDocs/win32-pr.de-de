---
description: Wird gesendet, wenn ein Satz von DVD-Navigationsbefehlen gestartet wird.
ms.assetid: 9cdcb211-a9e3-4a15-81bd-7ada2b9d823a
title: EC_DVD_BeginNavigationCommands (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BeginNavigationCommands
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e0c39b43fc29ed5fadcac0e85ff23ef9f1945a25e26bcfdb0f1e81f804abbc07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965900"
---
# <a name="ec_dvd_beginnavigationcommands"></a>\_EC-DVD \_ BeginNavigationCommands

Wird gesendet, wenn ein Satz von DVD-Navigationsbefehlen gestartet wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Ein Wert aus der [**DVD \_ NavCmdType-Enumeration.**](/windows/win32/api/strmif/ne-strmif-dvd_navcmdtype)

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieses Ereignis ist standardmäßig deaktiviert. Um dieses Ereignis zu aktivieren, rufen [**Sie IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) auf, und legen Sie die **Option DVD \_ EnableLoggingEvents** auf **TRUE** fest.

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

 

 




