---
title: Installieren des Online Store-Plug-in-Assistenten
description: Installieren des Online Store-Plug-in-Assistenten
ms.assetid: 75f7c279-4800-4146-8198-1dc76472237d
keywords:
- Windows Media Player Online Stores, Plug-ins
- Online Stores, Plug-ins
- Typ 1 Online Stores, Plug-ins
- Windows Media Player Online Stores, Plug-in-Assistent
- Online Stores, Plug-in-Assistent
- Typ 1 Online Stores, Plug-in-Assistent
- Windows Media Player Online Stores, Assistent zum Installieren von Plug-ins
- Online Stores, Assistent zum Installieren von Plug-ins
- Typ 1 Online Stores, Assistent zum Installieren von Plug-ins
- Plug-ins, Windows Media Player Online Stores
- Plug-ins, Online Stores
- Plug-ins, Typ 1 Online Stores
- Plug-ins, Installieren des Plug-in-Assistenten
- Plug-ins, Plug-in-Assistent
- Windows Media Player-Plug-ins, geben Sie 1 Online Stores ein.
- Windows Media Player-Plug-ins, Online Stores
- Windows Media Player-Plug-ins, Windows Media Player Online Stores
- Windows Media Player-Plug-ins, Installieren des Plug-in-Assistenten
- Windows Media Player-Plug-ins, Plug-in-Assistent
- Assistent zum Installieren von Plug-ins
- Plug-in-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d236c2160c5783f909430e6b49ef2e6361de22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037077"
---
# <a name="installing-the-online-store-plug-in-wizard"></a>Installieren des Online Store-Plug-in-Assistenten

Zum Einrichten der Entwicklungsumgebung für das Erstellen von 1-Online Store-Plug-Ins müssen Sie Folgendes installieren:

-   Microsoft Visual Studio 2005 oder höher
-   Windows Media Player 11 oder höher
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

    

    | Wert              | Visual Studio-Version |
    |--------------------|-----------------------|
    | VsWizardEngine. 8.0 | Visual Studio 2005    |
    | VsWizardEngine. 9.0 | Visual Studio 2008    |

    

     

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

[Entwickeln des Plug-Ins für einen Typ-1-Online Shop](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




