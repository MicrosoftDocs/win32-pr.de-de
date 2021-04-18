---
description: Die Put \_ machineaddress-Methode legt die Computer Adresse des Ursprungs Hosts fest.
ms.assetid: f4af55b1-e20b-4fe8-a15e-a1a68d22f1b9
title: Itsdp::p ut_MachineAddress-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec09d41cb7735383f08ce8c8983331165c54fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371759"
---
# <a name="itsdpput_machineaddress-method"></a><span data-ttu-id="97da8-103">Itsdp::p UT \_ machineaddress-Methode</span><span class="sxs-lookup"><span data-stu-id="97da8-103">ITSdp::put\_MachineAddress method</span></span>

<span data-ttu-id="97da8-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="97da8-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="97da8-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="97da8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="97da8-106">Die **Put \_ machineaddress** -Methode legt die Computer Adresse des Ursprungs Hosts fest.</span><span class="sxs-lookup"><span data-stu-id="97da8-106">The **put\_MachineAddress** method sets the machine address of the originating host.</span></span>

## <a name="syntax"></a><span data-ttu-id="97da8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="97da8-107">Syntax</span></span>


```C++
HRESULT put_MachineAddress(
  [in] BSTR pMachineAddress
);
```



## <a name="parameters"></a><span data-ttu-id="97da8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="97da8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97da8-109">*pmachineaddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97da8-109">*pMachineAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97da8-110">Zeiger auf einen **BSTR** -Wert, der die Computer Adresse des Konferenz Hosts enthält.</span><span class="sxs-lookup"><span data-stu-id="97da8-110">Pointer to a **BSTR** containing the machine address of the conference host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97da8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97da8-111">Return value</span></span>

<span data-ttu-id="97da8-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="97da8-112">This method can return one of these values.</span></span>



| <span data-ttu-id="97da8-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="97da8-113">Return code</span></span>                                                                                   | <span data-ttu-id="97da8-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97da8-114">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="97da8-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="97da8-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="97da8-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="97da8-116">Method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="97da8-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="97da8-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="97da8-118">Der *pmachineaddress* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="97da8-118">The *pMachineAddress* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="97da8-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="97da8-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="97da8-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="97da8-120">Insufficient memory exists to perform the operation.</span></span><br/>    |
| <dl> <span data-ttu-id="97da8-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="97da8-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="97da8-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="97da8-122">Unspecified error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="97da8-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="97da8-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="97da8-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="97da8-124">This method is not yet implemented.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="97da8-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97da8-125">Remarks</span></span>

<span data-ttu-id="97da8-126">Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *pmachineaddress* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="97da8-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMachineAddress* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="97da8-127">Der *pmachineaddress* -Parameter kann entweder ein DNS-Name ("johnsmith.workinghard.Microsoft.com") oder eine IP-Adresse ("10.111.222.111") sein.</span><span class="sxs-lookup"><span data-stu-id="97da8-127">The *pMachineAddress* parameter can be either a DNS name ("JohnSmith.workinghard.microsoft.com") or an IP address ("10.111.222.111").</span></span>

<span data-ttu-id="97da8-128">Diese Funktion kann Daten in unverschlüsselter Form über das Netzwerk senden. aus diesem Grund kann ein Benutzer, der sich im Netzwerk befindet, möglicherweise die Daten lesen.</span><span class="sxs-lookup"><span data-stu-id="97da8-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="97da8-129">Das Sicherheitsrisiko, dass Daten im Klartext gesendet werden, sollte vor der Verwendung dieser Methode berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="97da8-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="97da8-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97da8-130">Requirements</span></span>



| <span data-ttu-id="97da8-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97da8-131">Requirement</span></span> | <span data-ttu-id="97da8-132">Wert</span><span class="sxs-lookup"><span data-stu-id="97da8-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97da8-133">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="97da8-133">TAPI version</span></span><br/> | <span data-ttu-id="97da8-134">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="97da8-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="97da8-135">Header</span><span class="sxs-lookup"><span data-stu-id="97da8-135">Header</span></span><br/>       | <dl> <span data-ttu-id="97da8-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="97da8-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="97da8-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="97da8-137">Library</span></span><br/>      | <dl> <span data-ttu-id="97da8-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97da8-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="97da8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="97da8-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="97da8-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97da8-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97da8-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97da8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97da8-142">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="97da8-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="97da8-143">**Itsdp:: get \_ machineaddress**</span><span class="sxs-lookup"><span data-stu-id="97da8-143">**ITSdp::get\_MachineAddress**</span></span>](itsdp-get-machineaddress.md)
</dt> </dl>

 

