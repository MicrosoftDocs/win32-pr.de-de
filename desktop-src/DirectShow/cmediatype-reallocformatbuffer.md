---
description: Die rezugecformatbuffer-Methode ordnet den Format Block neu einer neuen Größe zu.
ms.assetid: 49bec677-09cc-4e1a-994a-13e873e61713
title: Cmediatype. rezuzucformatbuffer-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.ReallocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22e861c61f01a7594d720833e2b3a4b923a1e183
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359261"
---
# <a name="cmediatypereallocformatbuffer-method"></a><span data-ttu-id="372dc-103">Cmediatype. rezuzucformatbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="372dc-103">CMediaType.ReallocFormatBuffer method</span></span>

<span data-ttu-id="372dc-104">Die- `ReallocFormatBuffer` Methode ordnet den Format Block neu einer neuen Größe zu.</span><span class="sxs-lookup"><span data-stu-id="372dc-104">The `ReallocFormatBuffer` method reallocates the format block to a new size.</span></span>

## <a name="syntax"></a><span data-ttu-id="372dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="372dc-105">Syntax</span></span>


```C++
BYTE* ReallocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="372dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="372dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="372dc-107">*length*</span><span class="sxs-lookup"><span data-stu-id="372dc-107">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="372dc-108">Die für den Format Block erforderliche neue Größe in Byte.</span><span class="sxs-lookup"><span data-stu-id="372dc-108">New size required for the format block, in bytes.</span></span> <span data-ttu-id="372dc-109">Muss größer sein als Null.</span><span class="sxs-lookup"><span data-stu-id="372dc-109">Must be greater than zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="372dc-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="372dc-110">Return value</span></span>

<span data-ttu-id="372dc-111">Gibt bei erfolgreicher Ausführung einen Zeiger auf den neuen Block zurück.</span><span class="sxs-lookup"><span data-stu-id="372dc-111">Returns a pointer to the new block if successful.</span></span> <span data-ttu-id="372dc-112">Andernfalls wird entweder ein Zeiger auf den alten Format Block oder **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="372dc-112">Otherwise, returns either a pointer to the old format block, or **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="372dc-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="372dc-113">Remarks</span></span>

<span data-ttu-id="372dc-114">Diese Methode weist einen neuen Format Block zu.</span><span class="sxs-lookup"><span data-stu-id="372dc-114">This method allocates a new format block.</span></span> <span data-ttu-id="372dc-115">Er kopiert so viel des vorhandenen Format Blocks wie möglich in den neuen Format Block.</span><span class="sxs-lookup"><span data-stu-id="372dc-115">It copies as much of the existing format block as possible into the new format block.</span></span> <span data-ttu-id="372dc-116">Wenn der neue-Block kleiner als der vorhandene-Block ist, wird der vorhandene Format Block abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="372dc-116">If the new block is smaller than the existing block, the existing format block is truncated.</span></span> <span data-ttu-id="372dc-117">Wenn der neue Block größer ist, ist der Inhalt des zusätzlichen Speicherplatzes nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="372dc-117">If the new block is larger, the contents of the additional space are undefined.</span></span> <span data-ttu-id="372dc-118">Sie sind nicht explizit auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="372dc-118">They are not explicitly set to zero.</span></span>

<span data-ttu-id="372dc-119">Die-Methode aktualisiert die Member **cbformat** und **pbformat** der **am \_ \_ Medientyp** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="372dc-119">The method updates the **cbFormat** and **pbFormat** members of the **AM\_MEDIA\_TYPE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="372dc-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="372dc-120">Requirements</span></span>



| <span data-ttu-id="372dc-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="372dc-121">Requirement</span></span> | <span data-ttu-id="372dc-122">Wert</span><span class="sxs-lookup"><span data-stu-id="372dc-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="372dc-123">Header</span><span class="sxs-lookup"><span data-stu-id="372dc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="372dc-124"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="372dc-124"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="372dc-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="372dc-125">Library</span></span><br/> | <dl> <span data-ttu-id="372dc-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="372dc-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="372dc-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="372dc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="372dc-128">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="372dc-128">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




