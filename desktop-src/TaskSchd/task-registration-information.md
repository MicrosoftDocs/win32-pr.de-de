---
title: Aufgaben Registrierungsinformationen
description: Registrierungsinformationen bieten eine Möglichkeit, eine Aufgabe auf verschiedene Weise zu identifizieren. Beispielsweise kann eine Aufgabe vom Autor identifiziert werden, wie Sie erstellt wurde (als Aufgaben Quelle bezeichnet) und das Datum der Registrierung.
ms.assetid: 45c9fa99-2718-4202-8987-4b506bd677e9
keywords:
- Registrierungsinformationen Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6c5048e9cbb9b41abcd9052a02371cd575b57c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309195"
---
# <a name="task-registration-information"></a><span data-ttu-id="2b5d3-105">Aufgaben Registrierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="2b5d3-105">Task Registration Information</span></span>

<span data-ttu-id="2b5d3-106">Registrierungsinformationen bieten eine Möglichkeit, eine Aufgabe auf verschiedene Weise zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-106">Registration information provides a way to identify a task in several different ways.</span></span> <span data-ttu-id="2b5d3-107">Beispielsweise kann eine Aufgabe vom Autor identifiziert werden, wie Sie erstellt wurde (als Aufgaben Quelle bezeichnet) und das Datum der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-107">For example, a task can be identified by the author, how it was authored (referred to as the task source), and date of registration.</span></span>

## <a name="using-registration-information"></a><span data-ttu-id="2b5d3-108">Verwenden von Registrierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="2b5d3-108">Using Registration Information</span></span>

<span data-ttu-id="2b5d3-109">Registrierungsinformationen werden in der Regel angegeben, wenn die Aufgabe erstellt und dann auf folgende Weise verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="2b5d3-109">Registration information is typically specified when the task is created and then used in the following ways:</span></span>

-   <span data-ttu-id="2b5d3-110">Wird von der Taskplaner Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-110">Displayed by the Task Scheduler user interface.</span></span>
-   <span data-ttu-id="2b5d3-111">Get oder Set by C++ Applications or Scripts.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-111">Get or set by C++ applications or scripts.</span></span>
-   <span data-ttu-id="2b5d3-112">In einer Unternehmensumgebung, die als Suchkriterium verwendet wird, wenn alle registrierten Tasks aufgezählt werden.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-112">In an enterprise environment, used as a search criteria when enumerating over all registered tasks.</span></span>

## <a name="types-of-registration-information"></a><span data-ttu-id="2b5d3-113">Typen von Registrierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="2b5d3-113">Types of Registration Information</span></span>

<span data-ttu-id="2b5d3-114">Aufgaben Registrierungsinformationen werden durch die Eigenschaften des [**RegistrationInfo**](registrationinfo.md) -Objekts für Skript Anwendungen, die Eigenschaften der [**iregistrationinfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) -Schnittstelle für C++-Anwendungen und die untergeordneten Elemente des [**RegistrationInfo-Elements (TaskType)**](taskschedulerschema-registrationinfo-tasktype-element.md) zum Lesen oder Schreiben von XML definiert.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-114">Task registration information is defined by the properties of the [**RegistrationInfo**](registrationinfo.md) object for scripting applications, the properties of the [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) interface for C++ applications, and the child elements of the [**RegistrationInfo (taskType) element**](taskschedulerschema-registrationinfo-tasktype-element.md) for reading or writing XML.</span></span>

<span data-ttu-id="2b5d3-115">Diese Eigenschaften ermöglichen den Zugriff auf die folgenden Typen von Registrierungsinformationen:</span><span class="sxs-lookup"><span data-stu-id="2b5d3-115">These properties allow access to the following types of registration information:</span></span>

-   <span data-ttu-id="2b5d3-116">Aufgaben Autor</span><span class="sxs-lookup"><span data-stu-id="2b5d3-116">Task Author</span></span>

    <span data-ttu-id="2b5d3-117">Taskplaner legt den Autor der Aufgabe fest, wenn diese erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-117">Task Scheduler sets the author of the task when it is created.</span></span>

-   <span data-ttu-id="2b5d3-118">Registrierungsdatum der Aufgabe</span><span class="sxs-lookup"><span data-stu-id="2b5d3-118">Task Registration Date</span></span>

    <span data-ttu-id="2b5d3-119">Taskplaner legt dieses Datum fest, wenn der Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-119">Task Scheduler sets this date when the task is registered.</span></span>

-   <span data-ttu-id="2b5d3-120">Taskbeschreibung</span><span class="sxs-lookup"><span data-stu-id="2b5d3-120">Task Description</span></span>

    <span data-ttu-id="2b5d3-121">Eine benutzerdefinierte Beschreibung, die möglicherweise einschließt, welche Trigger verwendet werden, um den Task zu starten oder welche Aktionen der Task ausführt.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-121">A user-defined description that may include what triggers are used to start the task or what actions the task performs.</span></span>

-   <span data-ttu-id="2b5d3-122">Task Dokumentation</span><span class="sxs-lookup"><span data-stu-id="2b5d3-122">Task Documentation</span></span>

    <span data-ttu-id="2b5d3-123">Vom Benutzer bereitgestellte Dokumentation, die von der Aufgabe benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-123">User-supplied documentation that is needed by the task.</span></span>

-   <span data-ttu-id="2b5d3-124">Task Sicherheits Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b5d3-124">Task Security Descriptor</span></span>

    <span data-ttu-id="2b5d3-125">Ein vom Benutzer bereitgestellter Sicherheits Deskriptor.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-125">A user-supplied security descriptor.</span></span>

-   <span data-ttu-id="2b5d3-126">Task Quelle</span><span class="sxs-lookup"><span data-stu-id="2b5d3-126">Task Source</span></span>

    <span data-ttu-id="2b5d3-127">Vom Benutzer bereitgestellte Informationen, die den Ursprung der Aufgabe von beschreiben.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-127">User-supplied information that describes where the task originated from.</span></span> <span data-ttu-id="2b5d3-128">Beispielsweise kann eine Aufgabe aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer stammen.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-128">For example, a task may originate from a component, service, application, or user.</span></span>

-   <span data-ttu-id="2b5d3-129">Task-URI</span><span class="sxs-lookup"><span data-stu-id="2b5d3-129">Task URI</span></span>

    <span data-ttu-id="2b5d3-130">Ein URI (Uniform Resource Identifier) für den Task.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-130">A uniform resource identifier (URI) for the task.</span></span>

-   <span data-ttu-id="2b5d3-131">Taskversion</span><span class="sxs-lookup"><span data-stu-id="2b5d3-131">Task Version</span></span>

    <span data-ttu-id="2b5d3-132">Vom Benutzer bereitgestellte Informationen, die verwendet werden, wenn mehrere Versionen einer Aufgabe vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-132">User-supplied information that is used when multiple versions of a task exist.</span></span>

-   <span data-ttu-id="2b5d3-133">XML-Text</span><span class="sxs-lookup"><span data-stu-id="2b5d3-133">XML Text</span></span>

    <span data-ttu-id="2b5d3-134">Eine XML-formatierte Version der Registrierungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-134">An XML-formatted version of the registration information.</span></span> <span data-ttu-id="2b5d3-135">Beachten Sie, dass Sie die Registrierungsinformationen direkt über diesen XML-Code festlegen oder ändern können, und die entsprechenden Objekt-und Schnittstelleneigenschaften werden entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-135">Note that you can set or modify the registration information directly through this XML and the appropriate object and interface properties will be updated accordingly.</span></span>

## <a name="registering-tasks"></a><span data-ttu-id="2b5d3-136">Registrieren von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="2b5d3-136">Registering Tasks</span></span>

<span data-ttu-id="2b5d3-137">Eine Aufgabe kann registriert werden, nachdem die Aufgaben Definitionen erstellt wurden, und Registrierungsinformationen und Einstellungs Werte werden vom Benutzer bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-137">A task can be registered after the task definitions are created and registration information and setting values are supplied by the user.</span></span> <span data-ttu-id="2b5d3-138">Eine Aufgabe wird mithilfe der [**Task Folder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) -Methode für Skript Anwendungen oder der [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) -Methode für C++-Anwendungen registriert.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-138">A task is registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method for scripting applications or the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method for C++ applications.</span></span> <span data-ttu-id="2b5d3-139">Wenn Sie eine Aufgabe mithilfe von XML zum Definieren der Aufgabe registrieren möchten, verwenden Sie die [**Task Folder. RegisterTask**](taskfolder-registertask.md) -Methode für Skript Anwendungen und die [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Methode für C++-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-139">If you want to register a task using XML to define the task, you use the [**TaskFolder.RegisterTask**](taskfolder-registertask.md) method for scripting applications and the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) method for C++ applications.</span></span>

<span data-ttu-id="2b5d3-140">In den oben erwähnten Methoden können Sie den Sicherheitskontext angeben, um den Task auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-140">In the methods mentioned above, you can specify the security context to run the task.</span></span> <span data-ttu-id="2b5d3-141">Sie müssen ein Administrator im System sein, um die Ausführung von Aufträgen in anderen Kontexten als ihren eigenen zu planen.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-141">You have to be an administrator on the system to schedule jobs to run under contexts other than your own.</span></span> <span data-ttu-id="2b5d3-142">Weitere Informationen zu den Sicherheits Kontexten zum Ausführen von Tasks finden Sie unter [Sicherheits Kontexte zum](security-contexts-for-running-tasks.md)Ausführen von Tasks.</span><span class="sxs-lookup"><span data-stu-id="2b5d3-142">For more information on the security contexts to run tasks, see [Security Contexts for Running Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b5d3-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2b5d3-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b5d3-144">Informationen zum Taskplaner</span><span class="sxs-lookup"><span data-stu-id="2b5d3-144">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> <dt>

[<span data-ttu-id="2b5d3-145">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="2b5d3-145">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




