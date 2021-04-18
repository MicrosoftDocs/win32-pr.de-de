---
description: Das Codebeispiel crawlscopecommandline veranschaulicht, wie Befehlszeilenoptionen für CSM-Indizierungs Vorgänge (Crawl Scope Manager) definiert werden.
ms.assetid: 8c82fe18-8676-43d2-a3da-027a733ee0a4
title: Crawlscopecommandline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eb770c44f82af320e2b39fe679b632cf03825e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344414"
---
# <a name="crawlscopecommandline"></a>Crawlscopecommandline

Das Codebeispiel crawlscopecommandline veranschaulicht, wie Befehlszeilenoptionen für CSM-Indizierungs Vorgänge (Crawl Scope Manager) definiert werden.

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

| Standort | Pfad oder URL                                                                |
|----------|----------------------------------------------------------------------------|
| GitHub   |    [Crawlscopecommandline-Beispiel](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/CrawlScopeCommandLine)|

> [!NOTE]  
> Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.

## <a name="building-the-sample"></a>Erstellen des Beispiels

1. Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **crawlscopecommandline** .
2. Doppelklicken Sie auf das Symbol für die Datei csmcmd. sln, um das Projekt in Visual Studio zu öffnen.
  
    > [!NOTE]  
    > Die SLN-Datei wurde mit einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen. Dies wirkt sich nicht auf das Verhalten des Beispiels aus.

3. Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1. Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2. Geben Sie an der Eingabeaufforderung ein, `csmcmd.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für csmcmd.exe.

## <a name="related-topics"></a>Zugehörige Themen

### <a name="reference"></a>Referenz

[**Ienumsearchroots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)

[**Ienumsearchscoperules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)

[**Isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)

[**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)

[**Isearchroot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)

[**Isearchscoperule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)

[**Isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[**Isearchmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

### <a name="other-samples"></a>Weitere Beispiele

[Code Beispiele durchsuchen](-search-samples-ovw.md)
