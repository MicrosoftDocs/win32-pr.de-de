---
description: Die lineagentstateex- \_ Konstanten beschreiben den Status eines Agents für eine Adresse.
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: LINEAGENTSTATEEX_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 214b816a35e3fdb420a9d95772c466791c6d2f2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352130"
---
# <a name="lineagentstateex_-constants"></a>Lineagentstateex- \_ Konstanten

Die **lineagentstateex- \_ Konstanten** beschreiben den Status eines Agents für eine Adresse.

<dl> <dt>

<span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**lineagentstateex \_ busyacd**
</dt> <dd> <dl> <dt>



Der Agent ist ausgelastet, um einen von einer ACD-Warteschlange gerouteten Befehl zu verarbeiten


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**lineagentstateex \_ busyincoming**
</dt> <dd> <dl> <dt>



Der Agent verarbeitet einen eingehenden-Befehl, der nicht aus einer ACD-Warteschlange, in der der Agent angemeldet ist, an den Agent übertragen wurde.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**lineagentstateex \_ busyoutgoing**
</dt> <dd> <dl> <dt>



Der Agent ist ausgelastet, um einen ausgehenden-Befehl zu verarbeiten


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**lineagentstateex \_ notready**
</dt> <dd> <dl> <dt>



Der Agent ist angemeldet, aber mit einer anderen Aufgabe als dem Ausführen eines Aufrufens (z. b. bei einer Unterbrechung) beschäftigt. Es sollten keine weiteren Aufrufe an den Agent weitergeleitet werden.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**lineagentstateex ist \_ bereit**
</dt> <dd> <dl> <dt>



Der Agent ist zum Akzeptieren von Aufrufen bereit.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**lineagentstateex \_ veröffentlicht**
</dt> <dd> <dl> <dt>



Der Agent wurde freigegeben, wahrscheinlich weil Sie sich abgemeldet haben.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**lineagentstateex \_ unbekannt**
</dt> <dd> <dl> <dt>



Der Agent-Status ist zurzeit unbekannt, kann aber später bekannt werden. Dies kann ein Übergangszustand sein, wenn eine Zeile oder Adresse zum ersten Mal geöffnet wird.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,2<br/>                                                      |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




