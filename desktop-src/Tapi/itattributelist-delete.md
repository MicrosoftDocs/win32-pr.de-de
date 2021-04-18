---
description: Die Delete-Methode löscht das Attribut am angegebenen Index.
ms.assetid: 6bc6f3d2-d630-4a00-9d74-fb5fa7626e3f
title: Itattributelist::D Elete-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729dd79b88198f671949aeb79caf06289abd9a75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371760"
---
# <a name="itattributelistdelete-method"></a><span data-ttu-id="34e6b-103">Itattributelist::D Elete-Methode</span><span class="sxs-lookup"><span data-stu-id="34e6b-103">ITAttributeList::Delete method</span></span>

<span data-ttu-id="34e6b-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="34e6b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="34e6b-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="34e6b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="34e6b-106">Die **Delete** -Methode löscht das Attribut am angegebenen Index.</span><span class="sxs-lookup"><span data-stu-id="34e6b-106">The **Delete** method deletes the attribute at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="34e6b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="34e6b-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="34e6b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="34e6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34e6b-109">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34e6b-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e6b-110">Der Index des zu löschenden Attributs.</span><span class="sxs-lookup"><span data-stu-id="34e6b-110">Index of the attribute to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34e6b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34e6b-111">Return value</span></span>

<span data-ttu-id="34e6b-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="34e6b-112">This method can return one of these values.</span></span>



| <span data-ttu-id="34e6b-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="34e6b-113">Return code</span></span>                                                                                   | <span data-ttu-id="34e6b-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34e6b-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="34e6b-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="34e6b-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="34e6b-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="34e6b-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="34e6b-117"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="34e6b-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="34e6b-118">Der *Index* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="34e6b-118">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="34e6b-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="34e6b-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="34e6b-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="34e6b-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="34e6b-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="34e6b-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="34e6b-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="34e6b-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="34e6b-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="34e6b-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="34e6b-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="34e6b-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="34e6b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34e6b-125">Requirements</span></span>



| <span data-ttu-id="34e6b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34e6b-126">Requirement</span></span> | <span data-ttu-id="34e6b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="34e6b-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34e6b-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="34e6b-128">TAPI version</span></span><br/> | <span data-ttu-id="34e6b-129">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="34e6b-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="34e6b-130">Header</span><span class="sxs-lookup"><span data-stu-id="34e6b-130">Header</span></span><br/>       | <dl> <span data-ttu-id="34e6b-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="34e6b-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="34e6b-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="34e6b-132">Library</span></span><br/>      | <dl> <span data-ttu-id="34e6b-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34e6b-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="34e6b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="34e6b-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="34e6b-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34e6b-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34e6b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34e6b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e6b-137">**Itattributelist**</span><span class="sxs-lookup"><span data-stu-id="34e6b-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

 




