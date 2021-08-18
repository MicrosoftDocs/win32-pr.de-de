---
description: Signalisiert, dass ein bestimmter DVD Navigator-Befehl abgeschlossen wurde.
ms.assetid: f460db8e-b966-41fa-bfa1-4ad3fa65c3e3
title: EC_DVD_CMD_END (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_END
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 869da360f3321059df81a609d5ce953ad64f60485126fe7ae8f5e5a7df21753a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965880"
---
# <a name="ec_dvd_cmd_end"></a>EC \_ DVD \_ CMD \_ END

Signalisiert, dass ein [bestimmter DVD Navigator-Befehl](dvd-navigator-filter.md) abgeschlossen wurde.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Befehlsbezeichner. Übergeben Sie diesen Parameter an die [**IDvdInfo2::GetCmdFromEvent-Methode,**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) um einen [**IDvdCmd-Schnittstellenzeiger**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) abzurufen.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**HRESULT-Wert,** der den Status des Befehls angibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieses Ereignis wird nur ausgelöst, wenn Ihre Anwendung das FLAG \_ SENDEvents des DVD-CMD-FLAGs in einer IDvdControl2-Methode fest legt, die ein \_ \_ [**\_ DVD-CMD-FLAGS-Flag \_**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) verwendet. [](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)

Dieses Ereignis wird in der Titeldomäne ausgelöst.

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
</dt> <dt>

[Synchronisieren von DVD-Befehlen](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




