---
description: Diese Optionen identifizieren Abfrageressourcentypen.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 038cb64b1ad4f5f7ee2dd78ffc2e2a5ebab90d0e
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342985"
---
# <a name="d3dusage_query"></a><span data-ttu-id="df239-103">D3DUSAGE-ABFRAGE \_</span><span class="sxs-lookup"><span data-stu-id="df239-103">D3DUSAGE\_QUERY</span></span>

<span data-ttu-id="df239-104">Diese Optionen identifizieren Abfrageressourcentypen.</span><span class="sxs-lookup"><span data-stu-id="df239-104">These options identify query resource types.</span></span>



| <span data-ttu-id="df239-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="df239-105">\#define</span></span>                                   | <span data-ttu-id="df239-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df239-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df239-107">\_D3DUSAGE-ABFRAGEFILTER \_</span><span class="sxs-lookup"><span data-stu-id="df239-107">D3DUSAGE\_QUERY\_FILTER</span></span>                    | <span data-ttu-id="df239-108">Fragen Sie das Ressourcenformat ab, um festzustellen, ob es andere Texturfiltertypen als D3DTEXF POINT unterstützt \_ (was immer unterstützt wird).</span><span class="sxs-lookup"><span data-stu-id="df239-108">Query the resource format to see if it supports texture filter types other than D3DTEXF\_POINT (which is always supported).</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="df239-109">D3DUSAGE \_ QUERY \_ LEGACYBUMPMAP</span><span class="sxs-lookup"><span data-stu-id="df239-109">D3DUSAGE\_QUERY\_LEGACYBUMPMAP</span></span>             | <span data-ttu-id="df239-110">Fragen Sie die Ressource nach einer Legacy-Bump map ab.</span><span class="sxs-lookup"><span data-stu-id="df239-110">Query the resource about a legacy bump map.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="df239-111">D3DUSAGE \_ QUERY \_ POSTPIXELSHADER \_ BLENDING</span><span class="sxs-lookup"><span data-stu-id="df239-111">D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING</span></span> | <span data-ttu-id="df239-112">Fragen Sie die Ressource ab, um die Unterstützung für die Unterstützung der Vermischung von Postpixel-Shadern zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="df239-112">Query the resource to verify support for post pixel shader blending support.</span></span> <span data-ttu-id="df239-113">Wenn [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit D3DUSAGE \_ QUERY \_ POSTPIXELSHADER \_ BLENDING fehlschlägt, werden Postpixelmischungsvorgänge nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="df239-113">If [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) fails with D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING, post pixel blending operations are not supported.</span></span> <span data-ttu-id="df239-114">Dazu gehören Alphatest, Pixelzeil, Render-Ziel-Blending, Aktivieren von Farbschreib- und Dithering.</span><span class="sxs-lookup"><span data-stu-id="df239-114">These include alpha test, pixel fog, render-target blending, color write enable, and dithering.</span></span> |
| <span data-ttu-id="df239-115">D3DUSAGE \_ QUERY \_ SRGBREAD</span><span class="sxs-lookup"><span data-stu-id="df239-115">D3DUSAGE\_QUERY\_SRGBREAD</span></span>                  | <span data-ttu-id="df239-116">Fragen Sie die Ressource ab, um zu überprüfen, ob eine Textur die Gammakorrektur während eines Lesevorgangs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="df239-116">Query the resource to verify if a texture supports gamma correction during a read operation.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="df239-117">D3DUSAGE \_ QUERY \_ SRGBWRITE</span><span class="sxs-lookup"><span data-stu-id="df239-117">D3DUSAGE\_QUERY\_SRGBWRITE</span></span>                 | <span data-ttu-id="df239-118">Fragen Sie die Ressource ab, um zu überprüfen, ob eine Textur die Gammakorrektur während eines Schreibvorgangs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="df239-118">Query the resource to verify if a texture supports gamma correction during a write operation.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="df239-119">D3DUSAGE \_ QUERY \_ VERTEXTEXTURE</span><span class="sxs-lookup"><span data-stu-id="df239-119">D3DUSAGE\_QUERY\_VERTEXTEXTURE</span></span>             | <span data-ttu-id="df239-120">Fragen Sie die Ressource ab, um die Unterstützung für die Textursampling des Vertex-Shaders zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="df239-120">Query the resource to verify support for vertex shader texture sampling.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="df239-121">D3DUSAGE \_ QUERY \_ WRAPANDMIP</span><span class="sxs-lookup"><span data-stu-id="df239-121">D3DUSAGE\_QUERY\_WRAPANDMIP</span></span>                | <span data-ttu-id="df239-122">Fragen Sie die Ressource ab, um die Unterstützung für Texturumbruch und Mip-Zuordnung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="df239-122">Query the resource to verify support for texture wrapping and mip-mapping.</span></span>                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="df239-123">Verwenden [**Sie CheckDeviceFormat,**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) um die Hardwareunterstützung für diese Verwendungen und einige andere in [D3DUSAGE aufgeführte Verwendungen abfragt.](d3dusage.md)</span><span class="sxs-lookup"><span data-stu-id="df239-123">Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) to query hardware support for these usages, and some other usages listed in [D3DUSAGE](d3dusage.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="df239-124">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="df239-124">Constant Information</span></span>



| <span data-ttu-id="df239-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df239-125">Requirement</span></span>                         | <span data-ttu-id="df239-126">Wert</span><span class="sxs-lookup"><span data-stu-id="df239-126">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="df239-127">Header</span><span class="sxs-lookup"><span data-stu-id="df239-127">Header</span></span>                   | <span data-ttu-id="df239-128">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="df239-128">d3d9types.h</span></span> |
| <span data-ttu-id="df239-129">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="df239-129">Minimum operating system</span></span> | <span data-ttu-id="df239-130">Windows 98</span><span class="sxs-lookup"><span data-stu-id="df239-130">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="df239-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df239-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df239-132">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="df239-132">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
