---
description: Die get \_ videowidth-Methode ruft die Breite des systemeigenen Videos ab.
ms.assetid: dfd897f0-f580-44c0-9445-ba61ae267187
title: CBaseControlVideo.get_VideoWidth-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: faeeed7ea8af58103e74d9b8c3690523c893282f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365850"
---
# <a name="cbasecontrolvideoget_videowidth-method"></a><span data-ttu-id="d754b-103">Cbasecontrolvideo. get \_ videowidth-Methode</span><span class="sxs-lookup"><span data-stu-id="d754b-103">CBaseControlVideo.get\_VideoWidth method</span></span>

<span data-ttu-id="d754b-104">Die- `get_VideoWidth` Methode ruft die Breite des systemeigenen Videos ab.</span><span class="sxs-lookup"><span data-stu-id="d754b-104">The `get_VideoWidth` method retrieves the width of the native video.</span></span>

## <a name="syntax"></a><span data-ttu-id="d754b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d754b-105">Syntax</span></span>


```C++
HRESULT get_VideoWidth(
   long *pVideoWidth
);
```



## <a name="parameters"></a><span data-ttu-id="d754b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d754b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d754b-107">*pvideowidth*</span><span class="sxs-lookup"><span data-stu-id="d754b-107">*pVideoWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="d754b-108">Zeiger auf die Breite des nativen Videos in Pixel.</span><span class="sxs-lookup"><span data-stu-id="d754b-108">Pointer to the width of the native video, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d754b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d754b-109">Return value</span></span>

<span data-ttu-id="d754b-110">Wenn \_ nicht genügend Arbeitsspeicher verfügbar ist, wird noError zurückgegeben, wenn der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="d754b-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="d754b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d754b-111">Remarks</span></span>

<span data-ttu-id="d754b-112">Diese Member-Funktion implementiert die [**ibasicvideo:: get \_ videowidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) -Methode.</span><span class="sxs-lookup"><span data-stu-id="d754b-112">This member function implements the [**IBasicVideo::get\_VideoWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) method.</span></span> <span data-ttu-id="d754b-113">Er ruft den reinen virtuellen [**cbasecontrolvideo:: getvideoformat**](cbasecontrolvideo-getvideoformat.md) auf, um die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur aus der abgeleiteten Klasse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d754b-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="d754b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d754b-114">Requirements</span></span>



| <span data-ttu-id="d754b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d754b-115">Requirement</span></span> | <span data-ttu-id="d754b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d754b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d754b-117">Header</span><span class="sxs-lookup"><span data-stu-id="d754b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d754b-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d754b-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d754b-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d754b-119">Library</span></span><br/> | <dl> <span data-ttu-id="d754b-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d754b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d754b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d754b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d754b-122">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d754b-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




