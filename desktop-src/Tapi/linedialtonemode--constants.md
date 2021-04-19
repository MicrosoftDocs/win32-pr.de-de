---
description: Die Bitflag-Konstanten von linedialtonemode \_ beschreiben verschiedene Typen von Wähltönen. Ein spezieller Wählton weist in der Regel eine besondere Bedeutung auf (wie beim Warten auf die Nachricht).
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: LINEDIALTONEMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5128f2a176f3aeaf92bc3487b131b7720568085e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360297"
---
# <a name="linedialtonemode_-constants"></a>Linedialtonemode- \_ Konstanten

Die Bitflag-Konstanten von **linedialtonemode \_** beschreiben verschiedene Typen von Wähltönen. Ein spezieller Wählton weist in der Regel eine besondere Bedeutung auf (wie beim Warten auf die Nachricht).

<dl> <dt>

<span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**linedialtonemode \_ extern**
</dt> <dd> <dl> <dt>



Dies ist ein externer (öffentlicher Netzwerk) Wählton.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**linedialtonemode \_ intern**
</dt> <dd> <dl> <dt>



Dies ist ein interner Wählton, wie in einer PBX.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**linedialtonemode \_ Normal**
</dt> <dd> <dl> <dt>



Dies ist ein normaler Wählton, bei dem es sich in der Regel um einen kontinuierlichen Ton handelt.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**linedialtonemode \_ Special**
</dt> <dd> <dl> <dt>



Dies ist ein spezieller Wählton, der angibt, dass eine bestimmte Bedingung (die vom Switch oder Netzwerk bekannt ist) zurzeit wirksam ist. Bei speziellen Wähltönen wird normalerweise ein unterbrochener Ton verwendet. Wie bei einem normalen Wählton zeigt dies an, dass der Switch zum Empfangen der zu wählenden Zahl bereit ist.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**"linedialtonemode" \_ nicht verfügbar**
</dt> <dd> <dl> <dt>



Der Wähl Modus ist nicht verfügbar und wird nicht bekannt.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**"linedialtonemode" ist \_ unbekannt.**
</dt> <dd> <dl> <dt>



Der Dial-Tone-Modus ist zurzeit nicht bekannt, kann aber später bekannt werden.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die höherwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden. Die nieder wertigen 16 Bits sind reserviert.

Die **linedialtonemode- \_ Konstanten** werden in der [**linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) -Datenstruktur für einen-Rückruf im dialtoneverfahren-Zustand verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




