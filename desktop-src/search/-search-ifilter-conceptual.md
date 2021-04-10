---
description: Microsoft Windows Search verwendet Filter zum Extrahieren des Inhalts von Elementen für die Aufnahme in einen Volltextindex.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Entwickeln von Filter Handlern für Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8f45892549dc3f392824c31c78884b209d283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041631"
---
# <a name="developing-filter-handlers-for-windows-search"></a>Entwickeln von Filter Handlern für Windows Search

Microsoft Windows Search verwendet Filter zum Extrahieren des Inhalts von Elementen für die Aufnahme in einen Volltextindex. Sie können Windows Search erweitern, um neue oder proprietäre Dateitypen zu indizieren, indem Sie Filter zum Extrahieren des Inhalts schreiben und Eigenschaften Handler, um die Eigenschaften von Dateien zu extrahieren.

Dieser Abschnitt enthält das konzeptionelle Framework, das zum Implementieren eines Filter Handlers (einer Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle) erforderlich ist.

- [Grundlegendes zu Filter Handlern in Windows Search](-search-ifilter-about.md)
- [Bewährte Methoden zum Erstellen von Filter Handlern in Windows Search](-search-3x-wds-extidx-filters.md)
- [Zurückgeben von Eigenschaften aus einem Filter Handler](-search-ifilter-property-filtering.md)
- [Filtern von Handlern, die mit Windows ausgeliefert werden](-search-ifilter-implementations.md)
- [Implementieren von Filter Handlern in Windows Search](-search-ifilter-constructing-filters.md)
- [Registrieren von Filter Handlern](-search-ifilter-registering-filters.md)
- [Testen von Filter Handlern](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a>Weitere Ressourcen

- Das in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)verfügbare [ifiltersample](-search-sample-ifiltersample.md) -Codebeispiel veranschaulicht, wie eine IFilter-Basisklasse für die Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle erstellt wird.
- Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).
- Eine Übersicht über die Dateitypen finden Sie unter [Dateitypen](../shell/fa-file-types.md).
- Informationen zum Abfragen von Datei Zuordnungs Attributen für einen Dateityp finden Sie unter " [wahrtentypen", "systemfileassociation" und "Anwendungs Registrierung](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))".
