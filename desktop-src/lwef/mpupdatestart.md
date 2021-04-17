---
title: Mpupdatestart-Funktion (mpclient. h)
description: Startet einen Signatur Aktualisierungs Vorgang.
ms.assetid: BB056356-17E5-42F0-9636-9E1C254361E4
keywords:
- Mpupdatestart-Funktion Legacy Funktionen der Windows-Umgebung
topic_type:
- apiref
api_name:
- MpUpdateStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39867525529339c6b354ae771b070589ca52acfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478735"
---
# <a name="mpupdatestart-function"></a><span data-ttu-id="cebca-104">Mpupdatestart-Funktion</span><span class="sxs-lookup"><span data-stu-id="cebca-104">MpUpdateStart function</span></span>

<span data-ttu-id="cebca-105">Startet einen Signatur Aktualisierungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="cebca-105">Starts a signature update operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="cebca-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cebca-106">Syntax</span></span>


```C++
HRESULT WINAPI MpUpdateStart(
  _In_     MPHANDLE         hMpHandle,
  _In_     DWORD            dwUpdateOptions,
  _In_opt_ PMPCALLBACK_INFO pCallbackInfo,
  _Out_    PMPHANDLE        phUpdateHandle
);
```



## <a name="parameters"></a><span data-ttu-id="cebca-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cebca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cebca-108">*hmphandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cebca-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cebca-109">Typ: **mphandle**</span><span class="sxs-lookup"><span data-stu-id="cebca-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="cebca-110">Handle für die Malware Protection Manager-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cebca-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="cebca-111">Dieses Handle wird von der [**mpmanageropen**](mpmanageropen.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cebca-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="cebca-112">*dwupdateoptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cebca-112">*dwUpdateOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cebca-113">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cebca-113">Type: **DWORD**</span></span>

<span data-ttu-id="cebca-114">Gibt die Option für den Signatur Aktualisierungs Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="cebca-114">Specifies the option for the signature update operation.</span></span> <span data-ttu-id="cebca-115">Es kann sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="cebca-115">It can be one of the following values:</span></span>



| <span data-ttu-id="cebca-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cebca-116">Value</span></span>                                                                                                                                                                                              | <span data-ttu-id="cebca-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cebca-117">Meaning</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPUPDATE_OPTION_NONE"></span><span id="mpupdate_option_none"></span><dl> <span data-ttu-id="cebca-118"><dt>**MPUpdate- \_ Option " \_ None"**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-118"><dt>**MPUPDATE\_OPTION\_NONE**</dt></span></span> </dl>                | <span data-ttu-id="cebca-119">Eine bestimmte Option wird nicht angefordert.</span><span class="sxs-lookup"><span data-stu-id="cebca-119">No specific option is requested.</span></span><br/>                                                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_ASYNC"></span><span id="mpupdate_option_async"></span><dl> <span data-ttu-id="cebca-120"><dt>**MPUpdate- \_ Option \_ Async**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-120"><dt>**MPUPDATE\_OPTION\_ASYNC**</dt></span></span> </dl>             | <span data-ttu-id="cebca-121">Der Aktualisierungs Vorgang wird asynchron ausgeführt, wobei " **mpupdatestart** " unmittelbar nach der erfolgreichen Initiierung des Signatur Updates zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cebca-121">The update operation is to be asynchronous, where **MpUpdateStart** returns immediately after the successful initiation of the signature update.</span></span> <span data-ttu-id="cebca-122">(Standardmäßig ist der Aktualisierungs Vorgang synchron, d. h. **mpupdatestart** wird erst zurückgegeben, wenn das Signatur Update abgeschlossen ist.)</span><span class="sxs-lookup"><span data-stu-id="cebca-122">(By default the update operation is synchronous, meaning **MpUpdateStart** will return only after the signature update is finished.)</span></span><br/> |
| <span id="MPUPDATE_OPTION_PROGRESS"></span><span id="mpupdate_option_progress"></span><dl> <span data-ttu-id="cebca-123"><dt>**Status der MPUpdate- \_ Option \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-123"><dt>**MPUPDATE\_OPTION\_PROGRESS**</dt></span></span> </dl>    | <span data-ttu-id="cebca-124">Der Aufrufer ist daran interessiert, Statusinformationen zur Signatur Aktualisierung über einen Rückruf zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="cebca-124">The caller is interested in receiving signature update progress information via a callback.</span></span><br/>                                                                                                                                                                                           |
| <span id="MPUPDATE_OPTION_HTTP"></span><span id="mpupdate_option_http"></span><dl> <span data-ttu-id="cebca-125"><dt>**MPUpdate- \_ Option \_ http**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-125"><dt>**MPUPDATE\_OPTION\_HTTP**</dt></span></span> </dl>                | <span data-ttu-id="cebca-126">Das Signatur Update wird ausgeführt, indem das vollständige Signatur Paket von der Microsoft Security Portal-Website heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="cebca-126">The signature update is performed by downloading the full signature package from the Microsoft security portal site.</span></span> <span data-ttu-id="cebca-127">Dies kann als Fall Back Option verwendet werden, wenn der Client über Microsoft Update ein Problem mit der Signatur herunterladen hat.</span><span class="sxs-lookup"><span data-stu-id="cebca-127">This can be used as a fallback option if the client is experiencing a signature download problem via Microsoft Update.</span></span><br/>                                           |
| <span id="MPUPDATE_OPTION_UNC"></span><span id="mpupdate_option_unc"></span><dl> <span data-ttu-id="cebca-128"><dt>**MPUpdate- \_ Option \_ UNC**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-128"><dt>**MPUPDATE\_OPTION\_UNC**</dt></span></span> </dl>                   | <span data-ttu-id="cebca-129">Führt eine Signatur Aktualisierung mithilfe von direktem Download von UNC-Freigaben durch.</span><span class="sxs-lookup"><span data-stu-id="cebca-129">Performs signature update using direct download from UNC shares.</span></span><br/>                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_MANAGED"></span><span id="mpupdate_option_managed"></span><dl> <span data-ttu-id="cebca-130"><dt>**MPUpdate- \_ Option \_ verwaltet**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-130"><dt>**MPUPDATE\_OPTION\_MANAGED**</dt></span></span> </dl>       | <span data-ttu-id="cebca-131">Führt eine Signatur Aktualisierung mithilfe des verwalteten Dienstanbieter-WSUS aus.</span><span class="sxs-lookup"><span data-stu-id="cebca-131">Performs signature update using the Managed Service WSUS.</span></span><br/>                                                                                                                                                                                                                             |
| <span id="MPUPDATE_OPTION_UNMANAGED"></span><span id="mpupdate_option_unmanaged"></span><dl> <span data-ttu-id="cebca-132"><dt>**MPUpdate- \_ Option \_ nicht verwaltet**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-132"><dt>**MPUPDATE\_OPTION\_UNMANAGED**</dt></span></span> </dl> | <span data-ttu-id="cebca-133">Führt ein Signatur Update mit dem nicht verwalteten Dienst mu/Wu aus.</span><span class="sxs-lookup"><span data-stu-id="cebca-133">Performs signature update using the Unmanaged Service MU/WU.</span></span><br/>                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="cebca-134">*pcallbackinfo* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="cebca-134">*pCallbackInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cebca-135">Typ: **pmpcallback- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="cebca-135">Type: **PMPCALLBACK\_INFO**</span></span>

<span data-ttu-id="cebca-136">Ein Zeiger auf die Rückruf Informationen, die verwendet werden, um den Client mit Änderungen des Signatur Update Zustands (z. b. Start und Complete) und Fortschrittsinformationen zu Feeds.</span><span class="sxs-lookup"><span data-stu-id="cebca-136">A pointer to the callback information used to feed the client with signature update state changes (such as start and complete) and progress information.</span></span> <span data-ttu-id="cebca-137">Die [**mpcallback- \_ Daten**](mpcallback-data.md) , die in der Rückruffunktion zurückgegeben werden, melden den tatsächlichen Update Status und die Status bezogenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="cebca-137">The [**MPCALLBACK\_DATA**](mpcallback-data.md) passed back in the callback function reports actual update state and progress-related information.</span></span> <span data-ttu-id="cebca-138">Im folgenden finden Sie eine Liste möglicher Rückrufe:</span><span class="sxs-lookup"><span data-stu-id="cebca-138">The following is a list of possible callbacks:</span></span>



| <span data-ttu-id="cebca-139">Wert</span><span class="sxs-lookup"><span data-stu-id="cebca-139">Value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="cebca-140">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cebca-140">Meaning</span></span>                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span><dl> <span data-ttu-id="cebca-141"><dt>**mpnotify \_ sigupdate \_ Start**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-141"><dt>**MPNOTIFY\_SIGUPDATE\_START**</dt></span></span> </dl>                                      | <span data-ttu-id="cebca-142">Der Aktualisierungs Vorgang wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="cebca-142">Update operation started.</span></span><br/>                                                                                                                                  |
| <span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span><dl> <span data-ttu-id="cebca-143"><dt>**mpnotify \_ sigupdate ist fertiggestellt. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-143"><dt>**MPNOTIFY\_SIGUPDATE\_COMPLETE**</dt></span></span> </dl>                             | <span data-ttu-id="cebca-144">Der Aktualisierungs Vorgang wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cebca-144">Update operation completed.</span></span><br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span><dl> <span data-ttu-id="cebca-145"><dt>**mpnotify \_ sigupdate- \_ Suche \_ starten**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-145"><dt>**MPNOTIFY\_SIGUPDATE\_SEARCH\_START**</dt></span></span> </dl>                | <span data-ttu-id="cebca-146">Suche nach Updates gestartet.</span><span class="sxs-lookup"><span data-stu-id="cebca-146">Search for updates started.</span></span><br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span><dl> <span data-ttu-id="cebca-147"><dt>**mpnotify \_ sigupdate- \_ Suche ist \_ beendet**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-147"><dt>**MPNOTIFY\_SIGUPDATE\_SEARCH\_COMPLETE**</dt></span></span> </dl>       | <span data-ttu-id="cebca-148">Suche nach Updates wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cebca-148">Search for updates completed.</span></span> <span data-ttu-id="cebca-149">Zusätzliche Informationen sind über die [**mpsigupdate- \_ Daten**](mpsigupdate-data.md) Struktur verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cebca-149">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span><dl> <span data-ttu-id="cebca-150"><dt>**mpnotify \_ sigupdate \_ Download \_ starten**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-150"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_START**</dt></span></span> </dl>          | <span data-ttu-id="cebca-151">Der Download für das Update wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="cebca-151">Download for update started.</span></span><br/>                                                                                                                               |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span><dl> <span data-ttu-id="cebca-152"><dt>**mpnotify \_ sigupdate- \_ Download \_ Fortschritt**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-152"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_PROGRESS**</dt></span></span> </dl> | <span data-ttu-id="cebca-153">Statusinformationen herunterladen.</span><span class="sxs-lookup"><span data-stu-id="cebca-153">Download progress information.</span></span> <span data-ttu-id="cebca-154">Zusätzliche Informationen sind über die [**mpsigupdate- \_ Daten**](mpsigupdate-data.md) Struktur verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cebca-154">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                            |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span><dl> <span data-ttu-id="cebca-155"><dt>**mpnotify \_ sigupdate- \_ Download ist \_ fertiggestellt.**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-155"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_COMPLETE**</dt></span></span> </dl> | <span data-ttu-id="cebca-156">Der Download für das Update ist beendet.</span><span class="sxs-lookup"><span data-stu-id="cebca-156">Download for update complete.</span></span> <span data-ttu-id="cebca-157">Zusätzliche Informationen sind über die [**mpsigupdate- \_ Daten**](mpsigupdate-data.md) Struktur verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cebca-157">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span><dl> <span data-ttu-id="cebca-158"><dt>**mpnotify \_ sigupdate \_ Installation \_ starten**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-158"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_START**</dt></span></span> </dl>             | <span data-ttu-id="cebca-159">Die Installation des Updates wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="cebca-159">Installation of update started.</span></span><br/>                                                                                                                            |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span><dl> <span data-ttu-id="cebca-160"><dt>**mpnotify \_ sigupdate- \_ Installations \_ Fortschritt**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-160"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_PROGRESS**</dt></span></span> </dl>    | <span data-ttu-id="cebca-161">Informationen zum Installationsfortschritt.</span><span class="sxs-lookup"><span data-stu-id="cebca-161">Installation progress information.</span></span> <span data-ttu-id="cebca-162">Zusätzliche Informationen sind über die [**mpsigupdate- \_ Daten**](mpsigupdate-data.md) Struktur verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cebca-162">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                        |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span><dl> <span data-ttu-id="cebca-163"><dt>**mpnotify \_ sigupdate- \_ Installation ist \_ fertiggestellt.**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-163"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_COMPLETE**</dt></span></span> </dl>    | <span data-ttu-id="cebca-164">Die Installation des Updates ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cebca-164">Installation of update completed.</span></span> <span data-ttu-id="cebca-165">Zusätzliche Informationen sind über die [**mpsigupdate- \_ Daten**](mpsigupdate-data.md) Struktur verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cebca-165">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                         |
| <span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span><dl> <span data-ttu-id="cebca-166"><dt>**mpnotify \_ sigupdate- \_ Anforderung \_ verarbeitet**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-166"><dt>**MPNOTIFY\_SIGUPDATE\_REQUEST\_PROCESSED**</dt></span></span> </dl> | <span data-ttu-id="cebca-167">Der antischadsoftwaredienst hat eine Signatur Aktualisierungs Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="cebca-167">The antimalware service processed a signature update request.</span></span> <span data-ttu-id="cebca-168">Fehler oder Erfolg wird von *HRESULT* in [**mpcallback- \_ Daten**](mpcallback-data.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="cebca-168">Failure or success is indicated by *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span><br/> |
| <span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span><dl> <span data-ttu-id="cebca-169"><dt>**mpnotify- \_ sigupdate- \_ Neustart \_ erforderlich**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-169"><dt>**MPNOTIFY\_SIGUPDATE\_REBOOT\_REQUIRED**</dt></span></span> </dl>       | <span data-ttu-id="cebca-170">Zum Abschluss des Aktualisierungs Vorgangs ist ein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cebca-170">Requires reboot to complete the update operation.</span></span> <span data-ttu-id="cebca-171">Fehler oder Erfolg wird von *HRESULT* in [**mpcallback- \_ Daten**](mpcallback-data.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="cebca-171">Failure or success is indicated by *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span><br/>             |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <span data-ttu-id="cebca-172"><dt>**Interner mpnotify- \_ \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-172"><dt>**MPNOTIFY\_INTERNAL\_FAILURE**</dt></span></span> </dl>                                   | <span data-ttu-id="cebca-173">Generischer Fehler beim Signatur Aktualisierungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="cebca-173">Signature update operation has encountered a generic failure.</span></span> <span data-ttu-id="cebca-174">Das *HRESULT* in [**mpcallback- \_ Daten**](mpcallback-data.md) enthält den spezifischen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="cebca-174">The *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md) has the specific error code.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="cebca-175">*phupdatehandle* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cebca-175">*phUpdateHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cebca-176">Typ: **pmphandle**</span><span class="sxs-lookup"><span data-stu-id="cebca-176">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="cebca-177">Zurück gegebenes Aktualisierungs handle, das den derzeit initiierten Signatur Aktualisierungs Vorgang identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cebca-177">Returned update handle which identifies the currently initiated signature update operation.</span></span> <span data-ttu-id="cebca-178">Dieses Handle kann in nachfolgenden Funktionsaufrufen verwendet werden, z. b. um den Signatur Aktualisierungs Vorgang zu steuern.</span><span class="sxs-lookup"><span data-stu-id="cebca-178">This handle can be used in subsequent function calls, such as to control the signature update operation.</span></span> <span data-ttu-id="cebca-179">Das Handle muss mit der [**mplenker close**](mphandleclose.md) -Funktion geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="cebca-179">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cebca-180">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cebca-180">Return value</span></span>

<span data-ttu-id="cebca-181">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cebca-181">Type: **HRESULT**</span></span>

<span data-ttu-id="cebca-182">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cebca-182">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="cebca-183">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code.</span><span class="sxs-lookup"><span data-stu-id="cebca-183">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="cebca-184">Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cebca-184">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="cebca-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cebca-185">Requirements</span></span>



| <span data-ttu-id="cebca-186">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cebca-186">Requirement</span></span> | <span data-ttu-id="cebca-187">Wert</span><span class="sxs-lookup"><span data-stu-id="cebca-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cebca-188">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cebca-188">Minimum supported client</span></span><br/> | <span data-ttu-id="cebca-189">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cebca-189">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="cebca-190">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cebca-190">Minimum supported server</span></span><br/> | <span data-ttu-id="cebca-191">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cebca-191">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cebca-192">Header</span><span class="sxs-lookup"><span data-stu-id="cebca-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="cebca-193"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-193"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="cebca-194">DLL</span><span class="sxs-lookup"><span data-stu-id="cebca-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cebca-195"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cebca-195"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cebca-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cebca-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cebca-197">**Mperrormessageformat**</span><span class="sxs-lookup"><span data-stu-id="cebca-197">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="cebca-198">**Mplenker schließen**</span><span class="sxs-lookup"><span data-stu-id="cebca-198">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="cebca-199">**Mpmanageropen**</span><span class="sxs-lookup"><span data-stu-id="cebca-199">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="cebca-200">**mpcallback- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="cebca-200">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="cebca-201">**mpsigupdate- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="cebca-201">**MPSIGUPDATE\_DATA**</span></span>](mpsigupdate-data.md)
</dt> </dl>

 

 





