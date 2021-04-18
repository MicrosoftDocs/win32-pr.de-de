---
description: Die checkmediatype-Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.
ms.assetid: 9e31480b-129c-4741-846a-854c70c65606
title: Ctransformoutputpin. checkmediatype-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3c2bc617a5ff56a8b82184700af85e2634960ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365399"
---
# <a name="ctransformoutputpincheckmediatype-method"></a><span data-ttu-id="d9f0b-103">Ctransformoutputpin. checkmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="d9f0b-103">CTransformOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="d9f0b-104">Die- `CheckMediaType` Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9f0b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9f0b-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="d9f0b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9f0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9f0b-107">*MTiN*</span><span class="sxs-lookup"><span data-stu-id="d9f0b-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="d9f0b-108">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den vorgeschlagenen Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9f0b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9f0b-109">Return value</span></span>

<span data-ttu-id="d9f0b-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d9f0b-111">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-111">Possible values include the following.</span></span>



| <span data-ttu-id="d9f0b-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d9f0b-112">Return code</span></span>                                                                                  | <span data-ttu-id="d9f0b-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9f0b-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="d9f0b-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d9f0b-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d9f0b-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d9f0b-116"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="d9f0b-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d9f0b-117">Die Eingabe-PIN des Filters ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d9f0b-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9f0b-118">Remarks</span></span>

<span data-ttu-id="d9f0b-119">Diese Methode implementiert die rein virtuelle [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-119">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="d9f0b-120">Die Methode schlägt fehl, wenn die Eingabe-PIN des Filters nicht verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-120">The method fails if the filter's input pin is not connected.</span></span> <span data-ttu-id="d9f0b-121">Andernfalls wird die [**ctransformfilter:: checktransform**](ctransformfilter-checktransform.md) -Methode des Filters aufgerufen, die ebenfalls rein virtuell ist.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-121">Otherwise, it calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method, which is also pure virtual.</span></span> <span data-ttu-id="d9f0b-122">Die abgeleitete Klasse des Filters muss **checktransform** implementieren, das bestimmt, ob der vorgeschlagene Ausgabe Medientyp mit dem Eingabe Medientyp kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-122">The filter's derived class must implement **CheckTransform**, which determines if the proposed output media type is compatible with the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f0b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9f0b-123">Requirements</span></span>



| <span data-ttu-id="d9f0b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9f0b-124">Requirement</span></span> | <span data-ttu-id="d9f0b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="d9f0b-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f0b-126">Header</span><span class="sxs-lookup"><span data-stu-id="d9f0b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d9f0b-127"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9f0b-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d9f0b-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d9f0b-128">Library</span></span><br/> | <dl> <span data-ttu-id="d9f0b-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d9f0b-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




