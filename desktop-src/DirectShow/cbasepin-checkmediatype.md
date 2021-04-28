---
description: 'CBasePin.CheckMediaType-Methode: Die CheckMediaType-Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.'
ms.assetid: 6a138679-02b7-4ccc-8881-a0d496f84f93
title: CBasePin.CheckMediaType-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afe39f3a7aac155f3cc87fa6d58f402043861d1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099397"
---
# <a name="cbasepincheckmediatype-method"></a><span data-ttu-id="4e70e-103">CBasePin.CheckMediaType-Methode</span><span class="sxs-lookup"><span data-stu-id="4e70e-103">CBasePin.CheckMediaType method</span></span>

<span data-ttu-id="4e70e-104">Die `CheckMediaType` -Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="4e70e-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e70e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e70e-105">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="4e70e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e70e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e70e-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="4e70e-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="4e70e-108">Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den vorgeschlagenen Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="4e70e-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e70e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e70e-109">Return value</span></span>

<span data-ttu-id="4e70e-110">Gibt S \_ OK zurück, wenn der vorgeschlagene Medientyp akzeptabel ist.</span><span class="sxs-lookup"><span data-stu-id="4e70e-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="4e70e-111">Andernfalls wird S \_ FALSE oder ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4e70e-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e70e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e70e-112">Remarks</span></span>

<span data-ttu-id="4e70e-113">Die abgeleitete Klasse muss diese rein virtuelle Methode überschreiben.</span><span class="sxs-lookup"><span data-stu-id="4e70e-113">The derived class must override this pure virtual method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e70e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e70e-114">Requirements</span></span>



| <span data-ttu-id="4e70e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e70e-115">Requirement</span></span> | <span data-ttu-id="4e70e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4e70e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e70e-117">Header</span><span class="sxs-lookup"><span data-stu-id="4e70e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4e70e-118"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="4e70e-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4e70e-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4e70e-119">Library</span></span><br/> | <dl> <span data-ttu-id="4e70e-120"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4e70e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e70e-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4e70e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e70e-122">**CBasePin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4e70e-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




