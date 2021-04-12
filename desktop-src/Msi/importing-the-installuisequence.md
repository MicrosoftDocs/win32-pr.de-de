---
description: Die Benutzeroberflächen Sequenz wird in die-Beispieldatenbank importiert.
ms.assetid: 750e4dc6-91ff-4d9a-a968-abc2515e3b7c
title: Importieren der InstallUISequence-Sequenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f20de59a752da6d24a5f3e7fed94e00aa4f0048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216937"
---
# <a name="importing-the-installuisequence"></a><span data-ttu-id="e0d10-103">Importieren der InstallUISequence-Sequenz</span><span class="sxs-lookup"><span data-stu-id="e0d10-103">Importing the InstallUISequence</span></span>

<span data-ttu-id="e0d10-104">In der [Tabelle InstallUISequence](installuisequence-table.md) sind Aktionen aufgeführt, die ausgeführt werden, wenn die [Installations Aktion](install-action.md) der obersten Ebene ausgeführt wird und die Ebene der internen Benutzeroberfläche auf vollständige Benutzeroberfläche oder reduzierte Benutzeroberfläche festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e0d10-104">The [InstallUISequence table](installuisequence-table.md) lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="e0d10-105">Das Installationsprogramm überspringt die Aktionen in dieser Tabelle, wenn die Benutzeroberflächen Ebene auf grundlegende Benutzeroberfläche oder auf keine Benutzeroberfläche festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e0d10-105">The installer skips the actions in this table if the user interface level is set to basic UI or to no UI.</span></span> <span data-ttu-id="e0d10-106">Weitere Informationen finden Sie unter [Benutzeroberfläche](user-interface.md) und [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="e0d10-106">See [User Interface](user-interface.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="e0d10-107">Weitere Informationen finden Sie in der [Gruppe "Installationsprozedur Tabellen](installation-procedure-tables-group.md)" unter [Verwendung einer Sequenz Tabelle](using-a-sequence-table.md)und im [detaillierten Beispiel der Sequenz Tabelle](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="e0d10-107">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="e0d10-108">Wenn Sie im Abschnitt [Importieren einer leeren Datenbank](importing-a-blank-database.md) , die Sie uisample.msi aus dem Windows Installer SDK verwendet haben, die Sequenz Tabellen in Ihrer Kopie von MNP2000.msi bereits die vorgeschlagenen Aktions Sequenzen enthalten, die unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e0d10-108">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="e0d10-109">Es sollten keine Änderungen an diesen Sequenzen notwendig sein, um das Notepad-Installationspaket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e0d10-109">No changes to these sequences should be necessary to author the Notepad installation package.</span></span>

<span data-ttu-id="e0d10-110">Öffnen Sie MNP2000.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die Tabelle InstallUISequence ein.</span><span class="sxs-lookup"><span data-stu-id="e0d10-110">Use your database editor to open MNP2000.msi and enter the following data into the InstallUISequence table.</span></span>

[<span data-ttu-id="e0d10-111">InstallUISequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="e0d10-111">InstallUISequence Table</span></span>](installuisequence-table.md)



| <span data-ttu-id="e0d10-112">Aktion</span><span class="sxs-lookup"><span data-stu-id="e0d10-112">Action</span></span>                | <span data-ttu-id="e0d10-113">Bedingung</span><span class="sxs-lookup"><span data-stu-id="e0d10-113">Condition</span></span>                                    | <span data-ttu-id="e0d10-114">Sequenz</span><span class="sxs-lookup"><span data-stu-id="e0d10-114">Sequence</span></span> |
|-----------------------|----------------------------------------------|----------|
| <span data-ttu-id="e0d10-115">AppSearch</span><span class="sxs-lookup"><span data-stu-id="e0d10-115">AppSearch</span></span>             |                                              | <span data-ttu-id="e0d10-116">400</span><span class="sxs-lookup"><span data-stu-id="e0d10-116">400</span></span>      |
| <span data-ttu-id="e0d10-117">Ccpsearch</span><span class="sxs-lookup"><span data-stu-id="e0d10-117">CCPSearch</span></span>             | <span data-ttu-id="e0d10-118">Nicht installiert</span><span class="sxs-lookup"><span data-stu-id="e0d10-118">NOT Installed</span></span>                                | <span data-ttu-id="e0d10-119">500</span><span class="sxs-lookup"><span data-stu-id="e0d10-119">500</span></span>      |
| <span data-ttu-id="e0d10-120">Costfinalize</span><span class="sxs-lookup"><span data-stu-id="e0d10-120">CostFinalize</span></span>          |                                              | <span data-ttu-id="e0d10-121">1000</span><span class="sxs-lookup"><span data-stu-id="e0d10-121">1000</span></span>     |
| <span data-ttu-id="e0d10-122">Costinitialize</span><span class="sxs-lookup"><span data-stu-id="e0d10-122">CostInitialize</span></span>        |                                              | <span data-ttu-id="e0d10-123">800</span><span class="sxs-lookup"><span data-stu-id="e0d10-123">800</span></span>      |
| <span data-ttu-id="e0d10-124">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="e0d10-124">ExecuteAction</span></span>         |                                              | <span data-ttu-id="e0d10-125">1300</span><span class="sxs-lookup"><span data-stu-id="e0d10-125">1300</span></span>     |
| <span data-ttu-id="e0d10-126">Exitdlg</span><span class="sxs-lookup"><span data-stu-id="e0d10-126">ExitDlg</span></span>               |                                              | <span data-ttu-id="e0d10-127">-1</span><span class="sxs-lookup"><span data-stu-id="e0d10-127">-1</span></span>       |
| <span data-ttu-id="e0d10-128">Fatalerrordlg</span><span class="sxs-lookup"><span data-stu-id="e0d10-128">FatalErrorDlg</span></span>         |                                              | <span data-ttu-id="e0d10-129">-3</span><span class="sxs-lookup"><span data-stu-id="e0d10-129">-3</span></span>       |
| <span data-ttu-id="e0d10-130">Datei Kosten</span><span class="sxs-lookup"><span data-stu-id="e0d10-130">FileCost</span></span>              |                                              | <span data-ttu-id="e0d10-131">900</span><span class="sxs-lookup"><span data-stu-id="e0d10-131">900</span></span>      |
| <span data-ttu-id="e0d10-132">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="e0d10-132">LaunchConditions</span></span>      |                                              | <span data-ttu-id="e0d10-133">100</span><span class="sxs-lookup"><span data-stu-id="e0d10-133">100</span></span>      |
| <span data-ttu-id="e0d10-134">Maintenancewelcomedlg</span><span class="sxs-lookup"><span data-stu-id="e0d10-134">MaintenanceWelcomeDlg</span></span> | <span data-ttu-id="e0d10-135">Installiert, nicht fortsetzen und nicht vorab ausgewählt</span><span class="sxs-lookup"><span data-stu-id="e0d10-135">Installed AND NOT RESUME AND NOT Preselected</span></span> | <span data-ttu-id="e0d10-136">1250</span><span class="sxs-lookup"><span data-stu-id="e0d10-136">1250</span></span>     |
| <span data-ttu-id="e0d10-137">Preparedlg</span><span class="sxs-lookup"><span data-stu-id="e0d10-137">PrepareDlg</span></span>            |                                              | <span data-ttu-id="e0d10-138">140</span><span class="sxs-lookup"><span data-stu-id="e0d10-138">140</span></span>      |
| <span data-ttu-id="e0d10-139">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="e0d10-139">ProgressDlg</span></span>           |                                              | <span data-ttu-id="e0d10-140">1280</span><span class="sxs-lookup"><span data-stu-id="e0d10-140">1280</span></span>     |
| <span data-ttu-id="e0d10-141">Resumedlg</span><span class="sxs-lookup"><span data-stu-id="e0d10-141">ResumeDlg</span></span>             | <span data-ttu-id="e0d10-142">Installiert und (fortsetzen oder vorab ausgewählt)</span><span class="sxs-lookup"><span data-stu-id="e0d10-142">Installed AND (RESUME OR Preselected)</span></span>        | <span data-ttu-id="e0d10-143">1240</span><span class="sxs-lookup"><span data-stu-id="e0d10-143">1240</span></span>     |
| <span data-ttu-id="e0d10-144">RMCCPSEARCH</span><span class="sxs-lookup"><span data-stu-id="e0d10-144">RMCCPSearch</span></span>           | <span data-ttu-id="e0d10-145">Nicht installiert</span><span class="sxs-lookup"><span data-stu-id="e0d10-145">NOT Installed</span></span>                                | <span data-ttu-id="e0d10-146">600</span><span class="sxs-lookup"><span data-stu-id="e0d10-146">600</span></span>      |
| <span data-ttu-id="e0d10-147">Userexitdlg</span><span class="sxs-lookup"><span data-stu-id="e0d10-147">UserExitDlg</span></span>           |                                              | <span data-ttu-id="e0d10-148">-2</span><span class="sxs-lookup"><span data-stu-id="e0d10-148">-2</span></span>       |
| <span data-ttu-id="e0d10-149">Welcomedlg</span><span class="sxs-lookup"><span data-stu-id="e0d10-149">WelcomeDlg</span></span>            | <span data-ttu-id="e0d10-150">Nicht installiert</span><span class="sxs-lookup"><span data-stu-id="e0d10-150">NOT Installed</span></span>                                | <span data-ttu-id="e0d10-151">1230</span><span class="sxs-lookup"><span data-stu-id="e0d10-151">1230</span></span>     |
| <span data-ttu-id="e0d10-152">MigrateFeatureStates</span><span class="sxs-lookup"><span data-stu-id="e0d10-152">MigrateFeatureStates</span></span>  |                                              | <span data-ttu-id="e0d10-153">1200</span><span class="sxs-lookup"><span data-stu-id="e0d10-153">1200</span></span>     |
| <span data-ttu-id="e0d10-154">FindRelatedProducts</span><span class="sxs-lookup"><span data-stu-id="e0d10-154">FindRelatedProducts</span></span>   |                                              | <span data-ttu-id="e0d10-155">200</span><span class="sxs-lookup"><span data-stu-id="e0d10-155">200</span></span>      |



 

[<span data-ttu-id="e0d10-156">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="e0d10-156">Continue</span></span>](importing-the-adminexecutesequence.md)

 

 



