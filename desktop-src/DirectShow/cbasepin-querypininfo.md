---
description: 'Die querypininfo-Methode ruft Informationen über die PIN ab. Diese Methode implementiert die IPin:: querypininfo-Methode.'
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: Cbasepin. querypininfo-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f69977a15deb7d84b3370bb6e08c02a4e5129212
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368540"
---
# <a name="cbasepinquerypininfo-method"></a><span data-ttu-id="369e5-104">Cbasepin. querypininfo-Methode</span><span class="sxs-lookup"><span data-stu-id="369e5-104">CBasePin.QueryPinInfo method</span></span>

<span data-ttu-id="369e5-105">Die- `QueryPinInfo` Methode ruft Informationen über die PIN ab.</span><span class="sxs-lookup"><span data-stu-id="369e5-105">The `QueryPinInfo` method retrieves information about the pin.</span></span> <span data-ttu-id="369e5-106">Diese Methode implementiert die [**IPin:: querypininfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) -Methode.</span><span class="sxs-lookup"><span data-stu-id="369e5-106">This method implements the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="369e5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="369e5-107">Syntax</span></span>


```C++
HRESULT QueryPinInfo(
   PIN_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="369e5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="369e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="369e5-109">*pinfo*</span><span class="sxs-lookup"><span data-stu-id="369e5-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="369e5-110">Zeiger auf eine [**Pin- \_ Info**](/windows/win32/api/strmif/ns-strmif-pin_info) -Struktur, die die PIN-Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="369e5-110">Pointer to a [**PIN\_INFO**](/windows/win32/api/strmif/ns-strmif-pin_info) structure that receives the pin information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="369e5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="369e5-111">Return value</span></span>

<span data-ttu-id="369e5-112">Gibt den S \_ OK-oder E- \_ Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="369e5-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="369e5-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="369e5-113">Remarks</span></span>

<span data-ttu-id="369e5-114">Diese Methode verwendet die [**cbasepin:: m \_ PName**](cbasepin-m-pname.md) -Member-Variable für den **achname** -Member der PIN \_ Info-Struktur.</span><span class="sxs-lookup"><span data-stu-id="369e5-114">This method uses the [**CBasePin::m\_pName**](cbasepin-m-pname.md) member variable for the **achName** member of the PIN\_INFO structure.</span></span>

<span data-ttu-id="369e5-115">Wenn die-Methode zurückgibt, hat der **pFilter** -Member der PIN \_ -Informationsstruktur einen ausstehenden Verweis Zähler, wenn er nicht **null** ist.</span><span class="sxs-lookup"><span data-stu-id="369e5-115">When the method returns, if the **pFilter** member of the PIN\_INFO structure is non-**NULL**, it has an outstanding reference count.</span></span> <span data-ttu-id="369e5-116">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben.</span><span class="sxs-lookup"><span data-stu-id="369e5-116">Be sure to release the interface when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="369e5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="369e5-117">Requirements</span></span>



| <span data-ttu-id="369e5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="369e5-118">Requirement</span></span> | <span data-ttu-id="369e5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="369e5-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="369e5-120">Header</span><span class="sxs-lookup"><span data-stu-id="369e5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="369e5-121"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="369e5-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="369e5-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="369e5-122">Library</span></span><br/> | <dl> <span data-ttu-id="369e5-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="369e5-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="369e5-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="369e5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="369e5-125">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="369e5-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




