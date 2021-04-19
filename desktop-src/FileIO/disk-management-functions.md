---
description: Funktionen, die in der Datenträgerverwaltung verwendet werden
ms.assetid: 301d3062-29a1-4b44-bbcd-e9d5b7d7823b
title: Funktionen der Datenträgerverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 677443c58aa8b9a60758d817e31e3804ef25ae66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364168"
---
# <a name="disk-management-functions"></a><span data-ttu-id="9730a-103">Funktionen der Datenträgerverwaltung</span><span class="sxs-lookup"><span data-stu-id="9730a-103">Disk Management Functions</span></span>

<span data-ttu-id="9730a-104">Die folgenden Funktionen werden in der Datenträgerverwaltung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9730a-104">The following functions are used in disk management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9730a-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9730a-105">In this section</span></span>



| <span data-ttu-id="9730a-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="9730a-106">Function</span></span>                                                    | <span data-ttu-id="9730a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9730a-107">Description</span></span>                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9730a-108">**GetDiskFreeSpace**</span><span class="sxs-lookup"><span data-stu-id="9730a-108">**GetDiskFreeSpace**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)<br/>     | <span data-ttu-id="9730a-109">Ruft Informationen zum angegebenen Datenträger ab, einschließlich der Menge an freiem Speicherplatz auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="9730a-109">Retrieves information about the specified disk, including the amount of free space on the disk.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="9730a-110">**GetDiskFreeSpaceEx**</span><span class="sxs-lookup"><span data-stu-id="9730a-110">**GetDiskFreeSpaceEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)<br/> | <span data-ttu-id="9730a-111">Ruft Informationen über den verfügbaren Speicherplatz auf einem Datenträger Volume ab, d. h. die Gesamtmenge des Speicherplatzes, die Gesamtmenge an freiem Speicherplatz und die Gesamtmenge des verfügbaren freien Speicherplatzes für den Benutzer, der dem aufrufenden Thread zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9730a-111">Retrieves information about the amount of space that is available on a disk volume, which is the total amount of space, the total amount of free space, and the total amount of free space available to the user that is associated with the calling thread.</span></span><br/> |



 

<span data-ttu-id="9730a-112">Andere Funktionen, die in der Datenträgerverwaltung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9730a-112">Other functions used in disk management.</span></span>



| <span data-ttu-id="9730a-113">Funktion</span><span class="sxs-lookup"><span data-stu-id="9730a-113">Function</span></span>                         | <span data-ttu-id="9730a-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9730a-114">Description</span></span>                                                                                                                                                                                                                        |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9730a-115">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="9730a-115">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) | <span data-ttu-id="9730a-116">Erstellt oder öffnet ein Datei-oder e/a-Gerät.</span><span class="sxs-lookup"><span data-stu-id="9730a-116">Creates or opens a file or I/O device.</span></span> <span data-ttu-id="9730a-117">Die am häufigsten verwendeten e/a-Geräte lauten wie folgt: Datei, Dateistream, Verzeichnis, physischer Datenträger, Volume, Konsolen Puffer, Bandlaufwerk, Kommunikations Ressource, Mailslot und Pipe.</span><span class="sxs-lookup"><span data-stu-id="9730a-117">The most commonly used I/O devices are as follows: file, file stream, directory, physical disk, volume, console buffer, tape drive, communications resource, mailslot, and pipe.</span></span><br/> |
| [<span data-ttu-id="9730a-118">**DeleteFile**</span><span class="sxs-lookup"><span data-stu-id="9730a-118">**DeleteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) | <span data-ttu-id="9730a-119">Löscht eine vorhandene Datei.</span><span class="sxs-lookup"><span data-stu-id="9730a-119">Deletes an existing file.</span></span><br/>                                                                                                                                                                                               |



 

 

 




