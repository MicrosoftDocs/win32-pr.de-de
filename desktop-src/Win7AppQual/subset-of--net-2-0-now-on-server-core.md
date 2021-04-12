---
description: .
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: Teilmenge von .NET 2,0 jetzt auf Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e0f836ca7afaef920429df17ef8be845ce92e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218823"
---
# <a name="subset-of-net-20-now-on-server-core"></a><span data-ttu-id="48543-103">Teilmenge von .NET 2,0 jetzt auf Server Core</span><span class="sxs-lookup"><span data-stu-id="48543-103">Subset of .NET 2.0 Now on Server Core</span></span>

## <a name="platform"></a><span data-ttu-id="48543-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="48543-104">Platform</span></span>

<span data-ttu-id="48543-105">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="48543-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="48543-106">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="48543-106">Feature Impact</span></span>

 <span data-ttu-id="48543-107">**Schweregrad** -niedrig</span><span class="sxs-lookup"><span data-stu-id="48543-107">**Severity** - Low</span></span>  
<span data-ttu-id="48543-108">**Häufigkeit** -niedrig</span><span class="sxs-lookup"><span data-stu-id="48543-108">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="48543-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48543-109">Description</span></span>

<span data-ttu-id="48543-110">Die Server Core-Installationsoption für Windows Server 2008 R2 enthält jetzt eine Teilmenge der .NET Framework 2,0.</span><span class="sxs-lookup"><span data-stu-id="48543-110">The Server Core installation option for Windows Server 2008 R2 now includes a subset of the .NET Framework 2.0.</span></span> <span data-ttu-id="48543-111">Die Teilmenge ist die Funktionalität in .NET 2,0, die mit der Funktionalität in Server Core abgestimmt ist. der Server Core-Basis wurden keine Binärdateien hinzugefügt, um die Funktionsweise eines beliebigen Teils von .NET 2,0 zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="48543-111">The subset is the functionality in .NET 2.0 that aligns with the functionality in Server Core; no binaries were added to the Server Core base to allow any portion of .NET 2.0 to function.</span></span>

<span data-ttu-id="48543-112">In der Server Core-Installationsoption für Windows Server 2008 wurde keine .NET-Unterstützung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="48543-112">There was no .NET support in the Server Core installation option for Windows Server 2008.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="48543-113">Erscheinung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="48543-113">Manifestation of Impact</span></span>

<span data-ttu-id="48543-114">Dadurch können einige auf .NET 2,0 basierende Anwendungen auf Server Core in Windows Server 2008 R2 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="48543-114">This allows some .NET 2.0 based-applications to run on Server Core in Windows Server 2008 R2.</span></span>

## <a name="testing"></a><span data-ttu-id="48543-115">Test</span><span class="sxs-lookup"><span data-stu-id="48543-115">Testing</span></span>

<span data-ttu-id="48543-116">Vergewissern Sie sich, dass die .NET-Klassen, die Ihr Code verwendet, in Server Core enthalten sind</span><span class="sxs-lookup"><span data-stu-id="48543-116">Verify that the .NET classes your code uses is included in Server Core.</span></span> <span data-ttu-id="48543-117">Testen Sie außerdem alle Anwendungen, die diesen Code auf Server Core ausführen.</span><span class="sxs-lookup"><span data-stu-id="48543-117">Also test any applications that run this code on Server Core.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="48543-118">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="48543-118">Links to Other Resources</span></span>

-   <span data-ttu-id="48543-119">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="48543-119">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>
-   [<span data-ttu-id="48543-120">Server Core-Blog</span><span class="sxs-lookup"><span data-stu-id="48543-120">Server Core Blog</span></span>](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   <span data-ttu-id="48543-121">*Weitere Informationen finden Sie auch* im Abschnitt Server Core des *Windows Server 2008 R2 SDK* , sobald es verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="48543-121">*See also* the Server Core section of the *Windows Server 2008 R2 SDK* when it becomes available</span></span>

> [!Note]  
> <span data-ttu-id="48543-122">Diese Ressourcen sind in einigen Sprachen und Ländern bzw. Regionen möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="48543-122">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
