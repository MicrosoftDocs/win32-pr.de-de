---
description: CTransInPlaceInputPin.CTransInPlaceInputPin-Konstruktor – Konstruktormethode.
ms.assetid: db0a3f78-ddb9-43b5-aab5-da2faaebb527
title: CTransInPlaceInputPin.CTransInPlaceInputPin-Konstruktor (Transip.h)
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
ms.openlocfilehash: 6f97c89142e43691c91b2a4c0d04721d9112ed49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084758"
---
# <a name="ctransinplaceinputpinctransinplaceinputpin-constructor"></a><span data-ttu-id="dab70-103">CTransInPlaceInputPin.CTransInPlaceInputPin-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="dab70-103">CTransInPlaceInputPin.CTransInPlaceInputPin constructor</span></span>

<span data-ttu-id="dab70-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="dab70-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dab70-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dab70-105">Syntax</span></span>


```C++
CTransInPlaceInputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a><span data-ttu-id="dab70-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dab70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dab70-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="dab70-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="dab70-108">Eine Zeichenfolge, die den Debugnamen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="dab70-108">String containing the debug name of the object.</span></span> <span data-ttu-id="dab70-109">Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="dab70-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="dab70-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="dab70-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="dab70-111">Zeiger auf den Filter, der diesen Pin erstellt hat, der ein [**CTransInPlaceFilter-Objekt sein**](ctransinplacefilter.md) muss.</span><span class="sxs-lookup"><span data-stu-id="dab70-111">Pointer to the filter that created this pin, which must be a [**CTransInPlaceFilter**](ctransinplacefilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="dab70-112">*Phr*</span><span class="sxs-lookup"><span data-stu-id="dab70-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="dab70-113">Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="dab70-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="dab70-114">Initialisieren Sie den Wert auf S \_ OK, bevor Sie das -Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="dab70-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="dab70-115">Der Wert wird nur geändert, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="dab70-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="dab70-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="dab70-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="dab70-117">Breitzeichenzeichenfolge, die den Pinnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="dab70-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dab70-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dab70-118">Remarks</span></span>

<span data-ttu-id="dab70-119">Der *pName-Parameter* gibt den Pinnamen an, der von der [**IPin::QueryPinInfo-Methode zurückgegeben**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) wird.</span><span class="sxs-lookup"><span data-stu-id="dab70-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="dab70-120">Diese Zeichenfolge wird jedoch nicht für den Pinbezeichner verwendet.</span><span class="sxs-lookup"><span data-stu-id="dab70-120">However, this string is not used for the pin identifier.</span></span> <span data-ttu-id="dab70-121">Der Pinbezeichner für diese Klasse ist immer In.</span><span class="sxs-lookup"><span data-stu-id="dab70-121">The pin identifier for this class is always In.</span></span> <span data-ttu-id="dab70-122">Weitere Informationen finden Sie unter [**CTransformInputPin::QueryId**](ctransforminputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="dab70-122">For more information, see [**CTransformInputPin::QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dab70-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dab70-123">Requirements</span></span>



| <span data-ttu-id="dab70-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dab70-124">Requirement</span></span> | <span data-ttu-id="dab70-125">Wert</span><span class="sxs-lookup"><span data-stu-id="dab70-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dab70-126">Header</span><span class="sxs-lookup"><span data-stu-id="dab70-126">Header</span></span><br/>  | <dl> <span data-ttu-id="dab70-127"><dt>Transip.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="dab70-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dab70-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dab70-128">Library</span></span><br/> | <dl> <span data-ttu-id="dab70-129"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="dab70-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dab70-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dab70-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dab70-131">**CTransInPlaceInputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="dab70-131">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




