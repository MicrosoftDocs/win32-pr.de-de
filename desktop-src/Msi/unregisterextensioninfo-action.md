---
description: Mit der unregisterextensioninfo-Aktion wird das Entfernen von Erweiterungs bezogenen Informationen aus der Systemregistrierung verwaltet.
ms.assetid: 62bb9d17-c221-4bd2-bd7f-9930e28bb946
title: Unregisterextensioninfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d069a686c5f0e517a0cc9556634895216dd8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352791"
---
# <a name="unregisterextensioninfo-action"></a><span data-ttu-id="50dbf-103">Unregisterextensioninfo-Aktion</span><span class="sxs-lookup"><span data-stu-id="50dbf-103">UnregisterExtensionInfo Action</span></span>

<span data-ttu-id="50dbf-104">Mit der unregisterextensioninfo-Aktion wird das Entfernen von Erweiterungs bezogenen Informationen aus der Systemregistrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="50dbf-104">The UnregisterExtensionInfo action manages the removal of extension-related information from the system registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="50dbf-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="50dbf-105">Sequence Restrictions</span></span>

<span data-ttu-id="50dbf-106">Die unregisterextensioninfo-Aktion muss nach der [InstallInitialize](installinitialize-action.md) -Aktion und vor der [RegisterExtensionInfo](registerextensioninfo-action.md) -Aktion erfolgen.</span><span class="sxs-lookup"><span data-stu-id="50dbf-106">The UnregisterExtensionInfo action must come after the [InstallInitialize](installinitialize-action.md) action and before the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="50dbf-107">[Removeregistryvalues](removeregistryvalues-action.md) muss in der Sequenz vor ' unregisterextensioninfo ' stehen.</span><span class="sxs-lookup"><span data-stu-id="50dbf-107">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterExtensionInfo in the sequence.</span></span>

<span data-ttu-id="50dbf-108">Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="50dbf-108">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="50dbf-109">Wenn eine Teilmenge dieser Aktionen in einer Sequenz Tabelle enthalten ist, müssen Sie dieselbe relative Reihenfolge Reihenfolge aufweisen wie in der folgenden Abbildung:</span><span class="sxs-lookup"><span data-stu-id="50dbf-109">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="50dbf-110">Unregisterclassinfo</span><span class="sxs-lookup"><span data-stu-id="50dbf-110">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   <span data-ttu-id="50dbf-111">Unregisterextensioninfo</span><span class="sxs-lookup"><span data-stu-id="50dbf-111">UnregisterExtensionInfo</span></span>
-   [<span data-ttu-id="50dbf-112">Unregisterprogidinfo</span><span class="sxs-lookup"><span data-stu-id="50dbf-112">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="50dbf-113">Unregistermimeinfo</span><span class="sxs-lookup"><span data-stu-id="50dbf-113">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="50dbf-114">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="50dbf-114">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="50dbf-115">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="50dbf-115">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="50dbf-116">Registerprogidinfo</span><span class="sxs-lookup"><span data-stu-id="50dbf-116">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="50dbf-117">Registermimeinfo</span><span class="sxs-lookup"><span data-stu-id="50dbf-117">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="50dbf-118">Unregisterextensioninfo muss z. b. vor [unregisterprogidinfo](unregisterprogidinfo-action.md) in der Sequenz Tabelle stehen.</span><span class="sxs-lookup"><span data-stu-id="50dbf-118">For example, UnregisterExtensionInfo must come before [UnregisterProgIdInfo](unregisterprogidinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="50dbf-119">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="50dbf-119">ActionData Messages</span></span>



| <span data-ttu-id="50dbf-120">Feld</span><span class="sxs-lookup"><span data-stu-id="50dbf-120">Field</span></span> | <span data-ttu-id="50dbf-121">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="50dbf-121">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="50dbf-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="50dbf-122">\[1\]</span></span> | <span data-ttu-id="50dbf-123">Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="50dbf-123">Removed extension.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="50dbf-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50dbf-124">Remarks</span></span>

<span data-ttu-id="50dbf-125">Wenn das System die Bedarfs gesteuerte Installation von Erweiterungs Servern nicht unterstützt, entfernt unregisterextensioninfo alle Erweiterungs Server in der [Erweiterungs Tabelle](extension-table.md) , die entweder einer nicht installierten Funktion oder einem von der Registrierung installierten Feature zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="50dbf-125">If the system does not support the install-on-demand of extension servers, UnregisterExtensionInfo removes all extension servers in the [Extension table](extension-table.md) associated with either an uninstalled feature or a feature installed as advertised from the registry.</span></span> <span data-ttu-id="50dbf-126">Andernfalls entfernt diese Aktion die Erweiterungs Server, die einer Funktion zugeordnet sind, die aus der Registrierung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="50dbf-126">Otherwise, this action removes the extension servers associated with a feature that is selected to be removed from the registry.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50dbf-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="50dbf-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50dbf-128">**Shelladvtsupport (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="50dbf-128">**ShellAdvtSupport Property**</span></span>](shelladvtsupport.md)
</dt> </dl>

 

 



