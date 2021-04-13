---
title: Voraussetzungen für die Entwicklung mit DirectX
description: Wenn Sie mit der Entwicklung einer Windows-App mit DirectX beginnen, sollten Sie die Voraussetzungen auf dieser Seite berücksichtigen. Dies umfasst die Technologien, die Sie kennen müssen, bevor Sie sich mit beschäftigen.
ms.assetid: 93f566cf-0c16-4487-9d53-dc59746e4d00
keywords:
- DirectX-APP, Voraussetzungen
- DirectX-APP, Windows Store-App
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5e09484bef67546047214702fab7d2d0a5c48d
ms.sourcegitcommit: 6394972f1e8b01229db602469df6bb137e31d776
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2020
ms.locfileid: "104474718"
---
# <a name="prerequisites-for-developing-with-directx"></a><span data-ttu-id="8f0bb-106">Voraussetzungen für die Entwicklung mit DirectX</span><span class="sxs-lookup"><span data-stu-id="8f0bb-106">Prerequisites for developing with DirectX</span></span>

<span data-ttu-id="8f0bb-107">Wenn Sie mit der Entwicklung einer Windows-App mit DirectX beginnen, sollten Sie die Voraussetzungen auf dieser Seite berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-107">When you start to develop a Windows app using DirectX, keep the prerequisites on this page in mind.</span></span> <span data-ttu-id="8f0bb-108">Dies umfasst die Technologien, die Sie kennen müssen, bevor Sie sich mit beschäftigen.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-108">This includes the technologies you need to know before you dive in.</span></span>

## <a name="what-should-i-know-to-develop-a-windows-game-using-directx"></a><span data-ttu-id="8f0bb-109">Was sollte ich wissen, um ein Windows-Spiel mit DirectX zu entwickeln?</span><span class="sxs-lookup"><span data-stu-id="8f0bb-109">What should I know to develop a Windows game using DirectX?</span></span>

<span data-ttu-id="8f0bb-110">Bevor Sie mit der Entwicklung einer Windows Store-App mit DirectX beginnen, müssen Sie wissen, wie Sie in Windows mit C++ programmieren können.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-110">Before you start to develop a Windows Store app using DirectX, you need to know how to program in Windows with C++.</span></span> <span data-ttu-id="8f0bb-111">Windows-apps, die DirectX verwenden, werden auf einer geringen Programmier Ebene entwickelt, was bedeutet, dass Sie für viele Features des Betriebssystems verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-111">Windows apps using DirectX are developed at a low level of programming, which means that you will be exposed to many features of the operating system.</span></span> <span data-ttu-id="8f0bb-112">Hierzu gehören die Arbeitsspeicher-und Ressourcenverwaltung und die-Schnittstelle für das Grafikgerät selbst.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-112">These include memory and resource management, and the interface for the graphics device itself.</span></span> <span data-ttu-id="8f0bb-113">Wenn Sie mit der Entwicklung von Spiele-oder Grafik-apps noch nicht vertraut sind, können Sie diese Herausforderung finden.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-113">If you are new to game or graphics app development, you may find this challenging.</span></span> <span data-ttu-id="8f0bb-114">Sie werden sich aber auch als lohnend herausfinden, da das Erlernen der Spieleentwicklung auf dieser Ebene sehr viel größere Möglichkeiten für das Entwerfen und entwickeln von Spiel-und Grafik-Apps bietet.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-114">But you will also find it rewarding, because learning game development at this level creates far, far greater possibilities for game and graphics app design and development.</span></span>

<span data-ttu-id="8f0bb-115">Außerdem müssen Sie die Grundlagen der 2D-und 3D-Grafik Programmierung und-Mathematik verstehen, da viele der APIs, die Sie verwenden, mit diesen Prinzipien entwickelt wurden.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-115">You'll also need to understand the basics of 2D and 3D graphics programming and mathematics, because many of the APIs you'll use were developed with these principles in mind.</span></span> <span data-ttu-id="8f0bb-116">Wenn Sie mit den Vorgängen dahinter vertraut sind, ist es einfacher, ihre Parameter und Ergebnisse zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-116">It'll be easier for you to understand their parameters and results if you are familiar with the operations behind them.</span></span>

<span data-ttu-id="8f0bb-117">Sie sollten mindestens über Folgendes verfügen:</span><span class="sxs-lookup"><span data-stu-id="8f0bb-117">At a minimum, you should have a grasp of the following:</span></span>

-   <span data-ttu-id="8f0bb-118">Windows C/C++-Programmierung.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-118">Windows C/C++ programming.</span></span> <span data-ttu-id="8f0bb-119">Dies bedeutet, dass Sie Zeiger und Verweise, Ereignisse und Rückrufe und möglicherweise einige der allgemeinen Bibliotheken wie ATL verstehen.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-119">This means that you understand pointers and references, events and callbacks, and perhaps a few of the common libraries like ATL.</span></span>
-   <span data-ttu-id="8f0bb-120">Win32-Programmierung.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-120">Win32 programming.</span></span> <span data-ttu-id="8f0bb-121">Sie verstehen, wie Windows erstellt wird und wie Ereignisse der Benutzeroberfläche verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-121">You understand how windows are created, and how user interface events are processed.</span></span> <span data-ttu-id="8f0bb-122">Sie verstehen auch etwas über com und grundlegende Win32-APIs.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-122">You also understand a little bit about COM and essential Win32 APIs.</span></span>
-   <span data-ttu-id="8f0bb-123">Lineare Algebra und Trigonometry.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-123">Linear algebra and trigonometry.</span></span> <span data-ttu-id="8f0bb-124">Obwohl es nicht unbedingt erforderlich ist, haben Sie einen einfacheren Zeitpunkt, wenn Sie mit den Konzepten aus diesen beiden mathematischen Disziplinen vertraut sind, da Sie die Grundlage für einen Großteil der 3D-Grafik Programmierung sind.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-124">While not essential, you'll have an easier time if you are familiar with concepts from these two math disciplines, because they are the foundation of much of 3D graphics programming.</span></span>
-   <span data-ttu-id="8f0bb-125">Grundlegende Grafik Terminologie und-Konzepte, wie z. b. Bitmaps, Texturen, Scheitel Punkte, Meshes und Viewports.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-125">Basic graphics terminology and concepts, such as bitmaps, textures, vertices, meshes, and viewports.</span></span>

## <a name="what-does-directx-provide-me"></a><span data-ttu-id="8f0bb-126">Was bietet DirectX mir?</span><span class="sxs-lookup"><span data-stu-id="8f0bb-126">What does DirectX provide me?</span></span>

<span data-ttu-id="8f0bb-127">DirectX ist der primäre Satz von Grafik-APIs, die Sie zum Entwickeln von Windows-Spielen verwenden.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-127">DirectX is the primary set of graphics APIs you'll use to develop Windows games.</span></span> <span data-ttu-id="8f0bb-128">Im folgenden finden Sie die Kategorien von Features, mit denen Sie sich vertraut machen müssen, wenn Sie entscheiden, wie Sie Ihr Spiel entwickeln.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-128">Here are the categories of features that you must become familiar with when you decide how to develop your game.</span></span>



| <span data-ttu-id="8f0bb-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8f0bb-129">Library</span></span>     | <span data-ttu-id="8f0bb-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f0bb-130">Description</span></span>                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f0bb-131">Direct3D</span><span class="sxs-lookup"><span data-stu-id="8f0bb-131">Direct3D</span></span>    | <span data-ttu-id="8f0bb-132">Leistungsorientierter, Hardware beschleunigter Satz von Bibliotheken zum Rendern von 3D-Grafiken.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-132">A powerful, performance-oriented, hardware-accelerated set of libraries for rendering 3D graphics.</span></span>                                              |
| <span data-ttu-id="8f0bb-133">Direct2D</span><span class="sxs-lookup"><span data-stu-id="8f0bb-133">Direct2D</span></span>    | <span data-ttu-id="8f0bb-134">Ein Satz von 2D-Grafik Bibliotheken für Hardware beschleunigter Bitmap und Vector 2D Drawing.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-134">A set of 2D graphics libraries for hardware-accelerated bitmap and vector 2D drawing.</span></span>                                                           |
| <span data-ttu-id="8f0bb-135">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="8f0bb-135">DirectXMath</span></span> | <span data-ttu-id="8f0bb-136">Eine Bibliothek allgemeiner, optimierter mathematischer Vorgänge, die in 2D-und 3D-Grafiken verwendet werden, z. b. Vektor-und Matrix Operationen.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-136">A library of common, optimized math operations used in 2D and 3D graphics, such as vector and matrix operations.</span></span>                                |
| <span data-ttu-id="8f0bb-137">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="8f0bb-137">DirectWrite</span></span> | <span data-ttu-id="8f0bb-138">Eine Bibliothek mit 2D-Text Rendering und Layout-APIs.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-138">A library of 2D text rendering and layout APIs.</span></span> <span data-ttu-id="8f0bb-139">Es unterstützt sowohl Hardwarebeschleunigung als auch Software-rasterisierung.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-139">It supports both hardware acceleration and software rasterization.</span></span>                              |
| <span data-ttu-id="8f0bb-140">XAudio2</span><span class="sxs-lookup"><span data-stu-id="8f0bb-140">XAudio2</span></span>     | <span data-ttu-id="8f0bb-141">Eine plattformübergreifende audioapi auf niedriger Ebene für Microsoft Windows, die eine Signalverarbeitung und ein audiomischungs Fundament für die Spieleentwicklung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-141">A low-level, cross-platform audio API for Microsoft Windows that provides a signal processing and audio mixing foundation for game development.</span></span> |
| <span data-ttu-id="8f0bb-142">XInput</span><span class="sxs-lookup"><span data-stu-id="8f0bb-142">XInput</span></span>      | <span data-ttu-id="8f0bb-143">Eine Bibliothek, die verschiedene herkömmliche Gaming-Steuerelemente unterstützt, mit einem Schwerpunkt auf dem Xbox 360-Controller Modell.</span><span class="sxs-lookup"><span data-stu-id="8f0bb-143">A library that supports various traditional gaming controls, with an emphasis on the Xbox 360 controller model.</span></span>                                 |



 

## <a name="what-tools-do-i-need-to-develop-a-windows-game-with-directx"></a><span data-ttu-id="8f0bb-144">Welche Tools benötige ich, um ein Windows-Spiel mit DirectX zu entwickeln?</span><span class="sxs-lookup"><span data-stu-id="8f0bb-144">What tools do I need to develop a Windows game with DirectX?</span></span>

<span data-ttu-id="8f0bb-145">Für den Einstieg in dieses Tutorial benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8f0bb-145">To get started with this tutorial, you need:</span></span>

-   <span data-ttu-id="8f0bb-146">Windows 8.1 oder höher</span><span class="sxs-lookup"><span data-stu-id="8f0bb-146">Windows 8.1 or greater</span></span>
-   <span data-ttu-id="8f0bb-147">Microsoft Visual Studio 2013 oder höher</span><span class="sxs-lookup"><span data-stu-id="8f0bb-147">Microsoft Visual Studio 2013 or greater</span></span>

 

 




