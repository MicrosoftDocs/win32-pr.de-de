---
description: Das OpenSearch-Codebeispiel veranschaulicht, wie ein Verbund Suchdienst mithilfe des OpenSearch-Protokolls und einer OpenSearch-Deskriptor Datei (. OSDX) (Suchconnector) erstellt wird.
ms.assetid: 792884e4-826b-4474-82e1-1680d4d8b602
title: OpenSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8656efec434744d14714529d1e7b0d01a5349ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393458"
---
# <a name="opensearch"></a>OpenSearch

Das OpenSearch-Codebeispiel veranschaulicht, wie ein Verbund Suchdienst mithilfe des [OpenSearch](https://github.com/dewitt/opensearch) -Protokolls und einer OpenSearch-Deskriptor Datei (. OSDX) (Suchconnector) erstellt wird.

Dieses Thema enthält folgende Abschnitte:

-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="requirements"></a>Anforderungen



| Produkt     | Minimale Produkt Version |
|-------------|-------------------------|
| Windows     | Windows 7               |
| Windows SDK | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist in den folgenden Speicherorten verfügbar.



| Standort      | Pfad-URL                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [OpenSearch-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/OpenSearch)      |



 

 

> [!Note]  
> Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.

 

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel von der Eingabeaufforderung aus:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum **adventuresearch** -Projektverzeichnis. 
2.  Geben Sie `msbuild AdventureSearch.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum **adventuresearch** -Projektverzeichnis.
2.  Doppelklicken Sie auf das Symbol für die Datei "adventuresearch. sln", um das Projekt in Visual Studio zu öffnen.
    > [!Note]  
    > Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt. In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.

     

3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2.  Geben Sie an der Eingabeaufforderung ein, `AdventureSearch.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für AdventureSearch.exe.
3.  Geben Sie an der Eingabeaufforderung ein, `GetOSDX.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für GetOSDX.exe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Übersicht über das Suchconnector-Beschreibungs Schema](search-sconn-desc-schema-entry.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Verbundsuche in Windows 10](-search-federated-search-overview.md)
</dt> <dt>

[Code Beispiele durchsuchen](-search-samples-ovw.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Bibliotheks Beschreibungs Schema](../shell/library-schema-entry.md)
</dt> </dl>

 

 
