---
description: Die Disconnect-Methode unterbricht die Verbindung mit der Ausgabepin.
ms.assetid: 6e362e32-7b74-4392-b46f-1ab47a30a07b
title: Cpullpin. Disconnect-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec13a7f29a06bab4f79ddb58932796f8363adadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362046"
---
# <a name="cpullpindisconnect-method"></a><span data-ttu-id="a7f14-103">Cpullpin. Disconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="a7f14-103">CPullPin.Disconnect method</span></span>

<span data-ttu-id="a7f14-104">Die- `Disconnect` Methode unterbricht die Verbindung mit der Ausgabepin.</span><span class="sxs-lookup"><span data-stu-id="a7f14-104">The `Disconnect` method breaks the connection with the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7f14-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7f14-105">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="a7f14-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7f14-106">Parameters</span></span>

<span data-ttu-id="a7f14-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a7f14-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7f14-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7f14-108">Return value</span></span>

<span data-ttu-id="a7f14-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="a7f14-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7f14-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7f14-110">Remarks</span></span>

<span data-ttu-id="a7f14-111">Diese Methode unterbricht jede in der [**cpullpin:: Connect**](cpullpin-connect.md) -Methode hergestellte Verbindung.</span><span class="sxs-lookup"><span data-stu-id="a7f14-111">This method breaks any connection made in the [**CPullPin::Connect**](cpullpin-connect.md) method.</span></span> <span data-ttu-id="a7f14-112">Nennen Sie diese Methode in Ihrer [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a7f14-112">Call this method inside your [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span> <span data-ttu-id="a7f14-113">(Wenn Ihre PIN von [**cbasepin**](cbasepin.md)abgeleitet ist, überschreiben Sie [**cbasepin:: breakconnect**](cbasepin-breakconnect.md) , um diese Methode aufzurufen.)</span><span class="sxs-lookup"><span data-stu-id="a7f14-113">(If your pin derives from [**CBasePin**](cbasepin.md), override [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) to call this method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="a7f14-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7f14-114">Requirements</span></span>



| <span data-ttu-id="a7f14-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7f14-115">Requirement</span></span> | <span data-ttu-id="a7f14-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a7f14-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f14-117">Header</span><span class="sxs-lookup"><span data-stu-id="a7f14-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a7f14-118"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7f14-118"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="a7f14-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a7f14-119">Library</span></span><br/> | <dl> <span data-ttu-id="a7f14-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a7f14-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7f14-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7f14-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7f14-122">**Cpullpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a7f14-122">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




