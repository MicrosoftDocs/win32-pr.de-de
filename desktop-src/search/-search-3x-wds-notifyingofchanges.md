---
description: Mithilfe der Benachrichtigungs-APIs können Komponenten den Indexer darüber benachrichtigen, dass ein Element geändert, verschoben oder gelöscht wurde, und der Warteschlange von URLs, die eine Indizierung erfordern, Suchbereich zur Warteschlange des Windows Search-Indexers hinzufügen.
ms.assetid: 817550e2-a256-48d5-9fa6-1ea04f8b8589
title: Benachrichtigen des Indexes über Änderungen (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb386763be5192851368b1f46b69f94576fbe261a57d215d649d38ac5a19ecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118052227"
---
# <a name="notifying-the-index-of-changes-windows-search"></a>Benachrichtigen des Indexes über Änderungen (Windows Search)

Mithilfe der Benachrichtigungs-APIs können Komponenten den Indexer darüber benachrichtigen, dass ein Element geändert, verschoben oder gelöscht wurde, und der Warteschlange von URLs, die eine Indizierung erfordern, Suchbereich zur Warteschlange des Windows Search-Indexers hinzufügen.

Komponenten können den Indexer Windows Search benachrichtigen, dass sich die Daten in ihrem Speicher geändert haben. In der Regel können Sie sich auf die geplanten Durchforstungen des Indexers verlassen. Die Bereitstellung von Benachrichtigungen an den Indexer kann jedoch die Leistung verbessern, indem sichergestellt wird, dass der Indexer nicht den gesamten Speicher für inkrementelle Indizes durchforscht. Dies kann beispielsweise empfohlen werden, wenn Sie davon ausgehen, dass Ihr Datenspeicher sehr groß und/oder besonders ausgelastet ist, z. B. ein E-Mail-Datenspeicher.

-   [Implementieren von von Indexer verwalteten Benachrichtigungen](#implementing-indexer-managed-notifications)
    -   [Benachrichtigungswarteschlange](#notifications-queue)
    -   [ISearchPersistentItemsChangedSink](#isearchpersistentitemschangedsink)
-   [Implementieren von vom Anbieter verwalteten Benachrichtigungen](#implementing-provider-managed-notifications)
    -   [Benachrichtigungswarteschlange](#notifications-queue)
    -   [ISearchItemsChangedSink](#isearchitemschangedsink)
    -   [ISearchNotifyInlineSite](#isearchnotifyinlinesite)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="implementing-indexer-managed-notifications"></a>Implementieren von von Indexer verwalteten Benachrichtigungen

Mit vom Indexer verwalteten Benachrichtigungen können Sie den Zugriff auf Ihren Datenspeicher steuern und gleichzeitig die Warteschlange für Benachrichtigungen während des gesamten Indizierungsprozesses verwalten. Ihr Benachrichtigungsanbieter muss Änderungen am Datenspeicher überwachen und eine Benachrichtigungswarteschlange erstellen. Ihr Anbieter sendet regelmäßig einen Batch von Änderungsbenachrichtigungen an den Indexer. Wenn der Indexer Ihre Benachrichtigungen empfängt, gibt er eine Bestätigung zurück, und Sie können die Elemente aus Ihrer Warteschlange entfernen. Wenn Sie nach einem bestimmten Zeitraum keine Bestätigung erhalten, können Sie die Benachrichtigungen erneut senden. Im Falle eines Fehlers erstellt der Indexer seine interne Warteschlange von Elementen neu, um den Speicher zu durchforsten, oder führt eine inkrementelle Durchforstung des Speichers aus.

Um vom Indexer verwaltete Benachrichtigungen zu implementieren, müssen Sie Folgendes implementieren:

-   Ein Mechanismus zum Überwachen von Änderungen in Ihrem Datenspeicher.
-   Eine Datenstruktur, um Informationen zu diesen Änderungen in die Warteschlange zu stellen (mehrere [**SEARCH \_ ITEM PERSISTENT \_ \_ CHANGE-Strukturen).**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change)
-   [**ISearchPersistentItemsChangedSink-Schnittstelle,**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) um Ihre Benachrichtigungen an den Indexer zu senden und Benachrichtigungsbestätigungen vom Indexer zu erhalten.

### <a name="notifications-queue"></a>Benachrichtigungswarteschlange

Sie müssen jede Änderung in Ihrem Datenspeicher überwachen und in die Warteschlange stellen, um sie als Benachrichtigung an den Indexer zu senden. Wie viele Benachrichtigungen Sie in die Warteschlange stellen und wie oft Sie sie an den Indexer senden, hängt von Ihren Umständen ab. Möglicherweise senden Sie einen Batch von Benachrichtigungen für jede n Anzahl von Änderungen oder nach einem *bestimmten* *Zeitintervall* oder einer Kombination der beiden.

Der Indexer erwartet, dass die Benachrichtigungen in einem Array von [**SEARCH \_ ITEM PERSISTENT \_ \_ CHANGE-Strukturen**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) angezeigt werden, sodass Sie ihre Warteschlange auf ähnliche Weise implementieren können.

### <a name="isearchpersistentitemschangedsink"></a>ISearchPersistentItemsChangedSink

Um auf diese Schnittstelle zu zugreifen, instanziieren Sie zunächst ein [**ISearchManager-Objekt,**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) um Zugriff auf ein [**ISearchCatalogManager-Objekt zu**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) erhalten. Von diesem **ISearchCatalogManager-Objekt** instanziieren Sie ein [**ISearchPersistentItemsChangedSink-Objekt**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) und benachrichtigen den Indexer über die Datenänderungen mit einem Aufruf der **OnItemsChanged-Methode.**

In den Aufruf dieser Methode schließen Sie die Anzahl der gemeldeten Änderungen und ein Array von [**PERSISTENT CHANGE-Strukturen für SEARCH \_ ITEM \_ \_**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) ein. Sie erhalten ein Array von HR-Vervollständigungscodes zurück, die angeben, ob jede URL für die Indizierung akzeptiert wurde. Dies ist Ihre Bestätigung vom Indexer.

## <a name="implementing-provider-managed-notifications"></a>Implementieren von vom Anbieter verwalteten Benachrichtigungen

Mit vom Anbieter verwalteten Benachrichtigungen können Sie den Zugriff auf Ihren Datenspeicher steuern und den Fortschritt des Indexers überwachen, während er den Suchkatalog Windows aktualisiert. Ihr Anbieter muss Änderungen am Datenspeicher überwachen und eine Benachrichtigungswarteschlange erstellen. Ihr Anbieter sendet regelmäßig einen Batch von Änderungsbenachrichtigungen an den Indexer. Wenn der Indexer Ihre Benachrichtigungen empfängt, gibt er eine Bestätigung zurück. Wenn Sie nach einem bestimmten Zeitraum keine Bestätigung erhalten, können Sie die Benachrichtigungen erneut senden. Während der Indexer den Datenspeicher durchforscht und den Windows Search-Katalog aktualisiert, benachrichtigt er Ihren Anbieter über jedes Katalogupdate, und Sie können die Elemente aus der Warteschlange entfernen. Ihr Anbieter verwaltet während dieses Prozesses seine Benachrichtigungswarteschlange, sodass Sie im Falle eines Fehlers Benachrichtigungen erneut an den Indexer senden können.

Um vom Anbieter verwaltete Benachrichtigungen zu implementieren, müssen Sie Folgendes implementieren:

-   Ein Mechanismus zum Überwachen von Änderungen in Ihrem Datenspeicher.
-   Eine Datenstruktur, um Informationen zu diesen Änderungen in die Warteschlange zu stellen (mehrere [**SEARCH \_ ITEM \_ CHANGE-Strukturen).**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change)
-   [**ISearchItemsChangedSink-Schnittstelle,**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) um Ihre Benachrichtigungen an den Indexer zu senden und Benachrichtigungsbestätigungen vom Indexer zu erhalten.
-   [**ISearchNotifyInlineSite-Schnittstelle,**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) um Updates zum Status der Indizierung zu erhalten.

### <a name="notifications-queue"></a>Benachrichtigungswarteschlange

Sie müssen jede Änderung in Ihrem Datenspeicher überwachen und in die Warteschlange stellen, um sie als Benachrichtigung an den Indexer zu senden. Wie viele Benachrichtigungen Sie in die Warteschlange stellen und wie oft Sie sie an den Indexer senden, hängt von Ihren Umständen ab. Möglicherweise senden Sie einen Batch von Benachrichtigungen für jede n Anzahl von Änderungen oder nach einem *bestimmten* *Zeitintervall* oder einer Kombination der beiden.

Der Indexer erwartet, dass die Benachrichtigungen in einem Array von [**SEARCH \_ ITEM \_ CHANGE-Strukturen**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) enthalten sind, sodass Sie änderungsinformationen auf ähnliche Weise speichern können. Sie müssen jedoch auch in der Lage sein, die Benachrichtigungen, die Sie senden, mit den Bestätigungen und Updates zu übereinstimmen, die vom Indexer zurückgegeben werden. Möglicherweise möchten Sie auch erkennen können, wie lange das Empfangen von Bestätigungen dauert, damit Sie entscheiden können, ob/wann Benachrichtigungen erneut gesendet werden sollen.

### <a name="isearchitemschangedsink"></a>ISearchItemsChangedSink

Um auf diese Schnittstelle zu zugreifen, instanziieren Sie zunächst ein [**ISearchManager-Objekt,**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) um Zugriff auf ein [**ISearchCatalogManager-Objekt zu**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) erhalten. Aus diesem **ISearchCatalogManager-Objekt** instanziieren Sie ein [**ISearchItemsChangedSink-Objekt**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) und benachrichtigen den Indexer über die Datenänderungen mit einem Aufruf der **OnItemsChanged-Methode.**

In den Aufruf dieser Methode schließen Sie die Anzahl der gemeldeten Änderungen und ein Array von [**SEARCH \_ ITEM \_ CHANGE-Strukturen**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) ein. Sie erhalten ein Array von Vom Indexer zugewiesenen DocIds zurück, die jede Änderung darstellen, sowie ein Array von HR-Vervollständigungscodes, die angeben, ob jede URL für die Indizierung akzeptiert wurde. Dies ist Ihre Bestätigung vom Indexer, dass er Ihre Benachrichtigungen empfangen hat und die Indizierung der Elemente vorbereitet.

Ab diesem Zeitpunkt sendet der Indexer Updates mithilfe der [**ISearchNotifyInlineSite-Schnittstelle.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite)

### <a name="isearchnotifyinlinesite"></a>ISearchNotifyInlineSite

Um Updates zum Status Ihrer Elemente und des Katalogs zu erhalten, müssen Sie Ihre [**ISearchNotifyInlineSite-Schnittstelle**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) beim Indexer registrieren, damit sie Rückrufe senden kann. Jedes Update, das mithilfe von [**ISearchNotifyInlineSite::OnItemIndexedStatusChange**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-onitemindexedstatuschange) gesendet wird, identifiziert die Elemente anhand von DocId, des Status jedes Elements ([**SEARCH ITEM \_ \_ INDEXING \_ STATUS**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_indexing_status)) und der Indizierungsphase ([**SEARCH \_ INDEXING \_ PHASE**](/windows/desktop/api/Searchapi/ne-searchapi-search_indexing_phase)), in der sich die Elemente befinden.

Sie erhalten nicht nur Updates zum Status der einzelnen Elemente, wie zuvor beschrieben, sondern auch wichtige Informationen zum Status des Katalogs selbst. Die Windows Suchdienst kann vom Endbenutzer, einer Drittanbieteranwendung oder einem anderen Fehler unterbrochen oder neu gestartet werden. In diesem Fall benötigen Sie eine Möglichkeit, um zu bestimmen, welche Benachrichtigungen an den Indexer zurückgeusht werden sollen.

Die [**ISearchNotifyInlineSite::OnCatalogStatusChange-Methode,**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-oncatalogstatuschange) die vom Windows Suchdienst aufgerufen wird, informiert Clients mithilfe der in der folgenden Tabelle beschriebenen Parameter über den Status des Katalogs.



| Parameter                 | Beschreibung                                                                                                                                           |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| guidCatalogResetSignature | Eine GUID, die die Katalogzurücksetzung darstellt. Wenn sich diese GUID ändert, müssen alle Benachrichtigungen erneut gesendet werden.                                                        |
| guidCheckPointSignature   | Eine GUID, die den letzten wiederhergestellten Prüfpunkt darstellt. Wenn sich diese GUID ändert, müssen alle Benachrichtigungen, die seit dem letzten gespeicherten Prüfpunkt gesammelt wurden, erneut gesendet werden. |
| dwLastCheckPointNumber    | Eine Zahl, die den letzten gespeicherten Prüfpunkt angibt.                                                                                                        |



 

 

Wenn ein Katalogprüfpunkt auftritt, aktualisiert der Suchdienst *dwLastCheckPointNumber,* und alle vor diesem Prüfpunkt gesendeten Benachrichtigungen sind im Falle eines Dienstfehlers sicher und wiederherstellbar. Benachrichtigungsanbieter müssen im Falle einer Katalogwiederherstellung oder -zurücksetzung nur die Benachrichtigungen nachverfolgen, die zwischen Prüfpunkten und Demush gesendet werden.

Wenn eine Katalogwiederherstellung erfolgt, führt der Suchdienst ein Rollback des Katalogs auf den zuletzt gespeicherten Prüfpunkt aus und aktualisiert *guidCheckPointSignature*. In diesem Fall müssen Benachrichtigungsanbieter alle Benachrichtigungen, die seit dem letzten gespeicherten Prüfpunkt gesammelt wurden, wie von *dwLastCheckPointNumber identifiziert, erneut über die Benachrichtigungen senden.*

Wenn eine Katalogzurücksetzung erfolgen soll, setzt der Suchdienst den gesamten Katalog zurück und aktualisiert *guidCatalogResetSignature*. Der Benachrichtigungsanbieter muss den gesamten Durchforstungsbereich erneut übertragen.

## <a name="additional-resources"></a>Weitere Ressourcen

-   Eine Übersicht über den Indizierungsprozess finden Sie unter [Der Indizierungsprozess](-search-indexing-process-overview.md).
-   Eine Übersicht über den Katalog-Manager und den Katalogsuche-Manager (Catalog Search Manager, CSM) finden Sie unter Verwenden des [Katalog-Managers](-search-3x-wds-mngidx-catalog-manager.md) und [Verwenden der Durchforstungsbereich-Manager.](-search-3x-wds-extidx-csm.md)
-   Informationen zum Erstellen eines Shell-Datenspeichers finden Sie unter [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Entwickeln von Protokollhandlern](-search-3x-wds-phaddins.md)
</dt> <dt>

[Grundlegendes zu Protokollhandlern](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Hinzufügen von Symbolen und Kontextmenüs](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Codebeispiel: Shellerweiterungen für Protokollhandler](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installieren und Registrieren von Protokollhandlern](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Erstellen eines Suchconnectors für einen Protokollhandler](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Debuggen von Protokollhandlern](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
