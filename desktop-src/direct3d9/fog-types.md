---
description: 'Es gibt zwei Möglichkeiten zum Hinzufügen von Nebel zu einer Szene: mit Pixel Nebel und/oder Scheitelpunkt Nebel.'
ms.assetid: 96531830-2df1-40d4-af46-09b1ca153834
title: Nebel Typen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5dd845373ac4a42a32ab7a9965501df4894568
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123866"
---
# <a name="fog-types-direct3d-9"></a><span data-ttu-id="db19f-103">Nebel Typen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="db19f-103">Fog Types (Direct3D 9)</span></span>

<span data-ttu-id="db19f-104">Es gibt zwei Möglichkeiten zum Hinzufügen von Nebel zu einer Szene: mit Pixel Nebel und/oder Scheitelpunkt Nebel.</span><span class="sxs-lookup"><span data-stu-id="db19f-104">There are two ways to add fog to a scene: with pixel fog and/or vertex fog.</span></span> <span data-ttu-id="db19f-105">In den folgenden Themen werden die in den Nebel Gleichungen verwendeten Formeln und die Implementierung von Scheitelpunkt und Pixel Nebel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="db19f-105">The following topics illustrate the formulas used in fog equations, as well as implementing vertex and pixel fog.</span></span> <span data-ttu-id="db19f-106">Eine Anwendung kann Nebel mit einem Vertexshader implementieren und ggf. Pixel Nebel gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="db19f-106">An application can implement fog with a vertex shader, and pixel fog simultaneously if desired.</span></span>

-   [<span data-ttu-id="db19f-107">Nebel Formeln</span><span class="sxs-lookup"><span data-stu-id="db19f-107">Fog Formulas</span></span>](fog-formulas.md)
-   [<span data-ttu-id="db19f-108">Nebel Parameter</span><span class="sxs-lookup"><span data-stu-id="db19f-108">Fog Parameters</span></span>](fog-parameters.md)
-   [<span data-ttu-id="db19f-109">Nebel Mischung</span><span class="sxs-lookup"><span data-stu-id="db19f-109">Fog Blending</span></span>](fog-blending.md)
-   [<span data-ttu-id="db19f-110">Nebelfarbe</span><span class="sxs-lookup"><span data-stu-id="db19f-110">Fog Color</span></span>](fog-color.md)
-   [<span data-ttu-id="db19f-111">Scheitelpunkt Nebel</span><span class="sxs-lookup"><span data-stu-id="db19f-111">Vertex Fog</span></span>](vertex-fog.md)
-   [<span data-ttu-id="db19f-112">Pixel Nebel</span><span class="sxs-lookup"><span data-stu-id="db19f-112">Pixel Fog</span></span>](pixel-fog.md)

<span data-ttu-id="db19f-113">Nebel Mischung wird durch Rendering-Zustände gesteuert. Sie ist nicht Teil der programmierbaren Pixel Pipeline.</span><span class="sxs-lookup"><span data-stu-id="db19f-113">Fog blending is controlled by render states; it is not part of the programmable pixel pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db19f-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="db19f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db19f-115">Frame Puffer</span><span class="sxs-lookup"><span data-stu-id="db19f-115">Frame Buffer</span></span>](frame-buffer.md)
</dt> </dl>

 

 



