---
description: Konstruktormethode.
ms.assetid: db0a3f78-ddb9-43b5-aab5-da2faaebb527
title: Ctransinplaceinputpin. ctransinplaceinputpin-Konstruktor (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a801b2c4286f903ef450cac2fd76252f451f9add
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372301"
---
# <a name="ctransinplaceinputpinctransinplaceinputpin-constructor"></a><span data-ttu-id="8ee9e-103">Ctransinplaceinputpin. ctransinplaceinputpin-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="8ee9e-103">CTransInPlaceInputPin.CTransInPlaceInputPin constructor</span></span>

<span data-ttu-id="8ee9e-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="8ee9e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ee9e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ee9e-105">Syntax</span></span>


```C++
CTransInPlaceInputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a><span data-ttu-id="8ee9e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ee9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ee9e-107">*pobjectname*</span><span class="sxs-lookup"><span data-stu-id="8ee9e-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="8ee9e-108">Zeichenfolge, die den debugnamen des-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="8ee9e-108">String containing the debug name of the object.</span></span> <span data-ttu-id="8ee9e-109">Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="8ee9e-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ee9e-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="8ee9e-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="8ee9e-111">Ein Zeiger auf den Filter, der diese Pin erstellt hat, wobei es sich um ein [**ctransinplacefilter**](ctransinplacefilter.md) -Objekt handeln muss.</span><span class="sxs-lookup"><span data-stu-id="8ee9e-111">Pointer to the filter that created this pin, which must be a [**CTransInPlaceFilter**](ctransinplacefilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="8ee9e-112">*PHR*</span><span class="sxs-lookup"><span data-stu-id="8ee9e-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="8ee9e-113">Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="8ee9e-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="8ee9e-114">Initialisieren Sie den Wert \_ vor dem Erstellen des-Objekts auf S OK.</span><span class="sxs-lookup"><span data-stu-id="8ee9e-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="8ee9e-115">Der Wert wird nur geändert, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="8ee9e-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="8ee9e-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="8ee9e-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="8ee9e-117">Breit Zeichen-Zeichenfolge, die den Pin-Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="8ee9e-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ee9e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ee9e-118">Remarks</span></span>

<span data-ttu-id="8ee9e-119">Der *PName* -Parameter gibt den Pin-Namen an, der von der [**IPin:: querypininfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8ee9e-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="8ee9e-120">Diese Zeichenfolge wird jedoch nicht für den PIN-Bezeichner verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ee9e-120">However, this string is not used for the pin identifier.</span></span> <span data-ttu-id="8ee9e-121">Der PIN-Bezeichner für diese Klasse ist immer in.</span><span class="sxs-lookup"><span data-stu-id="8ee9e-121">The pin identifier for this class is always In.</span></span> <span data-ttu-id="8ee9e-122">Weitere Informationen finden Sie unter [**ctransforminputpin:: QueryId**](ctransforminputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="8ee9e-122">For more information, see [**CTransformInputPin::QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ee9e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ee9e-123">Requirements</span></span>



| <span data-ttu-id="8ee9e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ee9e-124">Requirement</span></span> | <span data-ttu-id="8ee9e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="8ee9e-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee9e-126">Header</span><span class="sxs-lookup"><span data-stu-id="8ee9e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8ee9e-127"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ee9e-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8ee9e-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8ee9e-128">Library</span></span><br/> | <dl> <span data-ttu-id="8ee9e-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8ee9e-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ee9e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ee9e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ee9e-131">**Ctransinplaceinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8ee9e-131">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




