---
description: Die deletemediatype-Funktion löscht eine zugeordnete am- \_ \_ Medientyp Struktur, einschließlich des Format Blocks.
ms.assetid: 970f6b2b-2bf5-418d-b4ae-637561cd6765
title: Deletemediatype-Funktion (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db0de399ab1be7808370a6d0da57c4c3ca7b8de1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369467"
---
# <a name="deletemediatype-function"></a><span data-ttu-id="fe3e8-103">Deletemediatype-Funktion</span><span class="sxs-lookup"><span data-stu-id="fe3e8-103">DeleteMediaType function</span></span>

<span data-ttu-id="fe3e8-104">Die **deletemediatype** -Funktion löscht eine zugeordnete [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, einschließlich des Format Blocks.</span><span class="sxs-lookup"><span data-stu-id="fe3e8-104">The **DeleteMediaType** function deletes an allocated [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, including the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe3e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe3e8-105">Syntax</span></span>


```C++
void WINAPI DeleteMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="fe3e8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe3e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe3e8-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="fe3e8-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="fe3e8-108">Ein Zeiger auf eine [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur.</span><span class="sxs-lookup"><span data-stu-id="fe3e8-108">A pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe3e8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe3e8-109">Return value</span></span>

<span data-ttu-id="fe3e8-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fe3e8-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe3e8-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe3e8-111">Remarks</span></span>

<span data-ttu-id="fe3e8-112">Verwenden Sie diese Funktion, um eine beliebige Medientyp Struktur freizugeben, die entweder mithilfe von [**cotaskmemzugc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) oder mit dem Wert von " [**kreatemediatype**](createmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="fe3e8-112">Use this function to release any media type structure that was allocated using either [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) or [**CreateMediaType**](createmediatype.md).</span></span>

<span data-ttu-id="fe3e8-113">Diese Funktion ist in der [DirectShow-Basisklassen](directshow-base-classes.md) Bibliothek definiert.</span><span class="sxs-lookup"><span data-stu-id="fe3e8-113">This function is defined in the [DirectShow Base Classes](directshow-base-classes.md) library.</span></span> <span data-ttu-id="fe3e8-114">Wenn Sie keine Verknüpfung mit der Basisklassen Bibliothek herstellen möchten, können Sie den folgenden Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="fe3e8-114">If you prefer not to link to the base class library, you can use the following code:</span></span>


```C++
// Release the format block for a media type.

void _FreeMediaType(AM_MEDIA_TYPE& mt)
{
    if (mt.cbFormat != 0)
    {
        CoTaskMemFree((PVOID)mt.pbFormat);
        mt.cbFormat = 0;
        mt.pbFormat = NULL;
    }
    if (mt.pUnk != NULL)
    {
        // pUnk should not be used.
        mt.pUnk->Release();
        mt.pUnk = NULL;
    }
}


// Delete a media type structure that was allocated on the heap.
void _DeleteMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt != NULL)
    {
        _FreeMediaType(*pmt); 
        CoTaskMemFree(pmt);
    }
}
```





## <a name="requirements"></a><span data-ttu-id="fe3e8-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe3e8-115">Requirements</span></span>



| <span data-ttu-id="fe3e8-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe3e8-116">Requirement</span></span> | <span data-ttu-id="fe3e8-117">Wert</span><span class="sxs-lookup"><span data-stu-id="fe3e8-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3e8-118">Header</span><span class="sxs-lookup"><span data-stu-id="fe3e8-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fe3e8-119"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe3e8-119"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="fe3e8-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fe3e8-120">Library</span></span><br/> | <dl> <span data-ttu-id="fe3e8-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="fe3e8-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe3e8-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe3e8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe3e8-123">**Freimediatype**</span><span class="sxs-lookup"><span data-stu-id="fe3e8-123">**FreeMediaType**</span></span>](freemediatype.md)
</dt> <dt>

[<span data-ttu-id="fe3e8-124">**Medientyp Funktionen**</span><span class="sxs-lookup"><span data-stu-id="fe3e8-124">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

