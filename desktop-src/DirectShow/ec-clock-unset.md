---
description: Die Verbindung mit dem Uhranbieter wurde getrennt.
ms.assetid: 0a885b7a-840d-4112-85f7-ff6f2d87bb75
title: EC_CLOCK_UNSET (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd7bc9daecb9e39ca2d121c9fa903b2e4e8257e6247f28d718ca093b302cc2e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998220"
---
# <a name="ec_clock_unset"></a>EC \_ CLOCK \_ UNSET

Die Verbindung mit dem Uhranbieter wurde getrennt.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Keinen.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Der Filter Graph Manager wählt beim nächsten Befehl zum Anhalten oder Ausführen eine neue Referenzuhr aus. Außerdem wird das Ereignis an die Anwendung weitergeleitet.

## <a name="remarks"></a>Hinweise

KSProxy signalisiert dieses Ereignis, wenn die Verbindung mit dem Pin eines Uhrfilters getrennt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




