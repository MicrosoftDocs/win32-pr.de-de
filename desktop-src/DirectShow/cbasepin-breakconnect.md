---
description: 'CBasePin.BreakConnect-Methode: Die BreakConnect-Methode gibt den Pin von einer Verbindung frei.'
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: CBasePin.BreakConnect-Methode (Amfilter.h)
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
ms.openlocfilehash: a9a099b1001c2b8c30398ca350e05d15562a8bc2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099438"
---
# <a name="cbasepinbreakconnect-method"></a><span data-ttu-id="8a07a-103">CBasePin.BreakConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="8a07a-103">CBasePin.BreakConnect method</span></span>

<span data-ttu-id="8a07a-104">Die `BreakConnect` -Methode gibt den Pin von einer Verbindung frei.</span><span class="sxs-lookup"><span data-stu-id="8a07a-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a07a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a07a-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="8a07a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a07a-106">Parameters</span></span>

<span data-ttu-id="8a07a-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8a07a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8a07a-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a07a-108">Return value</span></span>

<span data-ttu-id="8a07a-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="8a07a-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a07a-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a07a-110">Remarks</span></span>

<span data-ttu-id="8a07a-111">Diese Methode wird während der Verbindungstrennung durch die [**CBasePin::D isconnect-Methode**](cbasepin-disconnect.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8a07a-111">This method is called during pin disconnection by the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method.</span></span> <span data-ttu-id="8a07a-112">Sie wird auch während eines Verbindungsversuchs aufgerufen, wenn die [**CBasePin::CheckConnect-Methode**](cbasepin-checkconnect.md) fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="8a07a-112">It is also called during a connection attempt if the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method fails.</span></span>

<span data-ttu-id="8a07a-113">Diese Methode muss alle Ressourcen freigeben, die von der **CheckConnect-Methode** abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="8a07a-113">This method must free any resources that were obtained by the **CheckConnect** method.</span></span> <span data-ttu-id="8a07a-114">Wenn z. B. **CheckConnect** Arbeitsspeicher zuweist, `BreakConnect` sollte den Arbeitsspeicher freigeben.</span><span class="sxs-lookup"><span data-stu-id="8a07a-114">For example, if **CheckConnect** allocates memory, `BreakConnect` should free the memory.</span></span> <span data-ttu-id="8a07a-115">Wenn **CheckConnect** den Verbindungsanschluss für eine Schnittstelle abfragt, `BreakConnect` sollte die Schnittstelle freigeben.</span><span class="sxs-lookup"><span data-stu-id="8a07a-115">If **CheckConnect** queries the connecting pin for an interface, `BreakConnect` should free the interface.</span></span>

<span data-ttu-id="8a07a-116">Beachten Sie, dass `BreakConnect` ohne einen entsprechenden Aufruf von **CompleteConnect** aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a07a-116">Note that `BreakConnect` can be called without a corresponding call to **CompleteConnect**.</span></span> <span data-ttu-id="8a07a-117">Daher können Sie nicht davon ausgehen, dass **CompleteConnect** zuvor aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="8a07a-117">Therefore, you cannot assume that **CompleteConnect** has been called previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a07a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a07a-118">Requirements</span></span>



| <span data-ttu-id="8a07a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a07a-119">Requirement</span></span> | <span data-ttu-id="8a07a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8a07a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a07a-121">Header</span><span class="sxs-lookup"><span data-stu-id="8a07a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8a07a-122"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="8a07a-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8a07a-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8a07a-123">Library</span></span><br/> | <dl> <span data-ttu-id="8a07a-124"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8a07a-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a07a-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8a07a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a07a-126">**CBasePin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8a07a-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




