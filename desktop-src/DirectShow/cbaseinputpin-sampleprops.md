---
description: Die sampleproperties-Methode ruft die Eigenschaften des neuesten Beispiels in einer am \_ SAMPLE2 \_ Properties-Struktur ab.
ms.assetid: d4c98c35-f8b2-4111-bae9-4e0f58a0cc8a
title: Cbaseingeputpin. samplerequismethode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.SampleProps
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45663cfd221c7a31abe5f85a494869b24d1ddd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371343"
---
# <a name="cbaseinputpinsampleprops-method"></a><span data-ttu-id="ed41f-103">Cbaseingeputpin. samplerequismethode</span><span class="sxs-lookup"><span data-stu-id="ed41f-103">CBaseInputPin.SampleProps method</span></span>

<span data-ttu-id="ed41f-104">Die- `SampleProps` Methode ruft die Eigenschaften des neuesten Beispiels in einer [**am \_ SAMPLE2 \_ Properties**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) -Struktur ab.</span><span class="sxs-lookup"><span data-stu-id="ed41f-104">The `SampleProps` method retrieves the properties of the most recent sample, in an [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed41f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed41f-105">Syntax</span></span>


```C++
AM_SAMPLE2_PROPERTIES* SampleProps();
```



## <a name="parameters"></a><span data-ttu-id="ed41f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed41f-106">Parameters</span></span>

<span data-ttu-id="ed41f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ed41f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed41f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed41f-108">Return value</span></span>

<span data-ttu-id="ed41f-109">Gibt die Adresse der [**cbaseingeputpin:: m \_ samplerequis-Member**](cbaseinputpin-m-sampleprops.md) -Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="ed41f-109">Returns the address of the [**CBaseInputPin::m\_SampleProps**](cbaseinputpin-m-sampleprops.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed41f-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed41f-110">Requirements</span></span>



| <span data-ttu-id="ed41f-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed41f-111">Requirement</span></span> | <span data-ttu-id="ed41f-112">Wert</span><span class="sxs-lookup"><span data-stu-id="ed41f-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed41f-113">Header</span><span class="sxs-lookup"><span data-stu-id="ed41f-113">Header</span></span><br/>  | <dl> <span data-ttu-id="ed41f-114"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed41f-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ed41f-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ed41f-115">Library</span></span><br/> | <dl> <span data-ttu-id="ed41f-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ed41f-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed41f-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed41f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed41f-118">**Cbaseingeputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ed41f-118">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




