---
title: Benachrichtigen des Index von Änderungen (Features der Legacy-Windows-Umgebung)
description: Mit Microsoft Windows Desktop Search (WDS) 2,6 können Protokollhandler für einen bestimmten Datenspeicher den WDS-Indexer anweisen, wenn sich die Daten im Speicher geändert haben.
ms.assetid: 700b1707-dd11-4a30-8f00-5c4aae1173ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6021cfe5cd7061a3d3255e56d08e665a6caedf03
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104213700"
---
# <a name="notifying-the-index-of-changes-legacy-windows-environment-features"></a>Benachrichtigen des Index von Änderungen (Features der Legacy-Windows-Umgebung)

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .

Mit Microsoft Windows Desktop Search (WDS) 2,6 können Protokollhandler für einen bestimmten Datenspeicher den WDS-Indexer anweisen, wenn sich die Daten im Speicher geändert haben. Dadurch wird die Leistung verbessert, da der Indexer nicht den gesamten Speicher auf inkrementellen Indizes durchsucht. Mithilfe von Benachrichtigungs-APIs können Protokollhandler den Indexer Benachrichtigen, dass ein Element verschoben oder gelöscht wurde, und Sie können Bereiche zur Crawl Warteschlange des WDS-Indexers von URLs hinzufügen, die die Indizierung erfordern. Die Benachrichtigung ist hilfreich für Anwendungen wie z. b. e-Mail, bei denen der Protokollhandler den Speicher überwacht und den Indexer benachrichtigt, dass sich Elemente geändert haben und eine Indizierung erforderlich ist.

## <a name="isearchitemschangedsink"></a>Isearchitemschangedsink

Protokollhandler benachrichtigen den Indexer über Änderungen über die [**isearchitemschangedsink**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) -Schnittstelle. Informationen zu Datenänderungen sollten in Such \_ Element \_ Änderungs Strukturen und \_ Suchart \_ von \_ Änderungs Enumerationstypen gesammelt und dann über die **onitemschangi-** Methode der **isearchitemschangedsink** -Schnittstelle an den Indexer übermittelt werden.

Für den Zugriff auf diese Schnittstelle müssen benutzerdefinierte Protokollhandler zuerst ein [**isearchmanager**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager) -Objekt instanziieren, um Zugriff auf das [**isearchcatalogmanager**](/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager) -Objekt zu erhalten. Von dort aus kann ein [**isearchitemschangedsink**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) -Objekt instanziiert und der Indexer über die Datenänderungen benachrichtigt werden.

Mit der onitemschangi-Methode können Sie Datenänderungen sammeln und an Ihren Kundendaten Speicher übermitteln, um die Indizierung zu initiieren.



| Richtung | Variable              | BESCHREIBUNG                                                              |
|-----------|-----------------------|--------------------------------------------------------------------------|
| In        | dwnumofchanges     | Die Gesamtanzahl der Änderungen in der Benachrichtigung.                             |
| In        | Datachangeentries\[\] | Alle Änderungs Benachrichtigungen in einem Array von Such \_ Element- \_ Änderungs Strukturen. |
| aus       | dwbatchid             | Die Batch-ID, die mit Fehlern zurückgegeben wird.                       |
| aus       | hrcompletioncodes\[\] | Gibt an, ob jede URL für die Indizierung akzeptiert wurde.                    |



 

Die Struktur der Such \_ Element \_ Änderung identifiziert die Art der aufgetretenen Änderung sowie die aktuelle URL des Elements und die vorherige URL (falls zutreffend). Die-Struktur ist wie folgt definiert:



| Eigenschaftsname | Eigenschaftstyp                  | BESCHREIBUNG                                                                |
|---------------|--------------------------------|----------------------------------------------------------------------------|
| Änderung        | \_Art \_ der \_ Änderung suchen       | Der Typ der Änderung, die benachrichtigt wird.                                 |
| URL           | LPWSTR                         | Die URL für das-Objekt, das geändert wurde.                                   |
| Oldurl        | LPWSTR                         | Wenn es sich bei der Benachrichtigung um eine Verschiebung handelt, wird die alte URL bereitgestellt und muss eindeutig sein. |
| Priorität      | \_Benachrichtigungs \_ Priorität suchen | Die Priorität der Änderung.                                                |



 

Die \_ Suchart \_ der \_ Änderungs Enumeration wird wie folgt definiert:



| Enumerationswert                           | Wert   | BESCHREIBUNG                                                                                     |
|--------------------------------------|---------|-------------------------------------------------------------------------------------------------|
| Such \_ Änderung \_ Hinzufügen                  | 0       | Bei der Benachrichtigung handelt es sich um eine zusätzliche URL.                                                      |
| Durchsuchen von \_ Änderungen \_ Löschen               | 1       | Die Benachrichtigung dient zum Löschen einer URL.                                                  |
| Änderung der Suche \_ ändern \_               | 2       | Die Benachrichtigung ist, dass eine URL geändert wurde.                                               |
| \_Umbenennen von Änderungs Änderungen durchsuchen \_ \_         | 3       | Die Benachrichtigung dient zum Verschieben und Umbenennen eines Objekts in eine neue URL.                          |
| Verzeichnis für die Suche nach \_ Änderungs \_ Semantik \_ | 0x10000 | Die Benachrichtigung gilt für eine Container-URL.                                                        |
| \_Änderungs \_ Semantik suchen ( \_ flach)   | 0x20000 | Die Benachrichtigung gilt für eine Container-URL, für die nur die zugehörigen Container Eigenschaften indiziert werden sollen. |
| Sicherheit bei der Suche nach \_ Änderungs \_ Semantik \_  | 0x40000 | Die Benachrichtigung gilt für eine URL oder Container-URL, deren Sicherheitseigenschaften geändert wurden.    |



 

Die \_ Enumeration der Such Benachrichtigungs \_ Priorität wird wie folgt definiert:



| Enumerationswert               | Wert | BESCHREIBUNG                                                                                                                                                                    |
|--------------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_normale \_ Priorität suchen | 0     | Beim Indizieren der URL sollte nur eine normale Priorität verwendet werden. Diese Benachrichtigungen werden vor der normalen inkrementellen Indizierung von Dateien und Speichern eines Benutzers verarbeitet. |



 

 

 
