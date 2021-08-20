---
description: ASF Indexer
ms.assetid: 3f95b0ac-d70f-4bc2-8524-c7de1df34afa
title: ASF Indexer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adde38583d70bdbc23382e6d57316cc92b5fbd3963560a10960acbe29ea97624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881141"
---
# <a name="asf-indexer"></a>ASF Indexer

Der *ASF-Indexer* ist eine WMContainer-Schichtkomponente, die zum Lesen oder Schreiben von Indexobjekten in einer ASF-Datei (Advanced Systems Format) verwendet wird. Informationen zur Struktur einer ASF-Datei finden Sie unter [ASF-Dateistruktur.](asf-file-structure.md)

Eine Anwendung kann den Indexer verwenden, um Suchaufgaben basierend auf der Präsentationszeit auszuführen oder neue Indexeinträge für eine ASF-Datei zu generieren. Der ASF-Indexer implementiert die [**IMFASFIndexer-Schnittstelle.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Indextyp</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Präsentationszeitbasierter Index</td>
<td>Bietet eine präsentationszeitbasierte Indizierung für Audio- und Videostreams in Indexblöcken, um die Indizierung effizienter zu gestalten. Jeder Indexblock verweist auf Indexeinträge, die einen Byteoffset enthalten. <br/> Der Offset ist die Position des gesuchten Datenpakets relativ zum Anfang des ASF-Datenobjekts.<br/> GUID_NULL muss als GUID-Typ für den Indexbezeichner verwendet werden. Weitere Informationen: siehe <a href="using-the-indexer-to-write-a-new-index.md">Verwenden des Indexers zum Schreiben eines neuen Indexes.</a><br/></td>
</tr>
<tr class="even">
<td>Timecodeindex</td>
<td>Erleichtert die Suche nach Timecode in Datenströmen, die Timecodemetadaten enthalten. Die Zeitcodes entsprechen einem SMPTE-Format (<em>Hours:Minutes:Seconds:Frames</em>). Jeder Indexblock verweist auf Indexeinträge, die einen Byteoffset enthalten. <br/> Der Offset ist die Position des gesuchten Datenpakets relativ zum Anfang des ASF-Datenobjekts.<br/>
<blockquote>
[!Note]<br />
Timecodeindexobjekte werden derzeit nicht unterstützt.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>Framebasierter Index</td>
<td>Stellt framebasierte Indizierung für Videostreams bereit. Indizes im framebasierten Index sind framebasierte Zahlen, wobei der erste Frame für einen Stream in der ASF-Datei dem Eintrag 0 im framebasierten Indexobjekt entspricht. Jeder Indexblock verweist auf Indexeinträge, die einen Byteoffset enthalten.<br/>
<blockquote>
[!Note]<br />
Framebasierte Indexobjekte werden derzeit nicht unterstützt.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

In diesem Abschnitt werden die folgenden Themen behandelt:



| Thema                                                                                | Beschreibung                                                                                                                      |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Indexererstellung und -konfiguration](indexer-creation-and-configuration.md)         | Hier erfahren Sie, wie Sie ein Indexerobjekt erstellen und zum Lesen eines vorhandenen Indexes oder zum Schreiben eines neuen ASF-Indexobjekts für eine Datei konfigurieren. |
| [Verwenden des Indexers zum Suchen in einer Datei](using-the-indexer-to-seek.md)                 | Verwenden des Indexers zum Suchen innerhalb einer ASF-Datei.                                                                               |
| [Verwenden des Indexers zum Schreiben eines neuen Indexes](using-the-indexer-to-write-a-new-index.md) | Hier erfahren Sie, wie Sie den Indexer verwenden, um Indexeinträge zu generieren und ein neues Indexobjekt für eine ASF-Datei zu schreiben.                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMContainer ASF-Komponenten](wmcontainer-asf-components.md)
</dt> <dt>

[ASF-Unterstützung in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




