---
description: Die lineofferingmode \_ -bitflagkonstanten (TAPI-Versionen 1,4 und höher) beschreiben verschiedene Unterzustände eines Angebots Aufrufes.
ms.assetid: a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc
title: LINEOFFERINGMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b9e04720b4ea79f5b169e4a279a3af2e0cdda39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361406"
---
# <a name="lineofferingmode_-constants"></a>Lineofferingmode- \_ Konstanten

Die **lineofferingmode \_** -bitflagkonstanten (TAPI-Versionen 1,4 und höher) beschreiben verschiedene Unterzustände eines Angebots Aufrufes. Ein Modus ist als Aufruf Status für die Anwendung nach den Aufrufen State-trdansitionen für Angebot und innerhalb der [**line \_ CallState**](line-callstate.md) -Meldung verfügbar, die angibt, dass der Aufruf im linecallstate- \_ Angebot vorliegt. Diese Werte werden verwendet, wenn der Aufruf einer freigegebenen Adresse mit anderen Stationen (siehe [**lineaddresssharing- \_ Konstanten**](lineaddresssharing--constants.md)), primär elektronischer Schlüsselsysteme, erfolgt.

<dl> <dt>

<span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**lineofferingmode \_ aktiv**
</dt> <dd> <dl> <dt>



Gibt an, dass der Anruf an der aktuellen Station warnt (wird von linedevstate \_ -Klingel Meldungen begleitet), und wenn eine Anwendung für die automatische Beantwortung eingerichtet ist, kann Sie dies tun. Wenn der aufrufstatusmodus 0 (null) ist, sollte die Anwendung davon ausgehen, dass der Wert aktiv ist (Dies wäre die Situation bei einer nicht überbrücken Adresse). (TAPI-Versionen 1,4 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**lineofferingmode \_ inaktiv**
</dt> <dd> <dl> <dt>



Gibt an, dass der-Befehl an mehr als einer Station angeboten wird, aber die aktuelle Station hat keine Warnung (z. b. kann es sich um eine Aufsichts Station handeln, bei der der Angebots Status "Advisory" ist, z. b. blinkende eines Lichts); die Software auf der Stations Gruppe für die automatische Beantwortung sollte den Anruf vorzugsweise nicht beantworten, da dies das Vorrecht an der primären (Warnungs-) Station sein sollte, aber [**lineanswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) kann verwendet werden, um den Anruf zu verbinden. (TAPI-Versionen 1,4 und höher)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Nicht erweiterbar. Alle 32 Bits sind reserviert.

Aus Gründen der Abwärtskompatibilität liegt es in der Verantwortung des Dienstanbieters, die ausgehandelte API-Version in der Zeile zu untersuchen und diese lineofferingmode-Werte nicht zu verwenden, \_ Wenn Sie von der ausgehandelten Version nicht unterstützt werden. Anwendungen, die nicht von lineofferingmode erkannt werden, \_ nehmen wahrscheinlich an, dass sich ein im linecallstate-Angebot vorgegander Vorgang \_ im lineofferingmode-Modus befindet \_ .

Die inaktiven Werte für "lineofferingmode" \_ und "lineofferingmode" \_ werden verwendet, wenn sich der Aufruf auf einer Adresse befindet, die mit anderen Stationen gemeinsam genutzt wird (überbrückt; siehe [lineaddresssharing- \_ Konstanten](lineaddresssharing--constants.md)), primär mit elektronischen Schlüssel Systemen. Wenn der Anruf Zustands Modus des Angebots "aktiv" ist, bedeutet dies, dass der Anruf an der aktuellen Station warnt (wird von linedevstate \_ -Nachrichten begleitet), und wenn eine Anwendung für die automatische Beantwortung eingerichtet ist, kann Sie dies tun. Wenn der CallState-Modus "inaktiv" ist, wird der-Befehl auf mehreren Stationen angeboten, aber die aktuelle Station hat keine Warnung (es kann sich z. b. um eine Aufsichts Station handeln, bei der der Angebots Status "Advisory" ist, wie z. b. das Blinken eines Lichts). die Software auf der Stations Gruppe für die automatische Beantwortung sollte den Anruf vorzugsweise nicht beantworten, da dies das Vorrecht an der primären (Warnungs-) Station sein sollte, aber [**lineanswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) kann verwendet werden, um den Anruf zu verbinden. Wenn der aufrufstatusmodus 0 (null) ist, sollte die Anwendung davon ausgehen, dass der Wert aktiv ist (Dies wäre die Situation bei einer nicht überbrücken Adresse).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




