---
title: Beispiel für Aufzählung von Aufgaben
description: Zum Auflisten von Tasks müssen Sie die itaskscheduler-Enumeration zum Erstellen eines Enumerationsobjekt aufruft. Verwenden Sie dann die ienumworkitems-Schnittstelle des enumerationsobjeders, um die Aufgaben im Ordner "geplante Aufgaben" aufzuzählen.
ms.assetid: 65a8a8af-f4d8-4948-8dd4-b592f1381bfe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd929ebd7d8e9f1a3c372ce212d63dcb29df82b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338481"
---
# <a name="enumerating-tasks-example"></a><span data-ttu-id="37cb8-104">Beispiel für Aufzählung von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="37cb8-104">Enumerating Tasks Example</span></span>

<span data-ttu-id="37cb8-105">Zum Aufzählen von Tasks müssen Sie [**itaskscheduler:: Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) zum Erstellen eines [*Enumerationsobjekt*](e.md)abrufen.</span><span class="sxs-lookup"><span data-stu-id="37cb8-105">To enumerate tasks, you must call [**ITaskScheduler::Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) to create an [*enumeration object*](e.md).</span></span> <span data-ttu-id="37cb8-106">Verwenden Sie dann die [**ienumworkitems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) -Schnittstelle des enumerationsobjeders, um die Aufgaben im Ordner "geplante Aufgaben" aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="37cb8-106">Then, use the enumeration object's [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) interface to enumerate the tasks in the Scheduled Tasks folder.</span></span>

<span data-ttu-id="37cb8-107">Im folgenden Verfahren wird beschrieben, wie die Tasks im Ordner "geplante Aufgaben" aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="37cb8-107">The following procedure describes how to enumerate the tasks in the Scheduled Tasks folder.</span></span>

<span data-ttu-id="37cb8-108">**So zählen Sie die Tasks im Ordner "geplante Aufgaben" auf**</span><span class="sxs-lookup"><span data-stu-id="37cb8-108">**To enumerate the tasks in the Scheduled Tasks folder**</span></span>

1.  <span data-ttu-id="37cb8-109">Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts.</span><span class="sxs-lookup"><span data-stu-id="37cb8-109">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="37cb8-110">(In diesem Beispiel wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)</span><span class="sxs-lookup"><span data-stu-id="37cb8-110">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="37cb8-111">Zum Abrufen eines Enumerationsobjekt muss [**itaskscheduler:: Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="37cb8-111">Call [**ITaskScheduler::Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) to get an enumeration object.</span></span>
3.  <span data-ttu-id="37cb8-112">Rufen Sie [**ienumworkitems:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) auf, um die Aufgaben abzurufen.</span><span class="sxs-lookup"><span data-stu-id="37cb8-112">Call [**IEnumWorkItems::Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) to retrieve the tasks.</span></span> <span data-ttu-id="37cb8-113">(In diesem Beispiel wird versucht, fünf Aufgaben mit jedem-Befehl abzurufen.)</span><span class="sxs-lookup"><span data-stu-id="37cb8-113">(This example tries to retrieve five tasks with each call.)</span></span>
4.  <span data-ttu-id="37cb8-114">Verarbeiten Sie die zurückgegebenen Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="37cb8-114">Process the tasks returned.</span></span> <span data-ttu-id="37cb8-115">(In diesem Beispiel wird einfach der Name der einzelnen Aufgaben auf dem Bildschirm ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="37cb8-115">(This example simply prints the name of each task to the screen.</span></span>
5.  <span data-ttu-id="37cb8-116">Freigeben von Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="37cb8-116">Release resources.</span></span> <span data-ttu-id="37cb8-117">[**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) aufrufen, um den für Namen verwendeten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="37cb8-117">Call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory used for names.</span></span>



| <span data-ttu-id="37cb8-118">Ein Codebeispiel für</span><span class="sxs-lookup"><span data-stu-id="37cb8-118">For a code example of</span></span>                                                         | <span data-ttu-id="37cb8-119">Siehe</span><span class="sxs-lookup"><span data-stu-id="37cb8-119">See</span></span>                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="37cb8-120">Auflisten aller Aufgaben im Ordner "geplante Aufgaben" des lokalen Computers</span><span class="sxs-lookup"><span data-stu-id="37cb8-120">Enumerating all the tasks in the Scheduled Tasks folder of the local computer</span></span> | [<span data-ttu-id="37cb8-121">C/C++-Code Beispiel: Auflisten von Tasks</span><span class="sxs-lookup"><span data-stu-id="37cb8-121">C/C++ Code Example: Enumerating Tasks</span></span>](c-c-code-example-enumerating-tasks.md) |



 

## <a name="related-topics"></a><span data-ttu-id="37cb8-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="37cb8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37cb8-123">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="37cb8-123">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 