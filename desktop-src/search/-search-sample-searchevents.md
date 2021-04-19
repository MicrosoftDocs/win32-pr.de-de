---
description: Das searchevents-Codebeispiel veranschaulicht, wie Indizierungs Ereignisse priorisiert werden.
ms.assetid: a352c3e2-5860-4b9c-a3c7-a806f69b4f7d
title: Searchevents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21472d113694a41a3c7855c0fdaf8f2fa2b3b2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353027"
---
# <a name="searchevents"></a>Searchevents

Das searchevents-Codebeispiel veranschaulicht, wie Indizierungs Ereignisse priorisiert werden.

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
| GitHub        | [Searchevents-Beispiel](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/SearchEvents)    |

> [!NOTE]  
> Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.

## <a name="building-the-sample"></a>Erstellen des Beispiels

1. Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **searchevents** .
2. Doppelklicken Sie auf das Symbol für die Datei Eventing. sln, um das Projekt in Visual Studio zu öffnen.
  
    > [!NOTE]  
    > Die SLN-Datei wurde mit einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen. Dies wirkt sich nicht auf das Verhalten des Beispiels aus.

3. Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1. Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2. Geben Sie an der Eingabeaufforderung ein, `Eventing.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für Eventing.exe.

## <a name="related-topics"></a>Zugehörige Themen

### <a name="reference"></a>Referenz

[**IRow-tevents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)

[**Irowsetpriorisierung**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)

[**Prioritäts \_ Stufe**](/windows/win32/api/searchapi/ne-searchapi-priority_level)

[**rowevent- \_ Ausdruck ItemState**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)

[**rowsertevent- \_ Typ**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

### <a name="other-samples"></a>Weitere Beispiele

[Code Beispiele durchsuchen](-search-samples-ovw.md)
