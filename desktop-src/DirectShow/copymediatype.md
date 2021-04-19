---
description: Die copymediatype-Funktion kopiert eine am- \_ \_ Medientyp Struktur in eine andere Struktur, einschließlich des Format Blocks.
ms.assetid: 5b47e197-abb5-4b2c-ad65-a506c5e239be
title: Copymediatype-Funktion (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CopyMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e37f277244ae9b82c395d7901917e1fc1e78b35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361585"
---
# <a name="copymediatype-function"></a><span data-ttu-id="4dd22-103">Copymediatype-Funktion</span><span class="sxs-lookup"><span data-stu-id="4dd22-103">CopyMediaType function</span></span>

<span data-ttu-id="4dd22-104">Die **copymediatype** -Funktion kopiert eine [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur in eine andere Struktur, einschließlich des Format Blocks.</span><span class="sxs-lookup"><span data-stu-id="4dd22-104">The **CopyMediaType** function copies an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure into another structure, including the format block</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd22-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4dd22-105">Syntax</span></span>


```C++
HRESULT WINAPI CopyMediaType(
         AM_MEDIA_TYPE *pmtTarget,
   const AM_MEDIA_TYPE *pmtSource
);
```



## <a name="parameters"></a><span data-ttu-id="4dd22-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4dd22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dd22-107">*pmttarget*</span><span class="sxs-lookup"><span data-stu-id="4dd22-107">*pmtTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="4dd22-108">Zeiger auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur.</span><span class="sxs-lookup"><span data-stu-id="4dd22-108">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="4dd22-109">Die-Methode kopiert den Medientyp in diese-Struktur.</span><span class="sxs-lookup"><span data-stu-id="4dd22-109">The method copies the media type into this structure.</span></span>

</dd> <dt>

<span data-ttu-id="4dd22-110">*pmtsource*</span><span class="sxs-lookup"><span data-stu-id="4dd22-110">*pmtSource*</span></span> 
</dt> <dd>

<span data-ttu-id="4dd22-111">Zeiger auf eine zu Kopier Elle [**\_ \_ Quelltyp-Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur.</span><span class="sxs-lookup"><span data-stu-id="4dd22-111">Pointer to a source [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dd22-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4dd22-112">Return value</span></span>

<span data-ttu-id="4dd22-113">Gibt " \_ OK" oder "E \_ outo" zurück.</span><span class="sxs-lookup"><span data-stu-id="4dd22-113">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dd22-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4dd22-114">Remarks</span></span>

<span data-ttu-id="4dd22-115">Diese Funktion ordnet den Speicher für den Format Block zu.</span><span class="sxs-lookup"><span data-stu-id="4dd22-115">This function allocates the memory for the format block.</span></span> <span data-ttu-id="4dd22-116">Wenn der *pmttarget* -Parameter bereits einen zugeordneten Format Block enthält, tritt ein Speicherplatz auf.</span><span class="sxs-lookup"><span data-stu-id="4dd22-116">If the *pmtTarget* parameter already contains an allocated format block, a memory leak will occur.</span></span> <span data-ttu-id="4dd22-117">Um einen Speicherplatz zu vermeiden, rufen Sie " [**fremediatype**](freemediatype.md) " auf, bevor Sie diese Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4dd22-117">To avoid a memory leak, call [**FreeMediaType**](freemediatype.md) before calling this function.</span></span>

<span data-ttu-id="4dd22-118">Nachdem die Methode zurückgegeben wurde, können Sie [**freemediatype**](freemediatype.md) auf *pmttarget* aufzurufen, um den Format Block freizugeben.</span><span class="sxs-lookup"><span data-stu-id="4dd22-118">After the method returns, call [**FreeMediaType**](freemediatype.md) on *pmtTarget* to free the format block.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dd22-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4dd22-119">Requirements</span></span>



| <span data-ttu-id="4dd22-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4dd22-120">Requirement</span></span> | <span data-ttu-id="4dd22-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4dd22-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dd22-122">Header</span><span class="sxs-lookup"><span data-stu-id="4dd22-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4dd22-123"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4dd22-123"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="4dd22-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4dd22-124">Library</span></span><br/> | <dl> <span data-ttu-id="4dd22-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4dd22-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dd22-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4dd22-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dd22-127">**Medientyp Funktionen**</span><span class="sxs-lookup"><span data-stu-id="4dd22-127">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




