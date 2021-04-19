---
description: 'Die enummediatypes-Methode listet die bevorzugten Medientypen der PIN auf. Diese Methode implementiert die IPin:: enummediatypes-Methode.'
ms.assetid: 0c28b4b0-a45f-400f-a6d7-7668458f9642
title: Ctransinplaceinputpin. enummediatypes-Methode (transip. h)
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
ms.openlocfilehash: ffa634fa695eb0007b49fc1c36c730c7fbde361b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365984"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a><span data-ttu-id="027d7-104">Ctransinplaceinputpin. enummediatypes-Methode</span><span class="sxs-lookup"><span data-stu-id="027d7-104">CTransInPlaceInputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="027d7-105">Die `EnumMediaTypes` -Methode listet die bevorzugten Medientypen der PIN auf.</span><span class="sxs-lookup"><span data-stu-id="027d7-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="027d7-106">Diese Methode implementiert die [**IPin:: enummediatypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) -Methode.</span><span class="sxs-lookup"><span data-stu-id="027d7-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="027d7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="027d7-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="027d7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="027d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="027d7-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="027d7-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="027d7-110">Empfängt einen Zeiger auf die [**ienummediatypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="027d7-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="027d7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="027d7-111">Return value</span></span>

<span data-ttu-id="027d7-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="027d7-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="027d7-113">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="027d7-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="027d7-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="027d7-114">Return code</span></span>                                                                                           | <span data-ttu-id="027d7-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="027d7-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="027d7-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="027d7-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="027d7-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="027d7-117">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="027d7-118"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="027d7-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="027d7-119">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="027d7-119">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="027d7-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="027d7-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="027d7-121">**Null** -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="027d7-121">**NULL** pointer.</span></span><br/>                |
| <dl> <span data-ttu-id="027d7-122"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="027d7-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="027d7-123">Die Ausgabe-PIN ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="027d7-123">The output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="027d7-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="027d7-124">Remarks</span></span>

<span data-ttu-id="027d7-125">Diese Methode gibt die **ienummediatypes** -Schnittstelle von der Downstream-Eingabe-PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="027d7-125">This method returns the **IEnumMediaTypes** interface from downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="027d7-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="027d7-126">Requirements</span></span>



| <span data-ttu-id="027d7-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="027d7-127">Requirement</span></span> | <span data-ttu-id="027d7-128">Wert</span><span class="sxs-lookup"><span data-stu-id="027d7-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="027d7-129">Header</span><span class="sxs-lookup"><span data-stu-id="027d7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="027d7-130"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="027d7-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="027d7-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="027d7-131">Library</span></span><br/> | <dl> <span data-ttu-id="027d7-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="027d7-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="027d7-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="027d7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="027d7-134">**Ctransinplaceinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="027d7-134">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




