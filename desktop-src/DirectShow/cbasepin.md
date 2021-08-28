---
description: Die CBasePin-Klasse ist eine abstrakte Klasse, die einen generischen Pin implementiert.
ms.assetid: 23b9a0e2-24fe-4ff9-b2bb-97630c237de9
title: CBasePin-Klasse (Amfilter.h)
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
ms.openlocfilehash: 55f697d6ff1a2bd3ebac77a77d8ba98321f29d09a75181b52e8ef08b03eed682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056195"
---
# <a name="cbasepin-class"></a>CBasePin-Klasse

![cbasepin-Klassenhierarchie](images/filter02.png)

Die `CBasePin` -Klasse ist eine abstrakte Klasse, die einen generischen Pin implementiert.

In den folgenden Themen wird die Verwendung dieser Klasse beschrieben:

-   [CBasePin-Verbindungsprozess](cbasepin-connection-process.md)
-   [Benachrichtigen von CBasePin über Änderungen des Filterstatus](notifying-cbasepin-of-filter-state-changes.md)
-   [Ableiten von CBasePin](deriving-from-cbasepin.md)



| Geschützte Membervariablen                                               | BESCHREIBUNG                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**m \_ pName**](cbasepin-m-pname.md)                                     | Pinname.                                                                                                  |
| [**m \_ Verbunden**](cbasepin-m-connected.md)                             | Zeiger auf den Pin, der mit diesem Pin verbunden ist.                                                          |
| [**m \_ dir**](cbasepin-m-dir.md)                                         | Richtung des Pins.                                                                                      |
| [**m \_ pLock**](cbasepin-m-plock.md)                                     | Zeiger auf ein kritisches Abschnittsobjekt.                                                                      |
| [**m \_ bRunTimeError**](cbasepin-m-bruntimeerror.md)                     | Flag, das angibt, ob ein Laufzeitfehler aufgetreten ist.                                                 |
| [**m \_ bCanReconnectWhenActive**](cbasepin-m-bcanreconnectwhenactive.md) | Flag, das angibt, ob der Pin die dynamische wiederhergestellte Verbindung unterstützt.                                         |
| [**m \_ bTryMyTypesFirst**](cbasepin-m-btrymytypesfirst.md)               | Flag, das angibt, ob der Pin seine eigenen bevorzugten Medientypen vor denen des empfangenden Pins versucht. |
| [**m \_ pFilter**](cbasepin-m-pfilter.md)                                 | Zeiger auf den Filter, der die Stecknadel erstellt hat.                                                                |
| [**m \_ pQSink**](cbasepin-m-pqsink.md)                                   | Zeiger auf das Objekt, das Qualitätsnachrichten verarbeitet.                                                       |
| [**m \_ TypeVersion**](cbasepin-m-typeversion.md)                         | Aktuelle Version des Satz von bevorzugten Medientypen.                                                       |
| [**m \_ mt**](cbasepin-m-mt.md)                                           | Medientyp für die aktuelle Pinverbindung.                                                                 |
| [**m \_ tStart**](cbasepin-m-tstart.md)                                   | Segmentstartzeit.                                                                                        |
| [**m \_ tStop**](cbasepin-m-tstop.md)                                     | Segmentstoppzeit.                                                                                         |
| [**m \_ dRate**](cbasepin-m-drate.md)                                     | Segmentrate.                                                                                              |
| Geschützte Methoden                                                        | BESCHREIBUNG                                                                                                |
| [**DisplayPinInfo**](cbasepin-displaypininfo.md)                        | Verfolgt eine Pinverbindung während des Debuggens nach.                                                                  |
| [**DisplayTypeInfo**](cbasepin-displaytypeinfo.md)                      | Zeigt Während des Debuggens Medientypinformationen an.                                                          |
| [**AttemptConnection**](cbasepin-attemptconnection.md)                  | Stellt mithilfe eines angegebenen Medientyps eine Verbindung mit einem anderen Pin herstellt.                                                      |
| [**TryMediaTypes**](cbasepin-trymediatypes.md)                          | Bei einer Liste von Medientypen versucht, eine Verbindung mit einem dieser Typen herzustellen.                      |
| [**AgreeMediaType**](cbasepin-agreemediatype.md)                        | Sucht nach einem Medientyp, um eine Stecknadelverbindung herzustellen.                                                        |
| [**DisconnectInternal**](cbasepin-disconnectinternal.md)                | Unterbricht die aktuelle Pinverbindung.                                                                         |
| Öffentliche Methoden                                                           | BESCHREIBUNG                                                                                                |
| [**CBasePin**](cbasepin-cbasepin.md)                                    | Konstruktormethode.                                                                                        |
| [**~ CBasePin**](cbasepin--cbasepin.md)                                 | Destruktormethode. Virtuellen.                                                                                |
| [**Isconnected**](cbasepin-isconnected.md)                              | Bestimmt, ob die Stecknadel mit einem anderen Pin verbunden ist.                                                    |
| [**GetConnected**](cbasepin-getconnected.md)                            | Ruft den Pin ab, der mit diesem Pin verbunden ist.                                                           |
| [**IsStopped**](cbasepin-isstopped.md)                                  | Bestimmt, ob der Filter, der diesen Pin enthält, beendet wird.                                              |
| [**GetMediaTypeVersion**](cbasepin-getmediatypeversion.md)              | Ruft eine Versionsnummer für den Satz bevorzugter Medientypen ab. Virtuellen.                                  |
| [**IncrementTypeVersion**](cbasepin-incrementtypeversion.md)            | Erhöht die Versionsnummer für den Satz bevorzugter Medientypen.                                         |
| [**Aktiv**](cbasepin-active.md)                                        | Benachrichtigt den Pin, dass der Filter jetzt aktiv ist. Virtuellen.                                                   |
| [**Inaktiv**](cbasepin-inactive.md)                                    | Benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist. Virtuellen.                                             |
| [**Ausführung**](cbasepin-run.md)                                              | Benachrichtigt den Pin, dass der Filter jetzt ausgeführt wird. Virtuellen.                                                  |
| [**SetMediaType**](cbasepin-setmediatype.md)                            | Legt den Medientyp für die Verbindung fest. Virtuellen.                                                           |
| [**CheckConnect**](cbasepin-checkconnect.md)                            | Bestimmt, ob eine Stecknadelverbindung geeignet ist. Virtuellen.                                                  |
| [**BreakConnect**](cbasepin-breakconnect.md)                            | Gibt den Pin von einer Verbindung frei. Virtuellen.                                                               |
| [**CompleteConnect**](cbasepin-completeconnect.md)                      | Schließt eine Verbindung mit einem anderen Pin ab. Virtuellen.                                                            |
| [**GetMediaType**](cbasepin-getmediatype.md)                            | Ruft einen bevorzugten Medientyp nach Indexwert ab. Virtuellen.                                                 |
| [**CurrentStopTime**](cbasepin-currentstoptime.md)                      | Ruft die Segmentstoppzeit ab.                                                                           |
| [**CurrentStartTime**](cbasepin-currentstarttime.md)                    | Ruft die Startzeit des Segments ab.                                                                          |
| [**CurrentRate**](cbasepin-currentrate.md)                              | Ruft die Segmentrate ab.                                                                                |
| [**Name**](cbasepin-name.md)                                            | Ruft den Stecknadelbezeichner ab.                                                                              |
| [**SetReconnectWhenActive**](cbasepin-setreconnectwhenactive.md)        | Gibt an, ob der Pin dynamische Verbindungswiederherstellungen unterstützt.                                                  |
| [**CanReconnectWhenActive**](cbasepin-canreconnectwhenactive.md)        | Fragt ab, ob der Pin dynamische Verbindungswiederherstellungen unterstützt.                                                    |
| Reine virtuelle Methoden                                                     | BESCHREIBUNG                                                                                                |
| [**CheckMediaType**](cbasepin-checkmediatype.md)                        | Bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.                                                       |
| IPin-Methoden                                                             | BESCHREIBUNG                                                                                                |
| [**Verbinden**](cbasepin-connect.md)                                      | Verbindet die Stecknadel mit einer anderen Stecknadel.                                                                           |
| [**ReceiveConnection**](cbasepin-receiveconnection.md)                  | Akzeptiert eine Verbindung von einem anderen Pin.                                                                     |
| [**Trennen**](cbasepin-disconnect.md)                                | Unterbricht die aktuelle Stecknadelverbindung.                                                                         |
| [**ConnectedTo**](cbasepin-connectedto.md)                              | Ruft den Anheften ab, der mit diesem Pin verbunden ist.                                                                   |
| [**ConnectionMediaType**](cbasepin-connectionmediatype.md)              | Ruft ggf. den Medientyp für die aktuelle Pinverbindung ab.                                           |
| [**QueryPinInfo**](cbasepin-querypininfo.md)                            | Ruft Informationen über die Stecknadel ab.                                                                       |
| [**QueryDirection**](cbasepin-querydirection.md)                        | Ruft die Richtung des Pins ab (Eingabe oder Ausgabe).                                                      |
| [**QueryId**](cbasepin-queryid.md)                                      | Ruft den Stecknadelbezeichner ab.                                                                              |
| [**QueryAccept**](cbasepin-queryaccept.md)                              | Bestimmt, ob der Pin einen angegebenen Medientyp akzeptiert.                                                 |
| [**EnumMediaTypes**](cbasepin-enummediatypes.md)                        | Listet die bevorzugten Medientypen des Pins auf.                                                                |
| [**QueryInternalConnections**](cbasepin-queryinternalconnections.md)    | Ruft die Pins ab, die intern mit diesem Pin verbunden sind (innerhalb des Filters).                          |
| [**EndOfStream**](cbasepin-endofstream.md)                              | Benachrichtigt den Pin, dass keine zusätzlichen Daten erwartet werden.                                                      |
| [**NewSegment**](cbasepin-newsegment.md)                                | Benachrichtigt den Pin, dass medienbeispiele, die nach diesem Aufruf empfangen wurden, als Segment gruppiert werden.                     |
| IQualityControl-Methoden                                                  | BESCHREIBUNG                                                                                                |
| [**Benachrichtigen**](cbasepin-notify.md)                                        | Benachrichtigt den Pin, dass eine Qualitätsänderung angefordert wird.                                                       |
| [**SetSink**](cbasepin-setsink.md)                                      | Legt einen externen Qualitätsmanager fest.                                                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




