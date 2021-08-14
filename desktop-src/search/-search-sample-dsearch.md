---
description: Das DSearch-Codebeispiel veranschaulicht das Erstellen einer Klasse für eine statische Konsolenanwendung zum Abfragen von Windows Search mithilfe der Microsoft.Search.Interop-Assembly für ISearchQueryHelper.
ms.assetid: 9c09b1fe-c63e-4c6e-9c8b-f5e29cf0fe9e
title: DSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2505a8482a698f3147ae9c13ddb135c1da1c584f16cf52a5a05ca469efbc968
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680711"
---
# <a name="dsearch"></a>DSearch

Das DSearch-Codebeispiel veranschaulicht das Erstellen einer Klasse für eine statische Konsolenanwendung zum Abfragen von Windows Search mithilfe der Microsoft.Search.Interop-Assembly für [**ISearchQueryHelper.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)

Dieses Thema enthält folgende Abschnitte:

- [Requirements](#requirements)
- [Herunterladen des Beispiels](#downloading-the-sample)
- [Erstellen des Beispiels](#building-the-sample)
- [Ausführen des Beispiels](#running-the-sample)
- [Zugehörige Themen](#related-topics)

## <a name="requirements"></a>Anforderungen

| Product (Produkt)     | Produktversion          |
|-------------|--------------------------|
| Windows     | Windows 7, 8.1 oder 10    |
| Windows SDK | 7.0 oder höher           |

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist an folgendem Speicherort verfügbar.

| Standort      | Pfad-URL                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [DSearch-Beispiel](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/DSearch)         |

> [!NOTE]  
> Für alle Versionen von Windows, einschließlich Windows 7, wird empfohlen, die Beispiele für die aktuelle Version direkt von GitHub herunterzuladen.

## <a name="building-the-sample"></a>Erstellen des Beispiels

1. Öffnen Windows Explorer, und navigieren Sie zum **DSearch-Projektverzeichnis.**
2. Doppelklicken Sie auf das Symbol für die Datei DSearch.sln, um das Projekt in der Visual Studio.
  
    > [!NOTE]  
    > Die SLN-Datei wurde unter einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen. Dies wirkt sich nicht auf das Verhalten des Beispiels aus.

3. Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

1. Navigieren Sie zum Verzeichnis, das die neue ausführbare Datei enthält, indem Sie das Eingabeaufforderungsfenster oder den Windows verwenden.
2. Geben Sie an der Eingabeaufforderung ein, oder doppelklicken Sie im Windows Explorer auf das Symbol `DSearch.exe` für DSearch.exe.

## <a name="related-topics"></a>Zugehörige Themen

### <a name="reference"></a>Verweis

[**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)

[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

### <a name="other-samples"></a>Weitere Beispiele

[Suchcodebeispiele](-search-samples-ovw.md)
