---
description: Mithilfe der Benachrichtigungs-APIs können die Komponenten den Indexer Benachrichtigen, dass ein Element geändert, verschoben oder gelöscht wurde, und der Warteschlange von URLs des Windows Search-Indexers, die die Indizierung erfordern, Such Bereiche hinzufügen können.
ms.assetid: 817550e2-a256-48d5-9fa6-1ea04f8b8589
title: Benachrichtigen des Index von Änderungen (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a89112da20c4010e1fc23fab16778309195d20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128601"
---
# <a name="notifying-the-index-of-changes-windows-search"></a>Benachrichtigen des Index von Änderungen (Windows Search)

Mithilfe der Benachrichtigungs-APIs können die Komponenten den Indexer Benachrichtigen, dass ein Element geändert, verschoben oder gelöscht wurde, und der Warteschlange von URLs des Windows Search-Indexers, die die Indizierung erfordern, Such Bereiche hinzufügen können.

Komponenten können den Windows Search-Indexer Benachrichtigen, dass sich die Daten in Ihrem Speicher geändert haben. In der Regel können Sie sich auf die geplanten Crawls des Indexers verlassen. Das Bereitstellen von Benachrichtigungen an den Indexer kann jedoch die Leistung verbessern, indem sichergestellt wird, dass der Indexer nicht den gesamten Speicher auf inkrementellen Dies empfiehlt sich beispielsweise, wenn Sie davon ausgehen, dass der Datenspeicher sehr groß und/oder besonders ausgelastet ist, z. b. ein e-Mail-Datenspeicher.

-   [Implementieren von mit Indexer verwalteten Benachrichtigungen](#implementing-indexer-managed-notifications)
    -   [Warteschlange für Benachrichtigungen](#notifications-queue)
    -   [Isearchpersistentitemschangedsink](#isearchpersistentitemschangedsink)
-   [Implementieren von vom Anbieter verwalteten Benachrichtigungen](#implementing-provider-managed-notifications)
    -   [Warteschlange für Benachrichtigungen](#notifications-queue)
    -   [Isearchitemschangedsink](#isearchitemschangedsink)
    -   [Isearchnotifyinlinesite](#isearchnotifyinlinesite)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="implementing-indexer-managed-notifications"></a>Implementieren von mit Indexer verwalteten Benachrichtigungen

Durch Indexer verwaltete Benachrichtigungen können Sie den Zugriff auf Ihren Datenspeicher steuern und gleichzeitig die Benachrichtigungs Warteschlange während des gesamten Indizierungs Prozesses beibehalten. Ihr Benachrichtigungs Anbieter muss Änderungen am Datenspeicher überwachen und eine Benachrichtigungs Warteschlange erstellen. Der Anbieter sendet in regelmäßigen Abständen einen Batch mit Änderungs Benachrichtigungen an den Indexer. Wenn der Indexer Ihre Benachrichtigungen empfängt, wird eine Bestätigung zurückgegeben, und Sie können das Element (e) aus der Warteschlange entfernen. Wenn Sie nach einer bestimmten Zeitspanne keine Bestätigung erhalten, können Sie die Benachrichtigungen erneut senden. Im Falle eines Fehlers erstellt der Indexer die interne Warteschlange von Elementen neu, um den Speicher zu durchforsten oder eine inkrementelle durch Forstung durchführen.

Um von Indexer verwaltete Benachrichtigungen zu implementieren, müssen Sie Folgendes implementieren:

-   Ein Mechanismus zum Überwachen von Änderungen im Datenspeicher.
-   Eine Datenstruktur, in der Informationen zu diesen Änderungen in die Warteschlange eingereiht werden (mehrere [**Such \_ Elemente mit \_ permanenten \_ Änderungs**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) Strukturen).
-   [**Isearchpersistentitemschangedsink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) -Schnittstelle zum Senden von Benachrichtigungen an den Indexer und zum erhalten von Benachrichtigungs Bestätigungen über den Indexer.

### <a name="notifications-queue"></a>Warteschlange für Benachrichtigungen

Sie müssen jede Änderung in Ihrem Datenspeicher überwachen und in eine Warteschlange stellen, um Sie als Benachrichtigung an den Indexer zu senden. Wie viele Benachrichtigungen Sie in die Warteschlange eingereiht haben und wie oft Sie Sie an den Indexer senden, hängt von Ihren Umständen ab. Möglicherweise senden Sie einen Benachrichtigungs Stapel für jede *n* -Anzahl von Änderungen oder nach einem Zeitintervall von *t* oder eine Kombination aus beiden.

Der Indexer erwartet, dass die Benachrichtigungen in einem Array aus [**\_ \_ permanenten \_ Änderungs Strukturen für Such Elemente**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) enthalten sind, sodass Sie die Warteschlange möglicherweise ähnlich implementieren.

### <a name="isearchpersistentitemschangedsink"></a>Isearchpersistentitemschangedsink

Um auf diese Schnittstelle zuzugreifen, instanziieren Sie zuerst ein [**isearchmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) -Objekt, um Zugriff auf ein [**isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) -Objekt zu erhalten. Aus diesem **isearchcatalogmanager** -Objekt instanziieren Sie ein [**isearchpersistentitemschangedsink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) -Objekt und benachrichtigen den Indexer der Datenänderungen mit einem Aufruf der **onitemschangi-** Methode.

Beim aufzurufen dieser Methode fügen Sie die Anzahl der gemeldeten Änderungen und ein Array von [**\_ \_ permanenten \_ Änderungs Strukturen für Such Elemente**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) ein. Sie erhalten ein Array von HR-Abschluss Codes, die angeben, ob jede URL für die Indizierung akzeptiert wurde. Dies ist Ihre Bestätigung durch den Indexer.

## <a name="implementing-provider-managed-notifications"></a>Implementieren von vom Anbieter verwalteten Benachrichtigungen

Vom Anbieter verwaltete Benachrichtigungen ermöglichen es Ihnen, den Zugriff auf Ihren Datenspeicher zu steuern und den Fortschritt des Indexers zu überwachen, während er den Windows Search-Katalog aktualisiert. Der Anbieter muss Änderungen am Datenspeicher überwachen und eine Benachrichtigungs Warteschlange erstellen. Der Anbieter sendet in regelmäßigen Abständen einen Batch mit Änderungs Benachrichtigungen an den Indexer. Wenn der Indexer Ihre Benachrichtigungen empfängt, gibt er eine Bestätigung zurück. Wenn Sie nach einer bestimmten Zeitspanne keine Bestätigung erhalten, können Sie die Benachrichtigungen erneut senden. Da der Indexer den Datenspeicher durch crawlt und den Windows Search-Katalog aktualisiert, benachrichtigt er Ihren Anbieter über jedes Katalog Update, und Sie können die Elemente aus der Warteschlange entfernen. Der Anbieter behält die Benachrichtigungs Warteschlange in diesem Prozess bei, sodass Sie bei einem Ausfall Benachrichtigungen erneut an den Indexer senden können.

Um vom Anbieter verwaltete Benachrichtigungen zu implementieren, müssen Sie Folgendes implementieren:

-   Ein Mechanismus zum Überwachen von Änderungen im Datenspeicher.
-   Eine Datenstruktur, in der Informationen zu diesen Änderungen in die Warteschlange eingereiht werden (mehrere [**\_ \_ Änderungs Strukturen für Such Elemente**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) )
-   [**Isearchitemschangedsink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) -Schnittstelle zum Senden von Benachrichtigungen an den Indexer und zum erhalten von Benachrichtigungs Bestätigungen über den Indexer.
-   [**Isearchnotifyinlinesite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) -Schnittstelle zum Empfangen von Updates über den Status der Indizierung.

### <a name="notifications-queue"></a>Warteschlange für Benachrichtigungen

Sie müssen jede Änderung in Ihrem Datenspeicher überwachen und in eine Warteschlange stellen, um Sie als Benachrichtigung an den Indexer zu senden. Wie viele Benachrichtigungen Sie in die Warteschlange eingereiht haben und wie oft Sie Sie an den Indexer senden, hängt von Ihren Umständen ab. Möglicherweise senden Sie einen Benachrichtigungs Stapel für jede *n* -Anzahl von Änderungen oder nach einem Zeitintervall von *t* oder eine Kombination aus beiden.

Der Indexer erwartet, dass die Benachrichtigungen in ein Array von [**Such \_ Element- \_ Änderungs**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) Strukturen kommen, sodass Sie die Änderungs Informationen ähnlich speichern können. Allerdings müssen Sie auch die Benachrichtigungen, die Sie senden, mit den Bestätigungen und Updates vergleichen können, die vom Indexer zurückgegeben werden. Möglicherweise möchten Sie auch erkennen können, wie lange es dauert, Bestätigungen zu erhalten, sodass Sie entscheiden können, ob/wann Benachrichtigungen erneut gesendet werden sollen.

### <a name="isearchitemschangedsink"></a>Isearchitemschangedsink

Um auf diese Schnittstelle zuzugreifen, instanziieren Sie zuerst ein [**isearchmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) -Objekt, um Zugriff auf ein [**isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) -Objekt zu erhalten. Aus diesem **isearchcatalogmanager** -Objekt instanziieren Sie ein [**isearchitemschangedsink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) -Objekt und benachrichtigen den Indexer über die Datenänderungen mit einem Aufruf der **onitemschangi-** Methode.

Beim aufzurufen dieser Methode fügen Sie die Anzahl der gemeldeten Änderungen und ein Array von Änderungs Strukturen für [**Such \_ Elemente \_**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) ein. Sie erhalten ein Array von vom Indexer zugewiesenen DocIds, die jede Änderung darstellen, sowie ein Array von HR-Abschluss Codes, die angeben, ob jede URL für die Indizierung akzeptiert wurde. Dies ist Ihre Bestätigung vom Indexer, dass Sie Ihre Benachrichtigungen erhalten hat und sich darauf vorbereitet, die Elemente zu indizieren.

Ab diesem Zeitpunkt sendet der Indexer mithilfe der [**isearchnotifyinlinesite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) -Schnittstelle Updates.

### <a name="isearchnotifyinlinesite"></a>Isearchnotifyinlinesite

Um Updates zum Status Ihrer Elemente und des Katalogs zu erhalten, müssen Sie Ihre [**isearchnotifyinlinesite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) -Schnittstelle beim Indexer registrieren, damit Sie Rückrufe senden kann. Jedes Update, das mit [**isearchnotifyinlinesite:: onitemindexedstatuschange**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-onitemindexedstatuschange) gesendet wird, identifiziert die Elemente nach docid, den Status der einzelnen Elemente ([**Such \_ Element- \_ Indizierungs \_ Status**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_indexing_status)) und die Indizierungs Phase ([**Such \_ Indizierungs \_ Phase**](/windows/desktop/api/Searchapi/ne-searchapi-search_indexing_phase)), in der sich die Elemente befinden.

Sie erhalten nicht nur Updates zum Status der einzelnen Elemente, wie zuvor beschrieben, sondern auch wichtige Informationen zum Status des Katalogs. Der Windows Search-Dienst kann vom Endbenutzer, einer Drittanbieter Anwendung oder einem anderen Fehler unterbrochen oder neu gestartet werden. Wenn dies geschieht, benötigen Sie eine Möglichkeit, um zu bestimmen, welche Benachrichtigungen erneut an den Indexer gesendet werden sollen.

Die [**isearchnotifyinlinesite:: oncatalogstatuschange**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-oncatalogstatuschange) -Methode, die vom Windows Search-Dienst aufgerufen wird, informiert Clients über den Status des Katalogs mithilfe der in der folgenden Tabelle beschriebenen Parameter.



| Parameter                 | BESCHREIBUNG                                                                                                                                           |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| guidcatalogresetsignature | Eine GUID, die das Zurücksetzen des Katalogs darstellt. Wenn diese GUID geändert wird, müssen alle Benachrichtigungen erneut gesendet werden.                                                        |
| guidcheckpointsignature   | Eine GUID, die den letzten wiederhergestellten Prüfpunkt darstellt. Wenn diese GUID geändert wird, müssen alle seit dem letzten gespeicherten Prüfpunkt gesammelten Benachrichtigungen erneut gesendet werden. |
| dwlastcheckpointnumber    | Eine Zahl, die den letzten gespeicherten Prüfpunkt angibt.                                                                                                        |



 

 

Wenn ein Katalog-Prüfpunkt auftritt, aktualisiert der Suchdienst *dwlastcheckpointnumber*, und alle vor diesem Prüfpunkt gesendeten Benachrichtigungen sind sicher und können im Fall eines Dienst Fehlers wieder hergestellt werden. Benachrichtigungs Anbieter müssen nur die Benachrichtigungen, die zwischen Prüfpunkten gesendet werden, nachverfolgen und im Fall einer Katalog Wiederherstellung oder-zurück Setzung erneut pushen.

Wenn eine Katalog Wiederherstellung erfolgt, führt der Suchdienst einen Rollback des Katalogs zum letzten gespeicherten Prüfpunkt aus und aktualisiert die *guidcheckpointsignature*. In dieser Situation müssen Benachrichtigungs Anbieter alle seit dem letzten gespeicherten Prüfpunkt akkumulierten Benachrichtigungen, wie von *dwlastcheckpointnumber* identifiziert, erneut pushen.

Wenn ein Katalog zurückgesetzt werden soll, setzt der Suchdienst den gesamten Katalog zurück und aktualisiert die *guidcatalogresetsignature*. Der Benachrichtigungs Anbieter muss den gesamten Crawl Bereich erneut pushen.

## <a name="additional-resources"></a>Weitere Ressourcen

-   Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).
-   Informationen zu Übersichten des Katalog-Managers und des Katalog-Such-Managers (CSM) finden [Sie unter Verwenden des Katalog-Managers](-search-3x-wds-mngidx-catalog-manager.md) und [Verwenden des Crawl Scope-Managers](-search-3x-wds-extidx-csm.md).
-   Weitere Informationen zum Erstellen eines Shell-Datenspeicher finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Entwickeln von Protokoll Handlern](-search-3x-wds-phaddins.md)
</dt> <dt>

[Grundlegendes zu Protokoll Handlern](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Hinzufügen von Symbolen und Kontextmenüs](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Code Beispiel: Shellerweiterungen für Protokollhandler](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installieren und Registrieren von Protokoll Handlern](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Erstellen eines Suchconnector für einen Protokoll Handler](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Debuggen von Protokoll Handlern](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
