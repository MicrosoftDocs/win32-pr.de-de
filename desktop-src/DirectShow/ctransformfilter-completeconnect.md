---
description: Die completeconnect-Methode schließt eine PIN-Verbindung ab.
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: Ctransformfilter. completeconnect-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 630950cf9b05c08412394bf9270f2369b3f3b94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357724"
---
# <a name="ctransformfiltercompleteconnect-method"></a><span data-ttu-id="57dc9-103">Ctransformfilter. completeconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="57dc9-103">CTransformFilter.CompleteConnect method</span></span>

<span data-ttu-id="57dc9-104">Die- `CompleteConnect` Methode schließt eine PIN-Verbindung ab.</span><span class="sxs-lookup"><span data-stu-id="57dc9-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="57dc9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="57dc9-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="57dc9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="57dc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57dc9-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="57dc9-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="57dc9-108">Member des enumerierten Typs der [**Pin- \_ Richtung**](/windows/win32/api/strmif/ne-strmif-pin_direction) , der angibt, welche PIN im Filter die Verbindung herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="57dc9-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="57dc9-109">*preceivepin*</span><span class="sxs-lookup"><span data-stu-id="57dc9-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="57dc9-110">Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der anderen PIN bei diesem Verbindungsversuch.</span><span class="sxs-lookup"><span data-stu-id="57dc9-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57dc9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57dc9-111">Return value</span></span>

<span data-ttu-id="57dc9-112">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="57dc9-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="57dc9-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57dc9-113">Remarks</span></span>

<span data-ttu-id="57dc9-114">Die [**ctransforminputpin:: completeconnect**](ctransforminputpin-completeconnect.md) -Methode und die [**ctransformoutputpin:: completeconnect**](ctransformoutputpin-completeconnect.md) -Methode ruft diese Methode während des PIN-Verbindungsprozesses auf.</span><span class="sxs-lookup"><span data-stu-id="57dc9-114">The [**CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) and [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="57dc9-115">Diese Methode führt keine Aktion in der Basisklasse durch, aber die abgeleitete Klasse kann Sie überschreiben.</span><span class="sxs-lookup"><span data-stu-id="57dc9-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="57dc9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57dc9-116">Requirements</span></span>



| <span data-ttu-id="57dc9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57dc9-117">Requirement</span></span> | <span data-ttu-id="57dc9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="57dc9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57dc9-119">Header</span><span class="sxs-lookup"><span data-stu-id="57dc9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="57dc9-120"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57dc9-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="57dc9-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="57dc9-121">Library</span></span><br/> | <dl> <span data-ttu-id="57dc9-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="57dc9-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57dc9-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57dc9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57dc9-124">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="57dc9-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




