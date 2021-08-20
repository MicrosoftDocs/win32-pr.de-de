---
description: Veranschaulicht, wie das Dialogfeld "Datei wird verwendet" angepasst wird, um zusätzliche Informationen und Optionen für Dateien anzuzeigen, die derzeit in der Anwendung geöffnet sind.
title: Datei wird verwendet (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 22EFE7CC-D223-46b3-BD6B-293E3FA0BA01
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 27e0a216aed33d7b0295303539c6f46e489b4c4cba37fa7aedf0a7f2eddd7b60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968799"
---
# <a name="file-is-in-use-sample"></a>Datei wird verwendet (Beispiel)

Veranschaulicht, wie das Dialogfeld **"Datei wird verwendet"** angepasst wird, um zusätzliche Informationen und Optionen für Dateien anzuzeigen, die derzeit in der Anwendung geöffnet sind.

Dieses Thema enthält folgende Abschnitte:

-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)

## <a name="requirements"></a>Anforderungen



| Product (Produkt)                                | Mindestproduktversion |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 6.1                     |



 

Weitere Anforderungen finden Sie unter IFileIsInUse \_sample.docx im Beispiel enthaltene Datei.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [FileIsInUse-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über das Eingabeaufforderungsfenster:

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum **Projektverzeichnis FileIsInUse.**
2.  Geben Sie `msbuild FileIsInUse.sln` ein.

So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt):

1.  Öffnen Windows Explorer, und navigieren Sie zum **Projektverzeichnis FilesInUse.** Der vollständige Standardinstallationspfad ist beispielsweise `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse` .
2.  Doppelklicken Sie auf das Symbol für die Datei FileIsInUseSample.sln, um das Projekt in Visual Studio.
    > [!Note]  
    > Die Dateierweiterung SLN wird unter den Standardordnereinstellungen nicht angezeigt. In diesem Fall kann es durch sein eindeutiges Symbol oder durch seine Typbeschreibung identifiziert werden, "Microsoft Visual Studio Lösung".

     

3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie zum Verzeichnis, das die neue ausführbare Datei enthält, indem Sie das Eingabeaufforderungsfenster oder den Windows verwenden.
2.  Geben Sie an der Eingabeaufforderung ein, oder doppelklicken Sie im Windows Explorer auf das Symbol `FileIsInUseSample.exe` für FileIsInUseSample.exe.

Ausführliche Informationen zu diesem Codebeispiel finden Sie unter IFileIsInUsesample.docx \_ im Beispiel enthaltene Datei.

 

 



