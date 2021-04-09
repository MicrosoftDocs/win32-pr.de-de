---
description: Die isearchmanager-Schnittstelle stellt Methoden bereit, die Katalog übergreifende Änderungen vornehmen.
ms.assetid: e6f4432b-03bf-4711-a79e-1bf9242c5683
title: Verwenden des Such-Managers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3e8c52211c7d69ba7a50c9a9925dad8bb84f848
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958789"
---
# <a name="using-the-search-manager"></a>Verwenden des Such-Managers

Die [**isearchmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) -Schnittstelle stellt Methoden bereit, die Katalog übergreifende Änderungen vornehmen. Änderungen, die auf der **isearchmanager** -Ebene vorgenommen werden, gelten global für alle vom Indexer verwendeten Kataloge. Änderungen, die auf der [**isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) -Ebene vorgenommen werden, gelten jedoch für bestimmte Kataloge. Derzeit verwendet Windows Search jedoch nur einen Katalog, SystemIndex. Mit dem Such-Manager können Sie folgende Aufgaben ausführen:

- Sie erhalten eine Instanz des Katalog-Managers für den Such Katalog.
- Erhalten Sie Versionsinformationen zur Windows-Such-Engine.

Die folgenden Methoden der [**isearchmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) -Schnittstelle können Ihnen helfen, ihre Such Kataloge zu verwalten:

| Methode                                                                      | BESCHREIBUNG                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog)                     | Ruft einen Katalog anhand des Namens ab und gibt eine Instanz von [**isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) für diesen Katalog zurück. Dies ermöglicht es Ihnen, einen einzelnen Such Katalog zu verwalten.                                          |
| [**Getindexerversion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getindexerversion)       | Gibt die Version des Indexers in zwei Ganzzahlen zurück: Hauptversion und neben Version. Die Hauptversionsnummer für die Windows 10-Suche lautet z. b. "10", und die neben Versionsnummer ist "0". Bei Windows Vista Search und Windows Search 3,0 unter Windows XP lautet die Hauptversionsnummer "3", und die neben Versionsnummer ist "0". |
| [**Getindexerversionstr**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getindexerversionstr) | Gibt die vollständige Versionsnummer des Indexers als Zeichenfolge zurück, z. b. "10.0.18309.1000". Für Windows 10 entspricht dies in der Regel der Versionsnummer des Betriebssystems. Für Windows XP, Vista und 7 ist es anders.                                                                                                                                        |


Weitere Informationen zu diesen Methoden finden Sie in der [**isearchmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) -Dokumentation.

Die folgenden [**isearchmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) -Methoden sind für die zukünftige Verwendung reserviert. Sie sind jedoch implementiert und wirken sich nicht auf den Indexer oder Katalog aus, da zu diesem Zeitpunkt nur ein Katalog für Windows Search vorhanden ist.

- **\_BypassList-Abfrage**
- **\_localbypass erhalten**
- **\_Portnummer erhalten**
- **get \_ Proxyname**
- **\_UseProxy erhalten**
- **\_userAgent erhalten**
- **\_userAgent platzieren**
- **SetProxy**

" **GetParameter** " und " **SetParameter** " sind auch für die zukünftige Verwendung reserviert, aber nicht implementiert.

## <a name="related-topics"></a>Zugehörige Themen

[Verwalten des Indexes](-search-3x-wds-mngidx-overview.md)

[Schnittstellen für die Verwaltung des Indexes](interfaces-for-managing-the-index.md)

[Verwenden des Katalog-Managers](-search-3x-wds-mngidx-catalog-manager.md)

[Verwenden des Crawl Scope-Managers](-search-3x-wds-extidx-csm.md)
