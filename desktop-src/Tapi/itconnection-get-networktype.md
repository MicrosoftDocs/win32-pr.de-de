---
description: Der \_ Netzwerktyp wird von der Get Network Type-Methode abgerufen.
ms.assetid: 5597284a-9cc6-422b-a064-cda25aa5964b
title: 'Itconnection:: get_NetworkType-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31189ec0e3b42e3ed249cd0c62365b1f8c793908
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370024"
---
# <a name="itconnectionget_networktype-method"></a><span data-ttu-id="9a91f-103">Itconnection:: get \_ Network Type-Methode</span><span class="sxs-lookup"><span data-stu-id="9a91f-103">ITConnection::get\_NetworkType method</span></span>

<span data-ttu-id="9a91f-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9a91f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9a91f-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="9a91f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9a91f-106">Der **\_ Netzwerktyp wird von der Get Network Type** -Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9a91f-106">The **get\_NetworkType** method gets the network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a91f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a91f-107">Syntax</span></span>


```C++
HRESULT get_NetworkType(
  [out] BSTR *ppNetworkType
);
```



## <a name="parameters"></a><span data-ttu-id="9a91f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a91f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a91f-109">*ppnetworktype* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9a91f-109">*ppNetworkType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a91f-110">Zeiger auf einen **BSTR** -Wert, der den Netzwerktyp enthält.</span><span class="sxs-lookup"><span data-stu-id="9a91f-110">Pointer to a **BSTR** containing the network type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a91f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a91f-111">Return value</span></span>

<span data-ttu-id="9a91f-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9a91f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="9a91f-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9a91f-113">Return code</span></span>                                                                                   | <span data-ttu-id="9a91f-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a91f-114">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="9a91f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9a91f-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9a91f-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9a91f-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="9a91f-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="9a91f-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9a91f-118">Der *ppnetworktype* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="9a91f-118">The *ppNetworkType* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="9a91f-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="9a91f-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9a91f-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9a91f-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="9a91f-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="9a91f-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="9a91f-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="9a91f-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9a91f-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="9a91f-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="9a91f-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="9a91f-124">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="9a91f-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a91f-125">Remarks</span></span>

<span data-ttu-id="9a91f-126">Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *ppnetworktype* -Parameter zugewiesenen Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="9a91f-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppNetworkType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a91f-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a91f-127">Requirements</span></span>



| <span data-ttu-id="9a91f-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a91f-128">Requirement</span></span> | <span data-ttu-id="9a91f-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9a91f-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a91f-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="9a91f-130">TAPI version</span></span><br/> | <span data-ttu-id="9a91f-131">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="9a91f-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9a91f-132">Header</span><span class="sxs-lookup"><span data-stu-id="9a91f-132">Header</span></span><br/>       | <dl> <span data-ttu-id="9a91f-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a91f-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a91f-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9a91f-134">Library</span></span><br/>      | <dl> <span data-ttu-id="9a91f-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a91f-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9a91f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9a91f-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="9a91f-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a91f-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a91f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a91f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a91f-139">**Itconnection**</span><span class="sxs-lookup"><span data-stu-id="9a91f-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="9a91f-140">**Itconnection::p UT- \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="9a91f-140">**ITConnection::put\_NetworkType**</span></span>](itconnection-put-networktype.md)
</dt> </dl>

 

