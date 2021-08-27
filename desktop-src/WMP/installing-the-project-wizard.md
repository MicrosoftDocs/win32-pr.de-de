---
title: Installieren des Project-Assistenten
description: Installieren des Project-Assistenten
ms.assetid: bb27e5f0-d49e-46e5-a15f-be1a0a752c1c
keywords:
- Windows Media Player Onlineshops, Plug-Ins
- Onlineshops, Plug-Ins
- Geben Sie 2 Onlineshops und Plug-Ins ein.
- Windows Media Player Onlineshops, Plug-In-Assistent
- Onlineshops, Plug-In-Assistent
- Typ 2 Onlineshops, Plug-In-Assistent
- Windows Media Player Onlineshops, Projekt-Assistent
- Onlineshops, Projekt-Assistent
- Typ 2 Onlineshops, Projekt-Assistent
- Windows Media Player Onlineshops,Installations-Plug-In-Assistent
- Onlineshops, Plug-In-Assistent installieren
- Geben Sie 2 Onlineshops ein, und installieren Sie den Plug-In-Assistenten.
- Windows Media Player Onlineshops,Projektinstallations-Assistent
- Onlineshops,Projektinstallations-Assistent
- Typ 2 Onlineshops,Projektinstallations-Assistent
- Plug-Ins, Windows Media Player Onlineshops
- Plug-Ins, Onlineshops
- Plug-Ins, Geben Sie 2 Onlineshops ein.
- Plug-Ins, Plug-In-Assistent installieren
- Plug-Ins, Plug-In-Assistent
- Plug-Ins, Projektinstallations-Assistent
- Plug-Ins, Projekt-Assistent
- Windows Media Player Plug-Ins, geben Sie 2 Onlineshops ein.
- Windows Media Player Plug-Ins, Onlineshops
- Windows Media Player-Plug-Ins, Windows Media Player Onlineshops
- Windows Media Player-Plug-Ins,Installations-Plug-In-Assistent
- Windows Media Player Plug-Ins, Plug-In-Assistent
- Windows Media Player-Plug-Ins, Projektinstallations-Assistent
- Windows Media Player-Plug-Ins, Projekt-Assistent
- Installieren des Plug-In-Assistenten
- Plug-In-Assistent
- Projektinstallations-Assistent
- Projekt-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f00e0430791fb36285ba365eed752083889f2b55bd126c4a588d2a506f58acd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123520"
---
# <a name="installing-the-project-wizard"></a>Installieren des Project-Assistenten

Um Ihre Entwicklungsumgebung zum Erstellen von Plug-Ins vom Typ 2 für Onlineshops einzurichten, müssen Sie die folgenden Elemente installieren:

-   Microsoft Visual Studio .NET 2003 oder höher
-   Windows Media Player 9er Serie oder höher
-   Windows SDK, das das Windows Media Player SDK enthält
-   Assistent für Onlineshop-Plug-Ins

## <a name="installing-the-wizard"></a>Installieren des Assistenten

Verwenden Sie die folgenden Schritte, um den Assistenten für Onlineshop-Plug-Ins in Visual Studio zu installieren.

1.  Suchen Sie den Ordner, in dem Sie das Windows SDK installiert haben. Erweitern Sie den Ordner, um seine Unterordner anzuzeigen, und navigieren Sie zu Samples \\ Multimedia \\ WMP wizards services (Beispiele für WMP-Assistenten \\ für \\ Multimedia).
2.  Suchen Sie die folgenden drei Dateien:
    -   wmpservices.vsz
    -   wmpservices.vsdir
    -   wmpservices.ico
3.  Bearbeiten Sie die Datei wmpservices.vsz mithilfe eines Text-Editors wie Editor.

    Suchen Sie die folgende Zeile:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Ändern `<VsWizardEngine version goes here>` Sie in einen der folgenden Werte, je nachdem, welche Version von Visual Studio Sie installiert haben.

    

    | Wert              | Visual Studio-Version   |
    |--------------------|-------------------------|
    | VsWizardEngine.7.1 | Visual Studio .NET 2003 |
    | VsWizardEngine.8.0 | Visual Studio 2005      |
    | VsWizardEngine.9.0 | Visual Studio 2008      |

    

     

    Suchen Sie die folgende Zeile:

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    Ändern Sie `<path to wmpservices directory goes here>` in den Pfad, in dem sich die Assistentendateien befinden.

    Angenommen, Sie verfügen über Visual Studio 2008, und Ihre Assistentendateien befinden sich hier: C: \\ \\ Programme Microsoft SDKs Windows v7.0 Samples Multimedia WMP wizards services (C: Microsoft SDKs für Programmdateien \\ Windows \\ v7.0-Beispiele für \\ \\ \\ Multimedia-WMP-Assistentendienste). \\ \\ Die Datei wmpservices.vsz würde dann wie folgt aussehen:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Suchen Sie den Ordner, in dem Sie Visual Studio installiert haben. Erweitern Sie den Ordner, um seine Unterordner anzuzeigen, und suchen Sie nach einem Ordner mit dem Namen vcprojects.
5.  Kopieren Sie die drei in Schritt 2 aufgeführten Dateien in den Ordner vcprojects. Der Assistent ist jetzt installiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen des Plug-Ins für einen Typ 2 Online Store**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




