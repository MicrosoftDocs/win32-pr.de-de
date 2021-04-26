---
description: Diese Optionen identifizieren Abfrageressourcentypen.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eac450ed722da26fe4885d41707483adf401f89
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994107"
---
# <a name="d3dusage_query"></a><span data-ttu-id="95731-103">D3DUSAGE-ABFRAGE \_</span><span class="sxs-lookup"><span data-stu-id="95731-103">D3DUSAGE\_QUERY</span></span>

<span data-ttu-id="95731-104">Diese Optionen identifizieren Abfrageressourcentypen.</span><span class="sxs-lookup"><span data-stu-id="95731-104">These options identify query resource types.</span></span>



| <span data-ttu-id="95731-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="95731-105">\#define</span></span>                                   | <span data-ttu-id="95731-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95731-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95731-107">D3DUSAGE-ABFRAGEFILTER \_ \_</span><span class="sxs-lookup"><span data-stu-id="95731-107">D3DUSAGE\_QUERY\_FILTER</span></span>                    | <span data-ttu-id="95731-108">Fragen Sie das Ressourcenformat ab, um zu sehen, ob es andere Texturfiltertypen als D3DTEXF \_ POINT unterstützt (was immer unterstützt wird).</span><span class="sxs-lookup"><span data-stu-id="95731-108">Query the resource format to see if it supports texture filter types other than D3DTEXF\_POINT (which is always supported).</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="95731-109">D3DUSAGE \_ QUERY \_ LEGACYBUMPMAP</span><span class="sxs-lookup"><span data-stu-id="95731-109">D3DUSAGE\_QUERY\_LEGACYBUMPMAP</span></span>             | <span data-ttu-id="95731-110">Fragen Sie die Ressource nach einer Legacy-Bumpmap ab.</span><span class="sxs-lookup"><span data-stu-id="95731-110">Query the resource about a legacy bump map.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="95731-111">D3DUSAGE \_ QUERY \_ POSTPIXELSHADER \_ BLENDING</span><span class="sxs-lookup"><span data-stu-id="95731-111">D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING</span></span> | <span data-ttu-id="95731-112">Fragen Sie die Ressource ab, um die Unterstützung für Shaderblending nach Pixel zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="95731-112">Query the resource to verify support for post pixel shader blending support.</span></span> <span data-ttu-id="95731-113">Wenn [**CheckDeviceFormat mit**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) D3DUSAGE \_ QUERY \_ POSTPIXELSHADER BLENDING fehlschlägt, werden Vorgänge nach dem Mischen von \_ Pixeln nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95731-113">If [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) fails with D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING, post pixel blending operations are not supported.</span></span> <span data-ttu-id="95731-114">Dazu gehören Alphatest, Pixelverblendung, Renderzielblending, Aktivieren des Farbschreibens und Dithering.</span><span class="sxs-lookup"><span data-stu-id="95731-114">These include alpha test, pixel fog, render-target blending, color write enable, and dithering.</span></span> |
| <span data-ttu-id="95731-115">D3DUSAGE \_ QUERY \_ SRGBREAD</span><span class="sxs-lookup"><span data-stu-id="95731-115">D3DUSAGE\_QUERY\_SRGBREAD</span></span>                  | <span data-ttu-id="95731-116">Fragen Sie die Ressource ab, um zu überprüfen, ob eine Textur die Gammakorrektur während eines Lesevorgang unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95731-116">Query the resource to verify if a texture supports gamma correction during a read operation.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="95731-117">D3DUSAGE \_ QUERY \_ SRGBWRITE</span><span class="sxs-lookup"><span data-stu-id="95731-117">D3DUSAGE\_QUERY\_SRGBWRITE</span></span>                 | <span data-ttu-id="95731-118">Fragen Sie die Ressource ab, um zu überprüfen, ob eine Textur die Gammakorrektur während eines Schreibvorgang unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95731-118">Query the resource to verify if a texture supports gamma correction during a write operation.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="95731-119">D3DUSAGE \_ QUERY \_ VERTEXTEXTURE</span><span class="sxs-lookup"><span data-stu-id="95731-119">D3DUSAGE\_QUERY\_VERTEXTEXTURE</span></span>             | <span data-ttu-id="95731-120">Fragen Sie die Ressource ab, um die Unterstützung für vertex shader texture sampling zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="95731-120">Query the resource to verify support for vertex shader texture sampling.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="95731-121">D3DUSAGE \_ QUERY \_ WRAPANDMIP</span><span class="sxs-lookup"><span data-stu-id="95731-121">D3DUSAGE\_QUERY\_WRAPANDMIP</span></span>                | <span data-ttu-id="95731-122">Fragen Sie die Ressource ab, um die Unterstützung für Texturumbruch und Mipzuordnung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="95731-122">Query the resource to verify support for texture wrapping and mip-mapping.</span></span>                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="95731-123">Verwenden Sie [**CheckDeviceFormat,**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) um die Hardwareunterstützung für diese Und einige andere Verwendungen abzufragen, die in [D3DUSAGE](d3dusage.md)aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="95731-123">Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) to query hardware support for these usages, and some other usages listed in [D3DUSAGE](d3dusage.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="95731-124">Konstanteninformationen</span><span class="sxs-lookup"><span data-stu-id="95731-124">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="95731-125">Header</span><span class="sxs-lookup"><span data-stu-id="95731-125">Header</span></span>                   | <span data-ttu-id="95731-126">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="95731-126">d3d9types.h</span></span> |
| <span data-ttu-id="95731-127">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="95731-127">Minimum operating system</span></span> | <span data-ttu-id="95731-128">Windows 98</span><span class="sxs-lookup"><span data-stu-id="95731-128">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="95731-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95731-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95731-130">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="95731-130">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
