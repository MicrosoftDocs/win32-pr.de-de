---
description: Die unregistermimeinfo-Aktion hebt die Registrierung von MIME-bezogenen Registrierungsinformationen im System auf. Die-Aktion hebt die Registrierung von MIME-Informationen für Server aus der MIME-Tabelle auf, für die die entsprechende Funktion zurzeit zur Deinstallation ausgewählt ist.
ms.assetid: 9a5c12da-e78f-4c99-9b82-d41624593c61
title: Unregistermimeinfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02c1ca7c0cd12d9ec6236a0c0298ba793713f5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218673"
---
# <a name="unregistermimeinfo-action"></a><span data-ttu-id="f8a35-104">Unregistermimeinfo-Aktion</span><span class="sxs-lookup"><span data-stu-id="f8a35-104">UnregisterMIMEInfo Action</span></span>

<span data-ttu-id="f8a35-105">Die unregistermimeinfo-Aktion hebt die Registrierung von MIME-bezogenen Registrierungsinformationen im System auf.</span><span class="sxs-lookup"><span data-stu-id="f8a35-105">The UnregisterMIMEInfo action unregisters MIME-related registry information from the system.</span></span> <span data-ttu-id="f8a35-106">Die-Aktion hebt die Registrierung von MIME-Informationen für Server aus der [MIME-Tabelle](mime-table.md) auf, für die die entsprechende Funktion zurzeit zur Deinstallation ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="f8a35-106">The action unregisters MIME information for servers from the [MIME table](mime-table.md) for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="f8a35-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="f8a35-107">Sequence Restrictions</span></span>

<span data-ttu-id="f8a35-108">Die unregistermimeinfo-Aktion muss nach der [InstallInitialize](installinitialize-action.md) -Aktion, [unregisterclassinfo](unregisterclassinfo-action.md) Action, [unregisterextensioninfo](unregisterextensioninfo-action.md) Action und vor der [registermimeinfo](registermimeinfo-action.md) -Aktion erfolgen.</span><span class="sxs-lookup"><span data-stu-id="f8a35-108">The UnregisterMIMEInfo action must come after the [InstallInitialize](installinitialize-action.md) action, [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensionInfo](unregisterextensioninfo-action.md) action, and before the [RegisterMIMEInfo](registermimeinfo-action.md) action.</span></span>

<span data-ttu-id="f8a35-109">[Removeregistryvalues](removeregistryvalues-action.md) muss vor unregistermimeinfo in der Sequenz stehen.</span><span class="sxs-lookup"><span data-stu-id="f8a35-109">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterMIMEInfo in the sequence.</span></span>

<span data-ttu-id="f8a35-110">Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="f8a35-110">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="f8a35-111">Wenn eine Teilmenge dieser Aktionen in einer Sequenz Tabelle enthalten ist, müssen Sie dieselbe relative Reihenfolge Reihenfolge aufweisen wie in der folgenden Abbildung:</span><span class="sxs-lookup"><span data-stu-id="f8a35-111">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="f8a35-112">Unregisterclassinfo</span><span class="sxs-lookup"><span data-stu-id="f8a35-112">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="f8a35-113">Unregisterextensioninfo</span><span class="sxs-lookup"><span data-stu-id="f8a35-113">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="f8a35-114">Unregisterprogidinfo</span><span class="sxs-lookup"><span data-stu-id="f8a35-114">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   <span data-ttu-id="f8a35-115">Unregistermimeinfo</span><span class="sxs-lookup"><span data-stu-id="f8a35-115">UnregisterMIMEInfo</span></span>
-   [<span data-ttu-id="f8a35-116">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="f8a35-116">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="f8a35-117">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="f8a35-117">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="f8a35-118">Registerprogidinfo</span><span class="sxs-lookup"><span data-stu-id="f8a35-118">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="f8a35-119">Registermimeinfo</span><span class="sxs-lookup"><span data-stu-id="f8a35-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="f8a35-120">Beispielsweise muss unregistermimeinfo in der Sequenz Tabelle vor [RegisterExtensionInfo](registerextensioninfo-action.md) stehen.</span><span class="sxs-lookup"><span data-stu-id="f8a35-120">For example, UnregisterMIMEInfo must come before [RegisterExtensionInfo](registerextensioninfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="f8a35-121">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="f8a35-121">ActionData Messages</span></span>



| <span data-ttu-id="f8a35-122">Feld</span><span class="sxs-lookup"><span data-stu-id="f8a35-122">Field</span></span> | <span data-ttu-id="f8a35-123">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="f8a35-123">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="f8a35-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="f8a35-124">\[1\]</span></span> | <span data-ttu-id="f8a35-125">Der Bezeichner des nicht registrierten MIME-Inhaltstyps.</span><span class="sxs-lookup"><span data-stu-id="f8a35-125">Identifier of unregistered MIME content type.</span></span> |
| <span data-ttu-id="f8a35-126">\[2\]</span><span class="sxs-lookup"><span data-stu-id="f8a35-126">\[2\]</span></span> | <span data-ttu-id="f8a35-127">Erweiterung, die dem MIME-Inhaltstyp zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f8a35-127">Extension associated with MIME content type.</span></span>  |



 

 

 



