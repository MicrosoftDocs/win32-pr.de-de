---
description: Die Stop Services-Aktion beendet Systemdienste. Durch diese Aktion wird die ServiceControl-Tabelle abgefragt.
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: Stop Services-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb271b99c434a1ac54ab9744697b991e9e1fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347253"
---
# <a name="stopservices-action"></a><span data-ttu-id="3aaa7-104">Stop Services-Aktion</span><span class="sxs-lookup"><span data-stu-id="3aaa7-104">StopServices Action</span></span>

<span data-ttu-id="3aaa7-105">Die Stop Services-Aktion beendet Systemdienste.</span><span class="sxs-lookup"><span data-stu-id="3aaa7-105">The StopServices action stops system services.</span></span> <span data-ttu-id="3aaa7-106">Durch diese Aktion wird die [ServiceControl-Tabelle](servicecontrol-table.md)abgefragt.</span><span class="sxs-lookup"><span data-stu-id="3aaa7-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="3aaa7-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="3aaa7-107">Sequence Restrictions</span></span>

<span data-ttu-id="3aaa7-108">Die Dienst Aktionen müssen in der folgenden Reihenfolge verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="3aaa7-108">The services actions must be used in the following sequence:</span></span>

-   <span data-ttu-id="3aaa7-109">Stop Services</span><span class="sxs-lookup"><span data-stu-id="3aaa7-109">StopServices</span></span>
-   [<span data-ttu-id="3aaa7-110">Delta Service Services</span><span class="sxs-lookup"><span data-stu-id="3aaa7-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="3aaa7-111">Eine der folgenden Aktionen:</span><span class="sxs-lookup"><span data-stu-id="3aaa7-111">Any of the following actions:</span></span>

-   [<span data-ttu-id="3aaa7-112">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="3aaa7-112">InstallFiles</span></span>](installfiles-action.md)
-   [<span data-ttu-id="3aaa7-113">RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="3aaa7-113">RemoveFiles</span></span>](removefiles-action.md)
-   [<span data-ttu-id="3aaa7-114">Duplicatefiles</span><span class="sxs-lookup"><span data-stu-id="3aaa7-114">DuplicateFiles</span></span>](duplicatefiles-action.md)
-   [<span data-ttu-id="3aaa7-115">"Muvefiles"</span><span class="sxs-lookup"><span data-stu-id="3aaa7-115">MoveFiles</span></span>](movefiles-action.md)
-   [<span data-ttu-id="3aaa7-116">Patchdateien</span><span class="sxs-lookup"><span data-stu-id="3aaa7-116">PatchFiles</span></span>](patchfiles-action.md)
-   [<span data-ttu-id="3aaa7-117">RemoveDuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="3aaa7-117">RemoveDuplicateFiles</span></span>](removeduplicatefiles-action.md)
-   [<span data-ttu-id="3aaa7-118">Installdienste</span><span class="sxs-lookup"><span data-stu-id="3aaa7-118">InstallServices</span></span>](installservices-action.md)
-   [<span data-ttu-id="3aaa7-119">Startdienste</span><span class="sxs-lookup"><span data-stu-id="3aaa7-119">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="3aaa7-120">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="3aaa7-120">ActionData Messages</span></span>



| <span data-ttu-id="3aaa7-121">Feld</span><span class="sxs-lookup"><span data-stu-id="3aaa7-121">Field</span></span> | <span data-ttu-id="3aaa7-122">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="3aaa7-122">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="3aaa7-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="3aaa7-123">\[1\]</span></span> | <span data-ttu-id="3aaa7-124">Dienst Anzeige Name.</span><span class="sxs-lookup"><span data-stu-id="3aaa7-124">Service display name.</span></span>      |
| <span data-ttu-id="3aaa7-125">\[2\]</span><span class="sxs-lookup"><span data-stu-id="3aaa7-125">\[2\]</span></span> | <span data-ttu-id="3aaa7-126">Dienstname</span><span class="sxs-lookup"><span data-stu-id="3aaa7-126">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="3aaa7-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3aaa7-127">Remarks</span></span>

<span data-ttu-id="3aaa7-128">Diese Aktion erfordert, dass der Benutzer ein Administrator ist oder über erweiterte Berechtigungen mit der Berechtigung zum Steuern von Diensten oder der Anwendung zu einer verwalteten Installation verfügt.</span><span class="sxs-lookup"><span data-stu-id="3aaa7-128">This action requires that the user be an administrator or have elevated privileges with permission to control services or that the application be part of a managed installation.</span></span>

 

 



