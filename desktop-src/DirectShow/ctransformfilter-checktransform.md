---
description: Die checktransform-Methode überprüft, ob ein Eingabe Medientyp mit einem Ausgabe Medientyp kompatibel ist.
ms.assetid: 349145e5-c12d-41df-ae37-7846f8aaa423
title: Ctransformfilter. checktransform-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b3302304e6a0f9df41005f7ed63d9316a3cd410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368475"
---
# <a name="ctransformfilterchecktransform-method"></a><span data-ttu-id="f23eb-103">Ctransformfilter. checktransform-Methode</span><span class="sxs-lookup"><span data-stu-id="f23eb-103">CTransformFilter.CheckTransform method</span></span>

<span data-ttu-id="f23eb-104">Die- `CheckTransform` Methode überprüft, ob ein Eingabe Medientyp mit einem Ausgabe Medientyp kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="f23eb-104">The `CheckTransform` method checks whether an input media type is compatible with an output media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f23eb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f23eb-105">Syntax</span></span>


```C++
virtual HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="f23eb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f23eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f23eb-107">*MTiN*</span><span class="sxs-lookup"><span data-stu-id="f23eb-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="f23eb-108">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Eingabetyp angibt.</span><span class="sxs-lookup"><span data-stu-id="f23eb-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the input type.</span></span>

</dd> <dt>

<span data-ttu-id="f23eb-109">*mtout*</span><span class="sxs-lookup"><span data-stu-id="f23eb-109">*mtOut*</span></span> 
</dt> <dd>

<span data-ttu-id="f23eb-110">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Ausgabetyp angibt.</span><span class="sxs-lookup"><span data-stu-id="f23eb-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the output type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f23eb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f23eb-111">Return value</span></span>

<span data-ttu-id="f23eb-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f23eb-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f23eb-113">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f23eb-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="f23eb-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f23eb-114">Return code</span></span>                                                                                                | <span data-ttu-id="f23eb-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f23eb-115">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="f23eb-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f23eb-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="f23eb-117">Die Medientypen sind kompatibel.</span><span class="sxs-lookup"><span data-stu-id="f23eb-117">The media types are compatible.</span></span><br/>     |
| <dl> <span data-ttu-id="f23eb-118"><dt>**VFW \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt></span><span class="sxs-lookup"><span data-stu-id="f23eb-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="f23eb-119">Die Medientypen sind nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="f23eb-119">The media types are not compatible.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f23eb-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f23eb-120">Remarks</span></span>

<span data-ttu-id="f23eb-121">Diese Methode muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f23eb-121">The derived class must implement this method.</span></span> <span data-ttu-id="f23eb-122">Gibt \_ OK zurück, wenn der Filter beide angegebenen Medientypen akzeptieren kann, andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f23eb-122">Return S\_OK if the filter can accept both of the specified media types, or an error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f23eb-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f23eb-123">Requirements</span></span>



| <span data-ttu-id="f23eb-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f23eb-124">Requirement</span></span> | <span data-ttu-id="f23eb-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f23eb-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f23eb-126">Header</span><span class="sxs-lookup"><span data-stu-id="f23eb-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f23eb-127"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f23eb-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f23eb-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f23eb-128">Library</span></span><br/> | <dl> <span data-ttu-id="f23eb-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f23eb-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




