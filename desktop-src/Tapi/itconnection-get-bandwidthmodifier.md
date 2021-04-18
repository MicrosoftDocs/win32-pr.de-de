---
description: Die get \_ bandwidthmodifier-Methode ruft den Bandbreiten-Modifizierer ab, bei dem es sich um ein einzelnes alphanumerisches Wort handelt, das die Bedeutung der Bandbreiten Abbildung bereitstellt. Die beiden definierten Modifizierer sind CT (Conference Total) und AS (anwendungsspezifisches Maximum).
ms.assetid: 29bf137d-e88b-437f-8bf1-824e335d47a1
title: 'Itconnection:: get_BandwidthModifier-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e278edfbdc9ae56d89547c0bcf64f90fde77baf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371043"
---
# <a name="itconnectionget_bandwidthmodifier-method"></a><span data-ttu-id="bdb63-104">Itconnection:: get \_ bandwidthmodifier-Methode</span><span class="sxs-lookup"><span data-stu-id="bdb63-104">ITConnection::get\_BandwidthModifier method</span></span>

<span data-ttu-id="bdb63-105">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bdb63-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bdb63-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="bdb63-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bdb63-107">Die **get \_ bandwidthmodifier** -Methode ruft den Bandbreiten-Modifizierer ab, bei dem es sich um ein einzelnes alphanumerisches Wort handelt, das die Bedeutung der Bandbreiten Abbildung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bdb63-107">The **get\_BandwidthModifier** method gets the bandwidth modifier, which is a single, alphanumeric word giving the meaning of the bandwidth figure.</span></span> <span data-ttu-id="bdb63-108">Die beiden definierten Modifizierer sind CT (Conference Total) und AS (anwendungsspezifisches Maximum).</span><span class="sxs-lookup"><span data-stu-id="bdb63-108">The two modifiers defined are CT (Conference Total) and AS (Application Specific Maximum).</span></span>

## <a name="syntax"></a><span data-ttu-id="bdb63-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdb63-109">Syntax</span></span>


```C++
HRESULT get_BandwidthModifier(
  [out] BSTR *ppModifier
);
```



## <a name="parameters"></a><span data-ttu-id="bdb63-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdb63-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdb63-111">*ppmodifier* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bdb63-111">*ppModifier* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdb63-112">Zeiger auf ein **BSTR** , das den Bandbreiten-Modifizierer enthält.</span><span class="sxs-lookup"><span data-stu-id="bdb63-112">Pointer to a **BSTR** containing the bandwidth modifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdb63-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdb63-113">Return value</span></span>

<span data-ttu-id="bdb63-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bdb63-114">This method can return one of these values.</span></span>



| <span data-ttu-id="bdb63-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bdb63-115">Return code</span></span>                                                                                   | <span data-ttu-id="bdb63-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bdb63-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="bdb63-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bdb63-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bdb63-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="bdb63-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bdb63-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="bdb63-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bdb63-120">Der *ppmodifier* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="bdb63-120">The *ppModifier* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="bdb63-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="bdb63-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bdb63-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bdb63-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="bdb63-123"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="bdb63-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="bdb63-124">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="bdb63-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="bdb63-125"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="bdb63-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="bdb63-126">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="bdb63-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="bdb63-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bdb63-127">Remarks</span></span>

<span data-ttu-id="bdb63-128">Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *ppmodifier* -Parameter zugeordneten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="bdb63-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppModifier* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdb63-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdb63-129">Requirements</span></span>



| <span data-ttu-id="bdb63-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdb63-130">Requirement</span></span> | <span data-ttu-id="bdb63-131">Wert</span><span class="sxs-lookup"><span data-stu-id="bdb63-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdb63-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="bdb63-132">TAPI version</span></span><br/> | <span data-ttu-id="bdb63-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="bdb63-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bdb63-134">Header</span><span class="sxs-lookup"><span data-stu-id="bdb63-134">Header</span></span><br/>       | <dl> <span data-ttu-id="bdb63-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdb63-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="bdb63-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bdb63-136">Library</span></span><br/>      | <dl> <span data-ttu-id="bdb63-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdb63-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bdb63-138">DLL</span><span class="sxs-lookup"><span data-stu-id="bdb63-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="bdb63-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdb63-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdb63-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdb63-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdb63-141">**Itconnection**</span><span class="sxs-lookup"><span data-stu-id="bdb63-141">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

