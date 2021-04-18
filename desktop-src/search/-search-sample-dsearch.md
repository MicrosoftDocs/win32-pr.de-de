---
description: Das dsearch-Codebeispiel veranschaulicht, wie eine Klasse für eine statische Konsolenanwendung erstellt wird, um die Windows-Suche mithilfe der Microsoft. search. Interop-Assembly für isearchqueryhelper abzufragen.
ms.assetid: 9c09b1fe-c63e-4c6e-9c8b-f5e29cf0fe9e
title: Dsearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4285596a8109361accd6b3adecf80ea98074e55e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343264"
---
# <a name="dsearch"></a>Dsearch

Das dsearch-Codebeispiel veranschaulicht, wie eine Klasse für eine statische Konsolenanwendung erstellt wird, um die Windows-Suche mithilfe der Microsoft. search. Interop-Assembly für [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)abzufragen.

Dieses Thema enthält folgende Abschnitte:

- [Anforderungen](#requirements)
- [Herunterladen des Beispiels](#downloading-the-sample)
- [Beispiel zum Aufbau](#building-the-sample)
- [Ausführen des Beispiels](#running-the-sample)
- [Zugehörige Themen](#related-topics)

## <a name="requirements"></a>Anforderungen

| Produkt     | Produktversion          |
|-------------|--------------------------|
| Windows     | Windows 7, 8.1 oder 10    |
| Windows SDK | 7,0 oder höher           |

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im folgenden Speicherort verfügbar.

| Standort      | Pfad-URL                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [Dsearch-Beispiel](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/DSearch)         |

> [!NOTE]  
> Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.

## <a name="building-the-sample"></a>Erstellen des Beispiels

1. Öffnen Sie Windows-Explorer, und navigieren Sie zum **dsearch** -Projektverzeichnis.
2. Doppelklicken Sie auf das Symbol für die Datei dsearch. sln, um das Projekt in Visual Studio zu öffnen.
  
    > [!NOTE]  
    > Die SLN-Datei wurde mit einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen. Dies wirkt sich nicht auf das Verhalten des Beispiels aus.

3. Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1. Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2. Geben Sie an der Eingabeaufforderung ein, `DSearch.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für DSearch.exe.

## <a name="related-topics"></a>Zugehörige Themen

### <a name="reference"></a>Referenz

[**Isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)

[**Isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

### <a name="other-samples"></a>Weitere Beispiele

[Code Beispiele durchsuchen](-search-samples-ovw.md)
