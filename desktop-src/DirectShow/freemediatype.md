---
description: Die Funktion "fremediatype" löscht den Format Block in \_ einer \_ Medientyp-Struktur.
ms.assetid: b7ec335e-518d-4aa6-8cde-8cb92184d0b0
title: Fremediatype-Funktion (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f332ccc9a60473a9d814481b759221dc6468d5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365586"
---
# <a name="freemediatype-function"></a><span data-ttu-id="d4a45-103">Fremediatype-Funktion</span><span class="sxs-lookup"><span data-stu-id="d4a45-103">FreeMediaType function</span></span>

<span data-ttu-id="d4a45-104">Die Funktion " **fremediatype** " löscht den Format Block in einer [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d4a45-104">The **FreeMediaType** function deletes the format block in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4a45-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4a45-105">Syntax</span></span>


```C++
void FreeMediaType(
   AM_MEDIA_TYPE &mt
);
```



## <a name="parameters"></a><span data-ttu-id="d4a45-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4a45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4a45-107">*MT* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="d4a45-107">*mt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d4a45-108">Ein Verweis auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d4a45-108">A reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4a45-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4a45-109">Return value</span></span>

<span data-ttu-id="d4a45-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d4a45-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4a45-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4a45-111">Remarks</span></span>

<span data-ttu-id="d4a45-112">Der Format Block wird dem Heap zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d4a45-112">The format block is allocated on the heap.</span></span> <span data-ttu-id="d4a45-113">Der **pbformat** -Member des [**am- \_ Medien \_ Typs**](/windows/win32/api/strmif/ns-strmif-am_media_type) verweist auf den Format Block.</span><span class="sxs-lookup"><span data-stu-id="d4a45-113">The **pbFormat** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) points to the format block.</span></span> <span data-ttu-id="d4a45-114">Verwenden Sie diese Funktion, um nur den Format Block freizugeben.</span><span class="sxs-lookup"><span data-stu-id="d4a45-114">Use this function to free just the format block.</span></span> <span data-ttu-id="d4a45-115">Um eine zugeordnete **\_ \_ Medientyp** Struktur zu löschen, nennen Sie [**deletemediatype**](deletemediatype.md).</span><span class="sxs-lookup"><span data-stu-id="d4a45-115">To delete an allocated **AM\_MEDIA\_TYPE** structure, call [**DeleteMediaType**](deletemediatype.md).</span></span>

<span data-ttu-id="d4a45-116">Diese Funktion ist in der [DirectShow-Basisklassen](directshow-base-classes.md) Bibliothek definiert.</span><span class="sxs-lookup"><span data-stu-id="d4a45-116">This function is defined in the [DirectShow Base Classes](directshow-base-classes.md) library.</span></span> <span data-ttu-id="d4a45-117">Wenn Sie keine Verknüpfung mit der Basisklassen Bibliothek herstellen möchten, können Sie den folgenden Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="d4a45-117">If you prefer not to link to the base class library, you can use the following code:</span></span>


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
```



## <a name="requirements"></a><span data-ttu-id="d4a45-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4a45-118">Requirements</span></span>



| <span data-ttu-id="d4a45-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4a45-119">Requirement</span></span> | <span data-ttu-id="d4a45-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d4a45-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a45-121">Header</span><span class="sxs-lookup"><span data-stu-id="d4a45-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d4a45-122"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4a45-122"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="d4a45-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d4a45-123">Library</span></span><br/> | <dl> <span data-ttu-id="d4a45-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d4a45-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4a45-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4a45-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4a45-126">**Deletemediatype**</span><span class="sxs-lookup"><span data-stu-id="d4a45-126">**DeleteMediaType**</span></span>](deletemediatype.md)
</dt> <dt>

[<span data-ttu-id="d4a45-127">**Medientyp Funktionen**</span><span class="sxs-lookup"><span data-stu-id="d4a45-127">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




