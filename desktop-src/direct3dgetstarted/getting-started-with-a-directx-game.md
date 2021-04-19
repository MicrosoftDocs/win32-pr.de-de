---
title: Einstieg in DirectX für Windows
description: Das Erstellen eines Microsoft DirectX-Spiels für Windows stellt eine Herausforderung für einen neuen Entwickler dar. Hier überprüfen wir schnell die Konzepte und die Schritte, die Sie ausführen müssen, um mit der Entwicklung eines Spiels mit DirectX und C++ zu beginnen.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae09cd127a30401ae0493f5dd770fe1e67607b45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339279"
---
# <a name="get-started-with-directx-for-windows"></a><span data-ttu-id="749f3-104">Einstieg in DirectX für Windows</span><span class="sxs-lookup"><span data-stu-id="749f3-104">Get started with DirectX for Windows</span></span>

<span data-ttu-id="749f3-105">Das Erstellen eines Microsoft DirectX-Spiels für Windows stellt eine Herausforderung für einen neuen Entwickler dar.</span><span class="sxs-lookup"><span data-stu-id="749f3-105">Creating a Microsoft DirectX game for Windows is a challenge for a new developer.</span></span> <span data-ttu-id="749f3-106">Hier überprüfen wir schnell die Konzepte und die Schritte, die Sie ausführen müssen, um mit der Entwicklung eines Spiels mit DirectX und C++ zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="749f3-106">Here we quickly review the concepts involved and the steps you must take to begin developing a game using DirectX and C++.</span></span>

<span data-ttu-id="749f3-107">Fangen wir also an.</span><span class="sxs-lookup"><span data-stu-id="749f3-107">Let's get started.</span></span>

## <a name="what-skills-do-you-need"></a><span data-ttu-id="749f3-108">Welche Fähigkeiten benötigen Sie?</span><span class="sxs-lookup"><span data-stu-id="749f3-108">What skills do you need?</span></span>

<span data-ttu-id="749f3-109">Um ein Spiel in DirectX für Windows zu entwickeln, müssen Sie über einige grundlegende Kenntnisse verfügen.</span><span class="sxs-lookup"><span data-stu-id="749f3-109">To develop a game in DirectX for Windows, you must have a few basic skills.</span></span> <span data-ttu-id="749f3-110">Insbesondere müssen Sie in der Lage sein, Folgendes zu tun:</span><span class="sxs-lookup"><span data-stu-id="749f3-110">Specifically, you must be able to:</span></span>

-   <span data-ttu-id="749f3-111">Lesen und Schreiben von modernem C++-Code (C++ 11 hilft am meisten) und ist mit grundlegenden C++-Entwurfs Prinzipien und-Mustern wie Vorlagen und dem Werk Modell vertraut.</span><span class="sxs-lookup"><span data-stu-id="749f3-111">Read and write modern C++ code (C++11 helps the most), and be familiar with basic C++ design principles and patterns like templates and the factory model.</span></span> <span data-ttu-id="749f3-112">Sie müssen auch mit allgemeinen C++-Bibliotheken wie der Standardvorlagen Bibliothek und speziell mit den Typumwandlungs Operatoren, Zeiger Typen und den standardmäßigen Vorlagen Bibliotheksdaten Strukturen (z. b. Std:: Vector) vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="749f3-112">You must also be familiar with common C++ libraries like the Standard Template Library, and specifically with the casting operators, pointer types, and the standard template library data structures (such as std::vector).</span></span>
-   <span data-ttu-id="749f3-113">Verstehen Sie grundlegende Geometrie, Trigonometry und lineare Algebra.</span><span class="sxs-lookup"><span data-stu-id="749f3-113">Understand basic geometry, trigonometry, and linear algebra.</span></span> <span data-ttu-id="749f3-114">Bei einem Großteil des Codes, den Sie in den Beispielen finden, wird davon ausgegangen, dass Sie diese Formen der Mathematik und ihrer allgemeinen Regeln verstehen.</span><span class="sxs-lookup"><span data-stu-id="749f3-114">Much of the code you will find in the examples assumes you understand these forms of mathematics and their common rules.</span></span>
-   <span data-ttu-id="749f3-115">Vertrautheit mit com – besonders [**Microsoft:: WRL:: comptr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (intelligenter Zeiger).</span><span class="sxs-lookup"><span data-stu-id="749f3-115">Have familiarity with COM—especially [**Microsoft::WRL::ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (smart pointer).</span></span>
-   <span data-ttu-id="749f3-116">Lernen Sie die Grundlagen von Grafiken und Grafik Technologien kennen, insbesondere 3D-Grafiken.</span><span class="sxs-lookup"><span data-stu-id="749f3-116">Understand the foundations of graphics and graphics technology, particularly 3D graphics.</span></span> <span data-ttu-id="749f3-117">Obwohl DirectX selbst über eine eigene Terminologie verfügt, baut es immer noch auf ein gut erstelltes Verständnis allgemeiner 3D-Grafik Prinzipien auf.</span><span class="sxs-lookup"><span data-stu-id="749f3-117">While DirectX itself has its own terminology, it still builds upon a well-established understanding of general 3D graphics principles.</span></span>
-   <span data-ttu-id="749f3-118">Verstehen Sie das Konzept einer Nachrichten Schleife, da Sie eine Schleife implementieren, die auf das Windows-Betriebssystem lauscht.</span><span class="sxs-lookup"><span data-stu-id="749f3-118">Understand the concept of a message loop, because you'll be implementing a loop that listens to the Windows operating system.</span></span>

## <a name="and-were-off"></a><span data-ttu-id="749f3-119">Und wir sind los!</span><span class="sxs-lookup"><span data-stu-id="749f3-119">And we're off!</span></span>

<span data-ttu-id="749f3-120">Bist du bereit?</span><span class="sxs-lookup"><span data-stu-id="749f3-120">Ready to start?</span></span> <span data-ttu-id="749f3-121">Schauen wir uns das einmal an.</span><span class="sxs-lookup"><span data-stu-id="749f3-121">Let's review before we head on.</span></span> <span data-ttu-id="749f3-122">Sie haben:</span><span class="sxs-lookup"><span data-stu-id="749f3-122">You have:</span></span>

-   <span data-ttu-id="749f3-123">Eine aktualisierte und funktionierende Installation von Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="749f3-123">An updated and working installation of Windows 8.1.</span></span>
-   <span data-ttu-id="749f3-124">Eine Installation von [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span><span class="sxs-lookup"><span data-stu-id="749f3-124">An installation of [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span></span>
-   <span data-ttu-id="749f3-125">Ein unerschrockener-Geist und ein Wunsch, mehr über die Entwicklung von DirectX-spielen zu erfahren!</span><span class="sxs-lookup"><span data-stu-id="749f3-125">An intrepid spirit and a desire to learn more about DirectX game development!</span></span>

## <a name="next-steps"></a><span data-ttu-id="749f3-126">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="749f3-126">Next steps</span></span>



|                                                                                                    |                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="749f3-127">Arbeiten mit DirectX-Geräte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="749f3-127">Work with DirectX device resources</span></span>](work-with-dxgi.md)                                           | <span data-ttu-id="749f3-128">Erfahren Sie, wie Sie DXGI verwenden, um ein virtualisiertes Grafikgerät zu erstellen und eine SwapChain zu erstellen und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="749f3-128">Learn how to use DXGI to create a virtualized graphics device, and create and configure a swap chain.</span></span>     |
| [<span data-ttu-id="749f3-129">Grundlegendes zur Direct3D 11-Renderingpipeline</span><span class="sxs-lookup"><span data-stu-id="749f3-129">Understand the Direct3D 11 rendering pipeline</span></span>](understand-the-directx-11-2-graphics-pipeline.md) | <span data-ttu-id="749f3-130">Erfahren Sie, wie Sie sich mit der DirectX-Geräte Ressourcen Klasse verbinden und mithilfe der Direct3D-Grafik Pipeline zeichnen.</span><span class="sxs-lookup"><span data-stu-id="749f3-130">Learn how to hook into the DirectX device resources class, and draw using the Direct3D graphics pipeline.</span></span> |
| [<span data-ttu-id="749f3-131">Arbeiten mit Shader und Shaderressourcen</span><span class="sxs-lookup"><span data-stu-id="749f3-131">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)               | <span data-ttu-id="749f3-132">Erfahren Sie, wie Sie HLSL-Shader-Programme für Direct3D-Grafik Pipeline Stufen schreiben.</span><span class="sxs-lookup"><span data-stu-id="749f3-132">Learn how to write HLSL shader programs for Direct3D graphics pipeline stages.</span></span>                            |



 

 

 