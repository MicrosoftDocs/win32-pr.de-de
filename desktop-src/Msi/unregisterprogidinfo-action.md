---
description: Mit der unregisterprogidinfo-Aktion wird die Aufhebung der Registrierung von OLE ProgID-Informationen beim System verwaltet.
ms.assetid: c9837845-4ffc-4496-8330-11b46d27ec7a
title: Unregisterprogidinfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff880c1d339fc3db3db50bd34d3afb828f65ec07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869036"
---
# <a name="unregisterprogidinfo-action"></a><span data-ttu-id="f4d87-103">Unregisterprogidinfo-Aktion</span><span class="sxs-lookup"><span data-stu-id="f4d87-103">UnregisterProgIdInfo Action</span></span>

<span data-ttu-id="f4d87-104">Mit der unregisterprogidinfo-Aktion wird die Aufhebung der Registrierung von OLE ProgID-Informationen beim System verwaltet.</span><span class="sxs-lookup"><span data-stu-id="f4d87-104">The UnregisterProgIdInfo action manages the unregistration of OLE ProgId information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="f4d87-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="f4d87-105">Sequence Restrictions</span></span>

<span data-ttu-id="f4d87-106">Die unregisterprogidinfo-Aktion muss nach der Aktion [InstallInitialize](installinitialize-action.md) , [unregisterclassinfo](unregisterclassinfo-action.md) Action, [unregisterextensioninfo](unregisterextensioninfo-action.md) und vor der [registerprogidinfo](registerprogidinfo-action.md) -Aktion erfolgen.</span><span class="sxs-lookup"><span data-stu-id="f4d87-106">The UnregisterProgIdInfo action must come after the [InstallInitialize](installinitialize-action.md) action, [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensioninfo](unregisterextensioninfo-action.md) action, and before the [RegisterProgIdInfo](registerprogidinfo-action.md) action.</span></span>

<span data-ttu-id="f4d87-107">[Removeregistryvalues](removeregistryvalues-action.md) muss in der Sequenz vor ' unregisterprogidinfo ' stehen.</span><span class="sxs-lookup"><span data-stu-id="f4d87-107">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterProgIdInfo in the sequence.</span></span>

<span data-ttu-id="f4d87-108">Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="f4d87-108">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="f4d87-109">Wenn eine Teilmenge dieser Aktionen in einer Sequenz Tabelle enthalten ist, müssen Sie dieselbe relative Reihenfolge Reihenfolge aufweisen wie in der folgenden Abbildung:</span><span class="sxs-lookup"><span data-stu-id="f4d87-109">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="f4d87-110">Unregisterclassinfo</span><span class="sxs-lookup"><span data-stu-id="f4d87-110">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="f4d87-111">Unregisterextensioninfo</span><span class="sxs-lookup"><span data-stu-id="f4d87-111">UnregisterExtensioninfo</span></span>](unregisterextensioninfo-action.md)
-   <span data-ttu-id="f4d87-112">Unregisterprogidinfo</span><span class="sxs-lookup"><span data-stu-id="f4d87-112">UnregisterProgIdInfo</span></span>
-   [<span data-ttu-id="f4d87-113">Unregistermimeinfo</span><span class="sxs-lookup"><span data-stu-id="f4d87-113">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="f4d87-114">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="f4d87-114">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="f4d87-115">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="f4d87-115">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="f4d87-116">Registerprogidinfo</span><span class="sxs-lookup"><span data-stu-id="f4d87-116">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="f4d87-117">Registermimeinfo</span><span class="sxs-lookup"><span data-stu-id="f4d87-117">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="f4d87-118">Beispielsweise muss unregisterprogidinfo vor [unregistermimeinfo](unregistermimeinfo-action.md) in der Sequenz Tabelle stehen.</span><span class="sxs-lookup"><span data-stu-id="f4d87-118">For example, UnregisterProgIdInfo must come before [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="f4d87-119">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="f4d87-119">ActionData Messages</span></span>



| <span data-ttu-id="f4d87-120">Feld</span><span class="sxs-lookup"><span data-stu-id="f4d87-120">Field</span></span> | <span data-ttu-id="f4d87-121">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="f4d87-121">Description of action data</span></span>                |
|-------|-------------------------------------------|
| <span data-ttu-id="f4d87-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="f4d87-122">\[1\]</span></span> | <span data-ttu-id="f4d87-123">Programm Bezeichner des registrierten Programms.</span><span class="sxs-lookup"><span data-stu-id="f4d87-123">Program identifier of registered program.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f4d87-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4d87-124">Remarks</span></span>

<span data-ttu-id="f4d87-125">Die unregisterprogidinfo-Aktion entfernt ProgID-Informationen aus der Registrierung ([ProgID-Tabelle](progid-table.md)) für Funktionen, die mit den Erweiterungs Informationen ([Erweiterungs Tabelle](extension-table.md)) oder den Klassen Informationen ([Klassen Tabelle](class-table.md)) verbunden sind und derzeit für die Deinstallation ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="f4d87-125">The UnregisterProgIdInfo action removes ProgId information from the registry ([ProgId Table](progid-table.md)) for features that are connected to the extension information ([Extension table](extension-table.md)) or the Class information ([Class table](class-table.md)) and are currently selected to be uninstalled.</span></span>

 

 



