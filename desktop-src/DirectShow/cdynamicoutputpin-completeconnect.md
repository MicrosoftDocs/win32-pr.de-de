---
description: 'CDynamicOutputPin.CompleteConnect-Methode: Die CompleteConnect-Methode schließt eine Verbindung mit einem Eingabepin ab.'
ms.assetid: c23195e7-8d66-4217-bd59-8889459ce4f1
title: CDynamicOutputPin.CompleteConnect-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5fa15c84b9d9e0b686e17110c656b74161687705
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095738"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a><span data-ttu-id="26e6b-103">CDynamicOutputPin.CompleteConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="26e6b-103">CDynamicOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="26e6b-104">Die `CompleteConnect` -Methode schließt eine Verbindung mit einem Eingabepin ab.</span><span class="sxs-lookup"><span data-stu-id="26e6b-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="26e6b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="26e6b-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="26e6b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="26e6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26e6b-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="26e6b-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="26e6b-108">Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Eingabepins.</span><span class="sxs-lookup"><span data-stu-id="26e6b-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26e6b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26e6b-109">Return value</span></span>

<span data-ttu-id="26e6b-110">Gibt bei Erfolg S \_ OK oder einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="26e6b-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="26e6b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26e6b-111">Remarks</span></span>

<span data-ttu-id="26e6b-112">Diese Methode überschreibt die [**CBaseOutputPin::CompleteConnect-Methode.**](cbaseoutputpin-completeconnect.md)</span><span class="sxs-lookup"><span data-stu-id="26e6b-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="26e6b-113">Um dynamische Wiederherstellungsverknüpfungen zu unterstützen, committet diese Methode die Zuweisung, wenn der Filter aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="26e6b-113">To support dynamic reconnections, this method commits the allocator if the filter is active.</span></span> <span data-ttu-id="26e6b-114">In der Basisklasse können Verbindungen nur auftreten, wenn der Filter beendet wird, sodass für die Zuweisung immer ein Commit in der [**CBaseOutputPin::Active-Methode**](cbaseoutputpin-active.md) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26e6b-114">In the base class, connections can occur only when the filter is stopped, so the allocator is always committed in the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="26e6b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26e6b-115">Requirements</span></span>



| <span data-ttu-id="26e6b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26e6b-116">Requirement</span></span> | <span data-ttu-id="26e6b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="26e6b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26e6b-118">Header</span><span class="sxs-lookup"><span data-stu-id="26e6b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="26e6b-119"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="26e6b-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="26e6b-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="26e6b-120">Library</span></span><br/> | <dl> <span data-ttu-id="26e6b-121"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="26e6b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26e6b-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="26e6b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26e6b-123">**CDynamicOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="26e6b-123">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




