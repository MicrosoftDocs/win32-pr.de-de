---
description: Die Methode "Methode" erstellt eine GDI-geräteunabhängige Bitmap (DIB). Das DIB wird in einem freigegebenen mempory-Block zugeordnet, der einen Kopiervorgang ausschließt, wenn der besitzende Filter das Image löscht.
ms.assetid: 8a9ab1cf-4104-48e9-ba6c-28d0f1a1d226
title: Cimagezuzuordcator. kreatedib-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateDIB
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 316b7aeadfa442a8df4e80075380464758f3c6bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365506"
---
# <a name="cimageallocatorcreatedib-method"></a><span data-ttu-id="abde1-104">Cimagezuzuordcator. kreatedib-Methode</span><span class="sxs-lookup"><span data-stu-id="abde1-104">CImageAllocator.CreateDIB method</span></span>

<span data-ttu-id="abde1-105">Die `CreateDIB` -Methode erstellt eine GDI-geräteunabhängige Bitmap (DIB).</span><span class="sxs-lookup"><span data-stu-id="abde1-105">The `CreateDIB` method creates a GDI device-independent bitmap (DIB).</span></span> <span data-ttu-id="abde1-106">Das DIB wird in einem freigegebenen mempory-Block zugeordnet, der einen Kopiervorgang ausschließt, wenn der besitzende Filter das Image löscht.</span><span class="sxs-lookup"><span data-stu-id="abde1-106">The DIB is allocated in a shared mempory block, which eliminates a copy operation when the owning filter blits the image.</span></span>

## <a name="syntax"></a><span data-ttu-id="abde1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="abde1-107">Syntax</span></span>


```C++
HRESULT CreateDIB(
        LONG    InSize,
  [ref] DIBDATA &DibData
);
```



## <a name="parameters"></a><span data-ttu-id="abde1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="abde1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abde1-109">*Insize*</span><span class="sxs-lookup"><span data-stu-id="abde1-109">*InSize*</span></span> 
</dt> <dd>

<span data-ttu-id="abde1-110">Größe der Bitmap.</span><span class="sxs-lookup"><span data-stu-id="abde1-110">Size of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="abde1-111">*Dibdata* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="abde1-111">*DibData* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="abde1-112">Verweis auf eine [**dibdata**](dibdata.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="abde1-112">Reference to a [**DIBDATA**](dibdata.md) structure.</span></span> <span data-ttu-id="abde1-113">Die-Methode füllt diese-Struktur mit Informationen über das DIB aus.</span><span class="sxs-lookup"><span data-stu-id="abde1-113">The method fills in this structure with information about the DIB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abde1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="abde1-114">Return value</span></span>

<span data-ttu-id="abde1-115">Gibt \_ bei Erfolg S OK oder andernfalls einen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="abde1-115">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="abde1-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abde1-116">Requirements</span></span>



| <span data-ttu-id="abde1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abde1-117">Requirement</span></span> | <span data-ttu-id="abde1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="abde1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abde1-119">Header</span><span class="sxs-lookup"><span data-stu-id="abde1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="abde1-120"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="abde1-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="abde1-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="abde1-121">Library</span></span><br/> | <dl> <span data-ttu-id="abde1-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="abde1-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abde1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abde1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abde1-124">**Cimagezuordcator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="abde1-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> <dt>

[<span data-ttu-id="abde1-125">**Cimagezuordcator:: zuzuweisung**</span><span class="sxs-lookup"><span data-stu-id="abde1-125">**CImageAllocator::Alloc**</span></span>](cimageallocator-alloc.md)
</dt> </dl>

 

 




