---
description: Die Methode "Methode" gibt eine Zuweisung für die Verbindung an.
ms.assetid: 6b8e80f9-3b0d-498f-b1b0-bae491c25e81
title: Ctransinplaceoutputpin. log-Locator-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.SetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aacc2680bebcdd7de74f6f357380066a8fd37f1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370015"
---
# <a name="ctransinplaceoutputpinsetallocator-method"></a><span data-ttu-id="422ca-103">Ctransinplaceoutputpin. log-Locator-Methode</span><span class="sxs-lookup"><span data-stu-id="422ca-103">CTransInPlaceOutputPin.SetAllocator method</span></span>

<span data-ttu-id="422ca-104">Die- `SetAllocator` Methode gibt eine Zuweisung für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="422ca-104">The `SetAllocator` method specifies an allocator for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="422ca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="422ca-105">Syntax</span></span>


```C++
void SetAllocator(
   IMemAllocator *pAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="422ca-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="422ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="422ca-107">*pallocator*</span><span class="sxs-lookup"><span data-stu-id="422ca-107">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="422ca-108">Ein Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners.</span><span class="sxs-lookup"><span data-stu-id="422ca-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="422ca-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="422ca-109">Return value</span></span>

<span data-ttu-id="422ca-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="422ca-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="422ca-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="422ca-111">Remarks</span></span>

<span data-ttu-id="422ca-112">Die Ausgabe-PIN für diesen Filter stellt nie eine Zuweisung bereit.</span><span class="sxs-lookup"><span data-stu-id="422ca-112">The output pin for this filter never provides an allocator.</span></span> <span data-ttu-id="422ca-113">Diese Methode gibt die Zuweisung für die Ausgabepin an.</span><span class="sxs-lookup"><span data-stu-id="422ca-113">This method specifies the allocator for the output pin.</span></span> <span data-ttu-id="422ca-114">Er legt den Wert der [**cbaseoutputpin:: m \_ pallocator**](cbaseoutputpin-m-pallocator.md) -Member-Variable fest.</span><span class="sxs-lookup"><span data-stu-id="422ca-114">It sets the value of the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="422ca-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="422ca-115">Requirements</span></span>



| <span data-ttu-id="422ca-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="422ca-116">Requirement</span></span> | <span data-ttu-id="422ca-117">Wert</span><span class="sxs-lookup"><span data-stu-id="422ca-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="422ca-118">Header</span><span class="sxs-lookup"><span data-stu-id="422ca-118">Header</span></span><br/>  | <dl> <span data-ttu-id="422ca-119"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="422ca-119"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="422ca-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="422ca-120">Library</span></span><br/> | <dl> <span data-ttu-id="422ca-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="422ca-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="422ca-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="422ca-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="422ca-123">**Ctransinplaceoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="422ca-123">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




