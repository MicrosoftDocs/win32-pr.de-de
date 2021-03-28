---
description: Sie können eine rootansicht eines Verknüpfungs Punkts durch eine Verknüpfungs Datei zu diesem Verknüpfungs Punkt starten.
title: Öffnen einer Stamm Ansicht eines Verknüpfungs Punkts durch eine Verknüpfungs Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb83a6628b0dcffdf7d3bad66a25fc671c1feea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215936"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a>Öffnen einer Stamm Ansicht eines Verknüpfungs Punkts durch eine Verknüpfungs Datei

Sie können eine rootansicht eines Verknüpfungs Punkts durch eine Verknüpfungs [Datei](./links.md) zu diesem Verknüpfungs Punkt starten.

## <a name="instructions"></a>Instructions


Legen Sie die Zielzeile der Verknüpfungs Datei auf Explorer.exe mit einem/root-Flag fest. Die genaue Form des Befehls hängt vom Speicherort des Verbindungs Punkts ab:

-   Wenn der Verknüpfungs Punkt ein Unterordner des Desktops ist, verwenden Sie Folgendes:

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   Wenn der Verknüpfungs Punkt ein Dateisystem Ordner ist, verwenden Sie Folgendes:

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   Wenn der Verknüpfungs Punkt ein Unterordner eines virtuellen System Ordners ist, verwenden Sie Folgendes:

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    Die virtuellen Systemordner, die Verknüpfungs Punkte enthalten können, haben die folgenden Klassen Bezeichner (CLSIDs):

    

    |                   |                                        |
    |-------------------|----------------------------------------|
    | Arbeitsplatz       | {20d04fe0-3aea-1069-a2d8-08002b30309d} |
    | Meine Netzwerk Orte | {208d2c60-3aea-1069-A2D7-08002b30309d} |
    | Systemsteuerung     | {21ec2020-3aea-1069-A2DD-08002b30309d} |
    | Internet Explorer | {871c5380-42a0-1069-a2ea-08002b30309d} |

    

     

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Angeben des Speicher Orts der Namespace Erweiterung](nse-junction.md)
</dt> <dt>

[Öffnen einer Stamm Ansicht eines Verknüpfungs Punkts durch die Registrierung](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 
