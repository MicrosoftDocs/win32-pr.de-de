---
description: Das Netzwerkmonitor SDK umfasst die Funktionen und den Beispielcode, die Sie zum Erstellen von Experten benötigen. Sie können jedoch auch vorhandene Tools verwenden, einschließlich eines Dialog-Editors.
ms.assetid: 6a3834b7-753f-42cc-986f-3d7e8bf79fd9
title: Programmieren eines Experten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df633d971558f9b14374680b09a22771e10ea0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131461"
---
# <a name="programming-an-expert"></a><span data-ttu-id="1a1e2-104">Programmieren eines Experten</span><span class="sxs-lookup"><span data-stu-id="1a1e2-104">Programming an Expert</span></span>

<span data-ttu-id="1a1e2-105">Das Netzwerkmonitor SDK umfasst die Funktionen und den Beispielcode, die Sie zum Erstellen von Experten benötigen.</span><span class="sxs-lookup"><span data-stu-id="1a1e2-105">The Network Monitor SDK includes the functions and sample code you need to build experts.</span></span> <span data-ttu-id="1a1e2-106">Sie können jedoch auch vorhandene Tools verwenden, einschließlich eines Dialog-Editors.</span><span class="sxs-lookup"><span data-stu-id="1a1e2-106">However, you can also use existing tools, including a dialog editor.</span></span>

## <a name="minimum-requirements-to-run-an-expert"></a><span data-ttu-id="1a1e2-107">Mindestanforderungen für das Ausführen eines Experten</span><span class="sxs-lookup"><span data-stu-id="1a1e2-107">Minimum Requirements to Run an Expert</span></span>

<span data-ttu-id="1a1e2-108">In der folgenden Tabelle sind die DLL-Einstiegspunkte und die Expertenfunktionen aufgelistet, die Sie zum Erstellen eines Experten verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="1a1e2-108">The following table lists the DLL entry points and expert functions you must use to build an expert.</span></span>



| <span data-ttu-id="1a1e2-109">Name</span><span class="sxs-lookup"><span data-stu-id="1a1e2-109">Name</span></span>                                                 | <span data-ttu-id="1a1e2-110">type</span><span class="sxs-lookup"><span data-stu-id="1a1e2-110">Type</span></span>               | <span data-ttu-id="1a1e2-111">Erforderlich?</span><span class="sxs-lookup"><span data-stu-id="1a1e2-111">Required?</span></span>                                       |
|------------------------------------------------------|--------------------|-------------------------------------------------|
| [<span data-ttu-id="1a1e2-112">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="1a1e2-112">**DllMain**</span></span>](dllmain-expert.md)                    | <span data-ttu-id="1a1e2-113">DLL-Einstiegs Funktion</span><span class="sxs-lookup"><span data-stu-id="1a1e2-113">DLL entry function</span></span> | <span data-ttu-id="1a1e2-114">Ja</span><span class="sxs-lookup"><span data-stu-id="1a1e2-114">Yes</span></span>                                             |
| [<span data-ttu-id="1a1e2-115">**Experte registrieren**</span><span class="sxs-lookup"><span data-stu-id="1a1e2-115">**Register Expert**</span></span>](register-expert.md)           | <span data-ttu-id="1a1e2-116">DLL-Einstiegs Funktion</span><span class="sxs-lookup"><span data-stu-id="1a1e2-116">DLL entry function</span></span> | <span data-ttu-id="1a1e2-117">Ja</span><span class="sxs-lookup"><span data-stu-id="1a1e2-117">Yes</span></span>                                             |
| [<span data-ttu-id="1a1e2-118">**Ausführen**</span><span class="sxs-lookup"><span data-stu-id="1a1e2-118">**Run**</span></span>](run.md)                                   | <span data-ttu-id="1a1e2-119">DLL-Einstiegs Funktion</span><span class="sxs-lookup"><span data-stu-id="1a1e2-119">DLL entry function</span></span> | <span data-ttu-id="1a1e2-120">Ja</span><span class="sxs-lookup"><span data-stu-id="1a1e2-120">Yes</span></span>                                             |
| [<span data-ttu-id="1a1e2-121">**Konfigurieren**</span><span class="sxs-lookup"><span data-stu-id="1a1e2-121">**Configure**</span></span>](configure.md)                       | <span data-ttu-id="1a1e2-122">DLL-Einstiegs Funktion</span><span class="sxs-lookup"><span data-stu-id="1a1e2-122">DLL entry function</span></span> | <span data-ttu-id="1a1e2-123">Nur, wenn der Experte die Benutzerkonfiguration bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="1a1e2-123">Only if the expert provides user configuration.</span></span> |
| [<span data-ttu-id="1a1e2-124">**Profil Status**</span><span class="sxs-lookup"><span data-stu-id="1a1e2-124">**ExpertIndicateStatus**</span></span>](expertindicatestatus.md) | <span data-ttu-id="1a1e2-125">Expertenfunktion</span><span class="sxs-lookup"><span data-stu-id="1a1e2-125">Expert function</span></span>    | <span data-ttu-id="1a1e2-126">Ja</span><span class="sxs-lookup"><span data-stu-id="1a1e2-126">Yes</span></span>                                             |
| [<span data-ttu-id="1a1e2-127">**ExpertSubmitEvent**</span><span class="sxs-lookup"><span data-stu-id="1a1e2-127">**ExpertSubmitEvent**</span></span>](expertsubmitevent.md)       | <span data-ttu-id="1a1e2-128">Expertenfunktion</span><span class="sxs-lookup"><span data-stu-id="1a1e2-128">Expert function</span></span>    | <span data-ttu-id="1a1e2-129">Ja</span><span class="sxs-lookup"><span data-stu-id="1a1e2-129">Yes</span></span>                                             |



 

<span data-ttu-id="1a1e2-130">Sehen Sie sich die Referenz Themen für Experten und Parser im Netzwerkmonitor SDK an, um den Quellcode zu aktualisieren, und verwenden Sie dann den Beispielcode und die in den folgenden Themen aufgeführten Prozeduren:</span><span class="sxs-lookup"><span data-stu-id="1a1e2-130">Review the expert and parser reference topics in the Network Monitor SDK to update your source code and then use the sample code and procedures provided in these topics:</span></span>

-   [<span data-ttu-id="1a1e2-131">Entwickeln eines Experten</span><span class="sxs-lookup"><span data-stu-id="1a1e2-131">Building an Expert</span></span>](building-an-expert.md)
-   [<span data-ttu-id="1a1e2-132">Installieren eines Experten</span><span class="sxs-lookup"><span data-stu-id="1a1e2-132">Installing an Expert</span></span>](installing-an-expert-to-network-monitor-2-1.md)
-   [<span data-ttu-id="1a1e2-133">Debuggen eines Experten</span><span class="sxs-lookup"><span data-stu-id="1a1e2-133">Debugging an Expert</span></span>](debugging-an-expert.md)

<span data-ttu-id="1a1e2-134">Experten-DLLs benötigen C, nicht die C++-Aufruf Konvention, da Funktionen über eine Überlagerung durch Funktionszeiger aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1a1e2-134">Expert DLLs require the C, not the C++, calling convention because functions are called through function pointers by using an overlay.</span></span> <span data-ttu-id="1a1e2-135">Durch eine Reihe von spezialisierten Expertenfunktionen hat der Experte Zugriff auf die Frames in der Erfassung.</span><span class="sxs-lookup"><span data-stu-id="1a1e2-135">Through a set of specialized expert functions, the expert has access to the frames in the capture.</span></span> <span data-ttu-id="1a1e2-136">Der Experte kann den größten Teil der Netzwerkmonitor-API verwenden, um die zurückgegebenen Daten zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="1a1e2-136">The expert can use most of the Network Monitor API to manipulate the returned data.</span></span> <span data-ttu-id="1a1e2-137">Wenn ein Experte Informationen findet, die an den Benutzer gesendet werden, werden die Informationen in einer Ereignisdaten Struktur verpackt und an Netzwerkmonitor gesendet, die dann die Informationen in einem expertenausgabe Fenster anzeigt.</span><span class="sxs-lookup"><span data-stu-id="1a1e2-137">When an expert finds information to send to the user, it packages the information in an event data structure and submits it to Network Monitor, which then displays the information in an expert output window.</span></span> <span data-ttu-id="1a1e2-138">Der Experte muss Netzwerkmonitor in regelmäßigen Abständen mit Statusinformationen für den Prozentsatz aktualisieren, die von [**der Funktion "**](expertindicatestatus.md) Funktion" von "-Funktion" bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1a1e2-138">The expert must periodically update Network Monitor with percentage-completion status information, which is provided by the [**ExpertIndicateStatus**](expertindicatestatus.md) function.</span></span>

<span data-ttu-id="1a1e2-139">Die exportierten Funktionen des Experten werden wie folgt aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="1a1e2-139">The expert's exported functions are called as follows:</span></span>

-   <span data-ttu-id="1a1e2-140">Wenn Netzwerkmonitor die Liste der Experten erstellt, die dem Benutzer präsentiert werden sollen, ruft Netzwerkmonitor die [**Register-expertenfunktion**](register-expert.md) auf.</span><span class="sxs-lookup"><span data-stu-id="1a1e2-140">When Network Monitor is creating the list of experts to present to the user, Network Monitor calls the [**Register Expert**](register-expert.md) function.</span></span>
-   <span data-ttu-id="1a1e2-141">Wenn der Experte nach dem Aufruf von " **Register**" konfigurierbar ist, wird Netzwerkmonitor die Funktion " [**configure**](configure.md) " aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1a1e2-141">After the call to **Register**, if the expert is configurable, Network Monitor calls the [**Configure**](configure.md) function.</span></span>
-   <span data-ttu-id="1a1e2-142">Wenn der Netzwerkmonitor Benutzer auf " **Experte ausführen**" klickt, ruft Netzwerkmonitor die Funktion " [**Run**](run.md) " auf.</span><span class="sxs-lookup"><span data-stu-id="1a1e2-142">When the Network Monitor user clicks **Run Expert**, Network Monitor calls the [**Run**](run.md) function.</span></span>

<span data-ttu-id="1a1e2-143">Wenn Experten die angeforderten Frames analysieren und ein Problem finden, verwenden Sie " [**ExpertSubmitEvent**](expertsubmitevent.md) ", um ein Ereignis zu senden, das Informationen zum Problem enthält.</span><span class="sxs-lookup"><span data-stu-id="1a1e2-143">When experts analyze the requested frames and find a problem, they use [**ExpertSubmitEvent**](expertsubmitevent.md) to submit an event that contains information about the problem.</span></span> <span data-ttu-id="1a1e2-144">Netzwerkmonitor verteilt das Ereignis entweder an den standardmäßigen (freigegebenen) Ereignisanzeige oder (sofern der Experte für das Ereignis registriert) für eine private Ereignisanzeige.</span><span class="sxs-lookup"><span data-stu-id="1a1e2-144">Network Monitor distributes the event to either the standard (shared) Event Viewer or (if the expert registers for it) to a private Event Viewer.</span></span>

 

 



