---
description: ICE63 prüft, ob die Aktion "RemoveExistingProducts" ordnungsgemäß sequenziert werden soll.
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5faa6f2ddbcb95cdf12966c2887fe9438a5d610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866719"
---
# <a name="ice63"></a><span data-ttu-id="19712-103">ICE63</span><span class="sxs-lookup"><span data-stu-id="19712-103">ICE63</span></span>

<span data-ttu-id="19712-104">ICE63 prüft, ob die Aktion " [RemoveExistingProducts](removeexistingproducts-action.md)" ordnungsgemäß sequenziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="19712-104">ICE63 checks for proper sequencing of the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span> <span data-ttu-id="19712-105">Die Aktion "RemoveExistingProducts" kann platziert werden:</span><span class="sxs-lookup"><span data-stu-id="19712-105">The RemoveExistingProducts action may be placed:</span></span>

1.  <span data-ttu-id="19712-106">Zwischen InstallValidate und InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="19712-106">Between InstallValidate and InstallInitialize</span></span>
2.  <span data-ttu-id="19712-107">Direkt nach InstallInitialize oder nach InstallInitialize, wenn die Aktionen zwischen InstallInitialize und RemoveExistingProducts keine Skript Aktionen generieren.</span><span class="sxs-lookup"><span data-stu-id="19712-107">Immediately after InstallInitialize, or after InstallInitialize if the actions between InstallInitialize and RemoveExistingProducts do not generate any script actions.</span></span>
3.  <span data-ttu-id="19712-108">Unmittelbar nach InstallExecute oder InstallExecuteAgain und vor InstallFinalize (dieselbe Einschränkung wie oben).</span><span class="sxs-lookup"><span data-stu-id="19712-108">Immediately after InstallExecute or InstallExecuteAgain and before InstallFinalize (the same restriction as above applies).</span></span>
4.  <span data-ttu-id="19712-109">Nach InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="19712-109">After InstallFinalize.</span></span>

<span data-ttu-id="19712-110">Wenn eine Warnung oder ein von ICE63 gemeldeter Fehler nicht behoben werden konnte, führt dies zu einem Fehler des Upgrades.</span><span class="sxs-lookup"><span data-stu-id="19712-110">Failure to fix a warning or error reported by ICE63 leads to failure of the upgrade.</span></span>

## <a name="result"></a><span data-ttu-id="19712-111">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="19712-111">Result</span></span>

<span data-ttu-id="19712-112">ICE63 gibt eine Warnung oder einen Fehler aus, wenn die Sequenzierung der RemoveExistingProducts-Aktion nicht korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="19712-112">ICE63 posts a warning or error if the sequencing of the RemoveExistingProducts action is not correct.</span></span>

## <a name="example"></a><span data-ttu-id="19712-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="19712-113">Example</span></span>

<span data-ttu-id="19712-114">ICE63 meldet den folgenden Fehler für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="19712-114">ICE63 reports the following error for the example shown.</span></span>

``` syntax
WARNING: Some action falls between InstallInitialize and RemoveExistingProducts.
```

<span data-ttu-id="19712-115">Die Aktion "MyCustomAction" erfolgt zwischen "InstallInitialize" und "RemoveExistingProducts".</span><span class="sxs-lookup"><span data-stu-id="19712-115">The action 'MyCustomAction' occurs between InstallInitialize and RemoveExistingProducts.</span></span> <span data-ttu-id="19712-116">Wenn MyCustomAction Aktionen im Skript generiert, verursacht dies Probleme bei der Installation.</span><span class="sxs-lookup"><span data-stu-id="19712-116">If MyCustomAction generates any actions in the script, this causes problems in the installation.</span></span>

<span data-ttu-id="19712-117">Um diesen Fehler zu beheben, überprüfen Sie, ob MyCustomAction keine Skript Aktionen generiert oder die Aktionen neu sequenziert.</span><span class="sxs-lookup"><span data-stu-id="19712-117">To fix this error, verify that MyCustomAction does not generate any script actions or resequence the actions.</span></span>

[<span data-ttu-id="19712-118">InstallExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="19712-118">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="19712-119">Aktion</span><span class="sxs-lookup"><span data-stu-id="19712-119">Action</span></span>                 | <span data-ttu-id="19712-120">Bedingung</span><span class="sxs-lookup"><span data-stu-id="19712-120">Condition</span></span> | <span data-ttu-id="19712-121">Sequenz</span><span class="sxs-lookup"><span data-stu-id="19712-121">Sequence</span></span> |
|------------------------|-----------|----------|
| <span data-ttu-id="19712-122">Installinitialisieren</span><span class="sxs-lookup"><span data-stu-id="19712-122">InstallInitialize</span></span>      |           | <span data-ttu-id="19712-123">1000</span><span class="sxs-lookup"><span data-stu-id="19712-123">1000</span></span>     |
| <span data-ttu-id="19712-124">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="19712-124">MyCustomAction</span></span>         |           | <span data-ttu-id="19712-125">1010</span><span class="sxs-lookup"><span data-stu-id="19712-125">1010</span></span>     |
| <span data-ttu-id="19712-126">RemoveExistingProducts</span><span class="sxs-lookup"><span data-stu-id="19712-126">RemoveExistingProducts</span></span> |           | <span data-ttu-id="19712-127">1020</span><span class="sxs-lookup"><span data-stu-id="19712-127">1020</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="19712-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="19712-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19712-129">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="19712-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



