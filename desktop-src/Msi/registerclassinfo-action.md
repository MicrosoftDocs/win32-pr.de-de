---
description: Mit der RegisterClassInfo-Aktion wird die Registrierung von COM-Klassen Informationen beim System verwaltet. Es verwendet die AppID-Tabelle.
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: RegisterClassInfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd916772bc236dfc86df336347514c10d5dfbce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373028"
---
# <a name="registerclassinfo-action"></a><span data-ttu-id="40599-104">RegisterClassInfo-Aktion</span><span class="sxs-lookup"><span data-stu-id="40599-104">RegisterClassInfo Action</span></span>

<span data-ttu-id="40599-105">Mit der RegisterClassInfo-Aktion wird die Registrierung von COM-Klassen Informationen beim System verwaltet.</span><span class="sxs-lookup"><span data-stu-id="40599-105">The RegisterClassInfo action manages the registration of COM class information with the system.</span></span> <span data-ttu-id="40599-106">Es verwendet die [AppID-Tabelle](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="40599-106">It uses the [AppId table](appid-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="40599-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="40599-107">Sequence Restrictions</span></span>

<span data-ttu-id="40599-108">Die RegisterClassInfo-Aktion muss nach der Aktion " [InstallFiles](installfiles-action.md) " und der Aktion " [unregisterclassinfo](unregisterclassinfo-action.md) " erfolgen.</span><span class="sxs-lookup"><span data-stu-id="40599-108">The RegisterClassInfo action must come after the [InstallFiles](installfiles-action.md) action and the [UnregisterClassInfo](unregisterclassinfo-action.md) action.</span></span>

<span data-ttu-id="40599-109">Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="40599-109">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="40599-110">Wenn eine Teilmenge dieser Aktionen in einer Sequenz Tabelle enthalten ist, müssen Sie dieselbe relative Reihenfolge Reihenfolge aufweisen wie in der folgenden Abbildung:</span><span class="sxs-lookup"><span data-stu-id="40599-110">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="40599-111">Unregisterclassinfo</span><span class="sxs-lookup"><span data-stu-id="40599-111">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="40599-112">Unregisterextensioninfo</span><span class="sxs-lookup"><span data-stu-id="40599-112">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="40599-113">Unregisterprogidinfo</span><span class="sxs-lookup"><span data-stu-id="40599-113">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="40599-114">Unregistermimeinfo</span><span class="sxs-lookup"><span data-stu-id="40599-114">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   <span data-ttu-id="40599-115">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="40599-115">RegisterClassInfo</span></span>
-   [<span data-ttu-id="40599-116">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="40599-116">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="40599-117">Registerprogidinfo</span><span class="sxs-lookup"><span data-stu-id="40599-117">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="40599-118">Registermimeinfo</span><span class="sxs-lookup"><span data-stu-id="40599-118">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="40599-119">So muss z. b. registerClassInfo in der Sequenz Tabelle auf [unregistermimeinfo](unregistermimeinfo-action.md) folgen.</span><span class="sxs-lookup"><span data-stu-id="40599-119">For example, RegisterClassInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="40599-120">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="40599-120">ActionData Messages</span></span>



| <span data-ttu-id="40599-121">Feld</span><span class="sxs-lookup"><span data-stu-id="40599-121">Field</span></span> | <span data-ttu-id="40599-122">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="40599-122">Description of action data</span></span>                          |
|-------|-----------------------------------------------------|
| <span data-ttu-id="40599-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="40599-123">\[1\]</span></span> | <span data-ttu-id="40599-124">GUID-Klassen Bezeichner des registrierten COM-Servers.</span><span class="sxs-lookup"><span data-stu-id="40599-124">GUID class identifier of the registered COM server.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="40599-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40599-125">Remarks</span></span>

<span data-ttu-id="40599-126">Wenn das System install-on-Demand für OLE-Server unterstützt, registriert RegisterClassInfo alle COM-Klassen in der [Klassen Tabelle](class-table.md) , die einer für die Installation oder Ankündigung ausgewählten Funktion zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="40599-126">If the system supports install-on-demand for OLE servers, RegisterClassInfo registers all COM classes in the [Class table](class-table.md) associated with a feature selected to be installed or advertised.</span></span> <span data-ttu-id="40599-127">Andernfalls werden durch diese Aktion nur die com-Klassen registriert, die einer für die Installation ausgewählten Funktion zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="40599-127">Otherwise this action only registers the COM classes associated with a feature selected for installation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40599-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="40599-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40599-129">**Oleadvtsupport (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="40599-129">**OLEAdvtSupport property**</span></span>](oleadvtsupport.md)
</dt> </dl>

 

 



