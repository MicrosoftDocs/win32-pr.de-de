---
description: Signalisiert, dass ein bestimmter DVD-Navigator-Befehl abgeschlossen wurde.
ms.assetid: f460db8e-b966-41fa-bfa1-4ad3fa65c3e3
title: EC_DVD_CMD_END (dvdevcode. h)
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
ms.openlocfilehash: 550a3969ba431127b05234a0c9fe38eb5938ebf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370531"
---
# <a name="ec_dvd_cmd_end"></a>EC- \_ DVD- \_ cmd- \_ Ende

Signalisiert, dass ein bestimmter [DVD-Navigator](dvd-navigator-filter.md) -Befehl abgeschlossen wurde.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Befehls Bezeichner. Übergeben Sie diesen Parameter an die [**IDvdInfo2:: getcmdfromevent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) -Methode, um einen [**idvdcmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) -Schnittstellen Zeiger abzurufen.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**HRESULT** -Wert, der den Status des Befehls angibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird nur ausgelöst, wenn die Anwendung das Flag \_ sendevents für das DVD-cmd- \_ Flag \_ in einer [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -Methode festlegt, die ein [**DVD- \_ cmd- \_ Flags**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) -Flag annimmt.

Dieses Ereignis wird in der Titel Domäne ausgelöst.

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
</dt> <dt>

[Synchronisieren von DVD-Befehlen](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




