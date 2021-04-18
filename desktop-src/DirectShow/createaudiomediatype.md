---
description: Die Funktion "deateaudiomediatype" Initialisiert einen Medientyp aus einer WaveFormatEx-Struktur.
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: Funktion "kreateaudiomediatype" (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateAudioMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef4e525762d4b6928e6a9095fad34f3f4f2e96fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354719"
---
# <a name="createaudiomediatype-function"></a><span data-ttu-id="9695b-103">Funktion "kreateaudiomediatype"</span><span class="sxs-lookup"><span data-stu-id="9695b-103">CreateAudioMediaType function</span></span>

<span data-ttu-id="9695b-104">Die Funktion " **deateaudiomediatype** " Initialisiert einen Medientyp aus einer [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9695b-104">The **CreateAudioMediaType** function initializes a media type from a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9695b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9695b-105">Syntax</span></span>


```C++
HRESULT STDAPI CreateAudioMediaType(
   const WAVEFORMATEX  *pwfx,
         AM_MEDIA_TYPE *pmt,
         BOOL          bSetFormat
);
```



## <a name="parameters"></a><span data-ttu-id="9695b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9695b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9695b-107">*pwfx*</span><span class="sxs-lookup"><span data-stu-id="9695b-107">*pwfx*</span></span> 
</dt> <dd>

<span data-ttu-id="9695b-108">Ein Zeiger auf die angegebene [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9695b-108">Pointer to the supplied [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9695b-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="9695b-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="9695b-110">Zeiger auf die zu initialisierende [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9695b-110">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to initialize.</span></span>

</dd> <dt>

<span data-ttu-id="9695b-111">*bsetformat*</span><span class="sxs-lookup"><span data-stu-id="9695b-111">*bSetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="9695b-112">Flag zum angeben, ob der Format Block initialisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9695b-112">Flag indicating whether to initialize the format block.</span></span> <span data-ttu-id="9695b-113">Geben Sie **true** an, um es zu initialisieren, oder andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="9695b-113">Specify **TRUE** to initialize it, or **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9695b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9695b-114">Return value</span></span>

<span data-ttu-id="9695b-115">Gibt "E \_ outof Memory" zurück, wenn der Arbeitsspeicher für die Formatierungsdaten nicht zugeordnet werden konnte. \_Andernfalls OK.</span><span class="sxs-lookup"><span data-stu-id="9695b-115">Returns E\_OUTOFMEMORY if memory could not be allocated for the format data; S\_OK otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9695b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9695b-116">Remarks</span></span>

<span data-ttu-id="9695b-117">Wenn der *bsetformat* -Parameter **true** ist, ordnet die Methode den Speicher für den Format Block zu.</span><span class="sxs-lookup"><span data-stu-id="9695b-117">If the *bSetFormat* parameter is **TRUE**, the method allocates the memory for the format block.</span></span> <span data-ttu-id="9695b-118">Wenn der *PMT* -Parameter bereits einen zugeordneten Format Block enthält, tritt ein Speicherplatz auf.</span><span class="sxs-lookup"><span data-stu-id="9695b-118">If the *pmt* parameter already contains an allocated format block, a memory leak will occur.</span></span> <span data-ttu-id="9695b-119">Um einen Speicherplatz zu vermeiden, rufen Sie " [**fremediatype**](freemediatype.md) " auf, bevor Sie diese Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9695b-119">To avoid a memory leak, call [**FreeMediaType**](freemediatype.md) before calling this function.</span></span> <span data-ttu-id="9695b-120">Nachdem die Methode zurückgegeben wurde, können Sie **freemediatype** erneut aufzurufen, um den Format Block freizugeben.</span><span class="sxs-lookup"><span data-stu-id="9695b-120">After the method returns, call **FreeMediaType** again to free the format block.</span></span>

## <a name="requirements"></a><span data-ttu-id="9695b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9695b-121">Requirements</span></span>



| <span data-ttu-id="9695b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9695b-122">Requirement</span></span> | <span data-ttu-id="9695b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9695b-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9695b-124">Header</span><span class="sxs-lookup"><span data-stu-id="9695b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9695b-125"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9695b-125"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="9695b-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9695b-126">Library</span></span><br/> | <dl> <span data-ttu-id="9695b-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9695b-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9695b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9695b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9695b-129">**Medientyp Funktionen**</span><span class="sxs-lookup"><span data-stu-id="9695b-129">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

