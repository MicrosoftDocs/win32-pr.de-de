---
title: MipMap-Verpackung
description: Abhängig von der Ebene der Unterstützung für gekachelte Ressourcen folgen Mipmaps mit bestimmten Dimensionen nicht den standardmäßigen Kachel Formen und werden als alle in einer Weise, die für die Anwendung nicht transparent ist, in eine Weise verpackt.
ms.assetid: 3B416324-7656-495F-9BA9-8F5BE475ABC1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db4cd6f70129f46495673dfc82b5d261210ab21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036672"
---
# <a name="mipmap-packing"></a><span data-ttu-id="312a5-103">MipMap-Verpackung</span><span class="sxs-lookup"><span data-stu-id="312a5-103">Mipmap packing</span></span>

<span data-ttu-id="312a5-104">Abhängig von der [Ebene](tiled-resources-features-tiers.md) der Unterstützung für gekachelte Ressourcen folgen Mipmaps mit bestimmten Dimensionen nicht den standardmäßigen Kachel Formen und werden als alle in einer Weise, die für die Anwendung nicht transparent ist, in eine Weise verpackt.</span><span class="sxs-lookup"><span data-stu-id="312a5-104">Depending on the [tier](tiled-resources-features-tiers.md) of tiled resources support, mipmaps with certain dimensions don't follow the standard tile shapes and are considered to all be packed together with one another in a manner that is opaque to the application.</span></span> <span data-ttu-id="312a5-105">Höhere Ebenen der Unterstützung haben eine umfassendere Garantie, welche Arten von Oberflächen Dimensionen in die standardmäßigen Kachel Formen passen (und daher einzeln von Anwendungen zugeordnet werden können).</span><span class="sxs-lookup"><span data-stu-id="312a5-105">Higher tiers of support have broader guarantees about what types of surface dimensions fit in the standard tile shapes (and can therefore be individually mapped by applications).</span></span>

<span data-ttu-id="312a5-106">Die Unterschiede zwischen den Implementierungen bestehen darin, dass – mit den Dimensionen, dem Format, der Anzahl von Mipmaps und den Array Segmenten – eine Menge von MIPS (pro Array Slice) in einige Zahl N Kacheln gepackt werden kann.</span><span class="sxs-lookup"><span data-stu-id="312a5-106">What can vary between implementations is that—given a tiled resource's dimensions, format, number of mipmaps, and array slices—some number M of mips (per array slice) can be packed into some number N tiles.</span></span> <span data-ttu-id="312a5-107">Die [**ID3D11Device2:: getresourcetielt**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) -API ist vorhanden, damit der Treiber an die Anwendung übermittelt werden kann, was M und N sind (neben anderen Details über die Oberfläche, die von dieser API als Standard und nicht vom Hardwarehersteller abweichen).</span><span class="sxs-lookup"><span data-stu-id="312a5-107">The [**ID3D11Device2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) API exists to allow the driver to report to the application what M and N are (among other details about the surface that this API reports that are standard and don't vary by hardware vendor).</span></span> <span data-ttu-id="312a5-108">Der Satz von Kacheln für den verpackten MIPS beträgt weiterhin 64 KB und kann einzeln in verschiedenen Speicherorten in einem Kachel Pool zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="312a5-108">The set of tiles for the packed mips are still 64KB and can be individually mapped into disparate locations in a tile pool.</span></span> <span data-ttu-id="312a5-109">Die Pixel Form der Kacheln und die Art und Weise, wie die Mipmaps in den Satz von Kacheln passen, ist für einen Hardware Anbieter spezifisch und zu komplex.</span><span class="sxs-lookup"><span data-stu-id="312a5-109">But the pixel shape of the tiles and how the mipmaps fit across the set of tiles is specific to a hardware vendor and too complex to expose.</span></span> <span data-ttu-id="312a5-110">Anwendungen müssen also entweder alle Kacheln zuordnen, die als gepackt gekennzeichnet sind, oder keine von Ihnen.</span><span class="sxs-lookup"><span data-stu-id="312a5-110">So, applications are required to either map all of the tiles that are designated as packed, or none of them, at a time.</span></span> <span data-ttu-id="312a5-111">Andernfalls ist das Verhalten für den Zugriff auf die gekachelte Ressource nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="312a5-111">Otherwise, the behavior for accessing the tiled resource is undefined.</span></span>

<span data-ttu-id="312a5-112">Für hochgeladene Oberflächen gilt der Satz von verpackten MIPS und die Anzahl der gepackten Kacheln, die diese MIPS speichern (M und N, die zuvor beschrieben wurden), für jeden Array Slice einzeln.</span><span class="sxs-lookup"><span data-stu-id="312a5-112">For arrayed surfaces, the set of packed mips and the number of packed tiles storing those mips (M and N described preceding) applies individually for each array slice.</span></span>

<span data-ttu-id="312a5-113">Dedizierte APIs zum Kopieren von Kacheln ([**ID3D11DeviceContext2:: copytiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) und [**ID3D11DeviceContext2:: updatetiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) können nicht auf gepackte MIPS zugreifen.</span><span class="sxs-lookup"><span data-stu-id="312a5-113">Dedicated APIs for copying tiles ([**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) and [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) can't access packed mips.</span></span> <span data-ttu-id="312a5-114">Anwendungen, die Daten in und aus gepackten MIPS kopieren möchten, können dies mit allen nicht gekachelten Ressourcen spezifischen APIs zum Kopieren und Rendern von-Oberflächen tun.</span><span class="sxs-lookup"><span data-stu-id="312a5-114">Applications that want to copy data to and from packed mips can do so using all the non-tiled resource specific APIs for copying and rendering to surfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="312a5-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="312a5-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="312a5-116">Kacheln eines gekachelten Ressourcenbereichs</span><span class="sxs-lookup"><span data-stu-id="312a5-116">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 




