---
description: Die get \_ STARTADDRESS-Methode ruft die erste Adresse ab, die für die Sitzung verwendet werden soll.
ms.assetid: 3c4fec19-1b7d-4052-afd8-7aaf095907d0
title: 'Itconnection:: get_StartAddress-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84266d1874e7d04acb594bcfb9d99b440b0390b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352913"
---
# <a name="itconnectionget_startaddress-method"></a><span data-ttu-id="8092e-103">Itconnection:: get \_ STARTADDRESS-Methode</span><span class="sxs-lookup"><span data-stu-id="8092e-103">ITConnection::get\_StartAddress method</span></span>

<span data-ttu-id="8092e-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8092e-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8092e-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="8092e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8092e-106">Die **get \_ STARTADDRESS** -Methode ruft die erste Adresse ab, die für die Sitzung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8092e-106">The **get\_StartAddress** method gets the first address to be used for the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="8092e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8092e-107">Syntax</span></span>


```C++
HRESULT get_StartAddress(
  [out] BSTR *ppStartAddress
);
```



## <a name="parameters"></a><span data-ttu-id="8092e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8092e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8092e-109">*ppstartaddress* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8092e-109">*ppStartAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8092e-110">Zeiger auf einen **BSTR** -Wert, der die Anfangsadresse für die Sitzung enthält.</span><span class="sxs-lookup"><span data-stu-id="8092e-110">Pointer to a **BSTR** containing the starting address for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8092e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8092e-111">Return value</span></span>

<span data-ttu-id="8092e-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8092e-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8092e-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8092e-113">Return code</span></span>                                                                                   | <span data-ttu-id="8092e-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8092e-114">Description</span></span>                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="8092e-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8092e-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8092e-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8092e-116">Method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="8092e-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="8092e-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8092e-118">Der *ppstartaddress* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="8092e-118">The *ppStartAddress* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="8092e-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="8092e-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8092e-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8092e-120">Insufficient memory exists to perform the operation.</span></span><br/>   |
| <dl> <span data-ttu-id="8092e-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="8092e-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8092e-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="8092e-122">Unspecified error.</span></span><br/>                                     |
| <dl> <span data-ttu-id="8092e-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="8092e-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8092e-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="8092e-124">This method is not yet implemented.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="8092e-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8092e-125">Remarks</span></span>

<span data-ttu-id="8092e-126">Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *ppstartaddress* -Parameter zugewiesenen Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="8092e-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppStartAddress* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8092e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8092e-127">Requirements</span></span>



| <span data-ttu-id="8092e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8092e-128">Requirement</span></span> | <span data-ttu-id="8092e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="8092e-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8092e-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="8092e-130">TAPI version</span></span><br/> | <span data-ttu-id="8092e-131">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="8092e-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8092e-132">Header</span><span class="sxs-lookup"><span data-stu-id="8092e-132">Header</span></span><br/>       | <dl> <span data-ttu-id="8092e-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8092e-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8092e-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8092e-134">Library</span></span><br/>      | <dl> <span data-ttu-id="8092e-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8092e-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8092e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8092e-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="8092e-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8092e-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8092e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8092e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8092e-139">**Itconnection**</span><span class="sxs-lookup"><span data-stu-id="8092e-139">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

