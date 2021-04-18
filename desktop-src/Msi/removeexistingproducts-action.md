---
description: Die Aktion "RemoveExistingProducts" durchläuft die in der Spalte "action Property" der upgradetabelle aufgeführten Produktcodes und entfernt die Produkte nacheinander, indem parallele Installationen aufgerufen werden.
ms.assetid: 3e96283b-1085-4ace-b004-2fd94310eeb2
title: RemoveExistingProducts-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea3b792b02352277e8f29fa422b093fe876b560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351693"
---
# <a name="removeexistingproducts-action"></a><span data-ttu-id="6a263-103">RemoveExistingProducts-Aktion</span><span class="sxs-lookup"><span data-stu-id="6a263-103">RemoveExistingProducts Action</span></span>

<span data-ttu-id="6a263-104">Die Aktion "RemoveExistingProducts" durchläuft die in der Spalte "action Property" der [upgradetabelle](upgrade-table.md) aufgeführten Produktcodes und entfernt die Produkte nacheinander, indem parallele Installationen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6a263-104">The RemoveExistingProducts action goes through the product codes listed in the ActionProperty column of the [Upgrade table](upgrade-table.md) and removes the products in sequence by invoking concurrent installations.</span></span> <span data-ttu-id="6a263-105">Der Installer legt für jede gleichzeitige Installation die [**ProductCode**](productcode.md) -Eigenschaft auf den Produktcode fest und legt die [**Remove**](remove.md) -Eigenschaft auf den Wert im Feld entfernen der upgradetabelle fest.</span><span class="sxs-lookup"><span data-stu-id="6a263-105">For each concurrent installation the installer sets the [**ProductCode**](productcode.md) property to the product code and sets the [**REMOVE**](remove.md) property to the value in the Remove field of the Upgrade table.</span></span> <span data-ttu-id="6a263-106">Wenn das Feld entfernen leer ist, lautet der Wert standardmäßig alle, und das Installationsprogramm entfernt das gesamte Produkt.</span><span class="sxs-lookup"><span data-stu-id="6a263-106">If the Remove field is blank, its value defaults to ALL and the installer removes the entire product.</span></span>

<span data-ttu-id="6a263-107">Der Installer führt die Aktion RemoveExistingProducts nur bei der erstmaligen Installation eines Produkts aus.</span><span class="sxs-lookup"><span data-stu-id="6a263-107">The installer only runs the RemoveExistingProducts action the first time it installs a product.</span></span> <span data-ttu-id="6a263-108">Die Aktion wird während einer [Wartungs Installation](maintenance-installation.md) oder-Installation nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a263-108">It does not run the action during a [maintenance installation](maintenance-installation.md) or uninstallation.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="6a263-109">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="6a263-109">Sequence Restrictions</span></span>

<span data-ttu-id="6a263-110">Die Aktion "RemoveExistingProducts" muss in der Aktions Sequenz an einem der folgenden Speicherorte geplant werden.</span><span class="sxs-lookup"><span data-stu-id="6a263-110">The RemoveExistingProducts action must be scheduled in the action sequence in one of the following locations.</span></span>

-   <span data-ttu-id="6a263-111">Zwischen der [InstallValidate-Aktion](installvalidate-action.md) und der [InstallInitialize-Aktion](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="6a263-111">Between the [InstallValidate action](installvalidate-action.md) and the [InstallInitialize action](installinitialize-action.md).</span></span> <span data-ttu-id="6a263-112">In diesem Fall entfernt das Installationsprogramm die alten Anwendungen vollständig, bevor die neuen Anwendungen installiert werden.</span><span class="sxs-lookup"><span data-stu-id="6a263-112">In this case, the installer removes the old applications entirely before installing the new applications.</span></span> <span data-ttu-id="6a263-113">Dies ist eine ineffiziente Platzierung für die Aktion, da alle wiederverwendeten Dateien neu kopiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="6a263-113">This is an inefficient placement for the action because all reused files have to be recopied.</span></span>
-   <span data-ttu-id="6a263-114">Nach der [InstallInitialize-Aktion](installinitialize-action.md) und vor den Aktionen, mit denen Ausführungs Skript generiert wird.</span><span class="sxs-lookup"><span data-stu-id="6a263-114">After the [InstallInitialize action](installinitialize-action.md) and before any actions that generate execution script.</span></span>
-   <span data-ttu-id="6a263-115">Zwischen der [InstallExecute-Aktion](installexecute-action.md)oder der [InstallExecuteAgain](installexecuteagain-action.md)-Aktion und der [InstallFinalize](installfinalize-action.md)-Aktion.</span><span class="sxs-lookup"><span data-stu-id="6a263-115">Between the [InstallExecute action](installexecute-action.md), or the [InstallExecuteAgain action](installexecuteagain-action.md), and the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="6a263-116">Im Allgemeinen werden die letzten drei Aktionen direkt aufeinander geplant: InstallExecute, RemoveExistingProducts und InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="6a263-116">Generally the last three actions are scheduled right after one another: InstallExecute, RemoveExistingProducts, and InstallFinalize.</span></span> <span data-ttu-id="6a263-117">In diesem Fall werden die aktualisierten Dateien zuerst installiert, dann werden die alten Dateien entfernt.</span><span class="sxs-lookup"><span data-stu-id="6a263-117">In this case the updated files are installed first and then the old files are removed.</span></span> <span data-ttu-id="6a263-118">Wenn beim Entfernen der alten Anwendung jedoch ein Fehler auftritt, führt der Installer sowohl das Entfernen der alten Anwendung als auch die Installation der neuen Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="6a263-118">However, if the removal of the old application fails, then the installer rolls back both the removal of the old application and the install of the new application.</span></span>
-   <span data-ttu-id="6a263-119">Nach der [InstallFinalize-Aktion](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="6a263-119">After the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="6a263-120">Dies ist die effizienteste Platzierung für die Aktion.</span><span class="sxs-lookup"><span data-stu-id="6a263-120">This is the most efficient placement for the action.</span></span> <span data-ttu-id="6a263-121">In diesem Fall aktualisiert der Installer Dateien, bevor die alten Anwendungen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6a263-121">In this case, the installer updates files before removing the old applications.</span></span> <span data-ttu-id="6a263-122">Nur die zu Aktualisier Ende Dateien werden während der Installation installiert.</span><span class="sxs-lookup"><span data-stu-id="6a263-122">Only the files being updated get installed during the installation.</span></span> <span data-ttu-id="6a263-123">Wenn das Entfernen der alten Anwendung fehlschlägt, führt das Installationsprogramm nur ein Rollback für die Deinstallation der alten Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="6a263-123">If the removal of the old application fails, then the installer only rolls back the uninstallation of the old application.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="6a263-124">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="6a263-124">ActionData Messages</span></span>



| <span data-ttu-id="6a263-125">Feld</span><span class="sxs-lookup"><span data-stu-id="6a263-125">Field</span></span> | <span data-ttu-id="6a263-126">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="6a263-126">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="6a263-127">\[1\]</span><span class="sxs-lookup"><span data-stu-id="6a263-127">\[1\]</span></span> | <span data-ttu-id="6a263-128">Das Produkt wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="6a263-128">Removed product.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="6a263-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a263-129">Remarks</span></span>

<span data-ttu-id="6a263-130">Windows Installer legt die [**upgradingproductcode**](upgradingproductcode.md) -Eigenschaft fest, wenn diese Aktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a263-130">Windows Installer sets the [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) Property when it runs this action.</span></span>

 

 



