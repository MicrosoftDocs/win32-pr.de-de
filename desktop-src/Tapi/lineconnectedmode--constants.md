---
description: Die \_ LINECONNECTEDMODE-Bitflagkonstanten beschreiben verschiedene Unterstate eines verbundenen Aufrufs.
ms.assetid: d75a5989-3f4e-4e5d-90b1-4e450def017e
title: LINECONNECTEDMODE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1b8038f7d67f5805f4e4ea6669b4a5cf0f2eb693503401cb7610f2faa56e698
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117944884"
---
# <a name="lineconnectedmode_-constants"></a>LINECONNECTEDMODE-Konstanten \_

Die **\_ LINECONNECTEDMODE-Bitflagkonstanten** beschreiben verschiedene Unterstate eines verbundenen Aufrufs. Ein Modus ist als Aufrufstatus für die Anwendung verfügbar, nachdem der Aufrufzustand in verbunden überging, und innerhalb der LINE \_ CALLSTATE-Nachricht, die angibt, dass sich der Aufruf in LINECALLSTATE \_ CONNECTED befindet. Diese Werte werden verwendet, wenn sich der Aufruf auf einer Adresse befindet, die für andere Stationen freigegeben (bridged) ist (weitere Informationen finden Sie unter [**LINEADDRESSSHARING-Konstanten \_**](lineaddresssharing--constants.md)), hauptsächlich elektronische Schlüsselsysteme. Die **LINECONNECTEDMODE-Konstanten \_** haben die folgenden Werte:

<dl> <dt>

<span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE \_ ACTIVE**
</dt> <dd> <dl> <dt>



Gibt an, dass der Anruf an der aktuellen Station verbunden ist (die aktuelle Station ist ein Teilnehmer am Anruf). Wenn der Aufrufzustandsmodus 0 (null) ist, sollte die Anwendung davon ausgehen, dass der Wert "aktiv" ist (dies wäre die Situation bei einer nicht überbrückten Adresse). Der Modus kann während eines Aufrufs zwischen ACTIVE und INACTIVE wechseln, wenn der Benutzer beitritt und den Aufruf über eine manuelle Aktion verlässt. In einer solchen Überbrückungssituation kann ein [**lineDrop-**](/windows/desktop/api/Tapi/nf-tapi-linedrop) oder [**lineHold-Vorgang**](/windows/desktop/api/Tapi/nf-tapi-linehold) den Anruf möglicherweise nicht löschen oder zurückstellen, da der Status anderer Stationen im Anruf gesteuert werden kann (z. B. der Versuch, einen Anruf zu "halten", wenn andere Stationen teilnehmen, nicht möglich ist). Stattdessen kann der Aufruf in den INACTIVE-Modus geändert werden, wenn er an anderen Stationen verbunden bleibt.


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**LINECONNECTEDMODE \_ ACTIVEHELD**
</dt> <dd> <dl> <dt>



Gibt an, dass die Station ein aktiver Teilnehmer am Anruf ist, die Remoteseite den Anruf jedoch zurückgehalten hat (die andere Seite betrachtet den Aufruf als onhold-Zustand). Normalerweise sind solche Informationen nur verfügbar, wenn beide Endpunkte des Aufrufs in derselben Wechseldomäne liegen. Dieses Flag wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 2.0 oder höher aushandeln. (TAPI-Versionen 2.0 und höher)


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE \_ BESTÄTIGT**
</dt> <dd> <dl> <dt>



Gibt an, dass der Dienstanbieter eine positive Benachrichtigung erhalten hat, dass der Aufruf in den verbundenen Zustand eingetreten ist (z. B. durch Antwortüberwachung oder ähnliche Mechanismen). Dieses Flag wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 2.0 oder höher aushandeln. (TAPI-Versionen 2.0 und höher)


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE \_ INACTIVE**
</dt> <dd> <dl> <dt>



Gibt an, dass der Anruf an einer oder mehreren anderen Stationen aktiv ist, die aktuelle Station jedoch kein Teilnehmer des Anrufs ist. Wenn der Aufrufzustandsmodus NULL ist, sollte die Anwendung davon ausgehen, dass der Wert "aktiv" ist (dies wäre die Situation bei einer nicht überbrückten Adresse). Ein Aufruf im INACTIVE-Zustand kann mithilfe von [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)verknüpft werden. Viele Vorgänge, die in Aufrufen im Connected-Zustand gültig sind, können im INACTIVE-Modus unmöglich sein, z. B. die Überwachung von Tönen und Ziffern, da die Station nicht tatsächlich am Aufruf teilnimmt. Die Überwachung wird in der Regel angehalten (jedoch nicht abgebrochen), während sich der Aufruf im INACTIVE-Modus befindet.


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**LINECONNECTEDMODE \_ INACTIVEHELD**
</dt> <dd> <dl> <dt>



Gibt an, dass die Station kein aktiver Teilnehmer am Anruf ist und dass die Remotepartei den Anruf zurückgehalten hat. Dieses Flag wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 2.0 oder höher aushandeln. (TAPI-Versionen 2.0 und höher)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Nicht erweiterbar. Alle 32 Bits sind reserviert.

Aus Gründen der Abwärtskompatibilität ist der Dienstanbieter dafür verantwortlich, die ausgehandelte API-Version in der Zeile zu überprüfen und nicht die LINECONNECTEDMODE-Werte zu \_ verwenden, die in der ausgehandelten Version nicht unterstützt werden. Anwendungen, die LINECONNECTEDMODE nicht kennen, \_ gehen höchstwahrscheinlich davon aus, dass sich ein Aufruf in LINECALLSTATE \_ CONNECTED in LINECONNECTEDMODE \_ ACTIVE befindet.

Die WERTE LINECONNECTEDMODE \_ ACTIVE und LINECONNECTEDMODE \_ INACTIVE werden verwendet, wenn sich der Aufruf auf einer Adresse befindet, die für andere Stationen freigegeben wird (bridged; siehe [**LINEADDRESSSHARING-Konstanten \_**](lineaddresssharing--constants.md)), hauptsächlich elektronische Schlüsselsysteme. Wenn der Zustandsmodus des verbundenen Anrufs "aktiv" ist, bedeutet dies, dass der Anruf an der aktuellen Station verbunden ist (die aktuelle Station ist ein Teilnehmer am Anruf). Wenn der Anrufzustandsmodus "inaktiv" ist, ist der Aufruf an einer oder mehreren anderen Stationen aktiv, aber die aktuelle Station ist kein Teilnehmer am Anruf. Wenn der Aufrufzustandsmodus NULL ist, sollte die Anwendung davon ausgehen, dass der Wert "aktiv" ist (dies wäre die Situation bei einer nicht überbrückten Adresse). Der Modus kann während eines Aufrufs zwischen ACTIVE und INACTIVE wechseln, wenn der Benutzer beitritt und den Aufruf über eine manuelle Aktion verlässt.

In einer solchen überbrückten Situation kann ein [**lineDrop-**](/windows/desktop/api/Tapi/nf-tapi-linedrop) oder [**lineHold-Vorgang**](/windows/desktop/api/Tapi/nf-tapi-linehold) den Anruf möglicherweise nicht löschen oder zurückstellen, da der Status anderer Stationen im Anruf gesteuert werden kann (z. B. der Versuch, einen Anruf zu "halten", wenn andere Stationen teilnehmen, nicht möglich ist). Stattdessen kann der Aufruf einfach in den INACTIVE-Modus geändert werden, wenn er an anderen Stationen verbunden bleibt. Ein Aufruf im Inactive-Zustand kann mithilfe von [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)verknüpft werden.

Viele Vorgänge, die in Aufrufen im verbundenen Zustand gültig sind, können im INACTIVE-Modus unmöglich sein, z. B. die Überwachung von Tönen und Ziffern, da die Station nicht tatsächlich am Aufruf teilnimmt. Die Überwachung wird in der Regel angehalten (jedoch nicht abgebrochen), während sich der Aufruf im INACTIVE-Modus befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)
</dt> <dt>

[**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> </dl>

 

 




