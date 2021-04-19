---
description: Ein Filter empfängt nicht genügend Daten.
ms.assetid: c9cdfe46-02bb-4ea9-ac58-7d63e03c26d8
title: EC_STARVATION (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988d550b93ecb9a3c2f78f2d07f50a3965be945d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371981"
---
# <a name="ec_starvation"></a>EC- \_ Hunger

Ein Filter empfängt nicht genügend Daten.

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

Das Ereignis wird nicht an die Anwendung gesendet. Wenn das Filter Diagramm ausgeführt wird, hält der Filter Diagramm-Manager das Diagramm an und wartet auf den Abschluss der Pause. Anschließend wird das Diagramm erneut ausgeführt. Der Filter, der das Ereignis sendet, sollte seinen Übergang nicht beenden, um angehalten zu werden, bis genügend Daten zum Fortsetzen bereit stehen. Wenn das Filter Diagramm nicht ausgeführt wird, ignoriert der Filter Graph-Manager dieses Ereignis.

## <a name="remarks"></a>Bemerkungen

Wenn zu wenig Daten eintreffen, kann ein Parser oder Quell Filter dieses Ereignis senden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignis Benachrichtigungs Codes](event-notification-codes.md)
</dt> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




