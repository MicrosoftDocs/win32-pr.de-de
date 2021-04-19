---
description: Konstruktormethode.
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: Cbasevideorenderer. cbasevideorenderer-Konstruktor (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.CBaseVideoRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27ed49be63d9c2c05e12a2ac92ae33f64705460b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370109"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a><span data-ttu-id="e4977-103">Cbasevideorenderer. cbasevideorenderer-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="e4977-103">CBaseVideoRenderer.CBaseVideoRenderer constructor</span></span>

<span data-ttu-id="e4977-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="e4977-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4977-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4977-105">Syntax</span></span>


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="e4977-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4977-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4977-107">*Renderclass*</span><span class="sxs-lookup"><span data-stu-id="e4977-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="e4977-108">Klassen Bezeichner für diesen Renderer.</span><span class="sxs-lookup"><span data-stu-id="e4977-108">Class identifier for this renderer.</span></span>

</dd> <dt>

<span data-ttu-id="e4977-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="e4977-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="e4977-110">Zeiger auf eine Beschreibung, die für Debugzwecke verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4977-110">Pointer to a description used for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="e4977-111">*Kro*</span><span class="sxs-lookup"><span data-stu-id="e4977-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="e4977-112">Zeiger auf das aggregierte Besitzer Objekt.</span><span class="sxs-lookup"><span data-stu-id="e4977-112">Pointer to the aggregated owner object.</span></span>

</dd> <dt>

<span data-ttu-id="e4977-113">*PHR*</span><span class="sxs-lookup"><span data-stu-id="e4977-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="e4977-114">Zeiger auf einen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="e4977-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4977-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4977-115">Requirements</span></span>



| <span data-ttu-id="e4977-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4977-116">Requirement</span></span> | <span data-ttu-id="e4977-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e4977-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4977-118">Header</span><span class="sxs-lookup"><span data-stu-id="e4977-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e4977-119"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4977-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e4977-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e4977-120">Library</span></span><br/> | <dl> <span data-ttu-id="e4977-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e4977-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4977-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4977-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4977-123">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e4977-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




