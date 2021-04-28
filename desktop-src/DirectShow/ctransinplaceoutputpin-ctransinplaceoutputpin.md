---
description: CTransInPlaceOutputPin.CTransInPlaceOutputPin-Konstruktor – Konstruktormethode.
ms.assetid: fe7b2d62-0e6a-4253-b469-6cede5dc9bb1
title: CTransInPlaceOutputPin.CTransInPlaceOutputPin-Konstruktor (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6b63ee3aa52bc0363bcab90275be4148659b3bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094708"
---
# <a name="ctransinplaceoutputpinctransinplaceoutputpin-constructor"></a><span data-ttu-id="7f699-103">CTransInPlaceOutputPin.CTransInPlaceOutputPin-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="7f699-103">CTransInPlaceOutputPin.CTransInPlaceOutputPin constructor</span></span>

<span data-ttu-id="7f699-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="7f699-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f699-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f699-105">Syntax</span></span>


```C++
CTransInPlaceOutputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a><span data-ttu-id="7f699-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f699-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f699-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="7f699-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="7f699-108">Zeichenfolge, die den Debugnamen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="7f699-108">String containing the debug name of the object.</span></span> <span data-ttu-id="7f699-109">Weitere Informationen finden Sie unter [**CBaseObject.**](cbaseobject.md)</span><span class="sxs-lookup"><span data-stu-id="7f699-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f699-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="7f699-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="7f699-111">Zeiger auf den Filter, der diesen Pin erstellt hat, der ein [**CTransInPlaceFilter-Objekt**](ctransinplacefilter.md) sein muss.</span><span class="sxs-lookup"><span data-stu-id="7f699-111">Pointer to the filter that created this pin, which must be a [**CTransInPlaceFilter**](ctransinplacefilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="7f699-112">*Phr*</span><span class="sxs-lookup"><span data-stu-id="7f699-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="7f699-113">Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="7f699-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="7f699-114">Initialisieren Sie den Wert vor dem Erstellen des -Objekts mit S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7f699-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="7f699-115">Der Wert wird nur geändert, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="7f699-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="7f699-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="7f699-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="7f699-117">Breitzeichenzeichenfolge, die den Pinnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="7f699-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f699-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f699-118">Remarks</span></span>

<span data-ttu-id="7f699-119">Der *pName-Parameter* gibt den Pinnamen an, der von der [**IPin::QueryPinInfo-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7f699-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="7f699-120">Die Zeichenfolge wird jedoch nicht für den Stecknadelbezeichner verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f699-120">However, the string is not used for the pin identifier.</span></span> <span data-ttu-id="7f699-121">Der Stecknadelbezeichner für diese Klasse ist immer "Out".</span><span class="sxs-lookup"><span data-stu-id="7f699-121">The pin identifier for this class is always "Out".</span></span> <span data-ttu-id="7f699-122">Weitere Informationen finden Sie unter [**QueryId**](ctransforminputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="7f699-122">For more information, see [**QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f699-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f699-123">Requirements</span></span>



| <span data-ttu-id="7f699-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f699-124">Requirement</span></span> | <span data-ttu-id="7f699-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7f699-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f699-126">Header</span><span class="sxs-lookup"><span data-stu-id="7f699-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7f699-127"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f699-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7f699-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7f699-128">Library</span></span><br/> | <dl> <span data-ttu-id="7f699-129"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7f699-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f699-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7f699-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f699-131">**CTransInPlaceOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7f699-131">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




