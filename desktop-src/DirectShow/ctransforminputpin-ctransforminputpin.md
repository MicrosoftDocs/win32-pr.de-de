---
description: CTransformInputPin.CTransformInputPin-Konstruktor – Konstruktormethode.
ms.assetid: 097dce19-b430-42d6-8914-68350c7eca40
title: CTransformInputPin.CTransformInputPin-Konstruktor (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e893b4e1c7d4f396644a468d3d71fa3046fb712
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095048"
---
# <a name="ctransforminputpinctransforminputpin-constructor"></a><span data-ttu-id="8daaa-103">CTransformInputPin.CTransformInputPin-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="8daaa-103">CTransformInputPin.CTransformInputPin constructor</span></span>

<span data-ttu-id="8daaa-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="8daaa-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8daaa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8daaa-105">Syntax</span></span>


```C++
CTransformInputPin(
   TCHAR            *pObjectName,
   CTransformFilter *pTransformFilter,
   HRESULT          *phr,
   LPCWSTR          pName
);
```



## <a name="parameters"></a><span data-ttu-id="8daaa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8daaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8daaa-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="8daaa-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="8daaa-108">Eine Zeichenfolge, die den Debugnamen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="8daaa-108">String containing the debug name of the object.</span></span> <span data-ttu-id="8daaa-109">Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="8daaa-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="8daaa-110">*pTransformFilter*</span><span class="sxs-lookup"><span data-stu-id="8daaa-110">*pTransformFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="8daaa-111">Zeiger auf den Filter, der diesen Pin erstellt hat, der ein [**CTransformFilter-Objekt sein**](ctransformfilter.md) muss.</span><span class="sxs-lookup"><span data-stu-id="8daaa-111">Pointer to the filter that created this pin, which must be a [**CTransformFilter**](ctransformfilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="8daaa-112">*Phr*</span><span class="sxs-lookup"><span data-stu-id="8daaa-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="8daaa-113">Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="8daaa-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="8daaa-114">Initialisieren Sie den Wert auf S \_ OK, bevor Sie das -Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="8daaa-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="8daaa-115">Der Wert wird nur geändert, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="8daaa-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="8daaa-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="8daaa-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="8daaa-117">Breitzeichenzeichenfolge, die den Pinnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="8daaa-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8daaa-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8daaa-118">Remarks</span></span>

<span data-ttu-id="8daaa-119">Der *pName-Parameter* gibt den Pinnamen an, der von der [**IPin::QueryPinInfo-Methode zurückgegeben**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) wird.</span><span class="sxs-lookup"><span data-stu-id="8daaa-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="8daaa-120">Die Zeichenfolge wird jedoch nicht für den Pinbezeichner verwendet.</span><span class="sxs-lookup"><span data-stu-id="8daaa-120">However, the string is not used for the pin identifier.</span></span> <span data-ttu-id="8daaa-121">Der Pinbezeichner für diese Klasse ist immer "In".</span><span class="sxs-lookup"><span data-stu-id="8daaa-121">The pin identifier for this class is always "In".</span></span> <span data-ttu-id="8daaa-122">Weitere Informationen finden Sie unter [**QueryId**](ctransforminputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="8daaa-122">For more information, see [**QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8daaa-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8daaa-123">Requirements</span></span>



| <span data-ttu-id="8daaa-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8daaa-124">Requirement</span></span> | <span data-ttu-id="8daaa-125">Wert</span><span class="sxs-lookup"><span data-stu-id="8daaa-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8daaa-126">Header</span><span class="sxs-lookup"><span data-stu-id="8daaa-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8daaa-127"><dt>Transfrm.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="8daaa-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8daaa-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8daaa-128">Library</span></span><br/> | <dl> <span data-ttu-id="8daaa-129"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8daaa-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




