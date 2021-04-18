---
title: Mpbedrohlich Open-Funktion (mpclient. h)
description: Gibt ein enumerationshandle zum Abrufen von Bedrohungen zurück.
ms.assetid: E1178F0C-E9C0-4532-AE9B-452770600DF2
keywords:
- Mpbedrohlich Open-Funktion Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MpThreatOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca30435f9d7cba32771a2445d8a1156f0edaa9b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339984"
---
# <a name="mpthreatopen-function"></a><span data-ttu-id="4b63c-104">Mpbedrohlich Open-Funktion</span><span class="sxs-lookup"><span data-stu-id="4b63c-104">MpThreatOpen function</span></span>

<span data-ttu-id="4b63c-105">Gibt ein enumerationshandle zum Abrufen von Bedrohungen zurück.</span><span class="sxs-lookup"><span data-stu-id="4b63c-105">Returns an enumeration handle for the purpose of retrieving threats.</span></span> <span data-ttu-id="4b63c-106">Diese Funktion kann verwendet werden, um von einer bestimmten Überprüfung erkannte Bedrohungen, alle aktiven Bedrohungen im System, den Verlauf der Bedrohungs Desinfektion oder alle Bedrohungen in der Signaturdatenbank zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4b63c-106">This function can be used to open threats detected by a specific scan, all the active threats in the system, the history of threat disinfection, or all the threats present in the signature database.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b63c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b63c-107">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatOpen(
  _In_  MPHANDLE        hScanHandle,
  _In_  MPTHREAT_SOURCE ThreatSource,
  _In_  MPTHREAT_TYPE   ThreatType,
  _Out_ PMPHANDLE       phThreatEnumHandle
);
```



## <a name="parameters"></a><span data-ttu-id="4b63c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b63c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b63c-109">*hscanhandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b63c-109">*hScanHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b63c-110">Typ: **mphandle**</span><span class="sxs-lookup"><span data-stu-id="4b63c-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="4b63c-111">Kann ein Handle für einen abgeschlossenen Scanvorgang sein, der von der [**mpscanstart**](mpscanstart.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4b63c-111">Can be a handle to a completed scan operation, returned by the [**MpScanStart**](mpscanstart.md) function.</span></span> <span data-ttu-id="4b63c-112">Alternativ kann dieser Parameter auf das von [**mpmanageropen**](mpmanageropen.md) zurückgegebene Malware Protection Manager-Schnittstellen handle festgelegt werden, um alle aktiven Bedrohungen im System, den Verlauf der Bedrohungs Desinfektion oder Bedrohungen aus der Signaturdatenbank aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="4b63c-112">Alternately, this parameter can be set to the malware protection manager interface handle returned by [**MpManagerOpen**](mpmanageropen.md) to enumerate all active threats in the system, the history of threat disinfection, or threats from signature database.</span></span>

</dd> <dt>

<span data-ttu-id="4b63c-113">*Quelle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b63c-113">*ThreatSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b63c-114">Typ: **mpthreat- \_ Quelle**</span><span class="sxs-lookup"><span data-stu-id="4b63c-114">Type: **MPTHREAT\_SOURCE**</span></span>

<span data-ttu-id="4b63c-115">Wird verwendet, um die Quelle der Bedrohungs Aufzählung zu steuern.</span><span class="sxs-lookup"><span data-stu-id="4b63c-115">Used to control the source of threat enumeration.</span></span> <span data-ttu-id="4b63c-116">Die möglichen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4b63c-116">The possible values for this parameter are:</span></span>



| <span data-ttu-id="4b63c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4b63c-117">Value</span></span>                                                                                                                                                                                                 | <span data-ttu-id="4b63c-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4b63c-118">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_SOURCE_SCAN"></span><span id="mpthreat_source_scan"></span><dl> <span data-ttu-id="4b63c-119"><dt>**mpthreat- \_ Quell \_ Scan**</dt></span><span class="sxs-lookup"><span data-stu-id="4b63c-119"><dt>**MPTHREAT\_SOURCE\_SCAN**</dt></span></span> </dl>                   | <span data-ttu-id="4b63c-120">Bedrohungen, die dem jeweiligen Scan Handle zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4b63c-120">Threats that are associated with the specific scan handle.</span></span><br/>                                              |
| <span id="MPTHREAT_SOURCE_ACTIVE"></span><span id="mpthreat_source_active"></span><dl> <span data-ttu-id="4b63c-121"><dt>**mpthreat- \_ Quelle \_ aktiv**</dt></span><span class="sxs-lookup"><span data-stu-id="4b63c-121"><dt>**MPTHREAT\_SOURCE\_ACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="4b63c-122">Bedrohungen, die derzeit im System aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="4b63c-122">Threats that are currently active in the system.</span></span><br/>                                                        |
| <span id="MPTHREAT_SOURCE_HISTORY"></span><span id="mpthreat_source_history"></span><dl> <span data-ttu-id="4b63c-123"><dt>**mpthreat- \_ Quell \_ Verlauf**</dt></span><span class="sxs-lookup"><span data-stu-id="4b63c-123"><dt>**MPTHREAT\_SOURCE\_HISTORY**</dt></span></span> </dl>          | <span data-ttu-id="4b63c-124">Bedrohungen, die als Verlauf behandelt und beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="4b63c-124">Threats that are acted upon and preserved as a history.</span></span><br/>                                                 |
| <span id="MPTHREAT_SOURCE_QUARANTINE"></span><span id="mpthreat_source_quarantine"></span><dl> <span data-ttu-id="4b63c-125"><dt>**\_Quellen Quarantäne für mpthreat \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4b63c-125"><dt>**MPTHREAT\_SOURCE\_QUARANTINE**</dt></span></span> </dl> | <span data-ttu-id="4b63c-126">Bedrohungen, die unter Quarantäne gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4b63c-126">Threats that are quarantined.</span></span><br/>                                                                           |
| <span id="MPTHREAT_SOURCE_SIGNATURE"></span><span id="mpthreat_source_signature"></span><dl> <span data-ttu-id="4b63c-127"><dt>**mpthreat- \_ Quell \_ Signatur**</dt></span><span class="sxs-lookup"><span data-stu-id="4b63c-127"><dt>**MPTHREAT\_SOURCE\_SIGNATURE**</dt></span></span> </dl>    | <span data-ttu-id="4b63c-128">Bedrohungen, die mit der aktuellen Signaturdatenbank erkannt werden können.</span><span class="sxs-lookup"><span data-stu-id="4b63c-128">Threats that are possible to detect with the current signature database.</span></span><br/>                                |
| <span id="MPTHREAT_SOURCE_STATE"></span><span id="mpthreat_source_state"></span><dl> <span data-ttu-id="4b63c-129"><dt>**mpthreat- \_ Quell \_ Status**</dt></span><span class="sxs-lookup"><span data-stu-id="4b63c-129"><dt>**MPTHREAT\_SOURCE\_STATE**</dt></span></span> </dl>                | <span data-ttu-id="4b63c-130">Bedrohungen, die vor kurzem bearbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="4b63c-130">Threats that have been acted upon recently.</span></span> <span data-ttu-id="4b63c-131">("Kürzlich" wird durch eine konfigurierbare interne Einstellung definiert.)</span><span class="sxs-lookup"><span data-stu-id="4b63c-131">("Recently" is defined by a configurable internal setting.)</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4b63c-132">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b63c-132">*ThreatType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b63c-133">Typ: **mpthreat- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="4b63c-133">Type: **MPTHREAT\_TYPE**</span></span>

<span data-ttu-id="4b63c-134">Wird verwendet, um aufgelistete Bedrohungen basierend auf dem Erkennungs Typ zu filtern.</span><span class="sxs-lookup"><span data-stu-id="4b63c-134">Used to filter enumerated threats based on the detection type.</span></span> <span data-ttu-id="4b63c-135">Die möglichen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4b63c-135">The possible values for this parameter are:</span></span>



| <span data-ttu-id="4b63c-136">Wert</span><span class="sxs-lookup"><span data-stu-id="4b63c-136">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="4b63c-137">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4b63c-137">Meaning</span></span>                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span><dl> <span data-ttu-id="4b63c-138"><dt>**mpthreat- \_ Typ \_ knownbad**</dt></span><span class="sxs-lookup"><span data-stu-id="4b63c-138"><dt>**MPTHREAT\_TYPE\_KNOWNBAD**</dt></span></span> </dl>       | <span data-ttu-id="4b63c-139">Die Erkennung erfolgt basierend auf einer bestimmten Signatur, Emulation oder anderen Bedrohungs Erkennungsmethode.</span><span class="sxs-lookup"><span data-stu-id="4b63c-139">Detection is performed based on a specific signature, emulation, or other threat detection method.</span></span><br/> |
| <span id="MPTHREAT_TYPE_SUSPICIOUS"></span><span id="mpthreat_type_suspicious"></span><dl> <span data-ttu-id="4b63c-140"><dt>**mpthreat- \_ Typ \_ verdächtig**</dt></span><span class="sxs-lookup"><span data-stu-id="4b63c-140"><dt>**MPTHREAT\_TYPE\_SUSPICIOUS**</dt></span></span> </dl> | <span data-ttu-id="4b63c-141">Die Erkennung erfolgt basierend auf der Verhaltens Überwachung.</span><span class="sxs-lookup"><span data-stu-id="4b63c-141">Detection is performed based on behavior monitoring.</span></span><br/>                                               |
| <span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span><dl> <span data-ttu-id="4b63c-142"><dt>**mpthreat- \_ Typ \_ unbekannt**</dt></span><span class="sxs-lookup"><span data-stu-id="4b63c-142"><dt>**MPTHREAT\_TYPE\_UNKNOWN**</dt></span></span> </dl>          | <span data-ttu-id="4b63c-143">Die Erkennung erfolgt basierend auf unbekannten Bedrohungen (nicht klassifiziert).</span><span class="sxs-lookup"><span data-stu-id="4b63c-143">Detection is performed based on unknown threats (unclassified).</span></span><br/>                                    |
| <span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span><dl> <span data-ttu-id="4b63c-144"><dt>**mpthreat- \_ Typ \_ knowngood**</dt></span><span class="sxs-lookup"><span data-stu-id="4b63c-144"><dt>**MPTHREAT\_TYPE\_KNOWNGOOD**</dt></span></span> </dl>    | <span data-ttu-id="4b63c-145">Die Erkennung erfolgt basierend auf bekannten sicheren Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="4b63c-145">Detection is performed based on known safe threats.</span></span><br/>                                                |
| <span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span><dl> <span data-ttu-id="4b63c-146"><dt>**mpthreat- \_ Typ \_ NIS**</dt></span><span class="sxs-lookup"><span data-stu-id="4b63c-146"><dt>**MPTHREAT\_TYPE\_NIS**</dt></span></span> </dl>                      | <span data-ttu-id="4b63c-147">Die Erkennung erfolgt basierend auf NIS-Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="4b63c-147">Detection is performed based on NIS threats.</span></span><br/>                                                       |



 

</dd> <dt>

<span data-ttu-id="4b63c-148">*phbedrohlich-enumhandle* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4b63c-148">*phThreatEnumHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b63c-149">Typ: **pmphandle**</span><span class="sxs-lookup"><span data-stu-id="4b63c-149">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="4b63c-150">Rückgabe Handle für Bedrohungs Enumeration, das den enumerationskontext identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4b63c-150">Returned threat enumeration handle which identifies the enumeration context.</span></span> <span data-ttu-id="4b63c-151">Dieses Handle kann zum Auflisten von Bedrohungs Informationen mithilfe von [**mpgefährenumerate**](mpthreatenumerate.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b63c-151">This handle can be used to enumerate threat information using [**MpThreatEnumerate**](mpthreatenumerate.md).</span></span> <span data-ttu-id="4b63c-152">Das Handle muss mit der [**mplenker close**](mphandleclose.md) -Funktion geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="4b63c-152">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b63c-153">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4b63c-153">Return value</span></span>

<span data-ttu-id="4b63c-154">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4b63c-154">Type: **HRESULT**</span></span>

<span data-ttu-id="4b63c-155">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4b63c-155">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="4b63c-156">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code.</span><span class="sxs-lookup"><span data-stu-id="4b63c-156">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="4b63c-157">Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4b63c-157">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b63c-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b63c-158">Requirements</span></span>



| <span data-ttu-id="4b63c-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b63c-159">Requirement</span></span> | <span data-ttu-id="4b63c-160">Wert</span><span class="sxs-lookup"><span data-stu-id="4b63c-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b63c-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b63c-161">Minimum supported client</span></span><br/> | <span data-ttu-id="4b63c-162">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b63c-162">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="4b63c-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b63c-163">Minimum supported server</span></span><br/> | <span data-ttu-id="4b63c-164">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b63c-164">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4b63c-165">Header</span><span class="sxs-lookup"><span data-stu-id="4b63c-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b63c-166"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b63c-166"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="4b63c-167">DLL</span><span class="sxs-lookup"><span data-stu-id="4b63c-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b63c-168"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b63c-168"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b63c-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b63c-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b63c-170">**Mperrormessageformat**</span><span class="sxs-lookup"><span data-stu-id="4b63c-170">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="4b63c-171">**Mplenker schließen**</span><span class="sxs-lookup"><span data-stu-id="4b63c-171">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="4b63c-172">**Mpmanageropen**</span><span class="sxs-lookup"><span data-stu-id="4b63c-172">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="4b63c-173">**Mpscanstart**</span><span class="sxs-lookup"><span data-stu-id="4b63c-173">**MpScanStart**</span></span>](mpscanstart.md)
</dt> <dt>

[<span data-ttu-id="4b63c-174">**Mpzerenumerate**</span><span class="sxs-lookup"><span data-stu-id="4b63c-174">**MpThreatEnumerate**</span></span>](mpthreatenumerate.md)
</dt> </dl>

 

 





