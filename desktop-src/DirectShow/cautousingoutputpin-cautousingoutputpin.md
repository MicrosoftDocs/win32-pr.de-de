---
description: Konstruktormethode. Der Konstruktor erhält Zugriff auf die angegebene PIN.
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: Cautousingoutputpin. cautousingoutputpin-Konstruktor (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin.CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94bafcdcb6e44a07afdccea382d783c20a9ad2ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370289"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a><span data-ttu-id="9b533-104">Cautousingoutputpin. cautousingoutputpin-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="9b533-104">CAutoUsingOutputPin.CAutoUsingOutputPin constructor</span></span>

<span data-ttu-id="9b533-105">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="9b533-105">Constructor method.</span></span> <span data-ttu-id="9b533-106">Der Konstruktor erhält Zugriff auf die angegebene PIN.</span><span class="sxs-lookup"><span data-stu-id="9b533-106">The constructor obtains access to the specified pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b533-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b533-107">Syntax</span></span>


```C++
CAutoUsingOutputPin(
   CDynamicOutputPin *pOutputPin,
   HRESULT           *phr
);
```



## <a name="parameters"></a><span data-ttu-id="9b533-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b533-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b533-109">*poutputpin*</span><span class="sxs-lookup"><span data-stu-id="9b533-109">*pOutputPin*</span></span> 
</dt> <dd>

<span data-ttu-id="9b533-110">Zeiger auf ein [**cdynamicoutputpin**](cdynamicoutputpin.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="9b533-110">Pointer to a [**CDynamicOutputPin**](cdynamicoutputpin.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="9b533-111">*PHR*</span><span class="sxs-lookup"><span data-stu-id="9b533-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="9b533-112">Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="9b533-112">Pointer to a variable that contains an **HRESULT** value.</span></span> <span data-ttu-id="9b533-113">Der Wert muss S \_ OK lauten.</span><span class="sxs-lookup"><span data-stu-id="9b533-113">The value must be S\_OK.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b533-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b533-114">Remarks</span></span>

<span data-ttu-id="9b533-115">Wenn die-Methode zurückgegeben wird, gibt der Wert von *\* PHR* den Erfolg oder Misserfolg der Methode an.</span><span class="sxs-lookup"><span data-stu-id="9b533-115">When the method returns, the value of *\*phr* indicates the success or failure of the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b533-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b533-116">Requirements</span></span>



| <span data-ttu-id="9b533-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b533-117">Requirement</span></span> | <span data-ttu-id="9b533-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9b533-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b533-119">Header</span><span class="sxs-lookup"><span data-stu-id="9b533-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9b533-120"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b533-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9b533-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9b533-121">Library</span></span><br/> | <dl> <span data-ttu-id="9b533-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9b533-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b533-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b533-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b533-124">**Cautousingoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9b533-124">**CAutoUsingOutputPin Class**</span></span>](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 




