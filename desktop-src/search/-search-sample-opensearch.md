---
description: Im OpenSearch-Codebeispiel wird veranschaulicht, wie ein Verbundsuchdienst mithilfe des OpenSearch-Protokolls und einer OpenSearch-Deskriptordatei (OSDX)-Datei (einem Suchconnector) erstellt wird.
ms.assetid: 792884e4-826b-4474-82e1-1680d4d8b602
title: OpenSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6279b66be3b259058cc1b13bae6d9185e035211c65e87c21e070db638e74573
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118051840"
---
# <a name="opensearch"></a>OpenSearch

Im OpenSearch-Codebeispiel wird veranschaulicht, wie ein Verbundsuchdienst mithilfe des [OpenSearch-Protokolls](https://github.com/dewitt/opensearch) und einer OpenSearch-Deskriptordatei (OSDX)-Datei (einem Suchconnector) erstellt wird.

Dieses Thema enthält folgende Abschnitte:

-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="requirements"></a>Anforderungen



| Produkt     | Mindestproduktversion |
|-------------|-------------------------|
| Windows     | Windows 7               |
| Windows SDK | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist an den folgenden Speicherorten verfügbar.



| Standort      | Pfad-URL                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [OpenSearch Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/OpenSearch)      |



 

 

> [!Note]  
> Für alle Versionen von Windows, einschließlich Windows 7, wird empfohlen, die Beispiele für die aktuelle Version direkt von GitHub herunterzuladen.

 

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über die Eingabeaufforderung:

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum **AdventureSearch-Projektverzeichnis.** 
2.  Geben Sie `msbuild AdventureSearch.sln` ein.

So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt):

1.  Öffnen Windows Explorer, und navigieren Sie zum **AdventureSearch-Projektverzeichnis.**
2.  Doppelklicken Sie auf das Symbol für die Datei AdventureSearch.sln, um das Projekt in Visual Studio.
    > [!Note]  
    > Die Dateierweiterung SLN wird unter den Standardordnereinstellungen nicht angezeigt. In diesem Fall kann es durch sein eindeutiges Symbol oder durch seine Typbeschreibung identifiziert werden, "Microsoft Visual Studio Lösung".

     

3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie zum Verzeichnis, das die neue ausführbare Datei enthält, indem Sie das Eingabeaufforderungsfenster oder den Windows verwenden.
2.  Geben Sie an der Eingabeaufforderung ein, oder doppelklicken Sie im Windows Explorer auf das Symbol `AdventureSearch.exe` für AdventureSearch.exe.
3.  Geben Sie an der Eingabeaufforderung ein, oder doppelklicken Sie im Windows Explorer auf das Symbol `GetOSDX.exe` für GetOSDX.exe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Übersicht über das Suchconnector-Beschreibungsschema](search-sconn-desc-schema-entry.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Verbundsuche in Windows 10](-search-federated-search-overview.md)
</dt> <dt>

[Suchcodebeispiele](-search-samples-ovw.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Schema der Bibliotheksbeschreibung](../shell/library-schema-entry.md)
</dt> </dl>

 

 
