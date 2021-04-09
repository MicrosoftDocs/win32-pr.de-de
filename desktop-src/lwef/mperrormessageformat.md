---
title: Mperrormessageformat-Funktion (mpclient. h)
description: Gibt eine formatierte Fehlermeldung auf der Grundlage eines Fehlercodes zurück.
ms.assetid: C125FCE4-3BB0-4608-BBF3-E7FEF17D0807
keywords:
- Mperrormessageformat-Funktion Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MpErrorMessageFormat
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a3499b3be885b29135d22b470da4143cfb23ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957045"
---
# <a name="mperrormessageformat-function"></a><span data-ttu-id="58e01-104">Mperrormessageformat-Funktion</span><span class="sxs-lookup"><span data-stu-id="58e01-104">MpErrorMessageFormat function</span></span>

<span data-ttu-id="58e01-105">Gibt eine formatierte Fehlermeldung auf der Grundlage eines Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="58e01-105">Returns a formatted error message based on an error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="58e01-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="58e01-106">Syntax</span></span>


```C++
HRESULT WINAPI MpErrorMessageFormat(
  _In_  MPHANDLE hMpHandle,
  _In_  HRESULT  hrError,
  _Out_ LPWSTR   *pwszErrorDesc
);
```



## <a name="parameters"></a><span data-ttu-id="58e01-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="58e01-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58e01-108">*hmphandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58e01-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58e01-109">Typ: **mphandle**</span><span class="sxs-lookup"><span data-stu-id="58e01-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="58e01-110">Handle für die Malware Protection Manager-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="58e01-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="58e01-111">Dieses Handle wird von der [**mpmanageropen**](mpmanageropen.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="58e01-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="58e01-112">*hrError* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58e01-112">*hrError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58e01-113">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="58e01-113">Type: **HRESULT**</span></span>

<span data-ttu-id="58e01-114">Ein **HRESULT**-basierter Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="58e01-114">An **HRESULT**-based error code.</span></span>

</dd> <dt>

<span data-ttu-id="58e01-115">*pwszerrorde SC* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="58e01-115">*pwszErrorDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58e01-116">Typ: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="58e01-116">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="58e01-117">Gibt eine formatierte Fehlermeldung zurück, die auf _hrError \* basiert.</span><span class="sxs-lookup"><span data-stu-id="58e01-117">Returns a formatted error message based on _hrError\*.</span></span> <span data-ttu-id="58e01-118">Diese Zeichenfolge muss mithilfe von [**mpfrememory**](mpfreememory.md)freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="58e01-118">This string must be freed using [**MpFreeMemory**](mpfreememory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58e01-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58e01-119">Return value</span></span>

<span data-ttu-id="58e01-120">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="58e01-120">Type: **HRESULT**</span></span>

<span data-ttu-id="58e01-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="58e01-121">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="58e01-122">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code.</span><span class="sxs-lookup"><span data-stu-id="58e01-122">If the function fails then the return value is a failed **HRESULT** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="58e01-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58e01-123">Remarks</span></span>

<span data-ttu-id="58e01-124">Diese Funktion ist in der Lage, Systemfehler Codes zusätzlich zu bestimmten Fehlercodes zu formatieren, die von Malware Schutzfunktionen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="58e01-124">This function is capable of formatting system error codes in addition to specific error codes returned by malware protection functions.</span></span> <span data-ttu-id="58e01-125">Die **HRESULT** -Fehlercodes, die für Malware Schutzfunktionen spezifisch sind, haben die Funktion 0x50.</span><span class="sxs-lookup"><span data-stu-id="58e01-125">The **HRESULT** error codes specific to malware protection functions have a facility of 0x50.</span></span> <span data-ttu-id="58e01-126">Im folgenden finden Sie eine Liste einer Teilmenge der Malware Schutz spezifischen Fehlercodes, die von verschiedenen Malware Schutzfunktionen zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="58e01-126">Below is a list of a subset of the malware protection-specific error codes that can be returned by various malware protection functions.</span></span> <span data-ttu-id="58e01-127">Die folgenden Fehlercodes können mit dem Makro **HRESULT \_ aus \_ MP- \_ Status** in **HRESULT** konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="58e01-127">Using the macro **HRESULT\_FROM\_MP\_STATUS**, the following error codes can be converted to **HRESULT**.</span></span> <span data-ttu-id="58e01-128">Eine Liste mit anderen möglichen Fehlercodes finden Sie auch in den [Fehlercodes für die Antischadsoftware-Engine von Forefront Client Security](https://support.microsoft.com/kb/939359) .</span><span class="sxs-lookup"><span data-stu-id="58e01-128">See also [Forefront Client Security anti-malware engine error codes](https://support.microsoft.com/kb/939359) for a list of other possible error codes.</span></span>



| <span data-ttu-id="58e01-129">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="58e01-129">Error Code</span></span>                              | <span data-ttu-id="58e01-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58e01-130">Description</span></span>                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58e01-131">Fehler- \_ MP- \_ noengine</span><span class="sxs-lookup"><span data-stu-id="58e01-131">ERROR\_MP\_NOENGINE</span></span>                     | <span data-ttu-id="58e01-132">Es wurde keine Engine in den antischadsoftwaredienst geladen, um den angeforderten Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="58e01-132">No engine is loaded in antimalware service to perform the requested operation.</span></span>                                              |
| <span data-ttu-id="58e01-133">Fehler \_ MP " \_ kein Arbeits \_ Speicher"</span><span class="sxs-lookup"><span data-stu-id="58e01-133">ERROR\_MP\_NO\_MEMORY</span></span>                   | <span data-ttu-id="58e01-134">Die Antischadsoftware-Engine hat eine nicht genügend Arbeitsspeicher Situation gefunden.</span><span class="sxs-lookup"><span data-stu-id="58e01-134">The antimalware engine has encountered a no memory situation.</span></span>                                                               |
| <span data-ttu-id="58e01-135">Fehler beim \_ Entfernen des MP-Fehlers \_ \_</span><span class="sxs-lookup"><span data-stu-id="58e01-135">ERROR\_MP\_REMOVE\_FAILED</span></span>               | <span data-ttu-id="58e01-136">Fehler beim Entfernungs Vorgang für eine bestimmte Bedrohung.</span><span class="sxs-lookup"><span data-stu-id="58e01-136">Remove operation failed for a specific threat.</span></span>                                                                              |
| <span data-ttu-id="58e01-137">Fehler bei \_ MP- \_ Quarantäne. \_</span><span class="sxs-lookup"><span data-stu-id="58e01-137">ERROR\_MP\_QUARANTINE\_FAILED</span></span>           | <span data-ttu-id="58e01-138">Der Quarantäne Vorgang konnte für eine bestimmte Bedrohung nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="58e01-138">Quarantine operation failed for a specific threat.</span></span>                                                                          |
| <span data-ttu-id="58e01-139">Fehler- \_ MP- \_ Bedrohung \_ nicht \_ gefunden.</span><span class="sxs-lookup"><span data-stu-id="58e01-139">ERROR\_MP\_THREAT\_NOT\_FOUND</span></span>           | <span data-ttu-id="58e01-140">Die spezifische Bedrohung ist im System nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="58e01-140">The specific threat no longer exists in the system.</span></span>                                                                         |
| <span data-ttu-id="58e01-141">Fehler \_ beim \_ Entfernen von MP \_ nicht \_ unterstützt</span><span class="sxs-lookup"><span data-stu-id="58e01-141">ERROR\_MP\_REMOVE\_NOT\_SUPPORTED</span></span>       | <span data-ttu-id="58e01-142">Der Entfernungs Vorgang für eine bestimmte Bedrohung innerhalb des Container Typs wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58e01-142">Remove operation for a specific threat inside the container type is not supported.</span></span>                                          |
| <span data-ttu-id="58e01-143">Fehler \_ MP \_ Entfernen eines \_ unveränderlichen \_ Containers</span><span class="sxs-lookup"><span data-stu-id="58e01-143">ERROR\_MP\_REMOVE\_IMMUTABLE\_CONTAINER</span></span> | <span data-ttu-id="58e01-144">Aufgrund der Engine-Richtlinie wird ein Entfernungs Vorgang einer bestimmten Bedrohung in einem blockierten Container nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58e01-144">Due to engine policy, a remove operation of a specific threat inside a blocked container is not supported.</span></span> <span data-ttu-id="58e01-145">(E-Mail-Archive.)</span><span class="sxs-lookup"><span data-stu-id="58e01-145">(Mail archives.)</span></span> |
| <span data-ttu-id="58e01-146">Fehler \_ MP \_ baddb \_ oldengine</span><span class="sxs-lookup"><span data-stu-id="58e01-146">ERROR\_MP\_BADDB\_OLDENGINE</span></span>             | <span data-ttu-id="58e01-147">Die Signatur Aktualisierungs Anforderung hat eine ältere Engine oder Signatur Dateien bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="58e01-147">Signature update request provided an older engine or signature files(s).</span></span>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="58e01-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58e01-148">Requirements</span></span>



| <span data-ttu-id="58e01-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58e01-149">Requirement</span></span> | <span data-ttu-id="58e01-150">Wert</span><span class="sxs-lookup"><span data-stu-id="58e01-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58e01-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58e01-151">Minimum supported client</span></span><br/> | <span data-ttu-id="58e01-152">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58e01-152">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="58e01-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58e01-153">Minimum supported server</span></span><br/> | <span data-ttu-id="58e01-154">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58e01-154">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="58e01-155">Header</span><span class="sxs-lookup"><span data-stu-id="58e01-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="58e01-156"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="58e01-156"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="58e01-157">DLL</span><span class="sxs-lookup"><span data-stu-id="58e01-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58e01-158"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58e01-158"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58e01-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58e01-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e01-160">**Mpfrememory**</span><span class="sxs-lookup"><span data-stu-id="58e01-160">**MpFreeMemory**</span></span>](mpfreememory.md)
</dt> <dt>

[<span data-ttu-id="58e01-161">**Mpmanageropen**</span><span class="sxs-lookup"><span data-stu-id="58e01-161">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="58e01-162">Fehlercodes der Antischadsoftware-Engine für Forefront Client Security</span><span class="sxs-lookup"><span data-stu-id="58e01-162">Forefront Client Security anti-malware engine error codes</span></span>](https://support.microsoft.com/kb/939359)
</dt> </dl>

 

 





