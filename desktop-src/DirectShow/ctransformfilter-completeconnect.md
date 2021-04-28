---
description: 'CTransformFilter.CompleteConnect-Methode: Die CompleteConnect-Methode schließt eine Pinverbindung ab.'
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: CTransformFilter.CompleteConnect-Methode (Transfrm.h)
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
ms.openlocfilehash: d2251ba45c7a39ec9bf205fdd6643e02392e40e5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095168"
---
# <a name="ctransformfiltercompleteconnect-method"></a><span data-ttu-id="6b201-103">CTransformFilter.CompleteConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="6b201-103">CTransformFilter.CompleteConnect method</span></span>

<span data-ttu-id="6b201-104">Die `CompleteConnect` -Methode schließt eine Stecknadelverbindung ab.</span><span class="sxs-lookup"><span data-stu-id="6b201-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b201-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b201-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="6b201-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b201-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b201-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="6b201-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="6b201-108">Member des [**aufzählten PIN \_ DIRECTION-Typs,**](/windows/win32/api/strmif/ne-strmif-pin_direction) der an gibt, welcher Pin im Filter die Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6b201-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="6b201-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="6b201-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="6b201-110">Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des anderen Pins in diesem Verbindungsversuch.</span><span class="sxs-lookup"><span data-stu-id="6b201-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b201-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b201-111">Return value</span></span>

<span data-ttu-id="6b201-112">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="6b201-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b201-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b201-113">Remarks</span></span>

<span data-ttu-id="6b201-114">Die [**Methoden CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) und [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) rufen diese Methode während des Pinverbindungsprozesses auf.</span><span class="sxs-lookup"><span data-stu-id="6b201-114">The [**CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) and [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="6b201-115">Diese Methode führt in der Basisklasse nichts aus, aber die abgeleitete Klasse kann sie überschreiben.</span><span class="sxs-lookup"><span data-stu-id="6b201-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b201-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b201-116">Requirements</span></span>



| <span data-ttu-id="6b201-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b201-117">Requirement</span></span> | <span data-ttu-id="6b201-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6b201-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b201-119">Header</span><span class="sxs-lookup"><span data-stu-id="6b201-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6b201-120"><dt>Transfrm.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="6b201-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6b201-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b201-121">Library</span></span><br/> | <dl> <span data-ttu-id="6b201-122"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6b201-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b201-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6b201-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b201-124">**CTransformFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6b201-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




