---
description: Unterstützung von ASF in Media Foundation
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: Unterstützung von ASF in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb7774d0ddaee592cb583ffb771c900642ed216
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106366367"
---
# <a name="asf-support-in-media-foundation"></a>Unterstützung von ASF in Media Foundation

Media Foundation unterstützt Mediendateien im Advanced Systems-Format (ASF):

-   Windows Media Video (WMV-Dateien)
-   Windows Media Audio (WMA-Dateien)

Media Foundation stellt mehrere Objekte zum Lesen und Schreiben von ASF-Dateien bereit. Diese Objekte werden in zwei verschiedenen Architektur Ebenen bereitgestellt.

Zunächst enthält die *Pipeline* Schicht Objekte, die innerhalb der [Media Foundation Pipeline](media-foundation-pipeline.md) funktionieren und den von der Pipeline definierten APIs entsprechen. Die ASF-Pipeline Ebene enthält Folgendes:

-   [ASF-Medienquelle](asf-media-source.md): analysiert ASF-Dateien und übermittelt die Audiodaten-Datenpakete.
-   [Windows Media Codecs](windows-media-codecs.md): decodieren oder Codieren von Windows Media-Audiodaten und-Videostreams.
-   [ASF-Medien Senke](asf-media-sinks.md): empfängt Datenpakete und schreibt eine ASF-Datei.

Zweitens bietet die WM-Container Schicht eine Low-Level-Kontrolle über das Auswerten und Schreiben einer ASF-Datei. Die Pipeline Schicht verwendet intern wmcontainer. Anwendungen können auch wmcontainer für die Verwendung von ASF-und Schreib vornissen auf niedriger Ebene verwenden.

![Diagramm, das Elemente der Pipeline Schicht und des WM-Containers anzeigt](images/asf-components.png)

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                         | BESCHREIBUNG                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Struktur der ASF-Datei](asf-file-structure.md)<br/>                       | Übersicht über die Struktur der ASF-Datei und die von Media Foundation bereitgestellten Objekte zum Arbeiten mit ASF-Dateien.<br/> |
| [Komponenten der Pipeline Schicht-ASF](pipeline-layer-asf-components.md)<br/> | Beschreibt das analysieren und Erstellen von ASF-Dateien mithilfe der Pipeline Schicht.<br/>                                   |
| [Wmcontainer-ASF-Komponenten](wmcontainer-asf-components.md)<br/>       | Beschreibt das analysieren und Erstellen von ASF-Dateien mithilfe der wmcontainer-Ebene.<br/>                                |



 

Ausführliche Informationen zur Struktur einer ASF-Datei finden Sie in der ASF-Spezifikation, die von dieser [Microsoft-Website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea)heruntergeladen werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Programmier Handbuch](media-foundation-programming-guide.md)
</dt> </dl>

 

 




