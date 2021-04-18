---
description: Die Put \_ Description-Methode legt die Beschreibung der Sitzung fest.
ms.assetid: 535957e7-effe-4b1b-8cba-38a7a3fe9a9a
title: Itsdp::p ut_Description-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea8799ce9b2b8f3f44147b8ca60a92d2c37d5e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358765"
---
# <a name="itsdpput_description-method"></a><span data-ttu-id="dd4a4-103">Itsdp::p UT- \_ Beschreibungs Methode</span><span class="sxs-lookup"><span data-stu-id="dd4a4-103">ITSdp::put\_Description method</span></span>

<span data-ttu-id="dd4a4-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dd4a4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dd4a4-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="dd4a4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="dd4a4-106">Die **Put \_ Description** -Methode legt die Beschreibung der Sitzung fest.</span><span class="sxs-lookup"><span data-stu-id="dd4a4-106">The **put\_Description** method sets the session description.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd4a4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd4a4-107">Syntax</span></span>


```C++
HRESULT put_Description(
  [in] BSTR pDescription
);
```



## <a name="parameters"></a><span data-ttu-id="dd4a4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd4a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd4a4-109">*pdescription* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd4a4-109">*pDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd4a4-110">Zeiger auf einen **BSTR** -Wert, der die Sitzungs Beschreibung enthält.</span><span class="sxs-lookup"><span data-stu-id="dd4a4-110">Pointer to a **BSTR** containing the session description.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd4a4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd4a4-111">Return value</span></span>

<span data-ttu-id="dd4a4-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="dd4a4-112">This method can return one of these values.</span></span>



| <span data-ttu-id="dd4a4-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dd4a4-113">Return code</span></span>                                                                                   | <span data-ttu-id="dd4a4-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd4a4-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="dd4a4-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dd4a4-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dd4a4-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dd4a4-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="dd4a4-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="dd4a4-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="dd4a4-118">Der *pdescription* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="dd4a4-118">The *pDescription* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="dd4a4-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="dd4a4-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="dd4a4-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="dd4a4-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="dd4a4-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="dd4a4-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="dd4a4-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="dd4a4-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="dd4a4-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="dd4a4-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="dd4a4-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="dd4a4-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="dd4a4-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd4a4-125">Remarks</span></span>

<span data-ttu-id="dd4a4-126">Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *pdescription* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="dd4a4-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pDescription* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="dd4a4-127">Diese Funktion kann Daten in unverschlüsselter Form über das Netzwerk senden. aus diesem Grund kann ein Benutzer, der sich im Netzwerk befindet, möglicherweise die Daten lesen.</span><span class="sxs-lookup"><span data-stu-id="dd4a4-127">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="dd4a4-128">Das Sicherheitsrisiko, dass Daten im Klartext gesendet werden, sollte vor der Verwendung dieser Methode berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="dd4a4-128">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd4a4-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd4a4-129">Requirements</span></span>



| <span data-ttu-id="dd4a4-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd4a4-130">Requirement</span></span> | <span data-ttu-id="dd4a4-131">Wert</span><span class="sxs-lookup"><span data-stu-id="dd4a4-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd4a4-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="dd4a4-132">TAPI version</span></span><br/> | <span data-ttu-id="dd4a4-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="dd4a4-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="dd4a4-134">Header</span><span class="sxs-lookup"><span data-stu-id="dd4a4-134">Header</span></span><br/>       | <dl> <span data-ttu-id="dd4a4-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd4a4-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd4a4-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dd4a4-136">Library</span></span><br/>      | <dl> <span data-ttu-id="dd4a4-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd4a4-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="dd4a4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="dd4a4-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="dd4a4-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd4a4-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd4a4-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd4a4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd4a4-141">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="dd4a4-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="dd4a4-142">**Itsdp:: get- \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd4a4-142">**ITSdp::get\_Description**</span></span>](itsdp-get-description.md)
</dt> </dl>

 

