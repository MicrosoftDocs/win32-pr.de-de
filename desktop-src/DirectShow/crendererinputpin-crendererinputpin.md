---
description: Die crendererinputpin-Methode ist eine Konstruktormethode.
ms.assetid: 272f864e-d6a8-4a9e-b72f-892147db9970
title: Crendererinputpin. crendererinputpin-Konstruktor (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6888b234b87a48fc89f70c0db36122cbf7289ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372491"
---
# <a name="crendererinputpincrendererinputpin-constructor"></a><span data-ttu-id="d82b1-103">Crendererinputpin. crendererinputpin-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="d82b1-103">CRendererInputPin.CRendererInputPin constructor</span></span>

<span data-ttu-id="d82b1-104">Die- `CRendererInputPin` Methode ist eine Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="d82b1-104">The `CRendererInputPin` method is a constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d82b1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d82b1-105">Syntax</span></span>


```C++
CRendererInputPin(
   CBaseRenderer *pRenderer,
   HRESULT       *phr,
   LPCWSTR       Name
);
```



## <a name="parameters"></a><span data-ttu-id="d82b1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d82b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d82b1-107">*prenderer*</span><span class="sxs-lookup"><span data-stu-id="d82b1-107">*pRenderer*</span></span> 
</dt> <dd>

<span data-ttu-id="d82b1-108">Zeiger auf das [**cbaserenderer**](cbaserenderer.md) -Objekt, das den Filter implementiert.</span><span class="sxs-lookup"><span data-stu-id="d82b1-108">Pointer to the [**CBaseRenderer**](cbaserenderer.md) object that implements the filter.</span></span>

</dd> <dt>

<span data-ttu-id="d82b1-109">*PHR*</span><span class="sxs-lookup"><span data-stu-id="d82b1-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d82b1-110">Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt.</span><span class="sxs-lookup"><span data-stu-id="d82b1-110">Pointer to a variable that receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="d82b1-111">*Name*</span><span class="sxs-lookup"><span data-stu-id="d82b1-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="d82b1-112">Zeiger auf eine breit Zeichen-Zeichenfolge, die den PIN-Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="d82b1-112">Pointer to a wide-character string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d82b1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d82b1-113">Requirements</span></span>



| <span data-ttu-id="d82b1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d82b1-114">Requirement</span></span> | <span data-ttu-id="d82b1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d82b1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d82b1-116">Header</span><span class="sxs-lookup"><span data-stu-id="d82b1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d82b1-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d82b1-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d82b1-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d82b1-118">Library</span></span><br/> | <dl> <span data-ttu-id="d82b1-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d82b1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d82b1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d82b1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d82b1-121">**Crendererinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d82b1-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




