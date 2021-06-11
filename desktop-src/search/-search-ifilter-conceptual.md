---
description: Erfahren Sie, wie Sie Filterhandler in Windows Search. Bei der Suche werden Filter verwendet, um Elemente für die Aufnahme in einen Volltextindex zu extrahieren.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Entwickeln von Filterhandlern für Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa86c0a1e41ababf6f00db72a26784beb93e1879
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988859"
---
# <a name="developing-filter-handlers-for-windows-search"></a>Entwickeln von Filterhandlern für Windows Search

Microsoft Windows Search verwendet Filter, um den Inhalt von Elementen für die Aufnahme in einen Volltextindex zu extrahieren. Sie können die Windows Search, um neue oder proprietäre Dateitypen zu indizieren, indem Sie Filter schreiben, um den Inhalt zu extrahieren, und Eigenschaftenhandler, um die Eigenschaften von Dateien zu extrahieren.

Dieser Abschnitt enthält das konzeptionelle Framework, das zum Implementieren eines Filterhandlers (einer Implementierung der [**IFilter-Schnittstelle) erforderlich**](/windows/win32/api/filter/nn-filter-ifilter) ist.

- [Grundlegendes zu Filterhandlern in Windows Search](-search-ifilter-about.md)
- [Bewährte Methoden zum Erstellen von Filterhandlern in Windows Search](-search-3x-wds-extidx-filters.md)
- [Zurückgeben von Eigenschaften von einem Filterhandler](-search-ifilter-property-filtering.md)
- [Filterhandler, die mit Windows gesendet werden](-search-ifilter-implementations.md)
- [Implementieren von Filterhandlern in Windows Search](-search-ifilter-constructing-filters.md)
- [Registrieren von Filterhandlern](-search-ifilter-registering-filters.md)
- [Testen von Filterhandlern](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a>Weitere Ressourcen

- Das [IFilterSample-Codebeispiel,](-search-sample-ifiltersample.md) das auf [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)verfügbar ist, veranschaulicht das Erstellen einer IFilter-Basisklasse für die Implementierung der [**IFilter-Schnittstelle.**](/windows/win32/api/filter/nn-filter-ifilter)
- Eine Übersicht über den Indizierungsprozess finden Sie unter [Der Indizierungsprozess](-search-indexing-process-overview.md).
- Eine Übersicht über Dateitypen finden Sie unter [Dateitypen.](../shell/fa-file-types.md)
- Informationen zum Abfragen von Dateiassoziationsattributen für einen Dateityp finden Sie unter [PerceivedTypes, SystemFileAssociations und Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).
