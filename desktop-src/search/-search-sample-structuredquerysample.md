---
description: Das Codebeispiel StructuredQuerySample veranschaulicht, wie Zeilen aus der Konsole gelesen, mithilfe des Systemschemas analysiert und die resultierenden Bedingungsstrukturen angezeigt werden.
ms.assetid: 9bb56d80-670e-4b2b-bf3f-40d0a75a89b6
title: StructuredQuerySample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab8f32a3ed58133893ed5c38c16c2ac242e9a28c6384a4e354bb6b0524c5a1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462575"
---
# <a name="structuredquerysample"></a>StructuredQuerySample

Das Codebeispiel StructuredQuerySample veranschaulicht, wie Zeilen aus der Konsole gelesen, mithilfe des Systemschemas analysiert und die resultierenden Bedingungsstrukturen angezeigt werden.

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
| GitHub        | [StructuredQuerySample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample)  |

> [!NOTE]  
> Für alle Versionen von Windows, einschließlich Windows 7, wird empfohlen, die Beispiele für die aktuelle Version direkt von GitHub herunterzuladen.

## <a name="building-the-sample"></a>Erstellen des Beispiels

1. Öffnen Windows Explorer, und navigieren Sie zum **Projektverzeichnis StructuredQuerySample.**
2. Doppelklicken Sie auf das Symbol für die Datei StructuredQuerySample.sln, um das Projekt in der Visual Studio.

    > [!NOTE]  
    > Die SLN-Datei wurde unter einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen. Dies wirkt sich nicht auf das Verhalten des Beispiels aus.

3. Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

1. Navigieren Sie zum Verzeichnis, das die neue ausführbare Datei enthält, indem Sie das Eingabeaufforderungsfenster oder den Windows verwenden.
2. Geben Sie an der Eingabeaufforderung ein, oder doppelklicken Sie im Windows Explorer auf das Symbol `StructuredQuerySample.exe` für StructuredQuerySample.exe.

## <a name="related-topics"></a>Zugehörige Themen

### <a name="reference"></a>Verweis

[**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)

[**ICondition2**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition2)

[**IConditionFactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory)

[**IConditionFactory2**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory2)

[**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)

[**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser)

[**IQueryParserManager**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparsermanager)

[**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)

### <a name="other-samples"></a>Weitere Beispiele

[Suchcodebeispiele](-search-samples-ovw.md)
