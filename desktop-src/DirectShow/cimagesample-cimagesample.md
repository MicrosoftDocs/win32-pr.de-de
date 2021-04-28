---
description: 'CImageSample.CImageSample-Konstruktor: Konstruktormethode.'
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: CImageSample.CImageSample-Konstruktor (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecab52e347e03b698adccb79b77da879d26612b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095608"
---
# <a name="cimagesamplecimagesample-constructor"></a><span data-ttu-id="05c7e-103">CImageSample.CImageSample-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="05c7e-103">CImageSample.CImageSample constructor</span></span>

<span data-ttu-id="05c7e-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="05c7e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="05c7e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="05c7e-105">Syntax</span></span>


```C++
CImageSample(
   CBaseAllocator *pAllocator,
   TCHAR          *pName,
   HRESULT        *phr,
   LPBYTE         pBuffer,
   LONG           length
);
```



## <a name="parameters"></a><span data-ttu-id="05c7e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="05c7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05c7e-107">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="05c7e-107">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="05c7e-108">Zeiger auf die Zuweisung, die dieses Beispiel erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="05c7e-108">Pointer to the allocator that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="05c7e-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="05c7e-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="05c7e-110">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="05c7e-110">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="05c7e-111">*Phr*</span><span class="sxs-lookup"><span data-stu-id="05c7e-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="05c7e-112">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="05c7e-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="05c7e-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="05c7e-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="05c7e-114">Zeiger auf einen vom Aufrufer zugeordneten Speicherpuffer der *Größe*.</span><span class="sxs-lookup"><span data-stu-id="05c7e-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span> <span data-ttu-id="05c7e-115">Der Puffer sollte eine geräteunabhängige GDI-Bitmap (DIB) enthalten.</span><span class="sxs-lookup"><span data-stu-id="05c7e-115">The buffer should contain a GDI device-independent bitmap (DIB).</span></span>

</dd> <dt>

<span data-ttu-id="05c7e-116">*length*</span><span class="sxs-lookup"><span data-stu-id="05c7e-116">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="05c7e-117">Die Länge des Puffers.</span><span class="sxs-lookup"><span data-stu-id="05c7e-117">Length of the buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05c7e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05c7e-118">Remarks</span></span>

<span data-ttu-id="05c7e-119">Die [**CImageAllocator-Klasse**](cimageallocator.md) erstellt einen DIB mithilfe eines Dateizuordnungsobjekts, das von der Auslagerungsdatei des Betriebssystems erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="05c7e-119">The [**CImageAllocator**](cimageallocator.md) class creates a DIB using a file-mapping object that is backed by the operating-system paging file.</span></span> <span data-ttu-id="05c7e-120">Das Handle für das Dateizuordnungsobjekt wird im **hMapping-Member** der **m \_ DibData-Struktur** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="05c7e-120">The handle to the file-mapping object is stored in the **hMapping** member of the **m\_DibData** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="05c7e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05c7e-121">Requirements</span></span>



| <span data-ttu-id="05c7e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05c7e-122">Requirement</span></span> | <span data-ttu-id="05c7e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="05c7e-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05c7e-124">Header</span><span class="sxs-lookup"><span data-stu-id="05c7e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="05c7e-125"><dt>Winutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="05c7e-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="05c7e-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="05c7e-126">Library</span></span><br/> | <dl> <span data-ttu-id="05c7e-127"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="05c7e-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05c7e-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="05c7e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05c7e-129">**CImageSample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="05c7e-129">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




