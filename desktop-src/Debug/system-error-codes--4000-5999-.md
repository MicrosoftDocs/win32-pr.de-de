---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 4000-5999 und ist für Entwickler bestimmt.
ms.assetid: 1d2f7160-6322-4c75-abbc-4a882bbdf7ce
title: System Fehler Codes (4000-5999) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: bfd39042489f2a92ff2eb13df92a22e392c5405e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126892"
---
# <a name="system-error-codes-4000-5999"></a><span data-ttu-id="e671e-103">System Fehler Codes (4000-5999)</span><span class="sxs-lookup"><span data-stu-id="e671e-103">System Error Codes (4000-5999)</span></span>

> [!NOTE]
> <span data-ttu-id="e671e-104">Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen.</span><span class="sxs-lookup"><span data-stu-id="e671e-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="e671e-105">Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="e671e-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="e671e-106">In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) für die Fehler 4000 bis 5999 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e671e-106">The following list describes [system error codes](system-error-codes.md) for errors 4000 to 5999.</span></span> <span data-ttu-id="e671e-107">Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="e671e-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="e671e-108">Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".</span><span class="sxs-lookup"><span data-stu-id="e671e-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="e671e-109"><span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**Fehler \_ gewinnt \_ intern**</span><span class="sxs-lookup"><span data-stu-id="e671e-109"><span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**ERROR\_WINS\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-110">4000 (0xfa0)</span><span class="sxs-lookup"><span data-stu-id="e671e-110">4000 (0xFA0)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-111">Fehler beim Verarbeiten des Befehls.</span><span class="sxs-lookup"><span data-stu-id="e671e-111">WINS encountered an error while processing the command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-112"><span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**Fehler \_ beim \_ \_ \_ lokalen \_ WINS-Fehler.**</span><span class="sxs-lookup"><span data-stu-id="e671e-112"><span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**ERROR\_CAN\_NOT\_DEL\_LOCAL\_WINS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-113">4001 (0xfa1)</span><span class="sxs-lookup"><span data-stu-id="e671e-113">4001 (0xFA1)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-114">Der lokale WINS kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-114">The local WINS cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-115"><span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**Fehler bei \_ statischer \_ Init**</span><span class="sxs-lookup"><span data-stu-id="e671e-115"><span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**ERROR\_STATIC\_INIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-116">4002 (0xfa2)</span><span class="sxs-lookup"><span data-stu-id="e671e-116">4002 (0xFA2)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-117">Fehler beim Importieren aus der Datei.</span><span class="sxs-lookup"><span data-stu-id="e671e-117">The importation from the file failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-118"><span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**Fehler \_ inkl. \_ Sicherung**</span><span class="sxs-lookup"><span data-stu-id="e671e-118"><span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**ERROR\_INC\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-119">4003 (0xfa3)</span><span class="sxs-lookup"><span data-stu-id="e671e-119">4003 (0xFA3)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-120">Die Sicherung ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="e671e-120">The backup failed.</span></span> <span data-ttu-id="e671e-121">Wurde zuvor eine vollständige Sicherung durchgeführt?</span><span class="sxs-lookup"><span data-stu-id="e671e-121">Was a full backup done before?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-122"><span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**\_vollständige Fehler \_ Sicherung**</span><span class="sxs-lookup"><span data-stu-id="e671e-122"><span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**ERROR\_FULL\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-123">4004 (0xfa4)</span><span class="sxs-lookup"><span data-stu-id="e671e-123">4004 (0xFA4)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-124">Die Sicherung ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="e671e-124">The backup failed.</span></span> <span data-ttu-id="e671e-125">Überprüfen Sie das Verzeichnis, in dem Sie die Datenbank sichern.</span><span class="sxs-lookup"><span data-stu-id="e671e-125">Check the directory to which you are backing the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-126"><span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**Fehler- \_ rec \_ nicht \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="e671e-126"><span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**ERROR\_REC\_NON\_EXISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-127">4005 (0xfa5)</span><span class="sxs-lookup"><span data-stu-id="e671e-127">4005 (0xFA5)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-128">Der Name ist in der WINS-Datenbank nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e671e-128">The name does not exist in the WINS database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-129"><span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**Fehler- \_ RPL \_ nicht \_ zulässig**</span><span class="sxs-lookup"><span data-stu-id="e671e-129"><span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**ERROR\_RPL\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-130">4006 (0xfa6)</span><span class="sxs-lookup"><span data-stu-id="e671e-130">4006 (0xFA6)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-131">Die Replikation mit einem nicht konfigurierten Partner ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="e671e-131">Replication with a nonconfigured partner is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-132"><span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**Die ContentInfo-Version von "Peer" ist \_ \_ \_ \_ nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="e671e-132"><span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**PEERDIST\_ERROR\_CONTENTINFO\_VERSION\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-133">4050 (0xF-2)</span><span class="sxs-lookup"><span data-stu-id="e671e-133">4050 (0xFD2)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-134">Die Version der bereitgestellten Inhaltsinformationen wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e671e-134">The version of the supplied content information is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-135"><span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**der Peer-Manager- \_ Fehler \_ kann \_ \_ ContentInfo nicht analysieren.**</span><span class="sxs-lookup"><span data-stu-id="e671e-135"><span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**PEERDIST\_ERROR\_CANNOT\_PARSE\_CONTENTINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-136">4051 (0xF-3)</span><span class="sxs-lookup"><span data-stu-id="e671e-136">4051 (0xFD3)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-137">Die angegebenen Inhaltsinformationen sind falsch formatiert.</span><span class="sxs-lookup"><span data-stu-id="e671e-137">The supplied content information is malformed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-138"><span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**Fehler beim Peer von "Peer". \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-138"><span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**PEERDIST\_ERROR\_MISSING\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-139">4052 (0xF)</span><span class="sxs-lookup"><span data-stu-id="e671e-139">4052 (0xFD4)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-140">Die angeforderten Daten wurden in lokalen oder Peer Caches nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e671e-140">The requested data cannot be found in local or peer caches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-141"><span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**Peer \_ Fehler \_ nicht \_ mehr**</span><span class="sxs-lookup"><span data-stu-id="e671e-141"><span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**PEERDIST\_ERROR\_NO\_MORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-142">4053 (0xF D5)</span><span class="sxs-lookup"><span data-stu-id="e671e-142">4053 (0xFD5)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-143">Es sind keine weiteren Daten verfügbar oder erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e671e-143">No more data is available or required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-144"><span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**der Peer-Manager- \_ Fehler wurde \_ nicht \_ initialisiert.**</span><span class="sxs-lookup"><span data-stu-id="e671e-144"><span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**PEERDIST\_ERROR\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-145">4054 (0xF, 6)</span><span class="sxs-lookup"><span data-stu-id="e671e-145">4054 (0xFD6)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-146">Das angegebene Objekt wurde nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="e671e-146">The supplied object has not been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-147"><span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**der Peer-dist- \_ Fehler wurde \_ bereits \_ initialisiert.**</span><span class="sxs-lookup"><span data-stu-id="e671e-147"><span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**PEERDIST\_ERROR\_ALREADY\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-148">4055 (0xF)</span><span class="sxs-lookup"><span data-stu-id="e671e-148">4055 (0xFD7)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-149">Das angegebene Objekt wurde bereits initialisiert.</span><span class="sxs-lookup"><span data-stu-id="e671e-149">The supplied object has already been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-150"><span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**\_Fehler \_ beim Herunterfahren \_ des \_ Peer-dist-Vorgangs.**</span><span class="sxs-lookup"><span data-stu-id="e671e-150"><span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**PEERDIST\_ERROR\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-151">4056 (0xF D8)</span><span class="sxs-lookup"><span data-stu-id="e671e-151">4056 (0xFD8)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-152">Ein Shutdown-Vorgang wird bereits ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e671e-152">A shutdown operation is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-153"><span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**der Peer \_ Fehler ist \_ ungültig.**</span><span class="sxs-lookup"><span data-stu-id="e671e-153"><span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**PEERDIST\_ERROR\_INVALIDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-154">4057 (0xF)</span><span class="sxs-lookup"><span data-stu-id="e671e-154">4057 (0xFD9)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-155">Das angegebene Objekt wurde bereits für ungültig erklärt.</span><span class="sxs-lookup"><span data-stu-id="e671e-155">The supplied object has already been invalidated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-156"><span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**der Peer-Manager- \_ Fehler ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-156"><span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**PEERDIST\_ERROR\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-157">4058 (0xfda)</span><span class="sxs-lookup"><span data-stu-id="e671e-157">4058 (0xFDA)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-158">Ein Element ist bereits vorhanden und wurde nicht ersetzt.</span><span class="sxs-lookup"><span data-stu-id="e671e-158">An element already exists and was not replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-159"><span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**Fehler beim Peer \_ - \_ /Fehlervorgang. \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-159"><span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**PEERDIST\_ERROR\_OPERATION\_NOTFOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-160">4059 (0xF)</span><span class="sxs-lookup"><span data-stu-id="e671e-160">4059 (0xFDB)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-161">Der angeforderte Vorgang kann nicht abgebrochen werden, da er bereits abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-161">Can not cancel the requested operation as it has already been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-162"><span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**der Peer-Manager- \_ Fehler ist \_ bereits \_ abgeschlossen.**</span><span class="sxs-lookup"><span data-stu-id="e671e-162"><span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**PEERDIST\_ERROR\_ALREADY\_COMPLETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-163">4060 (0xF)</span><span class="sxs-lookup"><span data-stu-id="e671e-163">4060 (0xFDC)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-164">Der Vorgang kann nicht durchgeführt werden, da er bereits durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="e671e-164">Can not perform the reqested operation because it has already been carried out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-165"><span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**Peer \_ Fehler \_ außerhalb \_ des \_ gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="e671e-165"><span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**PEERDIST\_ERROR\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-166">4061 (0xF)</span><span class="sxs-lookup"><span data-stu-id="e671e-166">4061 (0xFDD)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-167">Ein Vorgang, auf den über die Grenzen gültiger Daten zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="e671e-167">An operation accessed data beyond the bounds of valid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-168"><span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**\_ \_ \_ nicht unterstützte Version von "Peer Manager"**</span><span class="sxs-lookup"><span data-stu-id="e671e-168"><span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**PEERDIST\_ERROR\_VERSION\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-169">4062 (0xF)</span><span class="sxs-lookup"><span data-stu-id="e671e-169">4062 (0xFDE)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-170">Die angeforderte Version wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e671e-170">The requested version is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-171"><span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**\_ \_ ungültige Konfiguration des Peer-dist-Fehlers \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-171"><span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**PEERDIST\_ERROR\_INVALID\_CONFIGURATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-172">4063 (0xF)</span><span class="sxs-lookup"><span data-stu-id="e671e-172">4063 (0xFDF)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-173">Ein Konfigurations Wert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e671e-173">A configuration value is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-174"><span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**der Peer \_ Fehler ist \_ nicht \_ lizenziert.**</span><span class="sxs-lookup"><span data-stu-id="e671e-174"><span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**PEERDIST\_ERROR\_NOT\_LICENSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-175">4064 (0xfe0)</span><span class="sxs-lookup"><span data-stu-id="e671e-175">4064 (0xFE0)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-176">Die SKU ist nicht lizenziert.</span><span class="sxs-lookup"><span data-stu-id="e671e-176">The SKU is not licensed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-177"><span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**Peer- \_ \_ /fehlerdienst nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="e671e-177"><span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**PEERDIST\_ERROR\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-178">4065 (0xfe1)</span><span class="sxs-lookup"><span data-stu-id="e671e-178">4065 (0xFE1)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-179">Der Peer-Manager-Dienst wird noch initialisiert und ist in Kürze verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e671e-179">PeerDist Service is still initializing and will be available shortly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-180"><span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**Fehler bei der Peer- \_ \_ Vertrauensstellung \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-180"><span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**PEERDIST\_ERROR\_TRUST\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-181">4066 (0xfe2)</span><span class="sxs-lookup"><span data-stu-id="e671e-181">4066 (0xFE2)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-182">Die Kommunikation mit einem oder mehreren Computern wird aufgrund aktueller Fehler vorübergehend blockiert.</span><span class="sxs-lookup"><span data-stu-id="e671e-182">Communication with one or more computers will be temporarily blocked due to recent errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-183"><span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**Fehler \_ DHCP- \_ Adress \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="e671e-183"><span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**ERROR\_DHCP\_ADDRESS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-184">4100 (0x1004)</span><span class="sxs-lookup"><span data-stu-id="e671e-184">4100 (0x1004)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-185">Der DHCP-Client hat eine IP-Adresse abgerufen, die bereits im Netzwerk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e671e-185">The DHCP client has obtained an IP address that is already in use on the network.</span></span> <span data-ttu-id="e671e-186">Die lokale Schnittstelle wird deaktiviert, bis der DHCP-Client eine neue Adresse abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="e671e-186">The local interface will be disabled until the DHCP client can obtain a new address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-187"><span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**Fehler beim \_ WMI- \_ GUID wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-187"><span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**ERROR\_WMI\_GUID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-188">4200 (0x1068)</span><span class="sxs-lookup"><span data-stu-id="e671e-188">4200 (0x1068)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-189">Die Übergabe der GUID wurde von einem WMI-Datenanbieter nicht als gültig erkannt.</span><span class="sxs-lookup"><span data-stu-id="e671e-189">The GUID passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-190"><span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**Fehler bei \_ WMI- \_ Instanz \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-190"><span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**ERROR\_WMI\_INSTANCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-191">4201 (0x1069)</span><span class="sxs-lookup"><span data-stu-id="e671e-191">4201 (0x1069)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-192">Der Übergabe des Instanznamens wurde von einem WMI-Datenanbieter nicht als gültig erkannt.</span><span class="sxs-lookup"><span data-stu-id="e671e-192">The instance name passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-193"><span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**Fehler \_ WMI- \_ ItemID \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-193"><span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**ERROR\_WMI\_ITEMID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-194">4202 (0x106a)</span><span class="sxs-lookup"><span data-stu-id="e671e-194">4202 (0x106A)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-195">Die bestandene Datenelement-ID wurde von einem WMI-Datenanbieter nicht als gültig erkannt.</span><span class="sxs-lookup"><span data-stu-id="e671e-195">The data item ID passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-196"><span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**Fehler \_ WMI \_ \_ erneut versuchen**</span><span class="sxs-lookup"><span data-stu-id="e671e-196"><span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**ERROR\_WMI\_TRY\_AGAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-197">4203 (0x106b)</span><span class="sxs-lookup"><span data-stu-id="e671e-197">4203 (0x106B)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-198">Die WMI-Anforderung konnte nicht abgeschlossen werden und sollte erneut versucht werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-198">The WMI request could not be completed and should be retried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-199"><span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**Fehler beim \_ WMI- \_ DP \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-199"><span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**ERROR\_WMI\_DP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-200">4204 (0x106c)</span><span class="sxs-lookup"><span data-stu-id="e671e-200">4204 (0x106C)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-201">Der WMI-Datenanbieter wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e671e-201">The WMI data provider could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-202"><span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**Fehler beim Verweis auf \_ WMI- \_ aufgelöste \_ Instanz \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-202"><span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**ERROR\_WMI\_UNRESOLVED\_INSTANCE\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-203">4205 (0x106d)</span><span class="sxs-lookup"><span data-stu-id="e671e-203">4205 (0x106D)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-204">Der WMI-Datenanbieter verweist auf einen Instanzsatz, der nicht registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="e671e-204">The WMI data provider references an instance set that has not been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-205"><span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**\_WMI-Fehler \_ bereits \_ aktiviert**</span><span class="sxs-lookup"><span data-stu-id="e671e-205"><span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**ERROR\_WMI\_ALREADY\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-206">4206 (0x106 e)</span><span class="sxs-lookup"><span data-stu-id="e671e-206">4206 (0x106E)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-207">Der WMI-Datenblock oder die Ereignis Benachrichtigung wurde bereits aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e671e-207">The WMI data block or event notification has already been enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-208"><span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**Fehler beim \_ WMI- \_ GUID. \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-208"><span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**ERROR\_WMI\_GUID\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-209">4207 (0x106f)</span><span class="sxs-lookup"><span data-stu-id="e671e-209">4207 (0x106F)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-210">Der WMI-Datenblock ist nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e671e-210">The WMI data block is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-211"><span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**Fehler \_ WMI- \_ Server nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="e671e-211"><span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**ERROR\_WMI\_SERVER\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-212">4208 (0x1070)</span><span class="sxs-lookup"><span data-stu-id="e671e-212">4208 (0x1070)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-213">Der WMI-Datendienst ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e671e-213">The WMI data service is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-214"><span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**Fehler beim WMI-Fehler. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-214"><span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**ERROR\_WMI\_DP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-215">4209 (0x1071)</span><span class="sxs-lookup"><span data-stu-id="e671e-215">4209 (0x1071)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-216">Fehler beim Ausführen der Anforderung durch den WMI-Datenanbieter.</span><span class="sxs-lookup"><span data-stu-id="e671e-216">The WMI data provider failed to carry out the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-217"><span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**Fehler \_ WMI \_ ungültige \_ MOF**</span><span class="sxs-lookup"><span data-stu-id="e671e-217"><span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**ERROR\_WMI\_INVALID\_MOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-218">4210 (0x1072)</span><span class="sxs-lookup"><span data-stu-id="e671e-218">4210 (0x1072)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-219">Die WMI-MOF-Informationen sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="e671e-219">The WMI MOF information is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-220"><span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**Fehler \_ WMI \_ ungültige \_ reginfo**</span><span class="sxs-lookup"><span data-stu-id="e671e-220"><span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**ERROR\_WMI\_INVALID\_REGINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-221">4211 (0x1073)</span><span class="sxs-lookup"><span data-stu-id="e671e-221">4211 (0x1073)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-222">Die WMI-Registrierungsinformationen sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="e671e-222">The WMI registration information is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-223"><span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**WMI-Fehler ist \_ \_ bereits \_ deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="e671e-223"><span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**ERROR\_WMI\_ALREADY\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-224">4212 (0x1074)</span><span class="sxs-lookup"><span data-stu-id="e671e-224">4212 (0x1074)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-225">Der WMI-Datenblock oder die Ereignis Benachrichtigung wurde bereits deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e671e-225">The WMI data block or event notification has already been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-226"><span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**WMI-Fehler schreibgeschützt \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-226"><span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**ERROR\_WMI\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-227">4213 (0x1075)</span><span class="sxs-lookup"><span data-stu-id="e671e-227">4213 (0x1075)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-228">Das WMI-Datenelement oder der Datenblock ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e671e-228">The WMI data item or data block is read only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-229"><span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**Fehler beim \_ WMI-Fehler \_ Satz. \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-229"><span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**ERROR\_WMI\_SET\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-230">4214 (0x1076)</span><span class="sxs-lookup"><span data-stu-id="e671e-230">4214 (0x1076)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-231">Das WMI-Datenelement oder der Datenblock konnte nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-231">The WMI data item or data block could not be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-232"><span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**Fehler \_ nicht \_ appcontainer**</span><span class="sxs-lookup"><span data-stu-id="e671e-232"><span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**ERROR\_NOT\_APPCONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-233">4250 (0x109a)</span><span class="sxs-lookup"><span data-stu-id="e671e-233">4250 (0x109A)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-234">Dieser Vorgang ist nur im Kontext eines App-Containers gültig.</span><span class="sxs-lookup"><span data-stu-id="e671e-234">This operation is only valid in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-235"><span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**Fehler \_ appcontainer \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="e671e-235"><span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**ERROR\_APPCONTAINER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-236">4251 (0x109b)</span><span class="sxs-lookup"><span data-stu-id="e671e-236">4251 (0x109B)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-237">Diese Anwendung kann nur im Kontext eines App-Containers ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-237">This application can only run in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-238"><span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**Fehler \_ \_ wird \_ in appcontainer nicht unterstützt \_ .**</span><span class="sxs-lookup"><span data-stu-id="e671e-238"><span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**ERROR\_NOT\_SUPPORTED\_IN\_APPCONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-239">4252 (0x109c)</span><span class="sxs-lookup"><span data-stu-id="e671e-239">4252 (0x109C)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-240">Diese Funktion wird im Kontext eines App-Containers nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e671e-240">This functionality is not supported in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-241"><span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**Fehler \_ ungültige \_ Paket- \_ sid- \_ Länge**</span><span class="sxs-lookup"><span data-stu-id="e671e-241"><span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**ERROR\_INVALID\_PACKAGE\_SID\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-242">4253 (0x109d)</span><span class="sxs-lookup"><span data-stu-id="e671e-242">4253 (0x109D)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-243">Die Länge der angegebenen SID ist keine gültige Länge für App-Container-SIDs.</span><span class="sxs-lookup"><span data-stu-id="e671e-243">The length of the SID supplied is not a valid length for app container SIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-244"><span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**\_ungültiger \_ Medien Fehler**</span><span class="sxs-lookup"><span data-stu-id="e671e-244"><span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**ERROR\_INVALID\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-245">4300 (0x10cc)</span><span class="sxs-lookup"><span data-stu-id="e671e-245">4300 (0x10CC)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-246">Der Medien Bezeichner stellt kein gültiges Medium dar.</span><span class="sxs-lookup"><span data-stu-id="e671e-246">The media identifier does not represent a valid medium.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-247"><span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**\_ungültige \_ Bibliothek.**</span><span class="sxs-lookup"><span data-stu-id="e671e-247"><span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**ERROR\_INVALID\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-248">4301 (0x10cd)</span><span class="sxs-lookup"><span data-stu-id="e671e-248">4301 (0x10CD)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-249">Der Bibliotheks Bezeichner stellt keine gültige Bibliothek dar.</span><span class="sxs-lookup"><span data-stu-id="e671e-249">The library identifier does not represent a valid library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-250"><span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**\_ungültiger \_ Medien \_ Pool**</span><span class="sxs-lookup"><span data-stu-id="e671e-250"><span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**ERROR\_INVALID\_MEDIA\_POOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-251">4302 (0x10ce)</span><span class="sxs-lookup"><span data-stu-id="e671e-251">4302 (0x10CE)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-252">Der Medienpool Bezeichner stellt keinen gültigen Medienpool dar.</span><span class="sxs-lookup"><span data-stu-id="e671e-252">The media pool identifier does not represent a valid media pool.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-253"><span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**Fehler \_ Laufwerk \_ Medien \_ stimmen nicht überein.**</span><span class="sxs-lookup"><span data-stu-id="e671e-253"><span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**ERROR\_DRIVE\_MEDIA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-254">4303 (0x10cf)</span><span class="sxs-lookup"><span data-stu-id="e671e-254">4303 (0x10CF)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-255">Das Laufwerk und das Medium sind nicht kompatibel oder nicht in verschiedenen Bibliotheken vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e671e-255">The drive and medium are not compatible or exist in different libraries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-256"><span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**Fehler \_ Medien \_ Offline**</span><span class="sxs-lookup"><span data-stu-id="e671e-256"><span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**ERROR\_MEDIA\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-257">4304 (0x10d0)</span><span class="sxs-lookup"><span data-stu-id="e671e-257">4304 (0x10D0)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-258">Das Medium ist zurzeit in einer Offline Bibliothek vorhanden und muss online sein, um diesen Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e671e-258">The medium currently exists in an offline library and must be online to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-259"><span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**Fehler \_ Bibliothek \_ Offline**</span><span class="sxs-lookup"><span data-stu-id="e671e-259"><span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**ERROR\_LIBRARY\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-260">4305 (0x10d1)</span><span class="sxs-lookup"><span data-stu-id="e671e-260">4305 (0x10D1)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-261">Der Vorgang kann nicht für eine Offline Bibliothek ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-261">The operation cannot be performed on an offline library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-262"><span id="ERROR_EMPTY"></span><span id="error_empty"></span>**Fehler \_ leer**</span><span class="sxs-lookup"><span data-stu-id="e671e-262"><span id="ERROR_EMPTY"></span><span id="error_empty"></span>**ERROR\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-263">4306 (0x10d2)</span><span class="sxs-lookup"><span data-stu-id="e671e-263">4306 (0x10D2)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-264">Die Bibliothek, das Laufwerk oder der Medienpool ist leer.</span><span class="sxs-lookup"><span data-stu-id="e671e-264">The library, drive, or media pool is empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-265"><span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**Fehler ist \_ nicht \_ leer.**</span><span class="sxs-lookup"><span data-stu-id="e671e-265"><span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**ERROR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-266">4307 (0x10d3)</span><span class="sxs-lookup"><span data-stu-id="e671e-266">4307 (0x10D3)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-267">Die Bibliothek, das Laufwerk oder der Medienpool müssen leer sein, um diesen Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e671e-267">The library, drive, or media pool must be empty to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-268"><span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**Fehler \_ Medien nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="e671e-268"><span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**ERROR\_MEDIA\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-269">4308 (0x10d4)</span><span class="sxs-lookup"><span data-stu-id="e671e-269">4308 (0x10D4)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-270">In diesem Medienpool oder in der Bibliothek sind zurzeit keine Medien verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e671e-270">No media is currently available in this media pool or library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-271"><span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**Fehler \_ Ressource \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="e671e-271"><span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**ERROR\_RESOURCE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-272">4309 (0x10d5)</span><span class="sxs-lookup"><span data-stu-id="e671e-272">4309 (0x10D5)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-273">Eine für diesen Vorgang erforderliche Ressource ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e671e-273">A resource required for this operation is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-274"><span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**Fehler \_ ungültiger \_ Reinigungs Fehler**</span><span class="sxs-lookup"><span data-stu-id="e671e-274"><span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**ERROR\_INVALID\_CLEANER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-275">4310 (0x10d6)</span><span class="sxs-lookup"><span data-stu-id="e671e-275">4310 (0x10D6)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-276">Der Medien Bezeichner stellt keinen gültigen Bereinigungs Wert dar.</span><span class="sxs-lookup"><span data-stu-id="e671e-276">The media identifier does not represent a valid cleaner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-277"><span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**Fehler \_ beim \_ \_ bereinigen.**</span><span class="sxs-lookup"><span data-stu-id="e671e-277"><span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**ERROR\_UNABLE\_TO\_CLEAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-278">4311 (0x10d7)</span><span class="sxs-lookup"><span data-stu-id="e671e-278">4311 (0x10D7)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-279">Das Laufwerk kann nicht bereinigt werden oder unterstützt keine Bereinigung.</span><span class="sxs-lookup"><span data-stu-id="e671e-279">The drive cannot be cleaned or does not support cleaning.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-280"><span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**Fehler \_ Objekt wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-280"><span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**ERROR\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-281">4312 (0x10d8)</span><span class="sxs-lookup"><span data-stu-id="e671e-281">4312 (0x10D8)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-282">Der Objekt Bezeichner stellt kein gültiges Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="e671e-282">The object identifier does not represent a valid object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-283"><span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**Fehler \_ Daten Bank \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="e671e-283"><span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**ERROR\_DATABASE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-284">4313 (0x10d9)</span><span class="sxs-lookup"><span data-stu-id="e671e-284">4313 (0x10D9)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-285">Aus der Datenbank kann nicht gelesen oder in diese geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-285">Unable to read from or write to the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-286"><span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**Fehler \_ Datenbank \_ voll**</span><span class="sxs-lookup"><span data-stu-id="e671e-286"><span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**ERROR\_DATABASE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-287">4314 (0x10da)</span><span class="sxs-lookup"><span data-stu-id="e671e-287">4314 (0x10DA)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-288">Die Datenbank ist voll.</span><span class="sxs-lookup"><span data-stu-id="e671e-288">The database is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-289"><span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**Fehler \_ Medien nicht \_ kompatibel**</span><span class="sxs-lookup"><span data-stu-id="e671e-289"><span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**ERROR\_MEDIA\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-290">4315 (0x10db)</span><span class="sxs-lookup"><span data-stu-id="e671e-290">4315 (0x10DB)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-291">Das Medium ist mit dem Gerät oder dem Medienpool nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e671e-291">The medium is not compatible with the device or media pool.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-292"><span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**die Fehler \_ Ressource ist \_ nicht \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-292"><span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**ERROR\_RESOURCE\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-293">4316 (0x10dc)</span><span class="sxs-lookup"><span data-stu-id="e671e-293">4316 (0x10DC)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-294">Die für diesen Vorgang erforderliche Ressource ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e671e-294">The resource required for this operation does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-295"><span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**\_ungültiger \_ Vorgang.**</span><span class="sxs-lookup"><span data-stu-id="e671e-295"><span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**ERROR\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-296">4317 (0x10dd)</span><span class="sxs-lookup"><span data-stu-id="e671e-296">4317 (0x10DD)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-297">Der Vorgangs Bezeichner ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e671e-297">The operation identifier is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-298"><span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**Fehler \_ Medien \_ nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="e671e-298"><span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**ERROR\_MEDIA\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-299">4318 (0x10de)</span><span class="sxs-lookup"><span data-stu-id="e671e-299">4318 (0x10DE)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-300">Das Medium ist nicht bereitgestellt oder kann nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-300">The media is not mounted or ready for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-301"><span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**Fehler \_ Gerät \_ nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="e671e-301"><span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**ERROR\_DEVICE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-302">4319 (0x10df)</span><span class="sxs-lookup"><span data-stu-id="e671e-302">4319 (0x10DF)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-303">Das Gerät ist nicht einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="e671e-303">The device is not ready for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-304"><span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**Fehler \_ Anforderung \_ abgelehnt**</span><span class="sxs-lookup"><span data-stu-id="e671e-304"><span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**ERROR\_REQUEST\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-305">4320 (0x10e0)</span><span class="sxs-lookup"><span data-stu-id="e671e-305">4320 (0x10E0)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-306">Der Operator oder Administrator hat die Anforderung abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="e671e-306">The operator or administrator has refused the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-307"><span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**Fehler \_ ungültiges \_ Laufwerks \_ Objekt.**</span><span class="sxs-lookup"><span data-stu-id="e671e-307"><span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**ERROR\_INVALID\_DRIVE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-308">4321 (0x10e1)</span><span class="sxs-lookup"><span data-stu-id="e671e-308">4321 (0x10E1)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-309">Der Laufwerks Bezeichner stellt kein gültiges Laufwerk dar.</span><span class="sxs-lookup"><span data-stu-id="e671e-309">The drive identifier does not represent a valid drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-310"><span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**Fehler \_ Bibliothek \_ voll**</span><span class="sxs-lookup"><span data-stu-id="e671e-310"><span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**ERROR\_LIBRARY\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-311">4322 (0x10e2)</span><span class="sxs-lookup"><span data-stu-id="e671e-311">4322 (0x10E2)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-312">Die Bibliothek ist voll.</span><span class="sxs-lookup"><span data-stu-id="e671e-312">Library is full.</span></span> <span data-ttu-id="e671e-313">Es ist kein Slot zur Verwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e671e-313">No slot is available for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-314"><span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**Fehler \_ Medium ist \_ nicht \_ verfügbar.**</span><span class="sxs-lookup"><span data-stu-id="e671e-314"><span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**ERROR\_MEDIUM\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-315">4323 (0x10e3)</span><span class="sxs-lookup"><span data-stu-id="e671e-315">4323 (0x10E3)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-316">Der Transport kann nicht auf das Medium zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e671e-316">The transport cannot access the medium.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-317"><span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**Fehler \_ beim \_ \_ Laden des \_ Mediums.**</span><span class="sxs-lookup"><span data-stu-id="e671e-317"><span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**ERROR\_UNABLE\_TO\_LOAD\_MEDIUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-318">4324 (0x10e4)</span><span class="sxs-lookup"><span data-stu-id="e671e-318">4324 (0x10E4)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-319">Das Medium kann nicht in das Laufwerk geladen werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-319">Unable to load the medium into the drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-320"><span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**Fehler \_ beim \_ \_ inventarisieren des \_ Laufwerks**</span><span class="sxs-lookup"><span data-stu-id="e671e-320"><span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-321">4325 (0x10e5)</span><span class="sxs-lookup"><span data-stu-id="e671e-321">4325 (0x10E5)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-322">Der Laufwerks Status kann nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-322">Unable to retrieve the drive status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-323"><span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**Fehler \_ beim \_ \_ inventarisieren des \_ Slots.**</span><span class="sxs-lookup"><span data-stu-id="e671e-323"><span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_SLOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-324">4326 (0x10e6)</span><span class="sxs-lookup"><span data-stu-id="e671e-324">4326 (0x10E6)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-325">Der slotstatus kann nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-325">Unable to retrieve the slot status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-326"><span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**Fehler \_ beim \_ \_ inventarisieren des \_ Transports.**</span><span class="sxs-lookup"><span data-stu-id="e671e-326"><span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_TRANSPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-327">4327 (0x10e7)</span><span class="sxs-lookup"><span data-stu-id="e671e-327">4327 (0x10E7)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-328">Der Status des Transports kann nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-328">Unable to retrieve status about the transport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-329"><span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**Fehler \_ Transport \_ voll**</span><span class="sxs-lookup"><span data-stu-id="e671e-329"><span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**ERROR\_TRANSPORT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-330">4328 (0x10e8)</span><span class="sxs-lookup"><span data-stu-id="e671e-330">4328 (0x10E8)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-331">Der Transport kann nicht verwendet werden, da er bereits verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e671e-331">Cannot use the transport because it is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-332"><span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**Fehler beim \_ Steuern von \_ ieport.**</span><span class="sxs-lookup"><span data-stu-id="e671e-332"><span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**ERROR\_CONTROLLING\_IEPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-333">4329 (0x10e9)</span><span class="sxs-lookup"><span data-stu-id="e671e-333">4329 (0x10E9)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-334">Der einschleusen-/Ausgabeport kann nicht geöffnet oder geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-334">Unable to open or close the inject/eject port.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-335"><span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**Fehler \_ beim \_ \_ \_ eingebundenen Medienobjekt \_ .**</span><span class="sxs-lookup"><span data-stu-id="e671e-335"><span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**ERROR\_UNABLE\_TO\_EJECT\_MOUNTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-336">4330 (0x10ea)</span><span class="sxs-lookup"><span data-stu-id="e671e-336">4330 (0x10EA)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-337">Das Medium kann nicht ausstoßen, weil es sich in einem Laufwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="e671e-337">Unable to eject the medium because it is in a drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-338"><span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**\_fehlerreinigungs \_ - \_ slotset**</span><span class="sxs-lookup"><span data-stu-id="e671e-338"><span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**ERROR\_CLEANER\_SLOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-339">4331 (0x10eb)</span><span class="sxs-lookup"><span data-stu-id="e671e-339">4331 (0x10EB)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-340">Ein Reinigungs Slot ist bereits reserviert.</span><span class="sxs-lookup"><span data-stu-id="e671e-340">A cleaner slot is already reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-341"><span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**Fehlerbereinigungs \_ \_ Slot \_ nicht \_ festgelegt**</span><span class="sxs-lookup"><span data-stu-id="e671e-341"><span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**ERROR\_CLEANER\_SLOT\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-342">4332 (0x10ec)</span><span class="sxs-lookup"><span data-stu-id="e671e-342">4332 (0x10EC)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-343">Ein Reinigungs Slot ist nicht reserviert.</span><span class="sxs-lookup"><span data-stu-id="e671e-343">A cleaner slot is not reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-344"><span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**Fehler \_ Reinigungs- \_ Cartridge \_ aufgewendet**</span><span class="sxs-lookup"><span data-stu-id="e671e-344"><span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**ERROR\_CLEANER\_CARTRIDGE\_SPENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-345">4333 (0x10ed)</span><span class="sxs-lookup"><span data-stu-id="e671e-345">4333 (0x10ED)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-346">Die Reinigungs Patrone hat die maximale Anzahl von Laufwerks Bereinigungs Vorlagen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e671e-346">The cleaner cartridge has performed the maximum number of drive cleanings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-347"><span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**\_unerwarteter Fehler bei \_ Omid.**</span><span class="sxs-lookup"><span data-stu-id="e671e-347"><span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**ERROR\_UNEXPECTED\_OMID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-348">4334 (0x10ee)</span><span class="sxs-lookup"><span data-stu-id="e671e-348">4334 (0x10EE)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-349">Unerwarteter auf-Medium-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e671e-349">Unexpected on-medium identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-350"><span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**Fehler \_ \_ beim Löschen des \_ letzten \_ Elements.**</span><span class="sxs-lookup"><span data-stu-id="e671e-350"><span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**ERROR\_CANT\_DELETE\_LAST\_ITEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-351">4335 (0x10ef)</span><span class="sxs-lookup"><span data-stu-id="e671e-351">4335 (0x10EF)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-352">Das letzte verbleibende Element in dieser Gruppe oder Ressource kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-352">The last remaining item in this group or resource cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-353"><span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**die Fehler \_ Meldung über \_ schreitet die \_ Maximale \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="e671e-353"><span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**ERROR\_MESSAGE\_EXCEEDS\_MAX\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-354">4336 (0x10f 0)</span><span class="sxs-lookup"><span data-stu-id="e671e-354">4336 (0x10F0)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-355">Die angegebene Meldung überschreitet die maximal zulässige Größe für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="e671e-355">The message provided exceeds the maximum size allowed for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-356"><span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**Fehler \_ Volume \_ enthält \_ sys- \_ Dateien**</span><span class="sxs-lookup"><span data-stu-id="e671e-356"><span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**ERROR\_VOLUME\_CONTAINS\_SYS\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-357">4337 (0x10f)</span><span class="sxs-lookup"><span data-stu-id="e671e-357">4337 (0x10F1)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-358">Das Volume enthält System-oder Auslagerungs Dateien.</span><span class="sxs-lookup"><span data-stu-id="e671e-358">The volume contains system or paging files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-359"><span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**\_Typ des indigenen Fehlers \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-359"><span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**ERROR\_INDIGENOUS\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-360">4338 (0x10f 2)</span><span class="sxs-lookup"><span data-stu-id="e671e-360">4338 (0x10F2)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-361">Der Medientyp kann nicht aus dieser Bibliothek entfernt werden, da mindestens ein Laufwerk in der Bibliothek meldet, dass dieser Medientyp unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e671e-361">The media type cannot be removed from this library since at least one drive in the library reports it can support this media type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-362"><span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**Fehler \_ beim \_ unterstützen von \_ Laufwerken**</span><span class="sxs-lookup"><span data-stu-id="e671e-362"><span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**ERROR\_NO\_SUPPORTING\_DRIVES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-363">4339 (0x10f)</span><span class="sxs-lookup"><span data-stu-id="e671e-363">4339 (0x10F3)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-364">Diese Offline Medien können nicht auf diesem System bereitgestellt werden, da keine aktivierten Laufwerke vorhanden sind, die verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e671e-364">This offline media cannot be mounted on this system since no enabled drives are present which can be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-365"><span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**Fehler \_ Reinigungs- \_ Cartridge \_ installiert**</span><span class="sxs-lookup"><span data-stu-id="e671e-365"><span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**ERROR\_CLEANER\_CARTRIDGE\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-366">4340 (0x10f)</span><span class="sxs-lookup"><span data-stu-id="e671e-366">4340 (0x10F4)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-367">In der Band Bibliothek ist eine Reinigungs Bare Cartridge vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e671e-367">A cleaner cartridge is present in the tape library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-368"><span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**Fehler- \_ ieport \_ voll**</span><span class="sxs-lookup"><span data-stu-id="e671e-368"><span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**ERROR\_IEPORT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-369">4341 (0x10f)</span><span class="sxs-lookup"><span data-stu-id="e671e-369">4341 (0x10F5)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-370">Der einschleusen-/Ausgabeport kann nicht verwendet werden, da er nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-370">Cannot use the inject/eject port because it is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-371"><span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**Fehler \_ Datei \_ Offline**</span><span class="sxs-lookup"><span data-stu-id="e671e-371"><span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**ERROR\_FILE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-372">4350 (0x10fe)</span><span class="sxs-lookup"><span data-stu-id="e671e-372">4350 (0x10FE)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-373">Diese Datei ist zurzeit nicht für die Verwendung auf diesem Computer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e671e-373">This file is currently not available for use on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-374"><span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**Fehler beim \_ Remote \_ Speicher ist \_ nicht \_ aktiv.**</span><span class="sxs-lookup"><span data-stu-id="e671e-374"><span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**ERROR\_REMOTE\_STORAGE\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-375">4351 (0x10ff)</span><span class="sxs-lookup"><span data-stu-id="e671e-375">4351 (0x10FF)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-376">Der Remote Speicherdienst ist zurzeit nicht funktionsfähig.</span><span class="sxs-lookup"><span data-stu-id="e671e-376">The remote storage service is not operational at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-377"><span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**Fehler beim \_ Remote \_ Speicher \_ Medium \_ .**</span><span class="sxs-lookup"><span data-stu-id="e671e-377"><span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**ERROR\_REMOTE\_STORAGE\_MEDIA\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-378">4352 (0x1100)</span><span class="sxs-lookup"><span data-stu-id="e671e-378">4352 (0x1100)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-379">Der Remote Speicherdienst hat einen Medien Fehler gefunden.</span><span class="sxs-lookup"><span data-stu-id="e671e-379">The remote storage service encountered a media error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-380"><span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**Fehler, \_ kein Analyse \_ \_ \_ Punkt**</span><span class="sxs-lookup"><span data-stu-id="e671e-380"><span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**ERROR\_NOT\_A\_REPARSE\_POINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-381">4390 (0x1126)</span><span class="sxs-lookup"><span data-stu-id="e671e-381">4390 (0x1126)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-382">Die Datei oder das Verzeichnis ist kein Analyse Punkt.</span><span class="sxs-lookup"><span data-stu-id="e671e-382">The file or directory is not a reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-383"><span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**Fehleranalyse \_ \_ Attribut \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="e671e-383"><span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**ERROR\_REPARSE\_ATTRIBUTE\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-384">4391 (0x1127)</span><span class="sxs-lookup"><span data-stu-id="e671e-384">4391 (0x1127)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-385">Das Attribut für den Analyse Punkt kann nicht festgelegt werden, da es mit einem vorhandenen Attribut in Konflikt steht.</span><span class="sxs-lookup"><span data-stu-id="e671e-385">The reparse point attribute cannot be set because it conflicts with an existing attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-386"><span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**Fehler beim Analysieren von \_ \_ \_ Daten.**</span><span class="sxs-lookup"><span data-stu-id="e671e-386"><span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**ERROR\_INVALID\_REPARSE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-387">4392 (0x1128)</span><span class="sxs-lookup"><span data-stu-id="e671e-387">4392 (0x1128)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-388">Die im Analyse Punkt Puffer vorhandenen Daten sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="e671e-388">The data present in the reparse point buffer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-389"><span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**Fehleranalyse- \_ \_ Tag ist \_ ungültig.**</span><span class="sxs-lookup"><span data-stu-id="e671e-389"><span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**ERROR\_REPARSE\_TAG\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-390">4393 (0x1129)</span><span class="sxs-lookup"><span data-stu-id="e671e-390">4393 (0x1129)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-391">Das im Analyse Punkt Puffer vorhandene Tag ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e671e-391">The tag present in the reparse point buffer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-392"><span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**Fehler beim Analysieren der \_ \_ tagnicht \_ Übereinstimmung.**</span><span class="sxs-lookup"><span data-stu-id="e671e-392"><span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**ERROR\_REPARSE\_TAG\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-393">4394 (0x112a)</span><span class="sxs-lookup"><span data-stu-id="e671e-393">4394 (0x112A)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-394">Es gibt einen Konflikt zwischen dem in der Anforderung angegebenen Tag und dem Tag, das im Analyse Punkt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-394">There is a mismatch between the tag specified in the request and the tag present in the reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-395"><span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**Fehler- \_ App- \_ Daten \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-395"><span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**ERROR\_APP\_DATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-396">4400 (0x1130)</span><span class="sxs-lookup"><span data-stu-id="e671e-396">4400 (0x1130)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-397">Es wurden keine schnellen Cache Daten gefunden.</span><span class="sxs-lookup"><span data-stu-id="e671e-397">Fast Cache data not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-398"><span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**Fehler- \_ App- \_ Daten \_ abgelaufen**</span><span class="sxs-lookup"><span data-stu-id="e671e-398"><span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**ERROR\_APP\_DATA\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-399">4401 (0x1131)</span><span class="sxs-lookup"><span data-stu-id="e671e-399">4401 (0x1131)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-400">Schnelle Cache Daten sind abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="e671e-400">Fast Cache data expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-401"><span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**Fehler- \_ App- \_ Daten \_ beschädigt**</span><span class="sxs-lookup"><span data-stu-id="e671e-401"><span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**ERROR\_APP\_DATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-402">4402 (0x1132)</span><span class="sxs-lookup"><span data-stu-id="e671e-402">4402 (0x1132)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-403">Schnelle Cache Daten sind beschädigt.</span><span class="sxs-lookup"><span data-stu-id="e671e-403">Fast Cache data corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-404"><span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**Fehler bei \_ App- \_ Daten \_ Limit \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="e671e-404"><span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**ERROR\_APP\_DATA\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-405">4403 (0x1133)</span><span class="sxs-lookup"><span data-stu-id="e671e-405">4403 (0x1133)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-406">Schnelle Cache Daten haben die maximale Größe überschritten und können nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-406">Fast Cache data has exceeded its max size and cannot be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-407"><span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**Fehler bei \_ App- \_ Daten \_ Neustart \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="e671e-407"><span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**ERROR\_APP\_DATA\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-408">4404 (0x1134)</span><span class="sxs-lookup"><span data-stu-id="e671e-408">4404 (0x1134)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-409">Der schnelle Cache wurde zurückgesetzt und erfordert einen Neustart, bis er aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e671e-409">Fast Cache has been ReArmed and requires a reboot until it can be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-410"><span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**Fehler \_ secureboot- \_ Rollback \_ erkannt**</span><span class="sxs-lookup"><span data-stu-id="e671e-410"><span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**ERROR\_SECUREBOOT\_ROLLBACK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-411">4420 (0x1144)</span><span class="sxs-lookup"><span data-stu-id="e671e-411">4420 (0x1144)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-412">Der sichere Start hat festgestellt, dass ein Rollback geschützter Daten versucht wurde.</span><span class="sxs-lookup"><span data-stu-id="e671e-412">Secure Boot detected that rollback of protected data has been attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-413"><span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**Fehler beim \_ secureboot- \_ Richtlinien \_ Verstoß.**</span><span class="sxs-lookup"><span data-stu-id="e671e-413"><span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**ERROR\_SECUREBOOT\_POLICY\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-414">4421 (0x1145)</span><span class="sxs-lookup"><span data-stu-id="e671e-414">4421 (0x1145)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-415">Der Wert wird durch eine Richtlinie für den sicheren Start geschützt und kann nicht geändert oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-415">The value is protected by Secure Boot policy and cannot be modified or deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-416"><span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**Fehlermeldung \_ secureboot \_ ungültige \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="e671e-416"><span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**ERROR\_SECUREBOOT\_INVALID\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-417">4422 (0x1146)</span><span class="sxs-lookup"><span data-stu-id="e671e-417">4422 (0x1146)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-418">Die Richtlinie für den sicheren Start ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e671e-418">The Secure Boot policy is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-419"><span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**Fehler \_ secureboot- \_ Richtlinien- \_ Verleger \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="e671e-419"><span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**ERROR\_SECUREBOOT\_POLICY\_PUBLISHER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-420">4423 (0x1147)</span><span class="sxs-lookup"><span data-stu-id="e671e-420">4423 (0x1147)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-421">Eine neue Richtlinie für den sicheren Start enthielt nicht den aktuellen Verleger in der Update Liste.</span><span class="sxs-lookup"><span data-stu-id="e671e-421">A new Secure Boot policy did not contain the current publisher on its update list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-422"><span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**Fehler \_ secureboot- \_ Richtlinie \_ nicht \_ signiert**</span><span class="sxs-lookup"><span data-stu-id="e671e-422"><span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**ERROR\_SECUREBOOT\_POLICY\_NOT\_SIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-423">4424 (0x1148)</span><span class="sxs-lookup"><span data-stu-id="e671e-423">4424 (0x1148)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-424">Die Richtlinie für den sicheren Start ist entweder nicht signiert oder wird von einem nicht vertrauenswürdigen Signatur Geber signiert.</span><span class="sxs-lookup"><span data-stu-id="e671e-424">The Secure Boot policy is either not signed or is signed by a non-trusted signer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-425"><span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**Fehler \_ secureboot ist \_ nicht \_ aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="e671e-425"><span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**ERROR\_SECUREBOOT\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-426">4425 (0x1149)</span><span class="sxs-lookup"><span data-stu-id="e671e-426">4425 (0x1149)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-427">Der sichere Start ist auf diesem Computer nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e671e-427">Secure Boot is not enabled on this machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-428"><span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**Fehler \_ secureboot- \_ Datei wurde \_ ersetzt**</span><span class="sxs-lookup"><span data-stu-id="e671e-428"><span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**ERROR\_SECUREBOOT\_FILE\_REPLACED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-429">4426 (0x114 a)</span><span class="sxs-lookup"><span data-stu-id="e671e-429">4426 (0x114A)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-430">Der sichere Start erfordert, dass bestimmte Dateien und Treiber nicht durch andere Dateien oder Treiber ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-430">Secure Boot requires that certain files and drivers are not replaced by other files or drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-431"><span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**Fehler beim \_ \_ auslagern, lesen, \_ \_ nicht \_ unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="e671e-431"><span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**ERROR\_OFFLOAD\_READ\_FLT\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-432">4440 (0x1158)</span><span class="sxs-lookup"><span data-stu-id="e671e-432">4440 (0x1158)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-433">Der Lesevorgang zum Kopieren auslagern wird von einem Filter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e671e-433">The copy offload read operation is not supported by a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-434"><span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**Fehler beim auslagern, \_ \_ \_ \_ nicht \_ unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="e671e-434"><span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**ERROR\_OFFLOAD\_WRITE\_FLT\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-435">4441 (0x1159)</span><span class="sxs-lookup"><span data-stu-id="e671e-435">4441 (0x1159)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-436">Der Kopiervorgang zum Kopieren auslagern wird von einem Filter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e671e-436">The copy offload write operation is not supported by a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-437"><span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**Fehler beim \_ \_ Auslagern der Lese \_ Datei \_ nicht \_ unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="e671e-437"><span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**ERROR\_OFFLOAD\_READ\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-438">4442 (0x115a)</span><span class="sxs-lookup"><span data-stu-id="e671e-438">4442 (0x115A)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-439">Der Lesevorgang zum Kopieren auslagern wird für die Datei nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e671e-439">The copy offload read operation is not supported for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-440"><span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**Fehler beim auslagern der \_ \_ Schreib \_ Datei \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="e671e-440"><span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**ERROR\_OFFLOAD\_WRITE\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-441">4443 (0x115b)</span><span class="sxs-lookup"><span data-stu-id="e671e-441">4443 (0x115B)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-442">Der Kopiervorgang zum Kopieren auslagern wird für die Datei nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e671e-442">The copy offload write operation is not supported for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-443"><span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**Fehler \_ Volume \_ nicht \_ SIS \_ aktiviert**</span><span class="sxs-lookup"><span data-stu-id="e671e-443"><span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**ERROR\_VOLUME\_NOT\_SIS\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-444">4500 (0x1194)</span><span class="sxs-lookup"><span data-stu-id="e671e-444">4500 (0x1194)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-445">Der Einzelinstanzspeicher ist auf diesem Volume nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e671e-445">Single Instance Storage is not available on this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-446"><span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**Fehler \_ abhängige \_ Ressource ist \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-446"><span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**ERROR\_DEPENDENT\_RESOURCE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-447">5001 (0x1389)</span><span class="sxs-lookup"><span data-stu-id="e671e-447">5001 (0x1389)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-448">Der Vorgang kann nicht abgeschlossen werden, da andere Ressourcen von dieser Ressource abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="e671e-448">The operation cannot be completed because other resources are dependent on this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-449"><span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**Fehler \_ Abhängigkeit wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-449"><span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**ERROR\_DEPENDENCY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-450">5002 (0x138a)</span><span class="sxs-lookup"><span data-stu-id="e671e-450">5002 (0x138A)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-451">Die Abhängigkeit der Cluster Ressource wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e671e-451">The cluster resource dependency cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-452"><span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**die Fehler \_ Abhängigkeit ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-452"><span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**ERROR\_DEPENDENCY\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-453">5003 (0x138b)</span><span class="sxs-lookup"><span data-stu-id="e671e-453">5003 (0x138B)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-454">Die Cluster Ressource kann nicht von der angegebenen Ressource abhängig gemacht werden, da Sie bereits abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-454">The cluster resource cannot be made dependent on the specified resource because it is already dependent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-455"><span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**Fehler \_ Ressource \_ nicht \_ Online**</span><span class="sxs-lookup"><span data-stu-id="e671e-455"><span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**ERROR\_RESOURCE\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-456">5004 (0x138c)</span><span class="sxs-lookup"><span data-stu-id="e671e-456">5004 (0x138C)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-457">Die Cluster Ressource ist nicht online.</span><span class="sxs-lookup"><span data-stu-id="e671e-457">The cluster resource is not online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-458"><span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**der Fehler \_ Host \_ Knoten ist \_ nicht \_ verfügbar.**</span><span class="sxs-lookup"><span data-stu-id="e671e-458"><span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**ERROR\_HOST\_NODE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-459">5005 (0x138d)</span><span class="sxs-lookup"><span data-stu-id="e671e-459">5005 (0x138D)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-460">Für diesen Vorgang ist kein Cluster Knoten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e671e-460">A cluster node is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-461"><span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**Fehler \_ Ressource \_ nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="e671e-461"><span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**ERROR\_RESOURCE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-462">5006 (0x138e)</span><span class="sxs-lookup"><span data-stu-id="e671e-462">5006 (0x138E)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-463">Die Cluster Ressource ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e671e-463">The cluster resource is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-464"><span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**Fehler \_ Ressource \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-464"><span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**ERROR\_RESOURCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-465">5007 (0x138f)</span><span class="sxs-lookup"><span data-stu-id="e671e-465">5007 (0x138F)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-466">Die Cluster Ressource wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e671e-466">The cluster resource could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-467"><span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**Fehler beim Beenden des \_ \_ Clusters**</span><span class="sxs-lookup"><span data-stu-id="e671e-467"><span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**ERROR\_SHUTDOWN\_CLUSTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-468">5008 (0x1390)</span><span class="sxs-lookup"><span data-stu-id="e671e-468">5008 (0x1390)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-469">Der Cluster wird heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="e671e-469">The cluster is being shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-470"><span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**Fehler beim Entfernen des \_ \_ \_ aktiven \_ Knotens.**</span><span class="sxs-lookup"><span data-stu-id="e671e-470"><span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**ERROR\_CANT\_EVICT\_ACTIVE\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-471">5009 (0x1391)</span><span class="sxs-lookup"><span data-stu-id="e671e-471">5009 (0x1391)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-472">Ein Cluster Knoten kann nicht aus dem Cluster entfernt werden, es sei denn, der Knoten ist herunter oder der letzte Knoten.</span><span class="sxs-lookup"><span data-stu-id="e671e-472">A cluster node cannot be evicted from the cluster unless the node is down or it is the last node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-473"><span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**das Fehler \_ Objekt ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-473"><span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**ERROR\_OBJECT\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-474">5010 (0x1392)</span><span class="sxs-lookup"><span data-stu-id="e671e-474">5010 (0x1392)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-475">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e671e-475">The object already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-476"><span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**Fehler \_ Objekt \_ in \_ Liste**</span><span class="sxs-lookup"><span data-stu-id="e671e-476"><span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**ERROR\_OBJECT\_IN\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-477">5011 (0x1393)</span><span class="sxs-lookup"><span data-stu-id="e671e-477">5011 (0x1393)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-478">Das Objekt ist bereits in der Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="e671e-478">The object is already in the list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-479"><span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**Fehler \_ Gruppe \_ nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="e671e-479"><span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**ERROR\_GROUP\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-480">5012 (0x1394)</span><span class="sxs-lookup"><span data-stu-id="e671e-480">5012 (0x1394)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-481">Die Clustergruppe ist für keine neuen Anforderungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e671e-481">The cluster group is not available for any new requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-482"><span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**Fehler \_ Gruppe \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-482"><span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**ERROR\_GROUP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-483">5013 (0x1395)</span><span class="sxs-lookup"><span data-stu-id="e671e-483">5013 (0x1395)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-484">Die Clustergruppe konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-484">The cluster group could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-485"><span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**die Fehler \_ Gruppe ist \_ nicht \_ Online.**</span><span class="sxs-lookup"><span data-stu-id="e671e-485"><span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**ERROR\_GROUP\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-486">5014 (0x1396)</span><span class="sxs-lookup"><span data-stu-id="e671e-486">5014 (0x1396)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-487">Der Vorgang konnte nicht abgeschlossen werden, da die Clustergruppe nicht online ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-487">The operation could not be completed because the cluster group is not online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-488"><span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**Fehler \_ Host \_ Knoten \_ nicht \_ Ressourcen \_ Besitzer**</span><span class="sxs-lookup"><span data-stu-id="e671e-488"><span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**ERROR\_HOST\_NODE\_NOT\_RESOURCE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-489">5015 (0x1397)</span><span class="sxs-lookup"><span data-stu-id="e671e-489">5015 (0x1397)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-490">Der Vorgang ist fehlgeschlagen, da entweder der angegebene Cluster Knoten nicht der Besitzer der Ressource ist oder der Knoten kein möglicher Besitzer der Ressource ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-490">The operation failed because either the specified cluster node is not the owner of the resource, or the node is not a possible owner of the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-491"><span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**Fehler \_ Host \_ Knoten, \_ nicht \_ Gruppen \_ Besitzer**</span><span class="sxs-lookup"><span data-stu-id="e671e-491"><span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**ERROR\_HOST\_NODE\_NOT\_GROUP\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-492">5016 (0x1398)</span><span class="sxs-lookup"><span data-stu-id="e671e-492">5016 (0x1398)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-493">Der Vorgang ist fehlgeschlagen, da entweder der angegebene Clusterknoten nicht Besitzer der Gruppe ist, oder der Knoten kein möglicher Besitzer der Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-493">The operation failed because either the specified cluster node is not the owner of the group, or the node is not a possible owner of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-494"><span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**Fehler \_ beim Erstellen des Fehlers. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-494"><span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**ERROR\_RESMON\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-495">5017 (0x1399)</span><span class="sxs-lookup"><span data-stu-id="e671e-495">5017 (0x1399)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-496">Die Cluster Ressource konnte im angegebenen Ressourcen Monitor nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-496">The cluster resource could not be created in the specified resource monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-497"><span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**Fehler \_ bei der \_ Online Fehlermeldung. \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-497"><span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**ERROR\_RESMON\_ONLINE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-498">5018 (0x139 a)</span><span class="sxs-lookup"><span data-stu-id="e671e-498">5018 (0x139A)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-499">Die Cluster Ressource konnte nicht vom Ressourcen Monitor online geschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-499">The cluster resource could not be brought online by the resource monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-500"><span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**Fehler \_ Ressource \_ Online**</span><span class="sxs-lookup"><span data-stu-id="e671e-500"><span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**ERROR\_RESOURCE\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-501">5019 (0x139 b)</span><span class="sxs-lookup"><span data-stu-id="e671e-501">5019 (0x139B)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-502">Der Vorgang konnte nicht abgeschlossen werden, da die Cluster Ressource online ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-502">The operation could not be completed because the cluster resource is online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-503"><span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**Fehler \_ Quorum \_ Ressource**</span><span class="sxs-lookup"><span data-stu-id="e671e-503"><span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**ERROR\_QUORUM\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-504">5020 (0x139 c)</span><span class="sxs-lookup"><span data-stu-id="e671e-504">5020 (0x139C)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-505">Die Cluster Ressource konnte nicht gelöscht oder offline geschaltet werden, da es sich um die Quorum Ressource handelt.</span><span class="sxs-lookup"><span data-stu-id="e671e-505">The cluster resource could not be deleted or brought offline because it is the quorum resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-506"><span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**Fehler \_ nicht \_ Quorum \_ fähig**</span><span class="sxs-lookup"><span data-stu-id="e671e-506"><span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**ERROR\_NOT\_QUORUM\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-507">5021 (0x139 d)</span><span class="sxs-lookup"><span data-stu-id="e671e-507">5021 (0x139D)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-508">Der Cluster konnte die angegebene Ressource nicht zu einer Quorum Ressource machen, da Sie keine Quorum Ressource sein kann.</span><span class="sxs-lookup"><span data-stu-id="e671e-508">The cluster could not make the specified resource a quorum resource because it is not capable of being a quorum resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-509"><span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**Fehler beim Herunterfahren des \_ Clusters \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-509"><span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**ERROR\_CLUSTER\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-510">5022 (0x139 e)</span><span class="sxs-lookup"><span data-stu-id="e671e-510">5022 (0x139E)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-511">Die Cluster Software wird heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="e671e-511">The cluster software is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-512"><span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**Fehler bei \_ ungültigem \_ Status**</span><span class="sxs-lookup"><span data-stu-id="e671e-512"><span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**ERROR\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-513">5023 (0x139 f)</span><span class="sxs-lookup"><span data-stu-id="e671e-513">5023 (0x139F)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-514">Die Gruppe oder Ressource weist nicht den richtigen Status auf, um den angeforderten Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e671e-514">The group or resource is not in the correct state to perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-515"><span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**\_gespeicherte Fehler Ressourcen \_ Eigenschaften \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-515"><span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**ERROR\_RESOURCE\_PROPERTIES\_STORED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-516">5024 (0x13a0)</span><span class="sxs-lookup"><span data-stu-id="e671e-516">5024 (0x13A0)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-517">Die Eigenschaften wurden gespeichert, aber nicht alle Änderungen werden wirksam, bis die Ressource das nächste Mal online geschaltet wird.</span><span class="sxs-lookup"><span data-stu-id="e671e-517">The properties were stored but not all changes will take effect until the next time the resource is brought online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-518"><span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**Fehler \_ nicht \_ Quorum \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="e671e-518"><span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**ERROR\_NOT\_QUORUM\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-519">5025 (0x13a1)</span><span class="sxs-lookup"><span data-stu-id="e671e-519">5025 (0x13A1)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-520">Der Cluster konnte die angegebene Ressource nicht zu einer Quorum Ressource machen, da Sie nicht zu einer freigegebenen Speicher Klasse gehört.</span><span class="sxs-lookup"><span data-stu-id="e671e-520">The cluster could not make the specified resource a quorum resource because it does not belong to a shared storage class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-521"><span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**Fehler \_ Kern \_ Ressource**</span><span class="sxs-lookup"><span data-stu-id="e671e-521"><span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**ERROR\_CORE\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-522">5026 (0x13a2)</span><span class="sxs-lookup"><span data-stu-id="e671e-522">5026 (0x13A2)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-523">Die Cluster Ressource konnte nicht gelöscht werden, da es sich um eine Kernressource handelt.</span><span class="sxs-lookup"><span data-stu-id="e671e-523">The cluster resource could not be deleted since it is a core resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-524"><span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**Fehler \_ Quorum \_ Ressource \_ Online \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-524"><span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**ERROR\_QUORUM\_RESOURCE\_ONLINE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-525">5027 (0x13a3)</span><span class="sxs-lookup"><span data-stu-id="e671e-525">5027 (0x13A3)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-526">Die Quorum Ressource konnte nicht online geschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-526">The quorum resource failed to come online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-527"><span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**Fehler beim \_ Öffnen von " \_ quortolog". \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-527"><span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**ERROR\_QUORUMLOG\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-528">5028 (0x13a4)</span><span class="sxs-lookup"><span data-stu-id="e671e-528">5028 (0x13A4)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-529">Das Quorum Protokoll konnte nicht erstellt oder bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-529">The quorum log could not be created or mounted successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-530"><span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**Fehler \_ Cluster Protokoll \_ beschädigt**</span><span class="sxs-lookup"><span data-stu-id="e671e-530"><span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**ERROR\_CLUSTERLOG\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-531">5029 (0x13a5)</span><span class="sxs-lookup"><span data-stu-id="e671e-531">5029 (0x13A5)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-532">Das Cluster Protokoll ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="e671e-532">The cluster log is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-533"><span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**Fehler \_ CLUSTERLOG- \_ Datensatz über \_ schreitet \_ MaxSize**</span><span class="sxs-lookup"><span data-stu-id="e671e-533"><span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**ERROR\_CLUSTERLOG\_RECORD\_EXCEEDS\_MAXSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-534">5030 (0x13a6)</span><span class="sxs-lookup"><span data-stu-id="e671e-534">5030 (0x13A6)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-535">Der Datensatz konnte nicht in das Cluster Protokoll geschrieben werden, da er die maximale Größe überschreitet.</span><span class="sxs-lookup"><span data-stu-id="e671e-535">The record could not be written to the cluster log since it exceeds the maximum size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-536"><span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**Fehler \_ Cluster Protokoll über \_ schreitet \_ MaxSize**</span><span class="sxs-lookup"><span data-stu-id="e671e-536"><span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**ERROR\_CLUSTERLOG\_EXCEEDS\_MAXSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-537">5031 (0x13a7)</span><span class="sxs-lookup"><span data-stu-id="e671e-537">5031 (0x13A7)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-538">Das Cluster Protokoll überschreitet die maximale Größe.</span><span class="sxs-lookup"><span data-stu-id="e671e-538">The cluster log exceeds its maximum size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-539"><span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**Fehler beim \_ CLUSTERLOG- \_ chkpoint \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-539"><span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**ERROR\_CLUSTERLOG\_CHKPOINT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-540">5032 (0x13a8)</span><span class="sxs-lookup"><span data-stu-id="e671e-540">5032 (0x13A8)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-541">Es wurde kein Prüf Punktdaten Satz im Cluster Protokoll gefunden.</span><span class="sxs-lookup"><span data-stu-id="e671e-541">No checkpoint record was found in the cluster log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-542"><span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**Fehler beim \_ CLUSTERLOG \_ nicht \_ genügend \_ Speicherplatz.**</span><span class="sxs-lookup"><span data-stu-id="e671e-542"><span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**ERROR\_CLUSTERLOG\_NOT\_ENOUGH\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-543">5033 (0x13a9)</span><span class="sxs-lookup"><span data-stu-id="e671e-543">5033 (0x13A9)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-544">Der mindestens erforderliche Speicherplatz für die Protokollierung ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e671e-544">The minimum required disk space needed for logging is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-545"><span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**Fehler \_ Quorum \_ Besitzer \_ Alive**</span><span class="sxs-lookup"><span data-stu-id="e671e-545"><span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**ERROR\_QUORUM\_OWNER\_ALIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-546">5034 (0x13aa)</span><span class="sxs-lookup"><span data-stu-id="e671e-546">5034 (0x13AA)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-547">Der Cluster Knoten konnte die Quorum Ressource nicht steuern, da die Ressource im Besitz eines anderen aktiven Knotens ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-547">The cluster node failed to take control of the quorum resource because the resource is owned by another active node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-548"><span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**Fehler \_ Netzwerk \_ nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="e671e-548"><span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**ERROR\_NETWORK\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-549">5035 (0x13ab)</span><span class="sxs-lookup"><span data-stu-id="e671e-549">5035 (0x13AB)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-550">Ein Cluster Netzwerk ist für diesen Vorgang nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e671e-550">A cluster network is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-551"><span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**der Fehler \_ Knoten ist \_ nicht \_ verfügbar.**</span><span class="sxs-lookup"><span data-stu-id="e671e-551"><span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**ERROR\_NODE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-552">5036 (0x13ac)</span><span class="sxs-lookup"><span data-stu-id="e671e-552">5036 (0x13AC)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-553">Für diesen Vorgang ist kein Cluster Knoten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e671e-553">A cluster node is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-554"><span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**Fehler \_ alle \_ Knoten \_ nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="e671e-554"><span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**ERROR\_ALL\_NODES\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-555">5037 (0x13ad)</span><span class="sxs-lookup"><span data-stu-id="e671e-555">5037 (0x13AD)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-556">Alle Cluster Knoten müssen ausgeführt werden, um diesen Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e671e-556">All cluster nodes must be running to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-557"><span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**Fehler bei \_ Ressource. \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-557"><span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**ERROR\_RESOURCE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-558">5038 (0x13ae)</span><span class="sxs-lookup"><span data-stu-id="e671e-558">5038 (0x13AE)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-559">Fehler in einer Clusterressource.</span><span class="sxs-lookup"><span data-stu-id="e671e-559">A cluster resource failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-560"><span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**\_ \_ Ungültiger Knoten beim Fehler Cluster. \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-560"><span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**ERROR\_CLUSTER\_INVALID\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-561">5039 (0x13af)</span><span class="sxs-lookup"><span data-stu-id="e671e-561">5039 (0x13AF)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-562">Der Cluster Knoten ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e671e-562">The cluster node is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-563"><span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**Fehler \_ Cluster \_ Knoten \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="e671e-563"><span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**ERROR\_CLUSTER\_NODE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-564">5040 (0x13b0)</span><span class="sxs-lookup"><span data-stu-id="e671e-564">5040 (0x13B0)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-565">Der Cluster Knoten ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e671e-565">The cluster node already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-566"><span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**Fehler \_ \_ beim Cluster \_ Beitritt \_ .**</span><span class="sxs-lookup"><span data-stu-id="e671e-566"><span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**ERROR\_CLUSTER\_JOIN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-567">5041 (0x13b1)</span><span class="sxs-lookup"><span data-stu-id="e671e-567">5041 (0x13B1)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-568">Ein Knoten wird gerade dem Cluster beitreten.</span><span class="sxs-lookup"><span data-stu-id="e671e-568">A node is in the process of joining the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-569"><span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**Fehler \_ Cluster \_ Knoten wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-569"><span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**ERROR\_CLUSTER\_NODE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-570">5042 (0x13b2)</span><span class="sxs-lookup"><span data-stu-id="e671e-570">5042 (0x13B2)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-571">Der Cluster Knoten wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e671e-571">The cluster node was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-572"><span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**der \_ lokale Knoten des Fehler Clusters wurde \_ \_ \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-572"><span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**ERROR\_CLUSTER\_LOCAL\_NODE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-573">5043 (0x13b3)</span><span class="sxs-lookup"><span data-stu-id="e671e-573">5043 (0x13B3)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-574">Die Informationen zum lokalen Cluster Knoten wurden nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e671e-574">The cluster local node information was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-575"><span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**Fehler \_ Cluster \_ Netzwerk \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="e671e-575"><span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**ERROR\_CLUSTER\_NETWORK\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-576">5044 (0x13b4)</span><span class="sxs-lookup"><span data-stu-id="e671e-576">5044 (0x13B4)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-577">Das Cluster Netzwerk ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e671e-577">The cluster network already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-578"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**Fehler \_ Cluster \_ Netzwerk \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-578"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-579">5045 (0x13b5)</span><span class="sxs-lookup"><span data-stu-id="e671e-579">5045 (0x13B5)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-580">Das Cluster Netzwerk wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e671e-580">The cluster network was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-581"><span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**Fehler \_ Cluster- \_ netinterface \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="e671e-581"><span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**ERROR\_CLUSTER\_NETINTERFACE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-582">5046 (0x13b6)</span><span class="sxs-lookup"><span data-stu-id="e671e-582">5046 (0x13B6)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-583">Die Cluster Netzwerkschnittstelle ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e671e-583">The cluster network interface already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-584"><span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**Fehler \_ Cluster- \_ netinterface \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-584"><span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**ERROR\_CLUSTER\_NETINTERFACE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-585">5047 (0x13b7)</span><span class="sxs-lookup"><span data-stu-id="e671e-585">5047 (0x13B7)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-586">Die Cluster Netzwerkschnittstelle wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e671e-586">The cluster network interface was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-587"><span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**\_ \_ ungültige Anforderung für Fehler Cluster. \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-587"><span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**ERROR\_CLUSTER\_INVALID\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-588">5048 (0x13b8)</span><span class="sxs-lookup"><span data-stu-id="e671e-588">5048 (0x13B8)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-589">Die Cluster Anforderung ist für dieses Objekt ungültig.</span><span class="sxs-lookup"><span data-stu-id="e671e-589">The cluster request is not valid for this object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-590"><span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**Fehler \_ Cluster bei \_ ungültigem \_ Netzwerk \_ Anbieter.**</span><span class="sxs-lookup"><span data-stu-id="e671e-590"><span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**ERROR\_CLUSTER\_INVALID\_NETWORK\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-591">5049 (0x13b9)</span><span class="sxs-lookup"><span data-stu-id="e671e-591">5049 (0x13B9)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-592">Der Cluster Netzwerkanbieter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e671e-592">The cluster network provider is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-593"><span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**Fehler \_ Cluster \_ Knoten \_ nach unten**</span><span class="sxs-lookup"><span data-stu-id="e671e-593"><span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**ERROR\_CLUSTER\_NODE\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-594">5050 (0x13ba)</span><span class="sxs-lookup"><span data-stu-id="e671e-594">5050 (0x13BA)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-595">Der Cluster Knoten ist nicht mehr festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e671e-595">The cluster node is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-596"><span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**Fehler \_ Cluster \_ Knoten \_ nicht erreichbar**</span><span class="sxs-lookup"><span data-stu-id="e671e-596"><span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**ERROR\_CLUSTER\_NODE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-597">5051 (0x13bb)</span><span class="sxs-lookup"><span data-stu-id="e671e-597">5051 (0x13BB)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-598">Der Cluster Knoten ist nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="e671e-598">The cluster node is not reachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-599"><span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**Fehler \_ Cluster \_ Knoten ist \_ nicht \_ Mitglied**</span><span class="sxs-lookup"><span data-stu-id="e671e-599"><span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**ERROR\_CLUSTER\_NODE\_NOT\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-600">5052 (0x13bc)</span><span class="sxs-lookup"><span data-stu-id="e671e-600">5052 (0x13BC)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-601">Der Cluster Knoten ist kein Mitglied des Clusters.</span><span class="sxs-lookup"><span data-stu-id="e671e-601">The cluster node is not a member of the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-602"><span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**Fehler \_ \_ beim Cluster \_ Beitritt \_ nicht \_ .**</span><span class="sxs-lookup"><span data-stu-id="e671e-602"><span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**ERROR\_CLUSTER\_JOIN\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-603">5053 (0x13bd)</span><span class="sxs-lookup"><span data-stu-id="e671e-603">5053 (0x13BD)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-604">Ein clusterjoinvorgang wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e671e-604">A cluster join operation is not in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-605"><span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**\_ \_ Ungültiges Netzwerk für Fehler Cluster. \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-605"><span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**ERROR\_CLUSTER\_INVALID\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-606">5054 (0x13be)</span><span class="sxs-lookup"><span data-stu-id="e671e-606">5054 (0x13BE)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-607">Das Cluster Netzwerk ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e671e-607">The cluster network is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-608"><span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**Fehler \_ Cluster \_ Knoten \_ hoch**</span><span class="sxs-lookup"><span data-stu-id="e671e-608"><span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**ERROR\_CLUSTER\_NODE\_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-609">5056 (0x13c0)</span><span class="sxs-lookup"><span data-stu-id="e671e-609">5056 (0x13C0)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-610">Der Cluster Knoten ist aktiv.</span><span class="sxs-lookup"><span data-stu-id="e671e-610">The cluster node is up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-611"><span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**Fehler \_ Cluster " \_ ipaddr" wird \_ \_ verwendet.**</span><span class="sxs-lookup"><span data-stu-id="e671e-611"><span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**ERROR\_CLUSTER\_IPADDR\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-612">5057 (0x13c1)</span><span class="sxs-lookup"><span data-stu-id="e671e-612">5057 (0x13C1)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-613">Die Cluster-IP-Adresse wird bereits verwendet.</span><span class="sxs-lookup"><span data-stu-id="e671e-613">The cluster IP address is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-614"><span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**Fehler \_ Cluster \_ Knoten wurde \_ nicht \_ angehalten.**</span><span class="sxs-lookup"><span data-stu-id="e671e-614"><span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**ERROR\_CLUSTER\_NODE\_NOT\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-615">5058 (0x13c2)</span><span class="sxs-lookup"><span data-stu-id="e671e-615">5058 (0x13C2)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-616">Der Cluster Knoten wurde nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="e671e-616">The cluster node is not paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-617"><span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**Fehler \_ Cluster \_ ohne \_ Sicherheits \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="e671e-617"><span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**ERROR\_CLUSTER\_NO\_SECURITY\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-618">5059 (0x13c3)</span><span class="sxs-lookup"><span data-stu-id="e671e-618">5059 (0x13C3)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-619">Es ist kein Cluster Sicherheitskontext verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e671e-619">No cluster security context is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-620"><span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**Fehler \_ Cluster \_ Netzwerk \_ nicht \_ intern**</span><span class="sxs-lookup"><span data-stu-id="e671e-620"><span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-621">5060 (0x13c4)</span><span class="sxs-lookup"><span data-stu-id="e671e-621">5060 (0x13C4)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-622">Das Cluster Netzwerk ist nicht für die interne Cluster Kommunikation konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="e671e-622">The cluster network is not configured for internal cluster communication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-623"><span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**Fehler \_ Cluster \_ Knoten ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-623"><span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-624">5061 (0x13c5)</span><span class="sxs-lookup"><span data-stu-id="e671e-624">5061 (0x13C5)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-625">Der Cluster Knoten ist bereits aktiv.</span><span class="sxs-lookup"><span data-stu-id="e671e-625">The cluster node is already up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-626"><span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**Fehler \_ Cluster \_ Knoten ist \_ bereits \_ herunter**</span><span class="sxs-lookup"><span data-stu-id="e671e-626"><span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-627">5062 (0x13c6)</span><span class="sxs-lookup"><span data-stu-id="e671e-627">5062 (0x13C6)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-628">Der Cluster Knoten ist bereits herunter.</span><span class="sxs-lookup"><span data-stu-id="e671e-628">The cluster node is already down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-629"><span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**Fehler \_ Cluster \_ Netzwerk ist \_ bereits \_ Online.**</span><span class="sxs-lookup"><span data-stu-id="e671e-629"><span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**ERROR\_CLUSTER\_NETWORK\_ALREADY\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-630">5063 (0x13c7)</span><span class="sxs-lookup"><span data-stu-id="e671e-630">5063 (0x13C7)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-631">Das Cluster Netzwerk ist bereits online.</span><span class="sxs-lookup"><span data-stu-id="e671e-631">The cluster network is already online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-632"><span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**Fehler \_ Cluster \_ Netzwerk ist \_ bereits \_ Offline.**</span><span class="sxs-lookup"><span data-stu-id="e671e-632"><span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**ERROR\_CLUSTER\_NETWORK\_ALREADY\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-633">5064 (0x13c8)</span><span class="sxs-lookup"><span data-stu-id="e671e-633">5064 (0x13C8)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-634">Das Cluster Netzwerk ist bereits offline.</span><span class="sxs-lookup"><span data-stu-id="e671e-634">The cluster network is already offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-635"><span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**Fehler \_ Cluster \_ Knoten ist \_ bereits \_ Mitglied**</span><span class="sxs-lookup"><span data-stu-id="e671e-635"><span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-636">5065 (0x13c9)</span><span class="sxs-lookup"><span data-stu-id="e671e-636">5065 (0x13C9)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-637">Der Cluster Knoten ist bereits Mitglied des Clusters.</span><span class="sxs-lookup"><span data-stu-id="e671e-637">The cluster node is already a member of the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-638"><span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**\_ \_ Letztes \_ internes \_ Netzwerk des Fehler Clusters**</span><span class="sxs-lookup"><span data-stu-id="e671e-638"><span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**ERROR\_CLUSTER\_LAST\_INTERNAL\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-639">5066 (0x13ca)</span><span class="sxs-lookup"><span data-stu-id="e671e-639">5066 (0x13CA)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-640">Das Cluster Netzwerk ist das einzige, das für die interne Cluster Kommunikation zwischen mindestens zwei aktiven Cluster Knoten konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-640">The cluster network is the only one configured for internal cluster communication between two or more active cluster nodes.</span></span> <span data-ttu-id="e671e-641">Die interne Kommunikationsfunktion kann nicht aus dem Netzwerk entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-641">The internal communication capability cannot be removed from the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-642"><span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**Fehler \_ Cluster \_ Netzwerk \_ hat \_ abhängige Elemente**</span><span class="sxs-lookup"><span data-stu-id="e671e-642"><span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**ERROR\_CLUSTER\_NETWORK\_HAS\_DEPENDENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-643">5067 (0x13cb)</span><span class="sxs-lookup"><span data-stu-id="e671e-643">5067 (0x13CB)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-644">Mindestens eine Cluster Ressource ist vom Netzwerk abhängig, um Dienste für Clients bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e671e-644">One or more cluster resources depend on the network to provide service to clients.</span></span> <span data-ttu-id="e671e-645">Die Client Zugriffs Funktion kann nicht aus dem Netzwerk entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-645">The client access capability cannot be removed from the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-646"><span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**Fehler \_ bei ungültigem \_ Vorgang \_ für \_ Quorum.**</span><span class="sxs-lookup"><span data-stu-id="e671e-646"><span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**ERROR\_INVALID\_OPERATION\_ON\_QUORUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-647">5068 (0x13cc)</span><span class="sxs-lookup"><span data-stu-id="e671e-647">5068 (0x13CC)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-648">Dieser Vorgang kann für die Cluster Ressource nicht ausgeführt werden, da es sich um die Quorum Ressource handelt.</span><span class="sxs-lookup"><span data-stu-id="e671e-648">This operation cannot be performed on the cluster resource as it the quorum resource.</span></span> <span data-ttu-id="e671e-649">Sie dürfen die Quorum Ressource nicht offline schalten oder die Liste möglicher Besitzer ändern.</span><span class="sxs-lookup"><span data-stu-id="e671e-649">You may not bring the quorum resource offline or modify its possible owners list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-650"><span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**die Fehler \_ Abhängigkeit ist \_ nicht \_ zulässig.**</span><span class="sxs-lookup"><span data-stu-id="e671e-650"><span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**ERROR\_DEPENDENCY\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-651">5069 (0x13cd)</span><span class="sxs-lookup"><span data-stu-id="e671e-651">5069 (0x13CD)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-652">Für die Cluster Quorum Ressource sind keine Abhängigkeiten zulässig.</span><span class="sxs-lookup"><span data-stu-id="e671e-652">The cluster quorum resource is not allowed to have any dependencies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-653"><span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**Fehler \_ Cluster \_ Knoten \_ angehalten**</span><span class="sxs-lookup"><span data-stu-id="e671e-653"><span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**ERROR\_CLUSTER\_NODE\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-654">5070 (0x13ce)</span><span class="sxs-lookup"><span data-stu-id="e671e-654">5070 (0x13CE)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-655">Der Cluster Knoten wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="e671e-655">The cluster node is paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-656"><span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**Fehler \_ Knoten \_ , \_ Host \_ Ressource nicht**</span><span class="sxs-lookup"><span data-stu-id="e671e-656"><span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**ERROR\_NODE\_CANT\_HOST\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-657">5071 (0x13cf)</span><span class="sxs-lookup"><span data-stu-id="e671e-657">5071 (0x13CF)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-658">Die Cluster Ressource kann nicht online geschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-658">The cluster resource cannot be brought online.</span></span> <span data-ttu-id="e671e-659">Der Besitzer Knoten kann diese Ressource nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="e671e-659">The owner node cannot run this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-660"><span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**Fehler \_ Cluster \_ Knoten ist \_ nicht \_ bereit**</span><span class="sxs-lookup"><span data-stu-id="e671e-660"><span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**ERROR\_CLUSTER\_NODE\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-661">5072 (0x13d0)</span><span class="sxs-lookup"><span data-stu-id="e671e-661">5072 (0x13D0)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-662">Der Cluster Knoten ist nicht bereit zum Ausführen des angeforderten Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="e671e-662">The cluster node is not ready to perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-663"><span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**Fehler beim Herunterfahren des \_ Cluster \_ Knotens \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-663"><span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**ERROR\_CLUSTER\_NODE\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-664">5073 (0x13d1)</span><span class="sxs-lookup"><span data-stu-id="e671e-664">5073 (0x13D1)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-665">Der Cluster Knoten wird heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="e671e-665">The cluster node is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-666"><span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**Fehler beim Abbrechen des Cluster Joins. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-666"><span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**ERROR\_CLUSTER\_JOIN\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-667">5074 (0x13d2)</span><span class="sxs-lookup"><span data-stu-id="e671e-667">5074 (0x13D2)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-668">Der clusterjoinvorgang wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="e671e-668">The cluster join operation was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-669"><span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**Fehler \_ Cluster- \_ inkompatible \_ Versionen**</span><span class="sxs-lookup"><span data-stu-id="e671e-669"><span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**ERROR\_CLUSTER\_INCOMPATIBLE\_VERSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-670">5075 (0x13d3)</span><span class="sxs-lookup"><span data-stu-id="e671e-670">5075 (0x13D3)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-671">Fehler beim clusterjoinvorgang aufgrund nicht kompatibler Softwareversionen zwischen dem Verknüpfungs Knoten und seinem Sponsor.</span><span class="sxs-lookup"><span data-stu-id="e671e-671">The cluster join operation failed due to incompatible software versions between the joining node and its sponsor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-672"><span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**Fehler \_ Cluster- \_ maxnum \_ von \_ Ressourcen \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="e671e-672"><span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**ERROR\_CLUSTER\_MAXNUM\_OF\_RESOURCES\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-673">5076 (0x13d4)</span><span class="sxs-lookup"><span data-stu-id="e671e-673">5076 (0x13D4)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-674">Diese Ressource kann nicht erstellt werden, da der Cluster das Limit für die Anzahl der zu überwachenden Ressourcen erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="e671e-674">This resource cannot be created because the cluster has reached the limit on the number of resources it can monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-675"><span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**Fehler beim \_ Ändern der Cluster \_ System \_ Konfiguration \_ .**</span><span class="sxs-lookup"><span data-stu-id="e671e-675"><span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**ERROR\_CLUSTER\_SYSTEM\_CONFIG\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-676">5077 (0x13d5)</span><span class="sxs-lookup"><span data-stu-id="e671e-676">5077 (0x13D5)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-677">Die Systemkonfiguration wurde während des clusterjoins oder-Formular Vorgangs geändert.</span><span class="sxs-lookup"><span data-stu-id="e671e-677">The system configuration changed during the cluster join or form operation.</span></span> <span data-ttu-id="e671e-678">Der Join-oder Form-Vorgang wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="e671e-678">The join or form operation was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-679"><span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**Fehler \_ beim \_ Cluster \_ Ressourcentyp \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-679"><span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**ERROR\_CLUSTER\_RESOURCE\_TYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-680">5078 (0x13d6)</span><span class="sxs-lookup"><span data-stu-id="e671e-680">5078 (0x13D6)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-681">Der angegebene Ressourcentyp wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e671e-681">The specified resource type was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-682"><span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**Fehler \_ Cluster- \_ RESTYPE \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="e671e-682"><span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**ERROR\_CLUSTER\_RESTYPE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-683">5079 (0x13d7)</span><span class="sxs-lookup"><span data-stu-id="e671e-683">5079 (0x13D7)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-684">Der angegebene Knoten unterstützt keine Ressource dieses Typs.</span><span class="sxs-lookup"><span data-stu-id="e671e-684">The specified node does not support a resource of this type.</span></span> <span data-ttu-id="e671e-685">Dies kann auf Versions Inkonsistenzen oder darauf zurückzuführen sein, dass die Ressourcen-DLL auf diesem Knoten fehlt.</span><span class="sxs-lookup"><span data-stu-id="e671e-685">This may be due to version inconsistencies or due to the absence of the resource DLL on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-686"><span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**Fehler \_ Cluster- \_ Resname wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-686"><span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**ERROR\_CLUSTER\_RESNAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-687">5080 (0x13d8)</span><span class="sxs-lookup"><span data-stu-id="e671e-687">5080 (0x13D8)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-688">Der angegebene Ressourcen Name wird von dieser Ressourcen-DLL nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e671e-688">The specified resource name is not supported by this resource DLL.</span></span> <span data-ttu-id="e671e-689">Dies kann auf einen ungültigen (oder geänderten) Namen zurückzuführen sein, der für die Ressourcen-DLL angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e671e-689">This may be due to a bad (or changed) name supplied to the resource DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-690"><span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**Fehler \_ Cluster \_ keine \_ RPC- \_ Pakete \_ registriert**</span><span class="sxs-lookup"><span data-stu-id="e671e-690"><span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**ERROR\_CLUSTER\_NO\_RPC\_PACKAGES\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-691">5081 (0x13d9)</span><span class="sxs-lookup"><span data-stu-id="e671e-691">5081 (0x13D9)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-692">Es konnte kein Authentifizierungs Paket beim RPC-Server registriert werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-692">No authentication package could be registered with the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-693"><span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**\_ \_ der Besitzer des Fehler Clusters ist \_ nicht \_ im \_ voraus.**</span><span class="sxs-lookup"><span data-stu-id="e671e-693"><span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**ERROR\_CLUSTER\_OWNER\_NOT\_IN\_PREFLIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-694">5082 (0x13da)</span><span class="sxs-lookup"><span data-stu-id="e671e-694">5082 (0x13DA)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-695">Die Gruppe kann nicht online geschaltet werden, da der Besitzer der Gruppe nicht in der bevorzugten Liste für die Gruppe enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-695">You cannot bring the group online because the owner of the group is not in the preferred list for the group.</span></span> <span data-ttu-id="e671e-696">Um den Besitzer Knoten für die Gruppe zu ändern, verschieben Sie die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="e671e-696">To change the owner node for the group, move the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-697"><span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**Fehler bei \_ Cluster Datenbank, nicht \_ \_ übereinstimmende**</span><span class="sxs-lookup"><span data-stu-id="e671e-697"><span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**ERROR\_CLUSTER\_DATABASE\_SEQMISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-698">5083 (0x13db)</span><span class="sxs-lookup"><span data-stu-id="e671e-698">5083 (0x13DB)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-699">Der Joinvorgang ist fehlgeschlagen, weil die Sequenznummer der Cluster Datenbank geändert wurde oder mit dem Knoten locker nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-699">The join operation failed because the cluster database sequence number has changed or is incompatible with the locker node.</span></span> <span data-ttu-id="e671e-700">Dies kann während eines Verknüpfungs Vorgangs vorkommen, wenn die Cluster Datenbank während des Joins geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="e671e-700">This may happen during a join operation if the cluster database was changing during the join.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-701"><span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**Fehler \_ beim resmon ( \_ ungültiger \_ Zustand)**</span><span class="sxs-lookup"><span data-stu-id="e671e-701"><span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**ERROR\_RESMON\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-702">5084 (0x13dc)</span><span class="sxs-lookup"><span data-stu-id="e671e-702">5084 (0x13DC)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-703">Der Ressourcen Monitor lässt nicht zu, dass der Fail-Vorgang ausgeführt wird, während sich die Ressource in Ihrem aktuellen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="e671e-703">The resource monitor will not allow the fail operation to be performed while the resource is in its current state.</span></span> <span data-ttu-id="e671e-704">Dies kann vorkommen, wenn sich die Ressource im Status "Ausstehend" befindet.</span><span class="sxs-lookup"><span data-stu-id="e671e-704">This may happen if the resource is in a pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-705"><span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**Fehler \_ Cluster- \_ Kaugummi \_ nicht \_ locker**</span><span class="sxs-lookup"><span data-stu-id="e671e-705"><span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**ERROR\_CLUSTER\_GUM\_NOT\_LOCKER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-706">5085 (0x13dd)</span><span class="sxs-lookup"><span data-stu-id="e671e-706">5085 (0x13DD)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-707">Ein nicht locker-Code hat eine Anforderung zum Reservieren der Sperre für globale Updates erhalten.</span><span class="sxs-lookup"><span data-stu-id="e671e-707">A non locker code got a request to reserve the lock for making global updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-708"><span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**Fehler Quorum Datenträger \_ \_ \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="e671e-708"><span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**ERROR\_QUORUM\_DISK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-709">5086 (0x13de)</span><span class="sxs-lookup"><span data-stu-id="e671e-709">5086 (0x13DE)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-710">Der Quorum Datenträger konnte vom Cluster Dienst nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-710">The quorum disk could not be located by the cluster service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-711"><span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**Fehler \_ Daten Bank \_ Sicherung \_ beschädigt**</span><span class="sxs-lookup"><span data-stu-id="e671e-711"><span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**ERROR\_DATABASE\_BACKUP\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-712">5087 (0x13df)</span><span class="sxs-lookup"><span data-stu-id="e671e-712">5087 (0x13DF)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-713">Die gesicherte Cluster Datenbank ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="e671e-713">The backed up cluster database is possibly corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-714"><span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**Fehler \_ Cluster \_ Knoten \_ \_ weist bereits \_ DFS \_ -Stamm auf.**</span><span class="sxs-lookup"><span data-stu-id="e671e-714"><span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_HAS\_DFS\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-715">5088 (0x13e0)</span><span class="sxs-lookup"><span data-stu-id="e671e-715">5088 (0x13E0)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-716">Ein DFS-Stamm ist bereits in diesem Cluster Knoten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e671e-716">A DFS root already exists in this cluster node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-717"><span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**fehlerhafte \_ Ressourcen \_ Eigenschaft \_ nicht änderbar**</span><span class="sxs-lookup"><span data-stu-id="e671e-717"><span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**ERROR\_RESOURCE\_PROPERTY\_UNCHANGEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-718">5089 (0x13e1)</span><span class="sxs-lookup"><span data-stu-id="e671e-718">5089 (0x13E1)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-719">Der Versuch, eine Ressourcen Eigenschaft zu ändern, ist fehlgeschlagen, da Sie einen Konflikt mit einer anderen vorhandenen Eigenschaft verursacht</span><span class="sxs-lookup"><span data-stu-id="e671e-719">An attempt to modify a resource property failed because it conflicts with another existing property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-720"><span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**\_ \_ \_ Ungültiger Status der Fehler Cluster Mitgliedschaft. \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-720"><span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**ERROR\_CLUSTER\_MEMBERSHIP\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-721">5890 (0x1702)</span><span class="sxs-lookup"><span data-stu-id="e671e-721">5890 (0x1702)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-722">Es wurde versucht, einen Vorgang auszuführen, der nicht mit dem aktuellen Mitgliedschaftsstatus des Knotens kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-722">An operation was attempted that is incompatible with the current membership state of the node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-723"><span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**Fehler \_ Cluster- \_ quorumschlag \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-723"><span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**ERROR\_CLUSTER\_QUORUMLOG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-724">5891 (0x1703)</span><span class="sxs-lookup"><span data-stu-id="e671e-724">5891 (0x1703)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-725">Die Quorum Ressource enthält nicht das Quorum Protokoll.</span><span class="sxs-lookup"><span data-stu-id="e671e-725">The quorum resource does not contain the quorum log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-726"><span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**Fehler beim \_ Anhalten der Cluster \_ Mitgliedschaft \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-726"><span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**ERROR\_CLUSTER\_MEMBERSHIP\_HALT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-727">5892 (0x1704)</span><span class="sxs-lookup"><span data-stu-id="e671e-727">5892 (0x1704)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-728">Das Mitgliedschafts Modul hat das Herunterfahren des Cluster Dienstanbieter auf diesem Knoten angefordert.</span><span class="sxs-lookup"><span data-stu-id="e671e-728">The membership engine requested shutdown of the cluster service on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-729"><span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**Fehler bei \_ Cluster \_ Instanz- \_ ID stimmen nicht \_ überein.**</span><span class="sxs-lookup"><span data-stu-id="e671e-729"><span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**ERROR\_CLUSTER\_INSTANCE\_ID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-730">5893 (0x1705)</span><span class="sxs-lookup"><span data-stu-id="e671e-730">5893 (0x1705)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-731">Der Joinvorgang ist fehlgeschlagen, da die Clusterinstanz-ID des verknüpften Knotens nicht mit der Cluster Instanz-ID des Sponsor-Knotens identisch ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-731">The join operation failed because the cluster instance ID of the joining node does not match the cluster instance ID of the sponsor node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-732"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**Fehler \_ Cluster \_ Netzwerk \_ \_ \_ für IP nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="e671e-732"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_FOUND\_FOR\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-733">5894 (0x1706)</span><span class="sxs-lookup"><span data-stu-id="e671e-733">5894 (0x1706)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-734">Ein entsprechendes Cluster Netzwerk für die angegebene IP-Adresse wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e671e-734">A matching cluster network for the specified IP address could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-735"><span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**Fehler \_ beim \_ \_ \_ Datentyp der Cluster Eigenschaft. \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-735"><span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**ERROR\_CLUSTER\_PROPERTY\_DATA\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-736">5895 (0x1707)</span><span class="sxs-lookup"><span data-stu-id="e671e-736">5895 (0x1707)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-737">Der tatsächliche Datentyp der Eigenschaft entsprach nicht dem erwarteten Datentyp der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e671e-737">The actual data type of the property did not match the expected data type of the property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-738"><span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**Fehler \_ Cluster entfernen \_ \_ ohne \_ Cleanup**</span><span class="sxs-lookup"><span data-stu-id="e671e-738"><span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**ERROR\_CLUSTER\_EVICT\_WITHOUT\_CLEANUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-739">5896 (0x1708)</span><span class="sxs-lookup"><span data-stu-id="e671e-739">5896 (0x1708)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-740">Der Cluster Knoten wurde erfolgreich aus dem Cluster entfernt, aber der Knoten wurde nicht bereinigt.</span><span class="sxs-lookup"><span data-stu-id="e671e-740">The cluster node was evicted from the cluster successfully, but the node was not cleaned up.</span></span> <span data-ttu-id="e671e-741">Informationen zu den fehlerhaften Bereinigungs Schritten und zur Wiederherstellung finden Sie im Ereignisprotokoll für die Failoverclustering-Anwendung mit Ereignisanzeige.</span><span class="sxs-lookup"><span data-stu-id="e671e-741">To determine what cleanup steps failed and how to recover, see the Failover Clustering application event log using Event Viewer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-742"><span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**Fehler \_ Cluster \_ Parameter \_ stimmen nicht überein.**</span><span class="sxs-lookup"><span data-stu-id="e671e-742"><span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**ERROR\_CLUSTER\_PARAMETER\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-743">5897 (0x1709)</span><span class="sxs-lookup"><span data-stu-id="e671e-743">5897 (0x1709)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-744">Mindestens zwei Parameterwerte, die für die Eigenschaften einer Ressource angegeben sind, sind in Konflikt.</span><span class="sxs-lookup"><span data-stu-id="e671e-744">Two or more parameter values specified for a resource's properties are in conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-745"><span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**Fehler \_ Knoten \_ kann \_ nicht \_ gruppiert werden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-745"><span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**ERROR\_NODE\_CANNOT\_BE\_CLUSTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-746">5898 (0x170a)</span><span class="sxs-lookup"><span data-stu-id="e671e-746">5898 (0x170A)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-747">Dieser Computer kann nicht Mitglied eines Clusters werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-747">This computer cannot be made a member of a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-748"><span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**\_ \_ falsche \_ Betriebssystem \_ Version des Fehler Clusters**</span><span class="sxs-lookup"><span data-stu-id="e671e-748"><span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**ERROR\_CLUSTER\_WRONG\_OS\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-749">5899 (0x170b)</span><span class="sxs-lookup"><span data-stu-id="e671e-749">5899 (0x170B)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-750">Dieser Computer kann nicht Mitglied eines Clusters werden, da er nicht die richtige Version von Windows installiert hat.</span><span class="sxs-lookup"><span data-stu-id="e671e-750">This computer cannot be made a member of a cluster because it does not have the correct version of Windows installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-751"><span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**Fehler \_ Cluster Fehler beim \_ Erstellen des DUP- \_ \_ \_ Cluster \_ namens**</span><span class="sxs-lookup"><span data-stu-id="e671e-751"><span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**ERROR\_CLUSTER\_CANT\_CREATE\_DUP\_CLUSTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-752">5900 (0x170c)</span><span class="sxs-lookup"><span data-stu-id="e671e-752">5900 (0x170C)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-753">Ein Cluster kann nicht mit dem angegebenen Cluster Namen erstellt werden, da dieser Cluster Name bereits verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e671e-753">A cluster cannot be created with the specified cluster name because that cluster name is already in use.</span></span> <span data-ttu-id="e671e-754">Geben Sie einen anderen Namen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="e671e-754">Specify a different name for the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-755"><span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**Fehler beim \_ Cluscfg-Commit. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-755"><span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**ERROR\_CLUSCFG\_ALREADY\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-756">5901 (0x170d)</span><span class="sxs-lookup"><span data-stu-id="e671e-756">5901 (0x170D)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-757">Für die Cluster Konfigurations Aktion wurde bereits ein Commit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e671e-757">The cluster configuration action has already been committed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-758"><span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**Fehler beim \_ Cluscfg- \_ Rollback. \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-758"><span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**ERROR\_CLUSCFG\_ROLLBACK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-759">5902 (0x170e)</span><span class="sxs-lookup"><span data-stu-id="e671e-759">5902 (0x170E)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-760">Für die Cluster Konfigurations Aktion konnte kein Rollback ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-760">The cluster configuration action could not be rolled back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-761"><span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**Fehler beim \_ Cluscfg-System Laufwerks \_ \_ \_ \_ Buchstaben \_ .**</span><span class="sxs-lookup"><span data-stu-id="e671e-761"><span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**ERROR\_CLUSCFG\_SYSTEM\_DISK\_DRIVE\_LETTER\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-762">5903 (0x170f)</span><span class="sxs-lookup"><span data-stu-id="e671e-762">5903 (0x170F)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-763">Der einem System Datenträger auf einem Knoten zugewiesene Laufwerk Buchstabe steht in Konflikt mit dem Laufwerk Buchstaben, der einem Datenträger auf einem anderen Knoten zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-763">The drive letter assigned to a system disk on one node conflicted with the drive letter assigned to a disk on another node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-764"><span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**Fehler beim \_ Gruppieren der \_ alten \_ Version.**</span><span class="sxs-lookup"><span data-stu-id="e671e-764"><span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**ERROR\_CLUSTER\_OLD\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-765">5904 (0x1710)</span><span class="sxs-lookup"><span data-stu-id="e671e-765">5904 (0x1710)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-766">Mindestens ein Knoten im Cluster führt eine Version von Windows aus, die diesen Vorgang nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e671e-766">One or more nodes in the cluster are running a version of Windows that does not support this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-767"><span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**Fehler \_ Cluster nicht \_ übereinstimmender \_ Computer \_ Acct- \_ Name**</span><span class="sxs-lookup"><span data-stu-id="e671e-767"><span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**ERROR\_CLUSTER\_MISMATCHED\_COMPUTER\_ACCT\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-768">5905 (0x1711)</span><span class="sxs-lookup"><span data-stu-id="e671e-768">5905 (0x1711)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-769">Der Name des entsprechenden Computer Kontos stimmt nicht mit dem Netzwerknamen für diese Ressource überein.</span><span class="sxs-lookup"><span data-stu-id="e671e-769">The name of the corresponding computer account doesn't match the Network Name for this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-770"><span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**Fehler \_ Cluster \_ ohne \_ Netzwerk \_ Adapter**</span><span class="sxs-lookup"><span data-stu-id="e671e-770"><span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**ERROR\_CLUSTER\_NO\_NET\_ADAPTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-771">5906 (0x1712)</span><span class="sxs-lookup"><span data-stu-id="e671e-771">5906 (0x1712)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-772">Es sind keine Netzwerkadapter verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e671e-772">No network adapters are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-773"><span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**Fehler \_ Cluster \_ vergiftet**</span><span class="sxs-lookup"><span data-stu-id="e671e-773"><span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**ERROR\_CLUSTER\_POISONED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-774">5907 (0x1713)</span><span class="sxs-lookup"><span data-stu-id="e671e-774">5907 (0x1713)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-775">Der Cluster Knoten wurde vergiftet.</span><span class="sxs-lookup"><span data-stu-id="e671e-775">The cluster node has been poisoned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-776"><span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**Verschieben von Fehler \_ Cluster \_ Gruppen \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-776"><span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**ERROR\_CLUSTER\_GROUP\_MOVING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-777">5908 (0x1714)</span><span class="sxs-lookup"><span data-stu-id="e671e-777">5908 (0x1714)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-778">Die Gruppe kann die Anforderung nicht akzeptieren, da Sie auf einen anderen Knoten verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="e671e-778">The group is unable to accept the request since it is moving to another node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-779"><span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**Fehler \_ Cluster \_ - \_ Ressourcentyp \_ ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="e671e-779"><span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**ERROR\_CLUSTER\_RESOURCE\_TYPE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-780">5909 (0x1715)</span><span class="sxs-lookup"><span data-stu-id="e671e-780">5909 (0x1715)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-781">Der Ressourcentyp kann die Anforderung nicht akzeptieren, da zu stark ausgelastet ist und einen anderen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="e671e-781">The resource type cannot accept the request since is too busy performing another operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-782"><span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**\_Timeout beim \_ Ressourcen \_ Rückruf \_ .**</span><span class="sxs-lookup"><span data-stu-id="e671e-782"><span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**ERROR\_RESOURCE\_CALL\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-783">5910 (0x1716)</span><span class="sxs-lookup"><span data-stu-id="e671e-783">5910 (0x1716)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-784">Timeout beim Abrufen der Cluster Ressourcen-DLL.</span><span class="sxs-lookup"><span data-stu-id="e671e-784">The call to the cluster resource DLL timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-785"><span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**Fehler \_ ungültige \_ Cluster- \_ IPv6- \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="e671e-785"><span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**ERROR\_INVALID\_CLUSTER\_IPV6\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-786">5911 (0x1717)</span><span class="sxs-lookup"><span data-stu-id="e671e-786">5911 (0x1717)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-787">Die Adresse ist für eine IPv6-Adress Ressource ungültig.</span><span class="sxs-lookup"><span data-stu-id="e671e-787">The address is not valid for an IPv6 Address resource.</span></span> <span data-ttu-id="e671e-788">Eine globale IPv6-Adresse ist erforderlich, und Sie muss mit einem Cluster Netzwerk identisch sein.</span><span class="sxs-lookup"><span data-stu-id="e671e-788">A global IPv6 address is required, and it must match a cluster network.</span></span> <span data-ttu-id="e671e-789">Kompatibilitäts Adressen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="e671e-789">Compatibility addresses are not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-790"><span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**Fehler bei der \_ internen Fehler Cluster \_ \_ \_ Funktion.**</span><span class="sxs-lookup"><span data-stu-id="e671e-790"><span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**ERROR\_CLUSTER\_INTERNAL\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-791">5912 (0x1718)</span><span class="sxs-lookup"><span data-stu-id="e671e-791">5912 (0x1718)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-792">Ein interner Cluster Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e671e-792">An internal cluster error occurred.</span></span> <span data-ttu-id="e671e-793">Es wurde versucht, eine ungültige Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e671e-793">A call to an invalid function was attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-794"><span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**Fehler \_ Cluster \_ Parameter \_ außerhalb \_ des \_ gültigen Bereichs**</span><span class="sxs-lookup"><span data-stu-id="e671e-794"><span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**ERROR\_CLUSTER\_PARAMETER\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-795">5913 (0x1719)</span><span class="sxs-lookup"><span data-stu-id="e671e-795">5913 (0x1719)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-796">Ein Parameterwert liegt außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="e671e-796">A parameter value is out of acceptable range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-797"><span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**Fehler \_ beim \_ partiellen Senden des Fehlers \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-797"><span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**ERROR\_CLUSTER\_PARTIAL\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-798">5914 (0x171a)</span><span class="sxs-lookup"><span data-stu-id="e671e-798">5914 (0x171A)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-799">Beim Senden von Daten an einen anderen Knoten im Cluster ist ein Netzwerkfehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e671e-799">A network error occurred while sending data to another node in the cluster.</span></span> <span data-ttu-id="e671e-800">Die Anzahl der übertragenen Bytes war kleiner als erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e671e-800">The number of bytes transmitted was less than required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-801"><span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**\_ \_ \_ Ungültige Funktion der Fehler Cluster Registrierung \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-801"><span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**ERROR\_CLUSTER\_REGISTRY\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-802">5915 (0x171b)</span><span class="sxs-lookup"><span data-stu-id="e671e-802">5915 (0x171B)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-803">Es wurde versucht, einen ungültigen Cluster Registrierungsvorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e671e-803">An invalid cluster registry operation was attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-804"><span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**Fehler beim Beenden des Fehler \_ Clusters \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-804"><span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**ERROR\_CLUSTER\_INVALID\_STRING\_TERMINATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-805">5916 (0x171c)</span><span class="sxs-lookup"><span data-stu-id="e671e-805">5916 (0x171C)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-806">Eine Eingabe Zeichenfolge von Zeichen wird nicht ordnungsgemäß beendet.</span><span class="sxs-lookup"><span data-stu-id="e671e-806">An input string of characters is not properly terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-807"><span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**\_ \_ ungültiges \_ Zeichen folgen \_ Format für Fehler Cluster**</span><span class="sxs-lookup"><span data-stu-id="e671e-807"><span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**ERROR\_CLUSTER\_INVALID\_STRING\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-808">5917 (0x171d)</span><span class="sxs-lookup"><span data-stu-id="e671e-808">5917 (0x171D)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-809">Eine Eingabe Zeichenfolge von Zeichen weist kein gültiges Format für die Daten auf, die Sie darstellt.</span><span class="sxs-lookup"><span data-stu-id="e671e-809">An input string of characters is not in a valid format for the data it represents.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-810"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**Fehler \_ Cluster- \_ Daten Bank \_ Transaktion \_ \_ wird ausgeführt.**</span><span class="sxs-lookup"><span data-stu-id="e671e-810"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**ERROR\_CLUSTER\_DATABASE\_TRANSACTION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-811">5918 (0x171e)</span><span class="sxs-lookup"><span data-stu-id="e671e-811">5918 (0x171E)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-812">Ein interner Cluster Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e671e-812">An internal cluster error occurred.</span></span> <span data-ttu-id="e671e-813">Es wurde versucht, eine Cluster Datenbanktransaktion auszuführen, während bereits eine Transaktion ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="e671e-813">A cluster database transaction was attempted while a transaction was already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-814"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**Fehler \_ Cluster- \_ Daten Bank \_ Transaktion wird \_ nicht \_ \_ ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="e671e-814"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**ERROR\_CLUSTER\_DATABASE\_TRANSACTION\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-815">5919 (0x171f)</span><span class="sxs-lookup"><span data-stu-id="e671e-815">5919 (0x171F)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-816">Ein interner Cluster Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e671e-816">An internal cluster error occurred.</span></span> <span data-ttu-id="e671e-817">Es wurde versucht, einen Commit für eine Cluster Datenbanktransaktion durchgeführt, während keine Transaktion durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="e671e-817">There was an attempt to commit a cluster database transaction while no transaction was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-818"><span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**Fehler beim \_ Cluster \_ NULL- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="e671e-818"><span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**ERROR\_CLUSTER\_NULL\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-819">5920 (0x1720)</span><span class="sxs-lookup"><span data-stu-id="e671e-819">5920 (0x1720)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-820">Ein interner Cluster Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e671e-820">An internal cluster error occurred.</span></span> <span data-ttu-id="e671e-821">Die Daten wurden nicht ordnungsgemäß initialisiert.</span><span class="sxs-lookup"><span data-stu-id="e671e-821">Data was not properly initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-822"><span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**\_ \_ teilweises \_ Lesen des Fehler Clusters**</span><span class="sxs-lookup"><span data-stu-id="e671e-822"><span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**ERROR\_CLUSTER\_PARTIAL\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-823">5921 (0x1721)</span><span class="sxs-lookup"><span data-stu-id="e671e-823">5921 (0x1721)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-824">Fehler beim Lesen aus einem Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="e671e-824">An error occurred while reading from a stream of data.</span></span> <span data-ttu-id="e671e-825">Es wurde eine unerwartete Anzahl von Bytes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e671e-825">An unexpected number of bytes was returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-826"><span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**Fehler \_ beim \_ partiellen Schreiben des Clusters \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-826"><span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**ERROR\_CLUSTER\_PARTIAL\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-827">5922 (0x1722)</span><span class="sxs-lookup"><span data-stu-id="e671e-827">5922 (0x1722)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-828">Fehler beim Schreiben in einen Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="e671e-828">An error occurred while writing to a stream of data.</span></span> <span data-ttu-id="e671e-829">Die erforderliche Anzahl von Bytes konnte nicht geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-829">The required number of bytes could not be written.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-830"><span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**Fehler \_ Cluster Fehler beim \_ \_ Deserialisieren von \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="e671e-830"><span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**ERROR\_CLUSTER\_CANT\_DESERIALIZE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-831">5923 (0x1723)</span><span class="sxs-lookup"><span data-stu-id="e671e-831">5923 (0x1723)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-832">Fehler beim Deserialisieren eines Streams von Cluster Daten.</span><span class="sxs-lookup"><span data-stu-id="e671e-832">An error occurred while deserializing a stream of cluster data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-833"><span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**Fehler \_ abhängiger \_ Ressourcen \_ Eigenschafts \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="e671e-833"><span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**ERROR\_DEPENDENT\_RESOURCE\_PROPERTY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-834">5924 (0x1724)</span><span class="sxs-lookup"><span data-stu-id="e671e-834">5924 (0x1724)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-835">Mindestens ein Eigenschafts Wert für diese Ressource steht in Konflikt mit einem oder mehreren Eigenschafts Werten, die den abhängigen Ressourcen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e671e-835">One or more property values for this resource are in conflict with one or more property values associated with its dependent resource(s).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-836"><span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**Fehler \_ Cluster \_ ohne \_ Quorum**</span><span class="sxs-lookup"><span data-stu-id="e671e-836"><span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**ERROR\_CLUSTER\_NO\_QUORUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-837">5925 (0x1725)</span><span class="sxs-lookup"><span data-stu-id="e671e-837">5925 (0x1725)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-838">Es war kein Quorum von Cluster Knoten vorhanden, um einen Cluster zu bilden.</span><span class="sxs-lookup"><span data-stu-id="e671e-838">A quorum of cluster nodes was not present to form a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-839"><span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**\_ \_ Ungültiges \_ IPv6- \_ Netzwerk für Fehler Cluster**</span><span class="sxs-lookup"><span data-stu-id="e671e-839"><span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**ERROR\_CLUSTER\_INVALID\_IPV6\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-840">5926 (0x1726)</span><span class="sxs-lookup"><span data-stu-id="e671e-840">5926 (0x1726)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-841">Das Cluster Netzwerk ist für eine IPv6-Adress Ressource ungültig oder entspricht nicht der konfigurierten Adresse.</span><span class="sxs-lookup"><span data-stu-id="e671e-841">The cluster network is not valid for an IPv6 Address resource, or it does not match the configured address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-842"><span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**Fehler \_ Cluster \_ ungültiges \_ IPv6- \_ Tunnel \_ Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="e671e-842"><span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**ERROR\_CLUSTER\_INVALID\_IPV6\_TUNNEL\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-843">5927 (0x1727)</span><span class="sxs-lookup"><span data-stu-id="e671e-843">5927 (0x1727)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-844">Das Cluster Netzwerk ist für eine IPv6-Tunnel Ressource ungültig.</span><span class="sxs-lookup"><span data-stu-id="e671e-844">The cluster network is not valid for an IPv6 Tunnel resource.</span></span> <span data-ttu-id="e671e-845">Überprüfen Sie die Konfiguration der IP-Adress Ressource, von der die IPv6-Tunnel Ressource abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-845">Check the configuration of the IP Address resource on which the IPv6 Tunnel resource depends.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-846"><span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**\_das Fehler Quorum ist \_ \_ \_ in \_ dieser \_ Gruppe nicht zulässig.**</span><span class="sxs-lookup"><span data-stu-id="e671e-846"><span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**ERROR\_QUORUM\_NOT\_ALLOWED\_IN\_THIS\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-847">5928 (0x1728)</span><span class="sxs-lookup"><span data-stu-id="e671e-847">5928 (0x1728)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-848">Die Quorum Ressource darf sich nicht in der verfügbaren Speicher Gruppe befinden.</span><span class="sxs-lookup"><span data-stu-id="e671e-848">Quorum resource cannot reside in the Available Storage group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-849"><span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**Fehler \_ Abhängigkeitsstruktur \_ \_ zu \_ Komplex**</span><span class="sxs-lookup"><span data-stu-id="e671e-849"><span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**ERROR\_DEPENDENCY\_TREE\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-850">5929 (0x1729)</span><span class="sxs-lookup"><span data-stu-id="e671e-850">5929 (0x1729)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-851">Die Abhängigkeiten für diese Ressource sind zu tief geschachtelt.</span><span class="sxs-lookup"><span data-stu-id="e671e-851">The dependencies for this resource are nested too deeply.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-852"><span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**Fehler \_ Ausnahme \_ beim \_ Ressourcen \_ Rückruf.**</span><span class="sxs-lookup"><span data-stu-id="e671e-852"><span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**ERROR\_EXCEPTION\_IN\_RESOURCE\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-853">5930 (0x172 a)</span><span class="sxs-lookup"><span data-stu-id="e671e-853">5930 (0x172A)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-854">Beim Abrufen der Ressourcen-DLL wurde eine nicht behandelte Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="e671e-854">The call into the resource DLL raised an unhandled exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-855"><span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**Fehler \_ Cluster- \_ RHS \_ konnte nicht \_ initialisiert werden**</span><span class="sxs-lookup"><span data-stu-id="e671e-855"><span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**ERROR\_CLUSTER\_RHS\_FAILED\_INITIALIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-856">5931 (0x172 b)</span><span class="sxs-lookup"><span data-stu-id="e671e-856">5931 (0x172B)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-857">Der RHS-Prozess konnte nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-857">The RHS process failed to initialize.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-858"><span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**Fehler \_ Cluster \_ nicht \_ installiert**</span><span class="sxs-lookup"><span data-stu-id="e671e-858"><span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**ERROR\_CLUSTER\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-859">5932 (0x172 c)</span><span class="sxs-lookup"><span data-stu-id="e671e-859">5932 (0x172C)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-860">Das Failoverclustering-Feature ist auf diesem Knoten nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="e671e-860">The Failover Clustering feature is not installed on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-861"><span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**Fehler \_ Cluster \_ Ressourcen \_ müssen \_ \_ \_ auf \_ \_ demselben \_ Knoten online sein**</span><span class="sxs-lookup"><span data-stu-id="e671e-861"><span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**ERROR\_CLUSTER\_RESOURCES\_MUST\_BE\_ONLINE\_ON\_THE\_SAME\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-862">5933 (0x172 d)</span><span class="sxs-lookup"><span data-stu-id="e671e-862">5933 (0x172D)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-863">Die Ressourcen müssen für diesen Vorgang auf dem gleichen Knoten online sein.</span><span class="sxs-lookup"><span data-stu-id="e671e-863">The resources must be online on the same node for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-864"><span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**\_Knoten "Max. Cluster Knoten" \_ \_ \_ im \_ Cluster**</span><span class="sxs-lookup"><span data-stu-id="e671e-864"><span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**ERROR\_CLUSTER\_MAX\_NODES\_IN\_CLUSTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-865">5934 (0x172 e)</span><span class="sxs-lookup"><span data-stu-id="e671e-865">5934 (0x172E)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-866">Ein neuer Knoten kann nicht hinzugefügt werden, da dieser Cluster bereits über die maximale Anzahl von Knoten verfügt.</span><span class="sxs-lookup"><span data-stu-id="e671e-866">A new node can not be added since this cluster is already at its maximum number of nodes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-867"><span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**Fehler \_ Cluster \_ zu \_ viele \_ Knoten**</span><span class="sxs-lookup"><span data-stu-id="e671e-867"><span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**ERROR\_CLUSTER\_TOO\_MANY\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-868">5935 (0x172 f)</span><span class="sxs-lookup"><span data-stu-id="e671e-868">5935 (0x172F)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-869">Dieser Cluster kann nicht erstellt werden, da die angegebene Anzahl von Knoten die maximal zulässige Grenze überschreitet.</span><span class="sxs-lookup"><span data-stu-id="e671e-869">This cluster can not be created since the specified number of nodes exceeds the maximum allowed limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-870"><span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**Fehler \_ Cluster \_ Objekt \_ bereits \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="e671e-870"><span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**ERROR\_CLUSTER\_OBJECT\_ALREADY\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-871">5936 (0x1730)</span><span class="sxs-lookup"><span data-stu-id="e671e-871">5936 (0x1730)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-872">Der Versuch, den angegebenen Cluster Namen zu verwenden, ist fehlgeschlagen, da ein aktiviertes Computer Objekt mit dem angegebenen Namen bereits in der Domäne vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-872">An attempt to use the specified cluster name failed because an enabled computer object with the given name already exists in the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-873"><span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**Fehler \_ nicht-Kern \_ Gruppen \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="e671e-873"><span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**ERROR\_NONCORE\_GROUPS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-874">5937 (0x1731)</span><span class="sxs-lookup"><span data-stu-id="e671e-874">5937 (0x1731)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-875">Dieser Cluster kann nicht zerstört werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-875">This cluster cannot be destroyed.</span></span> <span data-ttu-id="e671e-876">Sie verfügt über nicht-Kern Anwendungs Gruppen, die gelöscht werden müssen, bevor der Cluster zerstört werden kann.</span><span class="sxs-lookup"><span data-stu-id="e671e-876">It has non-core application groups which must be deleted before the cluster can be destroyed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-877"><span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**Fehler \_ Datei \_ Freigabe- \_ Ressourcen \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="e671e-877"><span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**ERROR\_FILE\_SHARE\_RESOURCE\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-878">5938 (0x1732)</span><span class="sxs-lookup"><span data-stu-id="e671e-878">5938 (0x1732)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-879">Die Dateifreigabe, die der Dateifreigabe Zeugen-Ressource zugeordnet ist, kann nicht von diesem Cluster oder einem ihrer Knoten gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-879">File share associated with file share witness resource cannot be hosted by this cluster or any of its nodes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-880"><span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**Fehler beim Entfernen einer \_ \_ \_ ungültigen \_ Anforderung durch den Cluster**</span><span class="sxs-lookup"><span data-stu-id="e671e-880"><span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**ERROR\_CLUSTER\_EVICT\_INVALID\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-881">5939 (0x1733)</span><span class="sxs-lookup"><span data-stu-id="e671e-881">5939 (0x1733)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-882">Das Entfernen dieses Knotens ist zu diesem Zeitpunkt ungültig.</span><span class="sxs-lookup"><span data-stu-id="e671e-882">Eviction of this node is invalid at this time.</span></span> <span data-ttu-id="e671e-883">Aufgrund der Quorum Anforderungen führt das Entfernen des Knotens zum Herunterfahren des Clusters.</span><span class="sxs-lookup"><span data-stu-id="e671e-883">Due to quorum requirements node eviction will result in cluster shutdown.</span></span> <span data-ttu-id="e671e-884">Wenn es sich um den letzten Knoten im Cluster handelt, sollte der Befehl zum Löschen des Clusters verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-884">If it is the last node in the cluster, destroy cluster command should be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-885"><span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**Fehler \_ Cluster- \_ Singleton- \_ Ressource**</span><span class="sxs-lookup"><span data-stu-id="e671e-885"><span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**ERROR\_CLUSTER\_SINGLETON\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-886">5940 (0x1734)</span><span class="sxs-lookup"><span data-stu-id="e671e-886">5940 (0x1734)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-887">Im Cluster ist nur eine Instanz dieses Ressourcentyps zulässig.</span><span class="sxs-lookup"><span data-stu-id="e671e-887">Only one instance of this resource type is allowed in the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-888"><span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**\_ \_ \_ Singleton- \_ Ressource für Fehler Cluster Gruppe**</span><span class="sxs-lookup"><span data-stu-id="e671e-888"><span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**ERROR\_CLUSTER\_GROUP\_SINGLETON\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-889">5941 (0x1735)</span><span class="sxs-lookup"><span data-stu-id="e671e-889">5941 (0x1735)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-890">Pro Ressourcengruppe ist nur eine Instanz dieses Ressourcentyps zulässig.</span><span class="sxs-lookup"><span data-stu-id="e671e-890">Only one instance of this resource type is allowed per resource group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-891"><span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**Fehler beim \_ Cluster \_ Ressourcen \_ Anbieter \_ .**</span><span class="sxs-lookup"><span data-stu-id="e671e-891"><span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**ERROR\_CLUSTER\_RESOURCE\_PROVIDER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-892">5942 (0x1736)</span><span class="sxs-lookup"><span data-stu-id="e671e-892">5942 (0x1736)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-893">Die Ressource konnte aufgrund eines Fehlers bei mindestens einer Anbieter Ressource nicht online geschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-893">The resource failed to come online due to the failure of one or more provider resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-894"><span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**Fehler bei der \_ Konfiguration der Cluster \_ Ressource. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-894"><span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**ERROR\_CLUSTER\_RESOURCE\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-895">5943 (0x1737)</span><span class="sxs-lookup"><span data-stu-id="e671e-895">5943 (0x1737)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-896">Die Ressource hat angegeben, dass Sie auf keinem Knoten online geschaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e671e-896">The resource has indicated that it cannot come online on any node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-897"><span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**Fehler \_ Cluster \_ Gruppe \_ ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="e671e-897"><span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**ERROR\_CLUSTER\_GROUP\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-898">5944 (0x1738)</span><span class="sxs-lookup"><span data-stu-id="e671e-898">5944 (0x1738)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-899">Der aktuelle Vorgang kann für diese Gruppe zu diesem Zeitpunkt nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-899">The current operation cannot be performed on this group at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-900"><span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**Fehler \_ Cluster nicht frei gegebenes \_ \_ \_ Volume**</span><span class="sxs-lookup"><span data-stu-id="e671e-900"><span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**ERROR\_CLUSTER\_NOT\_SHARED\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-901">5945 (0x1739)</span><span class="sxs-lookup"><span data-stu-id="e671e-901">5945 (0x1739)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-902">Das Verzeichnis oder die Datei befindet sich nicht auf einem freigegebenen Cluster Volume.</span><span class="sxs-lookup"><span data-stu-id="e671e-902">The directory or file is not located on a cluster shared volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-903"><span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**\_ \_ ungültiger \_ Sicherheits \_ Deskriptor für Fehler Cluster**</span><span class="sxs-lookup"><span data-stu-id="e671e-903"><span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**ERROR\_CLUSTER\_INVALID\_SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-904">5946 (0x173a)</span><span class="sxs-lookup"><span data-stu-id="e671e-904">5946 (0x173A)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-905">Die Sicherheits Beschreibung erfüllt die Anforderungen für einen Cluster nicht.</span><span class="sxs-lookup"><span data-stu-id="e671e-905">The Security Descriptor does not meet the requirements for a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-906"><span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**Fehler \_ frei \_ gegebene \_ Clustervolumes \_ in \_ Verwendung**</span><span class="sxs-lookup"><span data-stu-id="e671e-906"><span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**ERROR\_CLUSTER\_SHARED\_VOLUMES\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-907">5947 (0x173b)</span><span class="sxs-lookup"><span data-stu-id="e671e-907">5947 (0x173B)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-908">Im Cluster ist mindestens eine freigegebene Volumes-Ressource konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="e671e-908">There is one or more shared volumes resources configured in the cluster.</span></span> <span data-ttu-id="e671e-909">Diese Ressourcen müssen in den verfügbaren Speicher verschoben werden, damit der Vorgang erfolgreich ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="e671e-909">Those resources must be moved to available storage in order for operation to succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-910"><span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**Fehler \_ Cluster \_ Verwenden der frei \_ gegebenen \_ Volumes- \_ API**</span><span class="sxs-lookup"><span data-stu-id="e671e-910"><span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**ERROR\_CLUSTER\_USE\_SHARED\_VOLUMES\_API**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-911">5948 (0x173c)</span><span class="sxs-lookup"><span data-stu-id="e671e-911">5948 (0x173C)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-912">Diese Gruppe oder Ressource kann nicht direkt bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-912">This group or resource cannot be directly manipulated.</span></span> <span data-ttu-id="e671e-913">Verwenden Sie APIs für freigegebene Volumes, um den gewünschten Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e671e-913">Use shared volume APIs to perform desired operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-914"><span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**Fehler \_ Cluster \_ Sicherung \_ wird \_ ausgeführt.**</span><span class="sxs-lookup"><span data-stu-id="e671e-914"><span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**ERROR\_CLUSTER\_BACKUP\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-915">5949 (0x173d)</span><span class="sxs-lookup"><span data-stu-id="e671e-915">5949 (0x173D)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-916">Die Sicherungskopie wird gerade ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e671e-916">Back up is in progress.</span></span> <span data-ttu-id="e671e-917">Warten Sie auf den Abschluss der Sicherung, und wiederholen Sie dann den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e671e-917">Please wait for backup completion before trying this operation again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-918"><span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**Fehler bei \_ nicht- \_ CSV- \_ Pfad**</span><span class="sxs-lookup"><span data-stu-id="e671e-918"><span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**ERROR\_NON\_CSV\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-919">5950 (0x173e)</span><span class="sxs-lookup"><span data-stu-id="e671e-919">5950 (0x173E)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-920">Der Pfad gehört nicht zu einem freigegebenen Cluster Volume.</span><span class="sxs-lookup"><span data-stu-id="e671e-920">The path does not belong to a cluster shared volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-921"><span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**Fehler beim \_ CSV- \_ Volume \_ nicht \_ lokal.**</span><span class="sxs-lookup"><span data-stu-id="e671e-921"><span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**ERROR\_CSV\_VOLUME\_NOT\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-922">5951 (0x173f)</span><span class="sxs-lookup"><span data-stu-id="e671e-922">5951 (0x173F)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-923">Das freigegebene Cluster Volume ist nicht lokal auf diesem Knoten eingebunden.</span><span class="sxs-lookup"><span data-stu-id="e671e-923">The cluster shared volume is not locally mounted on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-924"><span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**Fehler beim \_ Beenden des Cluster- \_ Watchdog \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-924"><span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**ERROR\_CLUSTER\_WATCHDOG\_TERMINATING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-925">5952 (0x1740)</span><span class="sxs-lookup"><span data-stu-id="e671e-925">5952 (0x1740)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-926">Der Cluster Watchdog wird beendet.</span><span class="sxs-lookup"><span data-stu-id="e671e-926">The cluster watchdog is terminating.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-927"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**Fehler beim Verschieben von nicht \_ \_ \_ \_ \_ kompatiblen \_ Knoten durch Fehler Cluster Ressource**</span><span class="sxs-lookup"><span data-stu-id="e671e-927"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_INCOMPATIBLE\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-928">5953 (0x1741)</span><span class="sxs-lookup"><span data-stu-id="e671e-928">5953 (0x1741)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-929">Eine Ressource hat einen Wechsel zwischen zwei Knoten überprüft, da Sie nicht kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="e671e-929">A resource vetoed a move between two nodes because they are incompatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-930"><span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**Fehler \_ Cluster mit \_ ungültiger \_ Knoten \_ Gewichtung**</span><span class="sxs-lookup"><span data-stu-id="e671e-930"><span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**ERROR\_CLUSTER\_INVALID\_NODE\_WEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-931">5954 (0x1742)</span><span class="sxs-lookup"><span data-stu-id="e671e-931">5954 (0x1742)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-932">Die Anforderung ist ungültig, weil die Knoten Gewichtung nicht geändert werden kann, während sich der Cluster im nur Datenträger-Quorum Modus befindet, oder weil das Ändern der Knoten Gewichtung gegen die Mindestanforderungen für das Cluster Quorum verstoßen würde.</span><span class="sxs-lookup"><span data-stu-id="e671e-932">The request is invalid either because node weight cannot be changed while the cluster is in disk-only quorum mode, or because changing the node weight would violate the minimum cluster quorum requirements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-933"><span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**Fehler bei der Überprüfung des Fehlers bei der \_ Cluster \_ Ressource. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-933"><span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-934">5955 (0x1743)</span><span class="sxs-lookup"><span data-stu-id="e671e-934">5955 (0x1743)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-935">Die Ressource hat den-Rückruf überprüft.</span><span class="sxs-lookup"><span data-stu-id="e671e-935">The resource vetoed the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-936"><span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**Fehler \_ beim resmon der \_ System \_ Ressourcen \_ .**</span><span class="sxs-lookup"><span data-stu-id="e671e-936"><span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**ERROR\_RESMON\_SYSTEM\_RESOURCES\_LACKING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-937">5956 (0x1744)</span><span class="sxs-lookup"><span data-stu-id="e671e-937">5956 (0x1744)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-938">Die Ressource konnte nicht gestartet oder ausgeführt werden, da Sie nicht genügend Systemressourcen reservieren konnte.</span><span class="sxs-lookup"><span data-stu-id="e671e-938">Resource could not start or run because it could not reserve sufficient system resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-939"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**Fehler \_ \_ \_ \_ \_ \_ \_ \_ bei der Überprüfung der Fehler Cluster Ressource auf dem \_ Ziel nicht genügend Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="e671e-939"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_NOT\_ENOUGH\_RESOURCES\_ON\_DESTINATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-940">5957 (0x1745)</span><span class="sxs-lookup"><span data-stu-id="e671e-940">5957 (0x1745)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-941">Eine Ressource hat einen Wechsel zwischen zwei Knoten überprüft, weil das Ziel derzeit nicht über genügend Ressourcen verfügt, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e671e-941">A resource vetoed a move between two nodes because the destination currently does not have enough resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-942"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**Fehler \_ \_ \_ \_ \_ \_ \_ \_ bei der Überprüfung der Fehler Cluster Ressource für die \_ Quelle nicht genügend Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="e671e-942"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_NOT\_ENOUGH\_RESOURCES\_ON\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-943">5958 (0x1746)</span><span class="sxs-lookup"><span data-stu-id="e671e-943">5958 (0x1746)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-944">Eine Ressource hat einen Wechsel zwischen zwei Knoten überprüft, da die Quelle derzeit nicht über genügend Ressourcen verfügt, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e671e-944">A resource vetoed a move between two nodes because the source currently does not have enough resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-945"><span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**Fehler \_ Cluster \_ Gruppe in \_ Warteschlange eingereiht**</span><span class="sxs-lookup"><span data-stu-id="e671e-945"><span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**ERROR\_CLUSTER\_GROUP\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-946">5959 (0x1747)</span><span class="sxs-lookup"><span data-stu-id="e671e-946">5959 (0x1747)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-947">Der angeforderte Vorgang kann nicht abgeschlossen werden, da die Gruppe für einen Vorgang in die Warteschlange eingereiht wird.</span><span class="sxs-lookup"><span data-stu-id="e671e-947">The requested operation can not be completed because the group is queued for an operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-948"><span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**Fehler \_ beim \_ \_ gesperrten \_ Status der Cluster Ressource.**</span><span class="sxs-lookup"><span data-stu-id="e671e-948"><span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**ERROR\_CLUSTER\_RESOURCE\_LOCKED\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-949">5960 (0x1748)</span><span class="sxs-lookup"><span data-stu-id="e671e-949">5960 (0x1748)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-950">Der angeforderte Vorgang kann nicht abgeschlossen werden, da eine Ressource den gesperrten Status aufweist.</span><span class="sxs-lookup"><span data-stu-id="e671e-950">The requested operation can not be completed because a resource has locked status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-951"><span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**Failover für frei gegebenes \_ Cluster \_ \_ Volume \_ \_ nicht \_ zulässig**</span><span class="sxs-lookup"><span data-stu-id="e671e-951"><span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_FAILOVER\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-952">5961 (0x1749)</span><span class="sxs-lookup"><span data-stu-id="e671e-952">5961 (0x1749)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-953">Die Ressource kann nicht auf einen anderen Knoten verschoben werden, da ein frei gegebenes Cluster Volume den Vorgang überprüft hat.</span><span class="sxs-lookup"><span data-stu-id="e671e-953">The resource cannot move to another node because a cluster shared volume vetoed the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-954"><span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**Fehler \_ \_ \_ \_ beim Entladen des Cluster Knotens. \_**</span><span class="sxs-lookup"><span data-stu-id="e671e-954"><span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**ERROR\_CLUSTER\_NODE\_DRAIN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-955">5962 (0x174a)</span><span class="sxs-lookup"><span data-stu-id="e671e-955">5962 (0x174A)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-956">Ein Knoten Ausgleichs Vorgang wird bereits ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e671e-956">A node drain is already in progress.</span></span>

<span data-ttu-id="e671e-957">Dieser Wert wurde auch als **Fehler \_ Cluster \_ Knoten \_ - \_ Evakuierung \_ in** Bearbeitung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e671e-957">This value was also named **ERROR\_CLUSTER\_NODE\_EVACUATION\_IN\_PROGRESS**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-958"><span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**Fehler Cluster Datenträger \_ \_ \_ nicht \_ verbunden**</span><span class="sxs-lookup"><span data-stu-id="e671e-958"><span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**ERROR\_CLUSTER\_DISK\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-959">5963 (0x174b)</span><span class="sxs-lookup"><span data-stu-id="e671e-959">5963 (0x174B)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-960">Der Cluster Speicher ist nicht mit dem Knoten verbunden.</span><span class="sxs-lookup"><span data-stu-id="e671e-960">Clustered storage is not connected to the node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-961"><span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**Fehler Datenträger \_ \_ nicht \_ CSV- \_ fähig**</span><span class="sxs-lookup"><span data-stu-id="e671e-961"><span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**ERROR\_DISK\_NOT\_CSV\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-962">5964 (0x174c)</span><span class="sxs-lookup"><span data-stu-id="e671e-962">5964 (0x174C)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-963">Der Datenträger ist nicht so konfiguriert, dass er mit CSV verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e671e-963">The disk is not configured in a way to be used with CSV.</span></span> <span data-ttu-id="e671e-964">CSV-Datenträger müssen über mindestens eine Partition verfügen, die mit NTFS formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-964">CSV disks must have at least one partition that is formatted with NTFS.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-965"><span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**Fehler \_ Ressource \_ nicht \_ im \_ verfügbaren \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="e671e-965"><span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**ERROR\_RESOURCE\_NOT\_IN\_AVAILABLE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-966">5965 (0x174d)</span><span class="sxs-lookup"><span data-stu-id="e671e-966">5965 (0x174D)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-967">Die Ressource muss Teil der verfügbaren Speicher Gruppe sein, um diese Aktion abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e671e-967">The resource must be part of the Available Storage group to complete this action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-968"><span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**fehlerfrei gegebenes \_ Cluster \_ \_ Volume \_ umgeleitet**</span><span class="sxs-lookup"><span data-stu-id="e671e-968"><span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-969">5966 (0x174e)</span><span class="sxs-lookup"><span data-stu-id="e671e-969">5966 (0x174E)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-970">Fehler bei csvfs-Vorgang, weil sich das Volume im umgeleiteten Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="e671e-970">CSVFS failed operation as volume is in redirected mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-971"><span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**fehlerfrei gegebenes \_ Cluster \_ \_ Volume \_ nicht \_ umgeleitet**</span><span class="sxs-lookup"><span data-stu-id="e671e-971"><span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_NOT\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-972">5967 (0x174f)</span><span class="sxs-lookup"><span data-stu-id="e671e-972">5967 (0x174F)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-973">Fehler bei csvfs-Vorgang, weil sich das Volume nicht im umgeleiteten Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="e671e-973">CSVFS failed operation as volume is not in redirected mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-974"><span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**Fehler \_ Cluster \_ kann \_ keine \_ Eigenschaften zurückgeben.**</span><span class="sxs-lookup"><span data-stu-id="e671e-974"><span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**ERROR\_CLUSTER\_CANNOT\_RETURN\_PROPERTIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-975">5968 (0x1750)</span><span class="sxs-lookup"><span data-stu-id="e671e-975">5968 (0x1750)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-976">Cluster Eigenschaften können zurzeit nicht zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-976">Cluster properties cannot be returned at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-977"><span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**Fehler \_ Cluster \_ Ressource \_ enthält \_ nicht unterstützten Vergleichs \_ \_ Bereich \_ für frei \_ gegebene \_ Volumes**</span><span class="sxs-lookup"><span data-stu-id="e671e-977"><span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**ERROR\_CLUSTER\_RESOURCE\_CONTAINS\_UNSUPPORTED\_DIFF\_AREA\_FOR\_SHARED\_VOLUMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-978">5969 (0x1751)</span><span class="sxs-lookup"><span data-stu-id="e671e-978">5969 (0x1751)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-979">Die geclusterte Datenträger Ressource enthält den Bereich für Software Momentaufnahme-Vergleiche, der für freigegebene Clustervolumes nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e671e-979">The clustered disk resource contains software snapshot diff area that are not supported for Cluster Shared Volumes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-980"><span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**Fehler \_ Cluster \_ Ressource \_ befindet sich \_ im \_ Wartungs \_ Modus**</span><span class="sxs-lookup"><span data-stu-id="e671e-980"><span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**ERROR\_CLUSTER\_RESOURCE\_IS\_IN\_MAINTENANCE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-981">5970 (0x1752)</span><span class="sxs-lookup"><span data-stu-id="e671e-981">5970 (0x1752)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-982">Der Vorgang kann nicht abgeschlossen werden, da sich die Ressource im Wartungsmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="e671e-982">The operation cannot be completed because the resource is in maintenance mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-983"><span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**Fehler \_ Cluster- \_ Affinitäts \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="e671e-983"><span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**ERROR\_CLUSTER\_AFFINITY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-984">5971 (0x1753)</span><span class="sxs-lookup"><span data-stu-id="e671e-984">5971 (0x1753)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-985">Der Vorgang kann aufgrund von Cluster Affinitäts Konflikten nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="e671e-985">The operation cannot be completed because of cluster affinity conflicts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e671e-986"><span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**Fehler \_ Cluster \_ Ressource \_ ist \_ \_ virtuelle \_ Replikat Maschine**</span><span class="sxs-lookup"><span data-stu-id="e671e-986"><span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**ERROR\_CLUSTER\_RESOURCE\_IS\_REPLICA\_VIRTUAL\_MACHINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e671e-987">5972 (0x1754)</span><span class="sxs-lookup"><span data-stu-id="e671e-987">5972 (0x1754)</span></span>
</dt> <dt>



<span data-ttu-id="e671e-988">Der Vorgang kann nicht abgeschlossen werden, da die Ressource ein virtueller Replikat Computer ist.</span><span class="sxs-lookup"><span data-stu-id="e671e-988">The operation cannot be completed because the resource is a replica virtual machine.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="e671e-989">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e671e-989">Requirements</span></span>



| <span data-ttu-id="e671e-990">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e671e-990">Requirement</span></span> | <span data-ttu-id="e671e-991">Wert</span><span class="sxs-lookup"><span data-stu-id="e671e-991">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e671e-992">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e671e-992">Minimum supported client</span></span><br/> | <span data-ttu-id="e671e-993">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e671e-993">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e671e-994">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e671e-994">Minimum supported server</span></span><br/> | <span data-ttu-id="e671e-995">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e671e-995">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e671e-996">Header</span><span class="sxs-lookup"><span data-stu-id="e671e-996">Header</span></span><br/>                   | <dl> <span data-ttu-id="e671e-997"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="e671e-997"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e671e-998">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e671e-998">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e671e-999">System Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="e671e-999">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




