---
description: Zum Erstellen einer kompletten Liste der Volumes auf einem Computer oder zum Bearbeiten der einzelnen Volumes können Sie Volumes auflisten.
ms.assetid: 5adcd59a-48b7-4373-a10b-c352962f715a
title: Auflisten von Volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc294d72fa3fad24536b175ee7e5e023066586c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353561"
---
# <a name="enumerating-volumes"></a><span data-ttu-id="1189b-103">Auflisten von Volumes</span><span class="sxs-lookup"><span data-stu-id="1189b-103">Enumerating Volumes</span></span>

<span data-ttu-id="1189b-104">Zum Erstellen einer kompletten Liste der Volumes auf einem Computer oder zum Bearbeiten der einzelnen Volumes können Sie Volumes auflisten.</span><span class="sxs-lookup"><span data-stu-id="1189b-104">To make a complete list of the volumes on a computer, or to manipulate each volume in turn, you can enumerate volumes.</span></span> <span data-ttu-id="1189b-105">Innerhalb eines Volumes können Sie nach bereitgestellten [Ordnern](enumerating-volume-mount-points.md) oder anderen Objekten auf dem Volume suchen.</span><span class="sxs-lookup"><span data-stu-id="1189b-105">Within a volume, you can [scan for mounted folders](enumerating-volume-mount-points.md) or other objects on the volume.</span></span>

<span data-ttu-id="1189b-106">Mit drei Funktionen kann eine Anwendung Volumes auf einem Computer aufzählen:</span><span class="sxs-lookup"><span data-stu-id="1189b-106">Three functions allow an application to enumerate volumes on a computer:</span></span>

-   [<span data-ttu-id="1189b-107">**Findfirstvolume**</span><span class="sxs-lookup"><span data-stu-id="1189b-107">**FindFirstVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [<span data-ttu-id="1189b-108">**Findnextvolume**</span><span class="sxs-lookup"><span data-stu-id="1189b-108">**FindNextVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [<span data-ttu-id="1189b-109">**Findvolumeclose**</span><span class="sxs-lookup"><span data-stu-id="1189b-109">**FindVolumeClose**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)

<span data-ttu-id="1189b-110">Diese drei Funktionen funktionieren ähnlich wie die Funktionen " [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)", " [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)" und " [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) ".</span><span class="sxs-lookup"><span data-stu-id="1189b-110">These three functions operate in a manner very similar to the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span>

<span data-ttu-id="1189b-111">Beginnen Sie mit der Suche nach Volumes mit " [**findfirstvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)".</span><span class="sxs-lookup"><span data-stu-id="1189b-111">Begin a search for volumes with [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span></span> <span data-ttu-id="1189b-112">Wenn die Suche erfolgreich ist, verarbeiten Sie die Ergebnisse gemäß dem Design Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1189b-112">If the search is successful, process the results according to the design of your application.</span></span> <span data-ttu-id="1189b-113">Verwenden Sie dann [**findnextvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) in einer Schleife, um jedes nachfolgende Volume zu suchen und zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1189b-113">Then use [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) in a loop to locate and process each subsequent volume.</span></span> <span data-ttu-id="1189b-114">Wenn die Bereitstellung von Volumes erschöpft ist, schließen Sie die Suche mit [**findvolumeclose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).</span><span class="sxs-lookup"><span data-stu-id="1189b-114">When the supply of volumes is exhausted, close the search with [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).</span></span>

<span data-ttu-id="1189b-115">Sie sollten keine Korrelation zwischen der Reihenfolge der Volumes, die von diesen Funktionen zurückgegeben werden, und der Reihenfolge der Volumes annehmen, die von anderen Funktionen oder Tools zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1189b-115">You should not assume any correlation between the order of the volumes that are returned by these functions and the order of the volumes that are returned by other functions or tools.</span></span> <span data-ttu-id="1189b-116">Nehmen Sie insbesondere keine Korrelation zwischen der volumereihenfolge und den Laufwerk Buchstaben, die vom BIOS (sofern vorhanden) oder dem Datenträger Administrator zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="1189b-116">In particular, do not assume any correlation between volume order and drive letters as assigned by the BIOS (if any) or the Disk Administrator.</span></span>

<span data-ttu-id="1189b-117">Ein Beispiel für die Aufzählung der Volumes auf einem Computer finden Sie unter Beispiele für bereitgestellte [Ordner](volume-mount-point-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="1189b-117">See [Mounted Folder Examples](volume-mount-point-examples.md) for an example of how to enumerate the volumes on a computer.</span></span>

 

 



