---
description: Mit der registerprogidinfo-Aktion wird die Registrierung von OLE-ProgID-Informationen beim System verwaltet.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: Registerprogidinfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c7d53ca4c4125c6ebfc4d089c1c5a0934f9a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347566"
---
# <a name="registerprogidinfo-action"></a><span data-ttu-id="b5f10-103">Registerprogidinfo-Aktion</span><span class="sxs-lookup"><span data-stu-id="b5f10-103">RegisterProgIdInfo Action</span></span>

<span data-ttu-id="b5f10-104">Mit der registerprogidinfo-Aktion wird die Registrierung von OLE-ProgID-Informationen beim System verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b5f10-104">The RegisterProgIdInfo action manages the registration of OLE ProgId information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b5f10-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="b5f10-105">Sequence Restrictions</span></span>

<span data-ttu-id="b5f10-106">Die registerprogidinfo-Aktion muss nach der Aktion [InstallFiles](installfiles-action.md) , [unregisterprogidinfo](unregisterprogidinfo-action.md) Action, [RegisterClassInfo](registerclassinfo-action.md) und der [RegisterExtensionInfo](registerextensioninfo-action.md) -Aktion erfolgen.</span><span class="sxs-lookup"><span data-stu-id="b5f10-106">The RegisterProgIdInfo action must come after the [InstallFiles](installfiles-action.md) action, [UnregisterProgIdInfo](unregisterprogidinfo-action.md) action, [RegisterClassInfo](registerclassinfo-action.md) action, and the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="b5f10-107">Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="b5f10-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="b5f10-108">Wenn eine Teilmenge dieser Aktionen in einer Sequenz Tabelle enthalten ist, müssen Sie dieselbe relative Reihenfolge Reihenfolge aufweisen wie in der folgenden Abbildung:</span><span class="sxs-lookup"><span data-stu-id="b5f10-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="b5f10-109">Unregisterclassinfo</span><span class="sxs-lookup"><span data-stu-id="b5f10-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="b5f10-110">Unregisterextensioninfo</span><span class="sxs-lookup"><span data-stu-id="b5f10-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="b5f10-111">Unregisterprogidinfo</span><span class="sxs-lookup"><span data-stu-id="b5f10-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="b5f10-112">Unregistermimeinfo</span><span class="sxs-lookup"><span data-stu-id="b5f10-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="b5f10-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="b5f10-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="b5f10-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="b5f10-114">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   <span data-ttu-id="b5f10-115">Registerprogidinfo</span><span class="sxs-lookup"><span data-stu-id="b5f10-115">RegisterProgIdInfo</span></span>
-   [<span data-ttu-id="b5f10-116">Registermimeinfo</span><span class="sxs-lookup"><span data-stu-id="b5f10-116">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="b5f10-117">Registerprogidinfo muss z. b. nach [RegisterExtensionInfo](registerextensioninfo-action.md) in der Sequenz Tabelle stehen.</span><span class="sxs-lookup"><span data-stu-id="b5f10-117">For example, RegisterProgIdInfo must come after [RegisterExtensionInfo](registerextensioninfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b5f10-118">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="b5f10-118">ActionData Messages</span></span>



| <span data-ttu-id="b5f10-119">Feld</span><span class="sxs-lookup"><span data-stu-id="b5f10-119">Field</span></span> | <span data-ttu-id="b5f10-120">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="b5f10-120">Description of action data</span></span>                |
|-------|-------------------------------------------|
| <span data-ttu-id="b5f10-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="b5f10-121">\[1\]</span></span> | <span data-ttu-id="b5f10-122">Programm Bezeichner des registrierten Programms.</span><span class="sxs-lookup"><span data-stu-id="b5f10-122">Program identifier of registered program.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b5f10-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5f10-123">Remarks</span></span>

<span data-ttu-id="b5f10-124">Die registerprogidinfo-Aktion registriert alle ProgID-Informationen für Server, die in der [ProgID-Tabelle](progid-table.md) angegeben sind und für die der zugehörige Klassen Server oder Erweiterungs Server für die Installation ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f10-124">The RegisterProgIdInfo action registers all ProgId information for servers that are specified in the [ProgId table](progid-table.md) and for which the corresponding class server or extension server has been selected to be installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5f10-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b5f10-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5f10-126">Klassen Tabelle</span><span class="sxs-lookup"><span data-stu-id="b5f10-126">Class table</span></span>](class-table.md)
</dt> <dt>

[<span data-ttu-id="b5f10-127">Erweiterungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="b5f10-127">Extension table</span></span>](extension-table.md)
</dt> </dl>

 

 



