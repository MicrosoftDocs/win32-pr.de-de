---
description: ASF-Indexer
ms.assetid: 3f95b0ac-d70f-4bc2-8524-c7de1df34afa
title: ASF-Indexer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c729b547339149ee578a90283c570ec8460b0c57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338945"
---
# <a name="asf-indexer"></a>ASF-Indexer

Der ASF- *Indexer* ist eine wmcontainer-Ebenenkomponente, die verwendet wird, um Index Objekte in einer ASF-Datei (Advanced Systems Format) zu lesen oder zu schreiben. Weitere Informationen zur Struktur einer ASF-Datei finden Sie unter [Struktur der ASF-Datei](asf-file-structure.md).

Eine Anwendung kann den Indexer verwenden, um Suchvorgänge auf der Grundlage der Präsentationszeit auszuführen oder um neue Indexeinträge für eine ASF-Datei zu generieren. Der ASF-Indexer implementiert die [**imfasfindexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) -Schnittstelle.



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
<td>Präsentationszeit basierter Index</td>
<td>Stellt die Präsentationszeit basierte Indizierung für Audiodaten und Videostreams in Indexblöcken bereit, um die Indizierung zu erhöhen. Jeder Indexblock verweist auf Indexeinträge, die einen Byte Offset enthalten. <br/> Der Offset ist die Position des Datenpakets, das Seeding ist, relativ zum Anfang des ASF-Datenobjekts.<br/> GUID_NULL muss als GUID-Typ für den Index Bezeichner verwendet werden. Weitere Informationen finden Sie unter. Weitere Informationen finden <a href="using-the-indexer-to-write-a-new-index.md">Sie unter Verwenden des Indexers zum Schreiben eines neuen Indexes</a>.<br/></td>
</tr>
<tr class="even">
<td>Timecode-Index</td>
<td>Ermöglicht das Suchen nach Zeitcode in Streams, die Zeitcode-Metadaten enthalten. Die Timecodes entsprechen einem SMPTE-Format (<em>Stunden: Minuten: Sekunden: Frames</em>). Jeder Indexblock verweist auf Indexeinträge, die einen Byte Offset enthalten. <br/> Der Offset ist die Position des Datenpakets, das Seeding ist, relativ zum Anfang des ASF-Datenobjekts.<br/>
<blockquote>
[!Note]<br />
Timecode-Index Objekte werden zurzeit nicht unterstützt.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>Frame basierter Index</td>
<td>Stellt eine Frame basierte Indizierung für Videostreams bereit. Indizes in den Frame basierten Index entsprechen Frame Nummern, wobei der erste Frame für einen Datenstrom in der ASF-Datei dem Eintrag 0 im Frame basierten Index Objekt entspricht. Jeder Indexblock verweist auf Indexeinträge, die einen Byte Offset enthalten.<br/>
<blockquote>
[!Note]<br />
Frame basierte Index Objekte werden zurzeit nicht unterstützt.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

In diesem Abschnitt werden die folgenden Themen behandelt:



| Thema                                                                                | BESCHREIBUNG                                                                                                                      |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Erstellung und Konfiguration von Indexern](indexer-creation-and-configuration.md)         | So erstellen Sie ein Indexer-Objekt und konfigurieren es für das Lesen eines vorhandenen Indexes oder das Schreiben eines neuen ASF-Index Objekts für eine Datei. |
| [Verwenden des Indexers zum Suchen in einer Datei](using-the-indexer-to-seek.md)                 | Verwenden des Indexers, um in einer ASF-Datei zu suchen.                                                                               |
| [Verwenden des Indexers zum Schreiben eines neuen Indexes](using-the-indexer-to-write-a-new-index.md) | Verwenden des Indexers, um Indexeinträge zu generieren und ein neues Index Objekt für eine ASF-Datei zu schreiben.                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wmcontainer-ASF-Komponenten](wmcontainer-asf-components.md)
</dt> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




