---
title: Installieren des Online Store-Plug-In-Assistenten
description: Installieren des Online Store-Plug-In-Assistenten
ms.assetid: 75f7c279-4800-4146-8198-1dc76472237d
keywords:
- Windows Media Player,Plug-Ins
- Onlineshops, Plug-Ins
- 'Typ 1: Onlineshops,Plug-Ins'
- Windows Media Player,Plug-In-Assistent
- Onlineshops,Plug-In-Assistent
- Geben Sie 1 Onlineshops,Plug-In-Assistent ein.
- Windows Media Player,Installieren des Plug-In-Assistenten
- Onlineshops,Installieren des Plug-In-Assistenten
- Geben Sie 1 Onlineshops ein, und installieren Sie den Plug-In-Assistenten.
- Plug-Ins, Windows Media Player Onlineshops
- Plug-Ins, Onlineshops
- Plug-Ins, Geben Sie 1 Onlineshops ein.
- Plug-Ins, Installieren des Plug-In-Assistenten
- Plug-Ins, Plug-In-Assistent
- Windows Media Player Plug-Ins geben Sie 1 Onlineshops ein.
- Windows Media Player-Plug-Ins, Onlineshops
- Windows Media Player-Plug-Ins, Windows Media Player Onlineshops
- Windows Media Player Plug-Ins,Installieren des Plug-In-Assistenten
- Windows Media Player Plug-Ins, Plug-In-Assistent
- Installieren des Plug-In-Assistenten
- Plug-In-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1088d915715be44de092604d626bc24792f6d263a9765a1076ce1afa3f67ef4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135543"
---
# <a name="installing-the-online-store-plug-in-wizard"></a>Installieren des Online Store-Plug-In-Assistenten

Um Ihre Entwicklungsumgebung für das Erstellen von Plug-Ins für den Typ 1 des Onlineshops einrichten zu können, müssen Sie die folgenden Elemente installieren:

-   Microsoft Visual Studio 2005 oder höher
-   Windows Media Player 11 oder höher
-   Windows SDK, das das Windows Media Player SDK enthält
-   Plug-In-Assistent für Onlineshops

## <a name="installing-the-wizard"></a>Installieren des Assistenten

Gehen Sie wie folgt vor, um den Plug-In-Assistenten für den Onlineshop in Visual Studio.

1.  Suchen Sie den Ordner, in dem Sie das Windows SDK installiert haben. Erweitern Sie den Ordner, um dessen Unterordner zu sehen, und navigieren Sie zu \\ Beispiele Multimedia \\ WMP wizards services (Beispiele für Multimedia-WMP-Assistentendienste). \\ \\
2.  Suchen Sie die folgenden drei Dateien:
    -   wmpservices.vsz
    -   wmpservices.vsdir
    -   wmpservices.ico
3.  Bearbeiten Sie die Datei "wmpservices.vsz" mithilfe eines Text-Editors wie Editor.

    Suchen Sie die folgende Zeile:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Ändern `<VsWizardEngine version goes here>` Sie in einen der folgenden Werte, je nachdem, welche Version Visual Studio installiert haben.

    

    | Wert              | Visual Studio-Version |
    |--------------------|-----------------------|
    | VsWizardEngine.8.0 | Visual Studio 2005    |
    | VsWizardEngine.9.0 | Visual Studio 2008    |

    

     

    Suchen Sie die folgende Zeile:

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    Wechseln `<path to wmpservices directory goes here>` Sie in den Pfad, in dem sich die Assistentendateien befinden.

    Angenommen, Sie haben Visual Studio 2008, und Ihre Assistentendateien befinden sich hier: C: Programme \\ \\ Microsoft SDKs Windows \\ \\ v7.0 Samples Multimedia \\ \\ \\ WMP \\ wizards services(C: Programme Microsoft SDKs Windows v7.0 Samples Multimedia WMP wizards \\ services). Ihre Datei wmpservices.vsz würde dann wie die folgenden aussehen:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Suchen Sie den Ordner, in dem Sie Visual Studio. Erweitern Sie den Ordner, um seine Unterordner anzeigen zu können, und suchen Sie nach einem Ordner mit dem Namen vcprojects.
5.  Kopieren Sie die drei in Schritt 2 aufgeführten Dateien in den Ordner vcprojects. Der Assistent ist jetzt installiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen des Plug-Ins für eine Online-Store](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




