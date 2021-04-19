---
description: Diese Klasse implementiert die iamstreamcontrol-Schnittstelle für Eingabe-und Ausgabe Pins.
ms.assetid: a0ddc2d5-8385-4209-b1c5-9822c30f8a02
title: Cbasestreamcontrol-Klasse ("strinmctl. h")
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
ms.openlocfilehash: c20a4f08040bdb2c71bdd8f09aa657719228efa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370646"
---
# <a name="cbasestreamcontrol-class"></a>Cbasestreamcontrol-Klasse

![cbasestreamcontrol-Klassenhierarchie](images/strmctl1.png)

Diese Klasse implementiert die [**iamstreamcontrol**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) -Schnittstelle für Eingabe-und Ausgabe Pins. Er bietet Kontrolle über das Starten und Beenden einer einzelnen PIN für den Filter. Eine PIN, die **iamstreamcontrol** unterstützt, sollte von dieser Basisklasse erben. Im folgenden finden Sie eine typische Deklaration für eine Eingabe-PIN:

``` syntax
class CMyInputPin : public CBaseInputPin, public CBaseStreamControl
```

Stellen Sie sicher, dass **nondelegatingqueryinteface** überschrieben wird, um **iamstreamcontrol** verfügbar zu machen. Weitere Informationen finden Sie unter Gewusst [wie: Implementieren von IUnknown](how-to-implement-iunknown.md).



| Öffentliche Methoden                                                        | BESCHREIBUNG                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**Cbasestreamcontrol**](cbasestreamcontrol-cbasestreamcontrol.md)   | Konstruktormethode.                                                                                  |
| [**~ Cbasestreamcontrol**](cbasestreamcontrol--cbasestreamcontrol.md) | Dekonstruktormethode.                                                                                   |
| [**Checkstreamstate**](cbasestreamcontrol-checkstreamstate.md)       | Bestimmt, ob ein Medien Beispiel übermittelt oder verworfen werden soll.                                  |
| [**Lak**](cbasestreamcontrol-flushing.md)                       | Benachrichtigt die Basisklasse, dass die PIN gestartet oder beendet wurde.                                |
| [**Notifyfilterstate**](cbasestreamcontrol-notifyfilterstate.md)     | Benachrichtigt die PIN, wenn der Zustand des Filters geändert wird.                                                    |
| [**Setfiltergraph**](cbasestreamcontrol-setfiltergraph.md)           | Gibt die Ereignis Senke für streamsteuerungsereignisse an.                                                  |
| [**Setsyncsource**](cbasestreamcontrol-setsyncsource.md)             | Benachrichtigt die Basisklasse der aktuellen verweisuhr.                                              |
| Iamstreamcontrol-Methoden                                              | BESCHREIBUNG                                                                                          |
| [**GetInfo**](cbasestreamcontrol-getinfo.md)                         | Ruft Informationen zu den aktuellen streamsteuerungseinstellungen ab, einschließlich der Start-und Endzeit. |
| [**StartAt**](cbasestreamcontrol-startat.md)                         | Informiert die PIN, wann mit der Übermittlung von Daten begonnen werden soll.                                                       |
| [**StopAt**](cbasestreamcontrol-stopat.md)                           | Informiert den PIN, wann die Übermittlung von Daten beendet werden soll.                                                        |



 

## <a name="remarks"></a>Bemerkungen

Diese Klasse erfordert, dass die PIN und der besitzende Filter die Klasse Benachrichtigen, wenn verschiedene Ereignisse auftreten, z. b. der Filter, der dem Diagramm Beitritt oder eine neue verweisuhr empfängt. Sie sollten die folgenden Klassen Methoden aufzurufen:

-   In der [**imediafilter:: setsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) -Methode des Filters aufrufen Sie die [**cbasestreamcontrol:: setsyncsource**](cbasestreamcontrol-setsyncsource.md) -Methode. Diese Methode benachrichtigt die-Klasse über die aktuelle verweisuhr.
-   In der [**cbasefilter:: joinfiltergraph**](cbasefilter-joinfiltergraph.md) -Methode des Filters aufrufen Sie die [**cbasestreamcontrol:: setfiltergraph**](cbasestreamcontrol-setfiltergraph.md) -Methode. Diese Methode gibt der Klasse einen Zeiger auf den Filter Graph-Manager, sodass die Klasse die richtigen streamsteuerungsereignisse senden kann.
-   Wenn der Filter den Zustand ändert (in "wird ausgeführt", "angehalten" oder "beendet"), wird die Methode [**cbasestreamcontrol:: notifyfilterstate**](cbasestreamcontrol-notifyfilterstate.md) aufgerufen.
-   In den [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -und [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methoden der PIN wird die [**cbasestreamcontrol::**](cbasestreamcontrol-flushing.md) Flush-Methode aufgerufen.

Die `CBaseStreamControl` -Klasse verwendet die Referenzuhr des Filter Diagramms, um zu bestimmen, welche Beispiele der Filter liefern soll und welche verworfen werden sollen. Aufrufen Sie in der [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode der PIN die [**cbasestreamcontrol:: checkstreamstate**](cbasestreamcontrol-checkstreamstate.md) -Methode mit einem Zeiger auf das Beispiel für eingehende Medien. Wenn die Methode den Wert für den wertstream zurückgibt, übermitteln Sie \_ das Beispiel Downstream. Verwerfen Sie diese andernfalls.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Strauch. h" (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




