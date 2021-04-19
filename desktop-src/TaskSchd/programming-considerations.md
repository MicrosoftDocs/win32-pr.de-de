---
title: Überlegungen zur Programmierung (Taskplaner)
description: Beachten Sie beim Entwickeln von Anwendungen, die den Taskplaner 1,0 verwenden, die folgenden Programmierprobleme. Die Anwendung muss sicherstellen, dass der Taskplaner-Dienst ausgeführt wird, bevor versucht wird, mithilfe der Taskplaner-API Aufrufe durchführen. Wenn Sie Zeichen folgen abrufen, stellen Sie sicher, dass Sie "CoTaskMemFree" aufrufen, um jede Zeichenfolge freizugeben, nachdem Sie nicht mehr benötigt wird. Wenn Sie Arrays von Zeichen folgen abrufen, stellen Sie sicher, dass Sie zuerst jede Zeichenfolge im Array freigeben und dann das Array selbst freigeben. Wenn Sie ein Arbeits Element erstellen oder ändern, einschließlich Triggern, die mit einem Arbeits Element verknüpft sind, stellen Sie sicher, dass Sie IPersistFile speichern, um die Arbeitsaufgabe auf dem Datenträger zu speichern. Nachdem Sie eine der Schnittstellen verwendet haben, die von der Taskplaner-API bereitgestellt werden, stellen Sie sicher, dass Sie die IUnknown-Freigabe zum Freigeben der Schnittstelle IUnknown wird von jedem Taskplaner Objekt unterstützt.
ms.assetid: b9e1806c-acfa-4d44-a371-91bad788648c
keywords:
- Starten Taskplaner
- Überlegungen zur Programmierung Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599652f4a25f3d99020eda0846c41904ee76e5cf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106339109"
---
# <a name="programming-considerations-task-scheduler"></a><span data-ttu-id="c56b9-107">Überlegungen zur Programmierung (Taskplaner)</span><span class="sxs-lookup"><span data-stu-id="c56b9-107">Programming Considerations (Task Scheduler)</span></span>

<span data-ttu-id="c56b9-108">Beachten Sie beim Entwickeln von Anwendungen, die den Taskplaner 1,0 verwenden, die folgenden Programmierprobleme.</span><span class="sxs-lookup"><span data-stu-id="c56b9-108">When developing applications that use the Task Scheduler 1.0, keep the following programming issues in mind.</span></span>

-   <span data-ttu-id="c56b9-109">Die Anwendung muss sicherstellen, dass der Taskplaner-Dienst ausgeführt wird, bevor versucht wird, mithilfe der Taskplaner-API Aufrufe durchführen.</span><span class="sxs-lookup"><span data-stu-id="c56b9-109">Your application must ensure the Task Scheduler service is running before attempting to make any calls using the Task Scheduler API.</span></span>
-   <span data-ttu-id="c56b9-110">Wenn Sie Zeichen folgen abrufen, stellen Sie sicher, dass Sie " [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) " aufrufen, um jede Zeichenfolge freizugeben, nachdem Sie nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="c56b9-110">When retrieving strings, make sure that you call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to release each string after it is no longer needed.</span></span> <span data-ttu-id="c56b9-111">Wenn Sie Arrays von Zeichen folgen abrufen, stellen Sie sicher, dass Sie zuerst jede Zeichenfolge im Array freigeben und dann das Array selbst freigeben.</span><span class="sxs-lookup"><span data-stu-id="c56b9-111">When retrieving arrays of strings, make sure you first release each string in the array and then release the array itself.</span></span>
-   <span data-ttu-id="c56b9-112">Wenn Sie ein Arbeits Element erstellen oder ändern, einschließlich Triggern, die mit einem Arbeits Element verknüpft sind, stellen Sie sicher, dass Sie [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) zum Speichern der Arbeitsaufgabe auf dem Datenträger aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="c56b9-112">When creating or modifying a work item, including triggers associated with a work item, make sure you call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to save the work item to disk.</span></span>
-   <span data-ttu-id="c56b9-113">Nachdem Sie eine der Schnittstellen verwendet haben, die von der Taskplaner-API bereitgestellt werden, stellen Sie sicher, dass Sie [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) zum Freigeben der-Schnittstelle aufruft.</span><span class="sxs-lookup"><span data-stu-id="c56b9-113">After using any of the interfaces that are provided by the Task Scheduler API, make sure you call [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the interface.</span></span> <span data-ttu-id="c56b9-114">[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) wird von jedem Taskplaner Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c56b9-114">[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) is supported by each Task Scheduler object.</span></span>

<span data-ttu-id="c56b9-115">Der Abschnitt using der Taskplaner-Dokumentation enthält zahlreiche Beispiele, die diese Richtlinien befolgen.</span><span class="sxs-lookup"><span data-stu-id="c56b9-115">The Using section of the Task Scheduler documentation provides numerous examples that follow these guidelines.</span></span> <span data-ttu-id="c56b9-116">In der folgenden Tabelle finden Sie einige dieser Beispiele.</span><span class="sxs-lookup"><span data-stu-id="c56b9-116">The table below provides jumps to some of these examples.</span></span>

| <span data-ttu-id="c56b9-117">Beispiel für</span><span class="sxs-lookup"><span data-stu-id="c56b9-117">For an example of</span></span>         | <span data-ttu-id="c56b9-118">Siehe</span><span class="sxs-lookup"><span data-stu-id="c56b9-118">See</span></span>                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c56b9-119">Freigeben von Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="c56b9-119">Releasing strings</span></span>         | [<span data-ttu-id="c56b9-120">Abrufen von Beispielen für Arbeits Element Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c56b9-120">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       |
| <span data-ttu-id="c56b9-121">Arbeitselemente werden auf dem Datenträger gespeichert</span><span class="sxs-lookup"><span data-stu-id="c56b9-121">Saving work items to disk</span></span> | [<span data-ttu-id="c56b9-122">Festlegen von Beispielen für Arbeits Element Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c56b9-122">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             |
| <span data-ttu-id="c56b9-123">Freigeben von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c56b9-123">Releasing interfaces</span></span>      | [<span data-ttu-id="c56b9-124">Erstellen einer Aufgabe mit NewWorkItem-Beispiel</span><span class="sxs-lookup"><span data-stu-id="c56b9-124">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) |



 

 

 
