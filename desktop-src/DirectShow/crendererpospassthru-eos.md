---
description: Die EOS-Methode aktualisiert die zwischengespeicherten Zeitstempel nach einer Datenstrom Benachrichtigung.
ms.assetid: 7fb2f964-ec15-47f5-902b-29b9b121e876
title: Crendererpospassthru. EOS-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9e6990d946f32b441f0a33ceba8c0a59fdae488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358787"
---
# <a name="crendererpospassthrueos-method"></a><span data-ttu-id="34820-103">Crendererpospassthru. EOS-Methode</span><span class="sxs-lookup"><span data-stu-id="34820-103">CRendererPosPassThru.EOS method</span></span>

<span data-ttu-id="34820-104">Die- `EOS` Methode aktualisiert die zwischengespeicherten Zeitstempel nach einer Datenstrom Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="34820-104">The `EOS` method updates the cached time stamps after an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="34820-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34820-105">Syntax</span></span>


```C++
HRESULT EOS();
```



## <a name="parameters"></a><span data-ttu-id="34820-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="34820-106">Parameters</span></span>

<span data-ttu-id="34820-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="34820-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="34820-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34820-108">Return value</span></span>

<span data-ttu-id="34820-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="34820-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="34820-110">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="34820-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="34820-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="34820-111">Return code</span></span>                                                                            | <span data-ttu-id="34820-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34820-112">Description</span></span>                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="34820-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="34820-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="34820-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="34820-114">Success.</span></span><br/>                                       |
| <dl> <span data-ttu-id="34820-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="34820-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="34820-116">Fehler.</span><span class="sxs-lookup"><span data-stu-id="34820-116">Failure.</span></span> <span data-ttu-id="34820-117">Möglicherweise wird der Filter nicht gestreamt.</span><span class="sxs-lookup"><span data-stu-id="34820-117">Possibly the filter is not streaming.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="34820-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34820-118">Remarks</span></span>

<span data-ttu-id="34820-119">Der Filter sollte diese Methode beim Empfang einer Streamende Benachrichtigung ([**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)) abrufen.</span><span class="sxs-lookup"><span data-stu-id="34820-119">The filter should call this method when it receives an end-of-stream notification ([**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)).</span></span> <span data-ttu-id="34820-120">Die-Methode legt beide zwischengespeicherten Zeitstempel auf die Position des Stopps fest. Dadurch wird sichergestellt, dass die [**imediaseeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) -Methode die korrekten Werte am Ende des Streams zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="34820-120">The method sets both cached time stamps equal to the stop position, ensuring that the [**IMediaSeeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method returns the correct values at the end of the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="34820-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34820-121">Requirements</span></span>



| <span data-ttu-id="34820-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34820-122">Requirement</span></span> | <span data-ttu-id="34820-123">Wert</span><span class="sxs-lookup"><span data-stu-id="34820-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34820-124">Header</span><span class="sxs-lookup"><span data-stu-id="34820-124">Header</span></span><br/>  | <dl> <span data-ttu-id="34820-125"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34820-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="34820-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="34820-126">Library</span></span><br/> | <dl> <span data-ttu-id="34820-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="34820-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




