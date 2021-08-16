---
description: Die KLASSE CABSchedule implementiert einen Scheduler für Verweisuhren.
ms.assetid: 67aacffb-b781-4323-8973-355a76821401
title: CABSchedule-Klasse (Dsschedule.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2236eb66086bb590892401cab052f39d81a41941db38d2a73dedd5edb4c53ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955409"
---
# <a name="camschedule-class"></a>WEBCAMSchedule-Klasse

Die `CAMSchedule` -Klasse implementiert einen Scheduler für Verweisuhren.



| Öffentliche Methoden                                             | Beschreibung                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**CAMSchedule**](camschedule-camschedule.md)             | Konstruktormethode.                                                                  |
| [**~WEBCAMSchedule**](camschedule--camschedule.md)           | Destruktormethode. Virtuellen.                                                          |
| [**GetAdviseCount**](camschedule-getadvisecount.md)       | Ruft die Anzahl ausstehender Beratungsanforderungen ab.                                     |
| [**GetNextAdviseTime**](camschedule-getnextadvisetime.md) | Ruft den Zeitpunkt der nächsten Empfehlungsanforderung ab.                                       |
| [**AddAdvisePacket**](camschedule-addadvisepacket.md)     | Fügt der Liste der ausstehenden Anforderungen eine Empfehlungsanforderung hinzu.                              |
| [**Unadvise**](camschedule-unadvise.md)                   | Entfernt eine Empfehlungsanforderung.                                                           |
| [**Beraten**](camschedule-advise.md)                       | Verteilt alle Anforderungen, die für einen bestimmten Zeitraum oder früher geplant sind.          |
| [**Getevent**](camschedule-getevent.md)                   | Ruft ein Ereignishandle ab, das verwendet wird, um eine Änderung im nächsten Empfehlungszeitpunkt zu signalisieren. |



 

## <a name="remarks"></a>Hinweise

Dieses Hilfsobjekt verwaltet eine Liste von Beratungsanforderungen für eine Referenzuhr. Die [**CBaseReferenceClock-Klasse**](cbasereferenceclock.md) verwendet sie, um Beratungsanforderungen zu planen. Uhren verwenden dieses Objekt wie folgt:

1.  Die Uhr erstellt einen Arbeitsthread für die Planung.
2.  Der Arbeitsthread ruft die [**METHODE CABSchedule::GetEvent**](camschedule-getevent.md) auf, um ein Ereignishandle vom Scheduler abzurufen. Es wartet auf dieses Ereignis, anfänglich mit einem unendlichen Time out.
3.  Um eine neue Empfehlungsanforderung zu planen, ruft die Uhr die [**METHODE CABSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) auf. Eine Empfehlungsanfrage kann einmalig oder regelmäßig erfolgen. Der Scheduler speichert die Liste der Anforderungen in der Zeitreihenfolge.
4.  Wenn am Ende der Liste eine Anforderung hinzugefügt wird, signalisiert der Scheduler das Ereignis. (Die Liste ist zunächst leer, sodass die erste Anforderung garantiert das Ereignis signalisiert.)
5.  Wenn das Ereignis signalisiert wird, ruft der Arbeitsthread die [**METHODE CABSchedule::Advise**](camschedule-advise.md) auf und gibt die aktuelle Referenzzeit an. Wenn ausstehende Anforderungen abgelaufen sind, werden sie vom Planer gesendet.
6.  Die Advise-Methode gibt den Zeitpunkt der nächsten Anforderung zurück. Der Arbeitsthread verwendet diesen Wert, um einen neuen Time out-Wert zu berechnen.
7.  Die Schritte 2 6 werden unbegrenzt wiederholt.
8.  Um den Arbeitsthread zu beenden, legt die Uhr ein internes Flag fest und signalisiert das Ereignis.

In Schritt 2 wird entweder das Ereignis signalisiert, oder der Wartezeitsend tritt ein. Wenn das Ereignis signalisiert wird, bedeutet dies, dass am Ende der Liste eine neue Anforderung hinzugefügt wurde. Der Arbeitsthread muss einen neuen Time out-Wert berechnen. Andererseits bedeutet dies, dass eine Empfehlungsanforderung fällig ist und gesendet werden muss, wenn bei der Wartezeit ein Zeit überschritten wird. Der Aufruf von Advise in Schritt 5 behandelt beide Fälle.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dsschedule.h (include Streams.h)</dt> </dl>                                                                                |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




