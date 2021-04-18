---
description: Die Klasse "camschedule" implementiert einen Planer für Referenzuhren.
ms.assetid: 67aacffb-b781-4323-8973-355a76821401
title: Camschedule-Klasse (dsschedule. h)
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
ms.openlocfilehash: 1bef8ad07347284c53a3490c21032070788fa3ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365693"
---
# <a name="camschedule-class"></a>Camschedule-Klasse

Die- `CAMSchedule` Klasse implementiert einen Planer für Referenzuhren.



| Öffentliche Methoden                                             | BESCHREIBUNG                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**"Camschedule"**](camschedule-camschedule.md)             | Konstruktormethode.                                                                  |
| [**~ Camschedule**](camschedule--camschedule.md)           | Dekonstruktormethode. Virtu.                                                          |
| [**Getadviercount**](camschedule-getadvisecount.md)       | Ruft die Anzahl der ausstehenden Anforderungs Anforderungen ab.                                     |
| [**Getnextadvictime**](camschedule-getnextadvisetime.md) | Ruft den Zeitpunkt der nächsten anforderungsanforderung ab.                                       |
| [**Addadvisepacket**](camschedule-addadvisepacket.md)     | Fügt der Liste der ausstehenden Anforderungen eine anforderungsanforderung hinzu.                              |
| [**Unadvise**](camschedule-unadvise.md)                   | Entfernt eine Benachrichtigungs Anforderung.                                                           |
| [**Advise**](camschedule-advise.md)                       | Sendet alle Anforderungen, die für eine angegebene Zeit oder eine frühere Zeit geplant sind.          |
| [**GetEvent**](camschedule-getevent.md)                   | Ruft ein Ereignis Handle ab, das verwendet wird, um eine Änderung in der nächsten Empfehlung zu signalisieren. |



 

## <a name="remarks"></a>Bemerkungen

Dieses Hilfsobjekt verwaltet eine Liste von Anforderungs Anforderungen für eine Referenzuhr. Die [**cbasereferenceclock**](cbasereferenceclock.md) -Klasse verwendet diese, um Anforderungs Anforderungen zu planen. Uhren verwenden dieses Objekt wie folgt:

1.  Die Uhr erstellt einen Arbeits Thread zur Handhabung der Planung.
2.  Der Arbeits Thread ruft die " [**camschedule:: GetEvent**](camschedule-getevent.md) "-Methode auf, um ein Ereignis Handle aus dem Scheduler abzurufen. Er wartet auf dieses Ereignis, anfänglich mit einem unendlichen Timeout.
3.  Zum Planen einer neuen Benachrichtigungs Anforderung Ruft die Uhr die " [**camschedule:: addadvisepacket**](camschedule-addadvisepacket.md) "-Methode auf. Eine Benachrichtigungs Anforderung kann ein-oder periodisch sein. Der Scheduler speichert die Liste der Anforderungen in der angegebenen Reihenfolge.
4.  Wenn eine Anforderung am Anfang der Liste hinzugefügt wird, signalisiert der Planer das Ereignis. (Die Liste ist zuerst leer, sodass die erste Anforderung das Ereignis garantiert signalisiert.)
5.  Wenn das Ereignis signalisiert wird, ruft der Arbeits Thread die Methode " [**camschedule:: Empfehlung**](camschedule-advise.md) " auf und gibt den aktuellen Verweis Zeitpunkt an. Wenn ausstehende Anforderungen abgelaufen sind, werden Sie vom Scheduler versendet.
6.  Die Methode "Empfehlung" gibt den Zeitpunkt der nächsten Anforderung zurück. Der Arbeits Thread verwendet diesen Wert, um einen neuen Timeout Wert zu berechnen.
7.  Die Schritte 2 6 werden unbegrenzt wiederholt.
8.  Um den Arbeits Thread zu beenden, legt die Uhr ein internes Flag fest und signalisiert das Ereignis.

In Schritt 2 wird entweder das Ereignis signalisiert, oder der Warte Vorgang ist abgelaufen. Wenn das Ereignis signalisiert wird, bedeutet dies, dass am Anfang der Liste eine neue Anforderung hinzugefügt wurde. Der Arbeits Thread muss einen neuen Timeout Wert berechnen. Andererseits bedeutet dies, dass bei einem Timeout eine anforderungsanforderung ausgegeben wurde und verteilt werden muss. Der in Schritt 5 genannte Anrufe behandelt beide Fälle.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dsschedule. h (Include Streams. h)</dt> </dl>                                                                                |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




