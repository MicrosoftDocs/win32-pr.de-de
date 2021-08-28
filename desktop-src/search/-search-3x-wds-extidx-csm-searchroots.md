---
description: Mit Durchforstungsbereich-Manager (CSM) können Sie Suchsyntchen für Ihre Datenspeicher dem Suchdurchforstungsbereich hinzufügen Windows entfernen.
ms.assetid: 0f1ff41f-7c4c-4516-bb55-bf09a8f2f3bc
title: Verwalten von Suchsynten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cbe5fe6184681e6c37cb0b6a7f9a35c677fec53
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880196"
---
# <a name="managing-search-roots"></a>Verwalten von Suchsynten

Mit Durchforstungsbereich-Manager (CSM) können Sie Suchsyntchen für Ihre Datenspeicher dem Suchdurchforstungsbereich hinzufügen Windows entfernen.

Dieses Thema enthält die folgenden Themen:

-   [Informationen zu Search-Stämmen](#about-search-roots)
-   [Vorbereitungen](#before-you-begin)
-   [Windows 7: Neue Durchforstungsbereich-Manager-API](#windows-7-new-crawl-scope-manager-api)
-   [Hinzufügen von Stämmen zum Durchforstungsbereich](#adding-roots-to-the-crawl-scope)
-   [Entfernen von Stämmen aus dem Durchforstungsbereich](#removing-roots-from-the-crawl-scope)
-   [Aufzählen von Stämmen im Durchforstungsbereich](#enumerating-roots-in-the-crawl-scope)
-   [Zugehörige Themen](#related-topics)

 

## <a name="about-search-roots"></a>Informationen zu Search-Stämmen

Ein Suchstamm definiert die Basis eines Shellnamespace, in dem bestimmte Bereiche eingeschlossen oder ausgeschlossen werden können, und ist in der Regel der Container der höchsten Ebene in einem Protokoll, das aufzählt werden kann. Es wird nicht angegeben, welche Teile dieses Speichers indiziert werden sollen oder nicht. es signalisiert lediglich, dass ein Inhaltsspeicher vorhanden ist und einem registrierten Protokollhandler zugeordnet ist. Die Syntax zum Identifizieren einer Suchstamm-URL umfasst das Protokoll, die Sicherheits-ID des Speichers oder Benutzers, den Pfad und optional ein bestimmtes Element (z. B. eine Datei). Die folgenden Beispiele zeigen zwei Formen der Syntax für einen Suchstamm.


```
<protocol>://<store or SID>\<path>\[item]
or
<protocol>://<store or SID>/<path>/[item]
```



Auf das Protokollsegment müssen zwei (2) Schrägstriche &lt; ('/') folgen, es sei denn, es handelt sich um die Datei protocol, die drei Schrägstriche &gt; (file:///) erfordert. Das <site or SID> Segment stellt entweder einen Inhaltsspeicher oder eine Benutzersicherheits-ID dar, wenn der Suchstamm für den Benutzer spezifisch sein soll. Das Pfadsegment ist ein Satz von Containern, z. B. Verzeichnisse oder Ordner, und kann das &lt; &gt; Platzhalterzeichen ' \* ' enthalten. Das &lt; &gt; Elementsegment ist optional und kann auch das Platzhalterzeichen ' \* ' enthalten. Wenn Sie kein Element enthalten, stellen Sie sicher, dass Sie ihr Pfadsegment mit einem Schrägstrich beenden, da der Indexer andernt, dass der letzte Untercontainer ein Element ist.

Angenommen, Sie haben einen Protokollhandler (myPH) implementiert, um Dateien vom Typ \* .myext für eine benutzerdefinierte Anwendung zu verarbeiten. Alle diese Dateien befinden sich im Ordner WorkteamA \\ ProjectFiles auf einem lokalen Computer. Das Suchstammverzeichnis für könnte wie im folgenden Beispiel aussehen:

-   myPH:///C: \\ WorkteamA \\ ProjectFiles\\

Angenommen, Sie planen, alle MYEXT-Dateien, aber nichts anderes aus diesem Container in den Index einbinden. Das Suchstammverzeichnis für könnte wie im folgenden Beispiel aussehen:

-   myPH:///C: \\ WorkteamA \\ ProjectFiles \\ \* .myext.

Platzhaltermuster definieren URLs mithilfe des Platzhalterzeichens " " und werden als Muster und nicht als URL betrachtet, aber die Terminologie wird häufig \* synonym verwendet. Beispiel: file:///C: \\ \\ \* \\ ProjectA-Daten \\ würden mit den folgenden URLs übereinstimmen:

-   C: \\ ProjectA \\ **version1-Daten** \\\\
-   C: \\ ProjectA \\ **version2-Daten** \\\\

Dieses Muster würde jedoch nicht mit dieser URL übereinstimmen:

-   C: \\ Temporäre Daten zu ProjectA \\ **Version1 \\** \\\\

Sie sollten neue Suchsyntchen für Container erstellen, die sich noch nicht im Durchforstungsbereich des Indexers befinden. Wenn Pfad C: ParentScope bereits im Durchforstungsbereich enthalten ist, müssen Sie keinen neuen Suchstamm für \\ C: ParentScope ChildScope hinzufügen, es sei denn, Sie wissen, dass der untergeordnete Bereich zuvor ausgeschlossen \\ \\ wurde.

Auf der Benutzeroberfläche zum Festlegen Windows Suchoptionen werden Den Benutzern Suchsynten angezeigt, damit sie die Bereichsregeln für ihre Suchvorgänge verfeinern können. Im Rahmen des Installationsprozesses für Ihren benutzerdefinierten Protokollhandler, Container und/oder Ihre Anwendung können Sie einen Standard-Durchforstungsbereich mit Ein- und Ausschlussregeln definieren. Diese Regeln werden Endbenutzern als Standorte präsentiert. Benutzer können in den Unterverzeichnissen Ihres vordefinierten Suchstamms navigieren und diejenigen auswählen, die sie in Suchvorgängen einschließt, oder diejenigen löschen, die sie ausschließen möchten.

 

## <a name="before-you-begin"></a>Vorbereitungen

Bevor Sie eine der CSM-Schnittstellen (Durchforstungsbereich-Manager) verwenden können, müssen Sie die folgenden erforderlichen Schritte ausführen:

1.  Erstellen Sie das **CrawlSearchManager-Objekt,** und erhalten Sie dessen [**ISearchManager-Schnittstelle.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)
2.  Rufen [**Sie ISearchManager::GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) für "SystemIndex" auf, um eine Instanz einer [**ISearchCatalogManager-Schnittstelle abzurufen.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)
3.  Rufen [**Sie ISearchCatalogManager::GetCrawlScopeManager auf,**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager) um eine Instanz der [**ISearchCrawlScopeManager-Schnittstelle abzurufen.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)

Nachdem Sie Änderungen am Durchforstungsbereich-Manager (CSM) vorgenommen haben, müssen Sie [**ISearchCrawlScopeManager::SaveAll aufrufen.**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall) Diese Methode nimmt keine Parameter an und gibt bei Erfolg S \_ OK zurück.

 

## <a name="windows-7-new-crawl-scope-manager-api"></a>Windows 7: Neue Durchforstungsbereich-Manager-API

In **Windows 7 und höher** erweitert [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) die Funktionalität der [**ISearchCrawlScopeManager-Schnittstelle.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) Die [**ISearchCrawlScopeManager2::GetVersion-Methode**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) ruft die version Durchforstungsbereich-Manager (CSM) ab, die Clients informiert, wenn sich der Status des CSM geändert hat. **ISearchCrawlScopeManager2::GetVersion** führt nicht zu einem prozessübergreifenden Aufruf. Wenn die Funktion erfolgreich ausgeführt wird, bleibt der zurückgegebene Zeiger gültig, bis der Client **UnmapViewOfFile** für den Zeiger und **CloseHandle** für das zurückgegebene Handle aufruft.

 

## <a name="adding-roots-to-the-crawl-scope"></a>Hinzufügen von Stämmen zum Durchforstungsbereich

Der [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) informiert die Suchmaschine über Container, die durchforscht und/oder beobachtet werden sollen, sowie Elemente unter diesen Containern, die ein- oder ausgeschlossen werden sollen. Instanziieren Sie zum Hinzufügen eines neuen Suchstamms ein [**ISearchRoot-Objekt,**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) legen Sie die Stammattribute fest, rufen Sie [**dann ISearchCrawlScopeManager::AddRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-addroot) auf, und übergeben Sie ihm einen Zeiger auf Ihr **ISearchRoot-Objekt.** Die Suchstamm-URL hat das gleiche Formular wie der zuvor beschriebene Suchstamm.

In der folgenden Tabelle werden die relevanten put-Methoden für [**ISearchRoot beschrieben.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) Die anderen Put-Methoden der Schnittstelle werden derzeit nicht von der Windows verwendet. Es wird empfohlen, die Sicherheits-IDs (SIDs) der Benutzer in allen Stämmen zu verwenden, um die Sicherheit zu verbessern. Benutzerspezifische Stämme sind sicherer, da Abfragen in einem benutzerspezifischen Prozess ausgeführt werden. So wird beispielsweise sichergestellt, dass ein Benutzer keine Elemente sehen kann, die aus dem Posteingang eines anderen Benutzers indiziert wurden.



| Methode                     | Beschreibung                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| put \_ ProvidesNotifications | Legen Sie **auf TRUE** fest, wenn ein Protokollhandler oder eine andere Anwendung die Suchmaschine über Änderungen an den URLs unter dem Suchstamm benachrichtigt. Die Benachrichtigung gibt an, dass die URLs neu indiziert werden müssen. |
| put \_ RootURL               | Legt die Stamm-URL der aktuellen Suche fest. Die URL hat das zuvor beschriebene Suchstammformular.                                                                                                      |



 

 

Standardmäßig durchforstungt der Indexer beim Hinzufügen eines Suchstamms keinen Bereich. Sie müssen auch eine Includeregel für den Stamm hinzufügen. Wenn Sie einen benutzerspezifischen Stamm für eine Anwendung hinzufügen möchten, sollte diese Anwendung beim Starten der Anwendung die entsprechenden Stämme für neue Benutzer hinzufügen.

So fügen Sie die entsprechenden Stämme für neue Benutzer hinzu:

1.  Hier erhalten Sie die SID des Benutzers.
2.  Enumerieren Sie alle Stämme, um zu überprüfen, ob eine für diese SID vorhanden ist.
3.  Fügen Sie bei Bedarf mithilfe der SID einen neuen Stamm hinzu.

 

## <a name="removing-roots-from-the-crawl-scope"></a>Entfernen von Stämmen aus dem Durchforstungsbereich

Sie können [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) verwenden, um einen Stamm aus dem Durchforstungsbereich zu entfernen, wenn diese URL nicht mehr indiziert werden soll. Durch das Entfernen eines Stamms werden auch alle Bereichsregeln für diese URL gelöscht. Angenommen, Sie möchten einen Inhaltsspeicher und/oder dessen Protokollhandler aus einem System deinstallieren. Sie können die Anwendung deinstallieren, alle Daten entfernen und dann den Suchstamm aus dem Durchforstungsbereich entfernen, und die Durchforstungsbereich-Manager entfernt die Stamm- und alle Bereichsregeln, die dem Stamm zugeordnet sind.

Um einen vorhandenen Suchstamm zu entfernen, rufen [**Sie ISearchCrawlScopeManager::RemoveRoot mit**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) dem Suchstamm auf, den Sie entfernen möchten. Die Suchstamm-URL hat das gleiche Formular wie der zuvor beschriebene Suchstamm. Diese Methode gibt S FALSE zurück, wenn der Stamm nicht gefunden wird, und einen Fehlercode, wenn beim Entfernen eines gefundenen Stamms ein \_ Fehler aufgetreten ist.

Durch das Entfernen eines Suchstamms wird auch die URL von der Benutzeroberfläche für Windows Search-Optionen entfernt, sodass Benutzer diesen Container oder Speicherort möglicherweise nicht über die Benutzeroberfläche erneut hinzufügen können. Es ist auch möglich, alle benutzerspezifischen Außerkraftsetzungen eines Suchstamms zu entfernen und auf die ursprünglichen Stamm- und Bereichsregeln der Suche zurück zu setzen. Weitere Informationen finden Sie unter [Verwalten von Bereichsregeln.](-search-3x-wds-extidx-csm-scoperules.md)

> [!Note]  
> Wenn Windows Vista Benutzer über Benutzerprofile in Systemsteuerung entfernt werden, entfernt CSM alle Regeln und Stämme mit ihrer SID und entfernt ihre indizierten Elemente aus dem Katalog. Auf Windows XP müssen Sie die Stämme und Regeln der Benutzer manuell entfernen.

 

 

## <a name="enumerating-roots-in-the-crawl-scope"></a>Aufzählen von Stämmen im Durchforstungsbereich

Der CSM enumeriert Suchsynten mithilfe einer Enumeratorschnittstelle im COM-Stil, [**IEnumSearchRoots.**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots) Sie können diese Schnittstelle verwenden, um Suchsynten für eine Reihe von Zwecken zu aufzählen. Beispielsweise können Sie den gesamten Durchforstungsbereich in einer Benutzeroberfläche anzeigen oder feststellen, ob sich ein bestimmter Stamm oder das untergeordnete Teil eines Stamms bereits im Durchforstungsbereich befindet.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
</dt> <dt>

[**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Verwenden des Durchforstungsbereich-Manager](-search-3x-wds-extidx-csm.md)
</dt> <dt>

[Verwalten von Bereichsregeln](-search-3x-wds-extidx-csm-scoperules.md)
</dt> </dl>

 

 



