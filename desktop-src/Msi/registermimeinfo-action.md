---
description: Mit der registermimeinfo-Aktion werden MIME-bezogene Registrierungsinformationen beim System registriert.
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: Registermimeinfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41130d9e595cc2d95557470f79c217f3c3235d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756468"
---
# <a name="registermimeinfo-action"></a><span data-ttu-id="8705f-103">Registermimeinfo-Aktion</span><span class="sxs-lookup"><span data-stu-id="8705f-103">RegisterMIMEInfo Action</span></span>

<span data-ttu-id="8705f-104">Mit der registermimeinfo-Aktion werden MIME-bezogene Registrierungsinformationen beim System registriert.</span><span class="sxs-lookup"><span data-stu-id="8705f-104">The RegisterMIMEInfo action registers MIME-related registry information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8705f-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="8705f-105">Sequence Restrictions</span></span>

<span data-ttu-id="8705f-106">Die registermimeinfo-Aktion muss nach der [InstallFiles](installfiles-action.md) -Aktion, der [unregistermimeinfo](unregistermimeinfo-action.md) -Aktion, der [RegisterClassInfo](registerclassinfo-action.md) -Aktion und der [RegisterExtensionInfo](registerextensioninfo-action.md) -Aktion erfolgen.</span><span class="sxs-lookup"><span data-stu-id="8705f-106">The RegisterMIMEInfo action must come after the [InstallFiles](installfiles-action.md) action, [UnregisterMIMEInfo](unregistermimeinfo-action.md) action, [RegisterClassInfo](registerclassinfo-action.md) action, and the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="8705f-107">Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="8705f-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="8705f-108">Wenn eine Teilmenge dieser Aktionen in einer Sequenz Tabelle enthalten ist, müssen Sie dieselbe relative Reihenfolge Reihenfolge aufweisen wie in der folgenden Abbildung:</span><span class="sxs-lookup"><span data-stu-id="8705f-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="8705f-109">Unregisterclassinfo</span><span class="sxs-lookup"><span data-stu-id="8705f-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="8705f-110">Unregisterextensioninfo</span><span class="sxs-lookup"><span data-stu-id="8705f-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="8705f-111">Unregisterprogidinfo</span><span class="sxs-lookup"><span data-stu-id="8705f-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="8705f-112">Unregistermimeinfo</span><span class="sxs-lookup"><span data-stu-id="8705f-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="8705f-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="8705f-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="8705f-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="8705f-114">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="8705f-115">Registerprogidinfo</span><span class="sxs-lookup"><span data-stu-id="8705f-115">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   <span data-ttu-id="8705f-116">Registermimeinfo</span><span class="sxs-lookup"><span data-stu-id="8705f-116">RegisterMIMEInfo</span></span>

<span data-ttu-id="8705f-117">So muss z. b. registermimeinfo in der Sequenz Tabelle auf [unregistermimeinfo](unregistermimeinfo-action.md) folgen.</span><span class="sxs-lookup"><span data-stu-id="8705f-117">For example, RegisterMIMEInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="8705f-118">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="8705f-118">ActionData Messages</span></span>



| <span data-ttu-id="8705f-119">Feld</span><span class="sxs-lookup"><span data-stu-id="8705f-119">Field</span></span> | <span data-ttu-id="8705f-120">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="8705f-120">Description of action data</span></span>                   |
|-------|----------------------------------------------|
| <span data-ttu-id="8705f-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="8705f-121">\[1\]</span></span> | <span data-ttu-id="8705f-122">Der Bezeichner des registrierten MIME-Inhaltstyps.</span><span class="sxs-lookup"><span data-stu-id="8705f-122">Identifier of registered MIME content type.</span></span>  |
| <span data-ttu-id="8705f-123">\[2\]</span><span class="sxs-lookup"><span data-stu-id="8705f-123">\[2\]</span></span> | <span data-ttu-id="8705f-124">Erweiterung, die dem MIME-Inhaltstyp zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8705f-124">Extension associated with MIME content type.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8705f-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8705f-125">Remarks</span></span>

<span data-ttu-id="8705f-126">Mit der registermimeinfo-Aktion werden alle MIME-Informationen für Server aus der [MIME-Tabelle](mime-table.md) , für die der zugehörige Klassen Server oder Erweiterungs Server zur Installation ausgewählt wurde, registriert.</span><span class="sxs-lookup"><span data-stu-id="8705f-126">The RegisterMIMEInfo action registers all MIME information for servers from the [MIME table](mime-table.md) for which the corresponding class server or extension server has been selected to be installed.</span></span>

 

 



