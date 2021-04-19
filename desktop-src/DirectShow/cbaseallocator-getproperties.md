---
description: 'Die GetProperties-Methode ruft die Anzahl der Puffer, die von der Zuweisung erstellt werden, und die Puffer Eigenschaften ab. Diese Methode implementiert die imemzuzucator:: GetProperties-Methode.'
ms.assetid: ccee4d69-52fc-4e3c-b6a4-787914708be4
title: Cbasezucator. GetProperties-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abf143b11b6dd67fca6c87f9a31ce69f18951311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359373"
---
# <a name="cbaseallocatorgetproperties-method"></a><span data-ttu-id="f3549-104">Cbasezucator. GetProperties-Methode</span><span class="sxs-lookup"><span data-stu-id="f3549-104">CBaseAllocator.GetProperties method</span></span>

<span data-ttu-id="f3549-105">Die `GetProperties` -Methode ruft die Anzahl der Puffer, die von der Zuweisung erstellt werden, und die Puffer Eigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="f3549-105">The `GetProperties` method retrieves the number of buffers that the allocator will create, and the buffer properties.</span></span> <span data-ttu-id="f3549-106">Diese Methode implementiert die [**imemzuzucator:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f3549-106">This method implements the [**IMemAllocator::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3549-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3549-107">Syntax</span></span>


```C++
HRESULT GetProperties(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="f3549-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3549-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3549-109">*p-Eigenschaften*</span><span class="sxs-lookup"><span data-stu-id="f3549-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="f3549-110">Zeiger auf eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die die zuordnereigenschaften empfängt.</span><span class="sxs-lookup"><span data-stu-id="f3549-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that receives the allocator properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3549-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3549-111">Return value</span></span>

<span data-ttu-id="f3549-112">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="f3549-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3549-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3549-113">Requirements</span></span>



| <span data-ttu-id="f3549-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3549-114">Requirement</span></span> | <span data-ttu-id="f3549-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f3549-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3549-116">Header</span><span class="sxs-lookup"><span data-stu-id="f3549-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f3549-117"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3549-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f3549-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f3549-118">Library</span></span><br/> | <dl> <span data-ttu-id="f3549-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f3549-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3549-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3549-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3549-121">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f3549-121">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




