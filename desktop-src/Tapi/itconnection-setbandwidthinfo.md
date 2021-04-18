---
description: Die setbandwidthinfo-Methode legt die Bandbreiten Informationen fest.
ms.assetid: bf5db456-ea67-4a65-a681-df0741f73fc9
title: 'Itconnection:: setbandwidthinfo-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c17054743f6d47775e994dbfe3b80c7afe1ab68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372313"
---
# <a name="itconnectionsetbandwidthinfo-method"></a><span data-ttu-id="aec3b-103">Itconnection:: setbandwidthinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="aec3b-103">ITConnection::SetBandwidthInfo method</span></span>

<span data-ttu-id="aec3b-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aec3b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="aec3b-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="aec3b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="aec3b-106">Die **setbandwidthinfo** -Methode legt die Bandbreiten Informationen fest.</span><span class="sxs-lookup"><span data-stu-id="aec3b-106">The **SetBandwidthInfo** method sets the bandwidth information.</span></span>

## <a name="syntax"></a><span data-ttu-id="aec3b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="aec3b-107">Syntax</span></span>


```C++
HRESULT SetBandwidthInfo(
  [in] BSTR   pModifier,
  [in] DOUBLE Bandwidth
);
```



## <a name="parameters"></a><span data-ttu-id="aec3b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="aec3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aec3b-109">*pmodifizierer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aec3b-109">*pModifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec3b-110">Zeiger auf ein **BSTR** , das den Bereich der festgelegten Bandbreite angibt.</span><span class="sxs-lookup"><span data-stu-id="aec3b-110">Pointer to a **BSTR** indicating the scope of the bandwidth being set.</span></span> <span data-ttu-id="aec3b-111">Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="aec3b-111">For more information, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="aec3b-112">*Bandbreite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aec3b-112">*Bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec3b-113">Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="aec3b-113">Bandwidth.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aec3b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aec3b-114">Return value</span></span>

<span data-ttu-id="aec3b-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="aec3b-115">This method can return one of these values.</span></span>



| <span data-ttu-id="aec3b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="aec3b-116">Value</span></span>                                                                                         | <span data-ttu-id="aec3b-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="aec3b-117">Meaning</span></span>                                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="aec3b-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aec3b-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="aec3b-119">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="aec3b-119">Method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="aec3b-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="aec3b-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="aec3b-121">Der *pmodifier* -oder *Bandbreiten* Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="aec3b-121">The *pModifier* or *Bandwidth* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="aec3b-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="aec3b-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="aec3b-123">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="aec3b-123">Insufficient memory exists to perform the operation.</span></span><br/>   |
| <dl> <span data-ttu-id="aec3b-124"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="aec3b-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="aec3b-125">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="aec3b-125">Unspecified error.</span></span><br/>                                     |
| <dl> <span data-ttu-id="aec3b-126"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="aec3b-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="aec3b-127">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="aec3b-127">This method is not yet implemented.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="aec3b-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aec3b-128">Remarks</span></span>

<span data-ttu-id="aec3b-129">Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *pmodifier* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="aec3b-129">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pModifier* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="aec3b-130">Referenz: RFC 2327.</span><span class="sxs-lookup"><span data-stu-id="aec3b-130">Reference: RFC 2327.</span></span>

<span data-ttu-id="aec3b-131">Der bandänderungsmodifizierer ist normalerweise entweder CT oder wie folgt:</span><span class="sxs-lookup"><span data-stu-id="aec3b-131">The bandwidth modifier will normally be either CT or AS:</span></span>

<span data-ttu-id="aec3b-132">**Gesamtanzahl der CT-Konferenzen:** Jede Gültigkeits [*Dauer (Time to Live,*](t-tapgloss.md) TTL) auf der MBone oder innerhalb eines bestimmten Multicast Verwaltungsbereichs (in den häufig gestellten Fragen zur MBone-Bandbreite und TTL) ist in den häufig gestellten Fragen zu MBone eine implizite maximale Bandbreite zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="aec3b-132">**CT Conference Total:** An implicit maximum bandwidth is associated with each [*time to live*](t-tapgloss.md) (TTL) on the Mbone or within a particular multicast administrative scope region (the Mbone bandwidth versus TTL limits are given in the MBone FAQ).</span></span> <span data-ttu-id="aec3b-133">Wenn die Bandbreite einer Sitzung oder eines Mediums in einer Sitzung von der im Bereich impliziten Bandbreite abweicht, a \` b = CT:... " die Zeile sollte für die Sitzung angegeben werden, wodurch die vorgeschlagene Obergrenze für die verwendete Bandbreite angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aec3b-133">If the bandwidth of a session or media in a session is different from the bandwidth implicit from the scope, a \`b=CT:...' line should be supplied for the session giving the proposed upper limit to the bandwidth used.</span></span> <span data-ttu-id="aec3b-134">Der Hauptzweck dieses Konzepts besteht darin, eine ungefähre Vorstellung davon zu erhalten, ob zwei oder mehr Konferenzen gleichzeitig nebeneinander existieren können.</span><span class="sxs-lookup"><span data-stu-id="aec3b-134">The primary purpose of this is to give an approximate idea as to whether two or more conferences can coexist simultaneously.</span></span>

<span data-ttu-id="aec3b-135">**Als Application-Specific Maximum:** Die Bandbreite wird als anwendungsspezifisch interpretiert, d. h., es wird das Konzept der maximalen Bandbreite der Anwendung sein.</span><span class="sxs-lookup"><span data-stu-id="aec3b-135">**AS Application-Specific Maximum:** The bandwidth is interpreted to be application-specific, i.e., will be the application's concept of maximum bandwidth.</span></span> <span data-ttu-id="aec3b-136">Normalerweise stimmt dies mit dem fest, was für die "maximale Bandbreite" der Anwendung festgelegt ist, falls zutreffend.</span><span class="sxs-lookup"><span data-stu-id="aec3b-136">Normally this will coincide with what is set on the application's "maximum bandwidth" control, if applicable.</span></span>

<span data-ttu-id="aec3b-137">Beachten Sie, dass CT eine Gesamtbandbreite für alle Medien an allen Standorten liefert.</span><span class="sxs-lookup"><span data-stu-id="aec3b-137">Note that CT gives a total bandwidth figure for all the media at all sites.</span></span> <span data-ttu-id="aec3b-138">Da eine Bandbreiten Abbildung für ein einzelnes Medium an einem einzigen Standort bietet, kann es sein, dass viele Standorte gleichzeitig senden.</span><span class="sxs-lookup"><span data-stu-id="aec3b-138">AS gives a bandwidth figure for a single media at a single site, although there may be many sites sending simultaneously.</span></span>

<span data-ttu-id="aec3b-139">**Erweiterungsmechanismus:** Toolwriter können experimentelle bandänderungsmodifiziererer definieren, indem Sie Ihre modifiziererer mit "X-" versehen.</span><span class="sxs-lookup"><span data-stu-id="aec3b-139">**Extension Mechanism:** Tool writers can define experimental bandwidth modifiers by prefixing their modifiers with "X-".</span></span>

## <a name="requirements"></a><span data-ttu-id="aec3b-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aec3b-140">Requirements</span></span>



| <span data-ttu-id="aec3b-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aec3b-141">Requirement</span></span> | <span data-ttu-id="aec3b-142">Wert</span><span class="sxs-lookup"><span data-stu-id="aec3b-142">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aec3b-143">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="aec3b-143">TAPI version</span></span><br/> | <span data-ttu-id="aec3b-144">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="aec3b-144">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="aec3b-145">Header</span><span class="sxs-lookup"><span data-stu-id="aec3b-145">Header</span></span><br/>       | <dl> <span data-ttu-id="aec3b-146"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="aec3b-146"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="aec3b-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aec3b-147">Library</span></span><br/>      | <dl> <span data-ttu-id="aec3b-148"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aec3b-148"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="aec3b-149">DLL</span><span class="sxs-lookup"><span data-stu-id="aec3b-149">DLL</span></span><br/>          | <dl> <span data-ttu-id="aec3b-150"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aec3b-150"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aec3b-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aec3b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aec3b-152">**Itconnection**</span><span class="sxs-lookup"><span data-stu-id="aec3b-152">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

