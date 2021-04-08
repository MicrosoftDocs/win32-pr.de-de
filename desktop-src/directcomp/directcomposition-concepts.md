---
title: Directcomposition-Konzepte
description: Dieser Abschnitt enthält eine konzeptionelle Übersicht über directcomposition.
ms.assetid: 7839C264-C15F-4E89-82B6-2963A5C61CEC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea823d2edd27b2c725cefdd73cd053e94124d7f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037768"
---
# <a name="directcomposition-concepts"></a><span data-ttu-id="5b82e-103">Directcomposition-Konzepte</span><span class="sxs-lookup"><span data-stu-id="5b82e-103">DirectComposition concepts</span></span>

> [!NOTE]
> <span data-ttu-id="5b82e-104">Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen.</span><span class="sxs-lookup"><span data-stu-id="5b82e-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="5b82e-105">Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="5b82e-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="5b82e-106">Dieser Abschnitt enthält eine konzeptionelle Übersicht über directcomposition.</span><span class="sxs-lookup"><span data-stu-id="5b82e-106">This section provides a conceptual overview of DirectComposition.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5b82e-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5b82e-107">In this section</span></span>



| <span data-ttu-id="5b82e-108">Thema</span><span class="sxs-lookup"><span data-stu-id="5b82e-108">Topic</span></span>                                                                     | <span data-ttu-id="5b82e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b82e-109">Description</span></span>                                                                                                                                                                            |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b82e-110">Grundlegende Konzepte</span><span class="sxs-lookup"><span data-stu-id="5b82e-110">Basic concepts</span></span>](basic-concepts.md)<br/>                           | <span data-ttu-id="5b82e-111">Dieses Thema enthält eine Übersicht über die grundlegenden Konzepte von Microsoft directcomposition.</span><span class="sxs-lookup"><span data-stu-id="5b82e-111">This topic provides an overview of the basic concepts of Microsoft DirectComposition.</span></span><br/>                                                                                       |
| [<span data-ttu-id="5b82e-112">Bitmap-Objekte</span><span class="sxs-lookup"><span data-stu-id="5b82e-112">Bitmap objects</span></span>](bitmap-surfaces.md)<br/>                          | <span data-ttu-id="5b82e-113">In diesem Thema werden die Typen von Bitmapinhalten beschrieben, die von directcomposition unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="5b82e-113">This topic describes the types of bitmap content that DirectComposition supports.</span></span><br/>                                                                                           |
| [<span data-ttu-id="5b82e-114">Kompositions Oberfläche</span><span class="sxs-lookup"><span data-stu-id="5b82e-114">Composition surface</span></span>](composition-surface.md)<br/>                 | <span data-ttu-id="5b82e-115">In diesem Thema werden die Typen von Oberflächen beschrieben, die von directcomposition unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="5b82e-115">This topic describes the types of types of surfaces that DirectComposition supports.</span></span><br/>                                                                                        |
| [<span data-ttu-id="5b82e-116">Transformationen</span><span class="sxs-lookup"><span data-stu-id="5b82e-116">Transforms</span></span>](transforms.md)<br/>                                   | <span data-ttu-id="5b82e-117">In diesem Thema wird die Unterstützung von directcomposition für zweidimensionale (2D) affine (lineare) Transformationen erläutert, und es werden die Typen von Transformationen beschrieben, die von directcomposition unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="5b82e-117">This topic discusses DirectComposition support for two-dimensional (2D) affine (linear) transforms, and describes the types of transforms that DirectComposition supports.</span></span> <br/> |
| [<span data-ttu-id="5b82e-118">Effekte</span><span class="sxs-lookup"><span data-stu-id="5b82e-118">Effects</span></span>](effects.md)<br/>                                         | <span data-ttu-id="5b82e-119">In diesem Thema werden die Grundlagen von directcomposition-Effekten erläutert, und es werden die von directcomposition unterstützten Auswirkungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5b82e-119">This topic discusses the basics of DirectComposition effects, and describes the types of effects that DirectComposition supports.</span></span> <br/>                                          |
| [<span data-ttu-id="5b82e-120">Animation</span><span class="sxs-lookup"><span data-stu-id="5b82e-120">Animation</span></span>](animation.md)<br/>                                     | <span data-ttu-id="5b82e-121">In diesem Thema werden die Grundlagen der directcomposition-Animation erläutert.</span><span class="sxs-lookup"><span data-stu-id="5b82e-121">This topic discusses the basics of DirectComposition animation.</span></span> <br/>                                                                                                            |
| [<span data-ttu-id="5b82e-122">Freistellen</span><span class="sxs-lookup"><span data-stu-id="5b82e-122">Clipping</span></span>](clipping.md)<br/>                                       | <span data-ttu-id="5b82e-123">In diesem Thema wird die Unterstützung von directcomposition zum Abschneiden von visuellen Elementen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5b82e-123">This topic describes DirectComposition support for clipping visuals.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="5b82e-124">Architektur und Komponenten</span><span class="sxs-lookup"><span data-stu-id="5b82e-124">Architecture and components</span></span>](architecture-and-components.md)<br/> | <span data-ttu-id="5b82e-125">In diesem Thema werden die Komponenten beschrieben, die directcomposition bilden.</span><span class="sxs-lookup"><span data-stu-id="5b82e-125">This topic describes the components that make up DirectComposition.</span></span><br/>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="5b82e-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5b82e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b82e-127">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="5b82e-127">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 





