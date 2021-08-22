---
description: Die \_ LINEOFFERINGMODE-Bitflagkonstanten (TAPI-Versionen 1.4 und höher) beschreiben verschiedene Unterstates eines Angebotsaufrufs.
ms.assetid: a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc
title: LINEOFFERINGMODE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c2c36d18d006cdc1e2d9fc79095d58b6f56f1e58f4939c4e08ec6936af6855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518910"
---
# <a name="lineofferingmode_-constants"></a>LINEOFFERINGMODE-Konstanten \_

Die **\_ LINEOFFERINGMODE-Bitflagkonstanten** (TAPI-Versionen 1.4 und höher) beschreiben verschiedene Unterstates eines Angebotsaufrufs. Ein Modus ist als Aufrufstatus für die Anwendung verfügbar, nachdem der Aufrufzustand trdansitions to offering ist, und innerhalb der [**LINE \_ CALLSTATE-Nachricht,**](line-callstate.md) die angibt, dass sich der Aufruf in LINECALLSTATE \_ OFFERING befindet. Diese Werte werden verwendet, wenn sich der Aufruf auf einer Adresse befindet, die mit anderen Stationen gemeinsam genutzt (überbrückt) wird (siehe [**LINEADDRESSSHARING-Konstanten \_**](lineaddresssharing--constants.md)), hauptsächlich elektronische Schlüsselsysteme.

<dl> <dt>

<span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE \_ ACTIVE**
</dt> <dd> <dl> <dt>



Gibt an, dass der Anruf an der aktuellen Station eine Warnung auslöst (wird von LINEDEVSTATE RINGING-Nachrichten begleitet), und wenn eine Anwendung für die automatische Antwort eingerichtet ist, kann sie dies \_ tun. Wenn der Aufrufzustandsmodus NULL ist, sollte die Anwendung davon ausgehen, dass der Wert aktiv ist (dies wäre die Situation bei einer nicht überbrückten Adresse). (TAPI-Versionen 1.4 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE \_ INACTIVE**
</dt> <dd> <dl> <dt>



Gibt an, dass der Anruf an mehreren Stationen angeboten wird, die aktuelle Station jedoch keine Warnungen anzeigt (z. B. kann es sich um eine begleitende Station mit dem Angebotsstatus "Beratung" (z. B. Blinken eines Lichts) handelt). Software an der Station, die für die automatische Antwort festgelegt ist, sollte den Anruf vorzugsweise nicht beantworten, da dies das Vorrecht an der primären (warnenden) Station sein sollte, aber [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) kann verwendet werden, um den Anruf zu verbinden. (TAPI-Versionen 1.4 und höher)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Nicht erweiterbar. Alle 32 Bits sind reserviert.

Aus Gründen der Abwärtskompatibilität ist der Dienstanbieter dafür verantwortlich, die ausgehandelte API-Version in der Zeile zu überprüfen und diese LINEOFFERINGMODE-Werte nicht zu \_ verwenden, wenn sie in der ausgehandelten Version nicht unterstützt werden. Anwendungen, die LINEOFFERINGMODE nicht kennen, \_ gehen höchstwahrscheinlich davon aus, dass sich ein Aufruf in LINECALLSTATE \_ OFFERING in LINEOFFERINGMODE \_ ACTIVE befindet.

Die WERTE LINEOFFERINGMODE \_ ACTIVE und LINEOFFERINGMODE \_ INACTIVE werden verwendet, wenn sich der Aufruf auf einer Adresse befindet, die für andere Stationen freigegeben wird (bridged; siehe [LINEADDRESSSHARING-Konstanten \_ ](lineaddresssharing--constants.md)), hauptsächlich elektronische Schlüsselsysteme. Wenn der Zustandsmodus des Angebotsaufrufs "aktiv" ist, bedeutet dies, dass der Anruf an der aktuellen Station benachrichtigt wird (wird von LINEDEVSTATE \_ RINGING-Nachrichten begleitet), und wenn eine Anwendung für die automatische Antwort eingerichtet ist, kann dies der Fall sein. Wenn der Anrufzustandsmodus "inaktiv" ist, wird der Anruf an mehreren Stationen angeboten, aber die aktuelle Station gibt keine Warnung aus (z. B. kann es sich um eine begleitende Station mit dem Angebotsstatus "Beratung" handelt, z. B. blinkendes Licht). Software an der Station, die für die automatische Antwort festgelegt ist, sollte den Anruf vorzugsweise nicht beantworten, da dies das Vorrecht an der primären (warnenden) Station sein sollte, aber [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) kann verwendet werden, um den Anruf zu verbinden. Wenn der Aufrufzustandsmodus NULL ist, sollte die Anwendung davon ausgehen, dass der Wert aktiv ist (dies wäre die Situation bei einer nicht überbrückten Adresse).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




