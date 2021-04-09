---
title: Abrufen einer Aufgabenseite (Beispiel)
description: Zum Abrufen einer Aufgabenseite müssen Sie ITask QueryInterface aufrufen, um die iprovidetaskpage-Schnittstelle abzurufen, und dann iprovidetaskpage GetPage aufrufen. Die GetPage-Methode gibt ein Handle für die Seite zurück, die dann zum Anzeigen der angeforderten Seite verwendet werden kann.
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- Abrufen der Aufgabenseite Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd570edf3309b9b9ff0eada291d02a10850885ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039157"
---
# <a name="retrieving-a-task-page-example"></a><span data-ttu-id="f5c6a-105">Abrufen einer Aufgabenseite (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="f5c6a-105">Retrieving a Task Page Example</span></span>

<span data-ttu-id="f5c6a-106">Zum Abrufen einer Aufgabenseite müssen Sie **ITask:: QueryInterface** aufrufen, um die [**iprovidetaskpage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) -Schnittstelle abzurufen, und dann [**iprovidetaskpage:: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f5c6a-106">To retrieve a task page you must call **ITask::QueryInterface** to retrieve the [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) interface, then call [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage).</span></span> <span data-ttu-id="f5c6a-107">Die **GetPage** -Methode gibt ein Handle für die Seite zurück, die dann zum Anzeigen der angeforderten Seite verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f5c6a-107">The **GetPage** method returns a handle to the page, which can then be used to display the page you requested.</span></span>

> [!Note]  
> <span data-ttu-id="f5c6a-108">Im folgenden Codebeispiel werden alle Schnittstellen freigegeben, nachdem Sie nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="f5c6a-108">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="f5c6a-109">Im folgenden Verfahren wird das Erstellen eines neuen-Auslösers beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f5c6a-109">The following procedure describes how to create a new trigger.</span></span>

<span data-ttu-id="f5c6a-110">**So erstellen Sie einen neuen-Auslösung**</span><span class="sxs-lookup"><span data-stu-id="f5c6a-110">**To create a new trigger**</span></span>

1.  <span data-ttu-id="f5c6a-111">Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts.</span><span class="sxs-lookup"><span data-stu-id="f5c6a-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="f5c6a-112">(In diesem Beispiel wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)</span><span class="sxs-lookup"><span data-stu-id="f5c6a-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="f5c6a-113">Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f5c6a-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="f5c6a-114">(Beachten Sie, dass in diesem Beispiel die Aufgabe "Test Aufgabe" abgerufen wird.)</span><span class="sxs-lookup"><span data-stu-id="f5c6a-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="f5c6a-115">Rufen Sie **ITask:: QueryInterface** auf, um die [**iprovidetaskpage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) -Schnittstelle und [**iprovidetaskpage:: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) zum Abrufen der Seite abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f5c6a-115">Call **ITask::QueryInterface** to retrieve the [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) interface and [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) to retrieve the page.</span></span>
4.  <span data-ttu-id="f5c6a-116">Zeigen Sie mit dem zurückgegebenen Seiten Handle die Seite an.</span><span class="sxs-lookup"><span data-stu-id="f5c6a-116">Using the returned page handle, display the page.</span></span>



| <span data-ttu-id="f5c6a-117">Ein Codebeispiel für</span><span class="sxs-lookup"><span data-stu-id="f5c6a-117">For a code example of</span></span>                                   | <span data-ttu-id="f5c6a-118">Siehe</span><span class="sxs-lookup"><span data-stu-id="f5c6a-118">See</span></span>                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="f5c6a-119">Abrufen und Anzeigen der Aufgabenseite einer bekannten Aufgabe</span><span class="sxs-lookup"><span data-stu-id="f5c6a-119">Retrieving and displaying the Task page of a known task</span></span> | [<span data-ttu-id="f5c6a-120">Abrufen einer Aufgabenseite</span><span class="sxs-lookup"><span data-stu-id="f5c6a-120">Retrieving a Task Page</span></span>](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a><span data-ttu-id="f5c6a-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f5c6a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5c6a-122">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5c6a-122">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 