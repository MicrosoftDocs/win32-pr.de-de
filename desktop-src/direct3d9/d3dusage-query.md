---
description: Diese Optionen identifizieren Abfrage Ressourcentypen.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f5dda7f84dfa36e4f3b7ece1b359a4841bbbf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126877"
---
# <a name="d3dusage_query"></a><span data-ttu-id="b7f73-103">D3DUSAGE- \_ Abfrage</span><span class="sxs-lookup"><span data-stu-id="b7f73-103">D3DUSAGE\_QUERY</span></span>

<span data-ttu-id="b7f73-104">Diese Optionen identifizieren Abfrage Ressourcentypen.</span><span class="sxs-lookup"><span data-stu-id="b7f73-104">These options identify query resource types.</span></span>



|                                            |                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f73-105">\#definieren</span><span class="sxs-lookup"><span data-stu-id="b7f73-105">\#define</span></span>                                   | <span data-ttu-id="b7f73-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b7f73-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="b7f73-107">D3DUSAGE- \_ Abfrage \_ Filter</span><span class="sxs-lookup"><span data-stu-id="b7f73-107">D3DUSAGE\_QUERY\_FILTER</span></span>                    | <span data-ttu-id="b7f73-108">Fragen Sie das Ressourcen Format ab, um festzustellen, ob es andere Textur Filtertypen als D3DTEXF Point unterstützt \_ (was immer unterstützt wird).</span><span class="sxs-lookup"><span data-stu-id="b7f73-108">Query the resource format to see if it supports texture filter types other than D3DTEXF\_POINT (which is always supported).</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="b7f73-109">D3DUSAGE \_ Query \_ legacybumpmap</span><span class="sxs-lookup"><span data-stu-id="b7f73-109">D3DUSAGE\_QUERY\_LEGACYBUMPMAP</span></span>             | <span data-ttu-id="b7f73-110">Abfragen der Ressource über eine Legacy-Bump-Karte.</span><span class="sxs-lookup"><span data-stu-id="b7f73-110">Query the resource about a legacy bump map.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="b7f73-111">D3DUSAGE \_ Query \_ postpixelshader- \_ BLENDING</span><span class="sxs-lookup"><span data-stu-id="b7f73-111">D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING</span></span> | <span data-ttu-id="b7f73-112">Fragen Sie die Ressource ab, um die Unterstützung für die Unterstützung für die Unterstützung von Post</span><span class="sxs-lookup"><span data-stu-id="b7f73-112">Query the resource to verify support for post pixel shader blending support.</span></span> <span data-ttu-id="b7f73-113">Wenn [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit D3DUSAGE \_ Query \_ postpixelshader- \_ Blending fehlschlägt, werden Post Pixel Mischungs Vorgänge nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7f73-113">If [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) fails with D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING, post pixel blending operations are not supported.</span></span> <span data-ttu-id="b7f73-114">Hierzu gehören Alpha Test, Pixel Nebel, Mischung aus Renderziel, Farb Schreib Aktivierung und Dithering.</span><span class="sxs-lookup"><span data-stu-id="b7f73-114">These include alpha test, pixel fog, render-target blending, color write enable, and dithering.</span></span> |
| <span data-ttu-id="b7f73-115">D3DUSAGE \_ Abfrage \_ srgbread</span><span class="sxs-lookup"><span data-stu-id="b7f73-115">D3DUSAGE\_QUERY\_SRGBREAD</span></span>                  | <span data-ttu-id="b7f73-116">Fragen Sie die Ressource ab, um zu überprüfen, ob eine Textur während eines Lesevorgangs Gammakorrektur unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7f73-116">Query the resource to verify if a texture supports gamma correction during a read operation.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="b7f73-117">D3DUSAGE \_ Abfrage \_ srgbwrite</span><span class="sxs-lookup"><span data-stu-id="b7f73-117">D3DUSAGE\_QUERY\_SRGBWRITE</span></span>                 | <span data-ttu-id="b7f73-118">Fragen Sie die Ressource ab, um zu überprüfen, ob eine Textur während eines Schreibvorgangs Gammakorrektur unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7f73-118">Query the resource to verify if a texture supports gamma correction during a write operation.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="b7f73-119">D3DUSAGE \_ Query \_ vertextexture</span><span class="sxs-lookup"><span data-stu-id="b7f73-119">D3DUSAGE\_QUERY\_VERTEXTEXTURE</span></span>             | <span data-ttu-id="b7f73-120">Fragen Sie die Ressource ab, um die Unterstützung für die Vertexshader-Textur Stichproben</span><span class="sxs-lookup"><span data-stu-id="b7f73-120">Query the resource to verify support for vertex shader texture sampling.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="b7f73-121">D3DUSAGE \_ Query \_ wrapandmip</span><span class="sxs-lookup"><span data-stu-id="b7f73-121">D3DUSAGE\_QUERY\_WRAPANDMIP</span></span>                | <span data-ttu-id="b7f73-122">Fragen Sie die Ressource ab, um Unterstützung für Textur Wrapping und MIP-Zuordnung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b7f73-122">Query the resource to verify support for texture wrapping and mip-mapping.</span></span>                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="b7f73-123">Verwenden Sie [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) , um die Hardwareunterstützung für diese Verwendungen und andere in [D3DUSAGE](d3dusage.md)aufgelistete Verwendungen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="b7f73-123">Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) to query hardware support for these usages, and some other usages listed in [D3DUSAGE](d3dusage.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="b7f73-124">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="b7f73-124">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="b7f73-125">Header</span><span class="sxs-lookup"><span data-stu-id="b7f73-125">Header</span></span>                   | <span data-ttu-id="b7f73-126">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="b7f73-126">d3d9types.h</span></span> |
| <span data-ttu-id="b7f73-127">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="b7f73-127">Minimum operating system</span></span> | <span data-ttu-id="b7f73-128">Windows 98</span><span class="sxs-lookup"><span data-stu-id="b7f73-128">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="b7f73-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b7f73-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7f73-130">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="b7f73-130">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
