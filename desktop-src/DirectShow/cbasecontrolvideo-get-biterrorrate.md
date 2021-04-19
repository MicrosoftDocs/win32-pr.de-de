---
description: Die get \_ biterrorrate-Methode ruft eine ungefähre Bitfehlerrate für das Video ab.
ms.assetid: 4078611c-6e09-47c8-8e1c-f33bc6ddca79
title: CBaseControlVideo.get_BitErrorRate-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitErrorRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ae15a882f6dcd8840519f9067223dde3e925f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356456"
---
# <a name="cbasecontrolvideoget_biterrorrate-method"></a><span data-ttu-id="f7cfc-103">Cbasecontrolvideo. get \_ biterrorrate-Methode</span><span class="sxs-lookup"><span data-stu-id="f7cfc-103">CBaseControlVideo.get\_BitErrorRate method</span></span>

<span data-ttu-id="f7cfc-104">Die- `get_BitErrorRate` Methode ruft eine ungefähre Bitfehlerrate für das Video ab.</span><span class="sxs-lookup"><span data-stu-id="f7cfc-104">The `get_BitErrorRate` method retrieves an approximate bit error rate for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7cfc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7cfc-105">Syntax</span></span>


```C++
HRESULT get_BitErrorRate(
   long *pBitErrorRate
);
```



## <a name="parameters"></a><span data-ttu-id="f7cfc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7cfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7cfc-107">*pbiterrorrate*</span><span class="sxs-lookup"><span data-stu-id="f7cfc-107">*pBitErrorRate*</span></span> 
</dt> <dd>

<span data-ttu-id="f7cfc-108">Zeiger auf die Bitfehlerrate (ein Fehler für ungefähr diese viele Bits).</span><span class="sxs-lookup"><span data-stu-id="f7cfc-108">Pointer to the bit error rate (one error for approximately this many bits).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7cfc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f7cfc-109">Return value</span></span>

<span data-ttu-id="f7cfc-110">Wenn \_ nicht genügend Arbeitsspeicher verfügbar ist, wird noError zurückgegeben, wenn der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="f7cfc-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7cfc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7cfc-111">Remarks</span></span>

<span data-ttu-id="f7cfc-112">Diese Member-Funktion implementiert die [**ibasicvideo:: get \_ biterrorrate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f7cfc-112">This member function implements the [**IBasicVideo::get\_BitErrorRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) method.</span></span> <span data-ttu-id="f7cfc-113">Sie ruft die rein virtuelle [**cbasecontrolvideo:: getvideoformat**](cbasecontrolvideo-getvideoformat.md) -Methode auf, um die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur aus der abgeleiteten Klasse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f7cfc-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) method to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7cfc-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7cfc-114">Requirements</span></span>



| <span data-ttu-id="f7cfc-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7cfc-115">Requirement</span></span> | <span data-ttu-id="f7cfc-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f7cfc-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7cfc-117">Header</span><span class="sxs-lookup"><span data-stu-id="f7cfc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f7cfc-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7cfc-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f7cfc-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f7cfc-119">Library</span></span><br/> | <dl> <span data-ttu-id="f7cfc-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f7cfc-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7cfc-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7cfc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7cfc-122">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f7cfc-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




