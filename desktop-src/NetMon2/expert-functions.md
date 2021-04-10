---
description: Die folgenden Hilfsfunktionen können nur von Experten aufgerufen werden, die die Funktion "Run" oder "configure" exportieren.
ms.assetid: 6890087c-7c94-41ff-bb5c-4bf88a4e07cc
title: Expertenfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7441289008c7dcd647775c2932e210ccd09b24bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862027"
---
# <a name="expert-functions"></a><span data-ttu-id="52dcc-103">Expertenfunktionen</span><span class="sxs-lookup"><span data-stu-id="52dcc-103">Expert Functions</span></span>

<span data-ttu-id="52dcc-104">Die folgenden Hilfsfunktionen können nur von Experten aufgerufen werden, die die Funktion " [Run](run.md) " oder " [configure](configure.md) " exportieren.</span><span class="sxs-lookup"><span data-stu-id="52dcc-104">The following helper functions can only be called by experts that export the [Run](run.md) or [Configure](configure.md) function.</span></span>



| <span data-ttu-id="52dcc-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="52dcc-105">Function</span></span>                                         | <span data-ttu-id="52dcc-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52dcc-106">Description</span></span>                                                                             |
|--------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="52dcc-107">Expertgetframe</span><span class="sxs-lookup"><span data-stu-id="52dcc-107">ExpertGetFrame</span></span>](expertgetframe.md)             | <span data-ttu-id="52dcc-108">Ruft einen angegebenen Frame aus der Erfassung ab.</span><span class="sxs-lookup"><span data-stu-id="52dcc-108">Retrieves a given frame from the capture.</span></span>                                               |
| [<span data-ttu-id="52dcc-109">Profil Status</span><span class="sxs-lookup"><span data-stu-id="52dcc-109">ExpertIndicateStatus</span></span>](expertindicatestatus.md) | <span data-ttu-id="52dcc-110">Gibt den Prozentsatz des Abschlusses der Analyse der Erfassung durch den Experten an.</span><span class="sxs-lookup"><span data-stu-id="52dcc-110">Indicates the percentage of completion of the expert's analysis of capture.</span></span>             |
| [<span data-ttu-id="52dcc-111">Expertgetstartupinfo</span><span class="sxs-lookup"><span data-stu-id="52dcc-111">ExpertGetStartupInfo</span></span>](expertgetstartupinfo.md) | <span data-ttu-id="52dcc-112">Ruft die Startinformationen für den Experten ab.</span><span class="sxs-lookup"><span data-stu-id="52dcc-112">Retrieves the startup information for the expert.</span></span>                                       |
| [<span data-ttu-id="52dcc-113">Expertmemorysize</span><span class="sxs-lookup"><span data-stu-id="52dcc-113">ExpertMemorySize</span></span>](expertmemorysize.md)         | <span data-ttu-id="52dcc-114">Ruft die Größe des Arbeitsspeichers ab, der durch einen Aufrufe der Funktion " **expertenlocmemory** " zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="52dcc-114">Retrieves the size of memory allocated by a call to the **ExpertAllocMemory** function.</span></span> |
| [<span data-ttu-id="52dcc-115">ExpertSubmitEvent</span><span class="sxs-lookup"><span data-stu-id="52dcc-115">ExpertSubmitEvent</span></span>](expertsubmitevent.md)       | <span data-ttu-id="52dcc-116">Gibt ein Problem an und ruft Informationen über das Problem ab, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="52dcc-116">Indicates a problem and retrieves information about the problem if one exists.</span></span>          |
| [<span data-ttu-id="52dcc-117">"Expertenlocmemory"</span><span class="sxs-lookup"><span data-stu-id="52dcc-117">ExpertAllocMemory</span></span>](expertallocmemory.md)       | <span data-ttu-id="52dcc-118">Weist dem Experten Arbeitsspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="52dcc-118">Allocates memory for the expert.</span></span>                                                        |
| [<span data-ttu-id="52dcc-119">Expertrebelegcmemory</span><span class="sxs-lookup"><span data-stu-id="52dcc-119">ExpertReallocMemory</span></span>](expertreallocmemory.md)   | <span data-ttu-id="52dcc-120">Ändert die Größe des Arbeitsspeichers, der von der Funktion " **expertenlocmemory** " zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="52dcc-120">Changes the size of the memory allocated by the **ExpertAllocMemory** function.</span></span>         |
| [<span data-ttu-id="52dcc-121">Expertenarbeits Speicher</span><span class="sxs-lookup"><span data-stu-id="52dcc-121">ExpertFreeMemory</span></span>](expertfreememory.md)         | <span data-ttu-id="52dcc-122">Gibt vom Experten zugeordnete Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="52dcc-122">Frees memory allocated by the expert.</span></span>                                                   |



 

<span data-ttu-id="52dcc-123">Informationen zu Exportfunktionen und Hilfsfunktionen, die von Experten und Parser, Strukturen und Enumerationen aufgerufen werden können, finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="52dcc-123">For information about export functions, helper functions that can be called by experts and parsers, structures, and enumerations, see the following topics:</span></span>



| <span data-ttu-id="52dcc-124">Informationen über</span><span class="sxs-lookup"><span data-stu-id="52dcc-124">For information about</span></span>                                             | <span data-ttu-id="52dcc-125">Finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="52dcc-125">See</span></span>                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="52dcc-126">Funktionen, die von Experten exportiert werden</span><span class="sxs-lookup"><span data-stu-id="52dcc-126">Functions that are exported by experts</span></span>                            | [<span data-ttu-id="52dcc-127">Export Funktionen der Experten-dll</span><span class="sxs-lookup"><span data-stu-id="52dcc-127">Expert DLL Export Functions</span></span>](expert-dll-export-functions.md)               |
| <span data-ttu-id="52dcc-128">Von Expertenfunktionen verwendete Strukturen</span><span class="sxs-lookup"><span data-stu-id="52dcc-128">Structures that are used by expert functions</span></span>                      | [<span data-ttu-id="52dcc-129">Expertenstrukturen</span><span class="sxs-lookup"><span data-stu-id="52dcc-129">Expert Structures</span></span>](expert-structures.md)                                   |
| <span data-ttu-id="52dcc-130">Von expertenstrukturen und Funktionen verwendete Enumerationen</span><span class="sxs-lookup"><span data-stu-id="52dcc-130">Enumerations used by expert structures and functions</span></span>              | [<span data-ttu-id="52dcc-131">Expertenenumerationen</span><span class="sxs-lookup"><span data-stu-id="52dcc-131">Expert Enumerations</span></span>](expert-enumerations.md)                               |
| <span data-ttu-id="52dcc-132">Allgemeine Hilfsfunktionen, die von Experten und Parser aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="52dcc-132">Common helper functions that can be called by experts and parsers</span></span> | [<span data-ttu-id="52dcc-133">Allgemeine Funktionen für Experten und Parser</span><span class="sxs-lookup"><span data-stu-id="52dcc-133">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |



 

 

 



