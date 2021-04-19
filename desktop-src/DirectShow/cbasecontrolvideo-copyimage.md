---
description: Erstellt eine Speicher Kopie eines Bilds.
ms.assetid: 83a980bc-1298-439f-8dfc-49534591977f
title: Cbasecontrolvideo. CopyImage-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CopyImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23ada87e77d3c3441f489abed2e7af86a2a556ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370065"
---
# <a name="cbasecontrolvideocopyimage-method"></a><span data-ttu-id="3c9e3-103">Cbasecontrolvideo. CopyImage-Methode</span><span class="sxs-lookup"><span data-stu-id="3c9e3-103">CBaseControlVideo.CopyImage method</span></span>

<span data-ttu-id="3c9e3-104">Erstellt eine Speicher Kopie eines Bilds.</span><span class="sxs-lookup"><span data-stu-id="3c9e3-104">Creates a memory copy of an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c9e3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c9e3-105">Syntax</span></span>


```C++
HRESULT CopyImage(
   IMediaSample    *pMediaSample,
   VIDEOINFOHEADER *pVideoInfo,
   LONG            *pBufferSize,
   BYTE            *pVideoImage,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="3c9e3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c9e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c9e3-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="3c9e3-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="3c9e3-108">Zeiger auf das Beispiel, das das Videobild enthält.</span><span class="sxs-lookup"><span data-stu-id="3c9e3-108">Pointer to the sample containing the video image.</span></span>

</dd> <dt>

<span data-ttu-id="3c9e3-109">*pvideoinfo*</span><span class="sxs-lookup"><span data-stu-id="3c9e3-109">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="3c9e3-110">Zeiger auf das Format, das das Videobild darstellt.</span><span class="sxs-lookup"><span data-stu-id="3c9e3-110">Pointer to the format representing the video image.</span></span>

</dd> <dt>

<span data-ttu-id="3c9e3-111">*pbuffersize*</span><span class="sxs-lookup"><span data-stu-id="3c9e3-111">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="3c9e3-112">Ein Zeiger auf die Größe des Ausgabepuffers.</span><span class="sxs-lookup"><span data-stu-id="3c9e3-112">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3c9e3-113">*pvideoimage*</span><span class="sxs-lookup"><span data-stu-id="3c9e3-113">*pVideoImage*</span></span> 
</dt> <dd>

<span data-ttu-id="3c9e3-114">Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="3c9e3-114">Pointer to the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3c9e3-115">*psourcerect*</span><span class="sxs-lookup"><span data-stu-id="3c9e3-115">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="3c9e3-116">Zeiger auf das Quellvideo Rechteck.</span><span class="sxs-lookup"><span data-stu-id="3c9e3-116">Pointer to the source video rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c9e3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c9e3-117">Return value</span></span>

<span data-ttu-id="3c9e3-118">Wenn der *pvideoimage* -Parameter **null** ist, wird der *pbuffersize* -Parameter mit der Anzahl der Bytes aufgefüllt, die der Ausgabepuffer zum Speichern des Bilds benötigt.</span><span class="sxs-lookup"><span data-stu-id="3c9e3-118">If the *pVideoImage* parameter is **NULL**, the *pBufferSize* parameter is filled in with the number of bytes the output buffer requires to store the image.</span></span> <span data-ttu-id="3c9e3-119">Wenn der über gegebene Puffer zu klein ist oder die Member-Funktion nicht genügend Arbeitsspeicher zuweist, gibt die Member-Funktion E \_ outo fmemory zurück.</span><span class="sxs-lookup"><span data-stu-id="3c9e3-119">If the buffer passed in is too small or the member function fails to allocate sufficient memory, the member function returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c9e3-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c9e3-120">Remarks</span></span>

<span data-ttu-id="3c9e3-121">Die Member-Funktion Ruft das Bild aus dem Beispiel ab und kopiert es in den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="3c9e3-121">The member function retrieves the image from the sample and copies it into the output buffer.</span></span> <span data-ttu-id="3c9e3-122">Der Abschnitt des Videos, das in den Ausgabepuffer kopiert wird, spiegelt das Quell Rechteck wider, das über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle festgelegt wird (obwohl das Ziel Rechteck nicht widergespiegelt wird).</span><span class="sxs-lookup"><span data-stu-id="3c9e3-122">The section of video copied into the output buffer reflects the source rectangle that is set through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface (although it does not reflect the destination rectangle).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c9e3-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c9e3-123">Requirements</span></span>



| <span data-ttu-id="3c9e3-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c9e3-124">Requirement</span></span> | <span data-ttu-id="3c9e3-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3c9e3-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c9e3-126">Header</span><span class="sxs-lookup"><span data-stu-id="3c9e3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3c9e3-127"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c9e3-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3c9e3-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3c9e3-128">Library</span></span><br/> | <dl> <span data-ttu-id="3c9e3-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3c9e3-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c9e3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c9e3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c9e3-131">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3c9e3-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




