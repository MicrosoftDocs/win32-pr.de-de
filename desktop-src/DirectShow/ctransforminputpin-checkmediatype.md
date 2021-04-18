---
description: Die checkmediatype-Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.
ms.assetid: e09a4a3e-ac39-4d0e-9e8c-3e8f18057d0d
title: Ctransforminputpin. checkmediatype-Methode (Transfrm. h)
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
ms.openlocfilehash: 6841370795a3131cdbcc95a3bab160be2011c600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368453"
---
# <a name="ctransforminputpincheckmediatype-method"></a><span data-ttu-id="39668-103">Ctransforminputpin. checkmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="39668-103">CTransformInputPin.CheckMediaType method</span></span>

<span data-ttu-id="39668-104">Die- `CheckMediaType` Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="39668-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="39668-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="39668-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="39668-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="39668-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39668-107">*MTiN*</span><span class="sxs-lookup"><span data-stu-id="39668-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="39668-108">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den vorgeschlagenen Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="39668-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39668-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39668-109">Return value</span></span>

<span data-ttu-id="39668-110">Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="39668-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39668-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39668-111">Remarks</span></span>

<span data-ttu-id="39668-112">Diese Methode implementiert die rein virtuelle [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="39668-112">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="39668-113">Dabei wird die [**ctransformfilter:: checkinputtype**](ctransformfilter-checkinputtype.md) -Methode des Filters aufgerufen, die ebenfalls rein virtuell ist.</span><span class="sxs-lookup"><span data-stu-id="39668-113">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method, which is also pure virtual.</span></span> <span data-ttu-id="39668-114">Die abgeleitete Klasse des Filters muss **checkinputtype** implementieren, um zu bestimmen, ob ein bestimmter Eingabetyp zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="39668-114">The filter's derived class must implement **CheckInputType** to determine whether a given input type is acceptable.</span></span>

<span data-ttu-id="39668-115">Wenn die Ausgabe-PIN des Filters verbunden ist, ruft diese Methode auch die [**ctransformfilter:: checktransform**](ctransformfilter-checktransform.md) -Methode des Filters auf, um zu bestimmen, ob der Eingabetyp mit dem Ausgabetyp kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="39668-115">If the filter's output pin is connected, this method also calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method to determine whether the input type is compatible with the output type.</span></span> <span data-ttu-id="39668-116">Die **checktransform** -Methode ist auch rein virtuell.</span><span class="sxs-lookup"><span data-stu-id="39668-116">The **CheckTransform** method is pure virtual as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="39668-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39668-117">Requirements</span></span>



| <span data-ttu-id="39668-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39668-118">Requirement</span></span> | <span data-ttu-id="39668-119">Wert</span><span class="sxs-lookup"><span data-stu-id="39668-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39668-120">Header</span><span class="sxs-lookup"><span data-stu-id="39668-120">Header</span></span><br/>  | <dl> <span data-ttu-id="39668-121"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39668-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="39668-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="39668-122">Library</span></span><br/> | <dl> <span data-ttu-id="39668-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="39668-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




