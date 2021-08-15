---
description: Im Codebeispiel SearchEvents wird veranschaulicht, wie Indizierungsereignisse priorisiert werden.
ms.assetid: a352c3e2-5860-4b9c-a3c7-a806f69b4f7d
title: SearchEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98f6687de8a9e4816968a3134abf76f8b10e02f42d90a2578626be035843621c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969709"
---
# <a name="searchevents"></a>SearchEvents

Im Codebeispiel SearchEvents wird veranschaulicht, wie Indizierungsereignisse priorisiert werden.

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
| GitHub        | [SearchEvents-Beispiel](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/SearchEvents)    |

> [!NOTE]  
> Für alle Versionen von Windows, einschließlich Windows 7, wird empfohlen, die Beispiele für die aktuelle Version direkt von GitHub herunterzuladen.

## <a name="building-the-sample"></a>Erstellen des Beispiels

1. Öffnen Windows Explorer, und navigieren Sie zum **Projektverzeichnis SearchEvents.**
2. Doppelklicken Sie auf das Symbol für die Datei Eventing.sln, um das Projekt in Visual Studio.
  
    > [!NOTE]  
    > Die SLN-Datei wurde unter einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen. Dies wirkt sich nicht auf das Verhalten des Beispiels aus.

3. Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

1. Navigieren Sie zum Verzeichnis, das die neue ausführbare Datei enthält, indem Sie das Eingabeaufforderungsfenster oder den Windows verwenden.
2. Geben Sie an der Eingabeaufforderung ein, oder doppelklicken Sie im Windows Explorer auf das Symbol `Eventing.exe` für Eventing.exe.

## <a name="related-topics"></a>Zugehörige Themen

### <a name="reference"></a>Verweis

[**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)

[**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)

[**\_PRIORITÄTSSTUFE**](/windows/win32/api/searchapi/ne-searchapi-priority_level)

[**ROWSETEVENT \_ ITEMSTATE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)

[**ROWSETEVENT-TYP \_**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

### <a name="other-samples"></a>Weitere Beispiele

[Suchcodebeispiele](-search-samples-ovw.md)
