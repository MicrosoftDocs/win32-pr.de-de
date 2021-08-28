---
title: Aufrufen von WDS über die Befehlszeile
description: Sie können die Benutzeroberfläche der Microsoft Windows-Desktopsuche (WDS) mit einem bestimmten Filter, Speichern und Abfragen aus einer anderen Anwendung oder einer Webseite starten, die das Browser helper Object (BHO) verwendet, indem Sie die windowssearch.exe-Befehlszeilensyntax verwenden.
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac0125d9c4733654df7b2f6e08f49d10f5fee07
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467607"
---
# <a name="calling-wds-from-the-command-line"></a>Aufrufen von WDS über die Befehlszeile

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen [stattdessen Windows Search.](../search/-search-3x-wds-overview.md)

Sie können die Benutzeroberfläche der Microsoft Windows-Desktopsuche (WDS) mit einem bestimmten Filter, Speichern und Abfragen aus einer anderen Anwendung oder einer Webseite starten, die das Browser helper Object (BHO) verwendet, indem Sie die windowssearch.exe-Befehlszeilensyntax verwenden. Beim Aufrufen von WDS über die Befehlszeile werden keine Informationen über die Aktionen oder Die Auswahl des Benutzers im WDS-Fenster an die aufrufende Anwendung oder Webseite zurückgegeben.

Der WDS-Installationspfad wird in der Registrierungseinstellung InstallDir unter HKEY_LOCAL_MACHINE \\ Software Microsoft Windows Desktop Search \\ \\ angegeben. Der Standardpfad, in dem windowssearch.exe installiert ist, ist Programmdateien \\ Windows Desktopsuche.

## <a name="command-line-syntax"></a>Befehlszeilensyntax

Die folgende Syntax gilt für die Windows Desktop Search 2.x-Befehlszeilenschnittstelle.




| Optionen | Parameter | Bedeutung | 
|---------|-----------|---------|
| /startup | Initialisiert Windows Desktopsuche | 
| /indexnow | Deaktiviert das Indizierungs-Back-Off und scannt alle Indexpositionen erneut. | 
| /showstatus | Zeigt das Indizierungsstatusfenster an. | 
| /launchsearchwindow oder /url | Öffnet ein WDS-Fenster mit einer leeren Abfrage. | 
| /url | search:[store|show|abfrage] Abfragezeichenfolge | Öffnet ein WDS-Fenster mit einer Abfrage und filtert basierend auf den folgenden Parametern:<ul><li><p>store: Gibt die datenquelle an, die sie abfragen soll: files, outlook, outlookexpress. Wenn nicht angegeben, werden alle Filialen durchsucht. <br /></p><blockquote>[!Note]<br />Die erweiterte Abfragesyntax unterstützt zwar das Verweisen auf Microsoft Outlook als "oe", der store-Parameter in der Befehlszeile muss jedoch "outlookexpress" sein.</blockquote><p><br /></p></li><li><p>show: Gibt an, welcher wahrgenommene Ergebnistyp zurückgibt. Eine <a href="-search-2x-wds-perceivedtype.md">vollständige Liste der Typen</a> finden Sie unter Wahrgenommene Typen. Wenn kein Wert angegeben wird, werden alle Typen zurückgegeben. <br /></p><blockquote>[!Note]<br />Es gibt drei Unterschiede zwischen den wahrgenommenen Typwerten und den Werten für show. Verwenden <code>show</code> Sie für "Dokumente" anstelle von "doc", "pictures" anstelle von "pics" und "textdocuments" anstelle von "text".</blockquote><p><br /></p></li><li>query: Gibt die Suchkriterien an. Dieser Wert unterstützt <a href="-search-2x-wds-aqsreference.md">Erweiterte Abfragesyntaxparameter,</a> um die Ergebnisse zu verfeinern. Der Abfrageparameter muss der letzte Parameter in der URL sein.</li></ul> | 




 

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

 

 





