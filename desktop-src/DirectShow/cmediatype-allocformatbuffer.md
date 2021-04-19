---
description: Die Methode "belegcformatbuffer" weist Speicher für den Format Block zu.
ms.assetid: 5ff716c7-f9cf-4b1c-9d3a-62ab955c1392
title: Cmediatype. zucformatbuffer-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.AllocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6a9314fd06734adcc367b7be34dc8d6d1b9d996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364028"
---
# <a name="cmediatypeallocformatbuffer-method"></a><span data-ttu-id="695ad-103">Cmediatype. zucformatbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="695ad-103">CMediaType.AllocFormatBuffer method</span></span>

<span data-ttu-id="695ad-104">Die- `AllocFormatBuffer` Methode ordnet Speicher für den Format Block zu.</span><span class="sxs-lookup"><span data-stu-id="695ad-104">The `AllocFormatBuffer` method allocates memory for the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="695ad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="695ad-105">Syntax</span></span>


```C++
BYTE* AllocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="695ad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="695ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="695ad-107">*length*</span><span class="sxs-lookup"><span data-stu-id="695ad-107">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="695ad-108">Die für den Format Block erforderliche Größe (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="695ad-108">Size required for the format block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="695ad-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="695ad-109">Return value</span></span>

<span data-ttu-id="695ad-110">Gibt bei erfolgreicher Ausführung einen Zeiger auf den neuen Block zurück.</span><span class="sxs-lookup"><span data-stu-id="695ad-110">Returns a pointer to the new block if successful.</span></span> <span data-ttu-id="695ad-111">Andernfalls wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="695ad-111">Otherwise, returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="695ad-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="695ad-112">Remarks</span></span>

<span data-ttu-id="695ad-113">Wenn die Methode erfolgreich einen neuen Format Block zugeordnet hat, gibt Sie den vorhandenen Format Block frei.</span><span class="sxs-lookup"><span data-stu-id="695ad-113">If the method successfully allocates a new format block, it frees the existing format block.</span></span> <span data-ttu-id="695ad-114">Wenn die Zuordnung fehlschlägt, verlässt die Methode den vorhandenen Format Block.</span><span class="sxs-lookup"><span data-stu-id="695ad-114">If the allocation fails, the method leaves the existing format block.</span></span>

<span data-ttu-id="695ad-115">Die-Methode aktualisiert die Member **cbformat** und **pbformat** der **am \_ \_ Medientyp** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="695ad-115">The method updates the **cbFormat** and **pbFormat** members of the **AM\_MEDIA\_TYPE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="695ad-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="695ad-116">Requirements</span></span>



| <span data-ttu-id="695ad-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="695ad-117">Requirement</span></span> | <span data-ttu-id="695ad-118">Wert</span><span class="sxs-lookup"><span data-stu-id="695ad-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="695ad-119">Header</span><span class="sxs-lookup"><span data-stu-id="695ad-119">Header</span></span><br/>  | <dl> <span data-ttu-id="695ad-120"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="695ad-120"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="695ad-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="695ad-121">Library</span></span><br/> | <dl> <span data-ttu-id="695ad-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="695ad-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="695ad-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="695ad-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="695ad-124">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="695ad-124">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




