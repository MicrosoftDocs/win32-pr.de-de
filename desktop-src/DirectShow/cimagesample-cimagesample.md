---
description: Konstruktormethode.
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: Cimagesample. cimagesample-Konstruktor (winutil. h)
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
ms.openlocfilehash: 805be59cfc899b6461fa8c761eebb5821118640f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350786"
---
# <a name="cimagesamplecimagesample-constructor"></a><span data-ttu-id="1ab60-103">Cimagesample. cimagesample-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="1ab60-103">CImageSample.CImageSample constructor</span></span>

<span data-ttu-id="1ab60-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="1ab60-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ab60-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ab60-105">Syntax</span></span>


```C++
CImageSample(
   CBaseAllocator *pAllocator,
   TCHAR          *pName,
   HRESULT        *phr,
   LPBYTE         pBuffer,
   LONG           length
);
```



## <a name="parameters"></a><span data-ttu-id="1ab60-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ab60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ab60-107">*pallocator*</span><span class="sxs-lookup"><span data-stu-id="1ab60-107">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="1ab60-108">Ein Zeiger auf die Zuweisung, die dieses Beispiel erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="1ab60-108">Pointer to the allocator that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="1ab60-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="1ab60-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="1ab60-110">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1ab60-110">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="1ab60-111">*PHR*</span><span class="sxs-lookup"><span data-stu-id="1ab60-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="1ab60-112">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1ab60-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="1ab60-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="1ab60-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="1ab60-114">Zeiger auf einen vom Aufrufer zugeordneten Speicherpuffer mit einer Größen *Länge*.</span><span class="sxs-lookup"><span data-stu-id="1ab60-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span> <span data-ttu-id="1ab60-115">Der Puffer sollte eine GDI-geräteunabhängige Bitmap (DIB) enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ab60-115">The buffer should contain a GDI device-independent bitmap (DIB).</span></span>

</dd> <dt>

<span data-ttu-id="1ab60-116">*length*</span><span class="sxs-lookup"><span data-stu-id="1ab60-116">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="1ab60-117">Die Länge des Puffers.</span><span class="sxs-lookup"><span data-stu-id="1ab60-117">Length of the buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ab60-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ab60-118">Remarks</span></span>

<span data-ttu-id="1ab60-119">Die Klasse [**cimagezuordcator**](cimageallocator.md) erstellt mithilfe eines Datei Zuordnungsobjekts, das von der Auslagerungs Datei des Betriebssystems unterstützt wird, ein DIB.</span><span class="sxs-lookup"><span data-stu-id="1ab60-119">The [**CImageAllocator**](cimageallocator.md) class creates a DIB using a file-mapping object that is backed by the operating-system paging file.</span></span> <span data-ttu-id="1ab60-120">Das Handle für das Datei Zuordnung-Objekt wird im **hmapping** -Member der **m \_ dibdata** -Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1ab60-120">The handle to the file-mapping object is stored in the **hMapping** member of the **m\_DibData** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ab60-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ab60-121">Requirements</span></span>



| <span data-ttu-id="1ab60-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ab60-122">Requirement</span></span> | <span data-ttu-id="1ab60-123">Wert</span><span class="sxs-lookup"><span data-stu-id="1ab60-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab60-124">Header</span><span class="sxs-lookup"><span data-stu-id="1ab60-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1ab60-125"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ab60-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1ab60-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1ab60-126">Library</span></span><br/> | <dl> <span data-ttu-id="1ab60-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1ab60-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ab60-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ab60-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ab60-129">**Cimagesample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1ab60-129">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




