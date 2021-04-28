---
description: 'CTransInPlaceInputPin.EnumMediaTypes-Methode: Die EnumMediaTypes-Methode aufzählt die bevorzugten Medientypen des Pins. Diese Methode implementiert die IPin::EnumMediaTypes-Methode.'
ms.assetid: 0c28b4b0-a45f-400f-a6d7-7668458f9642
title: CTransInPlaceInputPin.EnumMediaTypes-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f9e05d0e9db50cabc700da7b3803c1606efab78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094758"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a><span data-ttu-id="ce919-104">CTransInPlaceInputPin.EnumMediaTypes-Methode</span><span class="sxs-lookup"><span data-stu-id="ce919-104">CTransInPlaceInputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="ce919-105">Die `EnumMediaTypes` -Methode aufzählt die bevorzugten Medientypen des Pins.</span><span class="sxs-lookup"><span data-stu-id="ce919-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="ce919-106">Diese Methode implementiert die [**IPin::EnumMediaTypes-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)</span><span class="sxs-lookup"><span data-stu-id="ce919-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce919-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce919-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="ce919-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce919-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce919-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="ce919-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="ce919-110">Empfängt einen Zeiger auf die [**IEnumMediaTypes-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)</span><span class="sxs-lookup"><span data-stu-id="ce919-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce919-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce919-111">Return value</span></span>

<span data-ttu-id="ce919-112">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="ce919-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ce919-113">Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.</span><span class="sxs-lookup"><span data-stu-id="ce919-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="ce919-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ce919-114">Return code</span></span>                                                                                           | <span data-ttu-id="ce919-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce919-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="ce919-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ce919-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="ce919-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="ce919-117">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="ce919-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ce919-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="ce919-119">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ce919-119">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="ce919-120"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="ce919-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="ce919-121">**NULL-Zeiger.**</span><span class="sxs-lookup"><span data-stu-id="ce919-121">**NULL** pointer.</span></span><br/>                |
| <dl> <span data-ttu-id="ce919-122"><dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="ce919-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="ce919-123">Der Ausgabepin ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="ce919-123">The output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ce919-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce919-124">Remarks</span></span>

<span data-ttu-id="ce919-125">Diese Methode gibt die **IEnumMediaTypes-Schnittstelle** vom Downstreameingabepin zurück.</span><span class="sxs-lookup"><span data-stu-id="ce919-125">This method returns the **IEnumMediaTypes** interface from downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce919-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce919-126">Requirements</span></span>



| <span data-ttu-id="ce919-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce919-127">Requirement</span></span> | <span data-ttu-id="ce919-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ce919-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce919-129">Header</span><span class="sxs-lookup"><span data-stu-id="ce919-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ce919-130"><dt>Transip.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce919-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ce919-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ce919-131">Library</span></span><br/> | <dl> <span data-ttu-id="ce919-132"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ce919-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce919-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ce919-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce919-134">**CTransInPlaceInputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ce919-134">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




