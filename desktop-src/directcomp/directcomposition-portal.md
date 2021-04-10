---
title: DirectComposition
description: In diesem Thema wird der Zweck von Microsoft directcomposition erläutert, dessen Lauf Zeitanforderungen identifiziert und der Programmier Hintergrund beschrieben, den Sie für die effektive Verwendung von Microsoft directcomposition benötigen.
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- Directcomposition-API
- Microsoft directcomposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb34a4bb3bb7c0ffe370777888e20704fd0165d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309631"
---
# <a name="directcomposition"></a><span data-ttu-id="f11e6-106">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="f11e6-106">DirectComposition</span></span>

> [!NOTE]
> <span data-ttu-id="f11e6-107">Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen.</span><span class="sxs-lookup"><span data-stu-id="f11e6-107">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="f11e6-108">Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="f11e6-108">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

## <a name="purpose"></a><span data-ttu-id="f11e6-109">Zweck</span><span class="sxs-lookup"><span data-stu-id="f11e6-109">Purpose</span></span>

<span data-ttu-id="f11e6-110">Microsoft directcomposition ist eine Windows-Komponente, die eine leistungsstarke bitmapkomposition mit Transformationen, Effekten und Animationen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="f11e6-110">Microsoft DirectComposition is a Windows component that enables high-performance bitmap composition with transforms, effects, and animations.</span></span> <span data-ttu-id="f11e6-111">Anwendungsentwickler können die DirectComposition-API zum Erstellen von visuell ansprechenden Benutzeroberflächen verwenden, die umfassende und fließende animierte Übergänge von einem visuellen Objekt zum nächsten ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f11e6-111">Application developers can use the DirectComposition API to create visually engaging user interfaces that feature rich and fluid animated transitions from one visual to another.</span></span>

<span data-ttu-id="f11e6-112">Directcomposition ermöglicht umfassende und fließende Übergänge durch das Erreichen einer hohen Framerate, die Verwendung von Grafikhardware und die unabhängige Funktionsweise des UI-Threads.</span><span class="sxs-lookup"><span data-stu-id="f11e6-112">DirectComposition enables rich and fluid transitions by achieving a high framerate, using graphics hardware, and operating independently of the UI thread.</span></span> <span data-ttu-id="f11e6-113">Directcomposition kann bitmapinhalte akzeptieren, die von verschiedenen renderingbibliotheken gezeichnet werden, einschließlich Microsoft DirectX-Bitmaps und Bitmaps, die in einem Fenster (HWND-Bitmaps) gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="f11e6-113">DirectComposition can accept bitmap content drawn by different rendering libraries, including Microsoft DirectX bitmaps, and bitmaps rendered to a window (HWND bitmaps).</span></span> <span data-ttu-id="f11e6-114">Außerdem unterstützt directcomposition eine Vielzahl von Transformationen, wie z. b. 2D-affine Transformationen und 3D-Perspektiven Transformationen, sowie grundlegende Effekte wie Clipping und Deckkraft.</span><span class="sxs-lookup"><span data-stu-id="f11e6-114">Also, DirectComposition supports a variety of transformations, such as 2D affine transforms and 3D perspective transforms, as well as basic effects such as clipping and opacity.</span></span>

<span data-ttu-id="f11e6-115">Directcomposition ist so konzipiert, dass die Erstellung von [*visuellen*](directcomposition-glossary.md) Elementen und die Erstellung animierter Übergänge vereinfacht werden.</span><span class="sxs-lookup"><span data-stu-id="f11e6-115">DirectComposition is designed to simplify the process of composing [*visuals*](directcomposition-glossary.md) and creating animated transitions.</span></span> <span data-ttu-id="f11e6-116">Wenn Ihre Anwendung bereits Renderingcode enthält oder bereits die empfohlene DirectX-API verwendet, müssen Sie nur eine minimale Menge an Arbeit durchführen, um directcomposition effektiv zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f11e6-116">If your application already contains rendering code or already uses the recommended DirectX API, you only need to do a minimal amount of work to use DirectComposition effectively.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="f11e6-117">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="f11e6-117">Developer audience</span></span>

<span data-ttu-id="f11e6-118">Die directcomposition-API ist für erfahrene und hochgradig leistungsfähige Grafik Entwickler gedacht, die C/C++ kennen, ein solides Verständnis der Component Object Model (com) haben und mit den Windows-Programmier Konzepten vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="f11e6-118">The DirectComposition API is intended for experienced and highly-capable graphics developers who know C/C++, have a solid understanding of the Component Object Model (COM), and are familiar with Windows programming concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f11e6-119">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="f11e6-119">Run-time requirements</span></span>

<span data-ttu-id="f11e6-120">Directcomposition wurde in Windows 8 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f11e6-120">DirectComposition was introduced in Windows 8.</span></span> <span data-ttu-id="f11e6-121">Es ist in 32-Bit-, 64-Bit-und Arm-Plattformen enthalten.</span><span class="sxs-lookup"><span data-stu-id="f11e6-121">It is included in 32-bit, 64-bit, and ARM platforms.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f11e6-122">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f11e6-122">In this section</span></span>



| <span data-ttu-id="f11e6-123">Thema</span><span class="sxs-lookup"><span data-stu-id="f11e6-123">Topic</span></span>                                                                       | <span data-ttu-id="f11e6-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f11e6-124">Description</span></span>                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f11e6-125">Gründe für die Verwendung von directcomposition</span><span class="sxs-lookup"><span data-stu-id="f11e6-125">Why use DirectComposition?</span></span>](why-use-directcomposition-.md)<br/>     | <span data-ttu-id="f11e6-126">In diesem Thema werden die Funktionen und Vorteile von directcomposition beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f11e6-126">This topic describes the capabilities and benefits of DirectComposition.</span></span> <br/>                                                                           |
| [<span data-ttu-id="f11e6-127">Verwenden von directcomposition</span><span class="sxs-lookup"><span data-stu-id="f11e6-127">How to Use DirectComposition</span></span>](how-to-use-directcomposition.md)<br/> | <span data-ttu-id="f11e6-128">In diesem Abschnitt werden bewährte Methoden für die Verwendung der directcomposition-API beschrieben, und es wird veranschaulicht, wie die API verwendet wird, um mehrere gängige Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f11e6-128">This section describes best practices for using the DirectComposition API, and demonstrates how to use the API to accomplish several common tasks.</span></span> <br/> |
| [<span data-ttu-id="f11e6-129">Directcomposition-Konzepte</span><span class="sxs-lookup"><span data-stu-id="f11e6-129">DirectComposition concepts</span></span>](directcomposition-concepts.md)<br/>     | <span data-ttu-id="f11e6-130">Dieser Abschnitt enthält eine konzeptionelle Übersicht über directcomposition.</span><span class="sxs-lookup"><span data-stu-id="f11e6-130">This section provides a conceptual overview of DirectComposition.</span></span><br/>                                                                                   |
| [<span data-ttu-id="f11e6-131">Directcomposition-Referenz</span><span class="sxs-lookup"><span data-stu-id="f11e6-131">DirectComposition reference</span></span>](reference.md)<br/>                     | <span data-ttu-id="f11e6-132">Dieser Abschnitt enthält ausführliche Referenzinformationen zu den Elementen, die die directcomposition-API bilden.</span><span class="sxs-lookup"><span data-stu-id="f11e6-132">This section provides detailed reference information for the elements that make up the DirectComposition API.</span></span><br/>                                       |
| [<span data-ttu-id="f11e6-133">Directcomposition-Beispiele</span><span class="sxs-lookup"><span data-stu-id="f11e6-133">DirectComposition samples</span></span>](directcomposition-code-samples.md)<br/>  | <span data-ttu-id="f11e6-134">Die folgenden Beispielanwendungen zeigen, wie Sie die directcomposition-API verwenden und ihre Funktionen veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="f11e6-134">The following sample applications show how to use the DirectComposition API and demonstrate its capabilities.</span></span> <br/>                                      |
| [<span data-ttu-id="f11e6-135">Directcomposition-Glossar</span><span class="sxs-lookup"><span data-stu-id="f11e6-135">DirectComposition glossary</span></span>](directcomposition-glossary.md)<br/>     | <span data-ttu-id="f11e6-136">In diesem Thema werden die directcomposition-Begriffe definiert.</span><span class="sxs-lookup"><span data-stu-id="f11e6-136">This topic defines DirectComposition terms.</span></span> <br/>                                                                                                        |



 

 

 





