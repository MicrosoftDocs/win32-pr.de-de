---
description: Gibt an, wann sich die aktuelle DVD-Titelnummer ändert.
ms.assetid: 9888f2ec-fc2d-4d6d-a03d-b381373337eb
title: EC_DVD_TITLE_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 667d8f11270865f1caa4549377db2cccb278053ea9848b71aa38f0d5f7528689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686210"
---
# <a name="ec_dvd_title_change"></a>ÄNDERUNG DES TITELS DER \_ EC-DVD \_ \_

Gibt an, wann sich die aktuelle DVD-Titelnummer ändert.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD-Wert,** der die neue Titelnummer angibt.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Titelnummern liegen zwischen 1 und 99. Diese Zahl gibt den TTN an, bei dem es sich um die Titelnummer in Bezug auf den gesamten Datenträger handelt, nicht den \_ VTS-TTN, bei dem es sich lediglich um die Titelnummer eines aktuellen VTS handelt.

Dieses Ereignis wird in der Titeldomäne ausgelöst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdevcode.h (include Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> <dt>

[DVD-Ereignisbenachrichtigungscodes](dvd-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




