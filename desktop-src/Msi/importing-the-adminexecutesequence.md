---
description: Die Tabelle AdminExecuteSequence listet Aktionen auf, die vom Installationsprogramm ausgeführt werden, wenn es die Administrator Aktion der obersten Ebene aufruft. Weitere Informationen finden Sie in der Gruppe "Installationsprozedur Tabellen" unter Verwendung einer Sequenz Tabelle und im detaillierten Beispiel der Sequenz Tabelle.
ms.assetid: 8b1da4a3-0b82-4b71-8a32-59e90025cbfa
title: Importieren von "AdminExecuteSequence"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cfef89ada780d9ce647f45667fdc34cc5b01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752784"
---
# <a name="importing-the-adminexecutesequence"></a><span data-ttu-id="33437-104">Importieren von "AdminExecuteSequence"</span><span class="sxs-lookup"><span data-stu-id="33437-104">Importing the AdminExecuteSequence</span></span>

<span data-ttu-id="33437-105">Die [Tabelle AdminExecuteSequence](adminexecutesequence-table.md) listet Aktionen auf, die vom Installationsprogramm ausgeführt werden, wenn es die [Administrator Aktion](admin-action.md)der obersten Ebene aufruft.</span><span class="sxs-lookup"><span data-stu-id="33437-105">The [AdminExecuteSequence table](adminexecutesequence-table.md) lists actions that the installer executes when it calls the top-level [ADMIN action](admin-action.md).</span></span> <span data-ttu-id="33437-106">Weitere Informationen finden Sie in der [Gruppe "Installationsprozedur Tabellen](installation-procedure-tables-group.md)" unter [Verwendung einer Sequenz Tabelle](using-a-sequence-table.md)und im [detaillierten Beispiel der Sequenz Tabelle](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="33437-106">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="33437-107">Wenn Sie im Abschnitt [Importieren einer leeren Datenbank](importing-a-blank-database.md) , die Sie uisample.msi aus dem Windows Installer SDK verwendet haben, die Sequenz Tabellen in Ihrer Kopie von MNP2000.msi bereits die vorgeschlagenen Aktions Sequenzen enthalten, die unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="33437-107">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="33437-108">Es sollten keine Änderungen an diesen Sequenzen notwendig sein, um das Notepad-Beispiel Installationspaket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="33437-108">No changes to these sequences should be necessary to author the Notepad sample installation package.</span></span>

<span data-ttu-id="33437-109">Öffnen Sie MNP2000.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die Tabelle AdminExecuteSequence ein.</span><span class="sxs-lookup"><span data-stu-id="33437-109">Use your database editor to open MNP2000.msi and enter the following data into the AdminExecuteSequence table.</span></span>

[<span data-ttu-id="33437-110">AdminExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="33437-110">AdminExecuteSequence Table</span></span>](adminexecutesequence-table.md)



| <span data-ttu-id="33437-111">Aktion</span><span class="sxs-lookup"><span data-stu-id="33437-111">Action</span></span>              | <span data-ttu-id="33437-112">Bedingung</span><span class="sxs-lookup"><span data-stu-id="33437-112">Condition</span></span> | <span data-ttu-id="33437-113">Sequenz</span><span class="sxs-lookup"><span data-stu-id="33437-113">Sequence</span></span> |
|---------------------|-----------|----------|
| <span data-ttu-id="33437-114">Costfinalize</span><span class="sxs-lookup"><span data-stu-id="33437-114">CostFinalize</span></span>        |           | <span data-ttu-id="33437-115">1000</span><span class="sxs-lookup"><span data-stu-id="33437-115">1000</span></span>     |
| <span data-ttu-id="33437-116">Costinitialize</span><span class="sxs-lookup"><span data-stu-id="33437-116">CostInitialize</span></span>      |           | <span data-ttu-id="33437-117">800</span><span class="sxs-lookup"><span data-stu-id="33437-117">800</span></span>      |
| <span data-ttu-id="33437-118">Datei Kosten</span><span class="sxs-lookup"><span data-stu-id="33437-118">FileCost</span></span>            |           | <span data-ttu-id="33437-119">900</span><span class="sxs-lookup"><span data-stu-id="33437-119">900</span></span>      |
| <span data-ttu-id="33437-120">Installadminpackage</span><span class="sxs-lookup"><span data-stu-id="33437-120">InstallAdminPackage</span></span> |           | <span data-ttu-id="33437-121">3900</span><span class="sxs-lookup"><span data-stu-id="33437-121">3900</span></span>     |
| <span data-ttu-id="33437-122">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="33437-122">InstallFiles</span></span>        |           | <span data-ttu-id="33437-123">4000</span><span class="sxs-lookup"><span data-stu-id="33437-123">4000</span></span>     |
| <span data-ttu-id="33437-124">InstallFinalize wurde</span><span class="sxs-lookup"><span data-stu-id="33437-124">InstallFinalize</span></span>     |           | <span data-ttu-id="33437-125">6600</span><span class="sxs-lookup"><span data-stu-id="33437-125">6600</span></span>     |
| <span data-ttu-id="33437-126">Installinitialisieren</span><span class="sxs-lookup"><span data-stu-id="33437-126">InstallInitialize</span></span>   |           | <span data-ttu-id="33437-127">1500</span><span class="sxs-lookup"><span data-stu-id="33437-127">1500</span></span>     |
| <span data-ttu-id="33437-128">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="33437-128">InstallValidate</span></span>     |           | <span data-ttu-id="33437-129">1400</span><span class="sxs-lookup"><span data-stu-id="33437-129">1400</span></span>     |



 

[<span data-ttu-id="33437-130">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="33437-130">Continue</span></span>](importing-the-adminuisequence.md)

 

 



