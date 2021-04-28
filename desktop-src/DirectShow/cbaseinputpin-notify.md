---
description: 'CBaseInputPin.Notify-Methode: Die Notify-Methode benachrichtigt den Pin, dass eine Qualitätsänderung angefordert wird. Diese Methode implementiert die IQualityControl::Notify-Methode.'
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: CBaseInputPin.Notify-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 610888193762618d427a0329a27d3019bd625e69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119998"
---
# <a name="cbaseinputpinnotify-method"></a><span data-ttu-id="9a63b-104">CBaseInputPin.Notify-Methode</span><span class="sxs-lookup"><span data-stu-id="9a63b-104">CBaseInputPin.Notify method</span></span>

<span data-ttu-id="9a63b-105">Die `Notify` -Methode benachrichtigt den Pin, dass eine Qualitätsänderung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="9a63b-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="9a63b-106">Diese Methode implementiert die [**IQualityControl::Notify-Methode.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)</span><span class="sxs-lookup"><span data-stu-id="9a63b-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a63b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a63b-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="9a63b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a63b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a63b-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="9a63b-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="9a63b-110">Zeiger auf den Filter, der die Qualitätskontrollnachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="9a63b-110">Pointer to the filter that is sending the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="9a63b-111">*Q*</span><span class="sxs-lookup"><span data-stu-id="9a63b-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="9a63b-112">[**Qualitätsstruktur,**](/windows/win32/api/strmif/ns-strmif-quality) die die Qualitätskontrollmeldung enthält.</span><span class="sxs-lookup"><span data-stu-id="9a63b-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a63b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a63b-113">Return value</span></span>

<span data-ttu-id="9a63b-114">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="9a63b-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a63b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a63b-115">Remarks</span></span>

<span data-ttu-id="9a63b-116">Filter übergeben in der Regel Qualitätskontrollmeldungen an einen Upstreamausgabepin, nicht an einen Eingabepin.</span><span class="sxs-lookup"><span data-stu-id="9a63b-116">Filters usually pass quality-control messages to an upstream output pin, not to an input pin.</span></span> <span data-ttu-id="9a63b-117">Daher gibt diese Methode S \_ OK zurück, ohne etwas zu tun.</span><span class="sxs-lookup"><span data-stu-id="9a63b-117">Therefore, this method returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a63b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a63b-118">Requirements</span></span>



| <span data-ttu-id="9a63b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a63b-119">Requirement</span></span> | <span data-ttu-id="9a63b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9a63b-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a63b-121">Header</span><span class="sxs-lookup"><span data-stu-id="9a63b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9a63b-122"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="9a63b-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9a63b-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9a63b-123">Library</span></span><br/> | <dl> <span data-ttu-id="9a63b-124"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9a63b-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a63b-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9a63b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a63b-126">**CBaseInputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9a63b-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="9a63b-127">Qualitätskontrollverwaltung</span><span class="sxs-lookup"><span data-stu-id="9a63b-127">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 




