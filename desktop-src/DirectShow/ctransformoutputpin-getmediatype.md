---
description: 'CTransformOutputPin.GetMediaType-Methode: Die GetMediaType-Methode ruft einen bevorzugten Medientyp nach Indexwert ab.'
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: CTransformOutputPin.GetMediaType-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dd0bf38f2fa3be0e077f2509001680bbfc84e15
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094898"
---
# <a name="ctransformoutputpingetmediatype-method"></a><span data-ttu-id="63d84-103">CTransformOutputPin.GetMediaType-Methode</span><span class="sxs-lookup"><span data-stu-id="63d84-103">CTransformOutputPin.GetMediaType method</span></span>

<span data-ttu-id="63d84-104">Die `GetMediaType` -Methode ruft einen bevorzugten Medientyp nach Indexwert ab.</span><span class="sxs-lookup"><span data-stu-id="63d84-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="63d84-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="63d84-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="63d84-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="63d84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63d84-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="63d84-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="63d84-108">Nullbasierter Indexwert.</span><span class="sxs-lookup"><span data-stu-id="63d84-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="63d84-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="63d84-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="63d84-110">Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp empfängt.</span><span class="sxs-lookup"><span data-stu-id="63d84-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63d84-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63d84-111">Return value</span></span>

<span data-ttu-id="63d84-112">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="63d84-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="63d84-113">Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.</span><span class="sxs-lookup"><span data-stu-id="63d84-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="63d84-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="63d84-114">Return code</span></span>                                                                                            | <span data-ttu-id="63d84-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63d84-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="63d84-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="63d84-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="63d84-117">Erfolg</span><span class="sxs-lookup"><span data-stu-id="63d84-117">Success</span></span><br/>            |
| <dl> <span data-ttu-id="63d84-118"><dt>**VFW \_ S KEINE ELEMENTE \_ \_ \_ MEHR**</dt></span><span class="sxs-lookup"><span data-stu-id="63d84-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="63d84-119">Index liegt nicht im Bereich</span><span class="sxs-lookup"><span data-stu-id="63d84-119">Index out of range</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="63d84-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63d84-120">Remarks</span></span>

<span data-ttu-id="63d84-121">Diese Methode überschreibt die [**CBasePin::GetMediaType-Methode.**](cbasepin-getmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="63d84-121">This method overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method.</span></span> <span data-ttu-id="63d84-122">Wenn der Eingabepin des Filters nicht verbunden ist, gibt die Methode VFW \_ S NO MORE ITEMS \_ \_ \_ zurück.</span><span class="sxs-lookup"><span data-stu-id="63d84-122">If the filter's input pin is not connected, the method returns VFW\_S\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="63d84-123">Andernfalls wird die [**CTransformFilter::GetMediaType-Methode**](ctransformfilter-getmediatype.md) des Filters aufgerufen, um den Medientyp abzurufen.</span><span class="sxs-lookup"><span data-stu-id="63d84-123">Otherwise, it calls the filter's [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method to retrieve the media type.</span></span> <span data-ttu-id="63d84-124">Die **CTransformFilter::GetMediaType-Methode** ist rein virtuell. Die abgeleitete Klasse des Filters muss sie überschreiben.</span><span class="sxs-lookup"><span data-stu-id="63d84-124">The **CTransformFilter::GetMediaType** method is pure virtual; the filter's derived class must override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="63d84-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63d84-125">Requirements</span></span>



| <span data-ttu-id="63d84-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63d84-126">Requirement</span></span> | <span data-ttu-id="63d84-127">Wert</span><span class="sxs-lookup"><span data-stu-id="63d84-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63d84-128">Header</span><span class="sxs-lookup"><span data-stu-id="63d84-128">Header</span></span><br/>  | <dl> <span data-ttu-id="63d84-129"><dt>Transfrm.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="63d84-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="63d84-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="63d84-130">Library</span></span><br/> | <dl> <span data-ttu-id="63d84-131"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="63d84-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




