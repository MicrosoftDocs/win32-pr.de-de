---
title: Erste Schritte mit DirectX für Windows
description: Das Erstellen eines Microsoft DirectX-Spiels für Windows ist eine Herausforderung für einen neuen Entwickler. Hier sehen wir uns schnell die beteiligten Konzepte und die Schritte an, die Sie ausführen müssen, um mit der Entwicklung eines Spiels mit DirectX und C++ zu beginnen.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bac8ca2805fed9ec42faf9deda9ddd51da39685
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343585"
---
# <a name="get-started-with-directx-for-windows"></a><span data-ttu-id="1f93f-104">Erste Schritte mit DirectX für Windows</span><span class="sxs-lookup"><span data-stu-id="1f93f-104">Get started with DirectX for Windows</span></span>

<span data-ttu-id="1f93f-105">Das Erstellen eines Microsoft DirectX-Spiels für Windows ist eine Herausforderung für einen neuen Entwickler.</span><span class="sxs-lookup"><span data-stu-id="1f93f-105">Creating a Microsoft DirectX game for Windows is a challenge for a new developer.</span></span> <span data-ttu-id="1f93f-106">Hier sehen wir uns schnell die beteiligten Konzepte und die Schritte an, die Sie ausführen müssen, um mit der Entwicklung eines Spiels mit DirectX und C++ zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="1f93f-106">Here we quickly review the concepts involved and the steps you must take to begin developing a game using DirectX and C++.</span></span>

<span data-ttu-id="1f93f-107">Fangen wir also an.</span><span class="sxs-lookup"><span data-stu-id="1f93f-107">Let's get started.</span></span>

## <a name="what-skills-do-you-need"></a><span data-ttu-id="1f93f-108">Welche Qualifikationen benötigen Sie?</span><span class="sxs-lookup"><span data-stu-id="1f93f-108">What skills do you need?</span></span>

<span data-ttu-id="1f93f-109">Um ein Spiel in DirectX für Windows entwickeln zu können, müssen Sie über einige Grundkenntnisse verfügen.</span><span class="sxs-lookup"><span data-stu-id="1f93f-109">To develop a game in DirectX for Windows, you must have a few basic skills.</span></span> <span data-ttu-id="1f93f-110">Insbesondere müssen Folgendes möglich sein:</span><span class="sxs-lookup"><span data-stu-id="1f93f-110">Specifically, you must be able to:</span></span>

-   <span data-ttu-id="1f93f-111">Lesen und Schreiben von modernem C++-Code (C++11 hilft am meisten) und Vertrautheit mit grundlegenden C++-Entwurfsprinzipien und -Mustern wie Vorlagen und dem Factorymodell.</span><span class="sxs-lookup"><span data-stu-id="1f93f-111">Read and write modern C++ code (C++11 helps the most), and be familiar with basic C++ design principles and patterns like templates and the factory model.</span></span> <span data-ttu-id="1f93f-112">Sie müssen auch mit allgemeinen C++-Bibliotheken wie der Standardvorlagenbibliothek und insbesondere mit den Umwandlungsoperatoren, Zeigertypen und den Standardvorlagenbibliothek-Datenstrukturen (z. B. std::vector) vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="1f93f-112">You must also be familiar with common C++ libraries like the Standard Template Library, and specifically with the casting operators, pointer types, and the standard template library data structures (such as std::vector).</span></span>
-   <span data-ttu-id="1f93f-113">Grundlegendes zur Geometrie, Trigonometrie und linearen Algebra.</span><span class="sxs-lookup"><span data-stu-id="1f93f-113">Understand basic geometry, trigonometry, and linear algebra.</span></span> <span data-ttu-id="1f93f-114">Ein Großteil des Codes, den Sie in den Beispielen finden, setzt voraus, dass Sie diese Formen der Mathematik und ihre allgemeinen Regeln verstehen.</span><span class="sxs-lookup"><span data-stu-id="1f93f-114">Much of the code you will find in the examples assumes you understand these forms of mathematics and their common rules.</span></span>
-   <span data-ttu-id="1f93f-115">Vertrautheit mit COM– insbesondere [**Microsoft::WRL::ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (intelligenter Zeiger).</span><span class="sxs-lookup"><span data-stu-id="1f93f-115">Have familiarity with COM—especially [**Microsoft::WRL::ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (smart pointer).</span></span>
-   <span data-ttu-id="1f93f-116">Machen Sie sich mit den Grundlagen der Grafik- und Grafiktechnologie, insbesondere 3D-Grafiken, aus.</span><span class="sxs-lookup"><span data-stu-id="1f93f-116">Understand the foundations of graphics and graphics technology, particularly 3D graphics.</span></span> <span data-ttu-id="1f93f-117">Obwohl DirectX selbst über eine eigene Terminologie verfügt, baut es immer noch auf einem fundierten Verständnis allgemeiner 3D-Grafikprinzipien auf.</span><span class="sxs-lookup"><span data-stu-id="1f93f-117">While DirectX itself has its own terminology, it still builds upon a well-established understanding of general 3D graphics principles.</span></span>
-   <span data-ttu-id="1f93f-118">Verstehen Sie das Konzept einer Nachrichtenschleife, da Sie eine Schleife implementieren, die auf das Windows-Betriebssystem lauscht.</span><span class="sxs-lookup"><span data-stu-id="1f93f-118">Understand the concept of a message loop, because you'll be implementing a loop that listens to the Windows operating system.</span></span>

## <a name="and-were-off"></a><span data-ttu-id="1f93f-119">Und wir sind los!</span><span class="sxs-lookup"><span data-stu-id="1f93f-119">And we're off!</span></span>

<span data-ttu-id="1f93f-120">Bist du bereit?</span><span class="sxs-lookup"><span data-stu-id="1f93f-120">Ready to start?</span></span> <span data-ttu-id="1f93f-121">Sehen wir uns dies noch einmal an.</span><span class="sxs-lookup"><span data-stu-id="1f93f-121">Let's review before we head on.</span></span> <span data-ttu-id="1f93f-122">Sie haben:</span><span class="sxs-lookup"><span data-stu-id="1f93f-122">You have:</span></span>

-   <span data-ttu-id="1f93f-123">Eine aktualisierte und funktionierende Installation von Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="1f93f-123">An updated and working installation of Windows 8.1.</span></span>
-   <span data-ttu-id="1f93f-124">Eine Installation von [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span><span class="sxs-lookup"><span data-stu-id="1f93f-124">An installation of [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span></span>
-   <span data-ttu-id="1f93f-125">Ein unerschrockener Kasten und der Wunsch, mehr über die DirectX-Spieleentwicklung zu erfahren!</span><span class="sxs-lookup"><span data-stu-id="1f93f-125">An intrepid spirit and a desire to learn more about DirectX game development!</span></span>

## <a name="next-steps"></a><span data-ttu-id="1f93f-126">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="1f93f-126">Next steps</span></span>



| <span data-ttu-id="1f93f-127">Thema</span><span class="sxs-lookup"><span data-stu-id="1f93f-127">Topic</span></span>                                                                                                   | <span data-ttu-id="1f93f-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f93f-128">Description</span></span>                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f93f-129">Arbeiten mit DirectX-Geräteressourcen</span><span class="sxs-lookup"><span data-stu-id="1f93f-129">Work with DirectX device resources</span></span>](work-with-dxgi.md)                                           | <span data-ttu-id="1f93f-130">Erfahren Sie, wie Sie DXGI verwenden, um ein virtualisiertes Grafikgerät zu erstellen und eine Austauschkette zu erstellen und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1f93f-130">Learn how to use DXGI to create a virtualized graphics device, and create and configure a swap chain.</span></span>     |
| [<span data-ttu-id="1f93f-131">Verstehen der Direct3D 11-Renderingpipeline</span><span class="sxs-lookup"><span data-stu-id="1f93f-131">Understand the Direct3D 11 rendering pipeline</span></span>](understand-the-directx-11-2-graphics-pipeline.md) | <span data-ttu-id="1f93f-132">Erfahren Sie, wie Sie mithilfe der Direct3D-Grafikpipeline eine Verbindung mit der DirectX-Geräteressourcenklasse erstellen und zeichnen.</span><span class="sxs-lookup"><span data-stu-id="1f93f-132">Learn how to hook into the DirectX device resources class, and draw using the Direct3D graphics pipeline.</span></span> |
| [<span data-ttu-id="1f93f-133">Arbeiten mit Shadern und Shaderressourcen</span><span class="sxs-lookup"><span data-stu-id="1f93f-133">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)               | <span data-ttu-id="1f93f-134">Erfahren Sie, wie Sie HLSL-Shaderprogramme für Direct3D-Grafikpipelinestufen schreiben.</span><span class="sxs-lookup"><span data-stu-id="1f93f-134">Learn how to write HLSL shader programs for Direct3D graphics pipeline stages.</span></span>                            |



 

 

 