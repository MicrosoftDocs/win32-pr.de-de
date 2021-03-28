---
description: Veranschaulicht, wie das Dialogfeld "Datei in Verwendung" angepasst wird, um zusätzliche Informationen und Optionen für Dateien anzuzeigen, die zurzeit in der Anwendung geöffnet sind.
title: Datei wird verwendet (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 22EFE7CC-D223-46b3-BD6B-293E3FA0BA01
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 223e0addf201f3526654a17346963b4639e0d215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345928"
---
# <a name="file-is-in-use-sample"></a>Datei wird verwendet (Beispiel)

Veranschaulicht, wie das Dialogfeld " **Datei in Verwendung** " angepasst wird, um zusätzliche Informationen und Optionen für Dateien anzuzeigen, die zurzeit in der Anwendung geöffnet sind.

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



 

Weitere Anforderungen finden Sie in dersample.docx Datei "iatleisinuse", \_ die im Beispiel enthalten ist.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Beispiel für "fleisinuse"](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über das Eingabe Aufforderungs Fenster:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis " **fleisinuse** ".
2.  Geben Sie `msbuild FileIsInUse.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **FilesInUse** . Der vollständige Standard Installationspfad lautet beispielsweise `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse` .
2.  Doppelklicken Sie auf das Symbol für die Datei "Datei" "" ", um das Projekt in Visual Studio zu öffnen.
    > [!Note]  
    > Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt. In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.

     

3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2.  Geben Sie an der Eingabeaufforderung ein, `FileIsInUseSample.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für FileIsInUseSample.exe.

Ausführliche Informationen zu diesem Codebeispiel finden Sie in der Datei "ifleisinusesample.docx", \_ die im Beispiel enthalten ist.

 

 



