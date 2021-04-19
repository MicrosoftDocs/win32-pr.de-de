---
description: Die get \_ IsValid-Methode überprüft das Sitzungs Deskriptor-Protokoll (SDP; siehe RFC 2327) für Struktur-und Feldwerte.
ms.assetid: a3f849ac-bda9-4937-bf3b-bce8df20cbf0
title: 'Itsdp:: get_IsValid-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ca3cfdc1061e0a2830010ec39b2e6667c9341c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367212"
---
# <a name="itsdpget_isvalid-method"></a><span data-ttu-id="9ffaf-103">Itsdp:: get \_ IsValid-Methode</span><span class="sxs-lookup"><span data-stu-id="9ffaf-103">ITSdp::get\_IsValid method</span></span>

<span data-ttu-id="9ffaf-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9ffaf-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9ffaf-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="9ffaf-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9ffaf-106">Die **get \_ IsValid** -Methode überprüft das Sitzungs Deskriptor-Protokoll (SDP; siehe RFC 2327) für Struktur-und Feldwerte.</span><span class="sxs-lookup"><span data-stu-id="9ffaf-106">The **get\_IsValid** method validates the Session Descriptor Protocol (SDP; see RFC 2327) blob for structure and field values.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ffaf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ffaf-107">Syntax</span></span>


```C++
HRESULT get_IsValid(
  [out] VARIANT_BOOL *pfIsValid
);
```



## <a name="parameters"></a><span data-ttu-id="9ffaf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ffaf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ffaf-109">*pfisvalid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9ffaf-109">*pfIsValid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ffaf-110">Gibt an, ob die BLOB-Struktur gültig ist.</span><span class="sxs-lookup"><span data-stu-id="9ffaf-110">Indicates whether the blob structure is valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ffaf-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ffaf-111">Return value</span></span>

<span data-ttu-id="9ffaf-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9ffaf-112">This method can return one of these values.</span></span>



| <span data-ttu-id="9ffaf-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9ffaf-113">Return code</span></span>                                                                                   | <span data-ttu-id="9ffaf-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ffaf-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="9ffaf-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9ffaf-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9ffaf-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9ffaf-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9ffaf-117"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="9ffaf-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9ffaf-118">Der *pfisvalid* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9ffaf-118">The *pfIsValid* parameter is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="9ffaf-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="9ffaf-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9ffaf-120">Der *pfisvalid* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="9ffaf-120">The *pfIsValid* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="9ffaf-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="9ffaf-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9ffaf-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9ffaf-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="9ffaf-123"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="9ffaf-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="9ffaf-124">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="9ffaf-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="9ffaf-125"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="9ffaf-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="9ffaf-126">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="9ffaf-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="9ffaf-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ffaf-127">Requirements</span></span>



| <span data-ttu-id="9ffaf-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ffaf-128">Requirement</span></span> | <span data-ttu-id="9ffaf-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9ffaf-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ffaf-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="9ffaf-130">TAPI version</span></span><br/> | <span data-ttu-id="9ffaf-131">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="9ffaf-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9ffaf-132">Header</span><span class="sxs-lookup"><span data-stu-id="9ffaf-132">Header</span></span><br/>       | <dl> <span data-ttu-id="9ffaf-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ffaf-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ffaf-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9ffaf-134">Library</span></span><br/>      | <dl> <span data-ttu-id="9ffaf-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ffaf-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9ffaf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9ffaf-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="9ffaf-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ffaf-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ffaf-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ffaf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ffaf-139">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="9ffaf-139">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




