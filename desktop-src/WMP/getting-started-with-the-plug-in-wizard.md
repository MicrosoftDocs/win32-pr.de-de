---
title: Erste Schritte mit dem Plug-In-Assistenten
description: Erste Schritte mit dem Plug-In-Assistenten
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Windows Media Player Plug-Ins,Installieren des Plug-In-Assistenten
- Plug-Ins, Installieren des Plug-In-Assistenten
- Erstellen von Plug-Ins, Installieren des Plug-In-Assistenten
- Windows Media Player Plug-In-Assistent, Installieren
- Installieren des Plug-In-Assistenten
- Plug-In-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2699d0316be93f6387bdc64c6671df868eaa70fb24a4ad3619026524106432
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576579"
---
# <a name="getting-started-with-the-plug-in-wizard"></a>Erste Schritte mit dem Plug-In-Assistenten

Um Ihre Entwicklungsumgebung zum Erstellen von Windows Media Player-Plug-Ins einrichten zu können, müssen Sie die folgenden Elemente installieren:

-   Microsoft Visual Studio .NET 2003 oder höher
-   Windows Media Player 9er Serie oder höher
-   Windows SDK, das das Windows Media Player SDK enthält
-   Windows Media Player Plug-In-Assistent

## <a name="installing-the-wizard"></a>Installieren des Assistenten

Führen Sie die folgenden Schritte aus, um den Windows Media Player Plug-In-Assistenten zu installieren.

1.  Suchen Sie den Ordner, in dem Sie das Windows SDK installiert haben. Erweitern Sie den Ordner, um seine Unterordner zu sehen, und navigieren Sie zu \\ Samples Multimedia \\ WMP wizards wmpwiz (Beispiele für Multimedia-WMP-Assistenten \\ \\ wmpwiz).
2.  Suchen Sie die folgenden drei Dateien:
    -   wmpwiz.vsz
    -   wmpwiz.vsdir
    -   wmpwiz.ico
3.  Bearbeiten Sie die Datei "wmpwiz.vsz Editor mithilfe eines Text-Editors, z. B. Editor.

    Suchen Sie die folgende Zeile:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Ändern Sie in einen der folgenden Werte, je nachdem, welche Version Visual Studio `<VsWizardEngine version goes here>` installiert haben.

    

    | Wert              | Visual Studio-Version   |
    |--------------------|-------------------------|
    | VsWizardEngine.7.1 | Visual Studio .NET 2003 |
    | VsWizardEngine.8.0 | Visual Studio 2005      |
    | VsWizardEngine.9.0 | Visual Studio 2008      |

    

     

    Suchen Sie die folgende Zeile:

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    Wechseln `<path to wmpwiz directory goes here>` Sie in den Pfad, in dem sich die Assistentendateien befinden.

    Angenommen, Sie haben Visual Studio 2008, und Ihre Assistentendateien befinden sich hier: C: Programme \\ \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Multimedia \\ \\ WMP \\ wizards \\ wmpwiz. Ihre Datei "wmpwiz.vsz" würde dann wie die folgenden aussehen:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Suchen Sie den Ordner, in dem Sie Visual Studio. Erweitern Sie den Ordner, um seine Unterordner anzeigen zu können, und suchen Sie nach einem Ordner mit dem Namen vcprojects.
5.  Kopieren Sie die drei in Schritt 2 aufgeführten Dateien in den Ordner vcprojects. Der Assistent ist jetzt installiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Plug-Ins](building-a-plug-in.md)
</dt> <dt>

[Verwenden des Plug-In-Assistenten mit Visual Studio](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




