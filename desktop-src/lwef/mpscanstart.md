---
title: Mpscanstart-Funktion (mpclient. h)
description: Startet einen Scanvorgang.
ms.assetid: 3AF147C8-A41F-4193-AE28-72C1FBD18BA2
keywords:
- Mpscanstart-Funktion Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MpScanStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d343787edc85a18dc7471d19165999a7252d18a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956735"
---
# <a name="mpscanstart-function"></a><span data-ttu-id="21d25-104">Mpscanstart-Funktion</span><span class="sxs-lookup"><span data-stu-id="21d25-104">MpScanStart function</span></span>

<span data-ttu-id="21d25-105">Startet einen Scanvorgang.</span><span class="sxs-lookup"><span data-stu-id="21d25-105">Starts a scanning operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="21d25-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="21d25-106">Syntax</span></span>


```C++
HRESULT WINAPI MpScanStart(
  _In_     MPHANDLE          hMpHandle,
  _In_     MPSCAN_TYPE       ScanType,
  _In_     DWORD             dwScanOptions,
  _In_opt_ PMPSCAN_RESOURCES pScanResources,
  _In_opt_ PMPCALLBACK_INFO  pCallbackInfo,
  _Out_    PMPHANDLE         phScanHandle
);
```



## <a name="parameters"></a><span data-ttu-id="21d25-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="21d25-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21d25-108">*hmphandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21d25-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21d25-109">Typ: **mphandle**</span><span class="sxs-lookup"><span data-stu-id="21d25-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="21d25-110">Handle für die Malware Protection Manager-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="21d25-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="21d25-111">Dieses Handle wird von der [**mpmanageropen**](mpmanageropen.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="21d25-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="21d25-112">*ScanType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21d25-112">*ScanType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21d25-113">Typ: **[ **mpscan- \_ Typ**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="21d25-113">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

<span data-ttu-id="21d25-114">Gibt den Typ des Scanvorgangs an.</span><span class="sxs-lookup"><span data-stu-id="21d25-114">Specifies the type of scan.</span></span> <span data-ttu-id="21d25-115">Dieser Parameter muss einer der Member der [**mpscan- \_ Typenumeration**](mpscan-type.md) sein.</span><span class="sxs-lookup"><span data-stu-id="21d25-115">This parameter must be one of the members of the [**MPSCAN\_TYPE**](mpscan-type.md) enueration.</span></span>

</dd> <dt>

<span data-ttu-id="21d25-116">*dwscanoptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21d25-116">*dwScanOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21d25-117">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="21d25-117">Type: **DWORD**</span></span>

<span data-ttu-id="21d25-118">Gibt verschiedene Optionen für den Scanvorgang an.</span><span class="sxs-lookup"><span data-stu-id="21d25-118">Specifies various options for scanning operation.</span></span>



| <span data-ttu-id="21d25-119">Wert</span><span class="sxs-lookup"><span data-stu-id="21d25-119">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="21d25-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="21d25-120">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPSCAN_OPTION_NONE"></span><span id="mpscan_option_none"></span><dl> <span data-ttu-id="21d25-121"><dt>**mpscan- \_ Option " \_ None"**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-121"><dt>**MPSCAN\_OPTION\_NONE**</dt></span></span> </dl>                               | <span data-ttu-id="21d25-122">Eine bestimmte Option wird nicht angefordert.</span><span class="sxs-lookup"><span data-stu-id="21d25-122">No specific option is requested.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_ASYNC"></span><span id="mpscan_option_async"></span><dl> <span data-ttu-id="21d25-123"><dt>**mpscan- \_ Option " \_ Async"**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-123"><dt>**MPSCAN\_OPTION\_ASYNC**</dt></span></span> </dl>                            | <span data-ttu-id="21d25-124">Der Scanvorgang wird asynchron ausgeführt, wobei **mpscanstart** sofort nach der erfolgreichen Initiierung des Scans zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="21d25-124">The scan operation is to be asynchronous, where **MpScanStart** returns immediately after the successful initiation of scanning.</span></span> <span data-ttu-id="21d25-125">(Der Scanvorgang ist standardmäßig synchron, was bedeutet, dass **mpscanstart** erst zurückgegeben wird, nachdem die Überprüfung abgeschlossen ist.)</span><span class="sxs-lookup"><span data-stu-id="21d25-125">(By default the scan operation is synchronous, meaning **MpScanStart** will return only after the scan is finished.)</span></span><br/>      |
| <span id="MPSCAN_OPTION_PROGRESS"></span><span id="mpscan_option_progress"></span><dl> <span data-ttu-id="21d25-126"><dt>**mpscan- \_ options Status \_**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-126"><dt>**MPSCAN\_OPTION\_PROGRESS**</dt></span></span> </dl>                   | <span data-ttu-id="21d25-127">Der Aufrufer ist daran interessiert, Informationen über den Scan Status über einen Rückruf zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="21d25-127">The caller is interested in receiving scan progress information via a callback.</span></span><br/>                                                                                                                                                                            |
| <span id="MPSCAN_OPTION_LOWPRIORITY"></span><span id="mpscan_option_lowpriority"></span><dl> <span data-ttu-id="21d25-128"><dt>**mpscan- \_ Option \_ LowPriority**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-128"><dt>**MPSCAN\_OPTION\_LOWPRIORITY**</dt></span></span> </dl>          | <span data-ttu-id="21d25-129">Führen Sie die Überprüfung mit niedriger Priorität aus.</span><span class="sxs-lookup"><span data-stu-id="21d25-129">Perform the scan with low priority.</span></span> <span data-ttu-id="21d25-130">(Standardmäßig wird der Scanvorgang mit normaler Priorität ausgeführt.)</span><span class="sxs-lookup"><span data-stu-id="21d25-130">(By default the scan operation is performed with normal priority.)</span></span><br/>                                                                                                                                                     |
| <span id="MPSCAN_OPTION_PACKEDEXES"></span><span id="mpscan_option_packedexes"></span><dl> <span data-ttu-id="21d25-131"><dt>**mpscan- \_ Option \_ packedexes**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-131"><dt>**MPSCAN\_OPTION\_PACKEDEXES**</dt></span></span> </dl>             | <span data-ttu-id="21d25-132">Scannen Sie gepackte ausführbare Dateien auf mögliche Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="21d25-132">Scan packed executables for possible threats.</span></span><br/>                                                                                                                                                                                                              |
| <span id="MPSCAN_OPTION_ARCHIVES"></span><span id="mpscan_option_archives"></span><dl> <span data-ttu-id="21d25-133"><dt>**mpscan- \_ options \_ Archive**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-133"><dt>**MPSCAN\_OPTION\_ARCHIVES**</dt></span></span> </dl>                   | <span data-ttu-id="21d25-134">Scannen Sie Archivinhalte auf mögliche Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="21d25-134">Scan archive contents for possible threats.</span></span> <span data-ttu-id="21d25-135">Archive sind Dateien mit Erweiterungen wie ZIP, CAB oder tar.</span><span class="sxs-lookup"><span data-stu-id="21d25-135">Archives are files with extensions such as .zip, .cab, or .tar.</span></span><br/>                                                                                                                                                |
| <span id="MPSCAN_OPTION_HEURISTICS"></span><span id="mpscan_option_heuristics"></span><dl> <span data-ttu-id="21d25-136"><dt>**mpscan- \_ options \_ Heuristik**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-136"><dt>**MPSCAN\_OPTION\_HEURISTICS**</dt></span></span> </dl>             | <span data-ttu-id="21d25-137">Aktivieren der Heuristik-basierten Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="21d25-137">Enable heuristics-based scanning.</span></span> <span data-ttu-id="21d25-138">Dadurch wird nach Bedrohungen gesucht, deren Erkennungstyp auf Heuristik festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="21d25-138">This will scan for threats with detection type set to heuristics.</span></span><br/>                                                                                                                                                        |
| <span id="MPSCAN_OPTION_REPORTFRIENDLY"></span><span id="mpscan_option_reportfriendly"></span><dl> <span data-ttu-id="21d25-139"><dt>**mpscan- \_ Option \_ Report Friendly**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-139"><dt>**MPSCAN\_OPTION\_REPORTFRIENDLY**</dt></span></span> </dl> | <span data-ttu-id="21d25-140">Melden Sie freundliche Elemente in einem Ressourcen Scan.</span><span class="sxs-lookup"><span data-stu-id="21d25-140">Report friendly items in a resource scan.</span></span> <span data-ttu-id="21d25-141">Dies ist nur für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="21d25-141">This is intended for internal use only.</span></span><br/>                                                                                                                                                                          |
| <span id="MPSCAN_OPTION_REPORTUNKNOWN"></span><span id="mpscan_option_reportunknown"></span><dl> <span data-ttu-id="21d25-142"><dt>**mpscan- \_ Option \_ Report Unknown**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-142"><dt>**MPSCAN\_OPTION\_REPORTUNKNOWN**</dt></span></span> </dl>    | <span data-ttu-id="21d25-143">Unbekannte Elemente in einem Ressourcen Scan melden.</span><span class="sxs-lookup"><span data-stu-id="21d25-143">Report unknown items in a resource scan.</span></span> <span data-ttu-id="21d25-144">Dies ist nur für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="21d25-144">This is intended for internal use only.</span></span><br/>                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_NOCONSOLIDATE"></span><span id="mpscan_option_noconsolidate"></span><dl> <span data-ttu-id="21d25-145"><dt>**mpscan- \_ Option \_ nokonsolidieren**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-145"><dt>**MPSCAN\_OPTION\_NOCONSOLIDATE**</dt></span></span> </dl>    | <span data-ttu-id="21d25-146">Konsolidieren Sie die Scanergebnisse nicht mit der globalen Bedrohungs Ansicht.</span><span class="sxs-lookup"><span data-stu-id="21d25-146">Do not consolidate scan results with global threat view.</span></span> <span data-ttu-id="21d25-147">Dies ist nützlich für einen Client (z. b. einen e-Mail-Client), der die Bereinigungs-UX allein steuern möchte, anstatt die standardmäßige Antischadsoftware-Reinigungs UX zuzulassen</span><span class="sxs-lookup"><span data-stu-id="21d25-147">This is useful for a client (such as an email client) which wants to control cleaning UX by itself rather than allowing default anti-malware cleaning UX.</span></span> <span data-ttu-id="21d25-148">Dies ist nur für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="21d25-148">This is intended for internal use only.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="21d25-149">*pscanresources* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="21d25-149">*pScanResources* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="21d25-150">Typ: **pmpscan- \_ Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="21d25-150">Type: **PMPSCAN\_RESOURCES**</span></span>

<span data-ttu-id="21d25-151">Ein Zeiger auf die Scan Ressourcen Informationen.</span><span class="sxs-lookup"><span data-stu-id="21d25-151">A pointer to the scan resource information.</span></span> <span data-ttu-id="21d25-152">Dieser Parameter muss für eine schnell Überprüfung **null** sein.</span><span class="sxs-lookup"><span data-stu-id="21d25-152">This parameter must be **NULL** for a quick scan.</span></span> <span data-ttu-id="21d25-153">Dies ist ein optionaler Parameter für eine vollständige Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="21d25-153">This is an optional parameter for a full scan.</span></span> <span data-ttu-id="21d25-154">Für einen Ressourcen Scan muss dieser Parameter mit mindestens einer Ressourcen Informationsstruktur angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="21d25-154">For a resource scan this parameter must be specified with at least one resource information structure.</span></span> <span data-ttu-id="21d25-155">Um bestimmte Ressourcen zu scannen, muss der Aufrufer über eine **generische \_ Lese** Berechtigung für die Ressource verfügen.</span><span class="sxs-lookup"><span data-stu-id="21d25-155">To scan specific resources the caller must have **GENERIC\_READ** permission for the resource.</span></span> <span data-ttu-id="21d25-156">Siehe [**mpscan- \_ Ressourcen**](mpscan-resources.md).</span><span class="sxs-lookup"><span data-stu-id="21d25-156">See [**MPSCAN\_RESOURCES**](mpscan-resources.md).</span></span>

</dd> <dt>

<span data-ttu-id="21d25-157">*pcallbackinfo* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="21d25-157">*pCallbackInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="21d25-158">Typ: **pmpcallback- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="21d25-158">Type: **PMPCALLBACK\_INFO**</span></span>

<span data-ttu-id="21d25-159">Ein Zeiger auf die Rückruf Informationen, die verwendet werden, um den Client mit Änderungen des Scan Zustands (z. b. Start und Complete) und Statusinformationen zu Feeds.</span><span class="sxs-lookup"><span data-stu-id="21d25-159">A pointer to the callback information used to feed the client with scan state changes (such as start and complete) and progress information.</span></span> <span data-ttu-id="21d25-160">Die [**mpcallback- \_ Daten**](mpcallback-data.md) , die in der Rückruffunktion zurückgegeben werden, melden den tatsächlichen Überprüfungs Zustand und die Status bezogenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="21d25-160">The [**MPCALLBACK\_DATA**](mpcallback-data.md) passed back in the callback function reports actual scan state and progress-related information.</span></span> <span data-ttu-id="21d25-161">Im folgenden finden Sie eine Liste möglicher Rückrufe:</span><span class="sxs-lookup"><span data-stu-id="21d25-161">The following is a list of possible callbacks:</span></span>



| <span data-ttu-id="21d25-162">Wert</span><span class="sxs-lookup"><span data-stu-id="21d25-162">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="21d25-163">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="21d25-163">Meaning</span></span>                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span><dl> <span data-ttu-id="21d25-164"><dt>**mpnotify- \_ Scan \_ Start**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-164"><dt>**MPNOTIFY\_SCAN\_START**</dt></span></span> </dl>                            | <span data-ttu-id="21d25-165">Der Scan Vorgang wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="21d25-165">Scan operation started.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span><dl> <span data-ttu-id="21d25-166"><dt>**mpnotify- \_ Scan ist \_ beendet**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-166"><dt>**MPNOTIFY\_SCAN\_COMPLETE**</dt></span></span> </dl>                   | <span data-ttu-id="21d25-167">Der Scan Vorgang wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="21d25-167">Scan operation completed.</span></span> <span data-ttu-id="21d25-168">Zusätzliche Informationen sind über die [**mpscan- \_ Daten**](mpscan-data.md) Struktur verfügbar.</span><span class="sxs-lookup"><span data-stu-id="21d25-168">Additional information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span><dl> <span data-ttu-id="21d25-169"><dt>**mpnotify- \_ Scan \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-169"><dt>**MPNOTIFY\_SCAN\_PAUSED**</dt></span></span> </dl>                         | <span data-ttu-id="21d25-170">Der Scan Vorgang wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="21d25-170">Scan operation is paused.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span><dl> <span data-ttu-id="21d25-171"><dt>**mpnotify-Scan wird fortgesetzt \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-171"><dt>**MPNOTIFY\_SCAN\_RESUMED**</dt></span></span> </dl>                      | <span data-ttu-id="21d25-172">Der Scan Vorgang wurde von der Pause fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="21d25-172">Scan operation resumed from pause.</span></span><br/>                                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span><dl> <span data-ttu-id="21d25-173"><dt>**mpnotify- \_ Scan \_ Abbruch**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-173"><dt>**MPNOTIFY\_SCAN\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="21d25-174">Der Scan Vorgang wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="21d25-174">Scan operation was cancelled.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span><dl> <span data-ttu-id="21d25-175"><dt>**mpnotify- \_ Scan Status \_**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-175"><dt>**MPNOTIFY\_SCAN\_PROGRESS**</dt></span></span> </dl>                   | <span data-ttu-id="21d25-176">Statusinformationen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="21d25-176">Scan progress information.</span></span> <span data-ttu-id="21d25-177">Zusätzliche Informationen (z. b. Ressourcen Statistiken) sind über die [**mpscan- \_ Daten**](mpscan-data.md) Struktur verfügbar.</span><span class="sxs-lookup"><span data-stu-id="21d25-177">Additional information (such as resource statistics) is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                               |
| <span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span><dl> <span data-ttu-id="21d25-178"><dt>**mpnotify- \_ Scan \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-178"><dt>**MPNOTIFY\_SCAN\_ERROR**</dt></span></span> </dl>                            | <span data-ttu-id="21d25-179">Überprüfen Sie die Fehlerinformationen für eine bestimmte Ressource.</span><span class="sxs-lookup"><span data-stu-id="21d25-179">Scan error information for a specific resource.</span></span> <span data-ttu-id="21d25-180">Die spezifischen Ressourcen Informationen sind über die [**mpscan- \_ Daten**](mpscan-data.md) Struktur verfügbar.</span><span class="sxs-lookup"><span data-stu-id="21d25-180">The specific resource information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                             |
| <span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span><dl> <span data-ttu-id="21d25-181"><dt>**mpnotify- \_ Scan \_ infiziert**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-181"><dt>**MPNOTIFY\_SCAN\_INFECTED**</dt></span></span> </dl>                   | <span data-ttu-id="21d25-182">Der Scan hat eine infizierte Ressource gefunden.</span><span class="sxs-lookup"><span data-stu-id="21d25-182">Scan found an infected resource.</span></span> <span data-ttu-id="21d25-183">Beachten Sie, dass dies in den meisten Fällen dazu führt, dass eine Bedrohung am Ende des Scans gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="21d25-183">Note that in most of the cases this will result in some threat reported at the end of the scan.</span></span> <span data-ttu-id="21d25-184">Manchmal kann es aufgrund von Ausschlüssen nicht als Bedrohung materialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="21d25-184">Sometimes it may not materialize as a threat because of exclusions.</span></span> <span data-ttu-id="21d25-185">Weitere Informationen zu infizierten Ressourcen sind über die [**mpscan- \_ Daten**](mpscan-data.md) Struktur verfügbar.</span><span class="sxs-lookup"><span data-stu-id="21d25-185">Additional infected resource information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/> |
| <span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span><dl> <span data-ttu-id="21d25-186"><dt>**mpnotify- \_ Scan \_ memorystart**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-186"><dt>**MPNOTIFY\_SCAN\_MEMORYSTART**</dt></span></span> </dl>          | <span data-ttu-id="21d25-187">Der schnell Scan Abschnitt der vollständigen Überprüfung wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="21d25-187">Quick scan portion of the full scan has started.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span><dl> <span data-ttu-id="21d25-188"><dt>**mpnotify- \_ Scan \_ memorycomplete**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-188"><dt>**MPNOTIFY\_SCAN\_MEMORYCOMPLETE**</dt></span></span> </dl> | <span data-ttu-id="21d25-189">Der schnell Scan Abschnitt der vollständigen Überprüfung wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="21d25-189">Quick scan portion of the full scan has completed.</span></span><br/>                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <span data-ttu-id="21d25-190"><dt>**Interner mpnotify- \_ \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-190"><dt>**MPNOTIFY\_INTERNAL\_FAILURE**</dt></span></span> </dl>          | <span data-ttu-id="21d25-191">Generischer Fehler beim Scan Vorgang.</span><span class="sxs-lookup"><span data-stu-id="21d25-191">Scan operation has encountered a generic failure.</span></span> <span data-ttu-id="21d25-192">Das *HRESULT* in [**mpcallback- \_ Daten**](mpcallback-data.md) enthält den spezifischen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="21d25-192">The *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md) has the specific error code.</span></span><br/>                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="21d25-193">*phscanhandle* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="21d25-193">*phScanHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21d25-194">Typ: **pmphandle**</span><span class="sxs-lookup"><span data-stu-id="21d25-194">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="21d25-195">Rückgabe Überprüfungs handle, das den derzeit initiierten Scan bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="21d25-195">Returned scan handle which identifies the currently initiated scan.</span></span> <span data-ttu-id="21d25-196">Dieses Handle kann in nachfolgenden Funktionsaufrufen verwendet werden, z. b., um ein Scanergebnis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="21d25-196">This handle can be used in subsequent function calls, such as to retrieve a scan result.</span></span> <span data-ttu-id="21d25-197">Das Handle muss mit der [**mplenker close**](mphandleclose.md) -Funktion geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="21d25-197">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21d25-198">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21d25-198">Return value</span></span>

<span data-ttu-id="21d25-199">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="21d25-199">Type: **HRESULT**</span></span>

<span data-ttu-id="21d25-200">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="21d25-200">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="21d25-201">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code.</span><span class="sxs-lookup"><span data-stu-id="21d25-201">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="21d25-202">Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="21d25-202">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="21d25-203">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21d25-203">Requirements</span></span>



| <span data-ttu-id="21d25-204">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21d25-204">Requirement</span></span> | <span data-ttu-id="21d25-205">Wert</span><span class="sxs-lookup"><span data-stu-id="21d25-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21d25-206">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21d25-206">Minimum supported client</span></span><br/> | <span data-ttu-id="21d25-207">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21d25-207">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="21d25-208">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21d25-208">Minimum supported server</span></span><br/> | <span data-ttu-id="21d25-209">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21d25-209">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="21d25-210">Header</span><span class="sxs-lookup"><span data-stu-id="21d25-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="21d25-211"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-211"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="21d25-212">DLL</span><span class="sxs-lookup"><span data-stu-id="21d25-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21d25-213"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21d25-213"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21d25-214">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21d25-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21d25-215">**Mperrormessageformat**</span><span class="sxs-lookup"><span data-stu-id="21d25-215">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="21d25-216">**Mplenker schließen**</span><span class="sxs-lookup"><span data-stu-id="21d25-216">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="21d25-217">**Mpmanageropen**</span><span class="sxs-lookup"><span data-stu-id="21d25-217">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="21d25-218">**mpcallback- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="21d25-218">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="21d25-219">**mpscan- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="21d25-219">**MPSCAN\_DATA**</span></span>](mpscan-data.md)
</dt> <dt>

[<span data-ttu-id="21d25-220">**mpscan- \_ Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="21d25-220">**MPSCAN\_RESOURCES**</span></span>](mpscan-resources.md)
</dt> <dt>

[<span data-ttu-id="21d25-221">**mpscan- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="21d25-221">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> </dl>

 

 





