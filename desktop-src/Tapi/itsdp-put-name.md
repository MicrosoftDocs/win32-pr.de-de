---
description: Mit der Put \_ Name-Methode wird der Sitzungsname festgelegt.
ms.assetid: aba05cdb-a870-490e-8bb0-98b11780b112
title: Itsdp::p ut_Name-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7383183b6b367d71d18070eedd5857740665fab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369698"
---
# <a name="itsdpput_name-method"></a><span data-ttu-id="2ac48-103">Itsdp::p UT- \_ namens Methode</span><span class="sxs-lookup"><span data-stu-id="2ac48-103">ITSdp::put\_Name method</span></span>

<span data-ttu-id="2ac48-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2ac48-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2ac48-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="2ac48-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2ac48-106">Mit der **Put \_ Name** -Methode wird der Sitzungsname festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2ac48-106">The **put\_Name** method sets the session name.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ac48-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ac48-107">Syntax</span></span>


```C++
HRESULT put_Name(
  [in] BSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="2ac48-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ac48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ac48-109">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ac48-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ac48-110">Zeiger auf einen **BSTR** -Wert, der den Sitzungs Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="2ac48-110">Pointer to a **BSTR** containing the session name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ac48-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ac48-111">Return value</span></span>

<span data-ttu-id="2ac48-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2ac48-112">This method can return one of these values.</span></span>



| <span data-ttu-id="2ac48-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2ac48-113">Return code</span></span>                                                                                   | <span data-ttu-id="2ac48-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ac48-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2ac48-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2ac48-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2ac48-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2ac48-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2ac48-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="2ac48-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2ac48-118">Der *PName* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="2ac48-118">The *pName* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="2ac48-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="2ac48-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2ac48-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2ac48-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2ac48-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="2ac48-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="2ac48-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="2ac48-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2ac48-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="2ac48-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2ac48-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2ac48-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="2ac48-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ac48-125">Remarks</span></span>

<span data-ttu-id="2ac48-126">Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *PName* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="2ac48-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pName* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ac48-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ac48-127">Requirements</span></span>



| <span data-ttu-id="2ac48-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ac48-128">Requirement</span></span> | <span data-ttu-id="2ac48-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2ac48-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac48-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="2ac48-130">TAPI version</span></span><br/> | <span data-ttu-id="2ac48-131">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="2ac48-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2ac48-132">Header</span><span class="sxs-lookup"><span data-stu-id="2ac48-132">Header</span></span><br/>       | <dl> <span data-ttu-id="2ac48-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ac48-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2ac48-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2ac48-134">Library</span></span><br/>      | <dl> <span data-ttu-id="2ac48-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ac48-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2ac48-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2ac48-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="2ac48-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ac48-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ac48-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ac48-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ac48-139">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="2ac48-139">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="2ac48-140">**Itsdp:: get- \_ Name**</span><span class="sxs-lookup"><span data-stu-id="2ac48-140">**ITSdp::get\_Name**</span></span>](itsdp-get-name.md)
</dt> </dl>

 

