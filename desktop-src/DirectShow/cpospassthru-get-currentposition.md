---
description: 'Die get \_ CurrentPosition-Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab. Diese Methode implementiert die imediaposition:: get \_ CurrentPosition-Methode.'
ms.assetid: 6e68af98-440d-4ecc-b1aa-d5e241de4999
title: CPosPassThru.get_CurrentPosition-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c146eb1ee3d0a48da90973ab181a4bd02182331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368501"
---
# <a name="cpospassthruget_currentposition-method"></a><span data-ttu-id="a2f82-104">Cpospassthru. get \_ CurrentPosition-Methode</span><span class="sxs-lookup"><span data-stu-id="a2f82-104">CPosPassThru.get\_CurrentPosition method</span></span>

<span data-ttu-id="a2f82-105">Die- `get_CurrentPosition` Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="a2f82-105">The `get_CurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="a2f82-106">Diese Methode implementiert die [**imediaposition:: get \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a2f82-106">This method implements the [**IMediaPosition::get\_CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2f82-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2f82-107">Syntax</span></span>


```C++
HRESULT get_CurrentPosition(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="a2f82-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2f82-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2f82-109">*plltime*</span><span class="sxs-lookup"><span data-stu-id="a2f82-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="a2f82-110">Ein Zeiger auf eine Variable, die die aktuelle Position (in Sekunden) empfängt.</span><span class="sxs-lookup"><span data-stu-id="a2f82-110">Pointer to a variable that receives the current position, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2f82-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2f82-111">Return value</span></span>

<span data-ttu-id="a2f82-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="a2f82-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2f82-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2f82-113">Requirements</span></span>



| <span data-ttu-id="a2f82-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2f82-114">Requirement</span></span> | <span data-ttu-id="a2f82-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a2f82-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2f82-116">Header</span><span class="sxs-lookup"><span data-stu-id="a2f82-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a2f82-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2f82-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a2f82-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a2f82-118">Library</span></span><br/> | <dl> <span data-ttu-id="a2f82-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a2f82-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2f82-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2f82-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2f82-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a2f82-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




