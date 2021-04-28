---
description: 'CTransformOutputPin.CheckMediaType-Methode: Die CheckMediaType-Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.'
ms.assetid: 9e31480b-129c-4741-846a-854c70c65606
title: CTransformOutputPin.CheckMediaType-Methode (Transfrm.h)
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
ms.openlocfilehash: 7dc0edc642687518979eab1d47c69af039bc3173
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084908"
---
# <a name="ctransformoutputpincheckmediatype-method"></a><span data-ttu-id="661f9-103">CTransformOutputPin.CheckMediaType-Methode</span><span class="sxs-lookup"><span data-stu-id="661f9-103">CTransformOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="661f9-104">Die `CheckMediaType` -Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="661f9-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="661f9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="661f9-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="661f9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="661f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="661f9-107">*Mtin*</span><span class="sxs-lookup"><span data-stu-id="661f9-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="661f9-108">Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den vorgeschlagenen Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="661f9-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="661f9-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="661f9-109">Return value</span></span>

<span data-ttu-id="661f9-110">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="661f9-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="661f9-111">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="661f9-111">Possible values include the following.</span></span>



| <span data-ttu-id="661f9-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="661f9-112">Return code</span></span>                                                                                  | <span data-ttu-id="661f9-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="661f9-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="661f9-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="661f9-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="661f9-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="661f9-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="661f9-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="661f9-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="661f9-117">Der Eingabepin des Filters ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="661f9-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="661f9-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="661f9-118">Remarks</span></span>

<span data-ttu-id="661f9-119">Diese Methode implementiert die rein virtuelle [**CBasePin::CheckMediaType-Methode.**](cbasepin-checkmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="661f9-119">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="661f9-120">Die Methode schlägt fehl, wenn der Eingabepin des Filters nicht verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="661f9-120">The method fails if the filter's input pin is not connected.</span></span> <span data-ttu-id="661f9-121">Andernfalls wird die [**CTransformFilter::CheckTransform-Methode**](ctransformfilter-checktransform.md) des Filters aufgerufen, die ebenfalls rein virtuell ist.</span><span class="sxs-lookup"><span data-stu-id="661f9-121">Otherwise, it calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method, which is also pure virtual.</span></span> <span data-ttu-id="661f9-122">Die abgeleitete Klasse des Filters muss **CheckTransform** implementieren, wodurch bestimmt wird, ob der vorgeschlagene Ausgabemedientyp mit dem Eingabemedientyp kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="661f9-122">The filter's derived class must implement **CheckTransform**, which determines if the proposed output media type is compatible with the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="661f9-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="661f9-123">Requirements</span></span>



| <span data-ttu-id="661f9-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="661f9-124">Requirement</span></span> | <span data-ttu-id="661f9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="661f9-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="661f9-126">Header</span><span class="sxs-lookup"><span data-stu-id="661f9-126">Header</span></span><br/>  | <dl> <span data-ttu-id="661f9-127"><dt>Transfrm.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="661f9-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="661f9-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="661f9-128">Library</span></span><br/> | <dl> <span data-ttu-id="661f9-129"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="661f9-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




