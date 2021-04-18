---
description: Hinzufügen von Ausgabe Knoten mit topoedit
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: Hinzufügen von Ausgabe Knoten mit topoedit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84dc30631332e8138b35e4bbc0ccde75ec9b0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347751"
---
# <a name="adding-output-nodes-with-topoedit"></a>Hinzufügen von Ausgabe Knoten mit topoedit

In einer Topologie stellt ein Ausgabe Knoten eine Medien Senke dar, die Mediendaten von einem Transformations Knoten empfängt und für die Wiedergabe darstellt. Der Typ des Ausgabe Knotens hängt vom Medientyp des Quell Knotens ab.

Die folgende Tabelle zeigt den Menübefehl bzw. den Symbolleisten Befehl zum Hinzufügen eines Ausgabe Knotens zur Topologie.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Quell Medientyp</th>
<th>Menü/Symbolleisten Befehl</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Audiodatenstrom</td>
<td>Klicken Sie im Menü <strong>Topologie</strong> auf <strong>SAR hinzufügen</strong>.</td>
<td>Erstellt einen Ausgabe Knoten für den streamingaudiorenderer (SAR), der einen Audiostream über ein Audiogerät (z. b. eine Soundkarte) wieder gibt.</td>
</tr>
<tr class="even">
<td>Videostream</td>
<td>Klicken Sie im Menü <strong>Topologie</strong> auf <strong>EVR hinzufügen</strong>.</td>
<td>Erstellt einen Ausgabe Knoten für den erweiterten Videorenderer (EVR), der Frames für einen Videostream anzeigt.</td>
</tr>
<tr class="odd">
<td>Benutzerdefinierte Medien Senke</td>
<td><ol>
<li>Klicken Sie im Menü <strong>Topologie</strong> auf <strong>benutzerdefinierte Senke hinzufügen</strong>.<br/> Das Dialogfeld <strong>benutzerdefinierte GUID eingeben</strong> wird geöffnet.<br/></li>
<li><p>Geben Sie im Feld <strong>GUID:</strong> die GUID der benutzerdefinierten Senke ein, die Sie der Topologie hinzufügen möchten.<br/></p>
<blockquote>
[!Note]<br />
Topoedit erwartet die GUID im Format &quot; {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} &quot; . Andernfalls kann der Knoten nicht hinzugefügt werden, und es wird eine &quot; ungültige GUID- &quot; Fehlermeldung angezeigt.
</blockquote>
<p><br/></p></li>
<li>Klicken Sie auf <strong>OK</strong>.<br/></li>
</ol></td>
<td>Erstellt einen Ausgabe Knoten für die streamsenke für eine benutzerdefinierte Medienquelle.<br/> Die benutzerdefinierte Senke muss <strong>cokreateinstance</strong> unterstützen, damit die Senke mit einer CLSID angegeben werden kann.<br/></td>
</tr>
</tbody>
</table>



 

Topoedit erstellt den angegebenen Ausgabe Knoten. Im Bereich **Topologie** wird der Ausgabe Knoten als grünes Feld angezeigt, in dem der Name der Datenstrom Senke angezeigt wird.

Informationen zum programmgesteuerten Hinzufügen von Ausgabe Knoten mithilfe Media Foundation APIs finden Sie unter [Erstellen von Ausgabe Knoten](creating-output-nodes.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von Topologien mithilfe von topoedit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Streamingaudiorenderer](streaming-audio-renderer.md)
</dt> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> <dt>

[Topoedit](topoedit.md)
</dt> </dl>

 

 




