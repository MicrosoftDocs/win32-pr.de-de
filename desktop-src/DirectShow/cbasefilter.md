---
description: Die cbasefilter-Klasse ist eine abstrakte Klasse zum Implementieren von Filtern.
ms.assetid: 4610c8d6-9d7d-47ca-b1d5-0a867153a5f6
title: Cbasefilter-Klasse (amfilter. h)
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
ms.openlocfilehash: fe032d0614b1067c9351b643d457a718b4917a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368648"
---
# <a name="cbasefilter-class"></a>Cbasefilter-Klasse

![cbasefilter-Klassenhierarchie](images/filter01.png)

Die- `CBaseFilter` Klasse ist eine abstrakte Klasse zum Implementieren von Filtern. Wenn Sie einen Filter mit dieser Klasse implementieren möchten, müssen Sie mindestens die folgenden Schritte ausführen:

-   Leiten Sie eine neue Klasse von ab `CBaseFilter` .
-   Fügen Sie Element Variablen ein, die die Pins für den Filter definieren. Die Pins müssen von der [**cbasepin**](cbasepin.md) -Klasse erben.
-   Überschreiben Sie die reine virtuelle Methode [**cbasefilter:: getpin**](cbasefilter-getpin.md), die Pins für den Filter abruft.
-   Überschreiben Sie die reine virtuelle Methode [**cbasefilter:: getpincount**](cbasefilter-getpincount.md), die die Anzahl der Pins abruft.
-   Stellen Sie Methoden zum Erstellen, verarbeiten oder Rendern von Medien Beispielen bereit.

Mehrere Basisklassen werden von abgeleitet `CBaseFilter` , einschließlich [**CSource**](csource.md), [**cbaserenderer**](cbaserenderer.md)und [**ctransformfilter**](ctransformfilter.md). In der Regel ist es einfacher, einen Filter mit einer dieser spezialisierten Klassen zu implementieren, anstatt Sie direkt zu verwenden `CBaseFilter` .



| Geschützte Member-Variablen                                     | BESCHREIBUNG                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**m- \_ Status**](cbasefilter-m-state.md)                        | Aktueller Status des Filters.                                                                       |
| [**m \_ pclock**](cbasefilter-m-pclock.md)                      | Zeiger auf die verweisuhr des Filters.                                                           |
| [**m \_ tSTART**](cbasefilter-m-tstart.md)                      | Die Verweis Zeit, die der streamzeit 0 entspricht.                                                  |
| [**m \_ CLSID**](cbasefilter-m-clsid.md)                        | Klassen Bezeichner (CLSID) des Filters.                                                            |
| [**m \_ Plock**](cbasefilter-m-plock.md)                        | Zeiger auf einen kritischen Abschnitt, der zum Serialisieren von Zustandsänderungen verwendet wird.                             |
| [**m \_ PName**](cbasefilter-m-pname.md)                        | Filter Name.                                                                                       |
| [**m- \_ PGraph**](cbasefilter-m-pgraph.md)                      | Zeiger auf den Filter Diagramm-Manager.                                                               |
| [**m \_ psink**](cbasefilter-m-psink.md)                        | Zeiger auf die [**imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) -Schnittstelle im Filter Diagramm-Manager.   |
| [**m \_ pinversion**](cbasefilter-m-pinversion.md)              | Aktuelle Version des Satzes von Pins für diesen Filter.                                                 |
| Öffentliche Methoden                                                 | BESCHREIBUNG                                                                                        |
| [**Cbasefilter**](cbasefilter-cbasefilter.md)                 | Konstruktormethode.                                                                                |
| [**~ Cbasefilter**](cbasefilter--cbasefilter.md)              | Dekonstruktormethode.                                                                                 |
| [**Streamtime**](cbasefilter-streamtime.md)                   | Ruft die aktuelle streamzeit ab. Virtu.                                                        |
| [**IsActive**](cbasefilter-isactive.md)                       | Bestimmt, ob der Filter derzeit aktiv ist (wird ausgeführt oder angehalten).                             |
| [**IsStopped**](cbasefilter-isstopped.md)                     | Bestimmt, ob der Filter aktuell beendet ist.                                                |
| [**NotifyEvent**](cbasefilter-notifyevent.md)                 | Sendet eine Ereignis Benachrichtigung an den Filter Diagramm-Manager.                                           |
| [**Getfiltergraph**](cbasefilter-getfiltergraph.md)           | Ruft einen Zeiger auf den Filter Diagramm-Manager ab.                                                   |
| [**Reconnectpin**](cbasefilter-reconnectpin.md)               | Unterbricht eine vorhandene Pin-Verbindung und verbindet Sie mit dem gleichen PIN, wobei ein angegebener Medientyp verwendet wird. |
| [**Getpinversion**](cbasefilter-getpinversion.md)             | Ruft eine Versionsnummer für den Satz von Pins für diesen Filter ab. Virtu.                            |
| [**Incrementpinversion**](cbasefilter-incrementpinversion.md) | Inkremente der Versionsnummer für den PIN-Satz.                                                  |
| [**Getsetupdata**](cbasefilter-getsetupdata.md)               | Ruft die Registrierungsdaten für den Filter ab. Virtu.                                           |
| Reine virtuelle Methoden                                           | BESCHREIBUNG                                                                                        |
| [**Getpincount**](cbasefilter-getpincount.md)                 | Ruft die Anzahl der Pins ab.                                                                      |
| [**Getpin**](cbasefilter-getpin.md)                           | Ruft eine PIN ab.                                                                                   |
| Ipersistent-Methoden                                               | BESCHREIBUNG                                                                                        |
| [**GetClassID**](cbasefilter-getclassid.md)                   | Ruft den Klassen Bezeichner ab.                                                                    |
| Imediafilter-Methoden                                           | BESCHREIBUNG                                                                                        |
| [**GetState**](cbasefilter-getstate.md)                       | Ruft den Zustand des Filters ab (wird ausgeführt, beendet oder angehalten).                                        |
| [**Setsyncsource**](cbasefilter-setsyncsource.md)             | Legt eine Referenzuhr für den Filter fest.                                                             |
| [**Getsyncsource**](cbasefilter-getsyncsource.md)             | Ruft die vom Filter verwendete Referenzuhr ab.                                            |
| [**Stop**](cbasefilter-stop.md)                               | Beendet den Filter.                                                                                  |
| [**Anhalten**](cbasefilter-pause.md)                             | Hält den Filter an.                                                                                 |
| [**Ausführen**](cbasefilter-run.md)                                 | Führt den Filter aus.                                                                                   |
| Ibasefilter-Methoden                                            | BESCHREIBUNG                                                                                        |
| [**Umanmeldungen**](cbasefilter-enumpins.md)                       | Listet die Pins für diesen Filter auf.                                                                |
| [**Findpin**](cbasefilter-findpin.md)                         | Ruft die PIN mit dem angegebenen Bezeichner ab.                                                   |
| [**Queryfilterinfo**](cbasefilter-queryfilterinfo.md)         | Ruft Informationen über den Filter ab.                                                            |
| [**Joinfiltergraph**](cbasefilter-joinfiltergraph.md)         | Benachrichtigt den Filter, dass ein Filter Diagramm verknüpft oder Links ist.                                     |
| [**Queryvendorinfo**](cbasefilter-queryvendorinfo.md)         | Ruft eine Zeichenfolge ab, die Hersteller Informationen enthält.                                                  |
| Iamoviesetup-Methoden                                           | BESCHREIBUNG                                                                                        |
| [**Registrieren**](cbasefilter-register.md)                       | Fügt den Filter der Registrierung hinzu.                                                                   |
| [**Unregister**](cbasefilter-unregister.md)                   | Entfernt den Filter aus der Registrierung.                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




