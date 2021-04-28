---
description: 'CTransformInputPin.CheckMediaType-Methode: Die CheckMediaType-Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.'
ms.assetid: e09a4a3e-ac39-4d0e-9e8c-3e8f18057d0d
title: CTransformInputPin.CheckMediaType-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c775618c9fe30de6171919d5b8bc8a80ea81d3a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084998"
---
# <a name="ctransforminputpincheckmediatype-method"></a><span data-ttu-id="2d478-103">CTransformInputPin.CheckMediaType-Methode</span><span class="sxs-lookup"><span data-stu-id="2d478-103">CTransformInputPin.CheckMediaType method</span></span>

<span data-ttu-id="2d478-104">Die `CheckMediaType` -Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="2d478-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d478-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d478-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="2d478-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d478-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d478-107">*Mtin*</span><span class="sxs-lookup"><span data-stu-id="2d478-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="2d478-108">Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den vorgeschlagenen Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="2d478-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d478-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d478-109">Return value</span></span>

<span data-ttu-id="2d478-110">Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="2d478-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d478-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d478-111">Remarks</span></span>

<span data-ttu-id="2d478-112">Diese Methode implementiert die rein virtuelle [**CBasePin::CheckMediaType-Methode.**](cbasepin-checkmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="2d478-112">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="2d478-113">Sie ruft die [**CTransformFilter::CheckInputType-Methode**](ctransformfilter-checkinputtype.md) des Filters auf, die ebenfalls rein virtuell ist.</span><span class="sxs-lookup"><span data-stu-id="2d478-113">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method, which is also pure virtual.</span></span> <span data-ttu-id="2d478-114">Die abgeleitete Klasse des Filters muss **CheckInputType** implementieren, um zu bestimmen, ob ein angegebener Eingabetyp akzeptabel ist.</span><span class="sxs-lookup"><span data-stu-id="2d478-114">The filter's derived class must implement **CheckInputType** to determine whether a given input type is acceptable.</span></span>

<span data-ttu-id="2d478-115">Wenn der Ausgabepin des Filters verbunden ist, ruft diese Methode auch die [**CTransformFilter::CheckTransform-Methode**](ctransformfilter-checktransform.md) des Filters auf, um zu bestimmen, ob der Eingabetyp mit dem Ausgabetyp kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="2d478-115">If the filter's output pin is connected, this method also calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method to determine whether the input type is compatible with the output type.</span></span> <span data-ttu-id="2d478-116">Die **CheckTransform-Methode** ist ebenfalls rein virtuell.</span><span class="sxs-lookup"><span data-stu-id="2d478-116">The **CheckTransform** method is pure virtual as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d478-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d478-117">Requirements</span></span>



| <span data-ttu-id="2d478-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d478-118">Requirement</span></span> | <span data-ttu-id="2d478-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2d478-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d478-120">Header</span><span class="sxs-lookup"><span data-stu-id="2d478-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2d478-121"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d478-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2d478-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2d478-122">Library</span></span><br/> | <dl> <span data-ttu-id="2d478-123"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2d478-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




