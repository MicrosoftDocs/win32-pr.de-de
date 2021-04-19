---
description: Mit der Put \_ AttributeList-Methode wird die Liste der Attribute festgelegt.
ms.assetid: f7d57c0c-9114-42a4-b2bc-c812334d8136
title: Itattributelist::p ut_AttributeList-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3876b2cd8ecdef46a933ff3f3c91be96dd028892
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367103"
---
# <a name="itattributelistput_attributelist-method"></a><span data-ttu-id="fe247-103">Itattributelist::p UT \_ AttributeList-Methode</span><span class="sxs-lookup"><span data-stu-id="fe247-103">ITAttributeList::put\_AttributeList method</span></span>

<span data-ttu-id="fe247-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fe247-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fe247-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="fe247-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fe247-106">Mit der **Put \_ AttributeList** -Methode wird die Liste der Attribute festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe247-106">The **put\_AttributeList** method sets the list of attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe247-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe247-107">Syntax</span></span>


```C++
HRESULT put_AttributeList(
  [in] VARIANT newVal
);
```



## <a name="parameters"></a><span data-ttu-id="fe247-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe247-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe247-109">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe247-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe247-110">Array von Attributen, die festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fe247-110">Array of attributes to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe247-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe247-111">Return value</span></span>

<span data-ttu-id="fe247-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fe247-112">This method can return one of these values.</span></span>



| <span data-ttu-id="fe247-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fe247-113">Return code</span></span>                                                                                   | <span data-ttu-id="fe247-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe247-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="fe247-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fe247-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fe247-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="fe247-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fe247-117"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="fe247-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fe247-118">Der *NewVal* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="fe247-118">The *newVal* parameter is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="fe247-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="fe247-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fe247-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fe247-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="fe247-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="fe247-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="fe247-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="fe247-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="fe247-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="fe247-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="fe247-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="fe247-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="fe247-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe247-125">Requirements</span></span>



| <span data-ttu-id="fe247-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe247-126">Requirement</span></span> | <span data-ttu-id="fe247-127">Wert</span><span class="sxs-lookup"><span data-stu-id="fe247-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe247-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="fe247-128">TAPI version</span></span><br/> | <span data-ttu-id="fe247-129">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="fe247-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="fe247-130">Header</span><span class="sxs-lookup"><span data-stu-id="fe247-130">Header</span></span><br/>       | <dl> <span data-ttu-id="fe247-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe247-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe247-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fe247-132">Library</span></span><br/>      | <dl> <span data-ttu-id="fe247-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe247-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fe247-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fe247-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="fe247-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe247-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe247-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe247-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe247-137">**Itattributelist**</span><span class="sxs-lookup"><span data-stu-id="fe247-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> <dt>

[<span data-ttu-id="fe247-138">**Itattributelist:: get \_ AttributeList**</span><span class="sxs-lookup"><span data-stu-id="fe247-138">**ITAttributeList::get\_AttributeList**</span></span>](itattributelist-get-attributelist.md)
</dt> </dl>

 

 




