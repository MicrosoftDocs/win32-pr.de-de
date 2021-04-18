---
description: Die get \_ AttributeList-Methode ruft die Liste der Attribute ab.
ms.assetid: 75518257-3339-441f-9965-b93e27f0e2bf
title: 'Itattributelist:: get_AttributeList-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499352cd5087f478e58653fd304e27101db9b433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365787"
---
# <a name="itattributelistget_attributelist-method"></a><span data-ttu-id="9ed30-103">Itattributelist:: get \_ AttributeList-Methode</span><span class="sxs-lookup"><span data-stu-id="9ed30-103">ITAttributeList::get\_AttributeList method</span></span>

<span data-ttu-id="9ed30-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9ed30-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9ed30-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="9ed30-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9ed30-106">Die **get \_ AttributeList** -Methode ruft die Liste der Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="9ed30-106">The **get\_AttributeList** method gets the list of attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ed30-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ed30-107">Syntax</span></span>


```C++
HRESULT get_AttributeList(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="9ed30-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ed30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ed30-109">*PVal* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9ed30-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed30-110">Array von Attributen.</span><span class="sxs-lookup"><span data-stu-id="9ed30-110">Array of attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ed30-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ed30-111">Return value</span></span>

<span data-ttu-id="9ed30-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9ed30-112">This method can return one of these values.</span></span>



| <span data-ttu-id="9ed30-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9ed30-113">Return code</span></span>                                                                                   | <span data-ttu-id="9ed30-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ed30-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="9ed30-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9ed30-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9ed30-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9ed30-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9ed30-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="9ed30-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9ed30-118">Der *PVal* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="9ed30-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="9ed30-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="9ed30-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9ed30-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9ed30-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="9ed30-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="9ed30-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="9ed30-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="9ed30-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="9ed30-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="9ed30-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="9ed30-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="9ed30-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="9ed30-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ed30-125">Requirements</span></span>



| <span data-ttu-id="9ed30-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ed30-126">Requirement</span></span> | <span data-ttu-id="9ed30-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9ed30-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed30-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="9ed30-128">TAPI version</span></span><br/> | <span data-ttu-id="9ed30-129">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="9ed30-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9ed30-130">Header</span><span class="sxs-lookup"><span data-stu-id="9ed30-130">Header</span></span><br/>       | <dl> <span data-ttu-id="9ed30-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ed30-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ed30-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9ed30-132">Library</span></span><br/>      | <dl> <span data-ttu-id="9ed30-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ed30-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9ed30-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9ed30-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="9ed30-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ed30-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ed30-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ed30-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed30-137">**Itattributelist**</span><span class="sxs-lookup"><span data-stu-id="9ed30-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> <dt>

[<span data-ttu-id="9ed30-138">**Itattributelist::p UT \_ AttributeList**</span><span class="sxs-lookup"><span data-stu-id="9ed30-138">**ITAttributeList::put\_AttributeList**</span></span>](itattributelist-put-attributelist.md)
</dt> </dl>

 

 




