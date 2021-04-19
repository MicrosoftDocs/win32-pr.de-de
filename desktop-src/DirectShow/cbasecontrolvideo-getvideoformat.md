---
description: Die getvideoformat-Methode ruft ein Video Beispiel ab, das das aktuelle Videoformat darstellt.
ms.assetid: f7457c5b-037c-4a63-963e-0fc6086609a4
title: Cbasecontrolvideo. getvideoformat-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d84b64818a02a60073fc21411e4a99bde07a6e00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370780"
---
# <a name="cbasecontrolvideogetvideoformat-method"></a><span data-ttu-id="9d168-103">Cbasecontrolvideo. getvideoformat-Methode</span><span class="sxs-lookup"><span data-stu-id="9d168-103">CBaseControlVideo.GetVideoFormat method</span></span>

<span data-ttu-id="9d168-104">Die- `GetVideoFormat` Methode ruft ein Video Beispiel ab, das das aktuelle Videoformat darstellt.</span><span class="sxs-lookup"><span data-stu-id="9d168-104">The `GetVideoFormat` method retrieves a video sample that represents the current video format.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d168-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d168-105">Syntax</span></span>


```C++
virtual VIDEOINFOHEADER* GetVideoFormat() = 0;
```



## <a name="parameters"></a><span data-ttu-id="9d168-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d168-106">Parameters</span></span>

<span data-ttu-id="9d168-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9d168-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9d168-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d168-108">Return value</span></span>

<span data-ttu-id="9d168-109">Gibt einen Zeiger auf eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur zurück, die das aktuelle Videoformat enthält.</span><span class="sxs-lookup"><span data-stu-id="9d168-109">Returns a pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure that contains the current video format.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d168-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d168-110">Remarks</span></span>

<span data-ttu-id="9d168-111">Um bestimmte Informationen über [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo)zurückzugeben und zu überprüfen, muss das Objekt das aktuelle Videoformat kennen.</span><span class="sxs-lookup"><span data-stu-id="9d168-111">To return and check certain information through [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), the object must know the current video format.</span></span> <span data-ttu-id="9d168-112">Diese Informationen werden abgerufen, indem diese reine virtuelle Methode aufgerufen wird, die von abgeleiteten Klassen überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="9d168-112">It gets this information by calling this pure virtual method that derived classes must override.</span></span> <span data-ttu-id="9d168-113">Diese Member-Funktion wird von den folgenden [**cbasecontrolvideo**](cbasecontrolvideo.md) -Element Funktionen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9d168-113">This member function is called by the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="9d168-114">**Cbasecontrolvideo:: onvideosizechange**</span><span class="sxs-lookup"><span data-stu-id="9d168-114">**CBaseControlVideo::OnVideoSizeChange**</span></span>](cbasecontrolvideo-onvideosizechange.md)
-   [<span data-ttu-id="9d168-115">**Cbasecontrolvideo:: \_ avgtimeperframe abrufen**</span><span class="sxs-lookup"><span data-stu-id="9d168-115">**CBaseControlVideo::get\_AvgTimePerFrame**</span></span>](cbasecontrolvideo-get-avgtimeperframe.md)
-   [<span data-ttu-id="9d168-116">**Cbasecontrolvideo:: get- \_ Bitrate**</span><span class="sxs-lookup"><span data-stu-id="9d168-116">**CBaseControlVideo::get\_BitRate**</span></span>](cbasecontrolvideo-get-bitrate.md)
-   [<span data-ttu-id="9d168-117">**Cbasecontrolvideo:: get \_ biterrorrate**</span><span class="sxs-lookup"><span data-stu-id="9d168-117">**CBaseControlVideo::get\_BitErrorRate**</span></span>](cbasecontrolvideo-get-biterrorrate.md)
-   [<span data-ttu-id="9d168-118">**Cbasecontrolvideo:: get \_ videowidth**</span><span class="sxs-lookup"><span data-stu-id="9d168-118">**CBaseControlVideo::get\_VideoWidth**</span></span>](cbasecontrolvideo-get-videowidth.md)
-   [<span data-ttu-id="9d168-119">**Cbasecontrolvideo:: get \_ videoheight**</span><span class="sxs-lookup"><span data-stu-id="9d168-119">**CBaseControlVideo::get\_VideoHeight**</span></span>](cbasecontrolvideo-get-videoheight.md)
-   [<span data-ttu-id="9d168-120">**Cbasecontrolvideo:: getvideopaletteentries**</span><span class="sxs-lookup"><span data-stu-id="9d168-120">**CBaseControlVideo::GetVideoPaletteEntries**</span></span>](cbasecontrolvideo-getvideopaletteentries.md)
-   [<span data-ttu-id="9d168-121">**Cbasecontrolvideo:: getvideosize**</span><span class="sxs-lookup"><span data-stu-id="9d168-121">**CBaseControlVideo::GetVideoSize**</span></span>](cbasecontrolvideo-getvideosize.md)

## <a name="requirements"></a><span data-ttu-id="9d168-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d168-122">Requirements</span></span>



| <span data-ttu-id="9d168-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d168-123">Requirement</span></span> | <span data-ttu-id="9d168-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9d168-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d168-125">Header</span><span class="sxs-lookup"><span data-stu-id="9d168-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9d168-126"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d168-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9d168-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9d168-127">Library</span></span><br/> | <dl> <span data-ttu-id="9d168-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9d168-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d168-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d168-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d168-130">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9d168-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




