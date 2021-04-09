---
title: Bits-Rückgabewerte
description: Die Datei "bitsmsg. h" enthält die folgenden Rückgabewert Konstanten.
ms.assetid: 8df5022a-b161-4558-9d60-efdbdf1754d6
keywords:
- Fehler Bits
- Fehler Bits, Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9086de1d55bbdc9695876bd06368ab28dbbb161
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948987"
---
# <a name="bits-return-values"></a><span data-ttu-id="db0a4-105">Bits-Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="db0a4-105">BITS Return Values</span></span>

<span data-ttu-id="db0a4-106">Die Datei "bitsmsg. h" enthält die folgenden Rückgabewert Konstanten.</span><span class="sxs-lookup"><span data-stu-id="db0a4-106">The Bitsmsg.h file contains the following return value constants.</span></span> <span data-ttu-id="db0a4-107">Die Konstanten stellen Rückgabewerte dar, die von Bits generiert werden, und http-Rückgabewerte, die Bits erfasst.</span><span class="sxs-lookup"><span data-stu-id="db0a4-107">The constants represent return values that BITS generates and HTTP return values that BITS captures.</span></span> <span data-ttu-id="db0a4-108">Alle anderen Rückgabewerte, die Sie empfangen können, sind com-, RPC-oder konvertierte Windows-Rückgabewerte (Bits verwendet das [HRESULT \_ aus \_ Win32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) -Makro, um die Windows-Rückgabewerte in HRESULT-Werte zu konvertieren).</span><span class="sxs-lookup"><span data-stu-id="db0a4-108">All other return values that you can receive are COM, RPC, or converted Windows return values (BITS uses the [HRESULT\_FROM\_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) macro to convert the Windows return values to HRESULT values).</span></span>

<span data-ttu-id="db0a4-109">Beachten Sie, dass die Datei "bitsmsg. h" zusätzliche Rückgabewerte enthält, die unten nicht aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="db0a4-109">Note that the Bitsmsg.h file contains additional return values not listed below.</span></span>

<dl> <dt>

<span data-ttu-id="db0a4-110"><span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>BG \_ S \_ partiell \_ vollständig (0x00200017)</span><span class="sxs-lookup"><span data-stu-id="db0a4-110"><span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>BG\_S\_PARTIAL\_COMPLETE (0x00200017)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-111">Eine Teilmenge der Auftragsdateien wurde erfolgreich übertragen, bevor die [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="db0a4-111">A subset of the job's files transferred successfully before the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method was called.</span></span> <span data-ttu-id="db0a4-112">Die, die nicht fertig waren, wurden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="db0a4-112">Those that were not complete were deleted.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-113"><span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG \_ S \_ können \_ \_ Dateien nicht löschen \_ (0x0020001a)</span><span class="sxs-lookup"><span data-stu-id="db0a4-113"><span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG\_S\_UNABLE\_TO\_DELETE\_FILES (0x0020001A)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-114">Es können nicht alle temporären Dateien gelöscht werden, die dem Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="db0a4-114">Unable to delete all temporary files associated with the job.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-115"><span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>\_ \_ Durch Richtlinie überschriebene BG S \_ \_ (0x00200055)</span><span class="sxs-lookup"><span data-stu-id="db0a4-115"><span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG\_S\_OVERRIDDEN\_BY\_POLICY (0x00200055)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-116">Die Konfigurationseinstellung wurde erfolgreich gespeichert, aber die Einstellung wird nicht verwendet, da eine konfigurierte Gruppenrichtlinie Einstellung die Einstellung überschreibt.</span><span class="sxs-lookup"><span data-stu-id="db0a4-116">The configuration preference has been saved successfully, but the preference will not be used because a configured Group Policy setting overrides the preference.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-117"><span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG \_ E \_ nicht \_ gefunden (0x80200001)</span><span class="sxs-lookup"><span data-stu-id="db0a4-117"><span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG\_E\_NOT\_FOUND (0x80200001)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-118">Der angeforderte Auftrag wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="db0a4-118">The requested job was not found.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-119"><span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>BG \_ E \_ ungültiger \_ Zustand (0x80200002)</span><span class="sxs-lookup"><span data-stu-id="db0a4-119"><span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>BG\_E\_INVALID\_STATE (0x80200002)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-120">Die angeforderte Aktion ist im aktuellen Auftragszustand unzulässig.</span><span class="sxs-lookup"><span data-stu-id="db0a4-120">The requested action is not allowed in the current job state.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-121"><span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG \_ E \_ empty (0x80200003)</span><span class="sxs-lookup"><span data-stu-id="db0a4-121"><span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG\_E\_EMPTY (0x80200003)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-122">Der Auftrag muss eine oder mehrere Dateien enthalten, bevor Sie den Auftrag fortsetzen können.</span><span class="sxs-lookup"><span data-stu-id="db0a4-122">The job must contain one or more files before you can resume the job.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-123"><span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>BG- \_ E- \_ Datei \_ nicht \_ verfügbar (0x80200004)</span><span class="sxs-lookup"><span data-stu-id="db0a4-123"><span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>BG\_E\_FILE\_NOT\_AVAILABLE (0x80200004)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-124">Die Dateiinformationen sind nicht verfügbar, da der Fehler keiner lokalen oder Remote Datei zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="db0a4-124">File information is not available because the error is not associated with a local or remote file.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-125"><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>Das BG \_ E- \_ Protokoll ist \_ nicht \_ verfügbar (0x80200005).</span><span class="sxs-lookup"><span data-stu-id="db0a4-125"><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>BG\_E\_PROTOCOL\_NOT\_AVAILABLE (0x80200005)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-126">Protokollinformationen sind nicht verfügbar, da der Fehler dem angegebenen Übertragungsprotokoll nicht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="db0a4-126">Protocol information is not available because the error is not associated with the specified transfer protocol.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-127"><span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>BG \_ E \_ \_ -Ziel gesperrt (0x8020000d)</span><span class="sxs-lookup"><span data-stu-id="db0a4-127"><span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>BG\_E\_DESTINATION\_LOCKED (0x8020000D)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-128">Das im lokalen Dateinamen angegebene Ziel Dateisystem-Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="db0a4-128">The destination file system volume, specified in the local file name, is locked.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-129"><span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>BG \_ E- \_ Volume \_ geändert (0x8020000E)</span><span class="sxs-lookup"><span data-stu-id="db0a4-129"><span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>BG\_E\_VOLUME\_CHANGED (0x8020000E)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-130">Das im lokalen Dateinamen angegebene Ziel Volume wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="db0a4-130">The destination volume, specified in the local file name, has changed.</span></span> <span data-ttu-id="db0a4-131">Die ursprüngliche Diskette wurde z. b. durch eine andere Diskette ersetzt.</span><span class="sxs-lookup"><span data-stu-id="db0a4-131">For example, the original floppy disk has been replaced with a different floppy disk.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-132"><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>BG \_ E- \_ Fehler \_ Informationen nicht \_ verfügbar (0x8020000f)</span><span class="sxs-lookup"><span data-stu-id="db0a4-132"><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>BG\_E\_ERROR\_INFORMATION\_UNAVAILABLE (0x8020000F)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-133">Fehlerinformationen sind nur verfügbar, wenn der Status des Auftrags "BG- \_ Auftragsstatus" lautet \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="db0a4-133">Error information is only available when the state of the job is BG\_JOB\_STATE\_ERROR.</span></span> <span data-ttu-id="db0a4-134">Die Fehlerinformationen sind nicht verfügbar, nachdem Bits mit der Übertragung der Auftragsdaten begonnen hat oder der Client beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="db0a4-134">The error information is not available after BITS begins transferring the job's data or the client exits.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-135"><span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>BG \_ E \_ \_ (Netzwerk getrennt) (0x80200010)</span><span class="sxs-lookup"><span data-stu-id="db0a4-135"><span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>BG\_E\_NETWORK\_DISCONNECTED (0x80200010)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-136">Der Netzwerkadapter ist inaktiv oder nicht getrennt.</span><span class="sxs-lookup"><span data-stu-id="db0a4-136">The network adapter is inactive or disconnected.</span></span> <span data-ttu-id="db0a4-137">Alle Aufträge werden in den Status " \_ \_ vorübergehender Status des BG-Auftragsstatus" versetzt \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="db0a4-137">All jobs are placed in the BG\_JOB\_STATE\_TRANSIENT\_ERROR state.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-138"><span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>BG \_ E \_ fehlende \_ Datei \_ Größe (0x80200011)</span><span class="sxs-lookup"><span data-stu-id="db0a4-138"><span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>BG\_E\_MISSING\_FILE\_SIZE (0x80200011)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-139">Der Server hat die Dateigröße nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="db0a4-139">The server did not return the file size.</span></span> <span data-ttu-id="db0a4-140">Bits überträgt nur statischen Inhalt und erfordert, dass der HTTP-Server den Content-Length-Header zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="db0a4-140">BITS only transfers static content and requires the HTTP server to return the Content-Length header.</span></span> <span data-ttu-id="db0a4-141">Die Übertragungs Anforderung schlägt fehl, wenn die URL auf dynamischen Inhalt verweist.</span><span class="sxs-lookup"><span data-stu-id="db0a4-141">The transfer request fails if the URL points to dynamic content.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-142"><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>BG \_ E \_ unzureichende \_ http- \_ Unterstützung (0x80200012)</span><span class="sxs-lookup"><span data-stu-id="db0a4-142"><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>BG\_E\_INSUFFICIENT\_HTTP\_SUPPORT (0x80200012)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-143">Das HTTP/1.1-Protokoll wird vom Server nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db0a4-143">The server does not support the HTTP/1.1 protocol.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-144"><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>BG \_ E \_ unzureichende \_ Bereichs \_ Unterstützung (0x80200013)</span><span class="sxs-lookup"><span data-stu-id="db0a4-144"><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>BG\_E\_INSUFFICIENT\_RANGE\_SUPPORT (0x80200013)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-145">Der Content-Range-Header wird vom Server nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db0a4-145">The server does not support the Content-Range header.</span></span> <span data-ttu-id="db0a4-146">Normalerweise erhalten Sie diesen Fehler, wenn Sie versuchen, dynamischen Inhalt herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="db0a4-146">Typically, you receive this error when you try to download dynamic content.</span></span> <span data-ttu-id="db0a4-147">Dieser Fehler kann auch ausgegeben werden, wenn ein zwischen Proxy den Content-Range-Header oder den Content-Length-Header entfernt.</span><span class="sxs-lookup"><span data-stu-id="db0a4-147">You can also receive this error if an intermediate proxy is removing the Content-Range or Content-Length header.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-148"><span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>BG \_ E \_ Remote \_ nicht \_ unterstützt (0x80200014)</span><span class="sxs-lookup"><span data-stu-id="db0a4-148"><span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>BG\_E\_REMOTE\_NOT\_SUPPORTED (0x80200014)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-149">Die Remote Verwendung von Bits wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db0a4-149">Remote use of BITS is not supported.</span></span> <span data-ttu-id="db0a4-150">Weitere Informationen finden Sie unter [Benutzer und Netzwerkverbindungen](users-and-network-connections.md).</span><span class="sxs-lookup"><span data-stu-id="db0a4-150">For more information, see [Users and Network Connections](users-and-network-connections.md).</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-151"><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>BG \_ E \_ neue \_ Besitzer \_ diff- \_ Zuordnung (0x80200015)</span><span class="sxs-lookup"><span data-stu-id="db0a4-151"><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>BG\_E\_NEW\_OWNER\_DIFF\_MAPPING (0x80200015)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-152">Die Zuordnung des Netzwerklaufwerks für die lokale Datei ist für den aktuellen Besitzer anders als für den vorherigen Besitzer.</span><span class="sxs-lookup"><span data-stu-id="db0a4-152">The network drive mapping for the local file is different for the current owner than for the previous owner.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-153"><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG \_ E \_ New \_ Owner \_ No \_ file \_ Access (0x80200016)</span><span class="sxs-lookup"><span data-stu-id="db0a4-153"><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG\_E\_NEW\_OWNER\_NO\_FILE\_ACCESS (0x80200016)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-154">Der neue Besitzer verfügt nicht über ausreichende Berechtigungen für die temporären Auftragsdateien.</span><span class="sxs-lookup"><span data-stu-id="db0a4-154">The new owner has insufficient permissions to the temporary job files.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-155"><span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>BG \_ E- \_ Proxy \_ Liste \_ zu \_ groß (0x80200018)</span><span class="sxs-lookup"><span data-stu-id="db0a4-155"><span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>BG\_E\_PROXY\_LIST\_TOO\_LARGE (0x80200018)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-156">Die Liste der HTTP-Proxys ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="db0a4-156">The HTTP proxy list is too long.</span></span> <span data-ttu-id="db0a4-157">Die Liste darf 32 KB nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="db0a4-157">The list must not exceed 32 KB.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-158"><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>BG \_ E \_ Proxy \_ Umgehungs \_ Liste \_ zu \_ groß (0x80200019)</span><span class="sxs-lookup"><span data-stu-id="db0a4-158"><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>BG\_E\_PROXY\_BYPASS\_LIST\_TOO\_LARGE (0x80200019)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-159">Die Liste der HTTP-Proxy Umgehungen ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="db0a4-159">The HTTP proxy bypass list is too long.</span></span> <span data-ttu-id="db0a4-160">Die Liste darf 32 KB nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="db0a4-160">The list must not exceed 32 KB.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-161"><span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG \_ E \_ zu \_ viele \_ Dateien (0x8020001c)</span><span class="sxs-lookup"><span data-stu-id="db0a4-161"><span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG\_E\_TOO\_MANY\_FILES (0x8020001C)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-162">Sie können einem Uploadauftrag nicht mehr als eine Datei hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="db0a4-162">You cannot add more than one file to an upload job.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-163"><span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>\_Lokale BG \_ E \_ \_ -Datei geändert (0x8020001d)</span><span class="sxs-lookup"><span data-stu-id="db0a4-163"><span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>BG\_E\_LOCAL\_FILE\_CHANGED (0x8020001D)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-164">Der Inhalt der lokalen Datei wurde geändert, nachdem der Übertragungsvorgang begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="db0a4-164">The contents of the local file changed after the transfer process began.</span></span> <span data-ttu-id="db0a4-165">Der Inhalt der lokalen Datei kann nicht geändert werden, nachdem der Übertragungsvorgang bei einem Upload-oder Upload-Reply-Auftrag gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="db0a4-165">The contents of the local file cannot change after the transfer process begins on an upload or upload-reply job.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-166"><span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG \_ E \_ zu \_ groß (0x80200020)</span><span class="sxs-lookup"><span data-stu-id="db0a4-166"><span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG\_E\_TOO\_LARGE (0x80200020)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-167">Die Größe der Uploaddatei überschreitet die auf dem Server angegebene maximal zulässige Uploadgröße.</span><span class="sxs-lookup"><span data-stu-id="db0a4-167">The size of the upload file exceeds the maximum allowed upload size specified on the server.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-168"><span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>BG \_ E \_ Zeichenfolge \_ zu \_ lang (0x80200021)</span><span class="sxs-lookup"><span data-stu-id="db0a4-168"><span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>BG\_E\_STRING\_TOO\_LONG (0x80200021)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-169">Die angegebene Zeichenfolge ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="db0a4-169">The specified string is too long.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-170"><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>Nicht übereinstimmende BG \_ E- \_ Client \_ Server \_ Protokoll \_ (0x80200022)</span><span class="sxs-lookup"><span data-stu-id="db0a4-170"><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>BG\_E\_CLIENT\_SERVER\_PROTOCOL\_MISMATCH (0x80200022)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-171">Der Client und der Server konnten kein Protokoll aushandeln, das für den Uploadauftrag verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="db0a4-171">The client and server were unable to negotiate a protocol to use for the upload job.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-172"><span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>BG \_ E \_ Server \_ Execute \_ aktiviert (0x80200023)</span><span class="sxs-lookup"><span data-stu-id="db0a4-172"><span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>BG\_E\_SERVER\_EXECUTE\_ENABLED (0x80200023)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-173">Skripterstellung oder Ausführungs Berechtigungen werden für das virtuelle IIS-Verzeichnis aktiviert, das dem Auftrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="db0a4-173">Scripting or execute permissions are enabled on the IIS virtual directory associated with the job.</span></span> <span data-ttu-id="db0a4-174">Zum Hochladen von Dateien in das virtuelle Verzeichnis deaktivieren Sie die Skripterstellung und Ausführungs Berechtigungen für das virtuelle Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="db0a4-174">To upload files to the virtual directory, disable the scripting and execute permissions on the virtual directory.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-175"><span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>BG \_ E \_ username \_ zu \_ groß (0x80200025)</span><span class="sxs-lookup"><span data-stu-id="db0a4-175"><span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>BG\_E\_USERNAME\_TOO\_LARGE (0x80200025)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-176">Der Benutzername darf nicht länger als 300 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="db0a4-176">The user name cannot exceed 300 characters.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-177"><span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>BG \_ E \_ Kennwort \_ zu \_ groß (0x80200026)</span><span class="sxs-lookup"><span data-stu-id="db0a4-177"><span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>BG\_E\_PASSWORD\_TOO\_LARGE (0x80200026)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-178">Das Kennwort darf nicht länger als 65535 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="db0a4-178">The password cannot exceed 65535 characters.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-179"><span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>BG \_ E \_ Ungültiges Authentifizierungs \_ \_ Ziel (0x80200027)</span><span class="sxs-lookup"><span data-stu-id="db0a4-179"><span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>BG\_E\_INVALID\_AUTH\_TARGET (0x80200027)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-180">Das angegebene Authentifizierungs Ziel ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="db0a4-180">The specified authentication target is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-181"><span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>BG \_ E \_ Ungültiges Authentifizierungs \_ \_ Schema (0x80200028)</span><span class="sxs-lookup"><span data-stu-id="db0a4-181"><span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>BG\_E\_INVALID\_AUTH\_SCHEME (0x80200028)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-182">Das angegebene Authentifizierungsschema ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="db0a4-182">The specified authentication scheme is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-183"><span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>BG \_ E \_ ungültiger \_ Bereich (0x8020002b)</span><span class="sxs-lookup"><span data-stu-id="db0a4-183"><span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>BG\_E\_INVALID\_RANGE (0x8020002B)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-184">Der angegebene Byte Bereich ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="db0a4-184">The specified byte range is invalid.</span></span> <span data-ttu-id="db0a4-185">Der Byte Bereich muss in der angegebenen Remote Datei vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="db0a4-185">The byte range must exist within the specified remote file.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-186"><span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>BG \_ E über \_ Lapp Ende \_ Bereiche (0x8020002c)</span><span class="sxs-lookup"><span data-stu-id="db0a4-186"><span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>BG\_E\_OVERLAPPING\_RANGES (0x8020002C)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-187">Die Liste der Byte Bereiche enthält überlappende oder doppelte Bereiche, die nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="db0a4-187">The list of byte ranges contains overlapping or duplicate ranges, which are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-188"><span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG \_ E \_ \_ von \_ Richtlinie blockiert (0x8020003E)</span><span class="sxs-lookup"><span data-stu-id="db0a4-188"><span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG\_E\_BLOCKED\_BY\_POLICY (0x8020003E)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-189">Gruppenrichtlinie Einstellungen verhindern, dass Hintergrund Aufträge zu diesem Zeitpunkt ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="db0a4-189">Group Policy settings prevent background jobs from running at this time.</span></span> <span data-ttu-id="db0a4-190">Weitere Informationen finden Sie in der [MaxInternetBandwidth](group-policies.md) -Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="db0a4-190">For details, see the [MaxInternetBandwidth](group-policies.md) policy.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-191"><span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>BG \_ E \_ ungültige \_ Proxy \_ Informationen (0x8020003f)</span><span class="sxs-lookup"><span data-stu-id="db0a4-191"><span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>BG\_E\_INVALID\_PROXY\_INFO (0x8020003F)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-192">Laufzeitfehler, der angibt, dass die Proxy Liste oder Proxy Umgehungs Liste, die Sie mithilfe der [**ibackgroundcopyjob:: setproxysettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) -Methode angegeben haben, ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="db0a4-192">Run-time error that indicates the proxy list or proxy bypass list that you specified using the [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) method is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-193"><span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>BG \_ E \_ ungültige \_ Anmelde Informationen (0x80200040)</span><span class="sxs-lookup"><span data-stu-id="db0a4-193"><span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>BG\_E\_INVALID\_CREDENTIALS (0x80200040)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-194">Das Format der angegebenen Sicherheits Anmelde Informationen ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="db0a4-194">The format of the supplied security credentials is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-195"><span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>BG \_ E- \_ Datensatz \_ gelöscht (0x80200042)</span><span class="sxs-lookup"><span data-stu-id="db0a4-195"><span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>BG\_E\_RECORD\_DELETED (0x80200042)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-196">Der Cache Daten Satz wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="db0a4-196">The cache record has been deleted.</span></span> <span data-ttu-id="db0a4-197">Der Versuch, ihn zu aktualisieren, wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="db0a4-197">The attempt to update it has been abandoned.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-198"><span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>BG \_ E \_ UPnP- \_ Fehler (0x80200045)</span><span class="sxs-lookup"><span data-stu-id="db0a4-198"><span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>BG\_E\_UPNP\_ERROR (0x80200045)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-199">Ein Universal Plug & Play (UPnP)-Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="db0a4-199">A Universal Plug and Play (UPnP) error has occurred.</span></span> <span data-ttu-id="db0a4-200">Überprüfen Sie Ihr Internet Gateway-Gerät.</span><span class="sxs-lookup"><span data-stu-id="db0a4-200">Please check your Internet Gateway Device.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-201"><span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>BG \_ E \_ Peer Caching \_ deaktiviert (0x80200047)</span><span class="sxs-lookup"><span data-stu-id="db0a4-201"><span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>BG\_E\_PEERCACHING\_DISABLED (0x80200047)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-202">Peer-Caching ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="db0a4-202">Peer-caching is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-203"><span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG \_ E \_ busycacherecord (0x80200048)</span><span class="sxs-lookup"><span data-stu-id="db0a4-203"><span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG\_E\_BUSYCACHERECORD (0x80200048)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-204">Der Cache Daten Satz wird verwendet und kann nicht geändert oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="db0a4-204">The cache record is in use and cannot be changed or deleted.</span></span> <span data-ttu-id="db0a4-205">Versuchen Sie es nach einigen Sekunden erneut.</span><span class="sxs-lookup"><span data-stu-id="db0a4-205">Try again after a few seconds.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-206"><span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG \_ E \_ zu \_ viele \_ Aufträge \_ pro \_ Benutzer (0x80200049)</span><span class="sxs-lookup"><span data-stu-id="db0a4-206"><span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG\_E\_TOO\_MANY\_JOBS\_PER\_USER (0x80200049)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-207">Die Auftrags Anzahl für den Benutzer hat den Auftrags Grenzwert pro Benutzer überschritten, der durch die Einstellung "maxjobsperGruppenrichtlinie User" festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="db0a4-207">The job count for the user has exceeded the per user job limit set by the MaxJobsPerUser Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-208"><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG \_ E \_ zu \_ viele \_ Aufträge \_ pro \_ Computer (0x80200050)</span><span class="sxs-lookup"><span data-stu-id="db0a4-208"><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG\_E\_TOO\_MANY\_JOBS\_PER\_MACHINE (0x80200050)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-209">Die Auftrags Anzahl für den Computer hat den Auftrags Grenzwert pro Computer überschritten, der durch die Einstellung maxjobspermachine Gruppenrichtlinie festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="db0a4-209">The job count for the computer has exceeded the per computer job limit set by the MaxJobsPerMachine Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-210"><span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG \_ E \_ zu \_ viele \_ Dateien \_ im \_ Auftrag (0x80200051)</span><span class="sxs-lookup"><span data-stu-id="db0a4-210"><span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG\_E\_TOO\_MANY\_FILES\_IN\_JOB (0x80200051)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-211">Die Dateianzahl für den Auftrag hat das von der Einstellung maxfilesperjob Gruppenrichtlinie festgelegte Limit für die pro-Auftragsdatei überschritten.</span><span class="sxs-lookup"><span data-stu-id="db0a4-211">The file count for the job has exceeded the per job file limit set by the MaxFilesPerJob Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-212"><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG \_ E \_ zu \_ viele \_ Bereiche \_ in der \_ Datei (0x80200052)</span><span class="sxs-lookup"><span data-stu-id="db0a4-212"><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG\_E\_TOO\_MANY\_RANGES\_IN\_FILE (0x80200052)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-213">Die Bereichs Anzahl für die Datei hat den Grenzwert pro Datei Bereich überschritten, der durch die Einstellung "maxrangesperGruppenrichtlinie file" festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="db0a4-213">The range count for the file has exceeded the per file range limit set by the MaxRangesPerFile Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-214"><span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>BG \_ E- \_ Validierung \_ fehlgeschlagen (0x80200053)</span><span class="sxs-lookup"><span data-stu-id="db0a4-214"><span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>BG\_E\_VALIDATION\_FAILED (0x80200053)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-215">Die Anwendung hat Daten von einer Website angefordert, aber die Antwort war nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="db0a4-215">The application requested data from a website, but the response was not valid.</span></span> <span data-ttu-id="db0a4-216">Ausführliche Informationen finden Sie unter Verwenden von Ereignisanzeige zum Anzeigen des Betriebs Protokolls für die Anwendungsprotokolle von \\ Microsoft \\ Windows \\ BITS-Client \\ .</span><span class="sxs-lookup"><span data-stu-id="db0a4-216">For details, use Event Viewer to view the Application Logs\\Microsoft\\Windows\\Bits-client\\Operational log.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-217"><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>BG \_ E \_ maxdownload \_ Timeout (0x80200054)</span><span class="sxs-lookup"><span data-stu-id="db0a4-217"><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>BG\_E\_MAXDOWNLOAD\_TIMEOUT (0x80200054)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-218">Beim Herunterladen des Auftrags durch Bits ist ein Timeout aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="db0a4-218">BITS timed out downloading the job.</span></span> <span data-ttu-id="db0a4-219">Der Download konnte nicht innerhalb der maximalen Downloadzeit, die für den Auftrag festgelegt wurde, oder in der Gruppenrichtlinie Einstellung maxdownloadtime ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="db0a4-219">The download did not complete within the maximum download time set on the job or the MaxDownloadTime Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-220"><span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>BG \_ E \_ http- \_ Fehler \_ 400 (0x80190190)</span><span class="sxs-lookup"><span data-stu-id="db0a4-220"><span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>BG\_E\_HTTP\_ERROR\_400 (0x80190190)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-221">Der Server konnte die Übertragungs Anforderung nicht verarbeiten, da die Syntax des Remote Dateinamens ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="db0a4-221">The server could not process the transfer request because the syntax of the remote file name is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-222"><span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>BG \_ E \_ http- \_ Fehler \_ 401 (0x80190191)</span><span class="sxs-lookup"><span data-stu-id="db0a4-222"><span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>BG\_E\_HTTP\_ERROR\_401 (0x80190191)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-223">Der Benutzer verfügt nicht über die Berechtigung für den Zugriff auf die Remote Datei.</span><span class="sxs-lookup"><span data-stu-id="db0a4-223">The user does not have permission to access the remote file.</span></span> <span data-ttu-id="db0a4-224">Für die angeforderte Ressource ist eine Benutzerauthentifizierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="db0a4-224">The requested resource requires user authentication.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-225"><span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>BG \_ E \_ http- \_ Fehler \_ 404 (0x80190194)</span><span class="sxs-lookup"><span data-stu-id="db0a4-225"><span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>BG\_E\_HTTP\_ERROR\_404 (0x80190194)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-226">Die angeforderte URL ist auf dem Server nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="db0a4-226">The requested URL does not exist on the server.</span></span>

<span data-ttu-id="db0a4-227">In IIS 7 kann dieser Fehler darauf hindeuten.</span><span class="sxs-lookup"><span data-stu-id="db0a4-227">In IIS 7, this error can indicate</span></span>

-   <span data-ttu-id="db0a4-228">Diese Bits-Uploads sind im virtuellen Verzeichnis (vdir) auf dem Server nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="db0a4-228">That BITS uploads are not enabled on the virtual directory (vdir) on the server.</span></span>
-   <span data-ttu-id="db0a4-229">Die Uploadgröße überschreitet die maximale uploadgrenze (Weitere Informationen finden Sie in der IIS-Erweiterungs Eigenschaft [**bitmaximumuploadsize**](bits-iis-extension-properties.md) ).</span><span class="sxs-lookup"><span data-stu-id="db0a4-229">That the upload size exceeds the maximum upload limit (for details, see the [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) IIS extension property).</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-230"><span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>BG \_ E \_ http- \_ Fehler \_ 407 (0x80190197)</span><span class="sxs-lookup"><span data-stu-id="db0a4-230"><span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>BG\_E\_HTTP\_ERROR\_407 (0x80190197)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-231">Der Benutzer verfügt nicht über die Berechtigung zum Zugriff auf den Proxy.</span><span class="sxs-lookup"><span data-stu-id="db0a4-231">The user does not have permission to access the proxy.</span></span> <span data-ttu-id="db0a4-232">Für den Proxy ist eine Benutzerauthentifizierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="db0a4-232">The proxy requires user authentication.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-233"><span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>BG \_ E \_ http- \_ Fehler \_ 414 (0x8019019E)</span><span class="sxs-lookup"><span data-stu-id="db0a4-233"><span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>BG\_E\_HTTP\_ERROR\_414 (0x8019019E)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-234">Der Server kann die Übertragungs Anforderung nicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="db0a4-234">The server cannot process the transfer request.</span></span> <span data-ttu-id="db0a4-235">Der Uniform Resource Identifier (URI) im Remote Dateinamen ist länger als der Server interpretieren kann.</span><span class="sxs-lookup"><span data-stu-id="db0a4-235">The Uniform Resource Identifier (URI) in the remote file name is longer than the server can interpret.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-236"><span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>BG \_ E \_ http- \_ Fehler \_ 501 (0x801901f 5)</span><span class="sxs-lookup"><span data-stu-id="db0a4-236"><span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>BG\_E\_HTTP\_ERROR\_501 (0x801901F5)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-237">Der Server unterstützt die erforderliche Funktionalität zum erfüllen der Anforderung nicht.</span><span class="sxs-lookup"><span data-stu-id="db0a4-237">The server does not support the functionality required to fulfill the request.</span></span> <span data-ttu-id="db0a4-238">In IIS 6 gibt dieser Fehler an, dass BITS-Uploads auf dem virtuellen Verzeichnis (vdir) auf dem Server nicht aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="db0a4-238">In IIS 6, this error indicates that BITS uploads are not enabled on the virtual directory (vdir) on the server.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-239"><span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>BG \_ E \_ http- \_ Fehler \_ 503 (0x801901f)</span><span class="sxs-lookup"><span data-stu-id="db0a4-239"><span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>BG\_E\_HTTP\_ERROR\_503 (0x801901F7)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-240">Der Dienst ist vorübergehend überlastet und kann die Anforderung nicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="db0a4-240">The service is temporarily overloaded and cannot process the request.</span></span> <span data-ttu-id="db0a4-241">Fortsetzen des Auftrags zu einem späteren Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="db0a4-241">Resume the job at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-242"><span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>BG \_ E \_ http- \_ Fehler \_ 504 (0x801901f)</span><span class="sxs-lookup"><span data-stu-id="db0a4-242"><span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>BG\_E\_HTTP\_ERROR\_504 (0x801901F8)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-243">Timeout bei der Übertragungs Anforderung beim Warten auf ein Gateway.</span><span class="sxs-lookup"><span data-stu-id="db0a4-243">The transfer request timed out while waiting for a gateway.</span></span> <span data-ttu-id="db0a4-244">Fortsetzen des Auftrags zu einem späteren Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="db0a4-244">Resume the job at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="db0a4-245"><span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>BG \_ E \_ http- \_ Fehler \_ 505 (0x801901f)</span><span class="sxs-lookup"><span data-stu-id="db0a4-245"><span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>BG\_E\_HTTP\_ERROR\_505 (0x801901F9)</span></span>
</dt> <dd>

<span data-ttu-id="db0a4-246">Die im Remote Dateinamen angegebene HTTP-Protokollversion wird vom Server nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db0a4-246">The server does not support the HTTP protocol version specified in the remote file name.</span></span>

</dd> </dl>

<span data-ttu-id="db0a4-247">Die Header Datei "bitsmsg. h" enthält zusätzliche http-Rückgabewerte, die nicht oben aufgeführt sind und von Bits intern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db0a4-247">The Bitsmsg.h header file contains additional HTTP return values not listed above that BITS uses internally.</span></span> <span data-ttu-id="db0a4-248">Weitere Informationen zu diesen und anderen HTTP-Rückgabe Werten, die Sie empfangen können, finden Sie in der Spezifikation von RFC 2616 von der Internet Engineering Task Force unter [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10) .</span><span class="sxs-lookup"><span data-stu-id="db0a4-248">For information on these and other HTTP return values you can receive, see the RFC 2616 specification from the Internet Engineering Task Force at [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10).</span></span>

 

 