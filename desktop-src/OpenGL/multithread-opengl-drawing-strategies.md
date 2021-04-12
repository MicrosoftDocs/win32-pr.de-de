---
title: Multithread-OpenGL-Zeichnungs Strategien
description: Der GDI unterstützt nicht mehrere Threads.
ms.assetid: 3930029d-b2d9-4beb-bad6-4962f952d7ee
keywords:
- OpenGL unter Windows, multithreadzeichnung
- Multithread-OpenGL-Zeichen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bccb08d48bd8ccb62584f15911a1eb65080c4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309792"
---
# <a name="multithread-opengl-drawing-strategies"></a><span data-ttu-id="a7a3a-105">Multithread-OpenGL-Zeichnungs Strategien</span><span class="sxs-lookup"><span data-stu-id="a7a3a-105">Multithread OpenGL Drawing Strategies</span></span>

<span data-ttu-id="a7a3a-106">Der GDI unterstützt nicht mehrere Threads.</span><span class="sxs-lookup"><span data-stu-id="a7a3a-106">The GDI does not support multiple threads.</span></span> <span data-ttu-id="a7a3a-107">Sie müssen für jeden Thread einen eindeutigen Gerätekontext und einen eindeutigen renderingkontext verwenden.</span><span class="sxs-lookup"><span data-stu-id="a7a3a-107">You must use a distinct device context and a distinct rendering context for each thread.</span></span> <span data-ttu-id="a7a3a-108">Dadurch werden die Leistungsvorteile der Verwendung mehrerer Threads bei Systemen mit nur einem Prozessor, auf denen OpenGL-Anwendungen ausgeführt werden, eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="a7a3a-108">This tends to limit the performance advantages of using multiple threads with single-processor systems running OpenGL applications.</span></span> <span data-ttu-id="a7a3a-109">Es gibt jedoch Möglichkeiten, Threads mit einem einzelnen Prozessor System zu verwenden, um die Leistung erheblich zu steigern.</span><span class="sxs-lookup"><span data-stu-id="a7a3a-109">However, there are ways to use threads with a single processor system to greatly increase performance.</span></span> <span data-ttu-id="a7a3a-110">Beispielsweise können Sie einen separaten Thread verwenden, um OpenGL-renderingaufrufe an dedizierte 3D-Hardware zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="a7a3a-110">For example, you can use a separate thread to pass OpenGL rendering calls to dedicated 3-D hardware.</span></span>

<span data-ttu-id="a7a3a-111">Symmetrische Multiprozessorsysteme (Symmetric Multiprocessing, SMP) können von der Verwendung mehrerer Threads profitieren.</span><span class="sxs-lookup"><span data-stu-id="a7a3a-111">Symmetric multiprocessing (SMP) systems can greatly benefit from using multiple threads.</span></span> <span data-ttu-id="a7a3a-112">Eine offensichtliche Strategie besteht darin, einen separaten Thread für jeden Prozessor zu verwenden, um das OpenGL-Rendering in separaten Fenstern zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a7a3a-112">An obvious strategy is to use a separate thread for each processor to handle OpenGL rendering in separate windows.</span></span> <span data-ttu-id="a7a3a-113">Beispielsweise können Sie in einer Anwendung für die Flugsimulation separate Prozessoren und Threads verwenden, um die Front-, rückwärts-und Seitenansichten zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="a7a3a-113">For example, in a flight-simulation application you could use separate processors and threads to render the front, back, and side views.</span></span>

<span data-ttu-id="a7a3a-114">Ein Thread kann nur über einen aktuellen aktiven renderingkontext verfügen.</span><span class="sxs-lookup"><span data-stu-id="a7a3a-114">A thread can have only one current, active rendering context.</span></span> <span data-ttu-id="a7a3a-115">Wenn Sie mehrere Threads und mehrere renderingkontexte verwenden, müssen Sie Ihre Verwendung sorgfältig synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="a7a3a-115">When you use multiple threads and multiple rendering contexts, you must be careful to synchronize their use.</span></span> <span data-ttu-id="a7a3a-116">Verwenden Sie z. b. nur einen Thread, um " [**Austausch Puffer**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) " aufzurufen, nachdem alle Threads gezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="a7a3a-116">For example, use one thread only to call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) after all threads finish drawing.</span></span>

 

 




