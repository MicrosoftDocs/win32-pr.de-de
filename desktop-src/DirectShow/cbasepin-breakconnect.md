---
description: Die breakconnect-Methode gibt die PIN von einer Verbindung frei.
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: Cbasepin. breakconnect-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8964ea76e48e4753f42923663ab45962cd672e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354793"
---
# <a name="cbasepinbreakconnect-method"></a><span data-ttu-id="76a73-103">Cbasepin. breakconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="76a73-103">CBasePin.BreakConnect method</span></span>

<span data-ttu-id="76a73-104">Die- `BreakConnect` Methode gibt die PIN von einer Verbindung frei.</span><span class="sxs-lookup"><span data-stu-id="76a73-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="76a73-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76a73-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="76a73-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="76a73-106">Parameters</span></span>

<span data-ttu-id="76a73-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="76a73-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="76a73-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76a73-108">Return value</span></span>

<span data-ttu-id="76a73-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="76a73-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="76a73-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76a73-110">Remarks</span></span>

<span data-ttu-id="76a73-111">Diese Methode wird während der PIN-Trennung durch die [**cbasepin::D isconnect**](cbasepin-disconnect.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="76a73-111">This method is called during pin disconnection by the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method.</span></span> <span data-ttu-id="76a73-112">Sie wird auch während eines Verbindungsversuchs aufgerufen, wenn die [**cbasepin:: checkConnect**](cbasepin-checkconnect.md) -Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="76a73-112">It is also called during a connection attempt if the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method fails.</span></span>

<span data-ttu-id="76a73-113">Diese Methode muss alle Ressourcen freigeben, die von der **checkConnect** -Methode abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="76a73-113">This method must free any resources that were obtained by the **CheckConnect** method.</span></span> <span data-ttu-id="76a73-114">Wenn **checkConnect** z. b. Arbeitsspeicher belegt, `BreakConnect` sollte den Arbeitsspeicher freigeben.</span><span class="sxs-lookup"><span data-stu-id="76a73-114">For example, if **CheckConnect** allocates memory, `BreakConnect` should free the memory.</span></span> <span data-ttu-id="76a73-115">Wenn **Check Connect** die Verbindungs-PIN für eine Schnittstelle abfragt, `BreakConnect` sollte die Schnittstelle freigeben.</span><span class="sxs-lookup"><span data-stu-id="76a73-115">If **CheckConnect** queries the connecting pin for an interface, `BreakConnect` should free the interface.</span></span>

<span data-ttu-id="76a73-116">Beachten Sie, dass `BreakConnect` ohne einen entsprechenden Aufruf von **completeconnect** aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="76a73-116">Note that `BreakConnect` can be called without a corresponding call to **CompleteConnect**.</span></span> <span data-ttu-id="76a73-117">Daher können Sie nicht davon ausgehen, dass **completeconnect** bereits zuvor aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="76a73-117">Therefore, you cannot assume that **CompleteConnect** has been called previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="76a73-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76a73-118">Requirements</span></span>



| <span data-ttu-id="76a73-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76a73-119">Requirement</span></span> | <span data-ttu-id="76a73-120">Wert</span><span class="sxs-lookup"><span data-stu-id="76a73-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76a73-121">Header</span><span class="sxs-lookup"><span data-stu-id="76a73-121">Header</span></span><br/>  | <dl> <span data-ttu-id="76a73-122"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76a73-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="76a73-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="76a73-123">Library</span></span><br/> | <dl> <span data-ttu-id="76a73-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="76a73-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76a73-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76a73-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76a73-126">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="76a73-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




