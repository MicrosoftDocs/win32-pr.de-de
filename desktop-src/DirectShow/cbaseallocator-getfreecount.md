---
description: Die getfrecount-Methode ruft die Anzahl von Medien Beispielen ab, die nicht verwendet werden.
ms.assetid: f4ce4cca-0168-42db-9fe7-858862f033a8
title: Cbasezucator. getfrecount-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetFreeCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0538229053b5d47ca1bdc8f30b38a0937e36cb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371278"
---
# <a name="cbaseallocatorgetfreecount-method"></a><span data-ttu-id="ca978-103">Cbasezucator. getfrecount-Methode</span><span class="sxs-lookup"><span data-stu-id="ca978-103">CBaseAllocator.GetFreeCount method</span></span>

<span data-ttu-id="ca978-104">Die- `GetFreeCount` Methode ruft die Anzahl von Medien Beispielen ab, die nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca978-104">The `GetFreeCount` method retrieves the number of media samples that are not in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca978-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca978-105">Syntax</span></span>


```C++
HRESULT GetFreeCount(
   LONG *plBuffersFree
);
```



## <a name="parameters"></a><span data-ttu-id="ca978-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca978-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca978-107">*plbuffersfree*</span><span class="sxs-lookup"><span data-stu-id="ca978-107">*plBuffersFree*</span></span> 
</dt> <dd>

<span data-ttu-id="ca978-108">Adresse einer Variablen, die die Anzahl von Stichproben empfängt, die nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca978-108">Address of a variable that receives the number of samples that are not in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca978-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca978-109">Return value</span></span>

<span data-ttu-id="ca978-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="ca978-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca978-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca978-111">Remarks</span></span>

<span data-ttu-id="ca978-112">Diese Methode implementiert die [**imemzuzuchanorcallbacktemp:: getfrecount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ca978-112">This method implements the [**IMemAllocatorCallbackTemp::GetFreeCount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) method.</span></span> <span data-ttu-id="ca978-113">Die Zuweisung wird von der Zuweisung nicht verfügbar gemacht, es sei denn, das *fenablereleasecallback* -Flag ist im cbasezucator-Konstruktor auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ca978-113">The allocator does not expose the IMemAllocatorCallbackTemp interface unless the *fEnableReleaseCallback* flag is set to **TRUE** in the CBaseAllocator constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca978-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca978-114">Requirements</span></span>



| <span data-ttu-id="ca978-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca978-115">Requirement</span></span> | <span data-ttu-id="ca978-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ca978-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca978-117">Header</span><span class="sxs-lookup"><span data-stu-id="ca978-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ca978-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca978-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ca978-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ca978-119">Library</span></span><br/> | <dl> <span data-ttu-id="ca978-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ca978-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca978-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca978-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca978-122">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ca978-122">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




