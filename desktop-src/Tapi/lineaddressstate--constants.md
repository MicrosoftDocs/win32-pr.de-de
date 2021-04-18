---
description: Die lineaddressstate \_ -Bitflag-Konstanten beschreiben verschiedene Adress Status Elemente.
ms.assetid: f06140d0-f41a-4228-93c5-21d609af5473
title: LINEADDRESSSTATE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483ac665c41989c65b43419442601dfb70667dc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352131"
---
# <a name="lineaddressstate_-constants"></a>Lineaddressstate- \_ Konstanten

Die **lineaddressstate \_** -Bitflag-Konstanten beschreiben verschiedene Adress Status Elemente.

<dl> <dt>

<span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**lineaddressstate \_ capschange**
</dt> <dd> <dl> <dt>



Gibt an, dass ein oder mehrere der Elemente in der [**lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) -Struktur für die Adresse aufgrund von Konfigurationsänderungen, die vom Benutzer oder anderen Bedingungen vorgenommen wurden, geändert wurden. Die Anwendung sollte [**linegetaddresscaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) zum Lesen der aktualisierten Struktur verwenden. Wenn ein Dienstanbieter eine [**Zeile \_ addressstate**](line-addressstate.md) -Nachricht mit diesem Wert an TAPI sendet, übergibt TAPI ihn an Anwendungen, die die TAPI-Version 1,4 oder höher ausgehandelt haben. Anwendungen, die eine vorherige API-Version aushandeln, erhalten [**Zeilen- \_ linedevstate**](line-linedevstate.md) -Nachrichten, die linedevstate \_ REIT enthalten, sodass diese die aktualisierten Informationen Herunterfahren und erneut initialisieren müssen.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**lineaddressstate \_ DevSpecific**
</dt> <dd> <dl> <dt>



Das gerätespezifische Element des Adress Status hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**lineaddressstate \_ Vorwärts**
</dt> <dd> <dl> <dt>



Der Weiterleitungs Status der Adresse hat sich geändert, einschließlich der Anzahl der Ringe zum Ermitteln der Bedingung "keine Antwort". Die Anwendung sollte den Adress Status überprüfen, um Details zum aktuellen Weiterleitungs Status der Adresse zu ermitteln.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**lineaddressstate \_ inusemany**
</dt> <dd> <dl> <dt>



Die überwachte oder überbrückte Adresse wurde von einer Station in der Verwendung durch mehr als eine Station geändert.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**lineaddressstate \_ inuseone**
</dt> <dd> <dl> <dt>



Die Adresse hat sich im Leerlauf geändert oder von vielen überbrückten Stationen verwendet, um von nur einer Station verwendet zu werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**lineaddressstate \_ inusezero**
</dt> <dd> <dl> <dt>



Die Adresse wurde in den Leerlauf geändert (Sie wird von keiner Station verwendet).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**lineaddressstate- \_ numrufe**
</dt> <dd> <dl> <dt>



Die Anzahl der Aufrufe für die Adresse hat sich geändert. Dies ist das Ergebnis von Ereignissen, z. b. einem neuen eingehenden-Befehl, einem ausgehenden-Rückruf für die Adresse oder einem-Rückruf, der seinen Haltezeit ändert. Dieses Flag deckt die Änderungen in allen Membern **dwnumactivecalls**, **dwnumonholdcalls** und **dwnumonholdcudingcalls** in der [**lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) -Struktur ab. Die Anwendung sollte alle drei Member überprüfen, wenn Sie eine [**Zeile \_ addressstate**](line-addressstate.md) (numcalls) empfängt.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**lineaddressstate \_ other**
</dt> <dd> <dl> <dt>



Address-Status Elemente, die nicht den unten aufgeführten unterliegen, wurden geändert. Die Anwendung sollte den aktuellen Adress Status überprüfen, um zu bestimmen, welche Elemente geändert wurden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**lineaddressstate- \_ Terminals**
</dt> <dd> <dl> <dt>



Die Terminal Einstellungen für die Adresse wurden geändert.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Eine Anwendung wird über Änderungen an diesen Status Elementen in der [**Zeile \_ addressstate**](line-addressstate.md) -Nachricht benachrichtigt. Die Gerätefunktionen der Adresse geben an, welche Adressen Zustandsänderungen für diese Adresse möglicherweise gemeldet werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zeile \_ addressstate**](line-addressstate.md)
</dt> <dt>

[**\_linienlinedevstate**](line-linedevstate.md)
</dt> <dt>

[**Lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**Lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**linegetaddresscaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> </dl>

 

 




