---
description: ICE13 überprüft, ob Dialoge in Sequenz Tabellen in den Tabellen "AdminUISequence" oder "InstallUISequence" angezeigt werden. Dialoge dürfen nicht in den Tabellen InstallExecuteSequence, AdminExecuteSequence oder AdvtExecuteSequence aufgeführt werden.
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fff440217ccffe41d5e4036f4ea0d03d1eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960040"
---
# <a name="ice13"></a><span data-ttu-id="a10ba-104">ICE13</span><span class="sxs-lookup"><span data-stu-id="a10ba-104">ICE13</span></span>

<span data-ttu-id="a10ba-105">ICE13 überprüft, ob Dialoge in Sequenz Tabellen in den Tabellen " [AdminUISequence](adminuisequence-table.md)" oder " [InstallUISequence](installuisequence-table.md) " angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a10ba-105">ICE13 validates that dialogs in sequence tables appear in the [AdminUISequence](adminuisequence-table.md), or [InstallUISequence](installuisequence-table.md) tables.</span></span> <span data-ttu-id="a10ba-106">Dialoge dürfen nicht in den Tabellen [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)oder [AdvtExecuteSequence](advtexecutesequence-table.md) aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a10ba-106">Dialogs must not be listed in the [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), or [AdvtExecuteSequence](advtexecutesequence-table.md) tables.</span></span>

## <a name="result"></a><span data-ttu-id="a10ba-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="a10ba-107">Result</span></span>

<span data-ttu-id="a10ba-108">ICE13 gibt eine Fehlermeldung aus, wenn ein Dialogfeld in einer Execute Sequence-Tabelle angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a10ba-108">ICE13 posts an error message if a dialog appears in an execute sequence table.</span></span>

## <a name="example"></a><span data-ttu-id="a10ba-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a10ba-109">Example</span></span>

<span data-ttu-id="a10ba-110">Im folgenden Beispiel gibt ICE13 eine Fehlermeldung aus, die besagt, dass "welcomedialog" nicht in der Tabelle "InstallExecuteSequence" aufgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a10ba-110">For the following example, ICE13 posts an error message stating that the 'WelcomeDialog' cannot be listed in the 'InstallExecuteSequence' table.</span></span>

<span data-ttu-id="a10ba-111">[InstallExecuteSequence-Tabelle](installexecutesequence-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="a10ba-111">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="a10ba-112">Aktion</span><span class="sxs-lookup"><span data-stu-id="a10ba-112">Action</span></span>          |
|-----------------|
| <span data-ttu-id="a10ba-113">InstallFinalize wurde</span><span class="sxs-lookup"><span data-stu-id="a10ba-113">InstallFinalize</span></span> |
| <span data-ttu-id="a10ba-114">Costfinalize</span><span class="sxs-lookup"><span data-stu-id="a10ba-114">CostFinalize</span></span>    |
| <span data-ttu-id="a10ba-115">Welcomedialog</span><span class="sxs-lookup"><span data-stu-id="a10ba-115">WelcomeDialog</span></span>   |



 

<span data-ttu-id="a10ba-116">[InstallUISequence-Tabelle](installuisequence-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="a10ba-116">[InstallUISequence Table](installuisequence-table.md) (partial)</span></span>



| <span data-ttu-id="a10ba-117">Aktion</span><span class="sxs-lookup"><span data-stu-id="a10ba-117">Action</span></span>         |
|----------------|
| <span data-ttu-id="a10ba-118">Costfinalize</span><span class="sxs-lookup"><span data-stu-id="a10ba-118">CostFinalize</span></span>   |
| <span data-ttu-id="a10ba-119">Costinitialize</span><span class="sxs-lookup"><span data-stu-id="a10ba-119">CostInitialize</span></span> |
| <span data-ttu-id="a10ba-120">Browgdialog</span><span class="sxs-lookup"><span data-stu-id="a10ba-120">BrowseDialog</span></span>   |



 

<span data-ttu-id="a10ba-121">[Dialog Feld Tabelle](dialog-table.md) (teilweise)</span><span class="sxs-lookup"><span data-stu-id="a10ba-121">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="a10ba-122">Dialog</span><span class="sxs-lookup"><span data-stu-id="a10ba-122">Dialog</span></span>        |
|---------------|
| <span data-ttu-id="a10ba-123">Browgdialog</span><span class="sxs-lookup"><span data-stu-id="a10ba-123">BrowseDialog</span></span>  |
| <span data-ttu-id="a10ba-124">Welcomedialog</span><span class="sxs-lookup"><span data-stu-id="a10ba-124">WelcomeDialog</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a10ba-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a10ba-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a10ba-126">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="a10ba-126">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



