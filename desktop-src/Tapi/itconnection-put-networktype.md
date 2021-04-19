---
description: Die Put \_ NetworkType-Methode legt den Netzwerktyp fest.
ms.assetid: 747e3133-d103-44dc-b119-5a4cb4ed7f18
title: Itconnection::p ut_NetworkType-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e08819bcc5cb00824c8c1510d85fdcb1de186b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356399"
---
# <a name="itconnectionput_networktype-method"></a><span data-ttu-id="ae081-103">Itconnection::p UT- \_ NetworkType-Methode</span><span class="sxs-lookup"><span data-stu-id="ae081-103">ITConnection::put\_NetworkType method</span></span>

<span data-ttu-id="ae081-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ae081-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ae081-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="ae081-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ae081-106">Die **Put \_ NetworkType** -Methode legt den Netzwerktyp fest.</span><span class="sxs-lookup"><span data-stu-id="ae081-106">The **put\_NetworkType** method sets the network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae081-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae081-107">Syntax</span></span>


```C++
HRESULT put_NetworkType(
  [in] BSTR pNetworkType
);
```



## <a name="parameters"></a><span data-ttu-id="ae081-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae081-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae081-109">*pnetworktype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae081-109">*pNetworkType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae081-110">Zeiger auf einen **BSTR** -Wert, der den Netzwerktyp enthält.</span><span class="sxs-lookup"><span data-stu-id="ae081-110">Pointer to a **BSTR** containing the network type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae081-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae081-111">Return value</span></span>

<span data-ttu-id="ae081-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ae081-112">This method can return one of these values.</span></span>



| <span data-ttu-id="ae081-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ae081-113">Return code</span></span>                                                                                   | <span data-ttu-id="ae081-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae081-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ae081-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ae081-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ae081-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ae081-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ae081-117"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ae081-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ae081-118">Der *pnetworktype* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ae081-118">The *pNetworkType* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="ae081-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="ae081-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ae081-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ae081-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ae081-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="ae081-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="ae081-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="ae081-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ae081-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="ae081-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="ae081-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ae081-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="ae081-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae081-125">Remarks</span></span>

<span data-ttu-id="ae081-126">Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *pnetworktype* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="ae081-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pNetworkType* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae081-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae081-127">Requirements</span></span>



| <span data-ttu-id="ae081-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae081-128">Requirement</span></span> | <span data-ttu-id="ae081-129">Wert</span><span class="sxs-lookup"><span data-stu-id="ae081-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae081-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="ae081-130">TAPI version</span></span><br/> | <span data-ttu-id="ae081-131">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ae081-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ae081-132">Header</span><span class="sxs-lookup"><span data-stu-id="ae081-132">Header</span></span><br/>       | <dl> <span data-ttu-id="ae081-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae081-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ae081-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ae081-134">Library</span></span><br/>      | <dl> <span data-ttu-id="ae081-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae081-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ae081-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ae081-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="ae081-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae081-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae081-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae081-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae081-139">**Itconnection**</span><span class="sxs-lookup"><span data-stu-id="ae081-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="ae081-140">**Itconnection:: get \_ Network Type**</span><span class="sxs-lookup"><span data-stu-id="ae081-140">**ITConnection::get\_NetworkType**</span></span>](itconnection-get-networktype.md)
</dt> </dl>

 

