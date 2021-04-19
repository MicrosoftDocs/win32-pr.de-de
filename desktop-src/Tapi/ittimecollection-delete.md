---
description: Die Delete-Methode löscht eine ittime-Komponente.
ms.assetid: 0445d659-7b83-4462-b199-511fd8270f32
title: Ittimecollection::D Elete-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9aad562660a2d563193e5074b52f4d1a513bb39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373711"
---
# <a name="ittimecollectiondelete-method"></a><span data-ttu-id="0bb28-103">Ittimecollection::D Elete-Methode</span><span class="sxs-lookup"><span data-stu-id="0bb28-103">ITTimeCollection::Delete method</span></span>

<span data-ttu-id="0bb28-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0bb28-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0bb28-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="0bb28-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0bb28-106">Die **Delete** -Methode löscht eine [**ittime**](ittime.md) -Komponente.</span><span class="sxs-lookup"><span data-stu-id="0bb28-106">The **Delete** method deletes an [**ITTime**](ittime.md) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bb28-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bb28-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="0bb28-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bb28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bb28-109">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0bb28-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb28-110">Der Index der zu löschenden [**ittime**](ittime.md) -Komponente.</span><span class="sxs-lookup"><span data-stu-id="0bb28-110">Index of the [**ITTime**](ittime.md) component to be deleted.</span></span> <span data-ttu-id="0bb28-111">(Das Index Array ist 1-basiert.)</span><span class="sxs-lookup"><span data-stu-id="0bb28-111">(The index array is one-based.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bb28-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0bb28-112">Return value</span></span>

<span data-ttu-id="0bb28-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0bb28-113">This method can return one of these values.</span></span>



| <span data-ttu-id="0bb28-114">Wert</span><span class="sxs-lookup"><span data-stu-id="0bb28-114">Value</span></span>                                                                                         | <span data-ttu-id="0bb28-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0bb28-115">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0bb28-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0bb28-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0bb28-117">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0bb28-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0bb28-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="0bb28-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0bb28-119">Der *Index* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0bb28-119">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="0bb28-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="0bb28-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0bb28-121">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0bb28-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="0bb28-122"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="0bb28-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="0bb28-123">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="0bb28-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0bb28-124"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="0bb28-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="0bb28-125">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="0bb28-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="0bb28-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bb28-126">Requirements</span></span>



| <span data-ttu-id="0bb28-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0bb28-127">Requirement</span></span> | <span data-ttu-id="0bb28-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0bb28-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb28-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="0bb28-129">TAPI version</span></span><br/> | <span data-ttu-id="0bb28-130">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="0bb28-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0bb28-131">Header</span><span class="sxs-lookup"><span data-stu-id="0bb28-131">Header</span></span><br/>       | <dl> <span data-ttu-id="0bb28-132"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bb28-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0bb28-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0bb28-133">Library</span></span><br/>      | <dl> <span data-ttu-id="0bb28-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bb28-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0bb28-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0bb28-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="0bb28-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bb28-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bb28-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bb28-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bb28-138">**Ittimecollection**</span><span class="sxs-lookup"><span data-stu-id="0bb28-138">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="0bb28-139">**Ittime**</span><span class="sxs-lookup"><span data-stu-id="0bb28-139">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




