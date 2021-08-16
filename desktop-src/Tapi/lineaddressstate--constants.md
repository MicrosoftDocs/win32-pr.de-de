---
description: Die \_ LINEADDRESSSTATE-Bitflagkonstanten beschreiben verschiedene Adressstatuselemente.
ms.assetid: f06140d0-f41a-4228-93c5-21d609af5473
title: LINEADDRESSSTATE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddf746d98328df51497374b990eb23f3885516ee1374d9cfdafb8799d016fb74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761852"
---
# <a name="lineaddressstate_-constants"></a>LINEADDRESSSTATE-Konstanten \_

Die **\_ LINEADDRESSSTATE-Bitflagkonstanten** beschreiben verschiedene Adressstatuselemente.

<dl> <dt>

<span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Gibt an, dass sich aufgrund von Konfigurationsänderungen durch den Benutzer oder unter anderen Umständen mindestens ein Member in der [**LINEADDRESSCAPS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) für die Adresse geändert hat. Die Anwendung sollte [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) verwenden, um die aktualisierte Struktur zu lesen. Wenn ein Dienstanbieter eine [**LINE \_ ADDRESSSTATE-Nachricht**](line-addressstate.md) mit diesem Wert an TAPI sendet, übergibt TAPI sie an Anwendungen, die TAPI Version 1.4 oder höher ausgehandelt haben. Anwendungen, die eine frühere API-Version aushandeln, erhalten [**LINE \_ LINEDEVSTATE-Nachrichten,**](line-linedevstate.md) die LINEDEVSTATE \_ REINIT angeben, sodass sie ihre Verbindung mit TAPI herunterfahren und erneut initialisieren müssen, um die aktualisierten Informationen abzurufen.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



Das gerätespezifische Element des Adressstatus wurde geändert.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**LINEADDRESSSTATE \_ FORWARD**
</dt> <dd> <dl> <dt>



Der Weiterleitungsstatus der Adresse wurde geändert, einschließlich möglicherweise der Anzahl von Ringen zum Bestimmen einer Bedingung ohne Antwort. Die Anwendung sollte den Adressstatus überprüfen, um Details zum aktuellen Weiterleitungsstatus der Adresse zu ermitteln.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE \_ INUSEMANY**
</dt> <dd> <dl> <dt>



Die überwachte oder überbrückte Adresse wurde von der Nutzung durch eine Station in die Nutzung durch mehrere Stationen geändert.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE \_ INUSEONE**
</dt> <dd> <dl> <dt>



Die Adresse hat sich von im Leerlauf oder in der Verwendung durch viele Brückenstationen in die Verwendung durch nur eine Station geändert.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE \_ INUSEZERO**
</dt> <dd> <dl> <dt>



Die Adresse wurde in den Leerlauf geändert (sie wird von keiner Station verwendet).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE \_ NUMCALLS**
</dt> <dd> <dl> <dt>



Die Anzahl der Aufrufe für die Adresse hat sich geändert. Dies ist das Ergebnis von Ereignissen wie einem neuen eingehenden Anruf, einem ausgehenden Anruf für die Adresse oder einem Anruf, der seinen Aufbewahrungsstatus ändert. Dieses Flag deckt Änderungen in den **Membern dwNumActiveCalls**, **dwNumOnHoldCalls** und **dwNumOnHoldPendingCalls** in der [**LINEADDRESSSTATUS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) ab. Die Anwendung sollte alle drei Member überprüfen, wenn sie eine [**LINE \_ ADDRESSSTATE-Nachricht**](line-addressstate.md) (numCalls) empfängt.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE \_ OTHER**
</dt> <dd> <dl> <dt>



Andere Als die unten aufgeführten Adressstatuselemente wurden geändert. Die Anwendung sollte den aktuellen Adressstatus überprüfen, um zu ermitteln, welche Elemente geändert wurden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**LINEADDRESSSTATE-TERMINALS \_**
</dt> <dd> <dl> <dt>



Die Terminaleinstellungen für die Adresse wurden geändert.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Eine Anwendung wird über Änderungen an diesen Statuselementen in der [**LINE \_ ADDRESSSTATE-Nachricht**](line-addressstate.md) benachrichtigt. Die Gerätefunktionen der Adresse geben an, welche Adressstatusänderungen möglicherweise für diese Adresse gemeldet werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LINE \_ ADDRESSSTATE**](line-addressstate.md)
</dt> <dt>

[**LINE \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> </dl>

 

 




