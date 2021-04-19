---
description: Mit der RegisterExtensionInfo-Aktion wird die Registrierung von Erweiterungs bezogenen Informationen im System verwaltet.
ms.assetid: 3c243ca3-9fa7-41ec-968e-7954d7d45432
title: RegisterExtensionInfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310344b6579ef65faac41238bb607ce98411b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348597"
---
# <a name="registerextensioninfo-action"></a><span data-ttu-id="ea5ef-103">RegisterExtensionInfo-Aktion</span><span class="sxs-lookup"><span data-stu-id="ea5ef-103">RegisterExtensionInfo Action</span></span>

<span data-ttu-id="ea5ef-104">Mit der RegisterExtensionInfo-Aktion wird die Registrierung von Erweiterungs bezogenen Informationen im System verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ea5ef-104">The RegisterExtensionInfo action manages the registration of extension related information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ea5ef-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="ea5ef-105">Sequence Restrictions</span></span>

<span data-ttu-id="ea5ef-106">Die Aktion RegisterExtensionInfo muss nach der Aktion [InstallFiles](installfiles-action.md) und der [unregisterextensioninfo](unregisterextensioninfo-action.md) -Aktion erfolgen.</span><span class="sxs-lookup"><span data-stu-id="ea5ef-106">The RegisterExtensionInfo action must come after the [InstallFiles](installfiles-action.md) action and the [UnregisterExtensionInfo](unregisterextensioninfo-action.md) action.</span></span>

<span data-ttu-id="ea5ef-107">Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="ea5ef-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="ea5ef-108">Wenn eine Teilmenge dieser Aktionen in einer Sequenz Tabelle enthalten ist, müssen Sie dieselbe relative Reihenfolge Reihenfolge aufweisen wie in der folgenden Abbildung:</span><span class="sxs-lookup"><span data-stu-id="ea5ef-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="ea5ef-109">Unregisterclassinfo</span><span class="sxs-lookup"><span data-stu-id="ea5ef-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="ea5ef-110">Unregisterextensioninfo</span><span class="sxs-lookup"><span data-stu-id="ea5ef-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="ea5ef-111">Unregisterprogidinfo</span><span class="sxs-lookup"><span data-stu-id="ea5ef-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="ea5ef-112">Unregistermimeinfo</span><span class="sxs-lookup"><span data-stu-id="ea5ef-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="ea5ef-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="ea5ef-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   <span data-ttu-id="ea5ef-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="ea5ef-114">RegisterExtensionInfo</span></span>
-   [<span data-ttu-id="ea5ef-115">Registerprogidinfo</span><span class="sxs-lookup"><span data-stu-id="ea5ef-115">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="ea5ef-116">Registermimeinfo</span><span class="sxs-lookup"><span data-stu-id="ea5ef-116">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="ea5ef-117">So muss z. b. RegisterExtensionInfo in der Sequenz Tabelle auf [unregistermimeinfo](unregistermimeinfo-action.md) folgen.</span><span class="sxs-lookup"><span data-stu-id="ea5ef-117">For example, RegisterExtensionInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ea5ef-118">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="ea5ef-118">ActionData Messages</span></span>



| <span data-ttu-id="ea5ef-119">Feld</span><span class="sxs-lookup"><span data-stu-id="ea5ef-119">Field</span></span> | <span data-ttu-id="ea5ef-120">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="ea5ef-120">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="ea5ef-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ea5ef-121">\[1\]</span></span> | <span data-ttu-id="ea5ef-122">Registrierte Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="ea5ef-122">Registered extension.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="ea5ef-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea5ef-123">Remarks</span></span>

<span data-ttu-id="ea5ef-124">Wenn das System die Installation bei Bedarf für Erweiterungs Server unterstützt, registriert RegisterExtensionInfo alle Erweiterungs Server in der [Erweiterungs Tabelle](extension-table.md) , die den Funktionen zugeordnet ist, die für die Installation oder Ankündigung festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="ea5ef-124">If the system supports installation-on-demand for extension servers, RegisterExtensionInfo registers all extension servers in the [Extension table](extension-table.md) associated with features set for installation or advertisement.</span></span> <span data-ttu-id="ea5ef-125">Andernfalls werden durch diese Aktion nur Erweiterungs Server registriert, die den Funktionen von zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="ea5ef-125">Otherwise this action only registers extension servers associated with features set to installation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea5ef-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ea5ef-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea5ef-127">**Shelladvtsupport (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="ea5ef-127">**ShellAdvtSupport property**</span></span>](shelladvtsupport.md)
</dt> </dl>

 

 



