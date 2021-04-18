---
description: 'Die getallocatorrequirements-Methode ruft die von der PIN angeforderten zuordnereigenschaften ab. Diese Methode implementiert die IMemInputPin:: getallo. Requirements-Methode.'
ms.assetid: 1355facc-f863-44b2-9284-8f06f62d39a2
title: Ctransinplaceinputpin. getallocatorrequirements-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa176cd5da0317821996593e19bb90396e82224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365556"
---
# <a name="ctransinplaceinputpingetallocatorrequirements-method"></a><span data-ttu-id="27e6c-104">Ctransinplaceinputpin. getalloerrequirements-Methode</span><span class="sxs-lookup"><span data-stu-id="27e6c-104">CTransInPlaceInputPin.GetAllocatorRequirements method</span></span>

<span data-ttu-id="27e6c-105">Die- `GetAllocatorRequirements` Methode ruft die von der PIN angeforderten zuordnereigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="27e6c-105">The `GetAllocatorRequirements` method retrieves the allocator properties requested by the pin.</span></span> <span data-ttu-id="27e6c-106">Diese Methode implementiert die [**IMemInputPin:: getallo. Requirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) -Methode.</span><span class="sxs-lookup"><span data-stu-id="27e6c-106">This method implements the [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="27e6c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="27e6c-107">Syntax</span></span>


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="27e6c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="27e6c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27e6c-109">*p-Eigenschaften*</span><span class="sxs-lookup"><span data-stu-id="27e6c-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="27e6c-110">Zeiger auf eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die mit den Anforderungen ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="27e6c-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure, which is filled in with the requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27e6c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27e6c-111">Return value</span></span>

<span data-ttu-id="27e6c-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="27e6c-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="27e6c-113">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="27e6c-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="27e6c-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="27e6c-114">Return code</span></span>                                                                               | <span data-ttu-id="27e6c-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27e6c-115">Description</span></span>                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="27e6c-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="27e6c-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="27e6c-117">Erfolg</span><span class="sxs-lookup"><span data-stu-id="27e6c-117">Success</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="27e6c-118"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="27e6c-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="27e6c-119">Die Ausgabe-PIN ist nicht verbunden, oder die downstreameingabepin unterstützt die-Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="27e6c-119">The output pin is not connected, or the downstream input pin does not support the method.</span></span><br/> |
| <dl> <span data-ttu-id="27e6c-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="27e6c-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="27e6c-121">**Null** -Zeigerargument</span><span class="sxs-lookup"><span data-stu-id="27e6c-121">**NULL** pointer argument</span></span><br/>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="27e6c-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27e6c-122">Remarks</span></span>

<span data-ttu-id="27e6c-123">Wenn die Ausgabe-PIN verbunden ist, übergibt diese Methode den-Befehl an die downstreameingabepin.</span><span class="sxs-lookup"><span data-stu-id="27e6c-123">If the output pin is connected, this method passes the call to the downstream input pin.</span></span> <span data-ttu-id="27e6c-124">Andernfalls wird E \_ notimpl zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="27e6c-124">Otherwise, it returns E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="27e6c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27e6c-125">Requirements</span></span>



| <span data-ttu-id="27e6c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27e6c-126">Requirement</span></span> | <span data-ttu-id="27e6c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="27e6c-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27e6c-128">Header</span><span class="sxs-lookup"><span data-stu-id="27e6c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="27e6c-129"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27e6c-129"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="27e6c-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="27e6c-130">Library</span></span><br/> | <dl> <span data-ttu-id="27e6c-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="27e6c-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27e6c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27e6c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27e6c-133">**Ctransinplaceinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="27e6c-133">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




