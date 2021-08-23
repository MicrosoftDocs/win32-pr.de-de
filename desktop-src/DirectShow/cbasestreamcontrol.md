---
description: Diese Klasse implementiert die IAMStreamControl-Schnittstelle für Eingabe- und Ausgabepins.
ms.assetid: a0ddc2d5-8385-4209-b1c5-9822c30f8a02
title: CBaseStreamControl-Klasse (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eb1d8d747d88a416792d59af79af41c047cb51aa61688aef9d6b105790bbae8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157201"
---
# <a name="cbasestreamcontrol-class"></a>CBaseStreamControl-Klasse

![cbasestreamcontrol-Klassenhierarchie](images/strmctl1.png)

Diese Klasse implementiert die [**IAMStreamControl-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) für Eingabe- und Ausgabepins. Sie ermöglicht die Steuerung des Startens und Beendens eines einzelnen Pins im Filter. Ein Pin, der **IAMStreamControl unterstützt,** sollte von dieser Basisklasse erben. Im Folgenden finden Sie eine typische Deklaration für einen Eingabepin:

``` syntax
class CMyInputPin : public CBaseInputPin, public CBaseStreamControl
```

Stellen Sie sicher, dass **Sie NonDelegatingQueryInteface überschreiben,** um **IAMStreamControl verfügbar zu machen.** Weitere Informationen finden Sie unter [Implementieren von IUnknown](how-to-implement-iunknown.md).



| Öffentliche Methoden                                                        | Beschreibung                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**CBaseStreamControl**](cbasestreamcontrol-cbasestreamcontrol.md)   | Konstruktormethode.                                                                                  |
| [**~CBaseStreamControl**](cbasestreamcontrol--cbasestreamcontrol.md) | Destruktormethode.                                                                                   |
| [**CheckStreamState**](cbasestreamcontrol-checkstreamstate.md)       | Bestimmt, ob ein Medienbeispiel übermittelt oder verworfen werden soll.                                  |
| [**Spülung**](cbasestreamcontrol-flushing.md)                       | Benachrichtigt die Basisklasse, dass das Leeren des Pins gestartet oder beendet wurde.                                |
| [**NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md)     | Benachrichtigt den Pin, wenn sich der Zustand des Filters ändert.                                                    |
| [**SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md)           | Gibt die Ereignissenke für Streamsteuersteuerereignisse an.                                                  |
| [**SetSyncSource**](cbasestreamcontrol-setsyncsource.md)             | Benachrichtigt die Basisklasse der aktuellen Referenzuhr.                                              |
| IAMStreamControl-Methoden                                              | Beschreibung                                                                                          |
| [**GetInfo**](cbasestreamcontrol-getinfo.md)                         | Ruft Informationen zu den aktuellen Streamsteuerungseinstellungen ab, einschließlich der Start- und Stoppzeiten. |
| [**Startat**](cbasestreamcontrol-startat.md)                         | Informiert den Pin darüber, wann mit der Bereitstellung von Daten zu beginnen ist.                                                       |
| [**Stopat**](cbasestreamcontrol-stopat.md)                           | Informiert den Pin darüber, wann die Daten nicht mehr zu liefern sind.                                                        |



 

## <a name="remarks"></a>Hinweise

Diese Klasse erfordert die Stecknadel und den besitzenden Filter, um die Klasse zu benachrichtigen, wenn verschiedene Ereignisse auftreten, z. B. der Filter, der den Graphen beitritt oder eine neue Verweisuhr empfängt. Sie sollten die folgenden Klassenmethoden aufrufen:

-   Rufen Sie in der [**IMediaFilter::SetSyncSource-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) des Filters die [**CBaseStreamControl::SetSyncSource-Methode**](cbasestreamcontrol-setsyncsource.md) auf. Diese Methode benachrichtigt die Klasse der aktuellen Referenzuhr.
-   Rufen Sie in der [**CBaseFilter::JoinFilterGraph-Methode**](cbasefilter-joinfiltergraph.md) des Filters die [**CBaseStreamControl::SetFilterGraph-Methode**](cbasestreamcontrol-setfiltergraph.md) auf. Diese Methode gibt der Klasse einen Zeiger auf den Filter-Graph-Manager, damit die Klasse die richtigen Streamsteuerungsereignisse senden kann.
-   Wenn der Filter den Zustand ändert (in wird ausgeführt, angehalten oder beendet), rufen Sie die [**CBaseStreamControl::NotifyFilterState-Methode**](cbasestreamcontrol-notifyfilterstate.md) auf.
-   Rufen Sie in den [**Methoden IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) und [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) des Pins die [**CBaseStreamControl::Flushing-Methode**](cbasestreamcontrol-flushing.md) auf.

Die -Klasse verwendet die Referenzuhr des Filterdiagramms, um zu bestimmen, welche Stichproben der Filter liefern und `CBaseStreamControl` welche verworfen werden sollen. Rufen Sie in der [**IMemInputPin::Receive-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) Ihres Pins die [**CBaseStreamControl::CheckStreamState-Methode**](cbasestreamcontrol-checkstreamstate.md) mit einem Zeiger auf das Beispiel für eingehende Medien auf. Wenn die Methode den Wert STREAM \_ FLOWING zurückgibt, stellen Sie das Beispiel nachgeschaltet zur Verfügung. Andernfalls verwerfen Sie sie.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Strmctl.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




