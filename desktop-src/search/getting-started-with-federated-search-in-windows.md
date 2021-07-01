---
description: Erfahren Sie mehr über die Verbundsuche, die es Benutzern ermöglicht, auf ihre Remotedaten innerhalb von Windows-Explorer.
ms.assetid: c25dbc33-3f9a-4e40-965e-9be639ababed
title: Erste Schritte mit Der Verbundsuche in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de3fc42686e94f2edc1c5d45bbb0374afe79535
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119065"
---
# <a name="getting-started-with-federated-search-in-windows"></a>Erste Schritte mit Der Verbundsuche in Windows

Die Windows 7-Unterstützung für den Suchverbund mit Remotedatenspeichern mithilfe von OpenSearch-Technologien ermöglicht Benutzern den Zugriff auf und die Interaktion mit ihren Remotedaten aus Windows-Explorer. Sie können einen webbasierten Datenspeicher erstellen, der mithilfe der Windows-Verbundsuche durchsucht werden kann, und eine umfassende Integration Ihrer Remotedatenquellen mit Windows-Explorer ermöglichen, ohne clientseitigen Windows-Code schreiben oder bereitstellen zu müssen.

Dieses Thema ist wie folgt organisiert:

-   [Was ist die Verbundsuche?](#what-is-federated-search)
-   [Schritte zum Erstellen der Verbundsuche](#steps-for-building-federated-search)
-   [Funktionsweise der Verbundsuche](#how-federated-search-works)
-   [Senden von Abfragen und Zurückgeben von Suchergebnissen in RSS oder Atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [Beispiele für die Verbundsuche](#federated-search-examples)
-   [Weitere Ressourcen](#additional-resources)
-   [Verwandte Themen](#related-topics)

## <a name="what-is-federated-search"></a>Was ist die Verbundsuche?

Windows 7 unterstützt die Verbindung externer Quellen mit dem Windows-Client über das [OpenSearch-Protokoll.](https://github.com/dewitt/opensearch) Auf diese Weise können Benutzer einen Remotedatenspeicher durchsuchen und Ergebnisse innerhalb Windows-Explorer. Der [OpenSearch](https://github.com/dewitt/opensearch) v1.1-Standard definiert einfache Dateiformate, die verwendet werden können, um zu beschreiben, wie ein Client den Webdienst nach dem Datenspeicher abfragen soll und wie der Dienst Ergebnisse zurückgeben soll, die vom Client gerendert werden sollen. Die Windows-Verbundsuche stellt eine Verbindung mit Webdiensten mit [OpenSearch-Abfragen](https://github.com/dewitt/opensearch) sicher und gibt Ergebnisse im RSS- oder Atom-XML-Format zurück.

Der folgende Screenshot veranschaulicht die Suchergebnisse, die nach der Remotesuche einer SharePoint-Website erzielt wurden.

![Screenshot: Suchergebnisse von einer SharePoint-Website, wie sie im Windows-Explorer angezeigt werden](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a>Schritte zum Erstellen der Verbundsuche

Führen Sie die folgenden Schritte aus, um eine Verbundsuche zu erstellen:

1.  Ermöglichen Sie das Durchsuchen Ihres Datenspeichers über Windows-Explorer, indem Sie einen [OpenSearch-kompatiblen](https://github.com/dewitt/opensearch)Webdienst bereitstellen, der Ergebnisse im RSS- oder Atom-Format zurückgeben kann.
2.  Erstellen Sie eine OpenSearch-Beschreibungsdatei (OSDX), in der beschrieben wird, wie Sie eine Verbindung mit dem Webdienst herstellen und benutzerdefinierte Elemente in RSS oder Atom XML zuordnen.
3.  Stellen Sie die Suchconnectors mit einer OSDX-Datei auf Windows-Clientcomputern zur Verfügung.

Das folgende Diagramm veranschaulicht die Schritte zum Erstellen der Verbundsuche.

![Diagramm des Prozesses zum Erstellen einer Verbundsuche](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a>Funktionsweise der Verbundsuche

Die Kommunikation zwischen Windows-Explorer und Ihrem [OpenSearch-Webdienst](https://github.com/dewitt/opensearch) erfolgt über die Windows-Datenebene. Die Windows-Datenschicht kann über Windows Store-Anbieter mit verschiedenen Arten von Datenspeichern kommunizieren. Jeder Anbieter ist auf die Kommunikation mit Datenspeichern spezialisiert, die ein bestimmtes Protokoll unterstützen und über bestimmte Funktionen verfügen. Die folgende Abbildung zeigt beispielsweise, wie der [OpenSearch-Anbieter](https://github.com/dewitt/opensearch) mit Datenspeichern kommuniziert, die einen Webdienst bereitstellen, der [den OpenSearch-Standard](https://github.com/dewitt/opensearch) unterstützt.

![Diagramm, das die Kommunikation vom Windows-Explorer auf dem Client über den Opensearch-Datenspeicher auf dem Remoteserver zeigt](images/windowssearchfederationfunctionality.png)

Damit Ihr Datenspeicher die Verbundsuche in Windows 7 unterstützen kann, müssen Sie eine Reihe von Aufgaben ausführen. In der folgenden Tabelle sind die Aufgaben zum Aktivieren Ihres Datenspeichers, die erforderlichen Aufgaben und der Ort der Dokumentation aufgeführt.



| Aufgabe                                                                                                     | Anforderung                                                                                                                                                                                            | Dokumentation                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aktivieren Sie die Suche nach Ihrem Datenspeicher durch Windows-Explorer.<br/>                                    | Erstellen Sie einen OpenSearch-kompatiblen Webdienst.<br/> Erstellen Sie eine OpenSearch-Beschreibungsdatei (.osdx).<br/>                                                                                       | [Verbinden Ihres Webdiensts in der Windows-Verbundsuche](-search-federated-search-web-service.md)<br/> [Aktivieren des Datenspeichers in der Windows-Verbundsuche](-search-federated-search-data-store.md)<br/> |
| Stellen Sie Ihren Webdienst aktiv für Benutzer in einem Unternehmen zur Verfügung.<br/>                               | Stellen Sie Ihren Benutzern eine OSDX-Datei zur Verfügung, kopieren Sie sie lokal, und machen Sie sie über eine Verknüpfung für den Benutzer zugänglich.<br/>                                                                                     | [Bereitstellen von Suchconnectors in der Windows-Verbundsuche](-search-federated-search-deploying.md)<br/>                                                                                                              |
| Aufzählen von Suchergebnissen in Windows-Explorer als Antwort auf eine Abfrage.<br/>                          | Implementieren Sie einen Webdienst, der eine Abfragezeichenfolge akzeptiert und Ergebnisse im RSS- oder Atom-Format zurückgibt.<br/>                                                                                              | [Verbinden Ihres Webdiensts in der Windows-Verbundsuche](-search-federated-search-web-service.md)<br/>                                                                                                            |
| Ermöglichen Sie es Benutzern, Ihren Datenspeicher zu ihren Windows-Explorer.<br/>                                | Erstellen Sie eine OSDX-Datei, und stellen Sie sie Ihren Benutzern zur Verfügung.<br/>                                                                                                                                           | [Aktivieren des Datenspeichers in der Windows-Verbundsuche](-search-federated-search-data-store.md)<br/>                                                                                                                |
| Zeigen Sie Ihre Elemente als dateispezifische Elemente in Windows-Explorer.<br/>                                    | Zurückgeben einer URL zur Datei oder zum Inhaltsstream mithilfe von **Gehäuse-** oder **media:content-Elementen**<br/> Geben Sie eine Dateierweiterung oder einen MIME-Typ an, den der Clientcomputer erkennt.<br/> | [Aktivieren des Datenspeichers in der Windows-Verbundsuche](-search-federated-search-data-store.md)<br/>                                                                                                                |
| Zeigen Sie benutzerdefinierte Eigenschaften in Windows-Explorer, die über die in RSS- oder Atom-Standards definierten hinausgehen.<br/> | Geben Sie zusätzliche Metadaten an, indem Sie einen anderen XML-Namespace in Ihrer RSS/Atom-Ausgabe verwenden.<br/> Fügen Sie Ihrer OSDX-Datei eine Eigenschaftenzuordnung hinzu.<br/>                                                       | [Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbundsuche](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Passen Sie die Eigenschaften an, die für Ihre Elemente in der Windows-Explorer.<br/>               | Fügen Sie Ihrer OSDX-Datei Proplist-Zuordnungen hinzu.<br/>                                                                                                                                                   | [Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbundsuche](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Zeigen Sie eine benutzerdefinierte Webseitenansicht Ihrer Elemente im Vorschaubereich an.<br/>                              | Gibt eindeutige Link- und Gehäusewerte zurück.<br/> Ordnen Sie der Windows Shell-Eigenschaft **System.WebPreviewUrl** einen URL-Wert zu.<br/>                                                               | [Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbundsuche](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Zeigen Sie eine Befehlsleistenschaltfläche in Windows-Explorer, die die Abfrage auf Ihre Website überrollt.<br/>   | Geben Sie `Url format="text/html"` eine Vorlage in der OSDX-Datei an.<br/>                                                                                                                              | [Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbundsuche](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Senden von Abfragen und Zurückgeben von Suchergebnissen in RSS oder Atom

Wenn der Benutzer einen Begriff in das Suchfeld in der oberen rechten Ecke von Windows-Explorer ein gibt, wird die Abfrage an den [OpenSearch-Anbieter](https://github.com/dewitt/opensearch) gesendet, der die Abfrage dann an den Remotedatenspeicher sendet. Der Remotewebdienst antwortet auf die Abfrage, indem er Ergebnisse in einem XML-Dokument, das in der Regel als Feed bezeichnet wird, in einem von zwei unterstützten Formaten (RSS oder Atom) liefert. Jedes Ergebniselement im Feed enthält untergeordnete XML-Elemente, die Elementmetadaten darstellen oder beschreiben, z. B. Titel, URL, Beschreibung, Miniaturansicht usw. Der [OpenSearch-Anbieter](https://github.com/dewitt/opensearch) ist für die Zuordnung der XML-Elementwerte zu Windows Shell-Systemeigenschaften verantwortlich, die von Windows-Anwendungen verwendet werden können.

## <a name="federated-search-examples"></a>Beispiele für die Verbundsuche

Die folgende OpenSearch Description(.osdx)-Beispieldatei besteht aus - und -Elementen, die die mindestens erforderlichen untergeordneten Elemente zum Verbinden eines externen Datenspeichers mit dem Windows-Client über das `ShortName` `Url` OpenSearch-Protokoll sind.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



Im folgenden Beispiel wird veranschaulicht, wie sie einen webfähigen Datenspeicher im RSS-Format durchsuchbar machen und angeben, dass ein Suchelement zurückgegeben wird:


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



Das folgende Beispiel veranschaulicht das Zuordnen von Eigenschaften zu Standardsystemeigenschaften, sodass angezeigte Elemente sortiert und gruppiert werden:


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



Im folgenden Beispiel wird veranschaulicht, wie jedem Element in der Datei eine Miniaturbildanzeige Windows-Explorer:


```
<media:thumbnail>    
```



## <a name="additional-resources"></a>Weitere Ressourcen

Weitere Informationen zum Implementieren des Suchverbunds in Remotedatenspeicher mit opensearch-Technologien in Windows 7 und höher finden Sie unter "Zusätzliche Ressourcen" unter [Verbundsuche in Windows.](-search-federated-search-overview.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbundsuche in Windows 10](-search-federated-search-overview.md)
</dt> <dt>

[Verbinden Ihres Webdiensts in der Windows-Verbundsuche](-search-federated-search-web-service.md)
</dt> <dt>

[Aktivieren des Datenspeichers in der Windows-Verbundsuche](-search-federated-search-data-store.md)
</dt> <dt>

[Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbundsuche](-search-federated-search-osdx-file.md)
</dt> <dt>

[Bewährte Methoden bei der Windows-Verbundsuche](-search-fedsearch-best.md)
</dt> <dt>

[Bereitstellen von Suchconnectors in der Windows-Verbundsuche](-search-federated-search-deploying.md)
</dt> </dl>

 

 




