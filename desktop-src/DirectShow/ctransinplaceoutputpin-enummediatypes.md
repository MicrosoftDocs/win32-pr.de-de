---
description: 'CTransInPlaceOutputPin.EnumMediaTypes-Methode: Die EnumMediaTypes-Methode aufzählt die bevorzugten Medientypen des Pins. Diese Methode implementiert die IPin::EnumMediaTypes-Methode.'
ms.assetid: 942c6594-3053-484a-a0f7-286dcd3f7550
title: CTransInPlaceOutputPin.EnumMediaTypes-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26dd58f23dc18a086c6c59f6f8a6a098e3449fea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084634"
---
# <a name="ctransinplaceoutputpinenummediatypes-method"></a><span data-ttu-id="08f66-104">CTransInPlaceOutputPin.EnumMediaTypes-Methode</span><span class="sxs-lookup"><span data-stu-id="08f66-104">CTransInPlaceOutputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="08f66-105">Die `EnumMediaTypes` -Methode aufzählt die bevorzugten Medientypen des Pins.</span><span class="sxs-lookup"><span data-stu-id="08f66-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="08f66-106">Diese Methode implementiert die [**IPin::EnumMediaTypes-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)</span><span class="sxs-lookup"><span data-stu-id="08f66-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="08f66-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="08f66-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="08f66-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="08f66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08f66-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="08f66-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="08f66-110">Empfängt einen Zeiger auf die [**IEnumMediaTypes-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)</span><span class="sxs-lookup"><span data-stu-id="08f66-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08f66-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08f66-111">Return value</span></span>

<span data-ttu-id="08f66-112">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="08f66-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="08f66-113">Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.</span><span class="sxs-lookup"><span data-stu-id="08f66-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="08f66-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="08f66-114">Return code</span></span>                                                                                           | <span data-ttu-id="08f66-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08f66-115">Description</span></span>                                         |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="08f66-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="08f66-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="08f66-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="08f66-117">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="08f66-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="08f66-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="08f66-119">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="08f66-119">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="08f66-120"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="08f66-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="08f66-121">**NULL-Zeiger.**</span><span class="sxs-lookup"><span data-stu-id="08f66-121">**NULL** pointer.</span></span><br/>                        |
| <dl> <span data-ttu-id="08f66-122"><dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="08f66-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="08f66-123">Der Eingabepin des Filters ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="08f66-123">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="08f66-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08f66-124">Remarks</span></span>

<span data-ttu-id="08f66-125">Diese Methode gibt die **IEnumMediaTypes-Schnittstelle** vom Upstreamausgabepin zurück.</span><span class="sxs-lookup"><span data-stu-id="08f66-125">This method returns the **IEnumMediaTypes** interface from the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="08f66-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08f66-126">Requirements</span></span>



| <span data-ttu-id="08f66-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08f66-127">Requirement</span></span> | <span data-ttu-id="08f66-128">Wert</span><span class="sxs-lookup"><span data-stu-id="08f66-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08f66-129">Header</span><span class="sxs-lookup"><span data-stu-id="08f66-129">Header</span></span><br/>  | <dl> <span data-ttu-id="08f66-130"><dt>Transip.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="08f66-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="08f66-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="08f66-131">Library</span></span><br/> | <dl> <span data-ttu-id="08f66-132"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="08f66-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08f66-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="08f66-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08f66-134">**CTransInPlaceOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="08f66-134">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




