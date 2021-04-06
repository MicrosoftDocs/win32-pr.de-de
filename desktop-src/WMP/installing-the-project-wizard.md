---
title: Installieren des Projekt-Assistenten
description: Installieren des Projekt-Assistenten
ms.assetid: bb27e5f0-d49e-46e5-a15f-be1a0a752c1c
keywords:
- Windows Media Player Online Stores, Plug-ins
- Online Stores, Plug-ins
- Typ 2 Online Stores, Plug-ins
- Windows Media Player Online Stores, Plug-in-Assistent
- Online Stores, Plug-in-Assistent
- Typ 2 Online Stores, Plug-in-Assistent
- Windows Media Player Online Stores, Projekt-Assistent
- Online Stores, Projekt-Assistent
- Typ 2 Online Stores, Projekt-Assistent
- Windows Media Player Online Stores, Assistent zum Installieren von Plug-ins
- Online Stores, Assistent zum Installieren von Plug-ins
- Typ 2 Online Stores, Assistent zum Installieren von Plug-ins
- Windows Media Player Online Stores, Assistent zum Installieren von Projekten
- Online Stores, Assistent zum Installieren von Projekten
- Typ 2 Online Stores, Assistent zum Installieren von Projekten
- Plug-ins, Windows Media Player Online Stores
- Plug-ins, Online Stores
- Plug-ins, Typ 2 Online Stores
- Plug-ins, Installieren des Plug-in-Assistenten
- Plug-ins, Plug-in-Assistent
- Plug-ins, Assistent zum Installieren von Projekten
- Plug-ins, Projekt-Assistent
- Windows Media Player-Plug-ins, Typ 2 Online Stores
- Windows Media Player-Plug-ins, Online Stores
- Windows Media Player-Plug-ins, Windows Media Player Online Stores
- Windows Media Player-Plug-ins, Installieren des Plug-in-Assistenten
- Windows Media Player-Plug-ins, Plug-in-Assistent
- Windows Media Player-Plug-ins, Assistent zum Installieren von Projekten
- Windows Media Player-Plug-ins, Projekt-Assistent
- Assistent zum Installieren von Plug-ins
- Plug-in-Assistent
- Assistent zum Installieren von Projekten
- Projekt-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc37754a028d73114b1b425dcbc80e268559355d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711988"
---
# <a name="installing-the-project-wizard"></a>Installieren des Projekt-Assistenten

Zum Einrichten der Entwicklungsumgebung für das Erstellen von Type 2 Online Store-Plug-Ins müssen Sie Folgendes installieren:

-   Microsoft Visual Studio .NET 2003 oder höher
-   Windows Media Player 9-Serie oder höher
-   Windows SDK, einschließlich des Windows Media Player SDK
-   Plug-in-Assistent für Online Store

## <a name="installing-the-wizard"></a>Installieren des Assistenten

Führen Sie die folgenden Schritte aus, um den Online-Store-Plug-in-Assistenten in Visual Studio zu installieren.

1.  Suchen Sie den Ordner, in dem Sie den Windows SDK installiert haben. Erweitern Sie den Ordner, um die Unterordner anzuzeigen, und navigieren Sie zu Samples \\ Multimedia \\ WMP- \\ Assistenten \\ Dienste.
2.  Suchen Sie die folgenden drei Dateien:
    -   wmpservices. VSZ
    -   wmpservices. vsdir
    -   wmpservices. ico
3.  Bearbeiten Sie die Datei wmpservices. vsz mithilfe eines Text-Editors, z. b. Notepad.

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
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    Wechseln `<path to wmpservices directory goes here>` Sie zu dem Pfad, in dem sich die Assistenten Dateien befinden.

    Nehmen Sie beispielsweise an, Sie verfügen über Visual Studio 2008, und ihre Assistenten Dateien finden Sie hier: C: \\ Program Files \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WMP Wizard \\ \\ Services. Die Datei "wmpservices. VSZ" würde dann wie folgt aussehen:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Suchen Sie den Ordner, in dem Sie Visual Studio installiert haben. Erweitern Sie den Ordner, um die Unterordner anzuzeigen, und suchen Sie einen Ordner mit dem Namen vcprojects.
5.  Kopieren Sie die drei in Schritt 2 aufgeführten Dateien in den Ordner vcprojects. Der Assistent ist jetzt installiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Entwickeln des Plug-Ins für einen Typ 2-Online Store**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




