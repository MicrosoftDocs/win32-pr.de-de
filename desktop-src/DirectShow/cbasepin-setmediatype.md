---
description: 'CBasePin.SetMediaType-Methode: Die SetMediaType-Methode legt den Medientyp für die Verbindung fest.'
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: CBasePin.SetMediaType-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b61b6179aa6364ebddd940b8853e22d628463e56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095987"
---
# <a name="cbasepinsetmediatype-method"></a><span data-ttu-id="a9c9c-103">CBasePin.SetMediaType-Methode</span><span class="sxs-lookup"><span data-stu-id="a9c9c-103">CBasePin.SetMediaType method</span></span>

<span data-ttu-id="a9c9c-104">Die `SetMediaType` -Methode legt den Medientyp für die Verbindung fest.</span><span class="sxs-lookup"><span data-stu-id="a9c9c-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9c9c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9c9c-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="a9c9c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9c9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9c9c-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="a9c9c-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="a9c9c-108">Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="a9c9c-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9c9c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9c9c-109">Return value</span></span>

<span data-ttu-id="a9c9c-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="a9c9c-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9c9c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9c9c-111">Remarks</span></span>

<span data-ttu-id="a9c9c-112">Diese Methode legt das Format für eine Stecknadelverbindung fest.</span><span class="sxs-lookup"><span data-stu-id="a9c9c-112">This method establishes the format for a pin connection.</span></span> <span data-ttu-id="a9c9c-113">Vor dem Aufrufen dieser Methode ruft der Pin die [**CBasePin::CheckMediaType-Methode**](cbasepin-checkmediatype.md) auf, um zu bestimmen, ob der Medientyp akzeptabel ist.</span><span class="sxs-lookup"><span data-stu-id="a9c9c-113">Before calling this method, the pin calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the media type is acceptable.</span></span> <span data-ttu-id="a9c9c-114">Daher wird angenommen, dass der *pmt-Parameter* ein zulässiger Medientyp ist.</span><span class="sxs-lookup"><span data-stu-id="a9c9c-114">Therefore, the *pmt* parameter is assumed to be an acceptable media type.</span></span>

<span data-ttu-id="a9c9c-115">In der Basisklasse legt diese Methode die [**CBasePin::m \_ mt-Membervariable**](cbasepin-m-mt.md) fest und gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="a9c9c-115">In the base class, this method sets the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable and returns S\_OK.</span></span> <span data-ttu-id="a9c9c-116">Eine abgeleitete Klasse kann diese Methode überschreiben, wenn sie eine Benachrichtigung erfordert, wenn der Medientyp festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a9c9c-116">A derived class can override this method if it requires notification when the media type is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9c9c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9c9c-117">Requirements</span></span>



| <span data-ttu-id="a9c9c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9c9c-118">Requirement</span></span> | <span data-ttu-id="a9c9c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a9c9c-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9c9c-120">Header</span><span class="sxs-lookup"><span data-stu-id="a9c9c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a9c9c-121"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="a9c9c-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a9c9c-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a9c9c-122">Library</span></span><br/> | <dl> <span data-ttu-id="a9c9c-123"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a9c9c-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9c9c-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a9c9c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9c9c-125">**CBasePin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a9c9c-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




