---
description: Die-Methode wird von der-Basisklasse benachrichtigt, dass die PIN gestartet oder beendet wurde.
ms.assetid: a3c000e1-18a1-48f7-9e2e-fe63cf13fc5c
title: Cbasestreamcontrol. geleert-Methode ("strinmctl. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.Flushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d4a3a2375ca799f5dd35def03295f29f61c0583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362019"
---
# <a name="cbasestreamcontrolflushing-method"></a><span data-ttu-id="c07e0-103">Cbasestreamcontrol. geleert-Methode</span><span class="sxs-lookup"><span data-stu-id="c07e0-103">CBaseStreamControl.Flushing method</span></span>

<span data-ttu-id="c07e0-104">Die- `Flushing` Methode benachrichtigt die-Basisklasse, dass die PIN gestartet oder beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c07e0-104">The `Flushing` method notifies the base class that the pin has started or stopped flushing.</span></span>

## <a name="syntax"></a><span data-ttu-id="c07e0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c07e0-105">Syntax</span></span>


```C++
void Flushing(
   BOOL bInProgress
);
```



## <a name="parameters"></a><span data-ttu-id="c07e0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c07e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c07e0-107">*binprogress*</span><span class="sxs-lookup"><span data-stu-id="c07e0-107">*bInProgress*</span></span> 
</dt> <dd>

<span data-ttu-id="c07e0-108">Gibt einen booleschen Wert an, der angibt, ob die PIN geleert wird.</span><span class="sxs-lookup"><span data-stu-id="c07e0-108">Specifies a Boolean value that indicates whether the pin is flushing.</span></span> <span data-ttu-id="c07e0-109">Verwenden Sie den Wert **true** , wenn die PIN einen Leerungs Vorgang startet, und **false** , wenn die PIN einen Löschvorgang beendet.</span><span class="sxs-lookup"><span data-stu-id="c07e0-109">Use the value **TRUE** when the pin begins a flush operation, and **FALSE** when the pin ends a flush operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c07e0-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c07e0-110">Return value</span></span>

<span data-ttu-id="c07e0-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c07e0-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c07e0-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c07e0-112">Remarks</span></span>

<span data-ttu-id="c07e0-113">Die PIN muss diese Methode innerhalb der [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -und [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c07e0-113">The pin must call this method from within its [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods.</span></span> <span data-ttu-id="c07e0-114">Geben Sie **true** in **beginflush** und **false** in **endflush** an.</span><span class="sxs-lookup"><span data-stu-id="c07e0-114">Specify **TRUE** in **BeginFlush** and **FALSE** in **EndFlush**.</span></span>

<span data-ttu-id="c07e0-115">Diese Methode bewirkt, dass die [**cbasestreamcontrol:: checkstreamstate**](cbasestreamcontrol-checkstreamstate.md) -Methode nicht mehr wartet.</span><span class="sxs-lookup"><span data-stu-id="c07e0-115">This method causes the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method to stop waiting.</span></span> <span data-ttu-id="c07e0-116">Während die PIN geleert wird, gibt **checkstreamstate** immer Stream- \_ verwerfen zurück.</span><span class="sxs-lookup"><span data-stu-id="c07e0-116">While the pin is flushing, **CheckStreamState** always returns STREAM\_DISCARDING.</span></span>

## <a name="requirements"></a><span data-ttu-id="c07e0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c07e0-117">Requirements</span></span>



| <span data-ttu-id="c07e0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c07e0-118">Requirement</span></span> | <span data-ttu-id="c07e0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c07e0-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c07e0-120">Header</span><span class="sxs-lookup"><span data-stu-id="c07e0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c07e0-121"><dt>"Strauch. h" (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c07e0-121"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c07e0-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c07e0-122">Library</span></span><br/> | <dl> <span data-ttu-id="c07e0-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c07e0-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c07e0-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c07e0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c07e0-125">**Cbasestreamcontrol-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c07e0-125">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




