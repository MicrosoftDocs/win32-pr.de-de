---
description: 'Die Checkfunktionen-Methode fragt ab, ob der Stream Suchfunktionen angegeben hat. Diese Methode implementiert die imediaseeking:: Checkfunktionen-Methode.'
ms.assetid: 5d37e179-9e04-44e1-acbc-dfd2682830c0
title: Csourceseeking. Checkfunktionen-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f537973ac6c8f084ea42ba915a6293e581debef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358280"
---
# <a name="csourceseekingcheckcapabilities-method"></a><span data-ttu-id="9cae9-104">Csourceseeking. checksources-Methode</span><span class="sxs-lookup"><span data-stu-id="9cae9-104">CSourceSeeking.CheckCapabilities method</span></span>

<span data-ttu-id="9cae9-105">Die- `CheckCapabilities` Methode fragt ab, ob der Stream Suchfunktionen angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="9cae9-105">The `CheckCapabilities` method queries whether the stream has specified seeking capabilities.</span></span> <span data-ttu-id="9cae9-106">Diese Methode implementiert die [**imediaseeking:: Checkfunktionen**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9cae9-106">This method implements the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cae9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cae9-107">Syntax</span></span>


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="9cae9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cae9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cae9-109">*pfunktionen*</span><span class="sxs-lookup"><span data-stu-id="9cae9-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="9cae9-110">Zeiger auf eine bitweise Kombination von einem oder mehreren Suchfunktionen, die [**\_ \_ Such \_ Funktionen**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) suchen.</span><span class="sxs-lookup"><span data-stu-id="9cae9-110">Pointer to a bitwise combination of one or more [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cae9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9cae9-111">Return value</span></span>

<span data-ttu-id="9cae9-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="9cae9-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="9cae9-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9cae9-113">Return code</span></span>                                                                               | <span data-ttu-id="9cae9-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cae9-114">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9cae9-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9cae9-115"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="9cae9-116">Nicht alle Funktionen in *pfunktionen* sind vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9cae9-116">Not all of the capabilities in *pCapabilities* are present.</span></span><br/> |
| <dl> <span data-ttu-id="9cae9-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9cae9-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="9cae9-118">Alle Funktionen in *pfunktionen* sind vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9cae9-118">All capabilities in *pCapabilities* are present.</span></span><br/>            |
| <dl> <span data-ttu-id="9cae9-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="9cae9-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="9cae9-120">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="9cae9-120">**NULL** pointer argument.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="9cae9-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9cae9-121">Remarks</span></span>

<span data-ttu-id="9cae9-122">Diese Methode überprüft den Wert von *\* psources* anhand der Element Variablen [**csourceseeking:: m \_ dwseekingcaps**](csourceseeking-m-dwseekingcaps.md) , wie implementiert.</span><span class="sxs-lookup"><span data-stu-id="9cae9-122">As implemented, this method checks the value of *\*pCapabilities* against the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span> <span data-ttu-id="9cae9-123">*\* P-Funktionen* werden jedoch nicht gleich **m \_ dwseekingcaps** festgelegt, wie für die [**imediaseeking:: Checkfunktionen**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) -Methode beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9cae9-123">However, it does not set *\*pCapabilities* equal to **m\_dwSeekingCaps**, as described for the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span> <span data-ttu-id="9cae9-124">Auch wenn keine der angegebenen Funktionen verfügbar ist, gibt die Methode E Fail nicht zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="9cae9-124">Also, in the case where none of the specified capabilities are available, the method does not return E\_FAIL.</span></span> <span data-ttu-id="9cae9-125">Eine umfassendere Implementierung sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="9cae9-125">A more complete implementation would be as follows:</span></span>


```C++
STDMETHODIMP CheckCapabilities(DWORD *pCapabilities)
{
    CheckPointer(pCapabilities, E_POINTER)
;
    DWORD dwCaps;
    HRESULT hr = GetCapabilities(&dwCaps);
    if (SUCCEEDED(hr))
    {
        dwCaps &= *pCapabilities;
        if (dwCaps)
        {
            hr =  (dwCaps == *pCapabilities ? S_OK : S_FALSE );
        }
        else 
        {
            hr = E_FAIL;
        }
        *pCapabilities = dwCaps;
    }
    else 
    {
        *pCapabilities = 0;
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="9cae9-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cae9-126">Requirements</span></span>



| <span data-ttu-id="9cae9-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9cae9-127">Requirement</span></span> | <span data-ttu-id="9cae9-128">Wert</span><span class="sxs-lookup"><span data-stu-id="9cae9-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cae9-129">Header</span><span class="sxs-lookup"><span data-stu-id="9cae9-129">Header</span></span><br/>  | <dl> <span data-ttu-id="9cae9-130"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9cae9-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9cae9-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9cae9-131">Library</span></span><br/> | <dl> <span data-ttu-id="9cae9-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9cae9-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cae9-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cae9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cae9-134">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9cae9-134">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




