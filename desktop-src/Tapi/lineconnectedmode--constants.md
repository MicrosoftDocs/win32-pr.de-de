---
description: Die \_ Bit-Flag-Konstanten von lineconnectedmode beschreiben verschiedene Unterzustände eines verbundenen Aufrufes.
ms.assetid: d75a5989-3f4e-4e5d-90b1-4e450def017e
title: LINECONNECTEDMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5191d3a575ef353c54c91c0e53b3228621b703cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359400"
---
# <a name="lineconnectedmode_-constants"></a>Lineconnectedmode- \_ Konstanten

Die Bit-Flag-Konstanten von **lineconnectedmode \_** beschreiben verschiedene Unterzustände eines verbundenen Aufrufes. Ein Modus ist als Anrufstatus für die Anwendung verfügbar, nachdem der Aufruf Status in verbunden übergegangen ist, und innerhalb der Zeile "CallState", die angibt, dass \_ der Aufruf von "linecallstate" \_ verbunden ist. Diese Werte werden verwendet, wenn der Aufruf einer freigegebenen Adresse (überbrückt) mit anderen Stationen erfolgt (Weitere Informationen finden Sie unter [**lineaddresssharing- \_ Konstanten**](lineaddresssharing--constants.md)), primär für elektronische Schlüsselsysteme. Die **lineconnectedmode- \_ Konstanten** haben die folgenden Werte:

<dl> <dt>

<span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**lineconnectedmode \_ aktiv**
</dt> <dd> <dl> <dt>



Gibt an, dass der-Befehl an der aktuellen Station verbunden ist (die aktuelle Station ist ein Teilnehmer des Aufrufes). Wenn der Zustands Modus des Aufrufes den Wert 0 (null) aufweist, sollte die Anwendung davon ausgehen, dass der Wert "aktiv" ist (Dies wäre die Situation bei einer nicht überbrückten Adresse). Der Modus kann während eines Aufrufes zwischen "aktiv" und "inaktiv" wechseln, wenn der Benutzer mit der manuellen Aktion verknüpft und den Vorgang verlässt. In solch einer überbrückten Situation kann es vorkommen, dass ein [**linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) -oder [**linehold**](/windows/desktop/api/Tapi/nf-tapi-linehold) -Vorgang den-Vorgang nicht tatsächlich löscht oder auf dem Stand hält, da der Status anderer Stationen des Aufrufes möglicherweise regelt (z. b. Wenn Sie versuchen, einen-Befehl anzuhalten, wenn andere Stationen teilnehmen); Stattdessen kann der-Befehl in den inaktiven Modus geändert werden, wenn er an anderen Stationen verbunden bleibt.


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**lineconnectedmode \_ activeheld**
</dt> <dd> <dl> <dt>



Gibt an, dass die Station ein aktiver Teilnehmer des Aufrufes ist, aber dass die Remote Partei den Anruf angehalten hat (die andere Partei hält den Anruf als "OnHold" an). Diese Informationen sind normalerweise nur verfügbar, wenn beide Endpunkte des Aufrufes innerhalb derselben Wechsel Domäne liegen. Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln. (TAPI-Versionen 2,0 und höher)


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**"lineconnectedmode" wurde \_ bestätigt.**
</dt> <dd> <dl> <dt>



Gibt an, dass der Dienstanbieter eine Benachrichtigung erhalten hat, dass der Anruf in den Status "verbunden" eingetreten ist (z. b. durch Antwort Aufsicht oder ähnliche Mechanismen). Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln. (TAPI-Versionen 2,0 und höher)


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**lineconnectedmode \_ inaktiv**
</dt> <dd> <dl> <dt>



Gibt an, dass der-Befehl an einer oder mehreren anderen Stationen aktiv ist, die aktuelle Station ist jedoch kein Teilnehmer des Aufrufes. Wenn der aufrufstatusmodus 0 (null) ist, sollte die Anwendung davon ausgehen, dass der Wert "aktiv" ist (Dies wäre die Situation bei einer nicht überbrücken Adresse). Ein Anruf im inaktiven Zustand kann mithilfe von [**lineanswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)verknüpft werden. Viele Vorgänge, die in Aufrufen im verbundenen Zustand gültig sind, können im inaktiven Modus nicht ausgeführt werden, wie z. b. die Überwachung von Tönen und Ziffern, da die Station nicht an dem Anruf teilnimmt. die Überwachung wird in der Regel angehalten (obwohl Sie nicht abgebrochen wird), während der-Befehl im inaktiven Modus


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**lineconnectedmode \_ inactiveheld**
</dt> <dd> <dl> <dt>



Gibt an, dass es sich bei der Station nicht um einen aktiven Teilnehmer des Aufrufes handelt und dass die Remote Partei den Anruf angehalten hat. Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln. (TAPI-Versionen 2,0 und höher)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Nicht erweiterbar. Alle 32 Bits sind reserviert.

Aus Gründen der Abwärtskompatibilität liegt es in der Verantwortung des Dienstanbieters, die ausgehandelte API-Version in der Zeile zu untersuchen und diese lineconnectedmode-Werte nicht zu verwenden, die \_ von der ausgehandelten Version nicht unterstützt werden. Anwendungen, die nicht von lineconnectedmode erkannt werden, \_ nehmen wahrscheinlich an, dass sich ein in linecallstate \_ verbundener Befehl in lineconnectedmode \_ aktiv befindet.

Die inaktiven Werte für "lineconnectedmode" \_ und "lineconnectedmode" \_ werden verwendet, wenn sich der Aufruf auf einer Adresse befindet, die für andere Stationen freigegeben ist (überbrückt, siehe [**lineaddresssharing- \_ Konstanten**](lineaddresssharing--constants.md)), primär in elektronischen Schlüssel Systemen. Wenn der verbundene CallState-Modus "aktiv" ist, bedeutet dies, dass der-Befehl an der aktuellen Station verbunden ist (die aktuelle Station ist ein Teilnehmer des Aufrufes). Wenn der aufrufsstatusmodus "inaktiv" ist, ist der-Befehl an einer oder mehreren anderen Stationen aktiv, aber die aktuelle Station ist kein Teilnehmer des Aufrufes. Wenn der aufrufstatusmodus 0 (null) ist, sollte die Anwendung davon ausgehen, dass der Wert "aktiv" ist (Dies wäre die Situation bei einer nicht überbrücken Adresse). Der Modus kann während eines Aufrufes zwischen "aktiv" und "inaktiv" wechseln, wenn der Benutzer mit der manuellen Aktion verknüpft und den Vorgang verlässt.

In solch einer überbrückten Situation kann es vorkommen, dass ein [**linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) -oder [**linehold**](/windows/desktop/api/Tapi/nf-tapi-linehold) -Vorgang den Rückruf nicht tatsächlich löscht oder auf dem Stand hält, da der Status anderer Stationen des Aufrufes möglicherweise regelt (z. b. Wenn Sie versuchen, einen Telefon anzuhalten, wenn andere Stationen teilnehmen); Stattdessen kann der-Befehl einfach in den inaktiven Modus geändert werden, wenn er an anderen Stationen verbunden bleibt. Ein-Anruf im inaktiven Zustand kann mithilfe von [**lineanswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)verknüpft werden.

Viele Vorgänge, die in Aufrufen im verbundenen Zustand gültig sind, können im inaktiven Modus nicht ausgeführt werden, wie z. b. die Überwachung von Tönen und Ziffern, da die Station nicht an dem Anruf teilnimmt. die Überwachung wird in der Regel angehalten (obwohl Sie nicht abgebrochen wird), während der-Befehl im inaktiven Modus

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**lineanswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)
</dt> <dt>

[**linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**linehold**](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> </dl>

 

 




