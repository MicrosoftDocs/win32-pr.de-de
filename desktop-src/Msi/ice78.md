---
description: ICE78 überprüft, ob die Tabelle advtuisequence entweder nicht vorhanden oder leer ist. Dies ist erforderlich, da während der Werbung keine Benutzeroberfläche zulässig ist.
ms.assetid: 8ed1c68f-331d-42f9-80df-bdcb42962482
title: ICE78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8993a0a03b0f70bf2d99511782bc9b7d259d4c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129968"
---
# <a name="ice78"></a><span data-ttu-id="7a2ab-104">ICE78</span><span class="sxs-lookup"><span data-stu-id="7a2ab-104">ICE78</span></span>

<span data-ttu-id="7a2ab-105">ICE78 überprüft, ob die [Tabelle advtuisequence](advtuisequence-table.md) entweder nicht vorhanden oder leer ist.</span><span class="sxs-lookup"><span data-stu-id="7a2ab-105">ICE78 verifies that the [AdvtUISequence table](advtuisequence-table.md) either does not exist or is empty.</span></span> <span data-ttu-id="7a2ab-106">Dies ist erforderlich, da während der Werbung keine Benutzeroberfläche zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="7a2ab-106">This is required because no user interface is allowed during advertising.</span></span>

## <a name="result"></a><span data-ttu-id="7a2ab-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="7a2ab-107">Result</span></span>

<span data-ttu-id="7a2ab-108">ICE78 gibt einen Fehler aus, wenn die advtuisequence-Tabelle vorhanden und nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="7a2ab-108">ICE78 posts an error if the AdvtUISequence table exists and is not empty.</span></span>

## <a name="example"></a><span data-ttu-id="7a2ab-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7a2ab-109">Example</span></span>

<span data-ttu-id="7a2ab-110">ICE78 meldet den folgenden Fehler für das Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7a2ab-110">ICE78 reports the following error for the example:</span></span>

<span data-ttu-id="7a2ab-111">Die Aktion ' Action1 ' wurde in der advtuisequence-Tabelle gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a2ab-111">Action 'Action1' found in AdvtUISequence table.</span></span> <span data-ttu-id="7a2ab-112">Während der Werbung ist keine Benutzeroberfläche zulässig.</span><span class="sxs-lookup"><span data-stu-id="7a2ab-112">No UI is allowed during advertising.</span></span> <span data-ttu-id="7a2ab-113">Daher muss die advtuisequence-Tabelle leer sein oder nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="7a2ab-113">Therefore AdvtUISequence table must be empty or not present.</span></span>

<span data-ttu-id="7a2ab-114">[Advtuisequence-Tabelle](advtuisequence-table.md)(partiell)</span><span class="sxs-lookup"><span data-stu-id="7a2ab-114">[AdvtUISequence table](advtuisequence-table.md)(partial)</span></span>



| <span data-ttu-id="7a2ab-115">Aktion</span><span class="sxs-lookup"><span data-stu-id="7a2ab-115">Action</span></span>  | <span data-ttu-id="7a2ab-116">Bedingung</span><span class="sxs-lookup"><span data-stu-id="7a2ab-116">Condition</span></span> | <span data-ttu-id="7a2ab-117">Sequenz</span><span class="sxs-lookup"><span data-stu-id="7a2ab-117">Sequence</span></span> |
|---------|-----------|----------|
| <span data-ttu-id="7a2ab-118">Action1</span><span class="sxs-lookup"><span data-stu-id="7a2ab-118">Action1</span></span> | <span data-ttu-id="7a2ab-119">TRUE</span><span class="sxs-lookup"><span data-stu-id="7a2ab-119">TRUE</span></span>      | <span data-ttu-id="7a2ab-120">1</span><span class="sxs-lookup"><span data-stu-id="7a2ab-120">1</span></span>        |



 

<span data-ttu-id="7a2ab-121">Um den Fehler zu beheben, entfernen Sie entweder "Action1" aus der Tabelle, oder entfernen Sie die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7a2ab-121">To fix the error, either remove "Action1" from the table, or remove the table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a2ab-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7a2ab-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a2ab-123">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="7a2ab-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



