---
description: ICE84 überprüft die AdvtExecuteSequence-Tabelle, die AdminExecuteSequence-Tabelle und die InstallExecuteSequence-Tabelle, um zu überprüfen, ob die folgenden Standard Aktionen nicht mit Bedingungen im Bedingungs Feld festgelegt wurden.
ms.assetid: 0d1bbf4b-ffab-409e-a292-891dfa823433
title: ICE84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8960f53f5a01e9bec95a02bb3241487aa31aaae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347778"
---
# <a name="ice84"></a><span data-ttu-id="ee02b-103">ICE84</span><span class="sxs-lookup"><span data-stu-id="ee02b-103">ICE84</span></span>

<span data-ttu-id="ee02b-104">ICE84 überprüft die [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md), die [AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)und die [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) , um zu überprüfen, ob die folgenden [Standard Aktionen](standard-actions.md) nicht mit Bedingungen im Bedingungs Feld festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="ee02b-104">ICE84 checks the [AdvtExecuteSequence table](advtexecutesequence-table.md), [AdminExecuteSequence table](adminexecutesequence-table.md), and the [InstallExecuteSequence table](installexecutesequence-table.md) to verify that the following [standard actions](standard-actions.md) have not been set with conditions in the Condition field.</span></span>

-   [<span data-ttu-id="ee02b-105">Costinitialize-Aktion</span><span class="sxs-lookup"><span data-stu-id="ee02b-105">CostInitialize action</span></span>](costinitialize-action.md)
-   [<span data-ttu-id="ee02b-106">Costfinalize-Aktion</span><span class="sxs-lookup"><span data-stu-id="ee02b-106">CostFinalize action</span></span>](costfinalize-action.md)
-   [<span data-ttu-id="ee02b-107">Filecost-Aktion</span><span class="sxs-lookup"><span data-stu-id="ee02b-107">FileCost action</span></span>](filecost-action.md)
-   [<span data-ttu-id="ee02b-108">InstallValidate-Aktion</span><span class="sxs-lookup"><span data-stu-id="ee02b-108">InstallValidate action</span></span>](installvalidate-action.md)
-   [<span data-ttu-id="ee02b-109">InstallInitialize-Aktion</span><span class="sxs-lookup"><span data-stu-id="ee02b-109">InstallInitialize action</span></span>](installinitialize-action.md)
-   [<span data-ttu-id="ee02b-110">InstallFinalize-Aktion</span><span class="sxs-lookup"><span data-stu-id="ee02b-110">InstallFinalize action</span></span>](installfinalize-action.md)
-   [<span data-ttu-id="ee02b-111">Processcomponents-Aktion</span><span class="sxs-lookup"><span data-stu-id="ee02b-111">ProcessComponents action</span></span>](processcomponents-action.md)
-   [<span data-ttu-id="ee02b-112">Publishfeatures-Aktion</span><span class="sxs-lookup"><span data-stu-id="ee02b-112">PublishFeatures action</span></span>](publishfeatures-action.md)
-   [<span data-ttu-id="ee02b-113">Publishproduct-Aktion</span><span class="sxs-lookup"><span data-stu-id="ee02b-113">PublishProduct action</span></span>](publishproduct-action.md)
-   [<span data-ttu-id="ee02b-114">Registerproduct-Aktion</span><span class="sxs-lookup"><span data-stu-id="ee02b-114">RegisterProduct action</span></span>](registerproduct-action.md)
-   [<span data-ttu-id="ee02b-115">Unpublishfeatures-Aktion</span><span class="sxs-lookup"><span data-stu-id="ee02b-115">UnpublishFeatures action</span></span>](unpublishfeatures-action.md)

<span data-ttu-id="ee02b-116">Wenn Bedingungen gefunden werden, gibt ICE84 eine Warnung aus.</span><span class="sxs-lookup"><span data-stu-id="ee02b-116">If conditions are found, ICE84 posts a warning.</span></span>

## <a name="result"></a><span data-ttu-id="ee02b-117">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="ee02b-117">Result</span></span>

<span data-ttu-id="ee02b-118">ICE84 gibt die folgende Warnung aus.</span><span class="sxs-lookup"><span data-stu-id="ee02b-118">ICE84 posts the following warning.</span></span>



| <span data-ttu-id="ee02b-119">ICE84-Fehler</span><span class="sxs-lookup"><span data-stu-id="ee02b-119">ICE84 error</span></span>                                                             | <span data-ttu-id="ee02b-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee02b-120">Description</span></span>                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="ee02b-121">Die \[ \] in der% s-Tabelle gefundene Aktion ' 1 ' ist eine erforderliche Aktion mit einer Bedingung.</span><span class="sxs-lookup"><span data-stu-id="ee02b-121">Action '\[1\]' found in %s table is a required action with a condition.</span></span> | <span data-ttu-id="ee02b-122">Eine erforderliche Aktion wurde mit einer Bedingung erstellt.</span><span class="sxs-lookup"><span data-stu-id="ee02b-122">A required action has been authored with a condition.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ee02b-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ee02b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee02b-124">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="ee02b-124">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



