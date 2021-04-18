---
description: Mit der get \_ avgtimeperframe-Methode wird die durchschnittliche Zeit pro Frame abgerufen.
ms.assetid: bcfdb241-9ec1-49f4-b2b5-0869c27da953
title: CBaseControlVideo.get_AvgTimePerFrame-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_AvgTimePerFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae69140348be6e2fdfc120ee7fb40096d663f720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368410"
---
# <a name="cbasecontrolvideoget_avgtimeperframe-method"></a><span data-ttu-id="215e9-103">Cbasecontrolvideo. get \_ avgtimeperframe-Methode</span><span class="sxs-lookup"><span data-stu-id="215e9-103">CBaseControlVideo.get\_AvgTimePerFrame method</span></span>

<span data-ttu-id="215e9-104">Die- `get_AvgTimePerFrame` Methode ruft die durchschnittliche Zeit pro Frame ab.</span><span class="sxs-lookup"><span data-stu-id="215e9-104">The `get_AvgTimePerFrame` method retrieves the average time per frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="215e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="215e9-105">Syntax</span></span>


```C++
HRESULT get_AvgTimePerFrame(
   REFTIME *pAvgTimePerFrame
);
```



## <a name="parameters"></a><span data-ttu-id="215e9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="215e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="215e9-107">*pavgtimeperframe*</span><span class="sxs-lookup"><span data-stu-id="215e9-107">*pAvgTimePerFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="215e9-108">Zeiger auf die durchschnittliche Zeit pro Frame.</span><span class="sxs-lookup"><span data-stu-id="215e9-108">Pointer to the average time per frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="215e9-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="215e9-109">Return value</span></span>

<span data-ttu-id="215e9-110">Wenn \_ nicht genügend Arbeitsspeicher verfügbar ist, wird noError zurückgegeben, wenn der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="215e9-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="215e9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="215e9-111">Remarks</span></span>

<span data-ttu-id="215e9-112">Diese Member-Funktion implementiert die [**ibasicvideo:: get \_ avgtimeperframe**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) -Methode.</span><span class="sxs-lookup"><span data-stu-id="215e9-112">This member function implements the [**IBasicVideo::get\_AvgTimePerFrame**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) method.</span></span> <span data-ttu-id="215e9-113">Er ruft die reine virtuelle [**cbasecontrolvideo:: getvideoformat**](cbasecontrolvideo-getvideoformat.md) -Member-Funktion auf, um die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur aus der abgeleiteten Klasse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="215e9-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) member function to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="215e9-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="215e9-114">Requirements</span></span>



| <span data-ttu-id="215e9-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="215e9-115">Requirement</span></span> | <span data-ttu-id="215e9-116">Wert</span><span class="sxs-lookup"><span data-stu-id="215e9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="215e9-117">Header</span><span class="sxs-lookup"><span data-stu-id="215e9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="215e9-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="215e9-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="215e9-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="215e9-119">Library</span></span><br/> | <dl> <span data-ttu-id="215e9-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="215e9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="215e9-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="215e9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="215e9-122">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="215e9-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




