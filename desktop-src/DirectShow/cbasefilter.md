---
description: Die CBaseFilter-Klasse ist eine abstrakte Klasse zum Implementieren von Filtern.
ms.assetid: 4610c8d6-9d7d-47ca-b1d5-0a867153a5f6
title: CBaseFilter-Klasse (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fbffdf47e019494570506dac164735a2471d0617daa190ad74fb3c8910a7dede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659635"
---
# <a name="cbasefilter-class"></a>CBaseFilter-Klasse

![cbasefilter-Klassenhierarchie](images/filter01.png)

Die `CBaseFilter` -Klasse ist eine abstrakte Klasse zum Implementieren von Filtern. Um einen Filter mit dieser Klasse zu implementieren, müssen Sie mindestens die folgenden Schritte ausführen:

-   Leiten Sie eine neue Klasse von `CBaseFilter` ab.
-   Schließen Sie Membervariablen ein, die die Pins für den Filter definieren. Die Pins müssen von der [**CBasePin-Klasse**](cbasepin.md) erben.
-   Überschreiben Sie die reine virtuelle Methode [**CBaseFilter::GetPin,**](cbasefilter-getpin.md)die Pins für den Filter abruft.
-   Überschreiben Sie die reine virtuelle Methode [**CBaseFilter::GetPinCount,**](cbasefilter-getpincount.md)die die Anzahl der Pins abruft.
-   Stellen Sie Methoden zum Generieren, Verarbeiten oder Rendern von Medienbeispielen bereit.

Mehrere Basisklassen werden von `CBaseFilter` abgeleitet, einschließlich [**CSource,**](csource.md) [**CBaseRenderer**](cbaserenderer.md)und [**CTransformFilter.**](ctransformfilter.md) In der Regel ist es einfacher, einen Filter mit einer dieser spezialisierten Klassen zu implementieren, anstatt ihn direkt zu `CBaseFilter` verwenden.



| Geschützte Membervariablen                                     | BESCHREIBUNG                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**m \_ State**](cbasefilter-m-state.md)                        | Aktueller Status des Filters.                                                                       |
| [**m \_ pClock**](cbasefilter-m-pclock.md)                      | Zeiger auf die Verweisuhr des Filters.                                                           |
| [**m \_ tStart**](cbasefilter-m-tstart.md)                      | Die Referenzzeit, die der Streamzeit 0 entspricht.                                                  |
| [**m \_ clsid**](cbasefilter-m-clsid.md)                        | Klassenbezeichner (CLSID) des Filters.                                                            |
| [**m \_ pLock**](cbasefilter-m-plock.md)                        | Zeiger auf einen kritischen Abschnitt, der zum Serialisieren von Zustandsänderungen verwendet wird.                             |
| [**m \_ pName**](cbasefilter-m-pname.md)                        | Filtername.                                                                                       |
| [**m \_ pGraph**](cbasefilter-m-pgraph.md)                      | Zeiger auf den Filtergraph-Manager.                                                               |
| [**m \_ pSink**](cbasefilter-m-psink.md)                        | Zeiger auf die [**IMediaEventSink-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) im Filtergraph-Manager.   |
| [**m \_ PinVersion**](cbasefilter-m-pinversion.md)              | Aktuelle Version des Stecknadelsatzes für diesen Filter.                                                 |
| Öffentliche Methoden                                                 | BESCHREIBUNG                                                                                        |
| [**CBaseFilter**](cbasefilter-cbasefilter.md)                 | Konstruktormethode.                                                                                |
| [**~ CBaseFilter**](cbasefilter--cbasefilter.md)              | Destruktormethode.                                                                                 |
| [**StreamTime**](cbasefilter-streamtime.md)                   | Ruft die aktuelle Streamzeit ab. Virtuellen.                                                        |
| [**IsActive**](cbasefilter-isactive.md)                       | Bestimmt, ob der Filter derzeit aktiv ist (wird ausgeführt oder angehalten).                             |
| [**IsStopped**](cbasefilter-isstopped.md)                     | Bestimmt, ob der Filter derzeit beendet wird.                                                |
| [**NotifyEvent**](cbasefilter-notifyevent.md)                 | Sendet eine Ereignisbenachrichtigung an den Filtergraph-Manager.                                           |
| [**GetFilterGraph**](cbasefilter-getfiltergraph.md)           | Ruft einen Zeiger auf den Filtergraph-Manager ab.                                                   |
| [**ReconnectPin**](cbasefilter-reconnectpin.md)               | Unterbricht eine vorhandene Pinverbindung und verbindet sie unter Verwendung eines angegebenen Medientyps erneut mit demselben Pin. |
| [**GetPinVersion**](cbasefilter-getpinversion.md)             | Ruft eine Versionsnummer für den Satz von Pins für diesen Filter ab. Virtuellen.                            |
| [**IncrementPinVersion**](cbasefilter-incrementpinversion.md) | Erhöht die Versionsnummer für den Satz von Pins.                                                  |
| [**GetSetupData**](cbasefilter-getsetupdata.md)               | Ruft die Registrierungsdaten für den Filter ab. Virtuellen.                                           |
| Reine virtuelle Methoden                                           | BESCHREIBUNG                                                                                        |
| [**GetPinCount**](cbasefilter-getpincount.md)                 | Ruft die Anzahl der Pins ab.                                                                      |
| [**GetPin**](cbasefilter-getpin.md)                           | Ruft eine Stecknadel ab.                                                                                   |
| IPersist-Methoden                                               | BESCHREIBUNG                                                                                        |
| [**Getclassid**](cbasefilter-getclassid.md)                   | Ruft den Klassenbezeichner ab.                                                                    |
| IMediaFilter-Methoden                                           | BESCHREIBUNG                                                                                        |
| [**GetState**](cbasefilter-getstate.md)                       | Ruft den Status des Filters ab (wird ausgeführt, angehalten oder angehalten).                                        |
| [**SetSyncSource**](cbasefilter-setsyncsource.md)             | Legt eine Verweisuhr für den Filter fest.                                                             |
| [**GetSyncSource**](cbasefilter-getsyncsource.md)             | Ruft die Referenzuhr ab, die der Filter verwendet.                                            |
| [**Beenden**](cbasefilter-stop.md)                               | Beendet den Filter.                                                                                  |
| [**Anhalten**](cbasefilter-pause.md)                             | Hält den Filter an.                                                                                 |
| [**Ausführung**](cbasefilter-run.md)                                 | Führt den Filter aus.                                                                                   |
| IBaseFilter-Methoden                                            | BESCHREIBUNG                                                                                        |
| [**EnumPins**](cbasefilter-enumpins.md)                       | Listet die Pins für diesen Filter auf.                                                                |
| [**FindPin**](cbasefilter-findpin.md)                         | Ruft die Stecknadel mit dem angegebenen Bezeichner ab.                                                   |
| [**QueryFilterInfo**](cbasefilter-queryfilterinfo.md)         | Ruft Informationen zum Filter ab.                                                            |
| [**JoinFilterGraph**](cbasefilter-joinfiltergraph.md)         | Benachrichtigt den Filter, dass er einem Filterdiagramm beigetreten ist oder dieses verlassen hat.                                     |
| [**QueryVendorInfo**](cbasefilter-queryvendorinfo.md)         | Ruft eine Zeichenfolge ab, die Anbieterinformationen enthält.                                                  |
| IAMovieSetup-Methoden                                           | BESCHREIBUNG                                                                                        |
| [**Registrieren**](cbasefilter-register.md)                       | Fügt der Registrierung den Filter hinzu.                                                                   |
| [**Registrierung**](cbasefilter-unregister.md)                   | Entfernt den Filter aus der Registrierung.                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




