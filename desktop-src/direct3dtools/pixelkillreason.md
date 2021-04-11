---
description: Eine-Aufzählung, mit der angegeben wird, warum ein Pixel abgelehnt wurde.
MS-HAID: vspixengine.PIXELKILLREASON
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Pixelkillreason-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 43836288-554B-430C-861D-AAC58DE3B282
api_name:
- PIXELKILLREASON
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f87b072eec1ac98ca68171593765567f5e77e70e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341819"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span data-ttu-id="1ff78-103"><span id="vspixengine.pixelkillreason"></span>Pixelkillreason-Enumeration</span><span class="sxs-lookup"><span data-stu-id="1ff78-103"><span id="vspixengine.pixelkillreason"></span>PIXELKILLREASON enumeration</span></span>

<span data-ttu-id="1ff78-104">Eine-Aufzählung, mit der angegeben wird, warum ein Pixel abgelehnt wurde.</span><span class="sxs-lookup"><span data-stu-id="1ff78-104">An enum used to indicate why a pixel was rejected.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff78-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ff78-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="1ff78-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="1ff78-106">Constants</span></span>

<span data-ttu-id="1ff78-107"><span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR \_ None**</span><span class="sxs-lookup"><span data-stu-id="1ff78-107"><span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR\_NONE**</span></span>  
<span data-ttu-id="1ff78-108">Ein Wert, der angibt, dass das Pixel nicht zurückgewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="1ff78-108">A value that indicates that the pixel was not rejected.</span></span>

<span data-ttu-id="1ff78-109"><span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR- \_ shaderkill**</span><span class="sxs-lookup"><span data-stu-id="1ff78-109"><span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR\_SHADERKILL**</span></span>  
<span data-ttu-id="1ff78-110">Ein Wert, der angibt, dass das Pixel zurückgewiesen wurde, weil der Shader nicht ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="1ff78-110">A value that indicates that the pixel was rejected because the shader didn't run.</span></span>

<span data-ttu-id="1ff78-111"><span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR \_ scissortest**</span><span class="sxs-lookup"><span data-stu-id="1ff78-111"><span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR\_SCISSORTEST**</span></span>  
<span data-ttu-id="1ff78-112">Ein Wert, der angibt, dass das Pixel zurückgewiesen wurde, weil der Scheren-Test fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="1ff78-112">A value that indicates that the pixel was rejected because the scissor test failed.</span></span>

<span data-ttu-id="1ff78-113"><span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR \_ Alpha Atest**</span><span class="sxs-lookup"><span data-stu-id="1ff78-113"><span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR\_ALPHATEST**</span></span>  
<span data-ttu-id="1ff78-114">Ein Wert, der angibt, dass das Pixel zurückgewiesen wurde, weil der Alpha Test fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="1ff78-114">A value that indicates that the pixel was rejected because the alpha test failed.</span></span>

<span data-ttu-id="1ff78-115"><span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR- \_ Schablonen Test**</span><span class="sxs-lookup"><span data-stu-id="1ff78-115"><span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR\_STENCILTEST**</span></span>  
<span data-ttu-id="1ff78-116">Ein Wert, der angibt, dass das Pixel zurückgewiesen wurde, weil der Schablonen Test fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="1ff78-116">A value that indicates that the pixel was rejected because the stencil test failed.</span></span>

<span data-ttu-id="1ff78-117"><span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR- \_ depthtest**</span><span class="sxs-lookup"><span data-stu-id="1ff78-117"><span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR\_DEPTHTEST**</span></span>  
<span data-ttu-id="1ff78-118">Ein Wert, der angibt, dass das Pixel zurückgewiesen wurde, weil der tiefen Test fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="1ff78-118">A value that indicates that the pixel was rejected because the depth test failed.</span></span>

<span data-ttu-id="1ff78-119"><span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR- \_ notkompatibilität**</span><span class="sxs-lookup"><span data-stu-id="1ff78-119"><span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR\_NOTCOMPUTABLE**</span></span>  
<span data-ttu-id="1ff78-120">Ein Wert, der angibt, dass der Pixel Verlauf nicht berechnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1ff78-120">A value that indicates that the pixel history can't be computed.</span></span>

<span data-ttu-id="1ff78-121"><span id="PKR_ERROR"></span><span id="pkr_error"></span>**PKR- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="1ff78-121"><span id="PKR_ERROR"></span><span id="pkr_error"></span>**PKR\_ERROR**</span></span>  
<span data-ttu-id="1ff78-122">Ein Wert, der angibt, dass das Pixel aufgrund eines allgemeinen Fehlers abgelehnt wurde.</span><span class="sxs-lookup"><span data-stu-id="1ff78-122">A value that indicates that the pixel was rejected because of a general error.</span></span>

<span data-ttu-id="1ff78-123"><span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR- \_ noschnittmenge**</span><span class="sxs-lookup"><span data-stu-id="1ff78-123"><span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR\_NOINTERSECTION**</span></span>  
<span data-ttu-id="1ff78-124">Ein Wert, der angibt, dass das Pixel zurückgewiesen wurde, weil der Draw-Befehl das Pixel nicht schneidet.</span><span class="sxs-lookup"><span data-stu-id="1ff78-124">A value that indicates that the pixel was rejected because the draw call does not intersect the pixel.</span></span>

<span data-ttu-id="1ff78-125"><span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR- \_ okkluded**</span><span class="sxs-lookup"><span data-stu-id="1ff78-125"><span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR\_OCCLUDED**</span></span>  
<span data-ttu-id="1ff78-126">Ein Wert, der angibt, dass das Pixel zurückgewiesen wurde, weil das Zeichnen geokelt wurde.</span><span class="sxs-lookup"><span data-stu-id="1ff78-126">A value that indicates that the pixel was rejected because the draw was occluded.</span></span>

<span data-ttu-id="1ff78-127"><span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR \_ depthstenciltest**</span><span class="sxs-lookup"><span data-stu-id="1ff78-127"><span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR\_DEPTHSTENCILTEST**</span></span>  
<span data-ttu-id="1ff78-128">Ein Wert, der angibt, dass das Pixel zurückgewiesen wurde, weil der tiefen-und Schablonen Test fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="1ff78-128">A value that indicates that the pixel was rejected because the depth and stencil test failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ff78-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ff78-129">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1ff78-130">Header</span><span class="sxs-lookup"><span data-stu-id="1ff78-130">Header</span></span></p></td><td><span data-ttu-id="1ff78-131">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1ff78-131">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



