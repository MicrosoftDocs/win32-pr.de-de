---
description: Die folgenden Funktionen sind die Einstiegspunkte für Experten-DLLs und für Aufrufe des Betriebssystems und Netzwerkmonitor.
ms.assetid: 1c0dcf6f-7f80-424b-9e6a-5a8b6a5b176f
title: Export Funktionen der Experten-dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923611521b98619b357eb2de93ee2269caf9c838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958730"
---
# <a name="expert-dll-export-functions"></a><span data-ttu-id="c0427-103">Export Funktionen der Experten-dll</span><span class="sxs-lookup"><span data-stu-id="c0427-103">Expert DLL Export Functions</span></span>

<span data-ttu-id="c0427-104">Die folgenden Funktionen sind die Einstiegspunkte für Experten-DLLs und für Aufrufe des Betriebssystems und Netzwerkmonitor.</span><span class="sxs-lookup"><span data-stu-id="c0427-104">The following functions are the entry points for expert DLLs and for calls from the operating system and Network Monitor.</span></span>



| <span data-ttu-id="c0427-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="c0427-105">Function</span></span>                                   | <span data-ttu-id="c0427-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0427-106">Description</span></span>                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0427-107">**DllMain-Experte**</span><span class="sxs-lookup"><span data-stu-id="c0427-107">**DllMain Expert**</span></span>](dllmain-expert.md)   | <span data-ttu-id="c0427-108">Gibt an, dass die Experten-dll geladen oder entladen wurde.</span><span class="sxs-lookup"><span data-stu-id="c0427-108">Indicates that the expert DLL has been loaded or unloaded.</span></span> <span data-ttu-id="c0427-109">Wenn ein Prozess die dll lädt oder entlädt, ruft das Betriebssystem die [**DllMain**](/windows/desktop/Dlls/dllmain) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="c0427-109">When a process loads or unloads the DLL, the operating system calls the [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span> |
| [<span data-ttu-id="c0427-110">**Experte registrieren**</span><span class="sxs-lookup"><span data-stu-id="c0427-110">**Register Expert**</span></span>](register-expert.md) | <span data-ttu-id="c0427-111">Bestimmt grundlegende Informationen zum Experten innerhalb der dll.</span><span class="sxs-lookup"><span data-stu-id="c0427-111">Determines basic information about the expert within the DLL.</span></span> <span data-ttu-id="c0427-112">Netzwerkmonitor Ruft die **Register** -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="c0427-112">Network Monitor calls the **Register** function.</span></span>                                                           |
| [<span data-ttu-id="c0427-113">**Konfigurieren**</span><span class="sxs-lookup"><span data-stu-id="c0427-113">**Configure**</span></span>](configure.md)             | <span data-ttu-id="c0427-114">Konfiguriert den Experten innerhalb der dll.</span><span class="sxs-lookup"><span data-stu-id="c0427-114">Configures the expert within the DLL.</span></span> <span data-ttu-id="c0427-115">Netzwerkmonitor Ruft die [**configure**](configure.md) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="c0427-115">Network Monitor calls the [**Configure**](configure.md) function.</span></span>                                                                 |
| [<span data-ttu-id="c0427-116">**Ausführen**</span><span class="sxs-lookup"><span data-stu-id="c0427-116">**Run**</span></span>](run.md)                         | <span data-ttu-id="c0427-117">Startet den Experten innerhalb der dll.</span><span class="sxs-lookup"><span data-stu-id="c0427-117">Starts the expert within the DLL.</span></span> <span data-ttu-id="c0427-118">Netzwerkmonitor Ruft die [**Run**](run.md) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="c0427-118">Network Monitor calls the [**Run**](run.md) function.</span></span>                                                                                 |



 

<span data-ttu-id="c0427-119">Netzwerkmonitor bietet auch Strukturen, Enumerationen und Hilfsfunktionen, die der Experte anrufen kann.</span><span class="sxs-lookup"><span data-stu-id="c0427-119">Network Monitor also provides structures, enumerations, and helper functions that the expert can call.</span></span>



| <span data-ttu-id="c0427-120">Informationen über</span><span class="sxs-lookup"><span data-stu-id="c0427-120">For information about</span></span>                                      | <span data-ttu-id="c0427-121">Finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="c0427-121">See</span></span>                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c0427-122">Hilfsfunktionen, die von Experten und Parser aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="c0427-122">Helper functions that can be called by experts and parsers</span></span> | [<span data-ttu-id="c0427-123">Allgemeine Funktionen für Experten und Parser</span><span class="sxs-lookup"><span data-stu-id="c0427-123">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |
| <span data-ttu-id="c0427-124">Hilfsfunktionen, die nur von Experten aufgerufen werden</span><span class="sxs-lookup"><span data-stu-id="c0427-124">Helper functions that are called only by experts</span></span>           | [<span data-ttu-id="c0427-125">Expertenfunktionen</span><span class="sxs-lookup"><span data-stu-id="c0427-125">Expert Functions</span></span>](expert-functions.md)                                     |
| <span data-ttu-id="c0427-126">Von Expertenfunktionen verwendete Strukturen</span><span class="sxs-lookup"><span data-stu-id="c0427-126">Structures that are used by expert functions</span></span>               | [<span data-ttu-id="c0427-127">Expertenstrukturen</span><span class="sxs-lookup"><span data-stu-id="c0427-127">Expert Structures</span></span>](expert-structures.md)                                   |
| <span data-ttu-id="c0427-128">Von expertenstrukturen und Funktionen verwendete Enumerationen</span><span class="sxs-lookup"><span data-stu-id="c0427-128">Enumerations used by expert structures and functions</span></span>       | [<span data-ttu-id="c0427-129">Expertenenumerationen</span><span class="sxs-lookup"><span data-stu-id="c0427-129">Expert Enumerations</span></span>](expert-enumerations.md)                               |



 

 

 
