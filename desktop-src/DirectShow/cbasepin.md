---
description: Die cbasepin-Klasse ist eine abstrakte Klasse, die eine generische Pin implementiert.
ms.assetid: 23b9a0e2-24fe-4ff9-b2bb-97630c237de9
title: Cbasepin-Klasse (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ba7b3a85b512b2ad8d6e85aa38627a2abc68c21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369700"
---
# <a name="cbasepin-class"></a>Cbasepin-Klasse

![cbasepin-Klassenhierarchie](images/filter02.png)

Die- `CBasePin` Klasse ist eine abstrakte Klasse, die eine generische Pin implementiert.

In den folgenden Themen wird beschrieben, wie diese Klasse verwendet wird:

-   [Cbasepin-Verbindungsprozess](cbasepin-connection-process.md)
-   [Benachrichtigen von cbasepin mit Filter Zustandsänderungen](notifying-cbasepin-of-filter-state-changes.md)
-   [Ableiten von cbasepin](deriving-from-cbasepin.md)



| Geschützte Member-Variablen                                               | BESCHREIBUNG                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**m \_ PName**](cbasepin-m-pname.md)                                     | Der Name der PIN.                                                                                                  |
| [**m \_ verbunden**](cbasepin-m-connected.md)                             | Zeiger auf die PIN, die mit dieser Pin verbunden ist.                                                          |
| [**m- \_ dir**](cbasepin-m-dir.md)                                         | Die Richtung der PIN.                                                                                      |
| [**m \_ Plock**](cbasepin-m-plock.md)                                     | Zeiger auf ein kritisches Abschnitts Objekt.                                                                      |
| [**m-" \_ bruntimeerror"**](cbasepin-m-bruntimeerror.md)                     | Flag, das angibt, ob ein Laufzeitfehler aufgetreten ist.                                                 |
| [**m \_ bcanreconnect. Active**](cbasepin-m-bcanreconnectwhenactive.md) | Flag, das angibt, ob die PIN dynamische erneute Verbindung unterstützt.                                         |
| [**m \_ btrymytypesfirst**](cbasepin-m-btrymytypesfirst.md)               | Flag, das angibt, ob die PIN vor denen der empfangenden Pin ihre eigenen bevorzugten Medientypen ausprobiert. |
| [**m \_ pFilter**](cbasepin-m-pfilter.md)                                 | Zeiger auf den Filter, der die PIN erstellt hat.                                                                |
| [**m- \_ pqsink**](cbasepin-m-pqsink.md)                                   | Zeiger auf das-Objekt, das Qualitäts Meldungen verarbeitet.                                                       |
| [**m \_ typeversion**](cbasepin-m-typeversion.md)                         | Aktuelle Version des Satzes bevorzugter Medientypen.                                                       |
| [**m \_ MT**](cbasepin-m-mt.md)                                           | Medientyp für die aktuelle PIN-Verbindung.                                                                 |
| [**m \_ tSTART**](cbasepin-m-tstart.md)                                   | Startzeit des Segments.                                                                                        |
| [**m \_ tpause**](cbasepin-m-tstop.md)                                     | Endzeit des Segments.                                                                                         |
| [**m \_ drate**](cbasepin-m-drate.md)                                     | Segment Rate.                                                                                              |
| Geschützte Methoden                                                        | BESCHREIBUNG                                                                                                |
| [**Displaypininfo**](cbasepin-displaypininfo.md)                        | Verfolgt eine PIN-Verbindung während des Debuggens.                                                                  |
| [**Displaytypeinfo**](cbasepin-displaytypeinfo.md)                      | Zeigt während des Debuggens Medientyp Informationen an.                                                          |
| [**Verbindung wird hergestellt**](cbasepin-attemptconnection.md)                  | Stellt mithilfe eines angegebenen Medientyps eine Verbindung mit einer anderen Pin her.                                                      |
| [**Trymediatypes**](cbasepin-trymediatypes.md)                          | Bei einer Liste von Medientypen wird von versucht, eine Verbindung mit einem dieser Typen abzuschließen.                      |
| [**Agreemediatype**](cbasepin-agreemediatype.md)                        | Sucht nach einem Medientyp, um eine PIN-Verbindung herzustellen.                                                        |
| [**Disconnectinternal**](cbasepin-disconnectinternal.md)                | Unterbricht die aktuelle PIN-Verbindung.                                                                         |
| Öffentliche Methoden                                                           | BESCHREIBUNG                                                                                                |
| [**Cbasepin**](cbasepin-cbasepin.md)                                    | Konstruktormethode.                                                                                        |
| [**~ Cbasepin**](cbasepin--cbasepin.md)                                 | Dekonstruktormethode. Virtu.                                                                                |
| [**IsConnected**](cbasepin-isconnected.md)                              | Bestimmt, ob die PIN mit einer anderen Pin verbunden ist.                                                    |
| [**Getconnected**](cbasepin-getconnected.md)                            | Ruft die PIN ab, die mit dieser Pin verbunden ist.                                                           |
| [**IsStopped**](cbasepin-isstopped.md)                                  | Bestimmt, ob der Filter, der diese PIN enthält, angehalten wird.                                              |
| [**Getmediatypeer Version**](cbasepin-getmediatypeversion.md)              | Ruft eine Versionsnummer für die Gruppe der bevorzugten Medientypen ab. Virtu.                                  |
| [**Incrementtypeversion**](cbasepin-incrementtypeversion.md)            | Inkremente der Versionsnummer für den Satz bevorzugter Medientypen.                                         |
| [**Aktiv**](cbasepin-active.md)                                        | Benachrichtigt die PIN, dass der Filter jetzt aktiv ist. Virtu.                                                   |
| [**Inaktiv**](cbasepin-inactive.md)                                    | Benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist. Virtu.                                             |
| [**Ausführen**](cbasepin-run.md)                                              | Benachrichtigt die PIN, dass der Filter jetzt ausgeführt wird. Virtu.                                                  |
| [**Setmediatype**](cbasepin-setmediatype.md)                            | Legt den Medientyp für die Verbindung fest. Virtu.                                                           |
| [**Check Connect**](cbasepin-checkconnect.md)                            | Bestimmt, ob eine PIN-Verbindung geeignet ist. Virtu.                                                  |
| [**Breakconnect**](cbasepin-breakconnect.md)                            | Gibt die PIN von einer Verbindung frei. Virtu.                                                               |
| [**Completeconnect**](cbasepin-completeconnect.md)                      | Schließt eine Verbindung mit einer anderen Pin ab. Virtu.                                                            |
| [**Getmediatype**](cbasepin-getmediatype.md)                            | Ruft einen bevorzugten Medientyp nach Indexwert ab. Virtu.                                                 |
| [**Currentstoptime**](cbasepin-currentstoptime.md)                      | Ruft die Endzeit des Segments ab.                                                                           |
| [**Currentstarttime**](cbasepin-currentstarttime.md)                    | Ruft die Startzeit des Segments ab.                                                                          |
| [**Currentrate**](cbasepin-currentrate.md)                              | Ruft die Segment Rate ab.                                                                                |
| [**Name**](cbasepin-name.md)                                            | Ruft den PIN-Bezeichner ab.                                                                              |
| [**"Ttreconnect-aktiv"**](cbasepin-setreconnectwhenactive.md)        | Gibt an, ob die PIN dynamische erneute Verbindungen unterstützt.                                                  |
| [**Canreconnect. Active**](cbasepin-canreconnectwhenactive.md)        | Fragt ab, ob die PIN dynamische erneute Verbindungen unterstützt.                                                    |
| Reine virtuelle Methoden                                                     | BESCHREIBUNG                                                                                                |
| [**Checkmediatype**](cbasepin-checkmediatype.md)                        | Bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.                                                       |
| IPin-Methoden                                                             | BESCHREIBUNG                                                                                                |
| [**Verbinden**](cbasepin-connect.md)                                      | Verbindet die PIN mit einer anderen Pin.                                                                           |
| [**Receiveconnection**](cbasepin-receiveconnection.md)                  | Akzeptiert eine Verbindung von einer anderen Pin.                                                                     |
| [**Trennen**](cbasepin-disconnect.md)                                | Unterbricht die aktuelle PIN-Verbindung.                                                                         |
| [**Connectedto**](cbasepin-connectedto.md)                              | Ruft die mit dieser Pin verbundene Pin ab.                                                                   |
| [**Connectionmediatype**](cbasepin-connectionmediatype.md)              | Ruft ggf. den Medientyp für die aktuelle PIN-Verbindung ab.                                           |
| [**Querypininfo**](cbasepin-querypininfo.md)                            | Ruft Informationen über die PIN ab.                                                                       |
| [**Querydirection**](cbasepin-querydirection.md)                        | Ruft die Richtung der PIN (Eingabe oder Ausgabe) ab.                                                      |
| [**QueryId**](cbasepin-queryid.md)                                      | Ruft den PIN-Bezeichner ab.                                                                              |
| [**Queryaccept**](cbasepin-queryaccept.md)                              | Bestimmt, ob die PIN einen angegebenen Medientyp akzeptiert.                                                 |
| [**Enummediatypes**](cbasepin-enummediatypes.md)                        | Listet die bevorzugten Medientypen der PIN auf.                                                                |
| [**QueryInternalConnections**](cbasepin-queryinternalconnections.md)    | Ruft die Pins ab, die intern mit dieser Pin (innerhalb des Filters) verbunden sind.                          |
| [**EndOfStream**](cbasepin-endofstream.md)                              | Benachrichtigt die PIN, dass keine weiteren Daten erwartet werden.                                                      |
| [**Newsegment**](cbasepin-newsegment.md)                                | Benachrichtigt die PIN, dass nach diesem-Befehl empfangene Medien Beispiele als Segment gruppiert werden.                     |
| Iqualitycontrol-Methoden                                                  | BESCHREIBUNG                                                                                                |
| [**Benachrichtigen**](cbasepin-notify.md)                                        | Benachrichtigt die PIN, dass eine Qualitätsänderung angefordert wird.                                                       |
| [**Setsink**](cbasepin-setsink.md)                                      | Legt einen externen Quality Manager fest.                                                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




