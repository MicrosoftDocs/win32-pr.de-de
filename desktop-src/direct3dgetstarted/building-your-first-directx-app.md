---
title: Erstellen Ihrer ersten Windows-App mit DirectX
description: In diesem Abschnitt wird beschrieben, warum Sie das C++ Model für die Entwicklung von Windows Store-Apps verwenden und grundlegende Tutorials und Verfahren für die ersten Schritte mit der Entwicklung von DirectX-apps bereitstellen.
ms.assetid: b632ba9c-1c30-4d21-ac79-7f2a193956fe
keywords:
- DirectX-APP, Einstieg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5e3afed57244789c0e3e06ab71ec39e581305c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707152"
---
# <a name="create-your-first-windows-app-using-directx"></a><span data-ttu-id="430b9-104">Erstellen Ihrer ersten Windows-App mit DirectX</span><span class="sxs-lookup"><span data-stu-id="430b9-104">Create your first Windows app using DirectX</span></span>

<span data-ttu-id="430b9-105">Wenn Sie DirectX wissen, können Sie eine DirectX-App mit System eigenem C++ und HLSL entwickeln, um die gesamte Nutzung der Grafikhardware zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="430b9-105">If you know DirectX, you can develop a DirectX app using native C++ and HLSL to take full advantage of graphics hardware.</span></span>

<span data-ttu-id="430b9-106">Verwenden Sie dieses grundlegende Tutorial für den Einstieg in die Entwicklung von DirectX-apps</span><span class="sxs-lookup"><span data-stu-id="430b9-106">Use this basic tutorial to get started with DirectX app development, then use the roadmap to continue exploring DirectX.</span></span>

## <a name="windows-desktop-app-with-c-and-directx"></a><span data-ttu-id="430b9-107">Windows-Desktop-App mit C++ und DirectX</span><span class="sxs-lookup"><span data-stu-id="430b9-107">Windows desktop app with C++ and DirectX</span></span>

<span data-ttu-id="430b9-108">Eine Windows-Desktop-App mit DirectX ist eine APP, die mit nativen C++ und DirectX-APIs entwickelt wurde.</span><span class="sxs-lookup"><span data-stu-id="430b9-108">A Windows desktop app with DirectX is an app developed using native C++ and DirectX APIs.</span></span> <span data-ttu-id="430b9-109">Dieses Modell ist komplexer als eine in einem verwalteten Framework geschriebene APP, bietet jedoch mehr Flexibilität und einen besseren Zugriff auf Systemressourcen, insbesondere Grafikgeräte.</span><span class="sxs-lookup"><span data-stu-id="430b9-109">This model is more complex than an app written in a managed framework, but it provides greater flexibility and greater access to system resources especially graphics devices.</span></span> <span data-ttu-id="430b9-110">Das ist ein gutes Modell für erfahrene Entwickler.</span><span class="sxs-lookup"><span data-stu-id="430b9-110">So, it is a good model for the experienced developer.</span></span>

## <a name="why-develop-a-windows-app-with-directx"></a><span data-ttu-id="430b9-111">Warum entwickeln Sie eine Windows-App mit DirectX?</span><span class="sxs-lookup"><span data-stu-id="430b9-111">Why develop a Windows app with DirectX?</span></span>

<span data-ttu-id="430b9-112">Die Antwort ist einfach: Sie möchten ein Spiel erstellen, das Grafik-oder multimediagingintensiv ist, und die Funktionen nutzen können, die von vielen Grafik Geräten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="430b9-112">The answer is simple: you want to make a game that is graphics- or multimedia-intensive, and can use the features that many graphics devices support.</span></span> <span data-ttu-id="430b9-113">Dies ist nicht einfach, wenn Sie mit der Spieleentwicklung oder der Windows-Entwicklung und C/C++ noch nicht vertraut sind. es gibt jedoch einige gute Neuigkeiten: DirectX 11 ist die einfachste und am weitesten geschlossene Version von Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="430b9-113">This won't be easy if you are new to game development or to Windows development and C/C++, but there's some good news: DirectX 11 is the simplest and most cohesive version of Microsoft DirectX yet.</span></span> <span data-ttu-id="430b9-114">Es ist auch die leistungsfähigste und funktionsreiche Funktion.</span><span class="sxs-lookup"><span data-stu-id="430b9-114">It's also the most powerful and feature-rich.</span></span> <span data-ttu-id="430b9-115">Wenn Sie die Spieleentwicklung beherrschen und die fortschrittlichsten Renderingverfahren erlernen, kann DirectX Ihnen die Gelegenheit bieten, dies zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="430b9-115">If your goal is to master game development and learn the most advanced rendering techniques, then DirectX can provide the opportunity for you to do that.</span></span>

<span data-ttu-id="430b9-116">Dies bedeutet, dass die Planung Ihres Spiels (oder eine interaktive Echt Zeit-APP) von wesentlicher Bedeutung ist.</span><span class="sxs-lookup"><span data-stu-id="430b9-116">That said, planning your game (or interactive, real-time app) is essential.</span></span> <span data-ttu-id="430b9-117">Wenn Sie mit der Spieleentwicklung noch nicht vertraut sind und das Spiel keine anspruchsvollen Grafik Anforderungen hat, sollten Sie es stattdessen mit .NET Framework entwickeln.</span><span class="sxs-lookup"><span data-stu-id="430b9-117">If you are new to game development, and your game doesn't have demanding graphics requirements, consider developing it with the .NET framework instead.</span></span> <span data-ttu-id="430b9-118">Außerdem sind viele "Middleware"-Grafiken und Spiel Entwicklungspakete für Windows-Plattformen verfügbar, und einige erfordern keine großen Programmierkenntnisse.</span><span class="sxs-lookup"><span data-stu-id="430b9-118">Also, many "middleware" graphics and game development packages are available for Windows platforms, and some do not require significant programming skills.</span></span>

<span data-ttu-id="430b9-119">Wenn Sie sicher sind oder einfach ein Spiel mit High-Fidelity-Grafiken (oder einer APP mit komplexem Grafik Inhalt) machen möchten, lesen Sie die Informationen unter!</span><span class="sxs-lookup"><span data-stu-id="430b9-119">If you are confident, or simply have a dream of making a game with high-fidelity graphics (or an app with complex graphics content), then read on!</span></span>

## <a name="in-this-section"></a><span data-ttu-id="430b9-120">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="430b9-120">In this section</span></span>



| <span data-ttu-id="430b9-121">Thema</span><span class="sxs-lookup"><span data-stu-id="430b9-121">Topic</span></span>                                                                                                                     | <span data-ttu-id="430b9-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="430b9-122">Description</span></span>                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="430b9-123">Voraussetzungen für die Entwicklung mit DirectX</span><span class="sxs-lookup"><span data-stu-id="430b9-123">Prerequisites for developing with DirectX</span></span>](pre-requisites-for-developing-a-tailored-c---with-directx-app.md)<br/> | <span data-ttu-id="430b9-124">Wenn Sie mit der Entwicklung einer Windows-App mit DirectX beginnen, sollten Sie die Voraussetzungen auf dieser Seite berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="430b9-124">When you start to develop a Windows app using DirectX, keep the prerequisites on this page in mind.</span></span> <span data-ttu-id="430b9-125">Dies umfasst die Technologien, die Sie kennen müssen, bevor Sie sich mit beschäftigen.</span><span class="sxs-lookup"><span data-stu-id="430b9-125">This includes the technologies you need to know before you dive in.</span></span><br/>                            |
| [<span data-ttu-id="430b9-126">Einstieg in DirectX für Windows</span><span class="sxs-lookup"><span data-stu-id="430b9-126">Get started with DirectX for Windows</span></span>](getting-started-with-a-directx-game.md)<br/>                                | <span data-ttu-id="430b9-127">Das Erstellen eines DirectX-Spiels für Windows stellt eine Herausforderung für einen neuen Entwickler dar.</span><span class="sxs-lookup"><span data-stu-id="430b9-127">Creating a DirectX game for Windows is a challenge for a new developer.</span></span> <span data-ttu-id="430b9-128">Hier überprüfen wir schnell die Konzepte und die Schritte, die Sie ausführen müssen, um mit der Entwicklung eines Spiels mit DirectX und C++ zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="430b9-128">Here we quickly review the concepts involved and the steps you must take to begin developing a game using DirectX and C++.</span></span><br/> |
| [<span data-ttu-id="430b9-129">Roadmap für DirectX-Desktop-Apps</span><span class="sxs-lookup"><span data-stu-id="430b9-129">Roadmap for Desktop DirectX apps</span></span>](roadmap-for-metro-style-apps-using-directx.md)<br/>                             | <span data-ttu-id="430b9-130">Hier finden Sie wichtige Ressourcen, die Ihnen bei den ersten Schritten mit der Verwendung von DirectX und C++ zum entwickeln Grafik intensiver Desktop-Apps wie Spielen helfen.</span><span class="sxs-lookup"><span data-stu-id="430b9-130">Here are key resources to help you get started with using DirectX and C++ to develop graphics-intensive Desktop apps, like games.</span></span> <br/>                                                                 |



 

 

 





