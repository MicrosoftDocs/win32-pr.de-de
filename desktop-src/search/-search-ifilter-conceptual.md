---
description: Erfahren Sie, wie Sie Filterhandler in der Windows entwickeln. Bei der Suche werden Filter verwendet, um Elemente für die Aufnahme in einen Volltextindex zu extrahieren.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Entwickeln von Filterhandlern für Windows Suchen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36cb8fe61ce85c86d0b8397d81303014ed1268bc0aef96b22e7b7bab335b7f10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597820"
---
# <a name="developing-filter-handlers-for-windows-search"></a>Entwickeln von Filterhandlern für Windows Suchen

Microsoft Windows Search verwendet Filter, um den Inhalt von Elementen für die Aufnahme in einen Volltextindex zu extrahieren. Sie können Windows Search erweitern, um neue oder proprietäre Dateitypen zu indizieren, indem Sie Filter schreiben, um den Inhalt zu extrahieren, und Eigenschaftenhandler, um die Eigenschaften von Dateien zu extrahieren.

Dieser Abschnitt enthält das konzeptionelle Framework, das zum Implementieren eines Filterhandlers (einer Implementierung der [**IFilter-Schnittstelle) erforderlich**](/windows/win32/api/filter/nn-filter-ifilter) ist.

- [Grundlegendes zu Filterhandlern in Windows Search](-search-ifilter-about.md)
- [Bewährte Methoden zum Erstellen von Filterhandlern in Windows Search](-search-3x-wds-extidx-filters.md)
- [Zurückgeben von Eigenschaften von einem Filterhandler](-search-ifilter-property-filtering.md)
- [Filterhandler, die mit Windows](-search-ifilter-implementations.md)
- [Implementieren von Filterhandlern in Windows Search](-search-ifilter-constructing-filters.md)
- [Registrieren von Filterhandlern](-search-ifilter-registering-filters.md)
- [Testen von Filterhandlern](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a>Weitere Ressourcen

- Das [IFilterSample-Codebeispiel,](-search-sample-ifiltersample.md) das auf GitHub verfügbar [ist,](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)veranschaulicht, wie eine IFilter-Basisklasse zum Implementieren der [**IFilter-Schnittstelle erstellt**](/windows/win32/api/filter/nn-filter-ifilter) wird.
- Eine Übersicht über den Indizierungsprozess finden Sie unter [Der Indizierungsprozess](-search-indexing-process-overview.md).
- Eine Übersicht über Dateitypen finden Sie unter [Dateitypen.](../shell/fa-file-types.md)
- Informationen zum Abfragen von Dateiassoziationsattributen für einen Dateityp finden Sie unter [PerceivedTypes, SystemFileAssociations und Application Registration.](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))
