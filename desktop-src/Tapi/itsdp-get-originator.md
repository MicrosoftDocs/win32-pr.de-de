---
description: Die get \_ Originator-Methode ruft den Absender der Konferenz ab.
ms.assetid: a324098d-ae22-42e9-901e-b277433af199
title: 'Itsdp:: get_Originator-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f751dd5a9dffe2d3bbc7883b8a0f8f18f8e6381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360365"
---
# <a name="itsdpget_originator-method"></a><span data-ttu-id="e6fdf-103">Itsdp:: get \_ Originator-Methode</span><span class="sxs-lookup"><span data-stu-id="e6fdf-103">ITSdp::get\_Originator method</span></span>

<span data-ttu-id="e6fdf-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e6fdf-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e6fdf-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="e6fdf-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e6fdf-106">Die **get \_ Originator** -Methode ruft den Absender der Konferenz ab.</span><span class="sxs-lookup"><span data-stu-id="e6fdf-106">The **get\_Originator** method gets the conference originator.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6fdf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6fdf-107">Syntax</span></span>


```C++
HRESULT get_Originator(
  [out] BSTR *ppOriginator
);
```



## <a name="parameters"></a><span data-ttu-id="e6fdf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6fdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6fdf-109">*pporiginator* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e6fdf-109">*ppOriginator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6fdf-110">Zeiger auf eine **BSTR** -Darstellung des Konferenz Ursprungs.</span><span class="sxs-lookup"><span data-stu-id="e6fdf-110">Pointer to a **BSTR** representation of the conference originator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6fdf-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6fdf-111">Return value</span></span>

<span data-ttu-id="e6fdf-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e6fdf-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e6fdf-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e6fdf-113">Return code</span></span>                                                                                   | <span data-ttu-id="e6fdf-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6fdf-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e6fdf-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e6fdf-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e6fdf-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e6fdf-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e6fdf-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="e6fdf-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e6fdf-118">Der *pporiginator* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="e6fdf-118">The *ppOriginator* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="e6fdf-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="e6fdf-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e6fdf-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e6fdf-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e6fdf-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="e6fdf-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="e6fdf-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="e6fdf-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e6fdf-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="e6fdf-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="e6fdf-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="e6fdf-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="e6fdf-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6fdf-125">Remarks</span></span>

<span data-ttu-id="e6fdf-126">Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *pporiginator* -Parameter reservierten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="e6fdf-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppOriginator* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6fdf-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6fdf-127">Requirements</span></span>



| <span data-ttu-id="e6fdf-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6fdf-128">Requirement</span></span> | <span data-ttu-id="e6fdf-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e6fdf-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6fdf-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="e6fdf-130">TAPI version</span></span><br/> | <span data-ttu-id="e6fdf-131">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e6fdf-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e6fdf-132">Header</span><span class="sxs-lookup"><span data-stu-id="e6fdf-132">Header</span></span><br/>       | <dl> <span data-ttu-id="e6fdf-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6fdf-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e6fdf-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e6fdf-134">Library</span></span><br/>      | <dl> <span data-ttu-id="e6fdf-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6fdf-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e6fdf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e6fdf-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="e6fdf-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6fdf-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6fdf-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6fdf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6fdf-139">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="e6fdf-139">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="e6fdf-140">**Itsdp: \_ :p UT-Absender**</span><span class="sxs-lookup"><span data-stu-id="e6fdf-140">**ITSdp::put\_Originator**</span></span>](itsdp-put-originator.md)
</dt> </dl>

 

