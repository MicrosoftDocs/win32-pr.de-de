---
description: Einführung in die Filter Basisklassen
ms.assetid: db6324d7-1914-44a8-a202-dff752b61c1a
title: Einführung in die Filter Basisklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44c104d8fe155a7c9f0edba72770a508c8ec43d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392337"
---
# <a name="introduction-to-the-filter-base-classes"></a>Einführung in die Filter Basisklassen

In diesem Artikel wird die Basisklassen Bibliothek von Microsoft DirectShow beschrieben. Diese Bibliothek ist für Filter Entwickler gedacht, aber Anwendungs Schreiber finden möglicherweise einige Hilfsklassen und debughilfsprogramme nützlich. Die Basisklassen Bibliothek ist jedoch für die DirectShow-Programmierung nicht erforderlich.

In den folgenden Abschnitten werden die wichtigsten Basisklassen in der-Bibliothek zusammengefasst.

**COM-Objektklassen**

Die folgenden Klassen unterstützen die Erstellung von COM-Objekten:



| Klasse                              | BESCHREIBUNG                            |
|------------------------------------|----------------------------------------|
| [**Cbaseobject**](cbaseobject.md) | Basisobjekt Klasse.                     |
| [**Cunknown**](cunknown.md)       | Implementiert die **IUnknown** -Schnittstelle. |



 

Die meisten DirectShow-Klassen werden von **cbaseobject** abgeleitet. Diese Klasse stellt Debuggingunterstützung bereit, indem die Anzahl aller aktiven Objekte in der dll zur Laufzeit beibehalten wird. In Debugbuilds wird die DLL bestätigt, wenn Sie entladen wird, während die Objekt Anzahl größer als 0 (null) ist. Dies erleichtert das Ermitteln von Verlusten aufgrund von Problemen bei der Verweis Zählung.

Alle Basisklassen, die COM-Schnittstellen unterstützen, werden von **cunknown** abgeleitet, das **cbaseobject** erbt. Die **cunknown** -Klasse unterstützt Verweis Zählung, **QueryInterface** und aggregration. Weitere Informationen finden Sie unter Gewusst [wie: Implementieren von IUnknown](how-to-implement-iunknown.md).

**Filter-und PIN-Klassen**

Die folgenden Klassen unterstützen die Erstellung von DirectShow Filter-und PIN-Objekten:



| Klasse                                    | BESCHREIBUNG                                                                                                                                                     |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cbasefilter**](cbasefilter.md)       | Basisklasse für Filter. Implementiert die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle.                                                                            |
| [**Cbasepin**](cbasepin.md)             | Basisklasse für Pins. Implementiert die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -und [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) -Schnittstellen.                                             |
| [**Cbaseingeputpin**](cbaseinputpin.md)   | Basisklasse für Eingabe Pins, die den lokalen Speicher Transport verwenden. Implementiert die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle. Diese Klasse wird von **cbasepin** abgeleitet. |
| [**Cbaseoutputpin**](cbaseoutputpin.md) | Basisklasse für Ausgabe Pins, die **IMemInputPin** -Verbindungen verwenden. Diese Klasse wird von **cbasepin** abgeleitet.                                                         |



 

Die folgenden Klassen sind hilfreich, um speziellere Filtertypen zu erstellen:



| Klasse                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CSource**](csource.md)                             | Basisklasse für Quell Filter. Diese Klasse ist für das Erstellen von pushquellen konzipiert. Sie eignet sich nicht für Pull-Quellen, z. b. Datei Leser. Um Ausgabe Pins für diese Klasse zu erstellen, verwenden Sie die [**csourcestream**](csourcestream.md) -Klasse.                                                                   |
| [**Ctransformfilter**](ctransformfilter.md)           | Basisklasse für Transformations Filter. Diese Klasse führt eine Kopie der Daten aus. Die Pins für diese Klasse sind [**ctransforminputpin**](ctransforminputpin.md) und [**ctransformoutputpin**](ctransformoutputpin.md).                                                                                            |
| [**Ctransinplacefilter**](ctransinplacefilter.md)     | Basisklasse für Transformations Filter, die keine Daten kopieren. Diese Klasse führt die Datenverarbeitung direkt in den Eingabedaten aus, bevor Sie Sie nach unten übergibt. Die Pins für diese Klasse sind [**ctransinplaceinputpin**](ctransinplaceinputpin.md) und [**ctransinplaceoutputpin**](ctransinplaceoutputpin.md). |
| [**Cvideotransformfilter**](cvideotransformfilter.md) | Basisklasse für Video Transformations Filter. Diese Klasse wird von **ctransformfilter** abgeleitet und bietet Unterstützung für die Qualitätskontrolle.                                                                                                                                                                                |
| [**Cbaserererderer**](cbaserenderer.md)                 | Basisklasse für rendererfilter. Die Eingabe-PIN für diese Klasse lautet [**crendererinputpin**](crendererinputpin.md).                                                                                                                                                                                          |
| [**Cbasevideorenderer**](cbasevideorenderer.md)       | Basisklasse für Videorenderer. Diese Klasse wird von **cbasererererererererer**                                                                                                                                                                                                                                |



 

Um diese Klassen verwenden zu können, müssen Sie eine eigene Klasse ableiten und Code schreiben, um die Funktionalität zu unterstützen, die für den Filter spezifisch ist. Umso spezieller ist die Basisklasse, der weniger Code, den Sie in der abgeleiteten Klasse schreiben müssen.

**Hilfsobjekte**

Die folgenden Klassen implementieren Hilfsobjekte, die von Filtern und Pins verwendet werden. Die meisten dieser Klassen können ohne ableiten von neuen Klassen verwendet werden:



| Klasse                                              | BESCHREIBUNG                                                                                                                                                        |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cpullpin**](cpullpin.md)                       | Hilfsobjekt für Eingabe Pins in Parserfiltern. Unterstützt [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Verbindungen mit pullquellen.                                       |
| [**Coutputqueue**](coutputqueue.md)               | Hilfsobjekt für Ausgabe Pins, die Beispiele zur Übermittlung in einem Arbeits Thread in die Warteschlange stellen.                                                                                  |
| [**Csourceseeking**](csourceseeking.md)           | Hilfe Objekt zum Implementieren der Suche in einem Quell Filter mit genau einer Ausgabe-PIN. (Diese Klasse ist nicht für Filter mit mehreren Pins (z. b. Parser) konzipiert. |
| [**Cenumpins**](cenumpins.md)                     | Enumeratorobjekt zum Aufzählen von Pins für einen Filter. Implementiert die [**iumumpins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) -Schnittstelle.                                                       |
| [**Cenum mediatypes**](cenummediatypes.md)         | Enumeratorobjekt zum Auflisten bevorzugter Medientypen in einer PIN. Implementiert die [**ienummediatypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) -Schnittstelle.                             |
| [**Cmemzuordcator**](cmemallocator.md)             | Arbeitsspeicherzuordnerobjekt. Implementiert die [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle.                                                                          |
| [**Cmediasample**](cmediasample.md)               | Medien Sample-Objekt. Implementiert die [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) -Schnittstelle.                                                                              |
| [**Cbasereferenceclock**](cbasereferenceclock.md) | Basisklasse für Referenzuhren. Implementiert die [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) -Schnittstelle.                                                              |
| [**Cmediatype**](cmediatype.md)                   | Hilfsobjekt zum Bearbeiten der [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Strukturen.                                                                                |



 

 

 



