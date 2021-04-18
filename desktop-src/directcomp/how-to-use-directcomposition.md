---
title: Verwenden von directcomposition
description: In diesem Abschnitt werden bewährte Methoden für die Verwendung von Microsoft directcomposition \ 32; beschrieben. API und veranschaulicht, wie die API verwendet wird, um mehrere häufige Aufgaben auszuführen.
ms.assetid: 49F6E356-90C7-423A-A31A-AEE41F882D3B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0658a9693567dfd88e9a986893048fa1d0fa1e5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106340463"
---
# <a name="how-to-use-directcomposition"></a><span data-ttu-id="eb7d2-103">Verwenden von directcomposition</span><span class="sxs-lookup"><span data-stu-id="eb7d2-103">How to use DirectComposition</span></span>

> [!NOTE]
> <span data-ttu-id="eb7d2-104">Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen.</span><span class="sxs-lookup"><span data-stu-id="eb7d2-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="eb7d2-105">Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="eb7d2-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="eb7d2-106">In diesem Abschnitt werden bewährte Methoden für die Verwendung der Microsoft directcomposition-API beschrieben, und es wird veranschaulicht, wie die API verwendet wird, um mehrere häufige Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="eb7d2-106">This section describes best practices for using the Microsoft DirectComposition API, and demonstrates how to use the API to accomplish several common tasks.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="eb7d2-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="eb7d2-107">In this section</span></span>



| <span data-ttu-id="eb7d2-108">Thema</span><span class="sxs-lookup"><span data-stu-id="eb7d2-108">Topic</span></span>                                                                                                                      | <span data-ttu-id="eb7d2-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb7d2-109">Description</span></span>                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb7d2-110">Bewährte Methoden für directcomposition</span><span class="sxs-lookup"><span data-stu-id="eb7d2-110">Best practices for DirectComposition</span></span>](best-practices-for-directcomposition.md)<br/>                                | <span data-ttu-id="eb7d2-111">In diesem Thema werden bewährte Methoden für die Verwendung von directcomposition beschrieben.</span><span class="sxs-lookup"><span data-stu-id="eb7d2-111">This topic describes best practices for using DirectComposition.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="eb7d2-112">Initialisieren von directcomposition</span><span class="sxs-lookup"><span data-stu-id="eb7d2-112">How to initialize DirectComposition</span></span>](initialize-directcomposition.md)<br/>                                         | <span data-ttu-id="eb7d2-113">In diesem Thema wird veranschaulicht, wie der minimale Satz von directcomposition-Objekten, die zum Erstellen einer einfachen Komposition benötigt werden, erstellt und initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="eb7d2-113">This topic demonstrates how to create and initialize the minimum set of DirectComposition objects needed to create a simple composition.</span></span><br/>                                                          |
| [<span data-ttu-id="eb7d2-114">Erstellen eines einfachen visuellen Baums</span><span class="sxs-lookup"><span data-stu-id="eb7d2-114">How to build a simple visual tree</span></span>](how-to--build-a-visual-tree.md)<br/>                                            | <span data-ttu-id="eb7d2-115">In diesem Thema wird veranschaulicht, wie Sie eine einfache visuelle directcomposition-Struktur erstellen.</span><span class="sxs-lookup"><span data-stu-id="eb7d2-115">This topic demonstrates how to build a simple DirectComposition visual tree.</span></span> <span data-ttu-id="eb7d2-116">Im Beispiel in diesem Thema wird eine visuelle Struktur erstellt und zusammengefasst, die aus einem visuellen Stamm Element und drei untergeordneten visuellen Elementen besteht.</span><span class="sxs-lookup"><span data-stu-id="eb7d2-116">The example in this topic builds and composes a visual tree that consists of a root visual and three child visuals.</span></span> <br/> |
| [<span data-ttu-id="eb7d2-117">Vorgehensweise beim Abschneiden mit einem Rechteck Clip-Objekt</span><span class="sxs-lookup"><span data-stu-id="eb7d2-117">How to clip with a rectangle clip object</span></span>](how-to--set-the-clip-rectangle-for-a-visual.md)<br/>                     | <span data-ttu-id="eb7d2-118">In diesem Thema wird veranschaulicht, wie ein Rechteck Clip-Objekt verwendet wird, um eine visuelle Struktur oder eine visuelle Struktur zu schneiden</span><span class="sxs-lookup"><span data-stu-id="eb7d2-118">This topic demonstrates how to use a rectangle clip object to clip a visual or visual tree.</span></span> <br/>                                                                                                      |
| [<span data-ttu-id="eb7d2-119">Anwenden von 2D-Transformationen</span><span class="sxs-lookup"><span data-stu-id="eb7d2-119">How to apply 2D transforms</span></span>](apply-2d-transforms.md)<br/>                                                           | <span data-ttu-id="eb7d2-120">In diesem Thema wird veranschaulicht, wie 2D-Transformationen mithilfe von directcomposition auf ein visuelles Element angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb7d2-120">This topic demonstrates how to apply 2D transforms to a visual by using DirectComposition.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="eb7d2-121">Anwenden von Effekten</span><span class="sxs-lookup"><span data-stu-id="eb7d2-121">How to apply effects</span></span>](how-to--apply-transforms-and-effects-to-a-visual.md)<br/>                                    | <span data-ttu-id="eb7d2-122">In diesem Thema wird die Verwendung von directcomposition zum Anwenden von Effekten und 3D-Transformationen auf ein visuelles Element veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="eb7d2-122">This topic demonstrates how to use DirectComposition to apply effects and 3D transformations to a visual.</span></span><br/>                                                                                         |
| [<span data-ttu-id="eb7d2-123">Anwenden von Animationen</span><span class="sxs-lookup"><span data-stu-id="eb7d2-123">How to apply animations</span></span>](how-to--animate-a-visual.md)<br/>                                                         | <span data-ttu-id="eb7d2-124">In diesem Thema wird veranschaulicht, wie die Eigenschaften eines visuellen Elements mithilfe von directcomposition animiert werden.</span><span class="sxs-lookup"><span data-stu-id="eb7d2-124">This topic demonstrates how to animate the properties of a visual by using DirectComposition.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="eb7d2-125">Animieren der Bitmap eines untergeordneten Fensters in Schichten</span><span class="sxs-lookup"><span data-stu-id="eb7d2-125">How to animate the bitmap of a layered child window</span></span>](how-to--animate-the-bitmap-of-a-layered-child-window.md)<br/> | <span data-ttu-id="eb7d2-126">In diesem Thema wird beschrieben, wie ein visuelles Element erstellt und animiert wird, das die Bitmap eines überlappenden untergeordneten Fensters als Inhalt der visuellen Elemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb7d2-126">This topic describes how to create and animate a visual that uses the bitmap of a layered child window as the visual's content.</span></span> <br/>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="eb7d2-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eb7d2-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb7d2-128">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="eb7d2-128">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 





