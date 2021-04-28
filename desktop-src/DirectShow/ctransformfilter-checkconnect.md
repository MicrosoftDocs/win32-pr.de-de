---
description: 'CTransformFilter.CheckConnect-Methode: Die CheckConnect-Methode bestimmt, ob eine Pinverbindung geeignet ist.'
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: CTransformFilter.CheckConnect-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5927aac2fa58322c93a23489a22dc96a1e2a67f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085098"
---
# <a name="ctransformfiltercheckconnect-method"></a><span data-ttu-id="23918-103">CTransformFilter.CheckConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="23918-103">CTransformFilter.CheckConnect method</span></span>

<span data-ttu-id="23918-104">Die `CheckConnect` -Methode bestimmt, ob eine Stecknadelverbindung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="23918-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="23918-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="23918-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="23918-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="23918-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23918-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="23918-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="23918-108">Member des [**PIN DIRECTION-Enumerationstyps, \_**](/windows/win32/api/strmif/ne-strmif-pin_direction) der angibt, welcher Pin auf dem Filter die Verbindung herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="23918-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="23918-109">*pPin*</span><span class="sxs-lookup"><span data-stu-id="23918-109">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="23918-110">Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des anderen Pins in diesem Verbindungsversuch.</span><span class="sxs-lookup"><span data-stu-id="23918-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23918-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="23918-111">Return value</span></span>

<span data-ttu-id="23918-112">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="23918-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="23918-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23918-113">Remarks</span></span>

<span data-ttu-id="23918-114">Die Methoden [**CTransformInputPin::CheckConnect**](ctransforminputpin-checkconnect.md) und [**CTransformOutputPin::CheckConnect**](ctransformoutputpin-checkconnect.md) rufen diese Methode während des Pinverbindungsprozesses auf.</span><span class="sxs-lookup"><span data-stu-id="23918-114">The [**CTransformInputPin::CheckConnect**](ctransforminputpin-checkconnect.md) and [**CTransformOutputPin::CheckConnect**](ctransformoutputpin-checkconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="23918-115">Diese Methode führt in der Basisklasse nichts aus.</span><span class="sxs-lookup"><span data-stu-id="23918-115">This method does nothing in the base class.</span></span> <span data-ttu-id="23918-116">Die abgeleitete Klasse kann sie überschreiben.</span><span class="sxs-lookup"><span data-stu-id="23918-116">The derived class can override it.</span></span> <span data-ttu-id="23918-117">Beispielsweise kann die abgeleitete Klasse den anderen Pin nach einer bestimmten Schnittstelle abfragen.</span><span class="sxs-lookup"><span data-stu-id="23918-117">For example, the derived class might query the other pin for a particular interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="23918-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23918-118">Requirements</span></span>



| <span data-ttu-id="23918-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23918-119">Requirement</span></span> | <span data-ttu-id="23918-120">Wert</span><span class="sxs-lookup"><span data-stu-id="23918-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23918-121">Header</span><span class="sxs-lookup"><span data-stu-id="23918-121">Header</span></span><br/>  | <dl> <span data-ttu-id="23918-122"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="23918-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="23918-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="23918-123">Library</span></span><br/> | <dl> <span data-ttu-id="23918-124"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="23918-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23918-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="23918-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23918-126">**CTransformFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="23918-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




