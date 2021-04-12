---
description: ICE75 überprüft, ob alle benutzerdefinierten Aktions Typen 17 (dll), Custom Action Type 18 (exe), Custom Action Type 21 (JScript) und Custom Action Type 22 (VBScript) benutzerdefinierte Aktionen nach der costfinalize-Aktion sequenziert werden.
ms.assetid: 831de042-bea6-42da-90a0-3847bb447414
title: ICE75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d708552b3ed2d397e29d37abdf0ceed01093fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347358"
---
# <a name="ice75"></a><span data-ttu-id="0967d-103">ICE75</span><span class="sxs-lookup"><span data-stu-id="0967d-103">ICE75</span></span>

<span data-ttu-id="0967d-104">ICE75 überprüft, ob alle benutzerdefinierten [Aktions Typen 17](custom-action-type-17.md) (dll), [Custom Action Type 18](custom-action-type-18.md) (exe), Custom [Action Type 21](custom-action-type-21.md) (JScript) und Custom [Action Type 22](custom-action-type-22.md) (VBScript) benutzerdefinierte Aktionen nach der [costfinalize-Aktion](costfinalize-action.md)sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="0967d-104">ICE75 verifies that all [Custom Action Type 17](custom-action-type-17.md) (DLL), [Custom Action Type 18](custom-action-type-18.md) (EXE), [Custom Action type 21](custom-action-type-21.md) (JScript), and [Custom Action Type 22](custom-action-type-22.md) (VBScript) custom actions are sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="0967d-105">Diese Typen von benutzerdefinierten Aktionen verwenden eine installierte Datei als Quelle.</span><span class="sxs-lookup"><span data-stu-id="0967d-105">These types of custom action use an installed file as their source.</span></span> <span data-ttu-id="0967d-106">ICE75 überprüft die Tabelle " [InstallUISequence](installuisequence-table.md)", " [InstallExecuteSequence Table](installexecutesequence-table.md)", " [AdminUISequence](adminuisequence-table.md)" und " [AdminExecuteSequence](adminexecutesequence-table.md)".</span><span class="sxs-lookup"><span data-stu-id="0967d-106">ICE75 checks the [InstallUISequence Table](installuisequence-table.md), [InstallExecuteSequence Table](installexecutesequence-table.md), [AdminUISequence Table](adminuisequence-table.md), and [AdminExecuteSequence Table](adminexecutesequence-table.md).</span></span> <span data-ttu-id="0967d-107">Beachten Sie, dass die Aktion "costfinalize" in diesen Sequenz Tabellen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0967d-107">Note that the CostFinalize action is required in these sequence tables.</span></span>

## <a name="result"></a><span data-ttu-id="0967d-108">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="0967d-108">Result</span></span>

<span data-ttu-id="0967d-109">ICE75 gibt einen Fehler aus, wenn eine benutzerdefinierte Aktion mithilfe einer installierten Datei als Quelldatei gefunden wird, die nach der costfinalize-Aktion nicht sequenziert wurde.</span><span class="sxs-lookup"><span data-stu-id="0967d-109">ICE75 posts an error if it finds a custom action using an installed file as a source file that is not sequenced after the CostFinalize action.</span></span>

## <a name="example"></a><span data-ttu-id="0967d-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0967d-110">Example</span></span>

<span data-ttu-id="0967d-111">ICE75 meldet die folgenden Fehler für das gezeigte Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0967d-111">ICE75 reports the following errors for the example shown:</span></span>

``` syntax
CostFinalize is missing from 'AdminUISequence'. CA_FileExe is a custom
 action whose source is an installed file. It must be sequenced after 
the CostFinalize action.
 
CA_FileDLL is a custom action whose source is an installed file.  It 
must be sequenced after the CostFinalize action in the 
AdminExecuteSequence table
```

<span data-ttu-id="0967d-112">[CustomAction-Tabelle](customaction-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="0967d-112">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="0967d-113">Aktion</span><span class="sxs-lookup"><span data-stu-id="0967d-113">Action</span></span>      | <span data-ttu-id="0967d-114">type</span><span class="sxs-lookup"><span data-stu-id="0967d-114">Type</span></span> | <span data-ttu-id="0967d-115">`Source`</span><span class="sxs-lookup"><span data-stu-id="0967d-115">Source</span></span>  |
|-------------|------|---------|
| <span data-ttu-id="0967d-116">\_Datei-exe-Datei</span><span class="sxs-lookup"><span data-stu-id="0967d-116">CA\_FileExe</span></span> | <span data-ttu-id="0967d-117">18</span><span class="sxs-lookup"><span data-stu-id="0967d-117">18</span></span>   | <span data-ttu-id="0967d-118">FileExe</span><span class="sxs-lookup"><span data-stu-id="0967d-118">FileExe</span></span> |
| <span data-ttu-id="0967d-119">ZS- \_ Datei-dll</span><span class="sxs-lookup"><span data-stu-id="0967d-119">CA\_FileDLL</span></span> | <span data-ttu-id="0967d-120">17</span><span class="sxs-lookup"><span data-stu-id="0967d-120">17</span></span>   | <span data-ttu-id="0967d-121">Filedll</span><span class="sxs-lookup"><span data-stu-id="0967d-121">FileDLL</span></span> |



 

<span data-ttu-id="0967d-122">[AdminUISequence-Tabelle](adminuisequence-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="0967d-122">[AdminUISequence Table](adminuisequence-table.md) (partial)</span></span>



| <span data-ttu-id="0967d-123">Aktion</span><span class="sxs-lookup"><span data-stu-id="0967d-123">Action</span></span>      | <span data-ttu-id="0967d-124">Sequenz</span><span class="sxs-lookup"><span data-stu-id="0967d-124">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="0967d-125">\_Datei-exe-Datei</span><span class="sxs-lookup"><span data-stu-id="0967d-125">CA\_FileExe</span></span> | <span data-ttu-id="0967d-126">1100</span><span class="sxs-lookup"><span data-stu-id="0967d-126">1100</span></span>     |



 

<span data-ttu-id="0967d-127">[AdminExecuteSequence-Tabelle](adminexecutesequence-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="0967d-127">[AdminExecuteSequence Table](adminexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="0967d-128">Aktion</span><span class="sxs-lookup"><span data-stu-id="0967d-128">Action</span></span>       | <span data-ttu-id="0967d-129">Sequenz</span><span class="sxs-lookup"><span data-stu-id="0967d-129">Sequence</span></span> |
|--------------|----------|
| <span data-ttu-id="0967d-130">ZS- \_ Datei-dll</span><span class="sxs-lookup"><span data-stu-id="0967d-130">CA\_FileDLL</span></span>  | <span data-ttu-id="0967d-131">800</span><span class="sxs-lookup"><span data-stu-id="0967d-131">800</span></span>      |
| <span data-ttu-id="0967d-132">Costfinalize</span><span class="sxs-lookup"><span data-stu-id="0967d-132">CostFinalize</span></span> | <span data-ttu-id="0967d-133">1000</span><span class="sxs-lookup"><span data-stu-id="0967d-133">1000</span></span>     |



 

<span data-ttu-id="0967d-134">Um die Fehler zu beheben, müssen Sie die benutzerdefinierten Aktionen nach der costfinalize-Aktion sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="0967d-134">To fix the errors, sequence the custom actions after the CostFinalize action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0967d-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0967d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0967d-136">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="0967d-136">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



