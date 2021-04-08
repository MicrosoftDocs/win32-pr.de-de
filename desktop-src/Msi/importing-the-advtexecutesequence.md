---
description: In der AdvtExecuteSequence-Tabelle sind Aktionen aufgeführt, die vom Installer beim Ausführen der Ankündigungs Aktion der obersten Ebene aufgerufen werden. Weitere Informationen finden Sie in der Gruppe "Installationsprozedur Tabellen" unter Verwendung einer Sequenz Tabelle und im detaillierten Beispiel der Sequenz Tabelle.
ms.assetid: 269bd28c-fa45-42b8-a610-1c4c5fcabc19
title: Importieren von AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4d7622670973a622b1376456ecfef445684cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757818"
---
# <a name="importing-the-advtexecutesequence"></a><span data-ttu-id="923fc-104">Importieren von AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="923fc-104">Importing the AdvtExecuteSequence</span></span>

<span data-ttu-id="923fc-105">In der [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md) sind Aktionen aufgeführt, die vom Installer beim Ausführen der Ankündigungs [Aktion](advertise-action.md)der obersten Ebene aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="923fc-105">The [AdvtExecuteSequence table](advtexecutesequence-table.md) lists actions the installer calls when it executes the top-level [ADVERTISE action](advertise-action.md).</span></span> <span data-ttu-id="923fc-106">Weitere Informationen finden Sie in der [Gruppe "Installationsprozedur Tabellen](installation-procedure-tables-group.md)" unter [Verwendung einer Sequenz Tabelle](using-a-sequence-table.md)und im [detaillierten Beispiel der Sequenz Tabelle](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="923fc-106">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="923fc-107">Wenn Sie im Abschnitt [Importieren einer leeren Datenbank](importing-a-blank-database.md) , die Sie uisample.msi aus dem Windows Installer SDK verwendet haben, die Sequenz Tabellen in Ihrer Kopie von MNP2000.msi bereits die vorgeschlagenen Aktions Sequenzen enthalten, die unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="923fc-107">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence table](using-a-sequence-table.md).</span></span> <span data-ttu-id="923fc-108">Es sollten keine Änderungen an diesen Sequenzen notwendig sein, um das Notepad-Beispiel Installationspaket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="923fc-108">No changes to these sequences should be necessary to author the Notepad sample installation package.</span></span>

<span data-ttu-id="923fc-109">Öffnen Sie MNP2000.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="923fc-109">Use your database editor to open MNP2000.msi and enter the following data into the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

[<span data-ttu-id="923fc-110">AdvtExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="923fc-110">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)



| <span data-ttu-id="923fc-111">Aktion</span><span class="sxs-lookup"><span data-stu-id="923fc-111">Action</span></span>                | <span data-ttu-id="923fc-112">Bedingung</span><span class="sxs-lookup"><span data-stu-id="923fc-112">Condition</span></span> | <span data-ttu-id="923fc-113">Sequenz</span><span class="sxs-lookup"><span data-stu-id="923fc-113">Sequence</span></span> |
|-----------------------|-----------|----------|
| <span data-ttu-id="923fc-114">Costfinalize</span><span class="sxs-lookup"><span data-stu-id="923fc-114">CostFinalize</span></span>          |           | <span data-ttu-id="923fc-115">1000</span><span class="sxs-lookup"><span data-stu-id="923fc-115">1000</span></span>     |
| <span data-ttu-id="923fc-116">Costinitialize</span><span class="sxs-lookup"><span data-stu-id="923fc-116">CostInitialize</span></span>        |           | <span data-ttu-id="923fc-117">800</span><span class="sxs-lookup"><span data-stu-id="923fc-117">800</span></span>      |
| <span data-ttu-id="923fc-118">"Kreateshortcuts"</span><span class="sxs-lookup"><span data-stu-id="923fc-118">CreateShortcuts</span></span>       |           | <span data-ttu-id="923fc-119">4500</span><span class="sxs-lookup"><span data-stu-id="923fc-119">4500</span></span>     |
| <span data-ttu-id="923fc-120">InstallFinalize wurde</span><span class="sxs-lookup"><span data-stu-id="923fc-120">InstallFinalize</span></span>       |           | <span data-ttu-id="923fc-121">6600</span><span class="sxs-lookup"><span data-stu-id="923fc-121">6600</span></span>     |
| <span data-ttu-id="923fc-122">Installinitialisieren</span><span class="sxs-lookup"><span data-stu-id="923fc-122">InstallInitialize</span></span>     |           | <span data-ttu-id="923fc-123">1500</span><span class="sxs-lookup"><span data-stu-id="923fc-123">1500</span></span>     |
| <span data-ttu-id="923fc-124">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="923fc-124">InstallValidate</span></span>       |           | <span data-ttu-id="923fc-125">1400</span><span class="sxs-lookup"><span data-stu-id="923fc-125">1400</span></span>     |
| <span data-ttu-id="923fc-126">PublishComponents</span><span class="sxs-lookup"><span data-stu-id="923fc-126">PublishComponents</span></span>     |           | <span data-ttu-id="923fc-127">6200</span><span class="sxs-lookup"><span data-stu-id="923fc-127">6200</span></span>     |
| <span data-ttu-id="923fc-128">Publishfeatures</span><span class="sxs-lookup"><span data-stu-id="923fc-128">PublishFeatures</span></span>       |           | <span data-ttu-id="923fc-129">6300</span><span class="sxs-lookup"><span data-stu-id="923fc-129">6300</span></span>     |
| <span data-ttu-id="923fc-130">Publishproduct</span><span class="sxs-lookup"><span data-stu-id="923fc-130">PublishProduct</span></span>        |           | <span data-ttu-id="923fc-131">6400</span><span class="sxs-lookup"><span data-stu-id="923fc-131">6400</span></span>     |
| <span data-ttu-id="923fc-132">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="923fc-132">RegisterClassInfo</span></span>     |           | <span data-ttu-id="923fc-133">4600</span><span class="sxs-lookup"><span data-stu-id="923fc-133">4600</span></span>     |
| <span data-ttu-id="923fc-134">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="923fc-134">RegisterExtensionInfo</span></span> |           | <span data-ttu-id="923fc-135">4700</span><span class="sxs-lookup"><span data-stu-id="923fc-135">4700</span></span>     |
| <span data-ttu-id="923fc-136">Registermimeinfo</span><span class="sxs-lookup"><span data-stu-id="923fc-136">RegisterMIMEInfo</span></span>      |           | <span data-ttu-id="923fc-137">4900</span><span class="sxs-lookup"><span data-stu-id="923fc-137">4900</span></span>     |
| <span data-ttu-id="923fc-138">Registerprogidinfo</span><span class="sxs-lookup"><span data-stu-id="923fc-138">RegisterProgIdInfo</span></span>    |           | <span data-ttu-id="923fc-139">4800</span><span class="sxs-lookup"><span data-stu-id="923fc-139">4800</span></span>     |



 

<span data-ttu-id="923fc-140">Die [advtuisequence-Tabelle](advtuisequence-table.md) wird vom Installer nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="923fc-140">The [AdvtUISequence table](advtuisequence-table.md) is not used by the installer.</span></span> <span data-ttu-id="923fc-141">Diese Tabelle sollte in der Installations Datenbank nicht vorhanden oder leer gelassen werden.</span><span class="sxs-lookup"><span data-stu-id="923fc-141">This table should not exist or be left empty in the installation database.</span></span>

[<span data-ttu-id="923fc-142">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="923fc-142">Continue</span></span>](adding-summary-information.md)

 

 



