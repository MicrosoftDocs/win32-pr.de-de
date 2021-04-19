---
description: Die Tabelle AdminUISequence listet Aktionen auf, die das Installationsprogramm aufruft, wenn es die Administrator Aktion der obersten Ebene ausführt und die Ebene der internen Benutzeroberfläche auf vollständige Benutzeroberfläche oder reduzierte Benutzeroberfläche festgelegt ist.
ms.assetid: f23bd5c2-1d7f-485f-a22b-99436dfab6bf
title: Importieren der AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f1b9d2a91a350097ac043c186478e4933f6e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349349"
---
# <a name="importing-the-adminuisequence"></a><span data-ttu-id="f2dc0-103">Importieren der AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="f2dc0-103">Importing the AdminUISequence</span></span>

<span data-ttu-id="f2dc0-104">Die [Tabelle AdminUISequence](adminuisequence-table.md) listet Aktionen auf, die das Installationsprogramm aufruft, wenn es die [Administrator Aktion](admin-action.md) der obersten Ebene ausführt und die Ebene der internen Benutzeroberfläche auf vollständige Benutzeroberfläche oder reduzierte Benutzeroberfläche festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f2dc0-104">The [AdminUISequence table](adminuisequence-table.md) lists actions that the installer calls when it executes the top-level [ADMIN action](admin-action.md) and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="f2dc0-105">Das Installationsprogramm überspringt die Aktionen in dieser Tabelle, wenn die Benutzeroberflächen Ebene auf grundlegende Benutzeroberfläche oder keine Benutzeroberfläche festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f2dc0-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="f2dc0-106">Weitere Informationen finden Sie unter [Benutzeroberfläche](user-interface.md) und [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f2dc0-106">See [User Interface](user-interface.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="f2dc0-107">Weitere Informationen finden Sie in der [Gruppe "Installationsprozedur Tabellen](installation-procedure-tables-group.md)" unter [Verwendung einer Sequenz Tabelle](using-a-sequence-table.md)und im [detaillierten Beispiel der Sequenz Tabelle](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="f2dc0-107">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="f2dc0-108">Wenn Sie im Abschnitt [Importieren einer leeren Datenbank](importing-a-blank-database.md) , die Sie uisample.msi aus dem Windows Installer SDK verwendet haben, die Sequenz Tabellen in Ihrer Kopie von MNP2000.msi bereits die vorgeschlagenen Aktions Sequenzen enthalten, die unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f2dc0-108">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="f2dc0-109">Um das Notepad-Beispiel zu installieren, sollten keine Änderungen an diesen Sequenzen erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="f2dc0-109">No changes to these sequences should be necessary to install the Notepad sample.</span></span>

<span data-ttu-id="f2dc0-110">Öffnen Sie MNP2000.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die Tabelle AdminExecuteSequence ein.</span><span class="sxs-lookup"><span data-stu-id="f2dc0-110">Use your database editor to open MNP2000.msi and enter the following data into the AdminExecuteSequence table.</span></span>

[<span data-ttu-id="f2dc0-111">AdminUISequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="f2dc0-111">AdminUISequence Table</span></span>](adminuisequence-table.md)



| <span data-ttu-id="f2dc0-112">Aktion</span><span class="sxs-lookup"><span data-stu-id="f2dc0-112">Action</span></span>          | <span data-ttu-id="f2dc0-113">Bedingung</span><span class="sxs-lookup"><span data-stu-id="f2dc0-113">Condition</span></span> | <span data-ttu-id="f2dc0-114">Sequenz</span><span class="sxs-lookup"><span data-stu-id="f2dc0-114">Sequence</span></span> |
|-----------------|-----------|----------|
| <span data-ttu-id="f2dc0-115">Adminwelcomedlg</span><span class="sxs-lookup"><span data-stu-id="f2dc0-115">AdminWelcomeDlg</span></span> |           | <span data-ttu-id="f2dc0-116">1230</span><span class="sxs-lookup"><span data-stu-id="f2dc0-116">1230</span></span>     |
| <span data-ttu-id="f2dc0-117">Costfinalize</span><span class="sxs-lookup"><span data-stu-id="f2dc0-117">CostFinalize</span></span>    |           | <span data-ttu-id="f2dc0-118">1000</span><span class="sxs-lookup"><span data-stu-id="f2dc0-118">1000</span></span>     |
| <span data-ttu-id="f2dc0-119">Costinitialize</span><span class="sxs-lookup"><span data-stu-id="f2dc0-119">CostInitialize</span></span>  |           | <span data-ttu-id="f2dc0-120">800</span><span class="sxs-lookup"><span data-stu-id="f2dc0-120">800</span></span>      |
| <span data-ttu-id="f2dc0-121">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="f2dc0-121">ExecuteAction</span></span>   |           | <span data-ttu-id="f2dc0-122">1300</span><span class="sxs-lookup"><span data-stu-id="f2dc0-122">1300</span></span>     |
| <span data-ttu-id="f2dc0-123">Exitdlg</span><span class="sxs-lookup"><span data-stu-id="f2dc0-123">ExitDlg</span></span>         |           | <span data-ttu-id="f2dc0-124">-1</span><span class="sxs-lookup"><span data-stu-id="f2dc0-124">-1</span></span>       |
| <span data-ttu-id="f2dc0-125">Fatalerrordlg</span><span class="sxs-lookup"><span data-stu-id="f2dc0-125">FatalErrorDlg</span></span>   |           | <span data-ttu-id="f2dc0-126">-3</span><span class="sxs-lookup"><span data-stu-id="f2dc0-126">-3</span></span>       |
| <span data-ttu-id="f2dc0-127">Datei Kosten</span><span class="sxs-lookup"><span data-stu-id="f2dc0-127">FileCost</span></span>        |           | <span data-ttu-id="f2dc0-128">900</span><span class="sxs-lookup"><span data-stu-id="f2dc0-128">900</span></span>      |
| <span data-ttu-id="f2dc0-129">Preparedlg</span><span class="sxs-lookup"><span data-stu-id="f2dc0-129">PrepareDlg</span></span>      |           | <span data-ttu-id="f2dc0-130">140</span><span class="sxs-lookup"><span data-stu-id="f2dc0-130">140</span></span>      |
| <span data-ttu-id="f2dc0-131">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="f2dc0-131">ProgressDlg</span></span>     |           | <span data-ttu-id="f2dc0-132">1280</span><span class="sxs-lookup"><span data-stu-id="f2dc0-132">1280</span></span>     |
| <span data-ttu-id="f2dc0-133">Userexitdlg</span><span class="sxs-lookup"><span data-stu-id="f2dc0-133">UserExitDlg</span></span>     |           | <span data-ttu-id="f2dc0-134">-2</span><span class="sxs-lookup"><span data-stu-id="f2dc0-134">-2</span></span>       |



 

[<span data-ttu-id="f2dc0-135">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="f2dc0-135">Continue</span></span>](importing-the-advtexecutesequence.md)

 

 



