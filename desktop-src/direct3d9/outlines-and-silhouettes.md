---
description: Sie können den Schablonen Puffer für abstraktere Effekte verwenden, z. b. Gliederung und Silhouette.
ms.assetid: 8b9cd2b3-c1bf-4ac9-aae5-7fc0c9e049ff
title: Kontur und Silhouetten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a282b650b96cdbb36dc252e1f31cb81d91f0bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745536"
---
# <a name="outlines-and-silhouettes-direct3d-9"></a><span data-ttu-id="361bc-103">Kontur und Silhouetten (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="361bc-103">Outlines and Silhouettes (Direct3D 9)</span></span>

<span data-ttu-id="361bc-104">Sie können den Schablonen Puffer für abstraktere Effekte verwenden, z. b. Gliederung und Silhouette.</span><span class="sxs-lookup"><span data-stu-id="361bc-104">You can use the stencil buffer for more abstract effects, such as outlining and silhouetting.</span></span>

<span data-ttu-id="361bc-105">Wenn Ihre Anwendung eine Schablone-Maske auf das Bild eines primitiven anwendet, das dieselbe Form aufweist, aber etwas kleiner ist, enthält das resultierende Bild nur den Umriss des primitiven.</span><span class="sxs-lookup"><span data-stu-id="361bc-105">If your application applies a stencil mask to the image of a primitive that is the same shape but slightly smaller, the resulting image contains only the primitive's outline.</span></span> <span data-ttu-id="361bc-106">Die Anwendung kann dann den Bereich der Schablone maskiert mit einer voll Tonfarbe ausfüllen, wodurch dem primitiven ein geprägte Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="361bc-106">The application can then fill the stencil-masked area of the image with a solid color, giving the primitive an embossed look.</span></span>

<span data-ttu-id="361bc-107">Wenn die Schablone-Maske dieselbe Größe und Form wie das primitive-Format aufweist, das Sie rendern, enthält das resultierende Bild eine Lücke, in der der primitive entsprechen sollte.</span><span class="sxs-lookup"><span data-stu-id="361bc-107">If the stencil mask is the same size and shape as the primitive you are rendering, the resulting image contains a hole where the primitive should be.</span></span> <span data-ttu-id="361bc-108">Die Anwendung kann dann das Loch mit Black auffüllen, um eine Silhouette des primitiven zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="361bc-108">Your application can then fill the hole with black to produce a silhouette of the primitive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="361bc-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="361bc-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="361bc-110">Techniken für Schablonen Puffer</span><span class="sxs-lookup"><span data-stu-id="361bc-110">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



