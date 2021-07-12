---
description: Sie können eine Stammansicht eines Verbindungspunkts über eine Verknüpfungsdatei zu diesem Verbindungspunkt starten.
title: Öffnen einer Stammansicht eines Verbindungspunkts durch eine Verknüpfungsdatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52096f0dbbcebadb60e2612f0304ed497199b2ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581608"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a>Öffnen einer Stammansicht eines Verbindungspunkts durch eine Verknüpfungsdatei

Sie können eine Stammansicht eines Verbindungspunkts über eine [Verknüpfungsdatei](./links.md) zu diesem Verbindungspunkt starten.

## <a name="instructions"></a>Anweisungen


Legen Sie die Zielzeile der Verknüpfungsdatei auf Explorer.exe mit einem /root-Flag fest. Die genaue Form des Befehls hängt vom Speicherort des Verbindungspunkts ab:

-   Wenn der Verbindungspunkt ein Unterordner des Desktops ist, verwenden Sie Folgendes:

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   Wenn der Verbindungspunkt ein Dateisystemordner ist, verwenden Sie Folgendes:

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   Wenn der Verbindungspunkt ein Unterordner eines virtuellen Systemordners ist, verwenden Sie Folgendes:

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    Die virtuellen Systemordner, die Verknüpfungspunkte enthalten können, verfügen über die folgenden Klassenbezeichner (CLSIDs):

    

    | Systemordner     | Klassen-ID                       |
    |-------------------|----------------------------------------|
    | Arbeitsplatz       | {20D04FE0-3AEA-1069-A2D8-08002B30309D} |
    | Meine Netzwerkorte | {208D2C60-3AEA-1069-A2D7-08002B30309D} |
    | Systemsteuerung     | {21EC2020-3AEA-1069-A2DD-08002B30309D} |
    | Internet Explorer | {871C5380-42A0-1069-A2EA-08002B30309D} |

    

     

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Angeben des Speicherorts einer Namespaceerweiterung](nse-junction.md)
</dt> <dt>

[Öffnen einer Stammansicht eines Verbindungspunkts über die Registrierung](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 
