---
description: Erfahren Sie mehr über die cmediatype. cmediatype-Konstruktormethode (mtype. h). Diese Methode verwendet die Parameter "mtype" und "PHR".
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: 'Cmediatype. cmediatype-Konstruktor (mtype. h): mtype-Parameter und PHR-Parameter'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12ef9012e59dfce1f45d21aa720ae13bd660f2d8
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106373553"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a><span data-ttu-id="640b8-104">Cmediatype. cmediatype-Konstruktor (mtype. h): mtype-Parameter und PHR-Parameter</span><span class="sxs-lookup"><span data-stu-id="640b8-104">CMediaType.CMediaType constructor (Mtype.h) - mtype and phr parameters</span></span>

<span data-ttu-id="640b8-105">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="640b8-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="640b8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="640b8-106">Syntax</span></span>


```C++
CMediaType(
  [ref] const AM_MEDIA_TYPE &mtype,
              HRESULT       *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="640b8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="640b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="640b8-108">*mtype* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="640b8-108">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="640b8-109">Verweis auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="640b8-109">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="640b8-110">Der-Konstruktor kopiert den Medientyp in das neue-Objekt, einschließlich des-Format Blocks, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="640b8-110">The constructor copies the media type to the new object, including the format block, if any.</span></span>

</dd> <dt>

<span data-ttu-id="640b8-111">*PHR*</span><span class="sxs-lookup"><span data-stu-id="640b8-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="640b8-112">Ein Zeiger auf eine Variable, die einen HRESULT-Wert empfängt.</span><span class="sxs-lookup"><span data-stu-id="640b8-112">Pointer to a variable that receives an HRESULT value.</span></span> <span data-ttu-id="640b8-113">Dieser Parameter kann ein **null** -Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="640b8-113">This parameter can be a **NULL** pointer.</span></span> <span data-ttu-id="640b8-114">Andernfalls muss der Aufrufer den Wert vor dem \_ Aufrufen des Konstruktors auf S OK festlegen.</span><span class="sxs-lookup"><span data-stu-id="640b8-114">Otherwise, the caller must set the value to S\_OK before calling the constructor.</span></span> <span data-ttu-id="640b8-115">Wenn der Konstruktor fehlschlägt, wird der Wert auf einen Fehlercode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="640b8-115">If the constructor fails, it sets the value to a failure code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="640b8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="640b8-116">Remarks</span></span>

<span data-ttu-id="640b8-117">Der Konstruktor ruft die [**cmediatype:: initmediatype**](cmediatype-initmediatype.md) -Methode auf, um den Medientyp zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="640b8-117">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="640b8-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="640b8-118">Requirements</span></span>

| <span data-ttu-id="640b8-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="640b8-119">Requirement</span></span>                   | <span data-ttu-id="640b8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="640b8-120">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="640b8-121">Header</span><span class="sxs-lookup"><span data-stu-id="640b8-121">Header</span></span>  | <span data-ttu-id="640b8-122">Mtype. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="640b8-122">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="640b8-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="640b8-123">Library</span></span> | <span data-ttu-id="640b8-124">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="640b8-124">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="640b8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="640b8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="640b8-126">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="640b8-126">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




