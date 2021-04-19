---
description: Einführung in die DirectShow-Filter Entwicklung
ms.assetid: d5162ea4-ef37-4993-a82c-782f03b08c64
title: Einführung in die DirectShow-Filter Entwicklung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a42c5d2437b32f521b0efc39775f186267d3c99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345396"
---
# <a name="introduction-to-directshow-filter-development"></a>Einführung in die DirectShow-Filter Entwicklung

Dieser Abschnitt enthält eine kurze Übersicht über die Aufgaben, die bei der Entwicklung eines benutzerdefinierten DirectShow-Filters beteiligt sind. Außerdem finden Sie hier Links zu Themen, in denen diese Aufgaben ausführlicher erörtert werden. Lesen Sie vor dem Lesen dieses Abschnitts die Themen in [Informationen zu DirectShow](about-directshow.md), die die allgemeine DirectShow-Architektur beschreiben.

**DirectShow-Basisklassen Bibliothek**

Das DirectShow SDK enthält eine Reihe von C++-Klassen zum Schreiben von Filtern. Obwohl Sie nicht erforderlich sind, sind diese Klassen die empfohlene Vorgehensweise zum Schreiben eines neuen Filters. Wenn Sie die Basisklassen verwenden möchten, kompilieren Sie Sie in eine statische Bibliothek, und verknüpfen Sie die LIB-Datei mit dem Projekt, wie unter [Erstellen von DirectShow-Filtern](building-directshow-filters.md)beschrieben.

Die Basisklassen Bibliothek definiert eine Stamm Klasse für Filter, die [**cbasefilter**](cbasefilter.md) -Klasse. Mehrere andere Klassen werden von **cbasefilter** abgeleitet und sind für bestimmte Arten von Filtern spezialisiert. Beispielsweise ist die [**ctransformfilter**](ctransformfilter.md) -Klasse für Transformations Filter konzipiert. Um einen neuen Filter zu erstellen, implementieren Sie eine Klasse, die von einer der Filterklassen erbt. Die Klassen Deklaration könnte z. b. wie folgt lauten:


```C++
class CMyFilter : public CTransformFilter
{
private:
    /* Declare variables and methods that are specific to your filter.
public:
    /* Override various methods in CTransformFilter */
};
```



Weitere Informationen zu den DirectShow-Basisklassen finden Sie unter den folgenden Themen:

-   [DirectShow-Basisklassen](directshow-base-classes.md)
-   [Aufbauen von DirectShow-Filtern](building-directshow-filters.md)

**Erstellen von Pins**

Ein Filter muss mindestens einen Pins erstellen. Die Anzahl der Pins kann zur Entwurfszeit korrigiert werden, oder der Filter kann nach Bedarf neue Pins erstellen. Pins werden im Allgemeinen von der [**cbasepin**](cbasepin.md) -Klasse oder von einer Klasse abgeleitet, die **cbasepin** erbt, z. b. [**cbasinputpin**](cbaseinputpin.md). Die Pins des Filters sollten als Element Variablen in der Filter-Klasse deklariert werden. Einige der Filterklassen definieren bereits die Pins, aber wenn der Filter direkt von **cbasefilter** erbt, müssen Sie die Pins in der abgeleiteten Klasse deklarieren.

**Aushandeln von PIN-Verbindungen**

Wenn der Filter Graph-Manager versucht, zwei Filter zu verbinden, müssen die Pins den verschiedenen Dingen zustimmen. Wenn dies nicht möglich ist, schlägt der Verbindungsversuch fehl. Im Allgemeinen werden bei Pins folgende Aushandlungen ausgehandelt:

-   Transport: Der Transport ist der Mechanismus, den die Filter zum Verschieben von Medien Beispielen aus der Ausgabe-PIN in die Eingabe-PIN verwenden. Sie können z. b. die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle ("Push Model") oder die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle ("Pull Model") verwenden.
-   Medientyp. Fast alle Pins verwenden Medientypen, um das Format der Daten zu beschreiben, die Sie bereitstellt.
-   Allocator. Die Zuweisung ist das Objekt, mit dem die Puffer erstellt werden, die die Daten enthalten. Die Pins müssen zustimmen, welche PIN die Zuweisung bereitstellt. Sie müssen außerdem die Größe der Puffer, die Anzahl der zu erstellenden Puffer und andere Puffer Eigenschaften akzeptieren.

Die Basisklassen implementieren ein Framework für diese Aushandlungen. Sie müssen die Details vervollständigen, indem Sie verschiedene Methoden in der Basisklasse überschreiben. Der Satz von Methoden, die Sie überschreiben müssen, hängt von der-Klasse und der Funktionalität des Filters ab. Weitere Informationen finden Sie unter Gewusst [wie: Verbinden von Filtern](how-filters-connect.md).

**Verarbeiten und Bereitstellung von Daten**

Die Hauptfunktion der meisten Filter ist die Verarbeitung und Bereitstellung von Mediendaten. Wie dies geschieht, hängt vom Filtertyp ab:

-   Eine Push-Quelle verfügt über einen Arbeits Thread, der kontinuierlich Stichproben mit Daten füllt und diese nach unten übermittelt.
-   Eine Pull-Quelle wartet darauf, dass der Downstream-Nachbar ein Beispiel anfordert. Er antwortet, indem er Daten in ein Beispiel schreibt und das Beispiel für den downstreamfilter bereitstellt. Der Downstream-Filter erstellt den Thread, der den Datenfluss steuert.
-   Ein Transformations Filter enthält Beispiele, die von seinem upstreamnachbar bereitgestellt werden. Wenn ein Beispiel empfangen wird, werden die Daten verarbeitet und nachgelagert.
-   Ein rendererfilter empfängt Beispiele von Upstream und plant das Rendering basierend auf den Zeitstempeln.

Andere Aufgaben im Zusammenhang mit dem Streaming umfassen das Leeren von Daten aus dem Diagramm, das Verarbeiten des Datenstroms und das reagieren auf Suchanforderungen. Weitere Informationen zu diesen Problemen finden Sie in den folgenden Themen:

-   [Datenfluss für Filter Entwickler](data-flow-for-filter-developers.md)
-   [Qualitäts Steuerungs Verwaltung](quality-control-management.md)
-   [Threads und kritische Abschnitte](threads-and-critical-sections.md)

**Unterstützendes com**

DirectShow-Filter sind COM-Objekte, die in der Regel in DLLs verpackt sind. Die Basisklassen Bibliothek implementiert ein Framework für die Unterstützung von com. Dies wird im Abschnitt [DirectShow und com](directshow-and-com.md)beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



