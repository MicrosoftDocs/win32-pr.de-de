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
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a><span data-ttu-id="e2247-103">Öffnen einer Stammansicht eines Verbindungspunkts durch eine Verknüpfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e2247-103">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>

<span data-ttu-id="e2247-104">Sie können eine Stammansicht eines Verbindungspunkts über eine [Verknüpfungsdatei](./links.md) zu diesem Verbindungspunkt starten.</span><span class="sxs-lookup"><span data-stu-id="e2247-104">You can launch a rooted view of a junction point through a [shortcut file](./links.md) to that junction point.</span></span>

## <a name="instructions"></a><span data-ttu-id="e2247-105">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="e2247-105">Instructions</span></span>


<span data-ttu-id="e2247-106">Legen Sie die Zielzeile der Verknüpfungsdatei auf Explorer.exe mit einem /root-Flag fest.</span><span class="sxs-lookup"><span data-stu-id="e2247-106">Set the shortcut file's Target line to Explorer.exe with a /root flag.</span></span> <span data-ttu-id="e2247-107">Die genaue Form des Befehls hängt vom Speicherort des Verbindungspunkts ab:</span><span class="sxs-lookup"><span data-stu-id="e2247-107">The exact form of the command depends on the location of the junction point:</span></span>

-   <span data-ttu-id="e2247-108">Wenn der Verbindungspunkt ein Unterordner des Desktops ist, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e2247-108">If the junction point is a subfolder of the Desktop, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   <span data-ttu-id="e2247-109">Wenn der Verbindungspunkt ein Dateisystemordner ist, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e2247-109">If the junction point is a file system folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   <span data-ttu-id="e2247-110">Wenn der Verbindungspunkt ein Unterordner eines virtuellen Systemordners ist, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e2247-110">If the junction point is a subfolder of a system virtual folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    <span data-ttu-id="e2247-111">Die virtuellen Systemordner, die Verknüpfungspunkte enthalten können, verfügen über die folgenden Klassenbezeichner (CLSIDs):</span><span class="sxs-lookup"><span data-stu-id="e2247-111">The system virtual folders that can contain junction points have the following class identifiers (CLSIDs):</span></span>

    

    | <span data-ttu-id="e2247-112">Systemordner</span><span class="sxs-lookup"><span data-stu-id="e2247-112">System folder</span></span>     | <span data-ttu-id="e2247-113">Klassen-ID</span><span class="sxs-lookup"><span data-stu-id="e2247-113">Class identifier</span></span>                       |
    |-------------------|----------------------------------------|
    | <span data-ttu-id="e2247-114">Arbeitsplatz</span><span class="sxs-lookup"><span data-stu-id="e2247-114">My Computer</span></span>       | <span data-ttu-id="e2247-115">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="e2247-115">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span></span> |
    | <span data-ttu-id="e2247-116">Meine Netzwerkorte</span><span class="sxs-lookup"><span data-stu-id="e2247-116">My Network Places</span></span> | <span data-ttu-id="e2247-117">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="e2247-117">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span></span> |
    | <span data-ttu-id="e2247-118">Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="e2247-118">Control Panel</span></span>     | <span data-ttu-id="e2247-119">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="e2247-119">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span></span> |
    | <span data-ttu-id="e2247-120">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="e2247-120">Internet Explorer</span></span> | <span data-ttu-id="e2247-121">{871C5380-42A0-1069-A2EA-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="e2247-121">{871C5380-42A0-1069-A2EA-08002B30309D}</span></span> |

    

     

## <a name="related-topics"></a><span data-ttu-id="e2247-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e2247-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2247-123">Angeben des Speicherorts einer Namespaceerweiterung</span><span class="sxs-lookup"><span data-stu-id="e2247-123">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="e2247-124">Öffnen einer Stammansicht eines Verbindungspunkts über die Registrierung</span><span class="sxs-lookup"><span data-stu-id="e2247-124">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 
