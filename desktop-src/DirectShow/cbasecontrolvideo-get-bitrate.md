---
description: Die get \_ Bitrate-Methode ruft eine ungefähre Bitrate für das Video ab.
ms.assetid: e12e4677-a038-479f-8b64-937ad521c4be
title: CBaseControlVideo.get_BitRate-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f1feaed786b397801bbd17d2d2d41c0ccb813d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371094"
---
# <a name="cbasecontrolvideoget_bitrate-method"></a><span data-ttu-id="d5cc7-103">Cbasecontrolvideo. get- \_ Bitrate-Methode</span><span class="sxs-lookup"><span data-stu-id="d5cc7-103">CBaseControlVideo.get\_BitRate method</span></span>

<span data-ttu-id="d5cc7-104">Die- `get_BitRate` Methode ruft eine ungefähre Bitrate für das Video ab.</span><span class="sxs-lookup"><span data-stu-id="d5cc7-104">The `get_BitRate` method retrieves an approximate bit rate for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5cc7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5cc7-105">Syntax</span></span>


```C++
HRESULT get_BitRate(
   long *pBitRate
);
```



## <a name="parameters"></a><span data-ttu-id="d5cc7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5cc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5cc7-107">*pbitrate*</span><span class="sxs-lookup"><span data-stu-id="d5cc7-107">*pBitRate*</span></span> 
</dt> <dd>

<span data-ttu-id="d5cc7-108">Zeiger auf die Bitrate in Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="d5cc7-108">Pointer to the bit rate, in bits per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5cc7-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5cc7-109">Return value</span></span>

<span data-ttu-id="d5cc7-110">Wenn \_ nicht genügend Arbeitsspeicher verfügbar ist, wird noError zurückgegeben, wenn der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="d5cc7-110">Returns NOERROR if successful or E\_OUTOFMEMORY if not enough memory is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5cc7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5cc7-111">Remarks</span></span>

<span data-ttu-id="d5cc7-112">Diese Member-Funktion implementiert die [**ibasicvideo:: get \_ Bitrate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) -Methode.</span><span class="sxs-lookup"><span data-stu-id="d5cc7-112">This member function implements the [**IBasicVideo::get\_BitRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) method.</span></span> <span data-ttu-id="d5cc7-113">Er ruft den reinen virtuellen [**cbasecontrolvideo:: getvideoformat**](cbasecontrolvideo-getvideoformat.md) auf, um die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur aus der abgeleiteten Klasse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d5cc7-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5cc7-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5cc7-114">Requirements</span></span>



| <span data-ttu-id="d5cc7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5cc7-115">Requirement</span></span> | <span data-ttu-id="d5cc7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d5cc7-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5cc7-117">Header</span><span class="sxs-lookup"><span data-stu-id="d5cc7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d5cc7-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5cc7-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d5cc7-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d5cc7-119">Library</span></span><br/> | <dl> <span data-ttu-id="d5cc7-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d5cc7-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5cc7-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5cc7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5cc7-122">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d5cc7-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




