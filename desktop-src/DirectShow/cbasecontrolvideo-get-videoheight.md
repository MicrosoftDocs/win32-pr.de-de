---
description: Die get \_ videoheight-Methode ruft die Höhe des nativen Videos ab.
ms.assetid: f33ba789-f9c6-47f1-879b-241bfdc72010
title: CBaseControlVideo.get_VideoHeight-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e738636cecd8031962ae31ebf54ac258d868013
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366051"
---
# <a name="cbasecontrolvideoget_videoheight-method"></a><span data-ttu-id="5da20-103">Cbasecontrolvideo. get \_ videoheight-Methode</span><span class="sxs-lookup"><span data-stu-id="5da20-103">CBaseControlVideo.get\_VideoHeight method</span></span>

<span data-ttu-id="5da20-104">Die- `get_VideoHeight` Methode ruft die Höhe des nativen Videos ab.</span><span class="sxs-lookup"><span data-stu-id="5da20-104">The `get_VideoHeight` method retrieves the height of the native video.</span></span>

## <a name="syntax"></a><span data-ttu-id="5da20-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5da20-105">Syntax</span></span>


```C++
HRESULT get_VideoHeight(
   long *pVideoHeight
);
```



## <a name="parameters"></a><span data-ttu-id="5da20-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5da20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5da20-107">*pvideoheight*</span><span class="sxs-lookup"><span data-stu-id="5da20-107">*pVideoHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="5da20-108">Zeiger auf die Höhe des nativen Videos in Pixel.</span><span class="sxs-lookup"><span data-stu-id="5da20-108">Pointer to the height of the native video, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5da20-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5da20-109">Return value</span></span>

<span data-ttu-id="5da20-110">Wenn \_ nicht genügend Arbeitsspeicher verfügbar ist, wird noError zurückgegeben, wenn der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="5da20-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="5da20-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5da20-111">Remarks</span></span>

<span data-ttu-id="5da20-112">Diese Member-Funktion implementiert die [**ibasicvideo:: get \_ videoheight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5da20-112">This member function implements the [**IBasicVideo::get\_VideoHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) method.</span></span> <span data-ttu-id="5da20-113">Er ruft den reinen virtuellen [**cbasecontrolvideo:: getvideoformat**](cbasecontrolvideo-getvideoformat.md) auf, um die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur aus der abgeleiteten Klasse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5da20-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="5da20-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5da20-114">Requirements</span></span>



| <span data-ttu-id="5da20-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5da20-115">Requirement</span></span> | <span data-ttu-id="5da20-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5da20-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5da20-117">Header</span><span class="sxs-lookup"><span data-stu-id="5da20-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5da20-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5da20-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5da20-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5da20-119">Library</span></span><br/> | <dl> <span data-ttu-id="5da20-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5da20-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5da20-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5da20-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5da20-122">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5da20-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




