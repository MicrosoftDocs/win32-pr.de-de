---
title: Gründe für die Verwendung von directcomposition
description: In diesem Thema werden die Funktionen und Vorteile von Microsoft directcomposition beschrieben.
ms.assetid: D597E737-24A1-49E9-8861-9DDD6D7FF2F8
keywords:
- Gründe für die Verwendung von directcomposition
- Gründe für die Verwendung von directcomposition
- Directcomposition-Funktionen und-Vorteile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7ad68f779abc023b7645ed9e66f8af3bf63a140
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340520"
---
# <a name="why-use-directcomposition"></a><span data-ttu-id="5f001-106">Gründe für die Verwendung von directcomposition</span><span class="sxs-lookup"><span data-stu-id="5f001-106">Why use DirectComposition?</span></span>

> [!NOTE]
> <span data-ttu-id="5f001-107">Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen.</span><span class="sxs-lookup"><span data-stu-id="5f001-107">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="5f001-108">Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="5f001-108">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="5f001-109">In diesem Thema werden die Funktionen und Vorteile von Microsoft directcomposition beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5f001-109">This topic describes the capabilities and benefits of Microsoft DirectComposition.</span></span> <span data-ttu-id="5f001-110">Sie enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="5f001-110">It contains the following sections:</span></span>

-   [<span data-ttu-id="5f001-111">Erstellen einer visuell ansprechenden Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="5f001-111">Create a visually engaging user interface</span></span>](#create-a-visually-engaging-user-interface)
-   [<span data-ttu-id="5f001-112">Umfassende, reibungslose Animationen für Ihre Anwendung aktivieren</span><span class="sxs-lookup"><span data-stu-id="5f001-112">Enable rich, smooth animations for your application</span></span>](#enable-rich-smooth-animations-for-your-application)
-   [<span data-ttu-id="5f001-113">Kombinieren von Bitmaps aus einer Vielzahl von Quellen</span><span class="sxs-lookup"><span data-stu-id="5f001-113">Combine bitmaps from a variety of sources</span></span>](#combine-bitmaps-from-a-variety-of-sources)
-   [<span data-ttu-id="5f001-114">Speicher Einsparungen bei der Integration in DWM</span><span class="sxs-lookup"><span data-stu-id="5f001-114">Memory savings though integration with DWM</span></span>](#memory-savings-though-integration-with-dwm)
-   [<span data-ttu-id="5f001-115">Behalten Sie, was Sie bereits haben</span><span class="sxs-lookup"><span data-stu-id="5f001-115">Keep what you already have</span></span>](#keep-what-you-already-have)
-   [<span data-ttu-id="5f001-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5f001-116">Related topics</span></span>](#related-topics)

## <a name="create-a-visually-engaging-user-interface"></a><span data-ttu-id="5f001-117">Erstellen einer visuell ansprechenden Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="5f001-117">Create a visually engaging user interface</span></span>

<span data-ttu-id="5f001-118">Mithilfe von directcomposition können Sie [*visuelle*](directcomposition-glossary.md) Elemente kombinieren und animieren, um eine visuell ansprechende Benutzeroberfläche für Ihre Windows-basierten Anwendungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5f001-118">DirectComposition lets you combine and animate [*visuals*](directcomposition-glossary.md) to create a visually engaging UI for your Windows-based applications.</span></span> <span data-ttu-id="5f001-119">Es kann Ihnen helfen, Ihre Anwendung zu einem eindeutigen Aussehen und Gefühl zu machen, indem Sie eine Identität einrichten, die Sie von anderen Anwendungen unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="5f001-119">It can help give your application a unique look and feel, establishing an identity that sets it apart from other applications.</span></span>

<span data-ttu-id="5f001-120">Directcomposition kann auch helfen, die Verwendung Ihrer Anwendungen zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="5f001-120">DirectComposition can also help make your applications easier to use.</span></span> <span data-ttu-id="5f001-121">Beispielsweise kannst du damit visuelle Hinweise und animierte Bildschirmübergänge erzeugen, die die Beziehungen zwischen Elementen auf dem Bildschirm verdeutlichen.</span><span class="sxs-lookup"><span data-stu-id="5f001-121">For example, you can use it to create visual cues and animated screen transitions that show relationships among items on the screen.</span></span>

## <a name="enable-rich-smooth-animations-for-your-application"></a><span data-ttu-id="5f001-122">Umfassende, reibungslose Animationen für Ihre Anwendung aktivieren</span><span class="sxs-lookup"><span data-stu-id="5f001-122">Enable rich, smooth animations for your application</span></span>

<span data-ttu-id="5f001-123">Directcomposition ist eine hochleistungsfähige Bitmap-Kompositions-Engine, die hardwarebeschleunigte Grafiken verwendet, um hohe Frameraten zu erzielen. Dies führt zu Smooth-und konsistenten schwenken, scrollen und Animationen komplexer Inhalte.</span><span class="sxs-lookup"><span data-stu-id="5f001-123">DirectComposition is a high-performance bitmap composition engine that uses hardware-accelerated graphics to achieve high frame rates, resulting in smooth and consistent panning, scrolling, and animations of complex content.</span></span> <span data-ttu-id="5f001-124">Da es auf einem dedizierten Thread funktioniert, der von dem Thread getrennt ist, der zum Renderns der Anwendungs Benutzeroberfläche verwendet wird, kann directcomposition den UI-Thread niemals "verhungern" oder die Fähigkeit der Anwendung beeinträchtigen, seine Benutzeroberflächen Elemente zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="5f001-124">Because it operates on a dedicated thread that is separate from the thread used to render the application UI, DirectComposition can never "starve" the UI thread or interfere with the application's ability to draw its UI elements.</span></span>

## <a name="combine-bitmaps-from-a-variety-of-sources"></a><span data-ttu-id="5f001-125">Kombinieren von Bitmaps aus einer Vielzahl von Quellen</span><span class="sxs-lookup"><span data-stu-id="5f001-125">Combine bitmaps from a variety of sources</span></span>

<span data-ttu-id="5f001-126">Viele Windows-basierte Anwendungen verfügen über eine Benutzeroberfläche, die aus Elementen besteht, die von verschiedenen Grafik Frameworks erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5f001-126">Many Windows-based applications have a UI that consists of elements created by a variety of different graphics frameworks.</span></span> <span data-ttu-id="5f001-127">Eine Anwendung kann z. b. Windows Forms zum Erstellen einer Statusleiste, Windows Graphics Device Interface (GDI) zum Erstellen der Hauptfenster Inhalte, Microsoft DirectX für Grafik Inhalte usw. verwenden.</span><span class="sxs-lookup"><span data-stu-id="5f001-127">For example, an application might use Windows Forms to create a status bar, Windows Graphics Device Interface (GDI) to create the main window content, Microsoft DirectX for graphics content, and so on.</span></span> <span data-ttu-id="5f001-128">Directcomposition ermöglicht es Ihnen, den Inhalt aus einer Vielzahl von Grafik Frameworks zu kombinieren und ihn im gleichen oberen oder untergeordneten Fenster zu rendernieren, ohne sich Gedanken darüber machen zu müssen, was geschieht, wenn sich der Inhalt von verschiedenen Frameworks überschneidet.</span><span class="sxs-lookup"><span data-stu-id="5f001-128">DirectComposition enables you to combine the content from a variety of graphics frameworks and have it render to the same top-level or child window without needing to worry about what happens if the content from different frameworks overlaps.</span></span>

## <a name="memory-savings-though-integration-with-dwm"></a><span data-ttu-id="5f001-129">Speicher Einsparungen bei der Integration in DWM</span><span class="sxs-lookup"><span data-stu-id="5f001-129">Memory savings though integration with DWM</span></span>

<span data-ttu-id="5f001-130">Die von directcomposition erstellten Kompositionen und Animationen werden an eine integrierte Komponente von Windows mit dem Namen [Desktopfenster-Manager (DWM)](/windows/desktop/dwm/dwm-overview) für das Rendering auf dem Bildschirm übermittelt.</span><span class="sxs-lookup"><span data-stu-id="5f001-130">Compositions and animations created by DirectComposition are passed to a built-in component of Windows called [Desktop Window Manager (DWM)](/windows/desktop/dwm/dwm-overview) for rendering to the screen.</span></span> <span data-ttu-id="5f001-131">Daher sind keine besonderen renderingkomponenten oder Benutzeroberflächen-Frameworks auf dem Computer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5f001-131">Therefore, no special rendering components or UI frameworks are required on the computer.</span></span>

## <a name="keep-what-you-already-have"></a><span data-ttu-id="5f001-132">Behalten Sie, was Sie bereits haben</span><span class="sxs-lookup"><span data-stu-id="5f001-132">Keep what you already have</span></span>

<span data-ttu-id="5f001-133">Der UI-Code in einer vorhandenen Windows-basierten Anwendung stellt eine bedeutende Investition dar.</span><span class="sxs-lookup"><span data-stu-id="5f001-133">The UI code in an existing Windows-based application represents a significant investment.</span></span> <span data-ttu-id="5f001-134">Zum größten Teil können Sie mit directcomposition vorhandene Inhalte der Benutzeroberfläche verfassen und animieren.</span><span class="sxs-lookup"><span data-stu-id="5f001-134">For the most part, DirectComposition lets you compose and animate your existing UI content.</span></span> <span data-ttu-id="5f001-135">Dies bedeutet, dass Sie directcomposition verwenden können, um wichtige Aktualisierungen und Verbesserungen an der Benutzeroberfläche Ihrer Anwendung vorzunehmen, ohne umfassende Änderungen an der vorhandenen UI-Codebasis vornehmen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="5f001-135">This means you can use DirectComposition to make significant updates and enhancements to your application UI without needing to make extensive changes to your existing UI code base.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f001-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5f001-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f001-137">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="5f001-137">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 