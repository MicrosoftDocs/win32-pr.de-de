---
description: Die displaytypeinfo-Methode zeigt während des Debuggens Medientyp Informationen an.
ms.assetid: fd10d37b-57f5-4246-8ca3-f4bc59911445
title: Cbasepin. displaytypeinfo-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 681e424505bb2ff840ac5beaa48431f17a5d177b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361557"
---
# <a name="cbasepindisplaytypeinfo-method"></a><span data-ttu-id="d7828-103">Cbasepin. displaytypeinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="d7828-103">CBasePin.DisplayTypeInfo method</span></span>

<span data-ttu-id="d7828-104">Die- `DisplayTypeInfo` Methode zeigt während des Debuggens Medientyp Informationen an.</span><span class="sxs-lookup"><span data-stu-id="d7828-104">The `DisplayTypeInfo` method displays media type information during debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7828-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7828-105">Syntax</span></span>


```C++
void DisplayTypeInfo(
         IPin       *pPin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="d7828-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7828-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7828-107">*ppin*</span><span class="sxs-lookup"><span data-stu-id="d7828-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="d7828-108">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d7828-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="d7828-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="d7828-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="d7828-110">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="d7828-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7828-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7828-111">Return value</span></span>

<span data-ttu-id="d7828-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d7828-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7828-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7828-113">Remarks</span></span>

<span data-ttu-id="d7828-114">In Debugbuilds ruft diese Methode die [**dbglog**](dbglog.md) -Funktion auf, um den angegebenen Medientyp anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d7828-114">In debug builds, this method calls the [**DbgLog**](dbglog.md) function to display the specified media type.</span></span> <span data-ttu-id="d7828-115">Bei Einzelhandels Builds führt diese Methode keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="d7828-115">In retail builds, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7828-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7828-116">Requirements</span></span>



| <span data-ttu-id="d7828-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7828-117">Requirement</span></span> | <span data-ttu-id="d7828-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d7828-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7828-119">Header</span><span class="sxs-lookup"><span data-stu-id="d7828-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d7828-120"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7828-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d7828-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d7828-121">Library</span></span><br/> | <dl> <span data-ttu-id="d7828-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d7828-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7828-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7828-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7828-124">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d7828-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




