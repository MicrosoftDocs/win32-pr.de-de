---
title: Vorab Zuordnung des Speicherplatzes für die Erfassungs Datei
description: Vorab Zuordnung des Speicherplatzes für die Erfassungs Datei
ms.assetid: 7a11b769-65b9-4eaa-bc42-5d1d744bf181
keywords:
- WM_CAP_FILE_ALLOCATE Meldung
- capfilezuweisung-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7442b08170fb6f018555c043c59d96860701ed4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309855"
---
# <a name="disk-space-preallocation-for-the-capture-file"></a><span data-ttu-id="40dcb-105">Vorab Zuordnung des Speicherplatzes für die Erfassungs Datei</span><span class="sxs-lookup"><span data-stu-id="40dcb-105">Disk Space Preallocation for the Capture File</span></span>

<span data-ttu-id="40dcb-106">Durch die vorab Zuordnung von Speicherplatz für die Erfassungs Datei wird eine Datei mit einer angegebenen Größe auf dem Datenträger erstellt, bevor ein Aufzeichnungs Vorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="40dcb-106">Preallocating disk space for the capture file builds a file of a specified size on the disk before the start of a capture operation.</span></span> <span data-ttu-id="40dcb-107">Durch das vorab zuordnen einer Erfassungs Datei wird die während der Erfassung erforderliche Verarbeitung reduziert, und es werden weniger gelöschte Frames erzielt.</span><span class="sxs-lookup"><span data-stu-id="40dcb-107">Preallocating a capture file reduces the processing required while capture is in progress and results in fewer dropped frames.</span></span> <span data-ttu-id="40dcb-108">Sie können eine Aufzeichnungsdatei vorab zuordnen, indem Sie [**die \_ \_ Datei \_**](wm-cap-file-allocate.md) Zuordnungs Nachricht der WM-Abdeckung (oder das [**capfilealloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) -Makro) verwenden.</span><span class="sxs-lookup"><span data-stu-id="40dcb-108">You can preallocate a capture file by using the [**WM\_CAP\_FILE\_ALLOCATE**](wm-cap-file-allocate.md) message (or the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro).</span></span>

<span data-ttu-id="40dcb-109">In der Regel sollte Ihre Anwendung ausreichend Speicherplatz zuordnen, um die größte erwartete Erfassungs Datei zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="40dcb-109">Typically, your application should preallocate enough disk space to contain the largest capture file anticipated.</span></span> <span data-ttu-id="40dcb-110">Durch die vorab Zuordnung von Speicherplatz wird die Größe der erfassten Datei nicht eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="40dcb-110">Preallocating disk space does not restrict the size of the captured file.</span></span> <span data-ttu-id="40dcb-111">Die Dateigröße wird automatisch vergrößert, wenn die erfassten Daten den zugewiesenen Speicherplatz überschreiten.</span><span class="sxs-lookup"><span data-stu-id="40dcb-111">The file size is automatically enlarged if the captured data exceeds the allocated space.</span></span> <span data-ttu-id="40dcb-112">Bei nachfolgenden Schreibvorgängen in der Erfassungs Datei werden die für die Datei zugeordneten Teile des Speicherplatzes wieder verwendet, und die Größe und Fragmentierung der Datei werden beibehalten.</span><span class="sxs-lookup"><span data-stu-id="40dcb-112">Subsequent write operations to the capture file reuse the portions of disk space allocated for the file, preserving the size and fragmentation of the file.</span></span>

<span data-ttu-id="40dcb-113">Sie können die Erfassungs Leistung auch verbessern, indem Sie die Erfassungs Datei defragmentieren.</span><span class="sxs-lookup"><span data-stu-id="40dcb-113">You can also improve capture performance by defragmenting the capture file.</span></span> <span data-ttu-id="40dcb-114">Verwenden Sie zum Defragmentieren der Datei ein Defragmentierungsdienstprogramm, z. b. Datenträger Defragmentierung.</span><span class="sxs-lookup"><span data-stu-id="40dcb-114">To defragment the file, use a defragmentation utility such as Disk Defragmenter.</span></span> <span data-ttu-id="40dcb-115">Wenn Sie eine defragmentierte Erfassungs Datei verwenden und Sie später vergrößern, sollten Sie die erweiterte Datei defragmentieren.</span><span class="sxs-lookup"><span data-stu-id="40dcb-115">If you use a defragmented capture file and later enlarge it, you should defragment the enlarged file.</span></span> <span data-ttu-id="40dcb-116">Durch das Vergrößern einer defragmentierten Erfassungs Datei kann der erweiterte Teil der Datei fragmentiert und die Leistung beim Aufzeichnungs Vorgang reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="40dcb-116">Enlarging a defragmented capture file can fragment the expanded portion of the file and reduce performance in the capture operation.</span></span>

<span data-ttu-id="40dcb-117">Sie können die Leistung auch verbessern, indem Sie einen unkomprimierten Datenträger für die Video Erfassung verwenden.</span><span class="sxs-lookup"><span data-stu-id="40dcb-117">You might also improve performance by using an uncompressed disk for video capture.</span></span> <span data-ttu-id="40dcb-118">Durch das Komprimieren von Daten während der Erfassung kann der Aufzeichnungs Durchsatz auf den Datenträger beschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="40dcb-118">Compressing data during capture can limit capture throughput to the disk.</span></span>

<span data-ttu-id="40dcb-119">Eine Anwendung kann eine permanente Erfassungs Datei reservieren, um die erforderliche Zeit für das vorab zuordnen und Defragmentieren einer Datei zu vermeiden, wenn Sie gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="40dcb-119">An application can reserve a permanent capture file to eliminate the time required to preallocate and defragment a file each time it is started.</span></span> <span data-ttu-id="40dcb-120">Da eine Aufzeichnungsdatei beträchtlichen Speicherplatz erfordern kann und die vorab Zuordnung einer Erfassungs Datei alle Daten aus einer vorhandenen Erfassungs Datei entfernt, sollte eine Anwendung den Benutzer entscheiden können, ob die Datei permanent oder temporär ist.</span><span class="sxs-lookup"><span data-stu-id="40dcb-120">Because a capture file can require considerable disk space, and preallocating a capture file removes all data from an existing capture file, an application should let the user decide if the file is permanent or temporary.</span></span>

 

 




