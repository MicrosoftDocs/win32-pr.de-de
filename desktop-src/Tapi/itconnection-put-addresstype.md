---
description: Die Put \_ adressstype-Methode legt den Adresstyp fest.
ms.assetid: 73c64904-925c-4a35-a8f9-88b196b59b1e
title: Itconnection::p ut_AddressType-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cb9bc9b83a71f78a68b6efc2fa73c259c4afe9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364644"
---
# <a name="itconnectionput_addresstype-method"></a><span data-ttu-id="82b65-103">Itconnection::p UT- \_ adressatormethode</span><span class="sxs-lookup"><span data-stu-id="82b65-103">ITConnection::put\_AddressType method</span></span>

<span data-ttu-id="82b65-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="82b65-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="82b65-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="82b65-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="82b65-106">Die **Put \_ adressstype** -Methode legt den Adresstyp fest.</span><span class="sxs-lookup"><span data-stu-id="82b65-106">The **put\_AddressType** method sets the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="82b65-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="82b65-107">Syntax</span></span>


```C++
HRESULT put_AddressType(
  [in] BSTR pAddressType
);
```



## <a name="parameters"></a><span data-ttu-id="82b65-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="82b65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82b65-109">*padresssstype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82b65-109">*pAddressType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82b65-110">Zeiger auf einen **BSTR** -Wert, der den adrestyp enthält.</span><span class="sxs-lookup"><span data-stu-id="82b65-110">Pointer to a **BSTR** containing the address type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82b65-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82b65-111">Return value</span></span>

<span data-ttu-id="82b65-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="82b65-112">This method can return one of these values.</span></span>



| <span data-ttu-id="82b65-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="82b65-113">Return code</span></span>                                                                                   | <span data-ttu-id="82b65-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="82b65-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="82b65-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="82b65-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="82b65-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="82b65-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="82b65-117"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="82b65-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="82b65-118">Der *padresssstype* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="82b65-118">The *pAddressType* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="82b65-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="82b65-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="82b65-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="82b65-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="82b65-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="82b65-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="82b65-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="82b65-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="82b65-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="82b65-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="82b65-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="82b65-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="82b65-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82b65-125">Remarks</span></span>

<span data-ttu-id="82b65-126">Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *padresstype* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="82b65-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pAddressType* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="82b65-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82b65-127">Requirements</span></span>



| <span data-ttu-id="82b65-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82b65-128">Requirement</span></span> | <span data-ttu-id="82b65-129">Wert</span><span class="sxs-lookup"><span data-stu-id="82b65-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82b65-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="82b65-130">TAPI version</span></span><br/> | <span data-ttu-id="82b65-131">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="82b65-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="82b65-132">Header</span><span class="sxs-lookup"><span data-stu-id="82b65-132">Header</span></span><br/>       | <dl> <span data-ttu-id="82b65-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="82b65-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="82b65-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="82b65-134">Library</span></span><br/>      | <dl> <span data-ttu-id="82b65-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82b65-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="82b65-136">DLL</span><span class="sxs-lookup"><span data-stu-id="82b65-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="82b65-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82b65-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82b65-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82b65-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82b65-139">**Itconnection**</span><span class="sxs-lookup"><span data-stu-id="82b65-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="82b65-140">**Itconnection:: get \_ adressstype**</span><span class="sxs-lookup"><span data-stu-id="82b65-140">**ITConnection::get\_AddressType**</span></span>](itconnection-get-addresstype.md)
</dt> </dl>

 

