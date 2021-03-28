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
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a><span data-ttu-id="4911f-103">Öffnen einer Stamm Ansicht eines Verknüpfungs Punkts durch eine Verknüpfungs Datei</span><span class="sxs-lookup"><span data-stu-id="4911f-103">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>

<span data-ttu-id="4911f-104">Sie können eine rootansicht eines Verknüpfungs Punkts durch eine Verknüpfungs [Datei](./links.md) zu diesem Verknüpfungs Punkt starten.</span><span class="sxs-lookup"><span data-stu-id="4911f-104">You can launch a rooted view of a junction point through a [shortcut file](./links.md) to that junction point.</span></span>

## <a name="instructions"></a><span data-ttu-id="4911f-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="4911f-105">Instructions</span></span>


<span data-ttu-id="4911f-106">Legen Sie die Zielzeile der Verknüpfungs Datei auf Explorer.exe mit einem/root-Flag fest.</span><span class="sxs-lookup"><span data-stu-id="4911f-106">Set the shortcut file's Target line to Explorer.exe with a /root flag.</span></span> <span data-ttu-id="4911f-107">Die genaue Form des Befehls hängt vom Speicherort des Verbindungs Punkts ab:</span><span class="sxs-lookup"><span data-stu-id="4911f-107">The exact form of the command depends on the location of the junction point:</span></span>

-   <span data-ttu-id="4911f-108">Wenn der Verknüpfungs Punkt ein Unterordner des Desktops ist, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4911f-108">If the junction point is a subfolder of the Desktop, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   <span data-ttu-id="4911f-109">Wenn der Verknüpfungs Punkt ein Dateisystem Ordner ist, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4911f-109">If the junction point is a file system folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   <span data-ttu-id="4911f-110">Wenn der Verknüpfungs Punkt ein Unterordner eines virtuellen System Ordners ist, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4911f-110">If the junction point is a subfolder of a system virtual folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    <span data-ttu-id="4911f-111">Die virtuellen Systemordner, die Verknüpfungs Punkte enthalten können, haben die folgenden Klassen Bezeichner (CLSIDs):</span><span class="sxs-lookup"><span data-stu-id="4911f-111">The system virtual folders that can contain junction points have the following class identifiers (CLSIDs):</span></span>

    

    |                   |                                        |
    |-------------------|----------------------------------------|
    | <span data-ttu-id="4911f-112">Arbeitsplatz</span><span class="sxs-lookup"><span data-stu-id="4911f-112">My Computer</span></span>       | <span data-ttu-id="4911f-113">{20d04fe0-3aea-1069-a2d8-08002b30309d}</span><span class="sxs-lookup"><span data-stu-id="4911f-113">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span></span> |
    | <span data-ttu-id="4911f-114">Meine Netzwerk Orte</span><span class="sxs-lookup"><span data-stu-id="4911f-114">My Network Places</span></span> | <span data-ttu-id="4911f-115">{208d2c60-3aea-1069-A2D7-08002b30309d}</span><span class="sxs-lookup"><span data-stu-id="4911f-115">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span></span> |
    | <span data-ttu-id="4911f-116">Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="4911f-116">Control Panel</span></span>     | <span data-ttu-id="4911f-117">{21ec2020-3aea-1069-A2DD-08002b30309d}</span><span class="sxs-lookup"><span data-stu-id="4911f-117">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span></span> |
    | <span data-ttu-id="4911f-118">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="4911f-118">Internet Explorer</span></span> | <span data-ttu-id="4911f-119">{871c5380-42a0-1069-a2ea-08002b30309d}</span><span class="sxs-lookup"><span data-stu-id="4911f-119">{871C5380-42A0-1069-A2EA-08002B30309D}</span></span> |

    

     

## <a name="related-topics"></a><span data-ttu-id="4911f-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4911f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4911f-121">Angeben des Speicher Orts der Namespace Erweiterung</span><span class="sxs-lookup"><span data-stu-id="4911f-121">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="4911f-122">Öffnen einer Stamm Ansicht eines Verknüpfungs Punkts durch die Registrierung</span><span class="sxs-lookup"><span data-stu-id="4911f-122">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 
