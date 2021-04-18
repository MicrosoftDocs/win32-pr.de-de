---
description: Die get \_ ProtocolVersion-Methode ruft die Protokollversion des Sitzungs Deskriptors-Protokolls (SDP; siehe RFC 2327) ab.
ms.assetid: 7c62357c-427f-40f9-a9d2-c4e1a8400e97
title: 'Itsdp:: get_ProtocolVersion-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652c6c3d6723a10cfe474376cf8b9f1342321db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358379"
---
# <a name="itsdpget_protocolversion-method"></a><span data-ttu-id="bf1e1-103">Itsdp:: get \_ ProtocolVersion-Methode</span><span class="sxs-lookup"><span data-stu-id="bf1e1-103">ITSdp::get\_ProtocolVersion method</span></span>

<span data-ttu-id="bf1e1-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bf1e1-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="bf1e1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bf1e1-106">Die **get \_ ProtocolVersion** -Methode ruft die Protokollversion des Sitzungs Deskriptors-Protokolls (SDP; siehe RFC 2327) ab.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-106">The **get\_ProtocolVersion** method gets the Session Descriptor Protocol (SDP; see RFC 2327) protocol version.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf1e1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf1e1-107">Syntax</span></span>


```C++
HRESULT get_ProtocolVersion(
  [out] unsigned char *pProtocolVersion
);
```



## <a name="parameters"></a><span data-ttu-id="bf1e1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf1e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf1e1-109">*pprotocolversion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bf1e1-109">*pProtocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1e1-110">Zeiger auf die Protokollversion.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-110">Pointer to the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf1e1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bf1e1-111">Return value</span></span>

<span data-ttu-id="bf1e1-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-112">This method can return one of these values.</span></span>



| <span data-ttu-id="bf1e1-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bf1e1-113">Return code</span></span>                                                                                   | <span data-ttu-id="bf1e1-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf1e1-114">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="bf1e1-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bf1e1-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bf1e1-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-116">Method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="bf1e1-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="bf1e1-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bf1e1-118">Der *pprotocolversion* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-118">The *pProtocolVersion* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="bf1e1-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="bf1e1-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bf1e1-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-120">Insufficient memory exists to perform the operation.</span></span><br/>     |
| <dl> <span data-ttu-id="bf1e1-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="bf1e1-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="bf1e1-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-122">Unspecified error.</span></span><br/>                                       |
| <dl> <span data-ttu-id="bf1e1-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="bf1e1-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="bf1e1-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="bf1e1-124">This method is not yet implemented.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="bf1e1-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf1e1-125">Requirements</span></span>



| <span data-ttu-id="bf1e1-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf1e1-126">Requirement</span></span> | <span data-ttu-id="bf1e1-127">Wert</span><span class="sxs-lookup"><span data-stu-id="bf1e1-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf1e1-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="bf1e1-128">TAPI version</span></span><br/> | <span data-ttu-id="bf1e1-129">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="bf1e1-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bf1e1-130">Header</span><span class="sxs-lookup"><span data-stu-id="bf1e1-130">Header</span></span><br/>       | <dl> <span data-ttu-id="bf1e1-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf1e1-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf1e1-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bf1e1-132">Library</span></span><br/>      | <dl> <span data-ttu-id="bf1e1-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf1e1-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bf1e1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bf1e1-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="bf1e1-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf1e1-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf1e1-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf1e1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf1e1-137">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="bf1e1-137">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




