---
description: ICE08 überprüft, ob die Komponenten Tabelle doppelte GUIDs enthält. Jede Komponente muss eine eindeutige GUID aufweisen. Wenn die Komponenten Tabelle nicht vorhanden ist, wird keine Validierung durchgeführt.
ms.assetid: c8ff53f3-6587-479d-afb8-b09d0df3b673
title: ICE08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051f32aa983fdae39fc3717d3c9036b542f14369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349502"
---
# <a name="ice08"></a><span data-ttu-id="6d539-105">ICE08</span><span class="sxs-lookup"><span data-stu-id="6d539-105">ICE08</span></span>

<span data-ttu-id="6d539-106">ICE08 überprüft, ob die [Komponenten Tabelle](component-table.md) doppelte [GUIDs](guid.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="6d539-106">ICE08 validates that the [Component table](component-table.md) contains no duplicate [GUIDs](guid.md).</span></span> <span data-ttu-id="6d539-107">Jede Komponente muss eine eindeutige GUID aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6d539-107">Every component must have a unique GUID.</span></span> <span data-ttu-id="6d539-108">Wenn die Komponenten Tabelle nicht vorhanden ist, wird keine Validierung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d539-108">No validation is done if the Component table does not exist.</span></span>

## <a name="result"></a><span data-ttu-id="6d539-109">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="6d539-109">Result</span></span>

<span data-ttu-id="6d539-110">ICE08 gibt eine Fehlermeldung aus, wenn mindestens zwei Einträge in der ComponentID-Spalte der Komponenten Tabelle dieselbe GUID enthalten.</span><span class="sxs-lookup"><span data-stu-id="6d539-110">ICE08 posts an error message if two or more entries in the ComponentId column of the Component table contain the same GUID.</span></span>

## <a name="example"></a><span data-ttu-id="6d539-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6d539-111">Example</span></span>

<span data-ttu-id="6d539-112">Im folgenden Beispiel würde ICE08 eine Meldung veröffentlichen, die besagt, dass die Komponenten rot und grün doppelte GUIDs aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6d539-112">For the following example, ICE08 would post a message stating that components Red and Green have duplicate GUIDs.</span></span>

<span data-ttu-id="6d539-113">[Komponenten Tabelle](component-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="6d539-113">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="6d539-114">Komponente</span><span class="sxs-lookup"><span data-stu-id="6d539-114">Component</span></span> | <span data-ttu-id="6d539-115">ComponentID</span><span class="sxs-lookup"><span data-stu-id="6d539-115">ComponentId</span></span>                            |
|-----------|----------------------------------------|
| <span data-ttu-id="6d539-116">Red</span><span class="sxs-lookup"><span data-stu-id="6d539-116">Red</span></span>       | <span data-ttu-id="6d539-117">{0000000A-0003-0000-0000-624474736554}</span><span class="sxs-lookup"><span data-stu-id="6d539-117">{0000000A-0003-0000-0000-624474736554}</span></span> |
| <span data-ttu-id="6d539-118">Blau</span><span class="sxs-lookup"><span data-stu-id="6d539-118">Blue</span></span>      | <span data-ttu-id="6d539-119">{0000000A-0003-0000-0000-624474736354}</span><span class="sxs-lookup"><span data-stu-id="6d539-119">{0000000A-0003-0000-0000-624474736354}</span></span> |
| <span data-ttu-id="6d539-120">Grün</span><span class="sxs-lookup"><span data-stu-id="6d539-120">Green</span></span>     | <span data-ttu-id="6d539-121">{0000000A-0003-0000-0000-624474736554}</span><span class="sxs-lookup"><span data-stu-id="6d539-121">{0000000A-0003-0000-0000-624474736554}</span></span> |



 

<span data-ttu-id="6d539-122">Um diesen Fehler zu beheben, ändern Sie eine der doppelten GUIDs.</span><span class="sxs-lookup"><span data-stu-id="6d539-122">To fix this error, change either of the duplicate GUIDs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d539-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d539-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d539-124">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="6d539-124">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



