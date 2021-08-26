---
description: Einführung in die DirectShow-Filterentwicklung
ms.assetid: d5162ea4-ef37-4993-a82c-782f03b08c64
title: Einführung in die DirectShow-Filterentwicklung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2769cfe3bd4f046c117c0567104094bcad0eed730c388b551593dde6b41df25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083690"
---
# <a name="introduction-to-directshow-filter-development"></a>Einführung in die DirectShow-Filterentwicklung

Dieser Abschnitt enthält eine kurze Übersicht über die Aufgaben bei der Entwicklung eines benutzerdefinierten DirectShow-Filters. Sie enthält auch Links zu Themen, in denen diese Aufgaben ausführlicher erläutert werden. Lesen Sie vor dem Lesen dieses Abschnitts die Themen unter [About DirectShow (Informationen zu DirectShow),](about-directshow.md)in denen die gesamte DirectShow-Architektur beschrieben wird.

**DirectShow-Basisklassenbibliothek**

Das DirectShow SDK enthält eine Reihe von C++-Klassen zum Schreiben von Filtern. Obwohl sie nicht erforderlich sind, sind diese Klassen die empfohlene Methode zum Schreiben eines neuen Filters. Um die Basisklassen zu verwenden, kompilieren Sie sie in eine statische Bibliothek, und verknüpfen Sie die LIB-Datei mit Ihrem Projekt, wie unter [Erstellen von DirectShow-Filtern beschrieben.](building-directshow-filters.md)

Die Basisklassenbibliothek definiert eine Stammklasse für Filter, die [**CBaseFilter-Klasse.**](cbasefilter.md) Mehrere andere Klassen leiten sich von **CBaseFilter ab** und sind auf bestimmte Arten von Filtern spezialisiert. Die [**CTransformFilter-Klasse**](ctransformfilter.md) ist beispielsweise für Transformationsfilter konzipiert. Um einen neuen Filter zu erstellen, implementieren Sie eine Klasse, die von einer der Filterklassen erbt. Ihre Klassendeklaration kann z. B. wie folgt lauten:


```C++
class CMyFilter : public CTransformFilter
{
private:
    /* Declare variables and methods that are specific to your filter.
public:
    /* Override various methods in CTransformFilter */
};
```



Weitere Informationen zu den DirectShow-Basisklassen finden Sie in den folgenden Themen:

-   [DirectShow-Basisklassen](directshow-base-classes.md)
-   [Erstellen von DirectShow-Filtern](building-directshow-filters.md)

**Erstellen von Stecknadeln**

Ein Filter muss einen oder mehrere Stecknadeln erstellen. Die Anzahl der Stecknadeln kann zur Entwurfszeit festgelegt werden, oder der Filter kann bei Bedarf neue Stecknadeln erstellen. Pins werden im Allgemeinen von der [**CBasePin-Klasse**](cbasepin.md) oder von einer Klasse, die **CBasePin** erbt, wie [**z. B. CBaseInputPin, ableiten.**](cbaseinputpin.md) Die Pins des Filters sollten als Membervariablen in der Filterklasse deklariert werden. Einige filter-Klassen definieren die Pins bereits. Wenn Ihr Filter jedoch direkt von **CBaseFilter** erbt, müssen Sie die Pins in Ihrer abgeleiteten Klasse deklarieren.

**Aushandeln von Pinverbindungen**

Wenn der Filter Graph-Manager versucht, zwei Filter zu verbinden, müssen sich die Pins auf verschiedene Punkte einigen. Wenn dies nicht möglich ist, schlägt der Verbindungsversuch fehl. Im Allgemeinen handelt Pins Folgendes aus:

-   Transport: Der Transport ist der Mechanismus, den die Filter verwenden, um Medienbeispiele vom Ausgabepin in den Eingabepin zu verschieben. Beispielsweise können sie die [**IMemInputPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ("Pushmodell") oder die [**IAsyncReader-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ("Pullmodell") verwenden.
-   Medientyp. Fast alle Pins verwenden Medientypen, um das Format der Daten zu beschreiben, die sie liefern.
-   Zuweisung. Die Zuweisung ist das Objekt, das die Puffer erstellt, die die Daten aufnehmen. Die Stecknadeln müssen sich darauf einigen, welche Stecknadel die Zuweisung bereitstellen wird. Sie müssen sich auch über die Größe der Puffer, die Anzahl der zu erstellenden Puffer und andere Puffereigenschaften einigen.

Die Basisklassen implementieren ein Framework für diese Beides. Sie müssen die Details vervollständigen, indem Sie verschiedene Methoden in der Basisklasse überschreiben. Die Gruppe von Methoden, die Sie überschreiben müssen, hängt von der -Klasse und der Funktionalität des Filters ab. Weitere Informationen finden Sie unter [How Filters Verbinden](how-filters-connect.md).

**Verarbeiten und Bereitstellen von Daten**

Die Hauptfunktion der meisten Filter besteht in der Verarbeitung und Bereitstellung von Mediendaten. Wie dies geschieht, hängt vom Typ des Filters ab:

-   Eine Pushquelle verfügt über einen Arbeitsthread, der kontinuierlich Stichproben mit Daten auffüllt und diese nachgeschaltet übergibt.
-   Eine Pullquelle wartet darauf, dass ihr nachgeschalteter Nachbar eine Stichprobe an fordert. Er antwortet, indem daten in ein Beispiel geschrieben und das Beispiel an den Downstreamfilter zu liefern ist. Der Downstreamfilter erstellt den Thread, der den Datenfluss steuert.
-   Ein Transformationsfilter verfügt über Stichproben, die von seinem Upstreamnachbarn übermittelt werden. Wenn ein Beispiel empfangen wird, werden die Daten verarbeitet und nachgeschaltet.
-   Ein Rendererfilter empfängt Beispiele von Upstream und geplant sie für das Rendering basierend auf den Zeitstempeln.

Weitere Aufgaben im Zusammenhang mit dem Streaming sind das Leeren von Daten aus dem Diagramm, das Verarbeiten des Datenstromendes und das Reagieren auf Suchanforderungen. Weitere Informationen zu diesen Problemen finden Sie in den folgenden Themen:

-   [Data Flow für Filterentwickler](data-flow-for-filter-developers.md)
-   [Qualitätskontrollverwaltung](quality-control-management.md)
-   [Threads und kritische Abschnitte](threads-and-critical-sections.md)

**Unterstützen von COM**

DirectShow-Filter sind COM-Objekte, die in der Regel in DLLs gepackt sind. Die Basisklassenbibliothek implementiert ein Framework für die Unterstützung von COM. Dies wird im Abschnitt [DirectShow und COM beschrieben.](directshow-and-com.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



