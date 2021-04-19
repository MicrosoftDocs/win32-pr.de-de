---
description: Die lineagentstate- \_ Konstanten beschreiben den Status eines Agents für eine Adresse.
ms.assetid: 1dbc33e7-05cc-4cb9-8904-f495b884b8db
title: LINEAGENTSTATE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b5afa8f93cfde5529f8f57fd8e48d37ecd415b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362132"
---
# <a name="lineagentstate_-constants"></a>Lineagentstate- \_ Konstanten

Die **lineagentstate- \_ Konstanten** beschreiben den Status eines Agents für eine Adresse.

<dl> <dt>

<span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**lineagentstate \_ busyacd**
</dt> <dd> <dl> <dt>



Der Agent ist ausgelastet, um einen von einer ACD-Warteschlange gerouteten Befehl zu verarbeiten


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**lineagentstate \_ busyincoming**
</dt> <dd> <dl> <dt>



Der Agent verarbeitet einen eingehenden-Befehl, der nicht aus einer ACD-Warteschlange, in der der Agent angemeldet ist, an den Agent übertragen wurde.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**lineagentstate- \_ busyother**
</dt> <dd> <dl> <dt>



Der Agent beschäftigt sich mit der Verarbeitung eines anderen Typs, z. b. eines ausgehenden persönlichen Aufrufes, der nicht von einer Vorhersage Dialer an den Agent übertragen Dieser Wert kann auch verwendet werden, wenn bekannt ist, dass der Agent bei einem-Befehl ausgelastet ist, aber der Typ des Aufrufes unbekannt ist.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**lineagentstate \_ busyoutbound**
</dt> <dd> <dl> <dt>



Der Agent ist ausgelastet, um einen ausgehenden-Befehl zu verarbeiten


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**lineagentstate \_ loggedoff**
</dt> <dd> <dl> <dt>



Es ist kein Agent für die Adresse angemeldet.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**lineagentstate \_ notready**
</dt> <dd> <dl> <dt>



Der Agent ist angemeldet, aber mit einer anderen Aufgabe als dem Ausführen eines Aufrufens (z. b. bei einer Unterbrechung) beschäftigt. Es sollten keine weiteren Aufrufe an den Agent weitergeleitet werden.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**lineagentstate ist \_ bereit**
</dt> <dd> <dl> <dt>



Der Agent ist zum Akzeptieren von Aufrufen bereit.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**"lineagentstate" \_ nicht erreichbar**
</dt> <dd> <dl> <dt>



Der Agent-Status ist unbekannt und wird nie bekannt werden. In [**lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)kann diese Bedingung auch durch das Mitglied " **dwagentstate** " dargestellt werden, das auf "0" festgelegt wird.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**lineagentstate \_ unbekannt**
</dt> <dd> <dl> <dt>



Der Agent-Status ist zurzeit unbekannt, kann aber später bekannt werden. Dies kann ein Übergangszustand sein, wenn eine Zeile oder Adresse zum ersten Mal geöffnet wird.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**lineagentstate \_ workingaftercall**
</dt> <dd> <dl> <dt>



Der Agent hat den vorangehenden-Befehl abgeschlossen, ist aber noch mit der Arbeit im Zusammenhang mit diesem-Befehl beschäftigt. Der Agent sollte keine weiteren Aufrufe empfangen.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die oberen 16 Bits dieses Satzes von Konstanten sind für gerätespezifische Erweiterungen reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




