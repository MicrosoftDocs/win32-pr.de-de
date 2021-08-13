---
title: Aufrufen von WDS über die Befehlszeile
description: Sie können die Benutzeroberfläche von Microsoft Windows Desktop Search (WDS) mit einem bestimmten Filter, Speichern und Abfragen aus einer anderen Anwendung oder einer Webseite starten, die das Browser helper Object (BHO) verwendet, indem Sie die windowssearch.exe-Befehlszeilensyntax verwenden.
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ba9fa8310af43340ef71c5d7e574f1b95addca86a4f90051dc85f593f43302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753216"
---
# <a name="calling-wds-from-the-command-line"></a>Aufrufen von WDS über die Befehlszeile

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren [Versionen Windows Search.](../search/-search-3x-wds-overview.md)

Sie können die Benutzeroberfläche von Microsoft Windows Desktop Search (WDS) mit einem bestimmten Filter, Speichern und Abfragen aus einer anderen Anwendung oder einer Webseite starten, die das Browser helper Object (BHO) verwendet, indem Sie die windowssearch.exe-Befehlszeilensyntax verwenden. Beim Aufrufen von WDS über die Befehlszeile werden keine Informationen über die Aktionen oder Die Auswahl des Benutzers im WDS-Fenster an die aufrufende Anwendung oder Webseite zurückgegeben.

Der WDS-Installationspfad wird in der Registrierungseinstellung InstallDir unter HKEY_LOCAL_MACHINE \\ Software Microsoft Windows Desktop Search \\ \\ angegeben. Der Standardpfad, in windowssearch.exe installiert ist, ist Programmdateien \\ Windows Desktopsuche.

## <a name="command-line-syntax"></a>Befehlszeilensyntax

Die folgende Syntax gilt für die Windows Desktop Search 2.x-Befehlszeilenschnittstelle.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Optionen</th>
<th>Parameter</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>/startup</td>

<td>Initialisiert Windows Desktopsuche</td>
</tr>
<tr class="even">
<td>/indexnow</td>

<td>Deaktiviert das Indizierungs-Back-Off und scannt alle Indexpositionen erneut.</td>
</tr>
<tr class="odd">
<td>/showstatus</td>

<td>Zeigt das Indizierungsstatusfenster an.</td>
</tr>
<tr class="even">
<td>/launchsearchwindow oder /url</td>

<td>Öffnet ein WDS-Fenster mit einer leeren Abfrage.</td>
</tr>
<tr class="odd">
<td>/url</td>
<td>search:[store|show|query] abfragezeichenfolge</td>
<td>Öffnet ein WDS-Fenster mit einer Abfrage und filtert basierend auf den folgenden Parametern:
<ul>
<li><p>store: Gibt die datenquelle an, die sie abfragen soll: files, outlook, outlookexpress. Wenn nicht angegeben, werden alle Filialen durchsucht. <br/></p>
<blockquote>
[!Note]<br />
Die erweiterte Abfragesyntax unterstützt zwar das Verweisen auf Microsoft Outlook als "oe", der store-Parameter in der Befehlszeile muss jedoch "outlookexpress" sein.
</blockquote>
<p><br/></p></li>
<li><p>show: Gibt an, welcher wahrgenommene Ergebnistyp zurückgeben werden soll. Eine <a href="-search-2x-wds-perceivedtype.md">vollständige Liste der Typen</a> finden Sie unter Wahrgenommene Typen. Wenn kein Wert angegeben wird, werden alle Typen zurückgegeben. <br/></p>
<blockquote>
[!Note]<br />
Es gibt drei Unterschiede zwischen den wahrgenommenen Typwerten und den Werten für show. Verwenden <code>show</code> Sie für "Dokumente" anstelle von "doc", "pictures" anstelle von "pics" und "textdocuments" anstelle von "text".
</blockquote>
<p><br/></p></li>
<li>query: Gibt die Suchkriterien an. Dieser Wert unterstützt <a href="-search-2x-wds-aqsreference.md">Erweiterte Abfragesyntaxparameter,</a> um die Ergebnisse zu verfeinern. Der Abfrageparameter muss der letzte Parameter in der URL sein.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="example"></a>Beispiel

Um beispielsweise alle Dateien nach Bildern zu durchsuchen, die den Kriterien "Hintergrund" entsprechen, verwenden Sie den folgenden Befehl:

`WindowsSearch.exe /url search:store=files&show=pictures&query=wallpaper`

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Erweiterte Abfragesyntax](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Wahrgenommene Typen](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Aufrufen von WDS über Webseiten](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





