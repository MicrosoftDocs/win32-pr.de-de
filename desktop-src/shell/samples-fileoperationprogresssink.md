---
description: Veranschaulicht, wie die IFileOperationProgressSink-Schnittstellenmethoden zum Überwachen der Details von IFileOperation-Schnittstellenaktionen verwendet werden.
title: Dateivorgangsfortschritt-Senke
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 196ABB75-1FE0-44f5-9060-59AAB4231567
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fe0ba5c86fdb2df5fe168559aa019941897563823e75670b0813ecb7e9e44d69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820350"
---
# <a name="file-operation-progress-sink"></a>Dateivorgangsfortschritt-Senke

Veranschaulicht, wie die [**IFileOperationProgressSink-Schnittstellenmethoden**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) zum Überwachen der Details von [**IFileOperation-Schnittstellenaktionen**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) verwendet werden.

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



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [FileOperationProgressSink-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/FileOperationProgressSink) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über das Eingabeaufforderungsfenster:

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum **Projektverzeichnis FileOperationProgressSink.**
2.  Geben Sie `msbuild FileOperationProgressSinkSample.sln` ein.

So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt):

1.  Öffnen Windows Explorer, und navigieren Sie zum **Projektverzeichnis FilesInUse.** Der vollständige Standardinstallationspfad ist beispielsweise `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample` .
2.  Doppelklicken Sie auf das Symbol für die Datei FileOperationProgressSinkSample.sln, um das Projekt in Visual Studio.
    > [!Note]  
    > Die Dateierweiterung SLN wird unter den Standardordnereinstellungen nicht angezeigt. In diesem Fall kann er anhand seines eindeutigen Symbols oder seiner Typbeschreibung "Microsoft Visual Studio identifiziert werden.

     

3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie zum Verzeichnis, das die neue ausführbare Datei enthält, indem Sie das Eingabeaufforderungsfenster oder den Windows verwenden.
2.  Geben Sie an der Eingabeaufforderung ein, oder doppelklicken Sie Windows Explorer auf das Symbol `FileOperationProgressSinkSample.exe` für FileOperationProgressSinkSample.exe.

 

 



