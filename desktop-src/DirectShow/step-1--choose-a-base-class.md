---
description: Wählen Sie beim Schreiben eines Transformationsfilters eine Basisklasse aus. Erfahren Sie, welche Klassen für Transformationsfilter geeignet sind.
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: 'Schritt 1: Auswählen einer Basisklasse'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c140beba3df02ace21d99779c152a79632fe0b4a1a916c4412c467b0f4ac5627
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315880"
---
# <a name="step-1-choose-a-base-class"></a>Schritt 1: Auswählen einer Basisklasse

Dies ist Schritt 1 des Tutorials [Schreiben von Transformationsfiltern](writing-transform-filters.md).

Unter der Annahme, dass Sie sich entscheiden, einen Filter und keine DMO zu schreiben, besteht der erste Schritt in der Auswahl der zu verwendenden Basisklasse. Die folgenden Klassen sind für Transformationsfilter geeignet:

-   [**CTransformFilter**](ctransformfilter.md) ist für Transformationsfilter konzipiert, die separate Eingabe- und Ausgabepuffer verwenden. Diese Art von Filter wird manchmal als Kopiertransformationsfilter bezeichnet. Wenn ein Kopiertransformationsfilter ein Eingabebeispiel empfängt, schreibt er neue Daten in ein Ausgabebeispiel und übergibt das Ausgabebeispiel an den nächsten Filter.
-   [**CTransInPlaceFilter**](ctransinplacefilter.md) ist für Filter konzipiert, die Daten im ursprünglichen Puffer ändern, die auch als Trans-in-Place-Filter bezeichnet werden. Wenn ein trans-in-place-Filter eine Stichprobe empfängt, ändert er die Daten in dieser Stichprobe und liefert das gleiche Beispiel nachgeschaltet. Der Eingabepin und der Ausgabepin des Filters verbinden sich immer mit übereinstimmenden Medientypen.
-   [**CVideoTransformFilter**](cvideotransformfilter.md) ist in erster Linie für Videodecoder konzipiert. Sie wird von **CTransformFilter ableiten,** enthält jedoch Funktionen zum Löschen von Frames, wenn der Downstreamrenderer zurückfällt.
-   [**CBaseFilter**](cbasefilter.md) ist eine generische Filterklasse. Die anderen Klassen in dieser Liste werden alle von **CBaseFilter ableiten.** Wenn keines davon geeignet ist, können Sie auf diese Klasse zurückfallen. Diese Klasse erfordert jedoch auch die meisten Arbeit auf Ihrer Seite.
-   \[! Wichtig\]  
    > In-Place-Videotransformationen können schwerwiegende Auswirkungen auf die Renderingleistung haben. Für place-Transformationen sind Lese-/Änderungs-/Schreibvorgänge für den Puffer erforderlich. Wenn sich der Arbeitsspeicher auf einer Grafikkarte befindet, sind Lesevorgänge deutlich langsamer. Darüber hinaus kann selbst eine Kopiertransformation unbeabsichtigte Lesevorgänge verursachen, wenn Sie sie nicht sorgfältig implementieren. Daher sollten Sie immer Leistungstests durchführen, wenn Sie eine Videotransformation schreiben.

     

Für den RLE-Beispielencoder ist entweder **CTransformFilter** oder **CVideoTransformFilter die beste Wahl.** Tatsächlich sind die Unterschiede zwischen ihnen größtenteils intern, sodass es einfach ist, von einem in den anderen zu konvertieren. Da die Medientypen auf den beiden Stecknadeln unterschiedlich sein müssen, ist die **CTransInPlaceFilter-Klasse** für diesen Filter nicht geeignet. In diesem Beispiel wird **CTransformFilter verwendet.**

Weiter: [Schritt 2. Deklarieren Sie die Filterklasse](step-2--declare-the-filter-class.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



