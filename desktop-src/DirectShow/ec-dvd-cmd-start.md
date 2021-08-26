---
description: Signalisiert, dass ein DVD Navigator-Befehl gestartet wurde.
ms.assetid: 230116b4-23f1-4c37-a781-da2c5aa20a1f
title: EC_DVD_CMD_START (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 418163b55699f8ba7c38026764f3326985d7e1788369729f42067cff62a56949
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998080"
---
# <a name="ec_dvd_cmd_start"></a>EC \_ DVD \_ CMD \_ START

Signalisiert, dass [ein DVD Navigator-Befehl](dvd-navigator-filter.md) gestartet wurde.

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

Dieses Ereignis wird nur ausgelöst, wenn Ihre Anwendung das **FLAG \_ SENDEvents des DVD-CMD-FLAGs \_ \_** in einer [**IDvdControl2-Methode**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) fest legt, die ein [**\_ DVD-CMD-FLAGS-Flag \_**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) verwendet.

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

 

 




