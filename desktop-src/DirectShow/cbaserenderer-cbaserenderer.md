---
description: Konstruktormethode.
ms.assetid: df5efbb3-6bce-4e30-b1b1-d69bf64fa87d
title: Cbaserenderer. cbaserenderer-Konstruktor (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b41f8d7f9681a64f58413aea2fd8717320278f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364764"
---
# <a name="cbaserenderercbaserenderer-constructor"></a><span data-ttu-id="25303-103">Cbaserenderer. cbaserenderer-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="25303-103">CBaseRenderer.CBaseRenderer constructor</span></span>

<span data-ttu-id="25303-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="25303-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="25303-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="25303-105">Syntax</span></span>


```C++
CBaseRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   UINT      TimerResolution = 1
);
```



## <a name="parameters"></a><span data-ttu-id="25303-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="25303-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25303-107">*Renderclass*</span><span class="sxs-lookup"><span data-stu-id="25303-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="25303-108">Klassen Bezeichner des Renderers.</span><span class="sxs-lookup"><span data-stu-id="25303-108">Class identifier of the renderer.</span></span>

</dd> <dt>

<span data-ttu-id="25303-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="25303-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="25303-110">Zeiger auf eine Zeichenfolge, die den Namen des Filters für Debugzwecke enthält.</span><span class="sxs-lookup"><span data-stu-id="25303-110">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="25303-111">*Kro*</span><span class="sxs-lookup"><span data-stu-id="25303-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="25303-112">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="25303-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="25303-113">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="25303-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="25303-114">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="25303-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="25303-115">*PHR*</span><span class="sxs-lookup"><span data-stu-id="25303-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="25303-116">Empfängt einen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="25303-116">Receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="25303-117">*TimerResolution*</span><span class="sxs-lookup"><span data-stu-id="25303-117">*TimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="25303-118">Zeit Geber Auflösung.</span><span class="sxs-lookup"><span data-stu-id="25303-118">Timer resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25303-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25303-119">Requirements</span></span>



| <span data-ttu-id="25303-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25303-120">Requirement</span></span> | <span data-ttu-id="25303-121">Wert</span><span class="sxs-lookup"><span data-stu-id="25303-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25303-122">Header</span><span class="sxs-lookup"><span data-stu-id="25303-122">Header</span></span><br/>  | <dl> <span data-ttu-id="25303-123"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25303-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="25303-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="25303-124">Library</span></span><br/> | <dl> <span data-ttu-id="25303-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="25303-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25303-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25303-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25303-127">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="25303-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




