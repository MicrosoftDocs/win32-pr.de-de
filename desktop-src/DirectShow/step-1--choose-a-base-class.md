---
description: 'Schritt 1:'
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: 'Schritt 1: Basisklasse auswählen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4679873e78e75b350335b5294db63579fd41f36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866476"
---
# <a name="step-1-choose-a-base-class"></a>Schritt 1: Basisklasse auswählen

Dies ist Schritt 1 des Tutorials zum [Schreiben von Transformations Filtern](writing-transform-filters.md).

Angenommen, Sie entscheiden sich für das Schreiben eines Filters und nicht eines DMO. der erste Schritt besteht darin, die zu verwendende Basisklasse auszuwählen. Die folgenden Klassen sind für Transformations Filter geeignet:

-   [**Ctransformfilter**](ctransformfilter.md) wurde für Transformations Filter entwickelt, für die separate Eingabe-und Ausgabepuffer verwendet werden. Diese Art von Filter wird manchmal als "Copy-Transform"-Filter bezeichnet. Wenn ein "Copy-Transform"-Filter ein Eingabe Beispiel empfängt, werden neue Daten in ein Ausgabe Beispiel geschrieben und das Ausgabe Beispiel an den nächsten Filter übermittelt.
-   [**Ctransinplacefilter**](ctransinplacefilter.md) wurde für Filter entwickelt, die Daten im ursprünglichen Puffer ändern, auch als "Trans-in-Place"-Filter bezeichnet. Wenn ein transdirektionale Filter eine Stichprobe empfängt, werden die Daten innerhalb dieses Beispiels geändert, und es wird das gleiche Beispiel für einen downstreamvorgang durchgeführt. Die Eingabe-PIN und die Ausgabe-PIN des Filters stellen immer eine Verbindung mit den entsprechenden Medientypen her.
-   [**Cvideotransformfilter**](cvideotransformfilter.md) ist hauptsächlich für Video Decoder konzipiert. Sie wird von **ctransformfilter** abgeleitet, bietet jedoch Funktionen zum Löschen von Frames, wenn der downstreamrenderer dahinter liegt.
-   [**Cbasefilter**](cbasefilter.md) ist eine generische Filterklasse. Die anderen Klassen in dieser Liste werden alle von **cbasefilter** abgeleitet. Wenn keines dieser Elemente geeignet ist, können Sie auf diese Klasse zurückgreifen. Diese Klasse erfordert jedoch auch die meiste Arbeit an Ihrem Teil.
-   \[! Wichtig\]  
    > Direkte Video Transformationen können schwerwiegende Auswirkungen auf die Renderingleistung haben. Direkte Transformationen erfordern Lese-und Schreibvorgänge für den Puffer. Wenn sich der Arbeitsspeicher auf einer Grafikkarte befindet, sind Lesevorgänge erheblich langsamer. Darüber hinaus kann auch eine Kopier Transformation unerwünschte Lesevorgänge verursachen, wenn Sie Sie nicht sorgfältig implementieren. Daher sollten Sie bei der Erstellung einer Video Transformation immer Leistungstests durchführen.

     

Für den RLE-Beispiel Encoder ist entweder **ctransformfilter** oder **cvideotransformfilter** die beste Wahl. Tatsächlich sind die Unterschiede zwischen Ihnen größtenteils intern, sodass es einfach ist, von einem in das andere zu konvertieren. Da sich die Medientypen auf den beiden Pins unterscheiden müssen, ist die **ctransinplacefilter** -Klasse für diesen Filter nicht geeignet. In diesem Beispiel wird **ctransformfilter** verwendet.

Weiter: [Schritt 2. Deklarieren Sie die Filter-Klasse](step-2--declare-the-filter-class.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



