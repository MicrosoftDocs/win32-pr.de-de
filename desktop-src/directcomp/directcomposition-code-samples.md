---
title: Directcomposition-Beispiele
description: Die folgenden Beispielanwendungen veranschaulichen die Verwendung von Microsoft directcomposition \ 32; API und veranschaulichen deren Funktionen.
ms.assetid: E2794CE7-20A3-4388-B1DC-D9822C970774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889ceb9a6f9383930b9231c9c19a2b610fba2815
ms.sourcegitcommit: 38c86be0218ed38d0f14db3df107db29827b6269
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390138"
---
# <a name="directcomposition-samples"></a><span data-ttu-id="2e83e-103">Directcomposition-Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e83e-103">DirectComposition samples</span></span>

> [!NOTE]
> <span data-ttu-id="2e83e-104">Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen.</span><span class="sxs-lookup"><span data-stu-id="2e83e-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="2e83e-105">Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="2e83e-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="2e83e-106">Die folgenden Beispielanwendungen zeigen, wie Sie die Microsoft directcomposition-API verwenden und ihre Funktionen veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="2e83e-106">The following sample applications show how to use the Microsoft DirectComposition API and demonstrate its capabilities.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2e83e-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="2e83e-107">In this section</span></span>



| <span data-ttu-id="2e83e-108">Thema</span><span class="sxs-lookup"><span data-stu-id="2e83e-108">Topic</span></span>                                                                                                                                 | <span data-ttu-id="2e83e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e83e-109">Description</span></span>                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e83e-110">Beispiel für ein untergeordnetes Fenster von directcomposition</span><span class="sxs-lookup"><span data-stu-id="2e83e-110">DirectComposition layered child window sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionLayeredChildWindow)<br/>                           | <span data-ttu-id="2e83e-111">Veranschaulicht die Verwendung von directcomposition zum Animieren der Bitmap eines untergeordneten Fensters in Schichten.</span><span class="sxs-lookup"><span data-stu-id="2e83e-111">Demonstrates how to use DirectComposition to animate the bitmap of a layered child window.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="2e83e-112">Verwalten der directcomposition-Animation mit dem Windows Animation Manager v2-Beispiel</span><span class="sxs-lookup"><span data-stu-id="2e83e-112">Managing DirectComposition animation with Windows Animation Manager v2 sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)<br/> | <span data-ttu-id="2e83e-113">Veranschaulicht, wie Windows Animation Manager v2 verwendet werden kann, um Animations Kurven (Funktionen) zu generieren, die von directcomposition genutzt werden können? zum Erstellen von animierten Übergängen in einer Desktop Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2e83e-113">Demonstrates how Windows Animation Manager v2 can be used to generate animation curves (functions) that can be consumed by DirectComposition? to create animated transitions in a desktop application.</span></span> <br/>                                                            |
| [<span data-ttu-id="2e83e-114">Directcomposition-Effekte mit Direct2D Bitmap-Inhalts Beispiel</span><span class="sxs-lookup"><span data-stu-id="2e83e-114">DirectComposition effects with Direct2D bitmap content sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionEffects)<br/>                                                     | <span data-ttu-id="2e83e-115">Veranschaulicht die Verwendung von directcomposition zum Anwenden von Animationen und Effekten auf visuelle Elemente mit Direct2D Bitmap-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="2e83e-115">Demonstrates how to use DirectComposition to apply animations and effects to visuals that have Direct2D bitmap content.</span></span> <br/>                                                                                                                                           |
| [<span data-ttu-id="2e83e-116">Beispiel für directcomposition-Backface und D2D-Batch Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="2e83e-116">DirectComposition Backface and D2D Batching sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DCompV2BackfaceandD2DBatching)<br/>                  | <span data-ttu-id="2e83e-117">Veranschaulicht, wie die directcomposition-API verwendet wird, um die Hintergrund Sichtbarkeit eines visuellen Elements zu übernehmen, um die Rückseite einer directcomposition-Visualisierung anzuzeigen und auszublenden.</span><span class="sxs-lookup"><span data-stu-id="2e83e-117">Demonstrates how to use the DirectComposition API to apply backface visibility to a visual element to show and hide the back side of a DirectComposition visual.</span></span> <span data-ttu-id="2e83e-118">In diesem Beispiel wird auch eine Leistungsoptimierung der Batch Verarbeitung D2D beginDraw/EndDraw-Aufrufe veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2e83e-118">This sample also demonstrates a performance optimization of batching D2D BeginDraw/EndDraw calls.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="2e83e-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2e83e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e83e-120">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="2e83e-120">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 





