---
description: 'Die getactualdatalength-Methode ruft die Länge der gültigen Daten im Puffer ab. Diese Methode implementiert die imediasample:: getactualdatalength-Methode.'
ms.assetid: bdb8c2b9-7be4-494b-bb96-34a9936d4a2f
title: Cmediasample. getactualdatalength-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e65b72c1e0b6db85a271c10f76e5630b0799b78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352105"
---
# <a name="cmediasamplegetactualdatalength-method"></a><span data-ttu-id="79523-104">Cmediasample. getactualdatalength-Methode</span><span class="sxs-lookup"><span data-stu-id="79523-104">CMediaSample.GetActualDataLength method</span></span>

<span data-ttu-id="79523-105">Die- `GetActualDataLength` Methode ruft die Länge der gültigen Daten im Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="79523-105">The `GetActualDataLength` method retrieves the length of the valid data in the buffer.</span></span> <span data-ttu-id="79523-106">Diese Methode implementiert die [**imediasample:: getactualdatalength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) -Methode.</span><span class="sxs-lookup"><span data-stu-id="79523-106">This method implements the [**IMediaSample::GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="79523-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="79523-107">Syntax</span></span>


```C++
LONG GetActualDataLength();
```



## <a name="parameters"></a><span data-ttu-id="79523-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="79523-108">Parameters</span></span>

<span data-ttu-id="79523-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="79523-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="79523-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79523-110">Return value</span></span>

<span data-ttu-id="79523-111">Gibt die Länge der gültigen Daten in Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="79523-111">Returns the length of the valid data, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="79523-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79523-112">Remarks</span></span>

<span data-ttu-id="79523-113">Die Variable [**cmediasample:: m \_ lactive**](cmediasample-m-lactual.md) Member gibt diese Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="79523-113">The [**CMediaSample::m\_lActual**](cmediasample-m-lactual.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="79523-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79523-114">Requirements</span></span>



| <span data-ttu-id="79523-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79523-115">Requirement</span></span> | <span data-ttu-id="79523-116">Wert</span><span class="sxs-lookup"><span data-stu-id="79523-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79523-117">Header</span><span class="sxs-lookup"><span data-stu-id="79523-117">Header</span></span><br/>  | <dl> <span data-ttu-id="79523-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79523-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="79523-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="79523-119">Library</span></span><br/> | <dl> <span data-ttu-id="79523-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="79523-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79523-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79523-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79523-122">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="79523-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

