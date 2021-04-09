---
title: Einstieg in den Plug-in-Assistenten
description: Einstieg in den Plug-in-Assistenten
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Windows Media Player-Plug-ins, Installieren des Plug-in-Assistenten
- Plug-ins, Installieren des Plug-in-Assistenten
- aufbauen von Plug-ins, Installieren des Plug-in-Assistenten
- Windows Media Player-Plug-in-Assistent, installieren
- Assistent zum Installieren von Plug-ins
- Plug-in-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4feb9cfa60c120bfc5bb675ea8a8078b95ad14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947924"
---
# <a name="getting-started-with-the-plug-in-wizard"></a>Einstieg in den Plug-in-Assistenten

Zum Einrichten der Entwicklungsumgebung für das Erstellen von Windows Media Player-Plug-Ins müssen Sie Folgendes installieren:

-   Microsoft Visual Studio .NET 2003 oder höher
-   Windows Media Player 9-Serie oder höher
-   Windows SDK, einschließlich des Windows Media Player SDK
-   Windows Media Player-Plug-in-Assistent

## <a name="installing-the-wizard"></a>Installieren des Assistenten

Führen Sie die folgenden Schritte aus, um den Assistenten für Windows Media Player-Plug-in zu installieren.

1.  Suchen Sie den Ordner, in dem Sie den Windows SDK installiert haben. Erweitern Sie den Ordner, um die Unterordner anzuzeigen, und navigieren Sie zu Samples \\ Multimedia \\ WMP- \\ Assistenten \\ wmpwiz.
2.  Suchen Sie die folgenden drei Dateien:
    -   wmpwiz. VSZ
    -   wmpwiz. vsdir
    -   wmpwiz. ico
3.  Bearbeiten Sie die Datei wmpwiz. vsz mithilfe eines Text-Editors, z. b. Notepad.

    Suchen Sie die folgende Zeile:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Wechseln `<VsWizardEngine version goes here>` Sie abhängig von der installierten Version von Visual Studio zu einem der folgenden Werte.

    

    | Wert              | Visual Studio-Version   |
    |--------------------|-------------------------|
    | VsWizardEngine. 7.1 | Visual Studio .NET 2003 |
    | VsWizardEngine. 8.0 | Visual Studio 2005      |
    | VsWizardEngine. 9.0 | Visual Studio 2008      |

    

     

    Suchen Sie die folgende Zeile:

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    Wechseln `<path to wmpwiz directory goes here>` Sie zu dem Pfad, in dem sich die Assistenten Dateien befinden.

    Nehmen Sie beispielsweise an, Sie haben Visual Studio 2008, und ihre Assistenten Dateien sind hier: C: \\ Programme \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WMP Wizard \\ \\ wmpwiz. Die Datei "wmpwiz. VSZ" würde dann wie folgt aussehen:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Suchen Sie den Ordner, in dem Sie Visual Studio installiert haben. Erweitern Sie den Ordner, um die Unterordner anzuzeigen, und suchen Sie einen Ordner mit dem Namen vcprojects.
5.  Kopieren Sie die drei in Schritt 2 aufgeführten Dateien in den Ordner vcprojects. Der Assistent ist jetzt installiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufbauen eines Plug-ins](building-a-plug-in.md)
</dt> <dt>

[Verwenden des Plug-in-Assistenten in Visual Studio](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




