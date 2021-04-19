---
description: Die Start Services-Aktion startet Systemdienste. Durch diese Aktion wird die ServiceControl-Tabelle abgefragt.
ms.assetid: 53791b1c-5fd5-45d8-817b-098566ab4f9c
title: StartServices-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c150a8970c5852d9cfc53581290e792c00b628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348309"
---
# <a name="startservices-action"></a><span data-ttu-id="d2ca9-104">StartServices-Aktion</span><span class="sxs-lookup"><span data-stu-id="d2ca9-104">StartServices Action</span></span>

<span data-ttu-id="d2ca9-105">Die Start Services-Aktion startet Systemdienste.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-105">The StartServices action starts system services.</span></span> <span data-ttu-id="d2ca9-106">Durch diese Aktion wird die [ServiceControl-Tabelle](servicecontrol-table.md)abgefragt.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d2ca9-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="d2ca9-107">Sequence Restrictions</span></span>

<span data-ttu-id="d2ca9-108">Die Dienst Aktionen müssen in der folgenden Reihenfolge verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="d2ca9-108">The services actions must be used in the following sequence:</span></span>

-   [<span data-ttu-id="d2ca9-109">Stop Services</span><span class="sxs-lookup"><span data-stu-id="d2ca9-109">StopServices</span></span>](stopservices-action.md)
-   [<span data-ttu-id="d2ca9-110">Delta Service Services</span><span class="sxs-lookup"><span data-stu-id="d2ca9-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="d2ca9-111">Eine der folgenden Aktionen:</span><span class="sxs-lookup"><span data-stu-id="d2ca9-111">Any of the following actions:</span></span>

-   [<span data-ttu-id="d2ca9-112">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="d2ca9-112">InstallFiles</span></span>](installfiles-action.md)
-   [<span data-ttu-id="d2ca9-113">RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="d2ca9-113">RemoveFiles</span></span>](removefiles-action.md)
-   [<span data-ttu-id="d2ca9-114">Duplicatefiles</span><span class="sxs-lookup"><span data-stu-id="d2ca9-114">DuplicateFiles</span></span>](duplicatefiles-action.md)
-   [<span data-ttu-id="d2ca9-115">"Muvefiles"</span><span class="sxs-lookup"><span data-stu-id="d2ca9-115">MoveFiles</span></span>](movefiles-action.md)
-   [<span data-ttu-id="d2ca9-116">Patchdateien</span><span class="sxs-lookup"><span data-stu-id="d2ca9-116">PatchFiles</span></span>](patchfiles-action.md)
-   [<span data-ttu-id="d2ca9-117">RemoveDuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="d2ca9-117">RemoveDuplicateFiles</span></span>](removeduplicatefiles-action.md)
-   [<span data-ttu-id="d2ca9-118">Installdienste</span><span class="sxs-lookup"><span data-stu-id="d2ca9-118">InstallServices</span></span>](installservices-action.md)
-   <span data-ttu-id="d2ca9-119">Startdienste</span><span class="sxs-lookup"><span data-stu-id="d2ca9-119">StartServices</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d2ca9-120">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="d2ca9-120">ActionData Messages</span></span>



| <span data-ttu-id="d2ca9-121">Feld</span><span class="sxs-lookup"><span data-stu-id="d2ca9-121">Field</span></span> | <span data-ttu-id="d2ca9-122">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="d2ca9-122">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="d2ca9-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d2ca9-123">\[1\]</span></span> | <span data-ttu-id="d2ca9-124">Dienst Anzeige Name.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-124">Service display name.</span></span>      |
| <span data-ttu-id="d2ca9-125">\[2\]</span><span class="sxs-lookup"><span data-stu-id="d2ca9-125">\[2\]</span></span> | <span data-ttu-id="d2ca9-126">Dienstname</span><span class="sxs-lookup"><span data-stu-id="d2ca9-126">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="d2ca9-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2ca9-127">Remarks</span></span>

<span data-ttu-id="d2ca9-128">Diese Aktion erfordert, dass der Benutzer ein Administrator ist oder über erweiterte Berechtigungen mit der Berechtigung zum Steuern von Diensten oder der Anwendung zu einer verwalteten Installation verfügt.</span><span class="sxs-lookup"><span data-stu-id="d2ca9-128">This action requires that the user be an administrator or have elevated privileges with permission to control services or that the application be part of a managed installation.</span></span>

 

 



