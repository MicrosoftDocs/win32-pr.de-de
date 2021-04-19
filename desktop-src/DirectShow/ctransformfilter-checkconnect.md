---
description: Die checkConnect-Methode bestimmt, ob eine PIN-Verbindung geeignet ist.
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: Ctransformfilter. checkConnect-Methode (Transfrm. h)
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
ms.openlocfilehash: 0d41c50323bae7cb4eaca52a87d8c1b936237ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370597"
---
# <a name="ctransformfiltercheckconnect-method"></a><span data-ttu-id="19a1c-103">Ctransformfilter. checkConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="19a1c-103">CTransformFilter.CheckConnect method</span></span>

<span data-ttu-id="19a1c-104">Die- `CheckConnect` Methode bestimmt, ob eine PIN-Verbindung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="19a1c-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="19a1c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="19a1c-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="19a1c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="19a1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19a1c-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="19a1c-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="19a1c-108">Member des enumerierten Typs der [**Pin- \_ Richtung**](/windows/win32/api/strmif/ne-strmif-pin_direction) , der angibt, welche PIN im Filter die Verbindung herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="19a1c-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="19a1c-109">*ppin*</span><span class="sxs-lookup"><span data-stu-id="19a1c-109">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="19a1c-110">Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der anderen PIN bei diesem Verbindungsversuch.</span><span class="sxs-lookup"><span data-stu-id="19a1c-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19a1c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19a1c-111">Return value</span></span>

<span data-ttu-id="19a1c-112">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="19a1c-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="19a1c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19a1c-113">Remarks</span></span>

<span data-ttu-id="19a1c-114">Die [**ctransforminputpin:: checkConnect**](ctransforminputpin-checkconnect.md) -Methode und die [**ctransformoutputpin:: checkConnect**](ctransformoutputpin-checkconnect.md) -Methode ruft diese Methode während des PIN-Verbindungsprozesses auf.</span><span class="sxs-lookup"><span data-stu-id="19a1c-114">The [**CTransformInputPin::CheckConnect**](ctransforminputpin-checkconnect.md) and [**CTransformOutputPin::CheckConnect**](ctransformoutputpin-checkconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="19a1c-115">Diese Methode führt in der Basisklasse keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="19a1c-115">This method does nothing in the base class.</span></span> <span data-ttu-id="19a1c-116">Diese kann von der abgeleiteten Klasse überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="19a1c-116">The derived class can override it.</span></span> <span data-ttu-id="19a1c-117">Beispielsweise kann die abgeleitete Klasse die andere PIN für eine bestimmte Schnittstelle Abfragen.</span><span class="sxs-lookup"><span data-stu-id="19a1c-117">For example, the derived class might query the other pin for a particular interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="19a1c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19a1c-118">Requirements</span></span>



| <span data-ttu-id="19a1c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19a1c-119">Requirement</span></span> | <span data-ttu-id="19a1c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="19a1c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19a1c-121">Header</span><span class="sxs-lookup"><span data-stu-id="19a1c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="19a1c-122"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19a1c-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="19a1c-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="19a1c-123">Library</span></span><br/> | <dl> <span data-ttu-id="19a1c-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="19a1c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19a1c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19a1c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19a1c-126">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="19a1c-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




