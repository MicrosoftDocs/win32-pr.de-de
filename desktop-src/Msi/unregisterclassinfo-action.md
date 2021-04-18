---
description: Die unregisterclassinfo-Aktion verwaltet das Entfernen von COM-Klassen Informationen aus der Systemregistrierung. Es verwendet die AppID-Tabelle.
ms.assetid: 579a69ee-92cd-4d4c-a007-998ec042f9fc
title: Unregisterclassinfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ee701925e07e4f74439efb45da00d430d90304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350970"
---
# <a name="unregisterclassinfo-action"></a><span data-ttu-id="26223-104">Unregisterclassinfo-Aktion</span><span class="sxs-lookup"><span data-stu-id="26223-104">UnregisterClassInfo Action</span></span>

<span data-ttu-id="26223-105">Die unregisterclassinfo-Aktion verwaltet das Entfernen von COM-Klassen Informationen aus der Systemregistrierung.</span><span class="sxs-lookup"><span data-stu-id="26223-105">The UnregisterClassInfo action manages the removal of COM class information from the system registry.</span></span> <span data-ttu-id="26223-106">Es verwendet die [AppID-Tabelle](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="26223-106">It uses the [AppId table](appid-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="26223-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="26223-107">Sequence Restrictions</span></span>

<span data-ttu-id="26223-108">Die unregisterclassinfo-Aktion muss nach der [InstallInitialize](installinitialize-action.md) -Aktion und vor der [RegisterClassInfo](registerclassinfo-action.md) -Aktion erfolgen.</span><span class="sxs-lookup"><span data-stu-id="26223-108">The UnregisterClassInfo action must come after the [InstallInitialize](installinitialize-action.md) action and before the [RegisterClassInfo](registerclassinfo-action.md) action.</span></span>

<span data-ttu-id="26223-109">[Removeregistryvalues](removeregistryvalues-action.md) muss in der Sequenz vor ' unregisterclassinfo ' stehen.</span><span class="sxs-lookup"><span data-stu-id="26223-109">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterClassInfo in the sequence.</span></span>

<span data-ttu-id="26223-110">Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="26223-110">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="26223-111">Wenn eine Teilmenge dieser Aktionen in einer Sequenz Tabelle angezeigt wird, müssen Sie in derselben relativen Reihenfolge wie in der folgenden Tabelle vorkommen:</span><span class="sxs-lookup"><span data-stu-id="26223-111">If any subset of these actions occur together in a sequence table, they must occur in the same relative sequence as shown in the following table:</span></span>

-   <span data-ttu-id="26223-112">Unregisterclassinfo</span><span class="sxs-lookup"><span data-stu-id="26223-112">UnregisterClassInfo</span></span>
-   [<span data-ttu-id="26223-113">Unregisterextensioninfo</span><span class="sxs-lookup"><span data-stu-id="26223-113">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="26223-114">Unregisterprogidinfo</span><span class="sxs-lookup"><span data-stu-id="26223-114">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="26223-115">Unregistermimeinfo</span><span class="sxs-lookup"><span data-stu-id="26223-115">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="26223-116">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="26223-116">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="26223-117">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="26223-117">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="26223-118">Registerprogidinfo</span><span class="sxs-lookup"><span data-stu-id="26223-118">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="26223-119">Registermimeinfo</span><span class="sxs-lookup"><span data-stu-id="26223-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="26223-120">So muss z. b. [RegisterExtensionInfo](registerextensioninfo-action.md) in der Sequenz Tabelle vor unregisterclassinfo stehen.</span><span class="sxs-lookup"><span data-stu-id="26223-120">For example, [RegisterExtensionInfo](registerextensioninfo-action.md) must come before UnregisterClassInfo in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="26223-121">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="26223-121">ActionData Messages</span></span>



| <span data-ttu-id="26223-122">Feld</span><span class="sxs-lookup"><span data-stu-id="26223-122">Field</span></span> | <span data-ttu-id="26223-123">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="26223-123">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="26223-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="26223-124">\[1\]</span></span> | <span data-ttu-id="26223-125">GUID der nicht registrierten COM-Klasse.</span><span class="sxs-lookup"><span data-stu-id="26223-125">GUID of unregistered COM class.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="26223-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26223-126">Remarks</span></span>

<span data-ttu-id="26223-127">Der Installer legt die [**oleadvtsupport**](oleadvtsupport.md) -Eigenschaft auf true fest, wenn das System des aktuellen Benutzers aktualisiert wurde, um bei Bedarf über com installieren zu können.</span><span class="sxs-lookup"><span data-stu-id="26223-127">The installer sets the [**OLEAdvtSupport**](oleadvtsupport.md) property to true when the current user's system has been upgraded to work with install-on-demand through COM.</span></span> <span data-ttu-id="26223-128">Wenn das System die Installation von on-Demand über com nicht unterstützt, entfernt unregisterclassinfo alle in der [Klassen Tabelle](class-table.md) aufgeführten com-Klassen, die entweder den nicht installierten Features oder den von der Systemregistrierung installierten Funktionen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="26223-128">If the system does not support install-on-demand through COM, UnregisterClassInfo removes all COM classes listed in the [Class table](class-table.md) associated with either uninstalled features or features installed as advertised from the system registry.</span></span> <span data-ttu-id="26223-129">Andernfalls entfernt diese Aktion nur die com-Klassen, die den Funktionen zugeordnet sind, die für die Deinstallation aus der Systemregistrierung ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="26223-129">Otherwise, this action removes only the COM classes associated with features selected to be uninstalled from the system registry.</span></span>

 

 



