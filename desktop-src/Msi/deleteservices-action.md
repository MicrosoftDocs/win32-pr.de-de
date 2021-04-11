---
description: Mit der Aktion "Delta Service" wird ein Dienst angehalten, und die Registrierung wird aus dem System entfernt. Durch diese Aktion wird die ServiceControl-Tabelle abgefragt.
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: Delta Service-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5fc22bbb0c11cd546f1ffbb9f3ad98e06efae3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346348"
---
# <a name="deleteservices-action"></a><span data-ttu-id="d5bca-104">Delta Service-Aktion</span><span class="sxs-lookup"><span data-stu-id="d5bca-104">DeleteServices Action</span></span>

<span data-ttu-id="d5bca-105">Mit der Aktion "Delta Service" wird ein Dienst angehalten, und die Registrierung wird aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="d5bca-105">The DeleteServices action stops a service and removes its registration from the system.</span></span> <span data-ttu-id="d5bca-106">Durch diese Aktion wird die [ServiceControl-Tabelle](servicecontrol-table.md)abgefragt.</span><span class="sxs-lookup"><span data-stu-id="d5bca-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d5bca-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="d5bca-107">Sequence Restrictions</span></span>

<span data-ttu-id="d5bca-108">Die Dienst Aktionen müssen in der folgenden Reihenfolge verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="d5bca-108">The services actions must be used in the following sequence:</span></span>

1.  [<span data-ttu-id="d5bca-109">Stop Services</span><span class="sxs-lookup"><span data-stu-id="d5bca-109">StopServices</span></span>](stopservices-action.md)
2.  <span data-ttu-id="d5bca-110">Delta Service Services</span><span class="sxs-lookup"><span data-stu-id="d5bca-110">DeleteServices</span></span>
3.  <span data-ttu-id="d5bca-111">Folgende Aktionen sind möglich: " [InstallFiles](installfiles-action.md)", " [RemoveFiles](removefiles-action.md)", " [duplicatefiles](duplicatefiles-action.md)", " [muvefiles](movefiles-action.md)", " [PATCHFILES](patchfiles-action.md)" und " [RemoveDuplicateFiles](removeduplicatefiles-action.md) ".</span><span class="sxs-lookup"><span data-stu-id="d5bca-111">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>
4.  [<span data-ttu-id="d5bca-112">Installservices-Aktion</span><span class="sxs-lookup"><span data-stu-id="d5bca-112">InstallServices action</span></span>](installservices-action.md)
5.  [<span data-ttu-id="d5bca-113">Startdienste</span><span class="sxs-lookup"><span data-stu-id="d5bca-113">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="d5bca-114">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="d5bca-114">ActionData Messages</span></span>



| <span data-ttu-id="d5bca-115">Feld</span><span class="sxs-lookup"><span data-stu-id="d5bca-115">Field</span></span> | <span data-ttu-id="d5bca-116">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="d5bca-116">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="d5bca-117">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d5bca-117">\[1\]</span></span> | <span data-ttu-id="d5bca-118">Dienst Anzeige Name.</span><span class="sxs-lookup"><span data-stu-id="d5bca-118">Service display name.</span></span>      |
| <span data-ttu-id="d5bca-119">\[2\]</span><span class="sxs-lookup"><span data-stu-id="d5bca-119">\[2\]</span></span> | <span data-ttu-id="d5bca-120">Dienstname</span><span class="sxs-lookup"><span data-stu-id="d5bca-120">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="d5bca-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5bca-121">Remarks</span></span>

<span data-ttu-id="d5bca-122">Diese Aktion erfordert, dass der Benutzer ein Administrator ist oder über erweiterte Berechtigungen mit der Berechtigung zum Löschen von Diensten verfügt oder dass die Anwendung Teil einer verwalteten Installation ist.</span><span class="sxs-lookup"><span data-stu-id="d5bca-122">This action requires the user be an administrator or have elevated privileges with permission to delete services or that the application be part of a managed installation.</span></span>

 

 



