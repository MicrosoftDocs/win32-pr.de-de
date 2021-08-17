---
description: ASF-Unterstützung in Media Foundation
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: ASF-Unterstützung in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db06c5a294e351b09d7f5327e8ee22891798671765bc5cc10eafd75785debde9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880957"
---
# <a name="asf-support-in-media-foundation"></a>ASF-Unterstützung in Media Foundation

Media Foundation unterstützt Mediendateien im Advanced Systems Format (ASF):

-   Windows Medienvideo (WMV-Dateien)
-   Windows Medienaudio (WMA-Dateien)

Media Foundation stellt mehrere Objekte zum Lesen und Schreiben von ASF-Dateien bereit. Diese Objekte werden in zwei verschiedenen Architekturebenen bereitgestellt.

Zunächst enthält die *Pipelineebene* Objekte, die innerhalb der [Media Foundation Pipeline](media-foundation-pipeline.md) funktionieren und den von der Pipeline definierten APIs entsprechen. Die ASF-Pipelineebene enthält Folgendes:

-   [ASF-Medienquelle:](asf-media-source.md)Analysiert ASF-Dateien und übermittelt die Audio-/Videodatenpakete.
-   [Windows Mediencodecs:](windows-media-codecs.md)Decodieren oder Codieren Windows Medienaudio- oder Videostreams.
-   [ASF-Mediensenke:](asf-media-sinks.md)Empfängt Datenpakete und schreibt eine ASF-Datei.

Zweitens bietet die WM-Containerebene eine Steuerung auf niedriger Ebene über das Analysieren und Schreiben einer ASF-Datei. Die Pipelineebene verwendet WMContainer intern. Anwendungen können WMContainer auch für asf-Analyse und -Schreibfunktionen auf niedriger Ebene verwenden.

![Diagramm mit Elementen der Pipelineebene und des WM-Containers](images/asf-components.png)

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                         | Beschreibung                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [ASF-Dateistruktur](asf-file-structure.md)<br/>                       | Übersicht über die ASF-Dateistruktur und die von Media Foundation bereitgestellten Objekte für die Arbeit mit ASF-Dateien.<br/> |
| [ASF-Komponenten auf Pipelineebene](pipeline-layer-asf-components.md)<br/> | Beschreibt, wie ASF-Dateien mithilfe der Pipelineebene analysiert und erstellt werden.<br/>                                   |
| [WMContainer ASF-Komponenten](wmcontainer-asf-components.md)<br/>       | Beschreibt, wie ASF-Dateien mithilfe der WMContainer-Ebene analysiert und erstellt werden.<br/>                                |



 

Ausführliche Informationen zur Struktur einer ASF-Datei finden Sie in der ASF-Spezifikation, die von dieser [Microsoft-Website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea)heruntergeladen werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Programmierhandbuch](media-foundation-programming-guide.md)
</dt> </dl>

 

 




