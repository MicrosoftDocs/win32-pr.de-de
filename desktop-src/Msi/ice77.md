---
description: ICE77 überprüft, ob benutzerdefinierte Aktionen mit dem Bitsatz "msidbcustomaction typeinscript" nach der InstallInitialize-Aktion und vor der InstallFinalize-Aktion sequenziert werden.
ms.assetid: 291cf731-b7e6-44c2-a8ec-78e0e037d1f5
title: ICE77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e072692b76cfd63bf62c5fd23f612a445e5fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129972"
---
# <a name="ice77"></a><span data-ttu-id="89a99-103">ICE77</span><span class="sxs-lookup"><span data-stu-id="89a99-103">ICE77</span></span>

<span data-ttu-id="89a99-104">ICE77 überprüft, ob benutzerdefinierte Aktionen mit dem Bitsatz " **msidbcustomaction typeinscript** " nach der [InstallInitialize-Aktion](installinitialize-action.md) und vor der [InstallFinalize-Aktion](installfinalize-action.md)sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="89a99-104">ICE77 verifies that custom actions with the **msidbCustomActionTypeInScript** bit set are sequenced after the [InstallInitialize action](installinitialize-action.md) and before the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="89a99-105">ICE77 überprüft die Sequenz in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) und der [AdminExecuteSequence-Tabelle](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="89a99-105">ICE77 checks the sequence in the [InstallExecuteSequence table](installexecutesequence-table.md) and [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="89a99-106">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="89a99-106">Result</span></span>

<span data-ttu-id="89a99-107">ICE77 gibt einen Fehler aus, wenn eine benutzerdefinierte in-Script-Aktion vor der InstallInitialize-Aktion oder nach der InstallFinalize-Aktion sequenziert wird.</span><span class="sxs-lookup"><span data-stu-id="89a99-107">ICE77 posts an error if an in-script custom action is sequenced before the InstallInitialize action or after the InstallFinalize action.</span></span>

<span data-ttu-id="89a99-108">ICE77 gibt einen Fehler aus, wenn die InstallInitialize-Aktion oder die InstallFinalize-Aktion fehlt.</span><span class="sxs-lookup"><span data-stu-id="89a99-108">ICE77 posts an error if the InstallInitialize action or the InstallFinalize action is missing.</span></span>

## <a name="example"></a><span data-ttu-id="89a99-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="89a99-109">Example</span></span>

<span data-ttu-id="89a99-110">ICE77 meldet die folgenden Fehler für das Beispiel:</span><span class="sxs-lookup"><span data-stu-id="89a99-110">ICE77 reports the following errors for the example:</span></span>

``` syntax
InstallFinalize is missing from 'InstallExecuteSequence'. 
CA_InScriptInstall is a in-script custom action. It must be sequenced 
before the InstallFinalize action.
 
CA_InScriptAdmin is a in-script custom action.  It must be sequenced 
in between the InstallInitialize action and the InstallFinalize action 
in the AdminExecuteSequence Sequence table.
```

<span data-ttu-id="89a99-111">[CustomAction-Tabelle](customaction-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="89a99-111">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="89a99-112">Aktion</span><span class="sxs-lookup"><span data-stu-id="89a99-112">Action</span></span>              | <span data-ttu-id="89a99-113">type</span><span class="sxs-lookup"><span data-stu-id="89a99-113">Type</span></span> |
|---------------------|------|
| <span data-ttu-id="89a99-114">ZS \_ inscriptinstall</span><span class="sxs-lookup"><span data-stu-id="89a99-114">CA\_InScriptInstall</span></span> | <span data-ttu-id="89a99-115">1025</span><span class="sxs-lookup"><span data-stu-id="89a99-115">1025</span></span> |
| <span data-ttu-id="89a99-116">ZS \_ inscriptadmin</span><span class="sxs-lookup"><span data-stu-id="89a99-116">CA\_InScriptAdmin</span></span>   | <span data-ttu-id="89a99-117">1026</span><span class="sxs-lookup"><span data-stu-id="89a99-117">1026</span></span> |



 

<span data-ttu-id="89a99-118">[InstallExecuteSequence-Tabelle](installexecutesequence-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="89a99-118">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="89a99-119">Aktion</span><span class="sxs-lookup"><span data-stu-id="89a99-119">Action</span></span>              | <span data-ttu-id="89a99-120">Sequenz</span><span class="sxs-lookup"><span data-stu-id="89a99-120">Sequence</span></span> |
|---------------------|----------|
| <span data-ttu-id="89a99-121">ZS \_ inscriptinstall</span><span class="sxs-lookup"><span data-stu-id="89a99-121">CA\_InScriptInstall</span></span> | <span data-ttu-id="89a99-122">2000</span><span class="sxs-lookup"><span data-stu-id="89a99-122">2000</span></span>     |
| <span data-ttu-id="89a99-123">Installinitialisieren</span><span class="sxs-lookup"><span data-stu-id="89a99-123">InstallInitialize</span></span>   | <span data-ttu-id="89a99-124">1500</span><span class="sxs-lookup"><span data-stu-id="89a99-124">1500</span></span>     |



 

<span data-ttu-id="89a99-125">[AdminExecuteSequence-Tabelle](adminexecutesequence-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="89a99-125">[AdminExecuteSequence Table](adminexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="89a99-126">Aktion</span><span class="sxs-lookup"><span data-stu-id="89a99-126">Action</span></span>            | <span data-ttu-id="89a99-127">Sequenz</span><span class="sxs-lookup"><span data-stu-id="89a99-127">Sequence</span></span> |
|-------------------|----------|
| <span data-ttu-id="89a99-128">ZS \_ inscriptadmin</span><span class="sxs-lookup"><span data-stu-id="89a99-128">CA\_InScriptAdmin</span></span> | <span data-ttu-id="89a99-129">1400</span><span class="sxs-lookup"><span data-stu-id="89a99-129">1400</span></span>     |
| <span data-ttu-id="89a99-130">Installinitialisieren</span><span class="sxs-lookup"><span data-stu-id="89a99-130">InstallInitialize</span></span> | <span data-ttu-id="89a99-131">1500</span><span class="sxs-lookup"><span data-stu-id="89a99-131">1500</span></span>     |
| <span data-ttu-id="89a99-132">InstallFinalize wurde</span><span class="sxs-lookup"><span data-stu-id="89a99-132">InstallFinalize</span></span>   | <span data-ttu-id="89a99-133">6600</span><span class="sxs-lookup"><span data-stu-id="89a99-133">6600</span></span>     |



 

<span data-ttu-id="89a99-134">Um die Fehler zu beheben, müssen Sie die benutzerdefinierten Aktionen in Skripts nach der InstallInitialize-Aktion und vor der InstallFinalize-Aktion sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="89a99-134">To fix the errors, sequence the in-script custom actions after the InstallInitialize action and before the InstallFinalize action.</span></span> <span data-ttu-id="89a99-135">Die InstallInitialize-und InstallFinalize-Aktionen müssen in der InstallExecuteSequence-Tabelle und der AdminExecuteSequence-Tabelle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="89a99-135">The InstallInitialize and InstallFinalize actions must be present in the InstallExecuteSequence table and the AdminExecuteSequence table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89a99-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="89a99-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89a99-137">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="89a99-137">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



