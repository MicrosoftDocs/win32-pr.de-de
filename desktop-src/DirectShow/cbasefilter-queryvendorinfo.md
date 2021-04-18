---
description: 'Die queryvendorinfo-Methode ruft eine Zeichenfolge ab, die Hersteller Informationen enthält. Diese Methode implementiert die ibasefilter:: queryvendorinfo-Methode.'
ms.assetid: 083c0556-d516-4daf-8621-e158ea78b5a3
title: Cbasefilter. queryvendorinfo-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryVendorInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1786477c042bb1d9ecc6340056a771141d0a3c74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361061"
---
# <a name="cbasefilterqueryvendorinfo-method"></a><span data-ttu-id="03872-104">Cbasefilter. queryvendorinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="03872-104">CBaseFilter.QueryVendorInfo method</span></span>

<span data-ttu-id="03872-105">Die- `QueryVendorInfo` Methode ruft eine Zeichenfolge ab, die Hersteller Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="03872-105">The `QueryVendorInfo` method retrieves a string containing vendor information.</span></span> <span data-ttu-id="03872-106">Diese Methode implementiert die [**ibasefilter:: queryvendorinfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) -Methode.</span><span class="sxs-lookup"><span data-stu-id="03872-106">This method implements the [**IBaseFilter::QueryVendorInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="03872-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="03872-107">Syntax</span></span>


```C++
HRESULT QueryVendorInfo(
   LPWSTR *pVendorInfo
);
```



## <a name="parameters"></a><span data-ttu-id="03872-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="03872-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03872-109">*pvendorinfo*</span><span class="sxs-lookup"><span data-stu-id="03872-109">*pVendorInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="03872-110">Adresse einer Variablen, die einen Zeiger auf eine breit Zeichen-Zeichenfolge mit den Hersteller Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="03872-110">Address of a variable that receives a pointer to a wide-character string containing the vendor information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03872-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03872-111">Return value</span></span>

<span data-ttu-id="03872-112">Gibt "E \_ notimpl" zurück.</span><span class="sxs-lookup"><span data-stu-id="03872-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="03872-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03872-113">Remarks</span></span>

<span data-ttu-id="03872-114">Überschreiben Sie diese Methode, um Hersteller Informationen für einen Filter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="03872-114">To provide vendor information for a filter, override this method.</span></span> <span data-ttu-id="03872-115">Wenn Sie diese Methode implementieren, verwenden Sie die **CoTaskMemAlloc** -Funktion, um Arbeitsspeicher für die Zeichenfolge zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="03872-115">If you implement this method, use the **CoTaskMemAlloc** function to allocate memory for the string.</span></span> <span data-ttu-id="03872-116">Der Aufrufer ist für das Aufrufen der **CoTaskMemFree** -Funktion verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="03872-116">The caller is responsible for calling the **CoTaskMemFree** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="03872-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03872-117">Requirements</span></span>



| <span data-ttu-id="03872-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03872-118">Requirement</span></span> | <span data-ttu-id="03872-119">Wert</span><span class="sxs-lookup"><span data-stu-id="03872-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03872-120">Header</span><span class="sxs-lookup"><span data-stu-id="03872-120">Header</span></span><br/>  | <dl> <span data-ttu-id="03872-121"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03872-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="03872-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="03872-122">Library</span></span><br/> | <dl> <span data-ttu-id="03872-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="03872-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03872-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03872-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03872-125">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="03872-125">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




