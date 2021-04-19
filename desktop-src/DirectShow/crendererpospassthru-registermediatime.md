---
description: Mit der registermediatime-Methode werden die Zeitstempel aus dem aktuellen Beispiel zwischengespeichert.
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: Crendererpospassthru. registermediatime-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c829690572d55ea700d51124b99370f23e755a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369659"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a><span data-ttu-id="b6bd6-103">Crendererpospassthru. registermediatime-Methode (ctlutil. h)</span><span class="sxs-lookup"><span data-stu-id="b6bd6-103">CRendererPosPassThru.RegisterMediaTime method (Ctlutil.h)</span></span>

<span data-ttu-id="b6bd6-104">Mit der **registermediatime** -Methode werden die Zeitstempel aus dem aktuellen Beispiel zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="b6bd6-104">The **RegisterMediaTime** method caches the time stamps from the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6bd6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6bd6-105">Syntax</span></span>


```C++
HRESULT RegisterMediaTime(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="b6bd6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6bd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6bd6-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="b6bd6-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="b6bd6-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="b6bd6-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6bd6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6bd6-109">Return value</span></span>

<span data-ttu-id="b6bd6-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b6bd6-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b6bd6-111">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="b6bd6-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="b6bd6-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b6bd6-112">Return code</span></span>                                                                                                  | <span data-ttu-id="b6bd6-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6bd6-113">Description</span></span>                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="b6bd6-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b6bd6-114"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="b6bd6-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="b6bd6-115">Success.</span></span><br/>                        |
| <dl> <span data-ttu-id="b6bd6-116"><dt>**VFW \_ E \_ Medien \_ Zeit \_ nicht \_ festgelegt**</dt></span><span class="sxs-lookup"><span data-stu-id="b6bd6-116"><dt>**VFW\_E\_MEDIA\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="b6bd6-117">Das Beispiel ist nicht mit einem Zeitstempel versehen.</span><span class="sxs-lookup"><span data-stu-id="b6bd6-117">The sample is not time-stamped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b6bd6-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6bd6-118">Remarks</span></span>

<span data-ttu-id="b6bd6-119">Diese Methode speichert die Zeitstempel aus dem aktuellen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="b6bd6-119">This method stores the time stamps from the current sample.</span></span> <span data-ttu-id="b6bd6-120">Die [**crendererpospassthru:: getmediatime**](crendererpospassthru-getmediatime.md) -Methode ruft die gleichen Werte ab.</span><span class="sxs-lookup"><span data-stu-id="b6bd6-120">The [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method retrieves the same values.</span></span>

<span data-ttu-id="b6bd6-121">Der Filter sollte diese Methode für jedes empfangene Beispiel aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b6bd6-121">The filter should call this method for each sample that it receives.</span></span> <span data-ttu-id="b6bd6-122">Die-Methode ist überladen, um entweder einen Zeiger auf das Beispiel oder den Zeitstempelwert selbst zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="b6bd6-122">The method is overloaded to accept either a pointer to the sample, or the time stamp values themselves.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6bd6-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6bd6-123">Requirements</span></span>



| <span data-ttu-id="b6bd6-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6bd6-124">Requirement</span></span> | <span data-ttu-id="b6bd6-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b6bd6-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6bd6-126">Header</span><span class="sxs-lookup"><span data-stu-id="b6bd6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b6bd6-127"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6bd6-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b6bd6-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b6bd6-128">Library</span></span><br/> | <dl> <span data-ttu-id="b6bd6-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b6bd6-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




