---
description: 'Das Codebeispiel "maxmatchingurls" veranschaulicht, wie drei Möglichkeiten zum Angeben der zu indizierenden Dateien bereitgestellt werden: URLs, die einem Dateityp, einem MIME-Typ oder einer angegebenen WHERE-Klausel entsprechen.'
ms.assetid: f7b3a8a6-b464-46d4-a99c-fc56eea9b1ec
title: Neu indiken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a7bb6ae3148f6969fc5349e1ebdf666a527282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484419"
---
# <a name="reindexmatchingurls"></a>Neu indiken

Das Codebeispiel "maxmatchingurls" veranschaulicht, wie drei Möglichkeiten zum Angeben der zu indizierenden Dateien bereitgestellt werden: URLs, die einem Dateityp, einem MIME-Typ oder einer angegebenen WHERE-Klausel entsprechen.

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

| Standort      | Pfad-URL                                                                      |
|---------------|-------------------------------------------------------------------------------|
| GitHub  | [Beispiel für "-xmatchingurls"](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/ReindexMatchingUrls) |

> [!NOTE]  
> Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.

## <a name="building-the-sample"></a>Erstellen des Beispiels

1. Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis " **mamatchingurls** ". Der vollständige Standard Installationspfad lautet beispielsweise `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls` .
2. Doppelklicken Sie auf das Symbol für die Datei REINDEX. sln, um das Projekt in Visual Studio zu öffnen.
  
    > [!NOTE]  
    > Die SLN-Datei wurde mit einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen. Dies wirkt sich nicht auf das Verhalten des Beispiels aus.

3. Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1. Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2. Geben Sie an der Eingabeaufforderung ein, `Reindex.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für Reindex.exe.

## <a name="related-topics"></a>Zugehörige Themen

### <a name="reference"></a>Referenz

[**Isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[**Isearchmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[**Isearchpersistentitemschangedsink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink)

[**Isearchviewchangedsink**](/windows/desktop/api/searchapi/nn-searchapi-isearchviewchangedsink)

[**Priorisieren von \_ Flags**](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)

### <a name="other-samples"></a>Weitere Beispiele

[Code Beispiele durchsuchen](-search-samples-ovw.md)
