---
description: Die Funktion "anatemediatype" weist eine neue am- \_ \_ Medientyp Struktur, einschließlich des Format Blocks, zu.
ms.assetid: 841a8c51-6027-49d6-b3d8-b5e21e3d5f13
title: Funktion "deatemediatype" (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03ea3eaee03ebf98ac22d702bde9a165fda21e51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369195"
---
# <a name="createmediatype-function"></a><span data-ttu-id="ed82b-103">Funktion "kreatemediatype"</span><span class="sxs-lookup"><span data-stu-id="ed82b-103">CreateMediaType function</span></span>

<span data-ttu-id="ed82b-104">Die Funktion " **anatemediatype** " weist eine neue [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, einschließlich des Format Blocks, zu.</span><span class="sxs-lookup"><span data-stu-id="ed82b-104">The **CreateMediaType** function allocates a new [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, including the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed82b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed82b-105">Syntax</span></span>


```C++
AM_MEDIA_TYPE* WINAPI CreateMediaType(
   AM_MEDIA_TYPE const *pSrc
);
```



## <a name="parameters"></a><span data-ttu-id="ed82b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed82b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed82b-107">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="ed82b-107">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="ed82b-108">Zeiger auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur.</span><span class="sxs-lookup"><span data-stu-id="ed82b-108">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="ed82b-109">Die-Methode kopiert diese-Struktur in die neue-Struktur.</span><span class="sxs-lookup"><span data-stu-id="ed82b-109">The method copies this structure into the new structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed82b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed82b-110">Return value</span></span>

<span data-ttu-id="ed82b-111">Gibt eine neue [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur zurück, oder **null** , wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="ed82b-111">Returns a new [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, or **NULL** if there is an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed82b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed82b-112">Remarks</span></span>

<span data-ttu-id="ed82b-113">Um den von dieser Funktion belegten Arbeitsspeicher freizugeben, nennen Sie [**deletemediatype**](deletemediatype.md).</span><span class="sxs-lookup"><span data-stu-id="ed82b-113">To free the memory allocated by this function, call [**DeleteMediaType**](deletemediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed82b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed82b-114">Requirements</span></span>



| <span data-ttu-id="ed82b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed82b-115">Requirement</span></span> | <span data-ttu-id="ed82b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ed82b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed82b-117">Header</span><span class="sxs-lookup"><span data-stu-id="ed82b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ed82b-118"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed82b-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="ed82b-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ed82b-119">Library</span></span><br/> | <dl> <span data-ttu-id="ed82b-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ed82b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed82b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed82b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed82b-122">**Medientyp Funktionen**</span><span class="sxs-lookup"><span data-stu-id="ed82b-122">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




