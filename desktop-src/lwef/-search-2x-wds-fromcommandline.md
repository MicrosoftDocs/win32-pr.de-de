---
title: Aufrufen von WDS über die Befehlszeile
description: Sie können die Benutzeroberfläche der Microsoft Windows-Desktop Suche (WDS) mit einem bestimmten Filter, einem bestimmten Speicher oder einer Webseite starten, die das Browserhilfsobjekt (BHO) mithilfe der windowssearch.exe Befehlszeilen Syntax verwendet.
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efae7aebc13f578e9c5c32542b451d3600a93a2b
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "103724019"
---
# <a name="calling-wds-from-the-command-line"></a>Aufrufen von WDS über die Befehlszeile

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .

Sie können die Benutzeroberfläche der Microsoft Windows-Desktop Suche (WDS) mit einem bestimmten Filter, einem bestimmten Speicher oder einer Webseite starten, die das Browserhilfsobjekt (BHO) mithilfe der windowssearch.exe Befehlszeilen Syntax verwendet. Wenn WDS von der Befehlszeile aufgerufen wird, werden keine Informationen über die Aktionen des Benutzers oder die Auswahl im WDS-Fenster an die aufrufenden Anwendung oder Webseite zurückgegeben.

Der WDS-Installationspfad wird in der Registrierungs Einstellung INSTALLDIR unter HKEY_LOCAL_MACHINE \\ Software \\ Microsoft \\ Windows-Desktop Suche angegeben. Der Standardpfad, auf windowssearch.exe installiert wird, ist Programme \\ Windows-Desktop Suche.

## <a name="command-line-syntax"></a>Befehlszeilensyntax

Die folgende Syntax gilt für die Befehlszeilenschnittstelle der Windows-Desktop Suche 2. x.



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

<td>Initialisiert die Windows-Desktop Suche.</td>
</tr>
<tr class="even">
<td>/indexnow</td>

<td>Deaktiviert die Indizierung und schaltet alle Index Speicherorte um.</td>
</tr>
<tr class="odd">
<td>/showstatus</td>

<td>Zeigt das Fenster "Index Status" an</td>
</tr>
<tr class="even">
<td>/launchsearchwindow oder/URL</td>

<td>Öffnet ein WDS-Fenster mit einer leeren Abfrage.</td>
</tr>
<tr class="odd">
<td>/url</td>
<td>Search: [Store | Show | Abfrage] Abfrage Zeichenfolge</td>
<td>Öffnet ein WDS-Fenster mit einer Abfrage und einem Filter basierend auf den folgenden Parametern:
<ul>
<li><p>Store: gibt die Datenquelle für die Abfrage an: Dateien, Outlook, OutlookExpress. Wenn nicht angegeben, werden alle Geschäfte durchsucht. <br/></p>
<blockquote>
[!Note]<br />
Obwohl die Erweiterte Abfrage Syntax das verweisen auf Microsoft Outlook als ' OE ' unterstützt, muss der Store-Parameter in der Befehlszeile ' OutlookExpress ' lauten.
</blockquote>
<p><br/></p></li>
<li><p>Show: gibt an, welche wahrgenommenen Ergebnisse zurückgegeben werden sollen. Eine umfassende Liste der Typen finden Sie unter <a href="-search-2x-wds-perceivedtype.md">wahrgenommene Typen</a> . Wenn nicht angegeben, werden alle Typen zurückgegeben. <br/></p>
<blockquote>
[!Note]<br />
Es gibt drei Unterschiede zwischen den wahrgenommenen Typwerten und den Werten für "anzeigen". Verwenden Sie für <code>show</code> "Dokumente" anstelle von "doc", "Bilder" anstelle von "Fotos" und "textdocuments" anstelle von "Text".
</blockquote>
<p><br/></p></li>
<li>Query: gibt die Suchkriterien an. Dieser Wert unterstützt <a href="-search-2x-wds-aqsreference.md">Erweiterte Abfrage Syntax</a> Parameter, um die Ergebnisse zu verfeinern. Der Abfrage Parameter muss der letzte Parameter in der URL sein.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="example"></a>Beispiel

Verwenden Sie beispielsweise den folgenden Befehl, um alle Dateien nach Bildern zu durchsuchen, die mit den Kriterien für das Hintergrund übereinstimmen:

`WindowsSearch.exe /url search:store=files&show=pictures&query=wallpaper`

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Erweiterte Abfragesyntax](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Wahrgenommene Typen](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Aufrufen von WDS von Webseiten](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





