---
description: Signalisiert eine DVD-Warnungsbedingung.
ms.assetid: d7221e8a-089f-4eaf-a193-548709c14336
title: EC_DVD_WARNING (Dvdevcode.h)
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
ms.openlocfilehash: a2f2d604b46a4c4bc2213fe74210defdf408336b69218589ff42209cebe025e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965560"
---
# <a name="ec_dvd_warning"></a>\_ \_ EC-DVD-WARNUNG

Signalisiert eine DVD-Warnungsbedingung.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD-Wert,** der die Warnungsbedingung angibt. Member des [**aufzählten DVD WARNING-Datentyps. \_**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning)

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Wenn *pParam1* gleich DVD \_ WARNING \_ Open, DVD WARNING Seek oder DVD \_ WARNING Read \_ \_ \_ ist, enthält *lParam2* den letzten von **GetLastError** zurückgegebenen Fehlercode.

</dd> </dl>

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

 

 




