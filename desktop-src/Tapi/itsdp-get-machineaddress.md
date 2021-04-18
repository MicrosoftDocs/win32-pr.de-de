---
description: Mit der get \_ machineaddress-Methode wird die Computer Adresse des Ursprungs Hosts abgerufen.
ms.assetid: 8a67cc9f-f9fc-4ec3-86f9-ffe34d075830
title: 'Itsdp:: get_MachineAddress-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34968efa16f04cba8f99dbc0dc42b0cf4995a43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364885"
---
# <a name="itsdpget_machineaddress-method"></a><span data-ttu-id="a0746-103">Itsdp:: get \_ machineaddress-Methode</span><span class="sxs-lookup"><span data-stu-id="a0746-103">ITSdp::get\_MachineAddress method</span></span>

<span data-ttu-id="a0746-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a0746-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a0746-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="a0746-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a0746-106">Mit der **get \_ machineaddress** -Methode wird die Computer Adresse des Ursprungs Hosts abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a0746-106">The **get\_MachineAddress** method gets the machine address of the originating host.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0746-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0746-107">Syntax</span></span>


```C++
HRESULT get_MachineAddress(
  [out] BSTR *ppMachineAddress
);
```



## <a name="parameters"></a><span data-ttu-id="a0746-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0746-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0746-109">*ppmachineaddress* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a0746-109">*ppMachineAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0746-110">Zeiger auf einen **BSTR** -Wert, der die Computer Adresse des Konferenz Hosts enthält.</span><span class="sxs-lookup"><span data-stu-id="a0746-110">Pointer to a **BSTR** containing the machine address of the conference host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0746-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0746-111">Return value</span></span>

<span data-ttu-id="a0746-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a0746-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a0746-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a0746-113">Return code</span></span>                                                                                   | <span data-ttu-id="a0746-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0746-114">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="a0746-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a0746-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a0746-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a0746-116">Method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="a0746-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="a0746-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a0746-118">Der *ppmachineaddres* s-Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="a0746-118">The *ppMachineAddres* s parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="a0746-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="a0746-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a0746-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0746-120">Insufficient memory exists to perform the operation.</span></span><br/>     |
| <dl> <span data-ttu-id="a0746-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="a0746-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a0746-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="a0746-122">Unspecified error.</span></span><br/>                                       |
| <dl> <span data-ttu-id="a0746-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="a0746-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a0746-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a0746-124">This method is not yet implemented.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="a0746-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0746-125">Remarks</span></span>

<span data-ttu-id="a0746-126">Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *ppmachineaddress* -Parameter zugewiesenen Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="a0746-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMachineAddress* parameter.</span></span>

<span data-ttu-id="a0746-127">Der *ppmachineaddress* -Parameter kann entweder als DNS-Name ("johnsmith.workinghard.Microsoft.com") oder als IP-Adresse ("10.111.222.111") zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a0746-127">The *ppMachineAddress* parameter can be returned as either a DNS name ("JohnSmith.workinghard.microsoft.com") or an IP address ("10.111.222.111").</span></span>

## <a name="requirements"></a><span data-ttu-id="a0746-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0746-128">Requirements</span></span>



| <span data-ttu-id="a0746-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0746-129">Requirement</span></span> | <span data-ttu-id="a0746-130">Wert</span><span class="sxs-lookup"><span data-stu-id="a0746-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0746-131">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="a0746-131">TAPI version</span></span><br/> | <span data-ttu-id="a0746-132">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="a0746-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a0746-133">Header</span><span class="sxs-lookup"><span data-stu-id="a0746-133">Header</span></span><br/>       | <dl> <span data-ttu-id="a0746-134"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0746-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0746-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a0746-135">Library</span></span><br/>      | <dl> <span data-ttu-id="a0746-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0746-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a0746-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a0746-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="a0746-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0746-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0746-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0746-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0746-140">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="a0746-140">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="a0746-141">**Itsdp::p UT \_ machineaddress**</span><span class="sxs-lookup"><span data-stu-id="a0746-141">**ITSdp::put\_MachineAddress**</span></span>](itsdp-put-machineaddress.md)
</dt> </dl>

 

