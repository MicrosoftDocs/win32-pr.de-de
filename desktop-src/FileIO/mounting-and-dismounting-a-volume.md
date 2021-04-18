---
description: Das Erstellen eines bereitgestellten Ordners ist ein zweistufiger Prozess.
ms.assetid: 02ecdf93-1133-48af-a6c9-52142256673f
title: Erstellen von bereitgestellten Ordnern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d64630716be6e85ac323c80e89dda0500ba6c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366223"
---
# <a name="creating-mounted-folders"></a><span data-ttu-id="1703c-103">Erstellen von bereitgestellten Ordnern</span><span class="sxs-lookup"><span data-stu-id="1703c-103">Creating Mounted Folders</span></span>

<span data-ttu-id="1703c-104">Das Erstellen eines bereitgestellten Ordners ist ein zweistufiger Prozess.</span><span class="sxs-lookup"><span data-stu-id="1703c-104">Creating a mounted folder is a two-step process.</span></span> <span data-ttu-id="1703c-105">Nennen Sie zuerst [**getvolumenameforvolumemountpoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) mit dem Bereitstellungspunkt (Laufwerksbuchstaben, VolumeGuid-Pfad oder eingebundenes Ordner) des Volumes, das dem bereitgestellten Ordner zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1703c-105">First, call [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) with the mount point (drive letter, volume GUID path, or mounted folder) of the volume to be assigned to the mounted folder.</span></span> <span data-ttu-id="1703c-106">Verwenden Sie dann die [**setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) -Funktion, um den zurückgegebenen Volume-GUID-Pfad dem gewünschten Verzeichnis auf einem anderen Volume zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="1703c-106">Then use the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function to associate the returned volume GUID path with the desired directory on another volume.</span></span> <span data-ttu-id="1703c-107">Beispielcode finden Sie unter [Erstellen eines eingebundenen Ordners](mounting-a-volume-at-a-mount-point.md).</span><span class="sxs-lookup"><span data-stu-id="1703c-107">For example code, see [Creating a Mounted Folder](mounting-a-volume-at-a-mount-point.md).</span></span>

<span data-ttu-id="1703c-108">Die Anwendung kann ein beliebiges leeres Verzeichnis auf einem anderen Volume als dem Stammverzeichnis als bereitgestellter Ordner festlegen.</span><span class="sxs-lookup"><span data-stu-id="1703c-108">Your application can designate any empty directory on a volume other than the root as a mounted folder.</span></span> <span data-ttu-id="1703c-109">Wenn Sie die [**setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) -Funktion aufrufen, wird dieses Verzeichnis zum bereitgestellten Ordner.</span><span class="sxs-lookup"><span data-stu-id="1703c-109">When you call the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, that directory becomes the mounted folder.</span></span> <span data-ttu-id="1703c-110">Sie können das gleiche Volume mehreren bereitgestellten Ordnern zuweisen.</span><span class="sxs-lookup"><span data-stu-id="1703c-110">You can assign the same volume to multiple mounted folders.</span></span>

<span data-ttu-id="1703c-111">Nachdem der bereitgestellte Ordner eingerichtet wurde, wird er über Computer Neustarts automatisch verwaltet.</span><span class="sxs-lookup"><span data-stu-id="1703c-111">After the mounted folder has been established, it is maintained through computer restarts automatically.</span></span>

<span data-ttu-id="1703c-112">Wenn ein Volume ausfällt, kann auf alle Volumes, die den bereitgestellten Ordnern auf diesem Volume zugewiesen wurden, nicht mehr über diese eingebundenen Ordner zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="1703c-112">If a volume fails, any volumes that have been assigned to mounted folders on that volume can no longer be accessed through those mounted folders.</span></span> <span data-ttu-id="1703c-113">Angenommen, Sie verfügen über zwei Volumes: c: und d:, und das Laufwerk d: ist dem bereitgestellten Ordner c: \\ mountd zugeordnet \\ .</span><span class="sxs-lookup"><span data-stu-id="1703c-113">For example, suppose you have two volumes, C: and D:, and that D: is associated with the mounted folder C:\\MountD\\.</span></span> <span data-ttu-id="1703c-114">Wenn das Volume "c:" ausfällt, kann auf Volume "D:" nicht mehr über den Pfad "c: mountd" zugegriffen werden \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="1703c-114">If volume C: fails, volume D: can no longer be accessed through the path C:\\MountD\\.</span></span>

<span data-ttu-id="1703c-115">Nur NTFS-Dateisystemvolumes können eingebundene Ordner enthalten, aber die Zielvolumes für die bereitgestellten Ordner können nicht-NTFS-Volumes sein.</span><span class="sxs-lookup"><span data-stu-id="1703c-115">Only NTFS file system volumes can have mounted folders, but the target volumes for the mounted folders can be non-NTFS volumes.</span></span>

<span data-ttu-id="1703c-116">Eingebundene Ordner werden mithilfe von Analyse Punkten implementiert und unterliegen ihren Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="1703c-116">Mounted folders are implemented by using reparse points and are subject to their restrictions.</span></span> <span data-ttu-id="1703c-117">Weitere Informationen finden Sie unter Analyse [Punkte](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="1703c-117">For more information, see [Reparse Points](reparse-points.md).</span></span> <span data-ttu-id="1703c-118">Es ist nicht erforderlich, Analyse Punkte für die Verwendung bereitgestellter Ordner zu manipulieren. Funktionen, wie z. b. [**setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , behandeln alle Analyse Punkt Details für Sie.</span><span class="sxs-lookup"><span data-stu-id="1703c-118">It is not necessary to manipulate reparse points to use mounted folders; functions such as [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) handle all the reparse point details for you.</span></span>

<span data-ttu-id="1703c-119">Da eingebundene Ordner Verzeichnisse sind, können Sie Sie wie andere Verzeichnisse umbenennen, entfernen, verschieben und anderweitig bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="1703c-119">Because mounted folders are directories, you can rename, remove, move, and otherwise manipulate them, as you would other directories.</span></span>

<span data-ttu-id="1703c-120">(Hinweis: in der TechNet-Dokumentation wird der Begriff bereitgestellte *Laufwerke* verwendet, um auf bereitgestellte *Ordner* zu verweisen.)</span><span class="sxs-lookup"><span data-stu-id="1703c-120">(Note: The TechNet documentation uses the term *mounted drives* to refer to *mounted folders*.)</span></span>

 

 



