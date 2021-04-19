---
description: Das ifiltersample-Codebeispiel veranschaulicht, wie eine IFilter-Basisklasse für die Implementierung der IFilter-Schnittstelle erstellt wird.
ms.assetid: 4c0df747-627d-4937-a117-d43137d5d081
title: Ifiltersample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f66bf32c4abe25038aa6b2a3b6d879ba65cf7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346077"
---
# <a name="ifiltersample"></a>Ifiltersample

Das ifiltersample-Codebeispiel veranschaulicht, wie eine IFilter-Basisklasse für die Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle erstellt wird.

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
| GitHub        | [Ifiltersample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)          |

> [!NOTE]  
> Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.

## <a name="building-the-sample"></a>Erstellen des Beispiels

1. Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **FilterBase** .
2. Doppelklicken Sie auf das Symbol für die Datei FilterBase. sln, um das Projekt in Visual Studio zu öffnen.

    > [!NOTE]  
    > Die SLN-Datei wurde mit einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen. Dies wirkt sich nicht auf das Verhalten des Beispiels aus.

3. Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1. Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2. Geben Sie an der Eingabeaufforderung ein, `FilterBase.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für FilterBase.exe.

## <a name="related-topics"></a>Zugehörige Themen

### <a name="reference"></a>Referenz

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)

### <a name="conceptual"></a>Konzept

[Entwickeln von Filter Handlern](-search-ifilter-conceptual.md)

### <a name="other-samples"></a>Weitere Beispiele

[Code Beispiele durchsuchen](-search-samples-ovw.md)
