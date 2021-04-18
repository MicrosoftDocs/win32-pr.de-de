---
description: Die breakconnect-Methode gibt eine PIN von einer Verbindung frei.
ms.assetid: cc384786-9cba-4f68-9c60-740205b35661
title: Ctransformfilter. breakconnect-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec60322a4782d84e84dc2030b69f6c385783e98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372271"
---
# <a name="ctransformfilterbreakconnect-method"></a><span data-ttu-id="bc011-103">Ctransformfilter. breakconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="bc011-103">CTransformFilter.BreakConnect method</span></span>

<span data-ttu-id="bc011-104">Die- `BreakConnect` Methode gibt eine PIN von einer Verbindung frei.</span><span class="sxs-lookup"><span data-stu-id="bc011-104">The `BreakConnect` method releases a pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc011-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc011-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect(
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a><span data-ttu-id="bc011-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc011-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc011-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="bc011-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="bc011-108">Member des enumerierten Typs der [**Pin- \_ Richtung**](/windows/win32/api/strmif/ne-strmif-pin_direction) , der angibt, welche Pin-Verbindung unterbrochen wurde (Eingabe oder Ausgabe).</span><span class="sxs-lookup"><span data-stu-id="bc011-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin connection was broken (input or output).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc011-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc011-109">Return value</span></span>

<span data-ttu-id="bc011-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="bc011-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc011-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc011-111">Remarks</span></span>

<span data-ttu-id="bc011-112">Die [**ctransforminputpin:: breakconnect**](ctransforminputpin-breakconnect.md) -Methode und die [**ctransformoutputpin:: breakconnect**](ctransformoutputpin-breakconnect.md) -Methode ruft diese Methode auf, wenn eine PIN-Verbindung unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="bc011-112">The [**CTransformInputPin::BreakConnect**](ctransforminputpin-breakconnect.md) and [**CTransformOutputPin::BreakConnect**](ctransformoutputpin-breakconnect.md) methods call this method when a pin connection is broken.</span></span> <span data-ttu-id="bc011-113">Diese Methode führt in der Basisklasse keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="bc011-113">This method does nothing in the base class.</span></span> <span data-ttu-id="bc011-114">Wenn Sie die [**checkConnect**](ctransformfilter-checkconnect.md) -Methode überschreiben, überschreiben Sie diese Methode, um alle Ressourcen freizugeben, die in der **checkConnect** -Methode (einschließlich Schnittstellen Zeigern)</span><span class="sxs-lookup"><span data-stu-id="bc011-114">If you override the [**CheckConnect**](ctransformfilter-checkconnect.md) method, override this method to release any resources obtained in the **CheckConnect** method, including interface pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc011-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc011-115">Requirements</span></span>



| <span data-ttu-id="bc011-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc011-116">Requirement</span></span> | <span data-ttu-id="bc011-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bc011-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc011-118">Header</span><span class="sxs-lookup"><span data-stu-id="bc011-118">Header</span></span><br/>  | <dl> <span data-ttu-id="bc011-119"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc011-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bc011-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bc011-120">Library</span></span><br/> | <dl> <span data-ttu-id="bc011-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bc011-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc011-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc011-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc011-123">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="bc011-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




