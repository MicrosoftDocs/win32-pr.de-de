---
description: Einige Anwendungen sind so konzipiert, dass mehrere Instanzen der Anwendung auf einem Computer installiert werden.
ms.assetid: 951d20c8-7908-40d8-a9d5-d321340c97f3
title: Einschränkungen beim Anwendungs Entwurf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c4307a979866e3df9f019e69b858e8347c295b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344954"
---
# <a name="application-design-restrictions"></a><span data-ttu-id="ae164-103">Einschränkungen beim Anwendungs Entwurf</span><span class="sxs-lookup"><span data-stu-id="ae164-103">Application Design Restrictions</span></span>

<span data-ttu-id="ae164-104">Einige Anwendungen sind so konzipiert, dass mehrere Instanzen der Anwendung auf einem Computer installiert werden.</span><span class="sxs-lookup"><span data-stu-id="ae164-104">Some applications are designed in a way that prevents multiple instances of the application from being installed on a computer.</span></span> <span data-ttu-id="ae164-105">Mit einer solchen Einschränkung kann eine Anwendung die Partitions Funktion nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae164-105">With such a limitation, an application cannot make use of the partitions feature.</span></span> <span data-ttu-id="ae164-106">Die folgenden Anwendungs Entwurfs Features müssen möglicherweise geändert werden, bevor Partitionen für diese Anwendung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ae164-106">The following application design features might need to be modified before partitions can be used for that application.</span></span>

## <a name="tables-and-arrays"></a><span data-ttu-id="ae164-107">Tabellen und Arrays</span><span class="sxs-lookup"><span data-stu-id="ae164-107">Tables and Arrays</span></span>

<span data-ttu-id="ae164-108">Einige Anwendungen erstellen Datenbanktabellen, in-Memory-Tabellen oder Arrays, die eine CLSID als eindeutigen Registrierungsschlüssel verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae164-108">Some applications create database tables, in-memory tables, or arrays that use a CLSID as a unique registry key.</span></span> <span data-ttu-id="ae164-109">Auf einem Computer ohne Partitionen lautet dieser Registrierungsschlüssel in der Regel Computer/CLSID (eine CLSID pro Computer).</span><span class="sxs-lookup"><span data-stu-id="ae164-109">On a computer without partitions, this registry key is typically computer/CLSID (one CLSID per computer).</span></span>

<span data-ttu-id="ae164-110">Umgekehrt ist dieser Registrierungsschlüssel auf einem Computer mit Partitionen der Computer/Partitions-ID/Anwendungs-ID/CLSID (mehrere Instanzen einer CLSID pro Computer).</span><span class="sxs-lookup"><span data-stu-id="ae164-110">Conversely, on a computer with partitions, this registry key is computer/partition ID/application ID/CLSID (multiple instances of a CLSID per computer).</span></span> <span data-ttu-id="ae164-111">Da mit der Partitions Funktion mehrere Instanzen einer CLSID auf einem Computer vorhanden sein können, können Anwendungen, die Entwurfs Elemente enthalten, die eine eindeutige CLSID pro Computer erfordern, beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="ae164-111">Because the partitions feature allows multiple instances of a CLSID to exist on a computer, applications that contain design elements that require a unique CLSID per computer might be adversely affected.</span></span>

## <a name="global-resources"></a><span data-ttu-id="ae164-112">Globale Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ae164-112">Global Resources</span></span>

<span data-ttu-id="ae164-113">Einige Anwendungen verwenden globale Ressourcen wie freigegebenen Arbeitsspeicher, Datendateien und Registrierungseinträge.</span><span class="sxs-lookup"><span data-stu-id="ae164-113">Some applications use global resources such as shared memory, data files, and registry entries.</span></span> <span data-ttu-id="ae164-114">Dies kann zu Problemen führen, wenn mehrere Instanzen einer solchen Anwendung gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ae164-114">This could cause problems if multiple instances of such an application are executing simultaneously.</span></span>

<span data-ttu-id="ae164-115">Wenn eine Komponente z. b. gemeinsam genutzten Speicher für die Interaktion mit anderen Komponenten verwendet, muss die Komponente so geändert werden, dass jede Instanz der Komponente ihren eigenen gemeinsam genutzten Speicher zuordnet.</span><span class="sxs-lookup"><span data-stu-id="ae164-115">For example, if a component uses shared memory for interacting with other components, the component will need to be modified so that each instance of the component allocates its own shared memory.</span></span>

## <a name="type-libraries"></a><span data-ttu-id="ae164-116">Typbibliotheken</span><span class="sxs-lookup"><span data-stu-id="ae164-116">Type Libraries</span></span>

<span data-ttu-id="ae164-117">Typbibliotheken stellen Informationen über die Schnittstellen und Methoden einer Komponente bereit.</span><span class="sxs-lookup"><span data-stu-id="ae164-117">Type libraries provide information about a component's interfaces and methods.</span></span> <span data-ttu-id="ae164-118">Diese Informationen werden für verschiedene Zwecke verwendet, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="ae164-118">This information is used for several purposes, including the following:</span></span>

-   <span data-ttu-id="ae164-119">Marshalling von Daten zwischen Komponenten, wenn Funktionsaufrufe durchgeführt werden</span><span class="sxs-lookup"><span data-stu-id="ae164-119">Marshaling data between components when function calls are made</span></span>
-   <span data-ttu-id="ae164-120">Unterstützung der COM+-Komponenten in der Warteschlange und der com+-Ereignis Dienste</span><span class="sxs-lookup"><span data-stu-id="ae164-120">Helping the COM+ Queued Components and COM+ Events services</span></span>
-   <span data-ttu-id="ae164-121">Bereitstellen der richtigen Informationen in einem Microsoft Visual Basic-Editor</span><span class="sxs-lookup"><span data-stu-id="ae164-121">Providing the correct information within a Microsoft Visual Basic editor</span></span>

<span data-ttu-id="ae164-122">Verweise auf eine Typbibliothek werden in der Registrierung eines Computers installiert.</span><span class="sxs-lookup"><span data-stu-id="ae164-122">References to a type library are installed in the registry of a computer.</span></span> <span data-ttu-id="ae164-123">Beim Entwickeln von Anwendungen, die in Partitionen aufgerufen werden, ist es wichtig, dass die aktuelle Version einer Typbibliothek in der Registrierung installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ae164-123">When developing applications that will be invoked from within partitions, it is important that the latest version of a type library is installed in the registry.</span></span> <span data-ttu-id="ae164-124">Dadurch wird sichergestellt, dass der verwendete Visual Basic-Editor genaue Informationen zu den Methoden erhält, die für diese Komponente verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ae164-124">This ensures that the Visual Basic editor being used will get accurate information about the methods available for that component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae164-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ae164-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae164-126">Komponenten und Partitionen in der com+-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="ae164-126">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="ae164-127">Partitions Implementierung</span><span class="sxs-lookup"><span data-stu-id="ae164-127">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="ae164-128">Registrieren und Aktivieren von Komponenten in Partitionen</span><span class="sxs-lookup"><span data-stu-id="ae164-128">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="ae164-129">Was sind COM+-Partitionen?</span><span class="sxs-lookup"><span data-stu-id="ae164-129">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



