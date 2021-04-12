---
description: Mit com+ werden neutrale Apartments eingeführt, um die Programmierung in Multithreadumgebungen zu vereinfachen. Das neutrale Apartment ist das bevorzugte Modell für com+ für Komponenten ohne Benutzeroberfläche.
ms.assetid: 679742af-7c04-4b0e-822a-a43e1aafa936
title: Neutrale Apartments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac3bdff2670e4f99ad94af20278eaca6a38861e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393069"
---
# <a name="neutral-apartments"></a><span data-ttu-id="a4fcb-104">Neutrale Apartments</span><span class="sxs-lookup"><span data-stu-id="a4fcb-104">Neutral Apartments</span></span>

<span data-ttu-id="a4fcb-105">Mit com+ werden neutrale Apartments eingeführt, um die Programmierung in Multithreadumgebungen zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="a4fcb-105">COM+ introduces neutral apartments to simplify programming in multithreaded environments.</span></span> <span data-ttu-id="a4fcb-106">Das neutrale Apartment ist das bevorzugte Modell für com+ für Komponenten ohne Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="a4fcb-106">The neutral apartment is the preferred model for COM+ for components with no user interface.</span></span>

<span data-ttu-id="a4fcb-107">In der Vergangenheit mussten com+-Entwickler, die Server Skalierbarkeit erforderten, kostenlose Thread Komponenten implementieren, um Engpässe zu vermeiden. das Implementieren von kostenlosen Threading Modellen ist jedoch komplizierter, da Sie mit dem Zugriff auf die Sperre umgehen müssen.</span><span class="sxs-lookup"><span data-stu-id="a4fcb-107">In the past, to prevent bottlenecks, COM+ developers requiring server scalability had to implement free-threaded components; however, free-threading models are complicated to implement because they must deal with interlocking access.</span></span> <span data-ttu-id="a4fcb-108">In neutralen Apartments befolgen Objekte die Richtlinien für multithreadwohnungen, können aber auch in jeder Art von Thread ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a4fcb-108">In neutral apartments, objects follow the guidelines for multithreaded apartments but can execute on any kind of thread.</span></span> <span data-ttu-id="a4fcb-109">Wenn ein Thread in einem neutralen Apartment ausgeführt wird, wird der Kontext des Objekts ohne einen Thread Wechsel empfangen.</span><span class="sxs-lookup"><span data-stu-id="a4fcb-109">When a thread is running in a neutral apartment, the object's context is received without causing a thread switch.</span></span>

<span data-ttu-id="a4fcb-110">Jeder Prozess kann nur über ein neutrales Apartment verfügen.</span><span class="sxs-lookup"><span data-stu-id="a4fcb-110">Each process can have only one neutral apartment.</span></span> <span data-ttu-id="a4fcb-111">Verwenden Sie die folgende Registrierungs Einstellung, um ein neutrales Apartment auszuwählen:</span><span class="sxs-lookup"><span data-stu-id="a4fcb-111">To select a neutral apartment, use the following registry setting:</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         ThreadingModel = Neutral
```

<span data-ttu-id="a4fcb-112">Komponenten mit Benutzeroberflächen sollten Single Thread-Apartments weiterhin als bevorzugtes Modell verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4fcb-112">Components that have user interfaces should continue to use single-threaded apartments as the preferred model.</span></span> <span data-ttu-id="a4fcb-113">Verwenden Sie die folgende Registrierungs Einstellung, um ein Single Thread-Apartment auszuwählen:</span><span class="sxs-lookup"><span data-stu-id="a4fcb-113">To select a single-threaded apartment, use the following registry setting:</span></span>

<span data-ttu-id="a4fcb-114">**ThreadingModel** = Apartment</span><span class="sxs-lookup"><span data-stu-id="a4fcb-114">**ThreadingModel** = Apartment</span></span>

 

 



