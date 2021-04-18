---
description: 'Die GetClassID-Methode ruft den Klassen Bezeichner des Filters ab. Diese Methode implementiert die ipersistent:: GetClassID-Methode.'
ms.assetid: c3a8b6ab-b36f-493e-9436-6784e25e2511
title: Cbasefilter. GetClassID-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02dfe8452da6366454dcc1cfeeed93c379c89bd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351356"
---
# <a name="cbasefiltergetclassid-method"></a><span data-ttu-id="9d878-104">Cbasefilter. GetClassID-Methode</span><span class="sxs-lookup"><span data-stu-id="9d878-104">CBaseFilter.GetClassID method</span></span>

<span data-ttu-id="9d878-105">Die- `GetClassID` Methode ruft den Klassen Bezeichner des Filters ab.</span><span class="sxs-lookup"><span data-stu-id="9d878-105">The `GetClassID` method retrieves the class identifier of the filter.</span></span> <span data-ttu-id="9d878-106">Diese Methode implementiert die **ipersistent:: GetClassID-** Methode.</span><span class="sxs-lookup"><span data-stu-id="9d878-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d878-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d878-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="9d878-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d878-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d878-109">*pclsid*</span><span class="sxs-lookup"><span data-stu-id="9d878-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="9d878-110">Ein Zeiger auf eine Variable, die den Klassen Bezeichner empfängt.</span><span class="sxs-lookup"><span data-stu-id="9d878-110">Pointer to a variable that receives the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d878-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d878-111">Return value</span></span>

<span data-ttu-id="9d878-112">Gibt den S \_ OK-oder E- \_ Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="9d878-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d878-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d878-113">Requirements</span></span>



| <span data-ttu-id="9d878-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d878-114">Requirement</span></span> | <span data-ttu-id="9d878-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9d878-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d878-116">Header</span><span class="sxs-lookup"><span data-stu-id="9d878-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9d878-117"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d878-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9d878-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9d878-118">Library</span></span><br/> | <dl> <span data-ttu-id="9d878-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9d878-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d878-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d878-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d878-121">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9d878-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




