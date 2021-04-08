---
description: Die wmcontainer-Objekte bieten eine Low-Level-Kontrolle über das Auswerten und Schreiben einer ASF-Datei (Advanced Systems Format).
ms.assetid: 258ea139-581f-4b94-9655-43ecf1e77f10
title: Wmcontainer-ASF-Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d7d1c1b76683cfe01dc0970ab1c077580215d2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959885"
---
# <a name="wmcontainer-asf-components"></a>Wmcontainer-ASF-Komponenten

Die wmcontainer-Objekte bieten eine Low-Level-Kontrolle über das Auswerten und Schreiben einer ASF-Datei (Advanced Systems Format).

In den [ASF-Komponenten der Pipeline Schicht](pipeline-layer-asf-components.md) werden intern die wmcontainer-Objekte verwendet. Die meisten Anwendungen sollten die Pipeline Komponenten anstelle von wmcontainer-Objekten verwenden. Verwenden Sie wmcontainer nur dann, wenn Sie eine niedrige Kontrolle über das Auswerten und Schreiben einer ASF-Datei benötigen.

Die wmcontainer-Ebene enthält die folgenden Objekte:

-   [ASF-Profil](asf-profile.md)
-   [ASF-ContentInfo-Objekt](asf-contentinfo-object.md)
-   [ASF-Splitter](asf-splitter.md)
-   [ASF Multiplexer](asf-multiplexer.md)
-   [ASF-Indexer](asf-index-object.md)

Die folgenden Themen enthalten Schritt-für-Schritt-Anleitungen zum Verwenden von wmcontainer zum Lesen oder Schreiben von ASF-Dateien.

-   [Tutorial: Lesen einer ASF-Datei mithilfe von wmcontainer-Objekten](tutorial--reading-an-asf-file.md)
-   [Tutorial: Kopieren von ASF-Streams mithilfe von wmcontainer-Objekten](tutorial--copying-asf-streams-from-one-file-to-another.md)
-   [Tutorial: Schreiben einer WMA-Datei mithilfe von wmcontainer-Objekten](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)

## <a name="about-wm-container"></a>Informationen zum WM-Container

Die wmcontainer-Objekte interagieren direkt mit den ASF-Datei Objekten. Das folgende Diagramm zeigt die Struktur der ASF-Datei und die entsprechenden wmcontainer-Objekte.

![Diagramm mit der ASF-Dateistruktur und den zugehörigen Media Foundation-Objekten](images/asf-components01.png)

Mit Ausnahme von Splitter und Multiplexer unterstützt jedes dieser Objekte sowohl das Auswerten (lesen) als auch das Schreiben von ASF-Dateien. Der Splitter wird nur zum Lesen von ASF-Dateien verwendet. Der Multiplexer wird nur zum Erstellen von neuen ASF-Dateien verwendet.

Alle von wmcontainer-Objekten ausgeführten Vorgänge sind synchron, was bedeutet, dass der aufrufende Thread blockiert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



