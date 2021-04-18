---
description: Die Put \_ CurrentPosition-Methode legt die aktuelle Position relativ zur Gesamtdauer des Streams fest. Diese Methode implementiert die imediaposition::p UT \_ CurrentPosition-Methode.
ms.assetid: 22d7e9e4-47da-45b5-9be0-3c5128f90353
title: CPosPassThru.put_CurrentPosition-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85426636a34d0e197b36496d5a38a847c61b9501
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358788"
---
# <a name="cpospassthruput_currentposition-method"></a><span data-ttu-id="0c197-104">Cpospassthru. Put \_ CurrentPosition-Methode</span><span class="sxs-lookup"><span data-stu-id="0c197-104">CPosPassThru.put\_CurrentPosition method</span></span>

<span data-ttu-id="0c197-105">Die- `put_CurrentPosition` Methode legt die aktuelle Position relativ zur Gesamtdauer des Streams fest.</span><span class="sxs-lookup"><span data-stu-id="0c197-105">The `put_CurrentPosition` method sets the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="0c197-106">Diese Methode implementiert die [**imediaposition::p UT \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0c197-106">This method implements the [**IMediaPosition::put\_CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c197-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c197-107">Syntax</span></span>


```C++
HRESULT put_CurrentPosition(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="0c197-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c197-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c197-109">*lltime*</span><span class="sxs-lookup"><span data-stu-id="0c197-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="0c197-110">Neue Position in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="0c197-110">New position, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c197-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c197-111">Return value</span></span>

<span data-ttu-id="0c197-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="0c197-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c197-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c197-113">Requirements</span></span>



| <span data-ttu-id="0c197-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c197-114">Requirement</span></span> | <span data-ttu-id="0c197-115">Wert</span><span class="sxs-lookup"><span data-stu-id="0c197-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c197-116">Header</span><span class="sxs-lookup"><span data-stu-id="0c197-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0c197-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c197-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0c197-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0c197-118">Library</span></span><br/> | <dl> <span data-ttu-id="0c197-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0c197-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c197-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c197-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c197-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0c197-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




