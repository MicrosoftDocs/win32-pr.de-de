---
description: Konstruktormethode.
ms.assetid: 2340b39a-cab6-4524-b8cd-b22d4bdd24d0
title: Cmemzuordcator. cmemzucator-Konstruktor (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b650e23761c3fe5b3f5014666f90c679f088c4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358374"
---
# <a name="cmemallocatorcmemallocator-constructor"></a><span data-ttu-id="35d91-103">Cmemzuzucator. cmemzucator-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="35d91-103">CMemAllocator.CMemAllocator constructor</span></span>

<span data-ttu-id="35d91-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="35d91-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="35d91-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="35d91-105">Syntax</span></span>


```C++
CMemAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="35d91-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="35d91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35d91-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="35d91-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="35d91-108">Zeiger auf eine Zeichenfolge, die den Namen der Zuweisung enthält.</span><span class="sxs-lookup"><span data-stu-id="35d91-108">Pointer to a string containing the name of the allocator.</span></span>

</dd> <dt>

<span data-ttu-id="35d91-109">*Kro*</span><span class="sxs-lookup"><span data-stu-id="35d91-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="35d91-110">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="35d91-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="35d91-111">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="35d91-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="35d91-112">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="35d91-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="35d91-113">*PHR*</span><span class="sxs-lookup"><span data-stu-id="35d91-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="35d91-114">Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="35d91-114">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35d91-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35d91-115">Requirements</span></span>



| <span data-ttu-id="35d91-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35d91-116">Requirement</span></span> | <span data-ttu-id="35d91-117">Wert</span><span class="sxs-lookup"><span data-stu-id="35d91-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35d91-118">Header</span><span class="sxs-lookup"><span data-stu-id="35d91-118">Header</span></span><br/>  | <dl> <span data-ttu-id="35d91-119"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35d91-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="35d91-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="35d91-120">Library</span></span><br/> | <dl> <span data-ttu-id="35d91-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="35d91-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35d91-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35d91-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d91-123">**Cmemzuordcator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="35d91-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




