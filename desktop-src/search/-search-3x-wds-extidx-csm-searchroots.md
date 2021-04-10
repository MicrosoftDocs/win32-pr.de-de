---
description: Mit dem Crawl Scope Manager (CSM) können Sie Such Stämme für Ihre Datenspeicher zu und aus dem Windows Search-Crawl Bereich hinzufügen und daraus entfernen.
ms.assetid: 0f1ff41f-7c4c-4516-bb55-bf09a8f2f3bc
title: Verwalten von Such Stämmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbdd63e5e71cd18d3028c6d08019890f90c0228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214467"
---
# <a name="managing-search-roots"></a>Verwalten von Such Stämmen

Mit dem Crawl Scope Manager (CSM) können Sie Such Stämme für Ihre Datenspeicher zu und aus dem Windows Search-Crawl Bereich hinzufügen und daraus entfernen.

Dieses Thema enthält die folgenden Themen:

-   [Informationen zu Such Stämmen](#about-search-roots)
-   [Vorbereitungen](#before-you-begin)
-   [Windows 7: neue Crawl Scope Manager-API](#windows-7-new-crawl-scope-manager-api)
-   [Hinzufügen von Stämmen zum Crawl Bereich](#adding-roots-to-the-crawl-scope)
-   [Entfernen von Stämmen aus dem Crawl Bereich](#removing-roots-from-the-crawl-scope)
-   [Enumerieren von Stämme im Crawl Bereich](#enumerating-roots-in-the-crawl-scope)
-   [Zugehörige Themen](#related-topics)

 

## <a name="about-search-roots"></a>Informationen zu Such Stämmen

Ein Such Stamm definiert die Basis eines shellnamespaces, in dem bestimmte Bereiche eingeschlossen oder ausgeschlossen werden können, und ist in der Regel der auf der höchsten Ebene enthaltene Container in einem Protokoll, das aufgelistet werden kann. Sie gibt nicht an, welche Teile dieses Stores indiziert werden sollen oder nicht. Es signalisiert lediglich, dass ein Inhalts Speicher vorhanden ist und einem registrierten Protokollhandler zugeordnet ist. Die Syntax zum Identifizieren einer Such Stamm-URL umfasst das Protokoll, die Sicherheits-ID des Stores oder Benutzers, den Pfad und optional ein bestimmtes Element (z. b. eine Datei). Die folgenden Beispiele zeigen zwei Formen der Syntax für einen Suchstamm.


```
<protocol>://<store or SID>\<path>\[item]
or
<protocol>://<store or SID>/<path>/[item]
```



<protocol>Auf das Segment müssen zwei (2) Schrägstriche ("/") folgen, es sei denn, es handelt sich um das file: Protocol-Protokoll, das drei Schrägstriche (file:///) erfordert. Das <site or SID> Segment stellt entweder einen Inhalts Speicher oder eine Benutzer Sicherheits-ID dar, wenn der Suchstamm für den Benutzer spezifisch ist. Das <path> Segment ist ein Satz von Containern, wie z. b. Verzeichnisse oder Ordner, und kann das Platzhalter Zeichen " \* " enthalten. Für <item> Segment ist optional und kann auch das Platzhalter Zeichen ' \* ' enthalten. Wenn Sie kein Element einschließen, stellen Sie sicher, dass Sie das Pfad Segment mit einem Schrägstrich beenden, oder der Indexer geht davon aus, dass der letzte unter Container ein Element ist.

Angenommen, Sie haben einen Protokollhandler (myph) implementiert, um Dateien des Typs " \* . myext" für eine benutzerdefinierte Anwendung zu verarbeiten. Alle diese Dateien befinden sich im Ordner workteama \\ ProjectFiles auf einem lokalen Computer. Der Suchstamm für könnte wie folgt aussehen:

-   myPH:///C: \\ workteama \\ ProjectFiles\\

Angenommen, Sie planen die Einbeziehung aller myext-Dateien, aber nichts anderes aus dem Container in den Index. Der Suchstamm für könnte wie folgt aussehen:

-   myPH:///C: \\ workteama \\ ProjectFiles \\ \* . myext.

Platzhalter Muster definieren URLs mithilfe des Platzhalter Zeichens " \* " und werden als Muster und nicht als URL angesehen, aber die Terminologie wird häufig austauschbar verwendet. Beispielsweise entsprechen file:///C: \\ ProjectA- \\ \* \\ Daten \\ den folgenden URLs:

-   C: \\ ProjectA \\ **Version1** \\ Daten\\
-   C: \\ ProjectA \\ **Version2** \\ Daten\\

Dieses Muster würde jedoch nicht mit dieser URL verglichen werden:

-   C: \\ ProjectA \\ **Version1 \\** temporäre \\ Daten\\

Sie sollten neue Such Stämme für Container erstellen, die sich nicht bereits im Crawl Bereich des Indexers befinden. Wenn Pfad C: Element \\ Bereich bereits im Crawl Bereich enthalten ist, müssen Sie kein neues Such Stammverzeichnis für C: Element \\ Scope childscope hinzufügen, \\ es sei denn, Sie wissen, dass der untergeordnete Bereich zuvor ausgeschlossen wurde.

Die Benutzeroberfläche zum Festlegen von Windows-Suchoptionen zeigt Such Stämme für Benutzer an, damit Sie die Bereichs Regeln für Ihre Suchvorgänge verfeinern können. Im Rahmen des Installationsvorgangs für Ihren benutzerdefinierten Protokollhandler, Container und/oder Ihre Anwendung können Sie einen Standard-Crawl Bereich mit Einschluss-und Ausschluss Regeln definieren. Diese Regeln werden Endbenutzern als Standorte angezeigt. Benutzer können in den Unterverzeichnissen Ihres vordefinierten Such Stamms navigieren und diejenigen auswählen, die Sie in Durchsuchen einschließen möchten, oder die auszuschließenden löschen.

 

## <a name="before-you-begin"></a>Vorbereitungen

Bevor Sie eine der CSM-Schnittstellen (Crawl Scope Manager) verwenden können, müssen Sie die folgenden Schritte ausführen:

1.  Erstellen Sie das **crawlsearchmanager** -Objekt, und rufen Sie dessen [**isearchmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) -Schnittstelle ab.
2.  Rufen Sie [**isearchmanager:: getCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) für "SystemIndex" auf, um eine Instanz einer [**isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) -Schnittstelle zu erhalten.
3.  Rufen Sie [**isearchcatalogmanager:: getcrawlscopemanager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager) auf, um eine Instanz der [**isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) -Schnittstelle zu erhalten.

Nachdem Sie die Änderungen am Crawl Scope Manager (CSM) vorgenommen haben, müssen Sie [**isearchcrawlscopemanager:: SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall)ausführen. Diese Methode nimmt keine Parameter an und gibt \_ bei Erfolg S OK zurück.

 

## <a name="windows-7-new-crawl-scope-manager-api"></a>Windows 7: neue Crawl Scope Manager-API

In **Windows 7 und** höher erweitert [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) die Funktionalität der [**isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) -Schnittstelle. Die [**ISearchCrawlScopeManager2:: GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) -Methode ruft die CSM-Version ab, mit der Clients informiert werden, wenn sich der Status des CSM geändert hat. **ISearchCrawlScopeManager2:: GetVersion** führt nicht zu einem prozessübergreifenden aufrufen. Wenn die Funktion erfolgreich ausgeführt wird, bleibt der zurückgegebene Zeiger gültig, bis der Client **UnmapViewOfFile** für den Zeiger und das **CloseHandle** für das zurückgegebene Handle aufruft.

 

## <a name="adding-roots-to-the-crawl-scope"></a>Hinzufügen von Stämmen zum Crawl Bereich

[**Isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) weist das Suchmodul an, die Container zu durchforsten und/oder zu überwachen, sowie Elemente unter diesen Containern, die eingeschlossen oder ausgeschlossen werden sollen. Zum Hinzufügen eines neuen Such Stamms instanziieren Sie ein [**isearchroot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) -Objekt, legen Sie die Stamm Attribute fest, und geben Sie dann [**isearchcrawlscopemanager:: addroot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-addroot) an, und übergeben Sie einen Zeiger auf das **isearchroot** -Objekt. Die Stamm-URL für die Suche hat dieselbe Form wie der zuvor beschriebene Such Stamm.

In der folgenden Tabelle werden die relevanten Put-Methoden für [**isearchroot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)beschrieben. die anderen Put-Methoden der Schnittstelle werden zurzeit nicht von Windows Search verwendet. Es wird empfohlen, die Sicherheits-IDs (SIDs) der Benutzer in alle Stämme einzubeziehen, um die Sicherheit zu verbessern. Pro-Benutzer-Stämme sind sicherer, wenn Abfragen in einem benutzerspezifischen Prozess ausgeführt werden. Dadurch wird sichergestellt, dass ein Benutzer die Elemente nicht sehen kann, die beispielsweise aus dem Posteingang eines anderen Benutzers indiziert wurden.



| Methode                     | BESCHREIBUNG                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bereitstellen von \_ providesbenachrichtigungen | Auf " **true** " festgelegt, wenn ein Protokollhandler oder eine andere Anwendung das Suchmodul über Änderungen an den URLs unter dem Suchstamm benachrichtigt. Die Benachrichtigung gibt an, dass die URLs neu indiziert werden müssen. |
| \_rooturl einfügen               | Legt die Stamm-URL der aktuellen Suche fest. Die URL übernimmt das Such Stamm Formular, das zuvor beschrieben wurde.                                                                                                      |



 

 

Standardmäßig durchsucht der Indexer einen Bereich nicht, wenn Sie einen Suchstamm hinzufügen. Außerdem müssen Sie eine include-Regel für den Stamm hinzufügen. Wenn Sie einen benutzerspezifischen Stamm für eine Anwendung hinzufügen möchten, sollte diese Anwendung beim Starten der Anwendung die entsprechenden Stämme für neue Benutzer hinzufügen.

Zum Hinzufügen der entsprechenden Stämme für neue Benutzer:

1.  Die SID des Benutzers erhalten.
2.  Listet alle Stämme auf, um zu überprüfen, ob für diese SID vorhanden ist.
3.  Fügen Sie ggf. einen neuen Stamm mithilfe der SID hinzu.

 

## <a name="removing-roots-from-the-crawl-scope"></a>Entfernen von Stämmen aus dem Crawl Bereich

Sie können [**isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) verwenden, um einen Stamm aus dem Crawl Bereich zu entfernen, wenn diese URL nicht mehr indiziert werden soll. Wenn Sie einen Stamm entfernen, werden auch alle Bereichs Regeln für diese URL gelöscht. Angenommen, Sie möchten einen Inhalts Speicher und/oder seinen Protokollhandler von einem System deinstallieren. Sie können die Anwendung deinstallieren, alle Daten entfernen und dann das Suchfeld aus dem Crawl Bereich entfernen, und der Crawl Scope-Manager entfernt die Stamm-und alle Bereichs Regeln, die dem Stamm zugeordnet sind.

Um einen vorhandenen Such Stamm zu entfernen, nennen Sie [**isearchcrawlscopemanager:: removeroot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) mit dem Stammverzeichnis für die Suche, das Sie entfernen möchten. Die Stamm-URL für die Suche hat dieselbe Form wie der zuvor beschriebene Such Stamm. Diese Methode gibt S \_ false zurück, wenn der Stamm nicht gefunden wurde, und einen Fehlercode, wenn beim Entfernen eines gefundenen Stamms ein Fehler aufgetreten ist.

Wenn Sie einen Suchstamm entfernen, wird auch die URL von der Benutzeroberfläche für Windows-Suchoptionen entfernt, sodass Benutzer diesen Container oder Speicherort möglicherweise nicht erneut über die Benutzeroberfläche hinzufügen können. Es ist auch möglich, alle Benutzer Satz Überschreibungen eines Suchstamms zu entfernen und die ursprünglichen Such Stamm-und Bereichs Regeln wiederherzustellen. Weitere Informationen finden Sie unter [Verwalten von Bereichs Regeln](-search-3x-wds-extidx-csm-scoperules.md).

> [!Note]  
> Wenn Benutzer unter Windows Vista über Benutzerprofile in der Systemsteuerung entfernt werden, entfernt CSM alle Regeln und Stämme mit ihrer sid und entfernt ihre indizierten Elemente aus dem Katalog. Unter Windows XP müssen Sie die Stamm Elemente und Regeln der Benutzer manuell entfernen.

 

 

## <a name="enumerating-roots-in-the-crawl-scope"></a>Enumerieren von Stämme im Crawl Bereich

Das CSM listet Such Stämme mithilfe einer standardmäßigen Enumeratorschnittstelle im com-Stil, [**ienumsearchroots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots), auf. Sie können diese Schnittstelle verwenden, um Such Stämme für eine Reihe von Zwecken aufzuzählen. Beispielsweise können Sie den gesamten Crawl Bereich auf einer Benutzeroberfläche anzeigen oder ermitteln, ob sich ein bestimmter Stamm oder das untergeordnete Element eines Stamms bereits im Crawl Bereich befindet.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**Isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[**Isearchroot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
</dt> <dt>

[**Ienumsearchroots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
</dt> <dt>

**Licher**
</dt> <dt>

[Verwenden des Crawl Scope-Managers](-search-3x-wds-extidx-csm.md)
</dt> <dt>

[Verwalten von Bereichs Regeln](-search-3x-wds-extidx-csm-scoperules.md)
</dt> </dl>

 

 



