---
description: Die WMContainer-Objekte bieten eine Steuerung auf niedriger Ebene über das Analysieren und Schreiben einer ASF-Datei (Advanced Systems Format).
ms.assetid: 258ea139-581f-4b94-9655-43ecf1e77f10
title: WMContainer ASF-Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c4d39edd9241a856d5ef854d91bc1198cb090ddf653960b19905407c28279a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736742"
---
# <a name="wmcontainer-asf-components"></a>WMContainer ASF-Komponenten

Die WMContainer-Objekte bieten eine Steuerung auf niedriger Ebene über das Analysieren und Schreiben einer ASF-Datei (Advanced Systems Format).

Die [ASF-Komponenten](pipeline-layer-asf-components.md) der Pipelineebene verwenden die WMContainer-Objekte intern. Die meisten Anwendungen sollten die Pipelinekomponenten anstelle von WMContainer-Objekten verwenden. Verwenden Sie WMContainer nur, wenn Sie die Kontrolle über das Analysieren und Schreiben einer ASF-Datei auf niedriger Ebene benötigen.

Die WMContainer-Ebene enthält die folgenden Objekte:

-   [ASF-Profil](asf-profile.md)
-   [ASF ContentInfo-Objekt](asf-contentinfo-object.md)
-   [ASF-Splitter](asf-splitter.md)
-   [ASF Multiplexer](asf-multiplexer.md)
-   [ASF Indexer](asf-index-object.md)

Die folgenden Themen enthalten schrittweise Anweisungen zur Verwendung von WMContainer zum Lesen oder Schreiben von ASF-Dateien.

-   [Tutorial: Lesen einer ASF-Datei mit WMContainer-Objekten](tutorial--reading-an-asf-file.md)
-   [Tutorial: Kopieren von ASF-Streams mit WMContainer-Objekten](tutorial--copying-asf-streams-from-one-file-to-another.md)
-   [Tutorial: Schreiben einer WMA-Datei mit WMContainer-Objekten](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)

## <a name="about-wm-container"></a>Informationen zu WM-Containern

Die WMContainer-Objekte interagieren direkt mit ASF-Dateiobjekten. Das folgende Diagramm zeigt die ASF-Dateistruktur und die entsprechenden WMContainer-Objekte.

![Diagramm der Asf-Dateistruktur und der entsprechenden Mediengrundobjekte](images/asf-components01.png)

Mit Ausnahme von Splitter und Multiplexer unterstützt jedes dieser Objekte das Analysieren (Lesen) und Schreiben von ASF-Dateien. Der Splitter wird nur zum Lesen von ASF-Dateien verwendet. Der Multiplexer wird nur zum Erstellen neuer ASF-Dateien verwendet.

Alle vorgänge, die von WMContainer-Objekten ausgeführt werden, sind synchron, d.h. sie blockieren den aufrufenden Thread.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Unterstützung in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



