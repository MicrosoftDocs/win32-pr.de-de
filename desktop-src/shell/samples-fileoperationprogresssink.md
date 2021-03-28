---
description: Zeigt, wie die IFileOperationProgressSink-Schnittstellen Methoden zum Überwachen der Details von IFileOperation-Schnittstellen Aktionen verwendet werden.
title: Dateivorgangsfortschritt-Senke
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 196ABB75-1FE0-44f5-9060-59AAB4231567
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 60e3bde90da36a6122608b463b28df670f0d2a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042425"
---
# <a name="file-operation-progress-sink"></a>Dateivorgangsfortschritt-Senke

Zeigt, wie die [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) -Schnittstellen Methoden zum Überwachen der Details von [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) -Schnittstellen Aktionen verwendet werden.

Dieses Thema enthält folgende Abschnitte:

-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)

## <a name="requirements"></a>Requirements (Anforderungen)



| Produkt                                | Minimale Produkt Version |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 6.1                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [FileOperationProgressSink-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/FileOperationProgressSink) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über das Eingabe Aufforderungs Fenster:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **FileOperationProgressSink** .
2.  Geben Sie `msbuild FileOperationProgressSinkSample.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **FilesInUse** . Der vollständige Standard Installationspfad lautet beispielsweise `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample` .
2.  Doppelklicken Sie auf das Symbol für die Datei "FileOperationProgressSink Sample. sln", um das Projekt in Visual Studio zu öffnen.
    > [!Note]  
    > Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt. In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.

     

3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2.  Geben Sie an der Eingabeaufforderung ein, `FileOperationProgressSinkSample.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für FileOperationProgressSinkSample.exe.

 

 



