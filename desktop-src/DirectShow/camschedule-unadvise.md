---
description: Die unempfehlung-Methode entfernt eine anforderungsanforderung.
ms.assetid: b3dfda82-577e-4499-a114-1c8721e4af9e
title: Camschedule. unempfehlung-Methode (dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25dd70a46fcc2b6572500b3164b64fd0facbcbe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371614"
---
# <a name="camscheduleunadvise-method"></a><span data-ttu-id="1921f-103">Camschedule. unempfehlung-Methode</span><span class="sxs-lookup"><span data-stu-id="1921f-103">CAMSchedule.Unadvise method</span></span>

<span data-ttu-id="1921f-104">Die- `Unadvise` Methode entfernt eine anforderungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="1921f-104">The `Unadvise` method removes an advise request.</span></span>

## <a name="syntax"></a><span data-ttu-id="1921f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1921f-105">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="1921f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1921f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1921f-107">*dwadviabcookie*</span><span class="sxs-lookup"><span data-stu-id="1921f-107">*dwAdviseCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="1921f-108">Der Bezeichner der Benachrichtigungs Anforderung, der von der Methode " [**camschedule:: addadvisepacket**](camschedule-addadvisepacket.md) " zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1921f-108">Identifier of the advise request, returned by the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1921f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1921f-109">Return value</span></span>

<span data-ttu-id="1921f-110">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="1921f-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="1921f-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1921f-111">Return code</span></span>                                                                             | <span data-ttu-id="1921f-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1921f-112">Description</span></span>          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="1921f-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="1921f-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="1921f-114">Nicht gefunden</span><span class="sxs-lookup"><span data-stu-id="1921f-114">Not found</span></span><br/> |
| <dl> <span data-ttu-id="1921f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1921f-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="1921f-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="1921f-116">Success</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="1921f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1921f-117">Requirements</span></span>



| <span data-ttu-id="1921f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1921f-118">Requirement</span></span> | <span data-ttu-id="1921f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="1921f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1921f-120">Header</span><span class="sxs-lookup"><span data-stu-id="1921f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="1921f-121"><dt>Dsschedule. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1921f-121"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="1921f-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1921f-122">Library</span></span><br/> | <dl> <span data-ttu-id="1921f-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1921f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1921f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1921f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1921f-125">**Camschedule-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1921f-125">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




