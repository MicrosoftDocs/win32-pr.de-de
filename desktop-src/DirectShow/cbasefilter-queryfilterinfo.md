---
description: 'Die queryfilterinfo-Methode ruft Informationen über den Filter ab. Diese Methode implementiert die ibasefilter:: queryfilterinfo-Methode.'
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: Cbasefilter. queryfilterinfo-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryFilterInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a706663c1fb39e0e2e84b4097ec620f9e608843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374021"
---
# <a name="cbasefilterqueryfilterinfo-method"></a><span data-ttu-id="56c20-104">Cbasefilter. queryfilterinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="56c20-104">CBaseFilter.QueryFilterInfo method</span></span>

<span data-ttu-id="56c20-105">Die- `QueryFilterInfo` Methode ruft Informationen über den Filter ab.</span><span class="sxs-lookup"><span data-stu-id="56c20-105">The `QueryFilterInfo` method retrieves information about the filter.</span></span> <span data-ttu-id="56c20-106">Diese Methode implementiert die [**ibasefilter:: queryfilterinfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) -Methode.</span><span class="sxs-lookup"><span data-stu-id="56c20-106">This method implements the [**IBaseFilter::QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="56c20-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="56c20-107">Syntax</span></span>


```C++
HRESULT QueryFilterInfo(
   FILTER_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="56c20-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="56c20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56c20-109">*pinfo*</span><span class="sxs-lookup"><span data-stu-id="56c20-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="56c20-110">Zeiger auf eine [**Filter \_ Informations**](/windows/win32/api/strmif/ns-strmif-filter_info) Struktur.</span><span class="sxs-lookup"><span data-stu-id="56c20-110">Pointer to a [**FILTER\_INFO**](/windows/win32/api/strmif/ns-strmif-filter_info) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56c20-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56c20-111">Return value</span></span>

<span data-ttu-id="56c20-112">Gibt den S \_ OK-oder E- \_ Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="56c20-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="56c20-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56c20-113">Remarks</span></span>

<span data-ttu-id="56c20-114">Diese Methode kopiert den Filternamen aus der [**cbasefilter:: m \_ PName**](cbasefilter-m-pname.md) -Element Variablen in den " **achname** "-Member der Filter \_ Informationsstruktur.</span><span class="sxs-lookup"><span data-stu-id="56c20-114">This method copies the filter's name from the [**CBaseFilter::m\_pName**](cbasefilter-m-pname.md) member variable into the **achName** member of the FILTER\_INFO structure.</span></span> <span data-ttu-id="56c20-115">Wenn **m \_ PName** **null** ist, legt die Methode " **achname** " auf L " \\ 0" fest.</span><span class="sxs-lookup"><span data-stu-id="56c20-115">If **m\_pName** is **NULL**, the method sets **achName** to L'\\0'.</span></span>

<span data-ttu-id="56c20-116">Die-Methode legt den **PGraph** -Member der Filter \_ Info-Struktur gleich der [**cbasefilter:: m \_ PGraph**](cbasefilter-m-pgraph.md) -Element Variablen fest und erhöht den Verweis Zähler.</span><span class="sxs-lookup"><span data-stu-id="56c20-116">The method sets the **pGraph** member of the FILTER\_INFO structure equal to the [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md) member variable, and increments the reference count.</span></span> <span data-ttu-id="56c20-117">Der Aufrufer muss die-Schnittstelle freigeben.</span><span class="sxs-lookup"><span data-stu-id="56c20-117">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="56c20-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56c20-118">Requirements</span></span>



| <span data-ttu-id="56c20-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56c20-119">Requirement</span></span> | <span data-ttu-id="56c20-120">Wert</span><span class="sxs-lookup"><span data-stu-id="56c20-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56c20-121">Header</span><span class="sxs-lookup"><span data-stu-id="56c20-121">Header</span></span><br/>  | <dl> <span data-ttu-id="56c20-122"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56c20-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="56c20-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="56c20-123">Library</span></span><br/> | <dl> <span data-ttu-id="56c20-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="56c20-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56c20-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56c20-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56c20-126">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="56c20-126">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




