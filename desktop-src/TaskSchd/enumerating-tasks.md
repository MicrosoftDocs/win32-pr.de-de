---
title: Auflisten von Tasks
description: Taskplaner 1,0 stellt ein Enumerationsobjekt zum Auflisten der Aufgaben im Ordner "geplante Aufgaben" bereit.
ms.assetid: ccd140a1-06f6-4e6b-afa6-f7ac9b9ff904
keywords:
- Aufzählen von Aufgaben Taskplaner
- Aufzählen von Aufgaben Taskplaner, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dda98cf40bc1ea360d20bcf13084faa692aa22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037257"
---
# <a name="enumerating-tasks"></a><span data-ttu-id="b9e4d-105">Auflisten von Tasks</span><span class="sxs-lookup"><span data-stu-id="b9e4d-105">Enumerating Tasks</span></span>

<span data-ttu-id="b9e4d-106">Taskplaner 1,0 stellt ein Enumerationsobjekt zum Auflisten der Aufgaben im [*Ordner "geplante Aufgaben*](s.md)" bereit.</span><span class="sxs-lookup"><span data-stu-id="b9e4d-106">Task Scheduler 1.0 provides an enumeration object for enumerating the tasks in the [*Scheduled Tasks folder*](s.md).</span></span>

> [!Note]  
> <span data-ttu-id="b9e4d-107">Für einen Computer mit Windows Server 2003, Windows XP oder Windows 2000 zum Erstellen, überwachen oder Steuern von Aufgaben auf einem Computer mit Windows Vista müssen bestimmte Vorgänge auf dem Computer mit Windows Vista ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b9e4d-107">For a Windows Server 2003, Windows XP, or Windows 2000 computer to create, monitor, or control tasks on a Windows Vista computer, certain operations must be completed on the Windows Vista computer.</span></span> <span data-ttu-id="b9e4d-108">Weitere Informationen finden Sie unter [MSBuild-Aufgaben](tasks.md).</span><span class="sxs-lookup"><span data-stu-id="b9e4d-108">For more information, see [Tasks](tasks.md).</span></span>

 

## <a name="using-the-enumeration-object"></a><span data-ttu-id="b9e4d-109">Verwenden des Enumerationsobjekt</span><span class="sxs-lookup"><span data-stu-id="b9e4d-109">Using the Enumeration Object</span></span>

<span data-ttu-id="b9e4d-110">Die [**ienumworkitems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) -Schnittstelle dieses Objekts bietet Methoden zum Auflisten der Aufgaben im Ordner, zum Zurücksetzen der Enumerationsfolge auf den Anfang der Liste, zum Überspringen von Aufgaben und zum Erstellen einer Kopie des aktuellen Enumerationsobjekt für die spätere Verwendung.</span><span class="sxs-lookup"><span data-stu-id="b9e4d-110">The [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) interface of this object provides methods for enumerating the tasks in the folder, resetting the enumeration sequence to the start of the list, skipping tasks, and making a copy of the current enumeration object for later use.</span></span>

<span data-ttu-id="b9e4d-111">Weitere Informationen zum Auflisten der Aufgaben im Ordner "geplante Aufgaben" finden Sie unter [**ienumworkitems:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).</span><span class="sxs-lookup"><span data-stu-id="b9e4d-111">For information about enumerating the tasks in the Scheduled tasks folder, see [**IEnumWorkItems::Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).</span></span>

<span data-ttu-id="b9e4d-112">Weitere Informationen zum Zurücksetzen der Enumeration auf den Anfang der Liste finden Sie unter [**ienumworkitems:: Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).</span><span class="sxs-lookup"><span data-stu-id="b9e4d-112">For information about resetting the enumeration to the start of the list, see [**IEnumWorkItems::Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).</span></span>

<span data-ttu-id="b9e4d-113">Weitere Informationen zum Überspringen von Aufgaben finden Sie unter [**ienumworkitems:: Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).</span><span class="sxs-lookup"><span data-stu-id="b9e4d-113">For information about skipping tasks, see [**IEnumWorkItems::Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).</span></span>

<span data-ttu-id="b9e4d-114">Weitere Informationen zum Erstellen einer Kopie des aktuellen Enumerationsobjekt finden Sie unter [**ienumworkitems:: Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).</span><span class="sxs-lookup"><span data-stu-id="b9e4d-114">For information about making a copy of the current enumeration object, see [**IEnumWorkItems::Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).</span></span>

<span data-ttu-id="b9e4d-115">Ein Beispiel für das Auflisten der Aufgaben im Ordner "geplante Aufgaben" finden Sie unter [Beispiel](enumerating-tasks-example.md)für das Auflisten von Tasks.</span><span class="sxs-lookup"><span data-stu-id="b9e4d-115">For an example of enumerating the tasks in the Scheduled Tasks folder, see [Enumerating Tasks Example](enumerating-tasks-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9e4d-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b9e4d-116">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b9e4d-117">**Licher**</span><span class="sxs-lookup"><span data-stu-id="b9e4d-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b9e4d-118">Aufgabeninformationen Taskplaner 1,0</span><span class="sxs-lookup"><span data-stu-id="b9e4d-118">Task Scheduler 1.0 Task Information</span></span>](task-scheduler-1-0-task-informatation.md)
</dt> </dl>

 

 




