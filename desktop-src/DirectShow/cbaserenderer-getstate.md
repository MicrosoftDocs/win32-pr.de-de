---
description: Mit der GetState-Methode wird der Zustand des Filters abgerufen (wird ausgeführt, beendet oder angehalten).
ms.assetid: 5d35824c-2509-499a-bbb1-1fb916b51808
title: Cbaserderderer. GetState-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 451078a6167ff7ca89ad4153c416826af8ac6d05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371013"
---
# <a name="cbaserenderergetstate-method"></a><span data-ttu-id="2004e-103">Cbaserderderer. GetState-Methode</span><span class="sxs-lookup"><span data-stu-id="2004e-103">CBaseRenderer.GetState method</span></span>

<span data-ttu-id="2004e-104">Mit der `GetState` -Methode wird der Zustand des Filters abgerufen (wird ausgeführt, beendet oder angehalten).</span><span class="sxs-lookup"><span data-stu-id="2004e-104">The `GetState` method retrieves the filters's state (running, stopped, or paused).</span></span>

## <a name="syntax"></a><span data-ttu-id="2004e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2004e-105">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="2004e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2004e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2004e-107">*dwmillisecstimeout*</span><span class="sxs-lookup"><span data-stu-id="2004e-107">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="2004e-108">Timeout Intervall in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="2004e-108">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="2004e-109">*State*</span><span class="sxs-lookup"><span data-stu-id="2004e-109">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="2004e-110">Ein Zeiger auf eine Variable, die einen Member des Enumerationstyps des [**Filter \_ Zustands**](/windows/win32/api/strmif/ne-strmif-filter_state) empfängt, der den Zustand des Filters angibt.</span><span class="sxs-lookup"><span data-stu-id="2004e-110">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the filter's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2004e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2004e-111">Return value</span></span>

<span data-ttu-id="2004e-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2004e-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="2004e-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2004e-113">Return code</span></span>                                                                                                | <span data-ttu-id="2004e-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2004e-114">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="2004e-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2004e-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="2004e-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="2004e-116">Success.</span></span><br/>                                            |
| <dl> <span data-ttu-id="2004e-117"><dt>**VFW \_ S \_ State \_ Intermediate**</dt></span><span class="sxs-lookup"><span data-stu-id="2004e-117"><dt>**VFW\_S\_STATE\_INTERMEDIATE**</dt></span></span> </dl> | <span data-ttu-id="2004e-118">Der Filter wechselt in den Status "angegeben".</span><span class="sxs-lookup"><span data-stu-id="2004e-118">The filter is transitioning to the indicated state.</span></span><br/> |
| <dl> <span data-ttu-id="2004e-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="2004e-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="2004e-120">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="2004e-120">**NULL** pointer argument.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="2004e-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2004e-121">Remarks</span></span>

<span data-ttu-id="2004e-122">Diese Methode überschreibt die [**cbasefilter:: GetState**](cbasefilter-getstate.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="2004e-122">This method overrides the [**CBaseFilter::GetState**](cbasefilter-getstate.md) method.</span></span> <span data-ttu-id="2004e-123">Wenn der Renderer angehalten wird, schließt er den Zustandsübergang erst ab, wenn er ein zum renderingmuster empfängt.</span><span class="sxs-lookup"><span data-stu-id="2004e-123">When the renderer is paused, it does not complete the state transition until it receives a sample to render.</span></span> <span data-ttu-id="2004e-124">Wenn das Timeout abläuft, bevor der Zustandsübergang beendet ist, gibt die Methode VFW \_ S \_ State Intermediate zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="2004e-124">If the time-out expires before the state transition is complete, the method returns VFW\_S\_STATE\_INTERMEDIATE.</span></span>

## <a name="requirements"></a><span data-ttu-id="2004e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2004e-125">Requirements</span></span>



| <span data-ttu-id="2004e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2004e-126">Requirement</span></span> | <span data-ttu-id="2004e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="2004e-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2004e-128">Header</span><span class="sxs-lookup"><span data-stu-id="2004e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="2004e-129"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2004e-129"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2004e-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2004e-130">Library</span></span><br/> | <dl> <span data-ttu-id="2004e-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2004e-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2004e-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2004e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2004e-133">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2004e-133">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




