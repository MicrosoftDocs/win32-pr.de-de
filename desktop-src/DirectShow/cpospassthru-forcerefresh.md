---
description: Die forceRefresh-Methode ist veraltet.
ms.assetid: 9895f72b-abf8-46a8-aa75-2a30901a4c41
title: Cpospassthru. forceRefresh-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ForceRefresh
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1955afe069dc419b710978eecf662758916e4cb1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372122"
---
# <a name="cpospassthruforcerefresh-method"></a><span data-ttu-id="4f732-103">Cpospassthru. forceRefresh-Methode</span><span class="sxs-lookup"><span data-stu-id="4f732-103">CPosPassThru.ForceRefresh method</span></span>

<span data-ttu-id="4f732-104">Die- `ForceRefresh` Methode ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="4f732-104">The `ForceRefresh` method is obsolete.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f732-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f732-105">Syntax</span></span>


```C++
HRESULT ForceRefresh();
```



## <a name="parameters"></a><span data-ttu-id="4f732-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f732-106">Parameters</span></span>

<span data-ttu-id="4f732-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4f732-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f732-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f732-108">Return value</span></span>

<span data-ttu-id="4f732-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="4f732-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f732-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f732-110">Remarks</span></span>

<span data-ttu-id="4f732-111">Ursprünglich war diese Klasse so konzipiert, dass Zeiger auf die Schnittstellen [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) und [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) der verbundenen Pin zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4f732-111">Originally this class was designed to cache pointers to the connected pin's [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interfaces.</span></span> <span data-ttu-id="4f732-112">Die- `ForceRefresh` Methode hat diese Schnittstellen freigegeben.</span><span class="sxs-lookup"><span data-stu-id="4f732-112">The `ForceRefresh` method released those interfaces.</span></span>

<span data-ttu-id="4f732-113">Wie momentan implementiert, speichert diese Klasse diese Schnittstellen nicht zwischen.</span><span class="sxs-lookup"><span data-stu-id="4f732-113">As currently implemented, this class does not cache those interfaces.</span></span> <span data-ttu-id="4f732-114">Aus Kompatibilitätsgründen `ForceRefresh` ist die Methode weiterhin enthalten, aber Sie gibt "OK" zurück, \_ ohne etwas zu tun.</span><span class="sxs-lookup"><span data-stu-id="4f732-114">For compatibility, the `ForceRefresh` method is still included, but it returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f732-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f732-115">Requirements</span></span>



| <span data-ttu-id="4f732-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f732-116">Requirement</span></span> | <span data-ttu-id="4f732-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4f732-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f732-118">Header</span><span class="sxs-lookup"><span data-stu-id="4f732-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4f732-119"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f732-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4f732-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4f732-120">Library</span></span><br/> | <dl> <span data-ttu-id="4f732-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4f732-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f732-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f732-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f732-123">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4f732-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




