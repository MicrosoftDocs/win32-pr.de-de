---
description: Die Unterstützung von Windows 7 zum Durchsuchen von Verbund zu Remote Daten speichern mithilfe von OpenSearch-Technologien ermöglicht Benutzern den Zugriff auf und die Interaktion mit ihren Remote Daten aus Windows-Explorer.
ms.assetid: c25dbc33-3f9a-4e40-965e-9be639ababed
title: Ersten Einstieg in die Verbund Suche in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058c1f887ff2bdba279cdd25e4910162dd9263d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525469"
---
# <a name="getting-started-with-federated-search-in-windows"></a>Ersten Einstieg in die Verbund Suche in Windows

Die Unterstützung von Windows 7 zum Durchsuchen von Verbund zu Remote Daten speichern mithilfe von OpenSearch-Technologien ermöglicht Benutzern den Zugriff auf und die Interaktion mit ihren Remote Daten aus Windows-Explorer. Sie können einen webbasierten Datenspeicher erstellen, der mithilfe der Windows-Verbund Suche durchsucht werden kann, und eine umfassende Integration Ihrer Remote Datenquellen mit Windows-Explorer aktivieren, ohne dass Windows-Client seitiger Code geschrieben oder bereitgestellt werden muss.

Dieses Thema ist wie folgt organisiert:

-   [Was ist eine Verbund Suche?](#what-is-federated-search)
-   [Schritte zum Aufbauen der Verbund Suche](#steps-for-building-federated-search)
-   [Funktionsweise der Verbund Suche](#how-federated-search-works)
-   [Senden von Abfragen und Zurückgeben von Suchergebnissen in RSS oder Atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [Beispiele für die Verbund Suche](#federated-search-examples)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="what-is-federated-search"></a>Was ist eine Verbund Suche?

Windows 7 unterstützt die Verbindung externer Quellen mit dem Windows-Client über das [OpenSearch](https://github.com/dewitt/opensearch) -Protokoll. Dies ermöglicht es Benutzern, in Windows-Explorer einen Remote Datenspeicher zu durchsuchen und Ergebnisse anzuzeigen. Der Standard [OpenSearch](https://github.com/dewitt/opensearch) v 1.1 definiert einfache Dateiformate, die verwendet werden können, um zu beschreiben, wie ein Client den Webdienst für den Datenspeicher Abfragen soll und wie der Dienst Ergebnisse zurückgeben soll, die vom Client gerendert werden sollen. Die Windows-Verbund Suche stellt eine Verbindung mit Webdiensten her, die [OpenSearch](https://github.com/dewitt/opensearch) -Abfragen empfangen, und gibt Ergebnisse entweder im RSS-oder Atom-XML-Format zurück.

Der folgende Screenshot veranschaulicht die Suchergebnisse, die nach der Remote Suche einer SharePoint-Website abgerufen werden.

![Screenshot, der Suchergebnisse von einer SharePoint-Website anzeigt, wie in Windows-Explorer angezeigt](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a>Schritte zum Aufbauen der Verbund Suche

Führen Sie die folgenden Schritte aus, um eine Verbund Suche zu erstellen:

1.  Aktivieren Sie den Datenspeicher in Windows-Explorer, indem Sie einen [OpenSearch](https://github.com/dewitt/opensearch)-kompatiblen Webdienst bereitstellen, der Ergebnisse im RSS-oder Atom-Format zurückgeben kann.
2.  Erstellen Sie eine OpenSearch-Beschreibungsdatei (OSDX-Datei), in der beschrieben wird, wie eine Verbindung mit dem Webdienst hergestellt wird und wie benutzerdefinierte Elemente in der RSS-oder Atom-XML-Datei
3.  Stellen Sie die Suchconnectors auf Windows-Client Computern mit einer OSDX-Datei bereit.

Das folgende Diagramm veranschaulicht die Schritte zum Aufbau der Verbund Suche.

![Diagramm des Prozesses zum Aufbauen der Verbund Suche](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a>Funktionsweise der Verbund Suche

Die Kommunikation zwischen Windows-Explorer und Ihrem [OpenSearch](https://github.com/dewitt/opensearch) -Webdienst erfolgt über die Windows-Datenschicht. Die Windows-Datenschicht kann über Windows Store-Anbieter mit unterschiedlichen Datenspeicher Typen kommunizieren. Jeder Anbieter spezialisiert sich auf die Kommunikation mit Daten speichern, die ein bestimmtes Protokoll unterstützen und über bestimmte Funktionen verfügen. Die folgende Abbildung zeigt z. b., wie der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter mit Daten speichern kommuniziert, die einen Webdienst bereitstellen, der den [OpenSearch](https://github.com/dewitt/opensearch) -Standard unterstützt.

![Diagramm, das die Kommunikation von Windows-Explorer auf dem Client über den OpenSearch-Datenspeicher auf dem Remote Server anzeigt](images/windowssearchfederationfunctionality.png)

Um dem Datenspeicher die Unterstützung der Verbund Suche in Windows 7 zu ermöglichen, müssen Sie eine Reihe von Tasks ausführen. In der folgenden Tabelle sind die Aufgaben zum Aktivieren des Datenspeicher, zum Ausführen der einzelnen Aufgaben und zum Speicherort der Dokumentation aufgeführt.



| Aufgabe                                                                                                     | Anforderung                                                                                                                                                                                            | Dokumentation                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aktivieren Sie den Datenspeicher, der von Windows Explorer durchsucht werden soll.<br/>                                    | Erstellen Sie einen mit OpenSearch kompatiblen Webdienst.<br/> Erstellen Sie eine OpenSearch-Beschreibungsdatei (OSDX-Datei).<br/>                                                                                       | [Verbinden des Webdiensts in der Windows-Verbund Suche](-search-federated-search-web-service.md)<br/> [Aktivieren des Datenspeicher in der Windows-Verbund Suche](-search-federated-search-data-store.md)<br/> |
| Stellen Sie Ihren Webdienst aktiv für Benutzer in einem Unternehmen bereit.<br/>                               | Stellen Sie eine OSDX-Datei für Ihre Benutzer bereit, kopieren Sie Sie lokal, und machen Sie den Benutzer über eine Verknüpfung zugänglich.<br/>                                                                                     | [Bereitstellen von Suchconnectors in der Windows-Verbund Suche](-search-federated-search-deploying.md)<br/>                                                                                                              |
| Listet die Suchergebnisse in Windows-Explorer als Antwort auf eine Abfrage auf.<br/>                          | Implementieren Sie einen Webdienst, der eine Abfrage Zeichenfolge akzeptiert und Ergebnisse im RSS-oder Atom-Format zurückgibt.<br/>                                                                                              | [Verbinden des Webdiensts in der Windows-Verbund Suche](-search-federated-search-web-service.md)<br/>                                                                                                            |
| Ermöglichen Sie es Benutzern, Ihren Datenspeicher Ihrem Windows-Explorer hinzuzufügen.<br/>                                | Erstellen Sie eine OSDX-Datei, und stellen Sie Sie für Ihre Benutzer bereit.<br/>                                                                                                                                           | [Aktivieren des Datenspeicher in der Windows-Verbund Suche](-search-federated-search-data-store.md)<br/>                                                                                                                |
| Zeigen Sie Ihre Elemente in Windows-Explorer als Datei ähnliche Elemente an.<br/>                                    | Zurückgeben einer URL zum Datei-oder Inhaltsstream mithilfe von **Gehäuse** oder **Medien: Inhalts** Elemente<br/> Geben Sie eine Dateinamenerweiterung oder einen MIME-Typ an, der vom Client Computer erkannt wird.<br/> | [Aktivieren des Datenspeicher in der Windows-Verbund Suche](-search-federated-search-data-store.md)<br/>                                                                                                                |
| Anzeigen benutzerdefinierter Eigenschaften in Windows-Explorer, außer den in den RSS-oder Atom-Standards definierten.<br/> | Stellen Sie zusätzliche Metadaten bereit, indem Sie einen anderen XML-Namespace in der RSS/Atom-Ausgabe verwenden.<br/> Fügen Sie der OSDX-Datei eine Eigenschaften Zuordnung hinzu.<br/>                                                       | [Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Passen Sie die Eigenschaften an, die für ihre Elemente in Windows-Explorer angezeigt werden.<br/>               | Fügen Sie der OSDX-Datei proplist-Zuordnungen hinzu.<br/>                                                                                                                                                   | [Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Zeigen Sie eine benutzerdefinierte Webseiten Ansicht Ihrer Elemente im Vorschaubereich an.<br/>                              | Gibt eindeutige Link-und Gehäuse Werte zurück.<br/> Ordnen Sie der Windows Shell-Eigenschaft **System. webpreviewurl** einen URL-Wert zu.<br/>                                                               | [Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Anzeigen einer Befehls leisten Schaltfläche in Windows-Explorer, die die Abfrage auf Ihre Website überträgt.<br/>   | Stellen Sie eine `Url format="text/html"` Vorlage in der OSDX-Datei bereit.<br/>                                                                                                                              | [Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Senden von Abfragen und Zurückgeben von Suchergebnissen in RSS oder Atom

Wenn der Benutzer einen Begriff in das Suchfeld in der oberen rechten Ecke von Windows-Explorer eingibt, wird die Abfrage an den [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter gesendet, der die Abfrage dann an den Remote Datenspeicher sendet. Der Remoteweb Dienst antwortet auf die Abfrage, indem Ergebnisse in einem XML-Dokument (in der Regel als Feed bezeichnet) in einem von zwei unterstützten Formaten (RSS oder Atom) bereitgestellt werden. Jedes Ergebnis Element im Feed enthält untergeordnete XML-Elemente, um Element Metadaten darzustellen oder zu beschreiben, wie z. b. Titel, URL, Beschreibung, Miniaturbild und so weiter. Der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter ist für die Zuordnung der XML-Element Werte zu den Windows Shell-Systemeigenschaften zuständig, die von Windows-Anwendungen verwendet werden können.

## <a name="federated-search-examples"></a>Beispiele für die Verbund Suche

Die folgende OpenSearch-Beispieldatei (OSDX-Datei) besteht aus `ShortName` -und- `Url` Elementen, bei denen es sich um die mindestens erforderlichen untergeordneten Elemente handelt, um einen externen Datenspeicher mit dem Windows-Client über das OpenSearch-Protokoll zu verbinden.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



Im folgenden Beispiel wird veranschaulicht, wie Sie einen webfähigen Datenspeicher im RSS-Format durchsuchbar machen und angeben, dass ein Suchelement zurückgegeben werden soll:


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, then you would be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



Im folgenden Beispiel wird veranschaulicht, wie Eigenschaften zu Standardsystem Eigenschaften zugeordnet werden, damit angezeigte Elemente sortiert und gruppiert werden:


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



Im folgenden Beispiel wird veranschaulicht, wie jedem Element in Windows-Explorer eine Miniaturbild Anzeige hinzugefügt wird:


```
<media:thumbnail>    
```



## <a name="additional-resources"></a>Weitere Ressourcen

Weitere Informationen zum Implementieren eines Such Verbunds in Remote Datenspeicher mithilfe von OpenSearch-Technologien in Windows 7 und höher finden Sie unter "zusätzliche Ressourcen" bei der [Verbund Suche in Windows](-search-federated-search-overview.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbundsuche in Windows 10](-search-federated-search-overview.md)
</dt> <dt>

[Verbinden des Webdiensts in der Windows-Verbund Suche](-search-federated-search-web-service.md)
</dt> <dt>

[Aktivieren des Datenspeicher in der Windows-Verbund Suche](-search-federated-search-data-store.md)
</dt> <dt>

[Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche](-search-federated-search-osdx-file.md)
</dt> <dt>

[Bewährte Methoden bei der Windows-Verbund Suche](-search-fedsearch-best.md)
</dt> <dt>

[Bereitstellen von Suchconnectors in der Windows-Verbund Suche](-search-federated-search-deploying.md)
</dt> </dl>

 

 




