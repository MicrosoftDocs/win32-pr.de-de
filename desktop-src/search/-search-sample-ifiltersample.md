---
description: Das IFilterSample-Codebeispiel veranschaulicht, wie Sie eine IFilter-Basisklasse zum Implementieren der IFilter-Schnittstelle erstellen.
ms.assetid: 4c0df747-627d-4937-a117-d43137d5d081
title: IFilterSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f015166d0366152d07a5fb8d182edcb5422112c66f016219970fef9b889df3ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863733"
---
# <a name="ifiltersample"></a>IFilterSample

Das IFilterSample-Codebeispiel veranschaulicht, wie Sie eine IFilter-Basisklasse zum Implementieren der [**IFilter-Schnittstelle**](/windows/win32/api/filter/nn-filter-ifilter) erstellen.

Dieses Thema enthält folgende Abschnitte:

- [Requirements](#requirements)
- [Herunterladen des Beispiels](#downloading-the-sample)
- [Erstellen des Beispiels](#building-the-sample)
- [Ausführen des Beispiels](#running-the-sample)
- [Zugehörige Themen](#related-topics)

## <a name="requirements"></a>Anforderungen

| Produkt     | Produktversion          |
|-------------|--------------------------|
| Windows     | Windows 7, 8.1 oder 10    |
| Windows SDK | 7.0 oder höher           |

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist an folgendem Speicherort verfügbar.

| Standort      | Pfad-URL                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [IFilterSample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)          |

> [!NOTE]  
> Für alle Versionen von Windows, einschließlich Windows 7, wird empfohlen, die Beispiele direkt aus GitHub herunterzuladen, um die aktuellste Version zu erhalten.

## <a name="building-the-sample"></a>Erstellen des Beispiels

1. Öffnen Sie Windows Explorer, und navigieren Sie zum **Projektverzeichnis FilterBase.**
2. Doppelklicken Sie auf das Symbol für die Datei FilterBase.sln, um das Projekt in Visual Studio zu öffnen.

    > [!NOTE]  
    > Die SLN-Datei wurde unter einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen. Dies wirkt sich nicht auf das Verhalten des Beispiels aus.

3. Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

1. Navigieren Sie mithilfe des Eingabeaufforderungsfensters oder Windows Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2. Geben Sie an der Eingabeaufforderung `FilterBase.exe` ein, oder doppelklicken Sie in Windows Explorer auf das Symbol für FilterBase.exe.

## <a name="related-topics"></a>Zugehörige Themen

### <a name="reference"></a>Verweis

[**Ifilter**](/windows/win32/api/filter/nn-filter-ifilter)

### <a name="conceptual"></a>Konzept

[Entwickeln von Filterhandlern](-search-ifilter-conceptual.md)

### <a name="other-samples"></a>Weitere Beispiele

[Suchen von Codebeispielen](-search-samples-ovw.md)
