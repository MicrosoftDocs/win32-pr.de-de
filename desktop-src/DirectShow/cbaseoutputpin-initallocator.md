---
description: Die initbelegcator-Methode erstellt eine Speicherzuweisung.
ms.assetid: a1fa0ffb-ed43-446d-811e-6c3594743592
title: CBaseOutputPin.IniTAllocator-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.InitAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e5385671ba4c7fdf1b719f83aafba7d84421bce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371294"
---
# <a name="cbaseoutputpininitallocator-method"></a><span data-ttu-id="fb582-103">CBaseOutputPin.IniTAllocator-Methode</span><span class="sxs-lookup"><span data-stu-id="fb582-103">CBaseOutputPin.InitAllocator method</span></span>

<span data-ttu-id="fb582-104">Die- `InitAllocator` Methode erstellt eine Speicherzuweisung.</span><span class="sxs-lookup"><span data-stu-id="fb582-104">The `InitAllocator` method creates a memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb582-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb582-105">Syntax</span></span>


```C++
virtual HRESULT InitAllocator(
   IMemAllocator **ppAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="fb582-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb582-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb582-107">*ppzuweisung*</span><span class="sxs-lookup"><span data-stu-id="fb582-107">*ppAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="fb582-108">Adresse einer Variablen, die einen Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners empfängt.</span><span class="sxs-lookup"><span data-stu-id="fb582-108">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb582-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb582-109">Return value</span></span>

<span data-ttu-id="fb582-110">Gibt " \_ OK" zurück, wenn erfolgreich, oder einen Fehlercode aus der **cokreateinzustance** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="fb582-110">Returns S\_OK if successful, or an error code from the **CoCreateInstance** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb582-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb582-111">Remarks</span></span>

<span data-ttu-id="fb582-112">Wenn die Eingabe-PIN keine Speicherzuweisung bereitstellt, ruft die [**cbaseoutputpin::D ecidezuordcator**](cbaseoutputpin-decideallocator.md) -Methode diese Methode auf, um eine Zuweisung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fb582-112">If the input pin does not provide a memory allocator, the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method calls this method to create an allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb582-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb582-113">Requirements</span></span>



| <span data-ttu-id="fb582-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb582-114">Requirement</span></span> | <span data-ttu-id="fb582-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fb582-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb582-116">Header</span><span class="sxs-lookup"><span data-stu-id="fb582-116">Header</span></span><br/>  | <dl> <span data-ttu-id="fb582-117"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb582-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fb582-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb582-118">Library</span></span><br/> | <dl> <span data-ttu-id="fb582-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="fb582-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb582-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb582-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb582-121">**Cbaseoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fb582-121">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




