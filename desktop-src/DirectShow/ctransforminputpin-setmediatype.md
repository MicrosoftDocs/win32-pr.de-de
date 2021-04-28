---
description: 'CTransformInputPin.SetMediaType-Methode: Die SetMediaType-Methode legt den Medientyp für die Verbindung fest.'
ms.assetid: 8e83380f-ba38-4fb8-ac32-40d68a4efea6
title: CTransformInputPin.SetMediaType-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9af7310dbbf8830d7469c1a72ae43b946f1fbc69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094998"
---
# <a name="ctransforminputpinsetmediatype-method"></a><span data-ttu-id="c22ac-103">CTransformInputPin.SetMediaType-Methode</span><span class="sxs-lookup"><span data-stu-id="c22ac-103">CTransformInputPin.SetMediaType method</span></span>

<span data-ttu-id="c22ac-104">Die `SetMediaType` -Methode legt den Medientyp für die Verbindung fest.</span><span class="sxs-lookup"><span data-stu-id="c22ac-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c22ac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c22ac-105">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a><span data-ttu-id="c22ac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c22ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c22ac-107">*Mt*</span><span class="sxs-lookup"><span data-stu-id="c22ac-107">*mt*</span></span> 
</dt> <dd>

<span data-ttu-id="c22ac-108">Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="c22ac-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c22ac-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c22ac-109">Return value</span></span>

<span data-ttu-id="c22ac-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="c22ac-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c22ac-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c22ac-111">Remarks</span></span>

<span data-ttu-id="c22ac-112">Diese Methode überschreibt die [**CBasePin::SetMediaType-Methode.**](cbasepin-setmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="c22ac-112">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span> <span data-ttu-id="c22ac-113">Sie ruft die [**CTransformFilter::SetMediaType-Methode**](ctransformfilter-setmediatype.md) des Filters auf, um den Filter zu informieren.</span><span class="sxs-lookup"><span data-stu-id="c22ac-113">It calls the filter's [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) method to inform the filter.</span></span>

<span data-ttu-id="c22ac-114">Der Pin muss überprüfen, ob der Medientyp akzeptabel ist, bevor diese Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c22ac-114">The pin must verify that the media type is acceptable before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c22ac-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c22ac-115">Requirements</span></span>



| <span data-ttu-id="c22ac-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c22ac-116">Requirement</span></span> | <span data-ttu-id="c22ac-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c22ac-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c22ac-118">Header</span><span class="sxs-lookup"><span data-stu-id="c22ac-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c22ac-119"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c22ac-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c22ac-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c22ac-120">Library</span></span><br/> | <dl> <span data-ttu-id="c22ac-121"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c22ac-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




