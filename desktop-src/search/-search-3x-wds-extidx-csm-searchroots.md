---
description: Mit dem Durchforstungsbereich-Manager (CSM) können Sie Suchstämmen für Ihre Datenspeicher dem Windows Durchforstungsbereich hinzufügen und daraus entfernen.
ms.assetid: 0f1ff41f-7c4c-4516-bb55-bf09a8f2f3bc
title: Verwalten von Suchstammstamm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758d3c10a4c69f336202274cd1fb40528848b0ddb431fd58646cf700d2b2d736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119095287"
---
# <a name="managing-search-roots"></a>Verwalten von Suchstammstamm

Mit dem Durchforstungsbereich-Manager (CSM) können Sie Suchstämmen für Ihre Datenspeicher dem Windows Durchforstungsbereich hinzufügen und daraus entfernen.

Dieses Thema enthält die folgenden Themen:

-   [Informationen zu Suchstammstamm](#about-search-roots)
-   [Vorbereitungen](#before-you-begin)
-   [Windows 7: Neue Durchforstungsbereich-Manager-API](#windows-7-new-crawl-scope-manager-api)
-   [Hinzufügen von Stämmen zum Durchforstungsbereich](#adding-roots-to-the-crawl-scope)
-   [Entfernen von Stämmen aus dem Durchforstungsbereich](#removing-roots-from-the-crawl-scope)
-   [Aufzählen von Stämmen im Durchforstungsbereich](#enumerating-roots-in-the-crawl-scope)
-   [Zugehörige Themen](#related-topics)

 

## <a name="about-search-roots"></a>Informationen zu Suchstammstamm

Ein Suchstamm definiert die Basis eines Shellnamespace, in dem bestimmte Bereiche eingeschlossen oder ausgeschlossen werden können, und ist in der Regel der Container der höchsten Ebene in einem Protokoll, das aufgezählt werden kann. Es wird nicht angegeben, welche Teile dieses Speichers indiziert werden sollen oder nicht. sie signalisiert lediglich, dass ein Inhaltsspeicher vorhanden ist und einem registrierten Protokollhandler zugeordnet ist. Die Syntax zum Identifizieren einer Suchstamm-URL umfasst das Protokoll, den Sicherheitsbezeichner des Speichers oder Benutzers, den Pfad und optional ein bestimmtes Element (z. B. eine Datei). Die folgenden Beispiele zeigen zwei Formen der Syntax für einen Suchstamm.


```
<protocol>://<store or SID>\<path>\[item]
or
<protocol>://<store or SID>/<path>/[item]
```



Auf das <protocol> Segment müssen zwei (2) Schrägstriche ("/") folgen, es sei denn, es handelt sich um die Datei "protocol", für die drei Schrägstriche (file:///) erforderlich sind. Das <site or SID> Segment stellt entweder einen Inhaltsspeicher oder eine Benutzersicherheits-ID dar, wenn der Suchstamm spezifisch für den Benutzer sein soll. Das <path> Segment besteht aus einer Gruppe von Containern, z. B. Verzeichnissen oder Ordnern, und kann das Platzhalterzeichen ' ' ' \* enthalten. Die <item> segment ist optional und kann auch das Platzhalterzeichen \* "" enthalten. Wenn Sie kein Element einschließen, stellen Sie sicher, dass Sie das Pfadsegment mit einem Schrägstrich fertig stellen, oder der Indexer geht davon aus, dass der letzte Untercontainer ein Element ist.

Angenommen, Sie haben einen Protokollhandler (myPH) implementiert, um Dateien vom Typ \* .myext für eine benutzerdefinierte Anwendung zu verarbeiten. Alle diese Dateien befinden sich im Ordner WorkteamA \\ ProjectFiles auf einem lokalen Computer. Der Suchstamm für könnte wie folgt aussehen:

-   myPH:///C: \\ WorkteamA \\ ProjectFiles\\

Angenommen, Sie planen, alle MYEXT-Dateien, aber nichts anderes aus diesem Container in den Index aufzunehmen. Der Suchstamm für könnte wie folgt aussehen:

-   myPH:///C: \\ WorkteamA \\ ProjectFiles \\ \* .myext.

Platzhaltermuster definieren URLs mithilfe des Platzhalterzeichens " \* " und werden als Muster und nicht als URL betrachtet, aber die Terminologie wird häufig synonym verwendet. Beispiel: file:///C: \\ \\ \* \\ \\ ProjectA-Daten entsprechen den folgenden URLs:

-   C: \\ ProjectA \\ **version1-Daten** \\\\
-   C: \\ ProjectA \\ **version2-Daten** \\\\

Dieses Muster würde jedoch nicht mit dieser URL übereinstimmen:

-   C: \\ Temporäre Daten von ProjectA \\ **version1 \\** \\\\

Sie sollten neue Suchstämmen für Container erstellen, die sich nicht bereits im Durchforstungsbereich des Indexers befinden. Wenn pfad C: \\ ParentScope bereits im Durchforstungsbereich enthalten ist, müssen Sie keinen neuen Suchstamm für C: ParentScope ChildScope hinzufügen, \\ es sei \\ denn, Sie wissen, dass der untergeordnete Bereich zuvor ausgeschlossen wurde.

Die Benutzeroberfläche zum Festlegen Windows Suchoptionen zeigt Benutzern Suchstamminformationen an, damit sie die Bereichsregeln für ihre Suchvorgänge verfeinern können. Im Rahmen des Installationsvorgangs für Ihren benutzerdefinierten Protokollhandler, Container und/oder Ihre Anwendung können Sie einen Standard-Durchforstungsbereich mit Ein- und Ausschlussregeln definieren. Diese Regeln werden Endbenutzern als Speicherorte angezeigt. Benutzer können innerhalb der Unterverzeichnisse Ihres vordefinierten Suchstamms navigieren und diejenigen auswählen, die sie in Suchvorgänge einschließen möchten, oder diejenigen löschen, die sie ausschließen möchten.

 

## <a name="before-you-begin"></a>Vorbereitungen

Bevor Sie eine der csm-Schnittstellen (Durchforstungsbereich-Manager) verwenden können, müssen Sie die folgenden erforderlichen Schritte ausführen:

1.  Erstellen Sie das **CrawlSearchManager-Objekt,** und rufen Sie dessen [**ISearchManager-Schnittstelle**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) ab.
2.  Rufen Sie [**ISearchManager::GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) für "SystemIndex" auf, um eine Instanz einer [**ISearchCatalogManager-Schnittstelle**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) abzurufen.
3.  Rufen Sie [**ISearchCatalogManager::GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager) auf, um eine Instanz der [**ISearchCrawlScopeManager-Schnittstelle**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) abzurufen.

Nachdem Sie Änderungen am Durchforstungsbereich-Manager (CSM) vorgenommen haben, müssen Sie [**ISearchCrawlScopeManager::SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall)aufrufen. Diese Methode verwendet keine Parameter und gibt bei Erfolg S \_ OK zurück.

 

## <a name="windows-7-new-crawl-scope-manager-api"></a>Windows 7: Neue Durchforstungsbereich-Manager-API

In **Windows 7 und höher** erweitert [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) die Funktionalität der [**ISearchCrawlScopeManager-Schnittstelle.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) Die [**ISearchCrawlScopeManager2::GetVersion-Methode**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) ruft die csm-Version (Durchforstungsbereich-Manager) ab, die Clients informiert, wenn sich der Zustand des CSM geändert hat. **ISearchCrawlScopeManager2::GetVersion** führt nicht zu einem prozessübergreifenden Aufruf. Wenn die Funktion erfolgreich ausgeführt wird, bleibt der zurückgegebene Zeiger gültig, bis der Client **UnmapViewOfFile** für den Zeiger und **CloseHandle** für das zurückgegebene Handle aufruft.

 

## <a name="adding-roots-to-the-crawl-scope"></a>Hinzufügen von Stämmen zum Durchforstungsbereich

Der [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) informiert die Suchmaschine über Container, die durchforstet und/oder überwacht werden sollen, und elemente unter diesen Containern, die eingeschlossen oder ausgeschlossen werden sollen. Um einen neuen Suchstamm hinzuzufügen, instanziieren Sie ein [**ISearchRoot-Objekt,**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) legen Sie die Stammattribute fest, und rufen Sie dann [**ISearchCrawlScopeManager::AddRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-addroot) auf, und übergeben Sie ihm einen Zeiger auf Ihr **ISearchRoot-Objekt.** Die Url des Suchstamms hat das gleiche Format wie der zuvor beschriebene Suchstamm.

In der folgenden Tabelle werden die relevanten Put-Methoden für [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)beschrieben. Die anderen Put-Methoden der Schnittstelle werden derzeit nicht von Windows Search verwendet. Es wird empfohlen, die Sicherheits-IDs (SIDs) der Benutzer in alle Stammgruppen zu einschließen, um die Sicherheit zu verbessern. Stammelemente pro Benutzer sind sicherer, da Abfragen in einem Pro-Benutzer-Prozess ausgeführt werden. Dadurch wird sichergestellt, dass einem Benutzer beispielsweise keine Elemente angezeigt werden, die aus dem Posteingang eines anderen Benutzers indiziert wurden.



| Methode                     | BESCHREIBUNG                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| put \_ ProvidesNotifications | Legen Sie diese Einstellung auf **TRUE** fest, wenn ein Protokollhandler oder eine andere Anwendung die Suchmaschine über Änderungen an den URLs unter dem Suchstamm benachrichtigt. Die Benachrichtigung gibt an, dass die URLs neu indiziert werden müssen. |
| \_put RootURL               | Legt die Stamm-URL der aktuellen Suche fest. Die URL nimmt das zuvor beschriebene Suchstammformular an.                                                                                                      |



 

 

Standardmäßig durchforstet der Indexer beim Hinzufügen eines Suchstamms keinen Bereich. Sie müssen auch eine Includeregel für den Stamm hinzufügen. Wenn Sie einen benutzerspezifischen Stamm für eine Anwendung hinzufügen möchten, sollte diese Anwendung beim Starten der Anwendung die entsprechenden Stammverzeichnis für neue Benutzer hinzufügen.

So fügen Sie die entsprechenden Stamms für neue Benutzer hinzu:

1.  Abrufen der SID des Benutzers.
2.  Aufzählen aller Stämme, um zu überprüfen, ob für diese SID ein Stamm vorhanden ist.
3.  Fügen Sie bei Bedarf mithilfe der SID einen neuen Stamm hinzu.

 

## <a name="removing-roots-from-the-crawl-scope"></a>Entfernen von Stämmen aus dem Durchforstungsbereich

Sie können [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) verwenden, um einen Stamm aus dem Durchforstungsbereich zu entfernen, wenn diese URL nicht mehr indiziert werden soll. Beim Entfernen eines Stamms werden auch alle Bereichsregeln für diese URL gelöscht. Angenommen, Sie möchten einen Inhaltsspeicher und/oder dessen Protokollhandler von einem System deinstallieren. Sie können die Anwendung deinstallieren, alle Daten entfernen und dann den Suchstamm aus dem Durchforstungsbereich entfernen. Die Durchforstungsbereich-Manager entfernt den Stamm und alle Bereichsregeln, die dem Stamm zugeordnet sind.

Um einen vorhandenen Suchstamm zu entfernen, rufen Sie [**ISearchCrawlScopeManager::RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) mit dem Suchstamm auf, den Sie entfernen möchten. Die Url des Suchstamms hat das gleiche Format wie der zuvor beschriebene Suchstamm. Diese Methode gibt S \_ FALSE zurück, wenn der Stamm nicht gefunden wurde, und einen Fehlercode, wenn beim Entfernen eines gefundenen Stamms ein Fehler aufgetreten ist.

Durch das Entfernen eines Suchstamms wird auch die URL für Windows Suchoptionen aus der Benutzeroberfläche entfernt, sodass Benutzer diesen Container oder Speicherort möglicherweise nicht über die Benutzeroberfläche erneut hinzufügen können. Es ist auch möglich, alle Außerkraftsetzungen von Benutzersets eines Suchstamms zu entfernen und auf die ursprünglichen Suchstamm- und Gültigkeitsbereichsregeln zurückzusetzen. Weitere Informationen finden Sie unter [Verwalten von Bereichsregeln.](-search-3x-wds-extidx-csm-scoperules.md)

> [!Note]  
> Wenn Benutzer auf Windows Vista über Benutzerprofile in Systemsteuerung entfernt werden, entfernt CSM alle Regeln und Stammelemente mit ihrer SID und entfernt ihre indizierten Elemente aus dem Katalog. Auf Windows XP müssen Sie die Stamm- und Regeln der Benutzer manuell entfernen.

 

 

## <a name="enumerating-roots-in-the-crawl-scope"></a>Aufzählen von Stämmen im Durchforstungsbereich

Der CSM listet Suchstammstamm mithilfe einer standardmäßigen Enumeratorschnittstelle im COM-Stil [**IEnumSearchRoots auf.**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots) Sie können diese Schnittstelle verwenden, um Suchstämme für eine Reihe von Zwecken aufzulisten. Beispielsweise können Sie den gesamten Durchforstungsbereich auf einer Benutzeroberfläche anzeigen oder ermitteln, ob sich ein bestimmter Stamm oder das untergeordnete Element eines Stamms bereits im Durchforstungsbereich befindet.

 

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

[Verwenden der Durchforstungsbereich-Manager](-search-3x-wds-extidx-csm.md)
</dt> <dt>

[Verwalten von Bereichsregeln](-search-3x-wds-extidx-csm-scoperules.md)
</dt> </dl>

 

 



