---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 1000-1299 und ist für Entwickler bestimmt.
ms.assetid: 0061feb6-e1a0-4fcd-8f80-954087c799d7
title: System Fehler Codes (1000-1299) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 592bd5c6653526d87fed05d6ec76f739355ae359
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523715"
---
# <a name="system-error-codes-1000-1299"></a><span data-ttu-id="6c758-103">System Fehler Codes (1000-1299)</span><span class="sxs-lookup"><span data-stu-id="6c758-103">System Error Codes (1000-1299)</span></span>

> [!NOTE]
> <span data-ttu-id="6c758-104">Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen.</span><span class="sxs-lookup"><span data-stu-id="6c758-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="6c758-105">Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="6c758-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="6c758-106">In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) für die Fehler 1000 bis 1299 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6c758-106">The following list describes [system error codes](system-error-codes.md) for errors 1000 to 1299.</span></span> <span data-ttu-id="6c758-107">Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="6c758-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="6c758-108">Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".</span><span class="sxs-lookup"><span data-stu-id="6c758-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="6c758-109"><span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**Fehler \_ Stapel \_ Überlauf**</span><span class="sxs-lookup"><span data-stu-id="6c758-109"><span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**ERROR\_STACK\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-110">1001 (0x3e9)</span><span class="sxs-lookup"><span data-stu-id="6c758-110">1001 (0x3E9)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-111">Rekursion zu tief Überlauf des Stapels.</span><span class="sxs-lookup"><span data-stu-id="6c758-111">Recursion too deep; the stack overflowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-112"><span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**\_ungültige \_ Meldung für Fehler**</span><span class="sxs-lookup"><span data-stu-id="6c758-112"><span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**ERROR\_INVALID\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-113">1002 (0x3ea)</span><span class="sxs-lookup"><span data-stu-id="6c758-113">1002 (0x3EA)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-114">Das Fenster kann nicht für die gesendete Nachricht fungieren.</span><span class="sxs-lookup"><span data-stu-id="6c758-114">The window cannot act on the sent message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-115"><span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**der Fehler \_ kann \_ nicht \_ vervollständigt werden.**</span><span class="sxs-lookup"><span data-stu-id="6c758-115"><span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**ERROR\_CAN\_NOT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-116">1003 (0x3eb)</span><span class="sxs-lookup"><span data-stu-id="6c758-116">1003 (0x3EB)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-117">Diese Funktion kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-117">Cannot complete this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-118"><span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**\_ungültige \_ Flags.**</span><span class="sxs-lookup"><span data-stu-id="6c758-118"><span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-119">1004 (0x3ec)</span><span class="sxs-lookup"><span data-stu-id="6c758-119">1004 (0x3EC)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-120">Ungültige Flags.</span><span class="sxs-lookup"><span data-stu-id="6c758-120">Invalid flags.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-121"><span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**Fehler \_ unbekanntes \_ Volume**</span><span class="sxs-lookup"><span data-stu-id="6c758-121"><span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**ERROR\_UNRECOGNIZED\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-122">1005 (0x3ed)</span><span class="sxs-lookup"><span data-stu-id="6c758-122">1005 (0x3ED)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-123">Das Volume enthält kein bekanntes Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="6c758-123">The volume does not contain a recognized file system.</span></span> <span data-ttu-id="6c758-124">Stellen Sie sicher, dass alle erforderlichen Dateisystem Treiber geladen sind und das Volume nicht beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="6c758-124">Please make sure that all required file system drivers are loaded and that the volume is not corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-125"><span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**Fehler \_ Datei \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="6c758-125"><span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**ERROR\_FILE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-126">1006 (0x3EE)</span><span class="sxs-lookup"><span data-stu-id="6c758-126">1006 (0x3EE)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-127">Das Volume für eine Datei wurde extern geändert, sodass die geöffnete Datei nicht mehr gültig ist.</span><span class="sxs-lookup"><span data-stu-id="6c758-127">The volume for a file has been externally altered so that the opened file is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-128"><span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**Fehler im \_ voll Bild \_ Modus**</span><span class="sxs-lookup"><span data-stu-id="6c758-128"><span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**ERROR\_FULLSCREEN\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-129">1007 (0x3ef)</span><span class="sxs-lookup"><span data-stu-id="6c758-129">1007 (0x3EF)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-130">Der angeforderte Vorgang kann nicht im Vollbildmodus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-130">The requested operation cannot be performed in full-screen mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-131"><span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**Fehler \_ ohne \_ Token**</span><span class="sxs-lookup"><span data-stu-id="6c758-131"><span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**ERROR\_NO\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-132">1008 (0x3f 0)</span><span class="sxs-lookup"><span data-stu-id="6c758-132">1008 (0x3F0)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-133">Es wurde versucht, auf ein nicht vorhandenes Token zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="6c758-133">An attempt was made to reference a token that does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-134"><span id="ERROR_BADDB"></span><span id="error_baddb"></span>**Fehler \_ baddb**</span><span class="sxs-lookup"><span data-stu-id="6c758-134"><span id="ERROR_BADDB"></span><span id="error_baddb"></span>**ERROR\_BADDB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-135">1009 (0x3f 1)</span><span class="sxs-lookup"><span data-stu-id="6c758-135">1009 (0x3F1)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-136">Die Konfigurations Registrierungsdatenbank ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6c758-136">The configuration registry database is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-137"><span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**Fehler \_ badkey**</span><span class="sxs-lookup"><span data-stu-id="6c758-137"><span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**ERROR\_BADKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-138">1010 (0x3f 2)</span><span class="sxs-lookup"><span data-stu-id="6c758-138">1010 (0x3F2)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-139">Der Konfigurations Registrierungsschlüssel ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c758-139">The configuration registry key is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-140"><span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**Fehler- \_ cantopen**</span><span class="sxs-lookup"><span data-stu-id="6c758-140"><span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**ERROR\_CANTOPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-141">1011 (0x3f)</span><span class="sxs-lookup"><span data-stu-id="6c758-141">1011 (0x3F3)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-142">Der Konfigurations Registrierungsschlüssel konnte nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-142">The configuration registry key could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-143"><span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**Fehler- \_ cantread**</span><span class="sxs-lookup"><span data-stu-id="6c758-143"><span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**ERROR\_CANTREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-144">1012 (0x3f 4)</span><span class="sxs-lookup"><span data-stu-id="6c758-144">1012 (0x3F4)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-145">Der Konfigurations Registrierungsschlüssel konnte nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-145">The configuration registry key could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-146"><span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**Fehler beim \_ kanschreiben**</span><span class="sxs-lookup"><span data-stu-id="6c758-146"><span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**ERROR\_CANTWRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-147">1013 (0x3f)</span><span class="sxs-lookup"><span data-stu-id="6c758-147">1013 (0x3F5)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-148">Der Konfigurations Registrierungsschlüssel konnte nicht geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-148">The configuration registry key could not be written.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-149"><span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**Fehler \_ Registrierung \_ wieder hergestellt**</span><span class="sxs-lookup"><span data-stu-id="6c758-149"><span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**ERROR\_REGISTRY\_RECOVERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-150">1014 (0x3f)</span><span class="sxs-lookup"><span data-stu-id="6c758-150">1014 (0x3F6)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-151">Eine der Dateien in der Registrierungsdatenbank musste mithilfe eines Protokolls oder einer alternativen Kopie wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-151">One of the files in the registry database had to be recovered by use of a log or alternate copy.</span></span> <span data-ttu-id="6c758-152">Die Wiederherstellung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6c758-152">The recovery was successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-153"><span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**Fehler \_ Registrierung \_ beschädigt**</span><span class="sxs-lookup"><span data-stu-id="6c758-153"><span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**ERROR\_REGISTRY\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-154">1015 (0x3f)</span><span class="sxs-lookup"><span data-stu-id="6c758-154">1015 (0x3F7)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-155">Die Registrierung ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6c758-155">The registry is corrupted.</span></span> <span data-ttu-id="6c758-156">Die Struktur einer der Dateien, die Registrierungsdaten enthalten, ist beschädigt, oder das Speicher Abbild des Systems der Datei ist beschädigt, oder die Datei konnte nicht wieder hergestellt werden, da die Alternative Kopie oder das alternative Protokoll nicht vorhanden oder beschädigt war.</span><span class="sxs-lookup"><span data-stu-id="6c758-156">The structure of one of the files containing registry data is corrupted, or the system's memory image of the file is corrupted, or the file could not be recovered because the alternate copy or log was absent or corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-157"><span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**Fehler Registrierungs-e/a Fehler \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-157"><span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**ERROR\_REGISTRY\_IO\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-158">1016 (0x3f 8)</span><span class="sxs-lookup"><span data-stu-id="6c758-158">1016 (0x3F8)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-159">Ein e/a-Vorgang, der von der Registrierung initiiert wurde, ist nicht wiederherstellbar.</span><span class="sxs-lookup"><span data-stu-id="6c758-159">An I/O operation initiated by the registry failed unrecoverably.</span></span> <span data-ttu-id="6c758-160">Eine der Dateien, die das System Abbild der Registrierung enthalten, konnte von der Registrierung nicht gelesen, geschrieben oder geleert werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-160">The registry could not read in, or write out, or flush, one of the files that contain the system's image of the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-161"><span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**Fehler bei der \_ \_ Registrierungs \_ Datei.**</span><span class="sxs-lookup"><span data-stu-id="6c758-161"><span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**ERROR\_NOT\_REGISTRY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-162">1017 (0x3f 9)</span><span class="sxs-lookup"><span data-stu-id="6c758-162">1017 (0x3F9)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-163">Das System hat versucht, eine Datei in die Registrierung zu laden oder wiederherzustellen, aber die angegebene Datei weist nicht das Registrierungsdatei Format auf.</span><span class="sxs-lookup"><span data-stu-id="6c758-163">The system has attempted to load or restore a file into the registry, but the specified file is not in a registry file format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-164"><span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**Fehler \_ Schlüssel \_ gelöscht**</span><span class="sxs-lookup"><span data-stu-id="6c758-164"><span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**ERROR\_KEY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-165">1018 (0x3fa)</span><span class="sxs-lookup"><span data-stu-id="6c758-165">1018 (0x3FA)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-166">Ungültiger Vorgang für einen Registrierungsschlüssel, der zum Löschen markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6c758-166">Illegal operation attempted on a registry key that has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-167"><span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**Fehler \_ ohne \_ Protokoll \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="6c758-167"><span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**ERROR\_NO\_LOG\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-168">1019 (0x3fb)</span><span class="sxs-lookup"><span data-stu-id="6c758-168">1019 (0x3FB)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-169">Das System konnte den erforderlichen Speicherplatz nicht in einem Registrierungs Protokoll zuordnen.</span><span class="sxs-lookup"><span data-stu-id="6c758-169">System could not allocate the required space in a registry log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-170"><span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**Fehler \_ Schlüssel \_ hat untergeordnete Elemente \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-170"><span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**ERROR\_KEY\_HAS\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-171">1020 (0x3fc)</span><span class="sxs-lookup"><span data-stu-id="6c758-171">1020 (0x3FC)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-172">In einem Registrierungsschlüssel, der bereits über Unterschlüssel oder Werte verfügt, kann keine symbolische Verknüpfung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-172">Cannot create a symbolic link in a registry key that already has subkeys or values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-173"><span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**Fehler untergeordnetes Element \_ \_ muss \_ \_ flüchtig sein**</span><span class="sxs-lookup"><span data-stu-id="6c758-173"><span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**ERROR\_CHILD\_MUST\_BE\_VOLATILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-174">1021 (0x3fd)</span><span class="sxs-lookup"><span data-stu-id="6c758-174">1021 (0x3FD)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-175">Unter einem flüchtigen übergeordneten Schlüssel kann kein stabiler Unterschlüssel erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-175">Cannot create a stable subkey under a volatile parent key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-176"><span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**Fehler beim einschließen der Aufzählung. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-176"><span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**ERROR\_NOTIFY\_ENUM\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-177">1022 (0x3fe)</span><span class="sxs-lookup"><span data-stu-id="6c758-177">1022 (0x3FE)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-178">Ein Benachrichtigungs Change Request wird abgeschlossen, und die Informationen werden nicht im Puffer des Aufrufers zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c758-178">A notify change request is being completed and the information is not being returned in the caller's buffer.</span></span> <span data-ttu-id="6c758-179">Der Aufrufer muss nun die Dateien aufzählen, um die Änderungen zu finden.</span><span class="sxs-lookup"><span data-stu-id="6c758-179">The caller now needs to enumerate the files to find the changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-180"><span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**Fehler \_ abhängige \_ Dienste werden \_ ausgeführt.**</span><span class="sxs-lookup"><span data-stu-id="6c758-180"><span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**ERROR\_DEPENDENT\_SERVICES\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-181">1051 (0x41b)</span><span class="sxs-lookup"><span data-stu-id="6c758-181">1051 (0x41B)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-182">Ein Steuerelement für die Beendigung wurde an einen Dienst gesendet, von dem andere ausgelaufende Dienste abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="6c758-182">A stop control has been sent to a service that other running services are dependent on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-183"><span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**\_ungültige \_ Dienst \_ Kontrolle.**</span><span class="sxs-lookup"><span data-stu-id="6c758-183"><span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**ERROR\_INVALID\_SERVICE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-184">1052 (0x41c)</span><span class="sxs-lookup"><span data-stu-id="6c758-184">1052 (0x41C)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-185">Das angeforderte Steuerelement ist für diesen Dienst ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c758-185">The requested control is not valid for this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-186"><span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**Timeout für Fehler \_ Dienst \_ Anforderung \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-186"><span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**ERROR\_SERVICE\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-187">1053 (0x41d)</span><span class="sxs-lookup"><span data-stu-id="6c758-187">1053 (0x41D)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-188">Der Dienst antwortete nicht rechtzeitig auf die Start- oder Steuerungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="6c758-188">The service did not respond to the start or control request in a timely fashion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-189"><span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**Fehler \_ Dienst \_ ohne \_ Thread**</span><span class="sxs-lookup"><span data-stu-id="6c758-189"><span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**ERROR\_SERVICE\_NO\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-190">1054 (0x41e)</span><span class="sxs-lookup"><span data-stu-id="6c758-190">1054 (0x41E)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-191">Für den Dienst konnte kein Thread erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-191">A thread could not be created for the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-192"><span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**Fehler \_ Dienst \_ Datenbank \_ gesperrt**</span><span class="sxs-lookup"><span data-stu-id="6c758-192"><span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**ERROR\_SERVICE\_DATABASE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-193">1055 (0x41f)</span><span class="sxs-lookup"><span data-stu-id="6c758-193">1055 (0x41F)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-194">Die Dienst Datenbank ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="6c758-194">The service database is locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-195"><span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**der Fehler \_ Dienst wird \_ bereits \_ ausgeführt.**</span><span class="sxs-lookup"><span data-stu-id="6c758-195"><span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**ERROR\_SERVICE\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-196">1056 (0x420)</span><span class="sxs-lookup"><span data-stu-id="6c758-196">1056 (0x420)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-197">Eine Instanz des Dienstanbieter wird bereits ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c758-197">An instance of the service is already running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-198"><span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**\_ungültiges \_ Dienst \_ Konto.**</span><span class="sxs-lookup"><span data-stu-id="6c758-198"><span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**ERROR\_INVALID\_SERVICE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-199">1057 (0x421)</span><span class="sxs-lookup"><span data-stu-id="6c758-199">1057 (0x421)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-200">Der Kontoname ist ungültig oder nicht vorhanden, oder das Kennwort für den angegebenen Kontonamen ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c758-200">The account name is invalid or does not exist, or the password is invalid for the account name specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-201"><span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**Fehler \_ Dienst \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="6c758-201"><span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**ERROR\_SERVICE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-202">1058 (0x422)</span><span class="sxs-lookup"><span data-stu-id="6c758-202">1058 (0x422)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-203">Der Dienst kann nicht gestartet werden, weil er deaktiviert wurde oder weil ihm keine aktivierten Geräte zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6c758-203">The service cannot be started, either because it is disabled or because it has no enabled devices associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-204"><span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**Fehler \_ zirkuläre \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="6c758-204"><span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**ERROR\_CIRCULAR\_DEPENDENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-205">1059 (0x423)</span><span class="sxs-lookup"><span data-stu-id="6c758-205">1059 (0x423)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-206">Es wurde eine zirkuläre Dienst Abhängigkeit angegeben.</span><span class="sxs-lookup"><span data-stu-id="6c758-206">Circular service dependency was specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-207"><span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**der Fehler \_ Dienst \_ ist \_ nicht \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="6c758-207"><span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**ERROR\_SERVICE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-208">1060 (0x424)</span><span class="sxs-lookup"><span data-stu-id="6c758-208">1060 (0x424)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-209">Der angegebene Dienst ist nicht als installierter Dienst vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6c758-209">The specified service does not exist as an installed service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-210"><span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**Fehler \_ Dienst \_ kann \_ STRG nicht akzeptieren \_ .**</span><span class="sxs-lookup"><span data-stu-id="6c758-210"><span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**ERROR\_SERVICE\_CANNOT\_ACCEPT\_CTRL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-211">1061 (0x425)</span><span class="sxs-lookup"><span data-stu-id="6c758-211">1061 (0x425)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-212">Der Dienst kann zurzeit keine Steuerungs Meldungen akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="6c758-212">The service cannot accept control messages at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-213"><span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**Fehler \_ Dienst \_ nicht \_ aktiv**</span><span class="sxs-lookup"><span data-stu-id="6c758-213"><span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**ERROR\_SERVICE\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-214">1062 (0x426)</span><span class="sxs-lookup"><span data-stu-id="6c758-214">1062 (0x426)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-215">Der Dienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="6c758-215">The service has not been started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-216"><span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**Fehler \_ bei \_ Dienst \_ Controller \_ Verbindung.**</span><span class="sxs-lookup"><span data-stu-id="6c758-216"><span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**ERROR\_FAILED\_SERVICE\_CONTROLLER\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-217">1063 (0x427)</span><span class="sxs-lookup"><span data-stu-id="6c758-217">1063 (0x427)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-218">Vom Dienst Prozess konnte keine Verbindung mit dem Dienst Controller hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-218">The service process could not connect to the service controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-219"><span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**Fehler \_ Ausnahme \_ im \_ Dienst.**</span><span class="sxs-lookup"><span data-stu-id="6c758-219"><span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**ERROR\_EXCEPTION\_IN\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-220">1064 (0x428)</span><span class="sxs-lookup"><span data-stu-id="6c758-220">1064 (0x428)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-221">Beim Verarbeiten der Steuerungs Anforderung ist eine Ausnahme im Dienst aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6c758-221">An exception occurred in the service when handling the control request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-222"><span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**Fehler \_ Datenbank \_ ist \_ nicht \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="6c758-222"><span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**ERROR\_DATABASE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-223">1065 (0x429)</span><span class="sxs-lookup"><span data-stu-id="6c758-223">1065 (0x429)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-224">Die angegebene Datenbank ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6c758-224">The database specified does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-225"><span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**Fehler \_ Dienst \_ spezifischer \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="6c758-225"><span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**ERROR\_SERVICE\_SPECIFIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-226">1066 (0x42a)</span><span class="sxs-lookup"><span data-stu-id="6c758-226">1066 (0x42A)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-227">Der Dienst hat einen Dienst spezifischen Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c758-227">The service has returned a service-specific error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-228"><span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**Fehler \_ Prozess \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="6c758-228"><span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**ERROR\_PROCESS\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-229">1067 (0x42b)</span><span class="sxs-lookup"><span data-stu-id="6c758-229">1067 (0x42B)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-230">Der Prozess wurde unerwartet beendet.</span><span class="sxs-lookup"><span data-stu-id="6c758-230">The process terminated unexpectedly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-231"><span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**Fehler \_ Dienst- \_ Abhängigkeitsfehler \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-231"><span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**ERROR\_SERVICE\_DEPENDENCY\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-232">1068 (0x42c)</span><span class="sxs-lookup"><span data-stu-id="6c758-232">1068 (0x42C)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-233">Der Abhängigkeits Dienst oder die Abhängigkeits Gruppe konnte nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-233">The dependency service or group failed to start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-234"><span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**Fehler beim Anmelden des Fehler \_ Diensts \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-234"><span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**ERROR\_SERVICE\_LOGON\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-235">1069 (0x42d)</span><span class="sxs-lookup"><span data-stu-id="6c758-235">1069 (0x42D)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-236">Der Dienst konnte wegen einer fehlerhaften Anmeldung nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-236">The service did not start due to a logon failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-237"><span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**Fehler \_ beim \_ Starten des dienstanhangs \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-237"><span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**ERROR\_SERVICE\_START\_HANG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-238">1070 (0x42e)</span><span class="sxs-lookup"><span data-stu-id="6c758-238">1070 (0x42E)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-239">Nachdem der Dienst gestartet wurde, hat der Dienst nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="6c758-239">After starting, the service hung in a start-pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-240"><span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**\_ungültige \_ Dienst \_ Sperre.**</span><span class="sxs-lookup"><span data-stu-id="6c758-240"><span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**ERROR\_INVALID\_SERVICE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-241">1071 (0x42f)</span><span class="sxs-lookup"><span data-stu-id="6c758-241">1071 (0x42F)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-242">Die angegebene Dienst Datenbanksperre ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c758-242">The specified service database lock is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-243"><span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**der Fehler \_ Dienst wurde \_ \_ zum \_ Löschen markiert.**</span><span class="sxs-lookup"><span data-stu-id="6c758-243"><span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**ERROR\_SERVICE\_MARKED\_FOR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-244">1072 (0x430)</span><span class="sxs-lookup"><span data-stu-id="6c758-244">1072 (0x430)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-245">Der angegebene Dienst wurde zum Löschen markiert.</span><span class="sxs-lookup"><span data-stu-id="6c758-245">The specified service has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-246"><span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**Fehler \_ Dienst \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="6c758-246"><span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**ERROR\_SERVICE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-247">1073 (0x431)</span><span class="sxs-lookup"><span data-stu-id="6c758-247">1073 (0x431)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-248">Der angegebene Dienst ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6c758-248">The specified service already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-249"><span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**Fehler \_ beim \_ Ausführen von \_ LKG.**</span><span class="sxs-lookup"><span data-stu-id="6c758-249"><span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**ERROR\_ALREADY\_RUNNING\_LKG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-250">1074 (0x432)</span><span class="sxs-lookup"><span data-stu-id="6c758-250">1074 (0x432)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-251">Das System wird zurzeit mit der zuletzt bekannten, ordnungsgemäßen Konfiguration ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c758-251">The system is currently running with the last-known-good configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-252"><span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**Fehler \_ Dienst \_ Abhängigkeit \_ gelöscht**</span><span class="sxs-lookup"><span data-stu-id="6c758-252"><span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**ERROR\_SERVICE\_DEPENDENCY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-253">1075 (0x433)</span><span class="sxs-lookup"><span data-stu-id="6c758-253">1075 (0x433)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-254">Der Abhängigkeits Dienst ist nicht vorhanden oder wurde zum Löschen markiert.</span><span class="sxs-lookup"><span data-stu-id="6c758-254">The dependency service does not exist or has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-255"><span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**Fehler beim \_ Start \_ bereits \_ akzeptiert.**</span><span class="sxs-lookup"><span data-stu-id="6c758-255"><span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**ERROR\_BOOT\_ALREADY\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-256">1076 (0x434)</span><span class="sxs-lookup"><span data-stu-id="6c758-256">1076 (0x434)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-257">Der aktuelle Start wurde bereits für die Verwendung als zuletzt bekannter, funktionierendes Steuerelement akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="6c758-257">The current boot has already been accepted for use as the last-known-good control set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-258"><span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**Fehler \_ Dienst wurde \_ nie \_ gestartet.**</span><span class="sxs-lookup"><span data-stu-id="6c758-258"><span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**ERROR\_SERVICE\_NEVER\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-259">1077 (0x435)</span><span class="sxs-lookup"><span data-stu-id="6c758-259">1077 (0x435)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-260">Seit dem letzten Start wurden keine Versuche unternommen, den Dienst zu starten.</span><span class="sxs-lookup"><span data-stu-id="6c758-260">No attempts to start the service have been made since the last boot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-261"><span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**Fehler beim \_ doppelten \_ Dienst \_ Namen.**</span><span class="sxs-lookup"><span data-stu-id="6c758-261"><span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**ERROR\_DUPLICATE\_SERVICE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-262">1078 (0x436)</span><span class="sxs-lookup"><span data-stu-id="6c758-262">1078 (0x436)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-263">Der Name wird bereits als Dienst Name oder Dienst Anzeige Name verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c758-263">The name is already in use as either a service name or a service display name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-264"><span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**Fehler \_ anderes \_ Dienst \_ Konto**</span><span class="sxs-lookup"><span data-stu-id="6c758-264"><span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**ERROR\_DIFFERENT\_SERVICE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-265">1079 (0x437)</span><span class="sxs-lookup"><span data-stu-id="6c758-265">1079 (0x437)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-266">Das für diesen Dienst angegebene Konto unterscheidet sich von dem Konto, das für andere Dienste angegeben wurde, die im selben Prozess ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-266">The account specified for this service is different from the account specified for other services running in the same process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-267"><span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**Fehler \_ beim \_ Erkennen des \_ Treiber \_ Fehlers.**</span><span class="sxs-lookup"><span data-stu-id="6c758-267"><span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**ERROR\_CANNOT\_DETECT\_DRIVER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-268">1080 (0x438)</span><span class="sxs-lookup"><span data-stu-id="6c758-268">1080 (0x438)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-269">Fehler Aktionen können nur für Win32-Dienste, nicht für Treiber, festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-269">Failure actions can only be set for Win32 services, not for drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-270"><span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**Fehler \_ beim \_ Erkennen des \_ Prozess \_ Abbruchs.**</span><span class="sxs-lookup"><span data-stu-id="6c758-270"><span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**ERROR\_CANNOT\_DETECT\_PROCESS\_ABORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-271">1081 (0x439)</span><span class="sxs-lookup"><span data-stu-id="6c758-271">1081 (0x439)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-272">Dieser Dienst wird in demselben Prozess wie der Dienststeuerungs-Manager ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c758-272">This service runs in the same process as the service control manager.</span></span> <span data-ttu-id="6c758-273">Daher kann der Dienststeuerungs-Manager keine Maßnahmen ergreifen, wenn dieser Dienst Prozess unerwartet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="6c758-273">Therefore, the service control manager cannot take action if this service's process terminates unexpectedly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-274"><span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**Fehler " \_ kein \_ Wiederherstellungs \_ Programm"**</span><span class="sxs-lookup"><span data-stu-id="6c758-274"><span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**ERROR\_NO\_RECOVERY\_PROGRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-275">1082 (0x43a)</span><span class="sxs-lookup"><span data-stu-id="6c758-275">1082 (0x43A)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-276">Es wurde kein Wiederherstellungsprogramm für diesen Dienst konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6c758-276">No recovery program has been configured for this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-277"><span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**Fehler \_ Dienst \_ nicht \_ in \_ exe**</span><span class="sxs-lookup"><span data-stu-id="6c758-277"><span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**ERROR\_SERVICE\_NOT\_IN\_EXE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-278">1083 (0x43b)</span><span class="sxs-lookup"><span data-stu-id="6c758-278">1083 (0x43B)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-279">Das ausführbare Programm, mit dem dieser Dienst für die Durchführung konfiguriert ist, implementiert den Dienst nicht.</span><span class="sxs-lookup"><span data-stu-id="6c758-279">The executable program that this service is configured to run in does not implement the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-280"><span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**Fehler \_ beim \_ SafeBoot- \_ Dienst.**</span><span class="sxs-lookup"><span data-stu-id="6c758-280"><span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**ERROR\_NOT\_SAFEBOOT\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-281">1084 (0x43c)</span><span class="sxs-lookup"><span data-stu-id="6c758-281">1084 (0x43C)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-282">Dieser Dienst kann nicht im abgesicherten Modus gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-282">This service cannot be started in Safe Mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-283"><span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**Fehler \_ Ende \_ des \_ Mediums**</span><span class="sxs-lookup"><span data-stu-id="6c758-283"><span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**ERROR\_END\_OF\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-284">1100 (0x44c)</span><span class="sxs-lookup"><span data-stu-id="6c758-284">1100 (0x44C)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-285">Das physische Ende des Bands wurde erreicht.</span><span class="sxs-lookup"><span data-stu-id="6c758-285">The physical end of the tape has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-286"><span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**Fehler \_ Datei Markierung \_ erkannt**</span><span class="sxs-lookup"><span data-stu-id="6c758-286"><span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**ERROR\_FILEMARK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-287">1101 (0x44d)</span><span class="sxs-lookup"><span data-stu-id="6c758-287">1101 (0x44D)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-288">Ein Band Zugriff hat ein Datei Zeichen erreicht.</span><span class="sxs-lookup"><span data-stu-id="6c758-288">A tape access reached a filemark.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-289"><span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**Fehler beim \_ Start \_ des \_ Mediums.**</span><span class="sxs-lookup"><span data-stu-id="6c758-289"><span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**ERROR\_BEGINNING\_OF\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-290">1102 (0x44e)</span><span class="sxs-lookup"><span data-stu-id="6c758-290">1102 (0x44E)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-291">Der Anfang des Bands oder eine Partition wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6c758-291">The beginning of the tape or a partition was encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-292"><span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**Fehler- \_ setmark \_ erkannt**</span><span class="sxs-lookup"><span data-stu-id="6c758-292"><span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**ERROR\_SETMARK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-293">1103 (0x44f)</span><span class="sxs-lookup"><span data-stu-id="6c758-293">1103 (0x44F)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-294">Ein Band Zugriff hat das Ende eines Satzes von Dateien erreicht.</span><span class="sxs-lookup"><span data-stu-id="6c758-294">A tape access reached the end of a set of files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-295"><span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**Fehler \_ beim \_ Erkennen von Daten. \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-295"><span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**ERROR\_NO\_DATA\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-296">1104 (0x450)</span><span class="sxs-lookup"><span data-stu-id="6c758-296">1104 (0x450)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-297">Es befinden sich keine weiteren Daten auf dem Band.</span><span class="sxs-lookup"><span data-stu-id="6c758-297">No more data is on the tape.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-298"><span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**Fehler \_ Partitions \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="6c758-298"><span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**ERROR\_PARTITION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-299">1105 (0x451)</span><span class="sxs-lookup"><span data-stu-id="6c758-299">1105 (0x451)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-300">Das Band konnte nicht partitioniert werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-300">Tape could not be partitioned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-301"><span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**Fehler \_ ungültige \_ Block \_ Länge.**</span><span class="sxs-lookup"><span data-stu-id="6c758-301"><span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**ERROR\_INVALID\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-302">1106 (0x452)</span><span class="sxs-lookup"><span data-stu-id="6c758-302">1106 (0x452)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-303">Beim Zugriff auf ein neues Band einer Partition mit mehreren Volumes ist die aktuelle Blockgröße falsch.</span><span class="sxs-lookup"><span data-stu-id="6c758-303">When accessing a new tape of a multivolume partition, the current block size is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-304"><span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**Fehler \_ Gerät \_ nicht \_ partitioniert**</span><span class="sxs-lookup"><span data-stu-id="6c758-304"><span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**ERROR\_DEVICE\_NOT\_PARTITIONED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-305">1107 (0x453)</span><span class="sxs-lookup"><span data-stu-id="6c758-305">1107 (0x453)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-306">Beim Laden eines Bands konnten keine Band Partitionsinformationen gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-306">Tape partition information could not be found when loading a tape.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-307"><span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**Fehler \_ beim \_ \_ Sperren des \_ Mediums.**</span><span class="sxs-lookup"><span data-stu-id="6c758-307"><span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**ERROR\_UNABLE\_TO\_LOCK\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-308">1108 (0x454)</span><span class="sxs-lookup"><span data-stu-id="6c758-308">1108 (0x454)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-309">Der Auswerfen-Mechanismus für Medien kann nicht gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-309">Unable to lock the media eject mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-310"><span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**Fehler \_ beim \_ \_ Entladen des \_ Mediums.**</span><span class="sxs-lookup"><span data-stu-id="6c758-310"><span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**ERROR\_UNABLE\_TO\_UNLOAD\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-311">1109 (0x455)</span><span class="sxs-lookup"><span data-stu-id="6c758-311">1109 (0x455)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-312">Das Medium kann nicht entladen werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-312">Unable to unload the media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-313"><span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**Fehler \_ Medien \_ geändert**</span><span class="sxs-lookup"><span data-stu-id="6c758-313"><span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**ERROR\_MEDIA\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-314">1110 (0x456)</span><span class="sxs-lookup"><span data-stu-id="6c758-314">1110 (0x456)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-315">Möglicherweise hat sich das Medium auf dem Laufwerk geändert.</span><span class="sxs-lookup"><span data-stu-id="6c758-315">The media in the drive may have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-316"><span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**\_ \_ Zurücksetzen des Fehler Busses**</span><span class="sxs-lookup"><span data-stu-id="6c758-316"><span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**ERROR\_BUS\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-317">1111 (0x457)</span><span class="sxs-lookup"><span data-stu-id="6c758-317">1111 (0x457)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-318">Der e/a-Bus wurde zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="6c758-318">The I/O bus was reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-319"><span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**Fehler " \_ kein \_ Medium \_ in \_ Laufwerk"**</span><span class="sxs-lookup"><span data-stu-id="6c758-319"><span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**ERROR\_NO\_MEDIA\_IN\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-320">1112 (0x458)</span><span class="sxs-lookup"><span data-stu-id="6c758-320">1112 (0x458)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-321">Kein Medium in Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="6c758-321">No media in drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-322"><span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**Fehler \_ keine \_ Unicode- \_ Übersetzung**</span><span class="sxs-lookup"><span data-stu-id="6c758-322"><span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**ERROR\_NO\_UNICODE\_TRANSLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-323">1113 (0x459)</span><span class="sxs-lookup"><span data-stu-id="6c758-323">1113 (0x459)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-324">Auf der Multi-Byte-Ziel Codepage ist keine Zuordnung für das Unicode-Zeichen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6c758-324">No mapping for the Unicode character exists in the target multi-byte code page.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-325"><span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**Fehler bei DLL-Initialisierung. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-325"><span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**ERROR\_DLL\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-326">1114 (0x45a)</span><span class="sxs-lookup"><span data-stu-id="6c758-326">1114 (0x45A)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-327">Fehler bei einer Initialisierungs Routine für eine Dynamic Link Library (dll).</span><span class="sxs-lookup"><span data-stu-id="6c758-327">A dynamic link library (DLL) initialization routine failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-328"><span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**Fehler \_ beim Herunterfahren. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-328"><span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**ERROR\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-329">1115 (0x45b)</span><span class="sxs-lookup"><span data-stu-id="6c758-329">1115 (0x45B)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-330">Ein System wird heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="6c758-330">A system shutdown is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-331"><span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**Fehler \_ \_ beim herunter \_ fahren \_ .**</span><span class="sxs-lookup"><span data-stu-id="6c758-331"><span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**ERROR\_NO\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-332">1116 (0x45c)</span><span class="sxs-lookup"><span data-stu-id="6c758-332">1116 (0x45C)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-333">Das Herunterfahren des Systems kann nicht abgebrochen werden, weil das Herunterfahren nicht durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="6c758-333">Unable to abort the system shutdown because no shutdown was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-334"><span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**Fehler- \_ IO- \_ Gerät**</span><span class="sxs-lookup"><span data-stu-id="6c758-334"><span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**ERROR\_IO\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-335">1117 (0x45d)</span><span class="sxs-lookup"><span data-stu-id="6c758-335">1117 (0x45D)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-336">Die Anforderung konnte aufgrund eines E/A-Gerätefehlers nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-336">The request could not be performed because of an I/O device error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-337"><span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**Fehler " \_ seriell \_ kein \_ Gerät"**</span><span class="sxs-lookup"><span data-stu-id="6c758-337"><span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**ERROR\_SERIAL\_NO\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-338">1118 (0x45e)</span><span class="sxs-lookup"><span data-stu-id="6c758-338">1118 (0x45E)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-339">Es wurde kein serielles Gerät erfolgreich initialisiert.</span><span class="sxs-lookup"><span data-stu-id="6c758-339">No serial device was successfully initialized.</span></span> <span data-ttu-id="6c758-340">Der serielle Treiber wird entladen.</span><span class="sxs-lookup"><span data-stu-id="6c758-340">The serial driver will unload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-341"><span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**Fehler \_ : UNQ \_ ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="6c758-341"><span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**ERROR\_IRQ\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-342">1119 (0x45f)</span><span class="sxs-lookup"><span data-stu-id="6c758-342">1119 (0x45F)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-343">Ein Gerät, das eine Interrupt-Anforderung (UNQ) mit anderen Geräten gemeinsam genutzt hat, kann nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-343">Unable to open a device that was sharing an interrupt request (IRQ) with other devices.</span></span> <span data-ttu-id="6c758-344">Mindestens ein anderes Gerät, das diesen UNQ verwendet, wurde bereits geöffnet.</span><span class="sxs-lookup"><span data-stu-id="6c758-344">At least one other device that uses that IRQ was already opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-345"><span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**Fehler \_ Weitere \_ Schreibvorgänge**</span><span class="sxs-lookup"><span data-stu-id="6c758-345"><span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**ERROR\_MORE\_WRITES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-346">1120 (0x460)</span><span class="sxs-lookup"><span data-stu-id="6c758-346">1120 (0x460)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-347">Ein serieller e/A-Vorgang wurde durch einen anderen Schreibvorgang an den seriellen Anschluss abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6c758-347">A serial I/O operation was completed by another write to the serial port.</span></span> <span data-ttu-id="6c758-348">Der serielle XOFF-Wert von IOCTL hat \_ \_ \_ Null erreicht.)</span><span class="sxs-lookup"><span data-stu-id="6c758-348">The IOCTL\_SERIAL\_XOFF\_COUNTER reached zero.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-349"><span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**Fehler \_ Zählers- \_ Timeout**</span><span class="sxs-lookup"><span data-stu-id="6c758-349"><span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**ERROR\_COUNTER\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-350">1121 (0x461)</span><span class="sxs-lookup"><span data-stu-id="6c758-350">1121 (0x461)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-351">Ein serieller e/A-Vorgang wurde abgeschlossen, da der Timeout Zeitraum abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="6c758-351">A serial I/O operation completed because the timeout period expired.</span></span> <span data-ttu-id="6c758-352">Der serielle XOFF-Wert von IOCTL \_ \_ \_ hat keine Null erreicht.)</span><span class="sxs-lookup"><span data-stu-id="6c758-352">The IOCTL\_SERIAL\_XOFF\_COUNTER did not reach zero.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-353"><span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**Fehler \_ Disketten \_ Kennung \_ \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6c758-353"><span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**ERROR\_FLOPPY\_ID\_MARK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-354">1122 (0x462)</span><span class="sxs-lookup"><span data-stu-id="6c758-354">1122 (0x462)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-355">Auf der Diskette wurde keine ID-Adress Markierung gefunden.</span><span class="sxs-lookup"><span data-stu-id="6c758-355">No ID address mark was found on the floppy disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-356"><span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**Fehler \_ Disketten \_ \_ Zylinder**</span><span class="sxs-lookup"><span data-stu-id="6c758-356"><span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**ERROR\_FLOPPY\_WRONG\_CYLINDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-357">1123 (0x463)</span><span class="sxs-lookup"><span data-stu-id="6c758-357">1123 (0x463)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-358">Konflikt zwischen dem Feld für die ID des Disketten Datenträgers und der Nachverfolgung der Disketten Adresse des Disketten Controllers.</span><span class="sxs-lookup"><span data-stu-id="6c758-358">Mismatch between the floppy disk sector ID field and the floppy disk controller track address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-359"><span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**Fehler \_ Disketten \_ unbekannter \_ Fehler.**</span><span class="sxs-lookup"><span data-stu-id="6c758-359"><span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**ERROR\_FLOPPY\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-360">1124 (0x464)</span><span class="sxs-lookup"><span data-stu-id="6c758-360">1124 (0x464)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-361">Der Disketten Controller hat einen Fehler gemeldet, der vom Disketten Treiber nicht erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="6c758-361">The floppy disk controller reported an error that is not recognized by the floppy disk driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-362"><span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**Fehler \_ Disketten \_ \_ Register**</span><span class="sxs-lookup"><span data-stu-id="6c758-362"><span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**ERROR\_FLOPPY\_BAD\_REGISTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-363">1125 (0x465)</span><span class="sxs-lookup"><span data-stu-id="6c758-363">1125 (0x465)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-364">Der Disketten Controller hat inkonsistente Ergebnisse in seinen Registern zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c758-364">The floppy disk controller returned inconsistent results in its registers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-365"><span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**Fehler \_ beim \_ Neuinitialisieren des Fehlers. \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-365"><span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**ERROR\_DISK\_RECALIBRATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-366">1126 (0x466)</span><span class="sxs-lookup"><span data-stu-id="6c758-366">1126 (0x466)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-367">Beim Zugriff auf die Festplatte ist ein Wiederholungs Vorgang auch nach Wiederholungs versuchen fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="6c758-367">While accessing the hard disk, a recalibrate operation failed, even after retries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-368"><span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**Fehler beim \_ Festplatten \_ Vorgang. \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-368"><span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**ERROR\_DISK\_OPERATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-369">1127 (0x467)</span><span class="sxs-lookup"><span data-stu-id="6c758-369">1127 (0x467)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-370">Beim Zugriff auf die Festplatte ist ein Datenträger Vorgang auch nach Wiederholungs versuchen fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="6c758-370">While accessing the hard disk, a disk operation failed even after retries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-371"><span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**Fehler \_ beim \_ Zurücksetzen des Datenträgers \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-371"><span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**ERROR\_DISK\_RESET\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-372">1128 (0x468)</span><span class="sxs-lookup"><span data-stu-id="6c758-372">1128 (0x468)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-373">Beim Zugriff auf die Festplatte war eine Datenträger Controller-zurück Setzung erforderlich, aber auch dies ist nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6c758-373">While accessing the hard disk, a disk controller reset was needed, but even that failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-374"><span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**Fehler bei \_ EOM- \_ Überlauf**</span><span class="sxs-lookup"><span data-stu-id="6c758-374"><span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**ERROR\_EOM\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-375">1129 (0x469)</span><span class="sxs-lookup"><span data-stu-id="6c758-375">1129 (0x469)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-376">Das physische Ende des Bands ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6c758-376">Physical end of tape encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-377"><span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**Fehler \_ nicht \_ genug \_ Server \_ Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="6c758-377"><span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**ERROR\_NOT\_ENOUGH\_SERVER\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-378">1130 (0x46a)</span><span class="sxs-lookup"><span data-stu-id="6c758-378">1130 (0x46A)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-379">Für diesen Befehl ist nicht genügend Serverspeicher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c758-379">Not enough server storage is available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-380"><span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**Fehler \_ möglicher \_ Deadlock**</span><span class="sxs-lookup"><span data-stu-id="6c758-380"><span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**ERROR\_POSSIBLE\_DEADLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-381">1131 (0x46b)</span><span class="sxs-lookup"><span data-stu-id="6c758-381">1131 (0x46B)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-382">Es wurde eine potenzielle Deadlockbedingung erkannt.</span><span class="sxs-lookup"><span data-stu-id="6c758-382">A potential deadlock condition has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-383"><span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**Fehler beim Zuordnen der \_ \_ Ausrichtung**</span><span class="sxs-lookup"><span data-stu-id="6c758-383"><span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**ERROR\_MAPPED\_ALIGNMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-384">1132 (0x46c)</span><span class="sxs-lookup"><span data-stu-id="6c758-384">1132 (0x46C)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-385">Die angegebene Basisadresse oder der angegebene Dateioffset weist nicht die richtige Ausrichtung auf.</span><span class="sxs-lookup"><span data-stu-id="6c758-385">The base address or the file offset specified does not have the proper alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-386"><span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**Fehler beim \_ Festlegen des \_ Energie \_ Zustands \_ .**</span><span class="sxs-lookup"><span data-stu-id="6c758-386"><span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**ERROR\_SET\_POWER\_STATE\_VETOED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-387">1140 (0x474)</span><span class="sxs-lookup"><span data-stu-id="6c758-387">1140 (0x474)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-388">Der Versuch, den System Energiezustand zu ändern, wurde von einer anderen Anwendung oder einem anderen Treiber geprüft.</span><span class="sxs-lookup"><span data-stu-id="6c758-388">An attempt to change the system power state was vetoed by another application or driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-389"><span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**Fehler beim \_ Festlegen des \_ Energie \_ Zustands \_ .**</span><span class="sxs-lookup"><span data-stu-id="6c758-389"><span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**ERROR\_SET\_POWER\_STATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-390">1141 (0x475)</span><span class="sxs-lookup"><span data-stu-id="6c758-390">1141 (0x475)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-391">Vom System-BIOS konnte der System Energiezustand nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-391">The system BIOS failed an attempt to change the system power state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-392"><span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**Fehler \_ zu \_ viele \_ Verknüpfungen**</span><span class="sxs-lookup"><span data-stu-id="6c758-392"><span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**ERROR\_TOO\_MANY\_LINKS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-393">1142 (0x476)</span><span class="sxs-lookup"><span data-stu-id="6c758-393">1142 (0x476)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-394">Es wurde versucht, mehr Verknüpfungen für eine Datei zu erstellen, als das Dateisystem unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c758-394">An attempt was made to create more links on a file than the file system supports.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-395"><span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**Fehler \_ alte \_ Win- \_ Version**</span><span class="sxs-lookup"><span data-stu-id="6c758-395"><span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**ERROR\_OLD\_WIN\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-396">1150 (0x47e)</span><span class="sxs-lookup"><span data-stu-id="6c758-396">1150 (0x47E)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-397">Das angegebene Programm erfordert eine neuere Version von Windows.</span><span class="sxs-lookup"><span data-stu-id="6c758-397">The specified program requires a newer version of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-398"><span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**Fehler- \_ App- \_ falsches \_ Betriebssystem**</span><span class="sxs-lookup"><span data-stu-id="6c758-398"><span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**ERROR\_APP\_WRONG\_OS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-399">1151 (0x47f)</span><span class="sxs-lookup"><span data-stu-id="6c758-399">1151 (0x47F)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-400">Das angegebene Programm ist keine MS-DOS- oder Windows-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6c758-400">The specified program is not a Windows or MS-DOS program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-401"><span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**Fehler bei \_ Einzel \_ Instanz- \_ App**</span><span class="sxs-lookup"><span data-stu-id="6c758-401"><span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**ERROR\_SINGLE\_INSTANCE\_APP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-402">1152 (0x480)</span><span class="sxs-lookup"><span data-stu-id="6c758-402">1152 (0x480)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-403">Es kann nicht mehr als eine Instanz des angegebenen Programms gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-403">Cannot start more than one instance of the specified program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-404"><span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**Fehler- \_ rmode- \_ App**</span><span class="sxs-lookup"><span data-stu-id="6c758-404"><span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**ERROR\_RMODE\_APP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-405">1153 (0x481)</span><span class="sxs-lookup"><span data-stu-id="6c758-405">1153 (0x481)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-406">Das angegebene Programm wurde für eine frühere Version von Windows geschrieben.</span><span class="sxs-lookup"><span data-stu-id="6c758-406">The specified program was written for an earlier version of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-407"><span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**Fehler \_ ungültige \_ dll.**</span><span class="sxs-lookup"><span data-stu-id="6c758-407"><span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**ERROR\_INVALID\_DLL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-408">1154 (0x482)</span><span class="sxs-lookup"><span data-stu-id="6c758-408">1154 (0x482)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-409">Eine der Bibliotheksdateien, die zum Ausführen dieser Anwendung benötigt werden, ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6c758-409">One of the library files needed to run this application is damaged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-410"><span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**Fehler \_ ohne \_ Zuordnung**</span><span class="sxs-lookup"><span data-stu-id="6c758-410"><span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**ERROR\_NO\_ASSOCIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-411">1155 (0x483)</span><span class="sxs-lookup"><span data-stu-id="6c758-411">1155 (0x483)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-412">Der angegebenen Datei ist keine Anwendung für diesen Vorgang zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6c758-412">No application is associated with the specified file for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-413"><span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**Fehler \_ DDE \_ schlägt fehl**</span><span class="sxs-lookup"><span data-stu-id="6c758-413"><span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**ERROR\_DDE\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-414">1156 (0x484)</span><span class="sxs-lookup"><span data-stu-id="6c758-414">1156 (0x484)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-415">Fehler beim Senden des Befehls an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6c758-415">An error occurred in sending the command to the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-416"><span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**Fehler- \_ dll wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6c758-416"><span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**ERROR\_DLL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-417">1157 (0x485)</span><span class="sxs-lookup"><span data-stu-id="6c758-417">1157 (0x485)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-418">Eine der Bibliotheksdateien, die zum Ausführen dieser Anwendung benötigt werden, wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6c758-418">One of the library files needed to run this application cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-419"><span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**Fehler \_ keine \_ weiteren \_ Benutzer \_ Handles**</span><span class="sxs-lookup"><span data-stu-id="6c758-419"><span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ERROR\_NO\_MORE\_USER\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-420">1158 (0x486)</span><span class="sxs-lookup"><span data-stu-id="6c758-420">1158 (0x486)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-421">Der aktuelle Prozess hat das gesamte System Kontingent von Handles für Fenster-Manager-Objekte verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c758-421">The current process has used all of its system allowance of handles for Window Manager objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-422"><span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**\_nur Fehlermeldung \_ Synchronisieren \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-422"><span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**ERROR\_MESSAGE\_SYNC\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-423">1159 (0x487)</span><span class="sxs-lookup"><span data-stu-id="6c758-423">1159 (0x487)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-424">Die Nachricht kann nur mit synchronen Vorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-424">The message can be used only with synchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-425"><span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**Fehler \_ Quell \_ Element \_ leer**</span><span class="sxs-lookup"><span data-stu-id="6c758-425"><span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**ERROR\_SOURCE\_ELEMENT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-426">1160 (0x488)</span><span class="sxs-lookup"><span data-stu-id="6c758-426">1160 (0x488)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-427">Das festgestellte Quell Element weist kein Medium auf.</span><span class="sxs-lookup"><span data-stu-id="6c758-427">The indicated source element has no media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-428"><span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**Fehler \_ Ziel \_ Element \_ voll**</span><span class="sxs-lookup"><span data-stu-id="6c758-428"><span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**ERROR\_DESTINATION\_ELEMENT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-429">1161 (0x489)</span><span class="sxs-lookup"><span data-stu-id="6c758-429">1161 (0x489)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-430">Das angegeben Ziel Element enthält bereits Medien.</span><span class="sxs-lookup"><span data-stu-id="6c758-430">The indicated destination element already contains media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-431"><span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**Fehler ungültige \_ \_ Element \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="6c758-431"><span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**ERROR\_ILLEGAL\_ELEMENT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-432">1162 (0x48a)</span><span class="sxs-lookup"><span data-stu-id="6c758-432">1162 (0x48A)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-433">Das angegeben Element ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6c758-433">The indicated element does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-434"><span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**das Fehler \_ Magazin ist \_ nicht \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="6c758-434"><span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**ERROR\_MAGAZINE\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-435">1163 (0x48b)</span><span class="sxs-lookup"><span data-stu-id="6c758-435">1163 (0x48B)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-436">Das festgestellte Element ist Teil eines Magazins, das nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6c758-436">The indicated element is part of a magazine that is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-437"><span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**Fehler bei der \_ \_ erneuten Initialisierung des Geräts. \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-437"><span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**ERROR\_DEVICE\_REINITIALIZATION\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-438">1164 (0x48c)</span><span class="sxs-lookup"><span data-stu-id="6c758-438">1164 (0x48C)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-439">Das für das Gerät erforderliche Gerät muss aufgrund von Hardwarefehlern erneut initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-439">The indicated device requires reinitialization due to hardware errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-440"><span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**Fehler \_ Gerät \_ erfordert \_ Bereinigen**</span><span class="sxs-lookup"><span data-stu-id="6c758-440"><span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**ERROR\_DEVICE\_REQUIRES\_CLEANING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-441">1165 (0x48d)</span><span class="sxs-lookup"><span data-stu-id="6c758-441">1165 (0x48D)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-442">Das Gerät hat angegeben, dass eine Bereinigung erforderlich ist, bevor weitere Vorgänge versucht werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-442">The device has indicated that cleaning is required before further operations are attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-443"><span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**Fehler \_ beim \_ Öffnen des Geräts. \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-443"><span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**ERROR\_DEVICE\_DOOR\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-444">1166 (0x48e)</span><span class="sxs-lookup"><span data-stu-id="6c758-444">1166 (0x48E)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-445">Das Gerät hat angegeben, dass seine Tür geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="6c758-445">The device has indicated that its door is open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-446"><span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**Fehler \_ Gerät \_ nicht \_ verbunden**</span><span class="sxs-lookup"><span data-stu-id="6c758-446"><span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**ERROR\_DEVICE\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-447">1167 (0x48f)</span><span class="sxs-lookup"><span data-stu-id="6c758-447">1167 (0x48F)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-448">Das Gerät ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="6c758-448">The device is not connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-449"><span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**Fehler \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6c758-449"><span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**ERROR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-450">1168 (0x490)</span><span class="sxs-lookup"><span data-stu-id="6c758-450">1168 (0x490)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-451">Element wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6c758-451">Element not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-452"><span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**Fehler \_ keine Entsprechung \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-452"><span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**ERROR\_NO\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-453">1169 (0x491)</span><span class="sxs-lookup"><span data-stu-id="6c758-453">1169 (0x491)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-454">Es gab keine Entsprechung für den angegebenen Schlüssel im Index.</span><span class="sxs-lookup"><span data-stu-id="6c758-454">There was no match for the specified key in the index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-455"><span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**Fehler \_ Satz \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6c758-455"><span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**ERROR\_SET\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-456">1170 (0x492)</span><span class="sxs-lookup"><span data-stu-id="6c758-456">1170 (0x492)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-457">Der angegebene Eigenschaften Satz ist im Objekt nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6c758-457">The property set specified does not exist on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-458"><span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**der Fehler \_ Punkt wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6c758-458"><span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**ERROR\_POINT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-459">1171 (0x493)</span><span class="sxs-lookup"><span data-stu-id="6c758-459">1171 (0x493)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-460">Der an getmoucmuvepoints über gegebene Punkt befindet sich nicht im Puffer.</span><span class="sxs-lookup"><span data-stu-id="6c758-460">The point passed to GetMouseMovePoints is not in the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-461"><span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**Fehler " \_ kein \_ Überwachungs \_ Dienst"**</span><span class="sxs-lookup"><span data-stu-id="6c758-461"><span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**ERROR\_NO\_TRACKING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-462">1172 (0x494)</span><span class="sxs-lookup"><span data-stu-id="6c758-462">1172 (0x494)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-463">Der Überwachungsdienst (Arbeitsstations Dienst) wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c758-463">The tracking (workstation) service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-464"><span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**Fehler " \_ keine \_ Volume- \_ ID"**</span><span class="sxs-lookup"><span data-stu-id="6c758-464"><span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**ERROR\_NO\_VOLUME\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-465">1173 (0x495)</span><span class="sxs-lookup"><span data-stu-id="6c758-465">1173 (0x495)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-466">Die Volume-ID wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6c758-466">The Volume ID could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-467"><span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**Fehler \_ beim \_ \_ Entfernen des \_ ersetzenden**</span><span class="sxs-lookup"><span data-stu-id="6c758-467"><span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**ERROR\_UNABLE\_TO\_REMOVE\_REPLACED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-468">1175 (0x497)</span><span class="sxs-lookup"><span data-stu-id="6c758-468">1175 (0x497)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-469">Die zu ersetzende Datei kann nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-469">Unable to remove the file to be replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-470"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**Fehler \_ beim \_ \_ Verschieben der \_ Ersetzung.**</span><span class="sxs-lookup"><span data-stu-id="6c758-470"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**ERROR\_UNABLE\_TO\_MOVE\_REPLACEMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-471">1176 (0x498)</span><span class="sxs-lookup"><span data-stu-id="6c758-471">1176 (0x498)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-472">Die Ersetzungs Datei kann nicht in die zu ersetzende Datei verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-472">Unable to move the replacement file to the file to be replaced.</span></span> <span data-ttu-id="6c758-473">Die zu ersetzende Datei hat den ursprünglichen Namen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="6c758-473">The file to be replaced has retained its original name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-474"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**Fehler \_ beim \_ \_ Verschieben von \_ Ersetzung \_ 2.**</span><span class="sxs-lookup"><span data-stu-id="6c758-474"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**ERROR\_UNABLE\_TO\_MOVE\_REPLACEMENT\_2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-475">1177 (0x499)</span><span class="sxs-lookup"><span data-stu-id="6c758-475">1177 (0x499)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-476">Die Ersetzungs Datei kann nicht in die zu ersetzende Datei verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-476">Unable to move the replacement file to the file to be replaced.</span></span> <span data-ttu-id="6c758-477">Die zu ersetzende Datei wurde mit dem Sicherungs Namen umbenannt.</span><span class="sxs-lookup"><span data-stu-id="6c758-477">The file to be replaced has been renamed using the backup name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-478"><span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**Fehler \_ Journal \_ wird \_ gelöscht \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-478"><span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**ERROR\_JOURNAL\_DELETE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-479">1178 (0x49a)</span><span class="sxs-lookup"><span data-stu-id="6c758-479">1178 (0x49A)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-480">Das Volume-Änderungs Journal wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6c758-480">The volume change journal is being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-481"><span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**das Fehler \_ Journal ist \_ nicht \_ aktiv.**</span><span class="sxs-lookup"><span data-stu-id="6c758-481"><span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**ERROR\_JOURNAL\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-482">1179 (0x49b)</span><span class="sxs-lookup"><span data-stu-id="6c758-482">1179 (0x49B)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-483">Das Volume-Änderungs Journal ist nicht aktiv.</span><span class="sxs-lookup"><span data-stu-id="6c758-483">The volume change journal is not active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-484"><span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**Fehler \_ mögliche \_ Datei \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6c758-484"><span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**ERROR\_POTENTIAL\_FILE\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-485">1180 (0x49c)</span><span class="sxs-lookup"><span data-stu-id="6c758-485">1180 (0x49C)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-486">Eine Datei wurde gefunden, Sie ist jedoch möglicherweise nicht die richtige Datei.</span><span class="sxs-lookup"><span data-stu-id="6c758-486">A file was found, but it may not be the correct file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-487"><span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**Fehler \_ Journal \_ Eintrag \_ gelöscht**</span><span class="sxs-lookup"><span data-stu-id="6c758-487"><span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**ERROR\_JOURNAL\_ENTRY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-488">1181 (0x49d)</span><span class="sxs-lookup"><span data-stu-id="6c758-488">1181 (0x49D)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-489">Der Journal Eintrag wurde aus dem Journal gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6c758-489">The journal entry has been deleted from the journal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-490"><span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**Fehler beim Herunterfahren des Fehlers. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-490"><span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**ERROR\_SHUTDOWN\_IS\_SCHEDULED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-491">1190 (0x4a6)</span><span class="sxs-lookup"><span data-stu-id="6c758-491">1190 (0x4A6)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-492">Das Herunterfahren des Systems wurde bereits geplant.</span><span class="sxs-lookup"><span data-stu-id="6c758-492">A system shutdown has already been scheduled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-493"><span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**Fehler \_ beim Herunterfahren \_ \_ der angemeldeten Benutzer \_ .**</span><span class="sxs-lookup"><span data-stu-id="6c758-493"><span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**ERROR\_SHUTDOWN\_USERS\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-494">1191 (0x4a7)</span><span class="sxs-lookup"><span data-stu-id="6c758-494">1191 (0x4A7)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-495">Das Herunterfahren des Systems kann nicht initiiert werden, da andere Benutzer auf dem Computer angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="6c758-495">The system shutdown cannot be initiated because there are other users logged on to the computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-496"><span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**fehlerhaftes \_ \_ Gerät**</span><span class="sxs-lookup"><span data-stu-id="6c758-496"><span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**ERROR\_BAD\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-497">1200 (0x4b0)</span><span class="sxs-lookup"><span data-stu-id="6c758-497">1200 (0x4B0)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-498">Der angegebene Gerätename ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c758-498">The specified device name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-499"><span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**Fehler beim wieder \_ herstellen der Verbindung. \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-499"><span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**ERROR\_CONNECTION\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-500">1201 (0x4b1)</span><span class="sxs-lookup"><span data-stu-id="6c758-500">1201 (0x4B1)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-501">Das Gerät ist zurzeit nicht verbunden, aber es handelt sich um eine gespeicherte Verbindung.</span><span class="sxs-lookup"><span data-stu-id="6c758-501">The device is not currently connected but it is a remembered connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-502"><span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**das Fehler \_ Gerät wurde \_ bereits \_ gespeichert.**</span><span class="sxs-lookup"><span data-stu-id="6c758-502"><span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**ERROR\_DEVICE\_ALREADY\_REMEMBERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-503">1202 (0x4b2)</span><span class="sxs-lookup"><span data-stu-id="6c758-503">1202 (0x4B2)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-504">Der Name des lokalen Geräts hat eine Verbindung mit einer anderen Netzwerkressource.</span><span class="sxs-lookup"><span data-stu-id="6c758-504">The local device name has a remembered connection to another network resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-505"><span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**Fehler \_ beim \_ Netzwerk \_ oder ungültigen \_ \_ Pfad.**</span><span class="sxs-lookup"><span data-stu-id="6c758-505"><span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**ERROR\_NO\_NET\_OR\_BAD\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-506">1203 (0x4b3)</span><span class="sxs-lookup"><span data-stu-id="6c758-506">1203 (0x4B3)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-507">Der Netzwerkpfad wurde entweder falsch eingegeben, ist nicht vorhanden, oder der Netzwerkanbieter ist zurzeit nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c758-507">The network path was either typed incorrectly, does not exist, or the network provider is not currently available.</span></span> <span data-ttu-id="6c758-508">Versuchen Sie, den Pfad erneut einzugeben, oder wenden Sie sich an Ihren Netzwerkadministrator.</span><span class="sxs-lookup"><span data-stu-id="6c758-508">Please try retyping the path or contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-509"><span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**fehlerhafter \_ \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="6c758-509"><span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**ERROR\_BAD\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-510">1204 (0x4b4)</span><span class="sxs-lookup"><span data-stu-id="6c758-510">1204 (0x4B4)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-511">Der angegebene Netzwerkanbieter Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c758-511">The specified network provider name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-512"><span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**Fehler \_ beim \_ Öffnen des \_ Profils.**</span><span class="sxs-lookup"><span data-stu-id="6c758-512"><span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**ERROR\_CANNOT\_OPEN\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-513">1205 (0x4b5)</span><span class="sxs-lookup"><span data-stu-id="6c758-513">1205 (0x4B5)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-514">Das Netzwerk Verbindungsprofil kann nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-514">Unable to open the network connection profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-515"><span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**fehlerhaftes \_ \_ Profil**</span><span class="sxs-lookup"><span data-stu-id="6c758-515"><span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ERROR\_BAD\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-516">1206 (0x4b6)</span><span class="sxs-lookup"><span data-stu-id="6c758-516">1206 (0x4B6)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-517">Das Netzwerk Verbindungsprofil ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6c758-517">The network connection profile is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-518"><span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**Fehler \_ nicht \_ Container**</span><span class="sxs-lookup"><span data-stu-id="6c758-518"><span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**ERROR\_NOT\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-519">1207 (0x4b7)</span><span class="sxs-lookup"><span data-stu-id="6c758-519">1207 (0x4B7)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-520">Ein nicht Container kann nicht aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-520">Cannot enumerate a noncontainer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-521"><span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**Fehler beim \_ erweiterten \_ Fehler.**</span><span class="sxs-lookup"><span data-stu-id="6c758-521"><span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**ERROR\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-522">1208 (0x4b8)</span><span class="sxs-lookup"><span data-stu-id="6c758-522">1208 (0x4B8)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-523">Ein erweiterter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6c758-523">An extended error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-524"><span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**Fehler \_ ungültiger \_ Gruppenname.**</span><span class="sxs-lookup"><span data-stu-id="6c758-524"><span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**ERROR\_INVALID\_GROUPNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-525">1209 (0x4b9)</span><span class="sxs-lookup"><span data-stu-id="6c758-525">1209 (0x4B9)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-526">Das Format des angegebenen Gruppennamens ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c758-526">The format of the specified group name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-527"><span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**Fehler \_ ungültiger \_ Computername.**</span><span class="sxs-lookup"><span data-stu-id="6c758-527"><span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**ERROR\_INVALID\_COMPUTERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-528">1210 (0x4ba)</span><span class="sxs-lookup"><span data-stu-id="6c758-528">1210 (0x4BA)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-529">Das Format des angegebenen Computer namens ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c758-529">The format of the specified computer name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-530"><span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**Fehler bei \_ ungültigem \_ Ereignis Name.**</span><span class="sxs-lookup"><span data-stu-id="6c758-530"><span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERROR\_INVALID\_EVENTNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-531">1211 (0x4bb)</span><span class="sxs-lookup"><span data-stu-id="6c758-531">1211 (0x4BB)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-532">Das Format des angegebenen Ereignis namens ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c758-532">The format of the specified event name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-533"><span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**\_ungültiger \_ Domänen Name.**</span><span class="sxs-lookup"><span data-stu-id="6c758-533"><span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**ERROR\_INVALID\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-534">1212 (0x4bc)</span><span class="sxs-lookup"><span data-stu-id="6c758-534">1212 (0x4BC)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-535">Das Format des angegebenen Domänen Namens ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c758-535">The format of the specified domain name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-536"><span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**Fehler \_ ungültiger \_ Dienst Name.**</span><span class="sxs-lookup"><span data-stu-id="6c758-536"><span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**ERROR\_INVALID\_SERVICENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-537">1213 (0x4bd)</span><span class="sxs-lookup"><span data-stu-id="6c758-537">1213 (0x4BD)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-538">Das Format des angegebenen Dienst namens ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c758-538">The format of the specified service name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-539"><span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**Fehler \_ beim \_ NetName.**</span><span class="sxs-lookup"><span data-stu-id="6c758-539"><span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**ERROR\_INVALID\_NETNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-540">1214 (0x4be)</span><span class="sxs-lookup"><span data-stu-id="6c758-540">1214 (0x4BE)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-541">Das Format des angegebenen Netzwerk namens ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c758-541">The format of the specified network name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-542"><span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**\_ungültiger \_ ShareName.**</span><span class="sxs-lookup"><span data-stu-id="6c758-542"><span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**ERROR\_INVALID\_SHARENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-543">1215 (0x4bf)</span><span class="sxs-lookup"><span data-stu-id="6c758-543">1215 (0x4BF)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-544">Das Format des angegebenen Freigabe namens ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c758-544">The format of the specified share name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-545"><span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**\_ungültiger \_ passwordname.**</span><span class="sxs-lookup"><span data-stu-id="6c758-545"><span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**ERROR\_INVALID\_PASSWORDNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-546">1216 (0x4c0)</span><span class="sxs-lookup"><span data-stu-id="6c758-546">1216 (0x4C0)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-547">Das Format des angegebenen Kennworts ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c758-547">The format of the specified password is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-548"><span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**Fehler \_ ungültiger \_ MessageName.**</span><span class="sxs-lookup"><span data-stu-id="6c758-548"><span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**ERROR\_INVALID\_MESSAGENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-549">1217 (0x4c1)</span><span class="sxs-lookup"><span data-stu-id="6c758-549">1217 (0x4C1)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-550">Das Format des angegebenen Nachrichten namens ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c758-550">The format of the specified message name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-551"><span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**Fehler \_ ungültige \_ messagedest.**</span><span class="sxs-lookup"><span data-stu-id="6c758-551"><span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**ERROR\_INVALID\_MESSAGEDEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-552">1218 (0x4c2)</span><span class="sxs-lookup"><span data-stu-id="6c758-552">1218 (0x4C2)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-553">Das Format des angegebenen Nachrichten Ziels ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c758-553">The format of the specified message destination is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-554"><span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**Konflikt mit Anmelde Informationen für die Fehler \_ Sitzung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-554"><span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**ERROR\_SESSION\_CREDENTIAL\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-555">1219 (0x4c3)</span><span class="sxs-lookup"><span data-stu-id="6c758-555">1219 (0x4C3)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-556">Mehrere Verbindungen mit einem Server oder einer gemeinsam genutzten Ressource durch denselben Benutzer mit mehr als einem Benutzernamen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="6c758-556">Multiple connections to a server or shared resource by the same user, using more than one user name, are not allowed.</span></span> <span data-ttu-id="6c758-557">Trennen Sie alle vorherigen Verbindungen mit dem Server oder der freigegebenen Ressource, und versuchen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="6c758-557">Disconnect all previous connections to the server or shared resource and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-558"><span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**Fehler bei \_ Remote \_ Sitzungs \_ Limit \_ überschritten.**</span><span class="sxs-lookup"><span data-stu-id="6c758-558"><span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**ERROR\_REMOTE\_SESSION\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-559">1220 (0x4c4)</span><span class="sxs-lookup"><span data-stu-id="6c758-559">1220 (0x4C4)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-560">Es wurde versucht, eine Sitzung mit einem Netzwerkserver einzurichten, aber es wurden bereits zu viele Sitzungen auf diesem Server eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6c758-560">An attempt was made to establish a session to a network server, but there are already too many sessions established to that server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-561"><span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**Fehler \_ DUP \_ Domain Name**</span><span class="sxs-lookup"><span data-stu-id="6c758-561"><span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**ERROR\_DUP\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-562">1221 (0x4c5)</span><span class="sxs-lookup"><span data-stu-id="6c758-562">1221 (0x4C5)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-563">Der Arbeitsgruppen-oder Domänen Name wird bereits von einem anderen Computer im Netzwerk verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c758-563">The workgroup or domain name is already in use by another computer on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-564"><span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**Fehler " \_ kein \_ Netzwerk"**</span><span class="sxs-lookup"><span data-stu-id="6c758-564"><span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**ERROR\_NO\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-565">1222 (0x4c6)</span><span class="sxs-lookup"><span data-stu-id="6c758-565">1222 (0x4C6)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-566">Das Netzwerk ist nicht vorhanden oder wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="6c758-566">The network is not present or not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-567"><span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**Fehler \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="6c758-567"><span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**ERROR\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-568">1223 (0x4c7)</span><span class="sxs-lookup"><span data-stu-id="6c758-568">1223 (0x4C7)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-569">Der Vorgang wurde vom Benutzer abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="6c758-569">The operation was canceled by the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-570"><span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**Benutzer zugeordnete Datei mit Fehler \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-570"><span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**ERROR\_USER\_MAPPED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-571">1224 (0x4c8)</span><span class="sxs-lookup"><span data-stu-id="6c758-571">1224 (0x4C8)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-572">Der angeforderte Vorgang kann nicht für eine Datei ausgeführt werden, in der ein vom Benutzer zugeordneter Abschnitt geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="6c758-572">The requested operation cannot be performed on a file with a user-mapped section open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-573"><span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**Fehler \_ Verbindung \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="6c758-573"><span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**ERROR\_CONNECTION\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-574">1225 (0x4c9)</span><span class="sxs-lookup"><span data-stu-id="6c758-574">1225 (0x4C9)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-575">Der Remote Computer hat die Netzwerkverbindung verweigert.</span><span class="sxs-lookup"><span data-stu-id="6c758-575">The remote computer refused the network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-576"><span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**Fehler beim Trennen der Verbindung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-576"><span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**ERROR\_GRACEFUL\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-577">1226 (0x4ca)</span><span class="sxs-lookup"><span data-stu-id="6c758-577">1226 (0x4CA)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-578">Die Netzwerkverbindung wurde ordnungsgemäß geschlossen.</span><span class="sxs-lookup"><span data-stu-id="6c758-578">The network connection was gracefully closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-579"><span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**die Fehler \_ Adresse ist \_ bereits \_ zugeordnet.**</span><span class="sxs-lookup"><span data-stu-id="6c758-579"><span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**ERROR\_ADDRESS\_ALREADY\_ASSOCIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-580">1227 (0x4cb)</span><span class="sxs-lookup"><span data-stu-id="6c758-580">1227 (0x4CB)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-581">Dem Netzwerk Transport Endpunkt ist bereits eine Adresse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6c758-581">The network transport endpoint already has an address associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-582"><span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**Fehler \_ Adresse \_ nicht \_ zugeordnet**</span><span class="sxs-lookup"><span data-stu-id="6c758-582"><span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**ERROR\_ADDRESS\_NOT\_ASSOCIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-583">1228 (0x4cc)</span><span class="sxs-lookup"><span data-stu-id="6c758-583">1228 (0x4CC)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-584">Dem Netzwerk Endpunkt wurde noch keine Adresse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6c758-584">An address has not yet been associated with the network endpoint.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-585"><span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**Fehler \_ Verbindung \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="6c758-585"><span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**ERROR\_CONNECTION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-586">1229 (0x4cd)</span><span class="sxs-lookup"><span data-stu-id="6c758-586">1229 (0x4CD)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-587">Es wurde versucht, einen Vorgang für eine nicht vorhandene Netzwerkverbindung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6c758-587">An operation was attempted on a nonexistent network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-588"><span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**Fehler \_ Verbindung \_ aktiv**</span><span class="sxs-lookup"><span data-stu-id="6c758-588"><span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**ERROR\_CONNECTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-589">1230 (0x4ce)</span><span class="sxs-lookup"><span data-stu-id="6c758-589">1230 (0x4CE)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-590">Es wurde versucht, einen ungültigen Vorgang für eine aktive Netzwerkverbindung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6c758-590">An invalid operation was attempted on an active network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-591"><span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**Fehler \_ Netzwerk \_ nicht erreichbar**</span><span class="sxs-lookup"><span data-stu-id="6c758-591"><span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**ERROR\_NETWORK\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-592">1231 (0x4cf)</span><span class="sxs-lookup"><span data-stu-id="6c758-592">1231 (0x4CF)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-593">Der Netzwerk Speicherort ist nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="6c758-593">The network location cannot be reached.</span></span> <span data-ttu-id="6c758-594">Informationen zur Netzwerkproblem Behandlung finden Sie in der Windows-Hilfe.</span><span class="sxs-lookup"><span data-stu-id="6c758-594">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-595"><span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**Fehler \_ Host ist \_ nicht erreichbar.**</span><span class="sxs-lookup"><span data-stu-id="6c758-595"><span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**ERROR\_HOST\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-596">1232 (0x4d0)</span><span class="sxs-lookup"><span data-stu-id="6c758-596">1232 (0x4D0)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-597">Der Netzwerk Speicherort ist nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="6c758-597">The network location cannot be reached.</span></span> <span data-ttu-id="6c758-598">Informationen zur Netzwerkproblem Behandlung finden Sie in der Windows-Hilfe.</span><span class="sxs-lookup"><span data-stu-id="6c758-598">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-599"><span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**das Fehler \_ Protokoll ist \_ nicht erreichbar.**</span><span class="sxs-lookup"><span data-stu-id="6c758-599"><span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**ERROR\_PROTOCOL\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-600">1233 (0x4d1)</span><span class="sxs-lookup"><span data-stu-id="6c758-600">1233 (0x4D1)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-601">Der Netzwerk Speicherort ist nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="6c758-601">The network location cannot be reached.</span></span> <span data-ttu-id="6c758-602">Informationen zur Netzwerkproblem Behandlung finden Sie in der Windows-Hilfe.</span><span class="sxs-lookup"><span data-stu-id="6c758-602">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-603"><span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**der \_ fehlerport ist \_ nicht erreichbar.**</span><span class="sxs-lookup"><span data-stu-id="6c758-603"><span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**ERROR\_PORT\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-604">1234 (0x4d2)</span><span class="sxs-lookup"><span data-stu-id="6c758-604">1234 (0x4D2)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-605">Am Zielnetzwerk Endpunkt auf dem Remote System ist kein Dienst Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="6c758-605">No service is operating at the destination network endpoint on the remote system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-606"><span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**Fehler \_ Anforderung \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="6c758-606"><span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**ERROR\_REQUEST\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-607">1235 (0x4d3)</span><span class="sxs-lookup"><span data-stu-id="6c758-607">1235 (0x4D3)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-608">Die Anforderung wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="6c758-608">The request was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-609"><span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**Fehler \_ Verbindung \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="6c758-609"><span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**ERROR\_CONNECTION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-610">1236 (0x4d4)</span><span class="sxs-lookup"><span data-stu-id="6c758-610">1236 (0x4D4)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-611">Die Netzwerkverbindung wurde vom lokalen System abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="6c758-611">The network connection was aborted by the local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-612"><span id="ERROR_RETRY"></span><span id="error_retry"></span>**Fehler beim \_ Wiederholungsversuch.**</span><span class="sxs-lookup"><span data-stu-id="6c758-612"><span id="ERROR_RETRY"></span><span id="error_retry"></span>**ERROR\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-613">1237 (0x4d5)</span><span class="sxs-lookup"><span data-stu-id="6c758-613">1237 (0x4D5)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-614">Der Vorgang konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-614">The operation could not be completed.</span></span> <span data-ttu-id="6c758-615">Es sollte eine Wiederholung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-615">A retry should be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-616"><span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**Limit für die \_ Anzahl von Verbindungsfehlern \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-616"><span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**ERROR\_CONNECTION\_COUNT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-617">1238 (0x4d6)</span><span class="sxs-lookup"><span data-stu-id="6c758-617">1238 (0x4D6)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-618">Es konnte keine Verbindung mit dem Server hergestellt werden, da der Grenzwert für die Anzahl der gleichzeitigen Verbindungen für dieses Konto erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="6c758-618">A connection to the server could not be made because the limit on the number of concurrent connections for this account has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-619"><span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**Einschränkung der Fehler \_ Anmelde \_ Zeit \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-619"><span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**ERROR\_LOGIN\_TIME\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-620">1239 (0x4d7)</span><span class="sxs-lookup"><span data-stu-id="6c758-620">1239 (0x4D7)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-621">Es wird versucht, sich während einer nicht autorisierten Tageszeit für dieses Konto anzumelden.</span><span class="sxs-lookup"><span data-stu-id="6c758-621">Attempting to log in during an unauthorized time of day for this account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-622"><span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**Fehler beim \_ Anmelden mit \_ wksta- \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="6c758-622"><span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**ERROR\_LOGIN\_WKSTA\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-623">1240 (0x4d8)</span><span class="sxs-lookup"><span data-stu-id="6c758-623">1240 (0x4D8)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-624">Das Konto ist nicht autorisiert, sich von dieser Station aus anzumelden.</span><span class="sxs-lookup"><span data-stu-id="6c758-624">The account is not authorized to log in from this station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-625"><span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**Fehler \_ hafte \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="6c758-625"><span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**ERROR\_INCORRECT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-626">1241 (0x4d9)</span><span class="sxs-lookup"><span data-stu-id="6c758-626">1241 (0x4D9)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-627">Die Netzwerkadresse konnte nicht für den angeforderten Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-627">The network address could not be used for the operation requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-628"><span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**Fehler \_ bereits \_ registriert**</span><span class="sxs-lookup"><span data-stu-id="6c758-628"><span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**ERROR\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-629">1242 (0x4da)</span><span class="sxs-lookup"><span data-stu-id="6c758-629">1242 (0x4DA)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-630">Der Dienst ist bereits registriert.</span><span class="sxs-lookup"><span data-stu-id="6c758-630">The service is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-631"><span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**Fehler \_ Dienst \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6c758-631"><span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**ERROR\_SERVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-632">1243 (0x4db)</span><span class="sxs-lookup"><span data-stu-id="6c758-632">1243 (0x4DB)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-633">Der angegebene Dienst ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6c758-633">The specified service does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-634"><span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**Fehler \_ nicht \_ authentifiziert**</span><span class="sxs-lookup"><span data-stu-id="6c758-634"><span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**ERROR\_NOT\_AUTHENTICATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-635">1244 (0x4dc)</span><span class="sxs-lookup"><span data-stu-id="6c758-635">1244 (0x4DC)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-636">Der angeforderte Vorgang wurde nicht ausgeführt, da der Benutzer nicht authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="6c758-636">The operation being requested was not performed because the user has not been authenticated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-637"><span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**Fehler \_ nicht \_ angemeldet \_ .**</span><span class="sxs-lookup"><span data-stu-id="6c758-637"><span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**ERROR\_NOT\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-638">1245 (0x4dd)</span><span class="sxs-lookup"><span data-stu-id="6c758-638">1245 (0x4DD)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-639">Der angeforderte Vorgang wurde nicht ausgeführt, da sich der Benutzer nicht am Netzwerk angemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="6c758-639">The operation being requested was not performed because the user has not logged on to the network.</span></span> <span data-ttu-id="6c758-640">Der angegebene Dienst ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6c758-640">The specified service does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-641"><span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**Fehler beim \_ fortsetzen**</span><span class="sxs-lookup"><span data-stu-id="6c758-641"><span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**ERROR\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-642">1246 (0x4de)</span><span class="sxs-lookup"><span data-stu-id="6c758-642">1246 (0x4DE)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-643">Fahren Sie mit der aktuell ausgeführten Arbeit fort.</span><span class="sxs-lookup"><span data-stu-id="6c758-643">Continue with work in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-644"><span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**Fehler \_ bereits \_ Initialisiert**</span><span class="sxs-lookup"><span data-stu-id="6c758-644"><span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**ERROR\_ALREADY\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-645">1247 (0x4df)</span><span class="sxs-lookup"><span data-stu-id="6c758-645">1247 (0x4DF)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-646">Es wurde versucht, eine Initialisierungs Operation auszuführen, wenn die Initialisierung bereits abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="6c758-646">An attempt was made to perform an initialization operation when initialization has already been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-647"><span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**Fehler \_ keine \_ weiteren \_ Geräte**</span><span class="sxs-lookup"><span data-stu-id="6c758-647"><span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**ERROR\_NO\_MORE\_DEVICES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-648">1248 (0x4e0)</span><span class="sxs-lookup"><span data-stu-id="6c758-648">1248 (0x4E0)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-649">Keine weiteren lokalen Geräte.</span><span class="sxs-lookup"><span data-stu-id="6c758-649">No more local devices.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-650"><span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**Fehler " \_ kein \_ solcher \_ Standort"**</span><span class="sxs-lookup"><span data-stu-id="6c758-650"><span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**ERROR\_NO\_SUCH\_SITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-651">1249 (0x4e1)</span><span class="sxs-lookup"><span data-stu-id="6c758-651">1249 (0x4E1)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-652">Die angegebene Site ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6c758-652">The specified site does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-653"><span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**Fehler \_ Domänen \_ Controller \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="6c758-653"><span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**ERROR\_DOMAIN\_CONTROLLER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-654">1250 (0x4e2)</span><span class="sxs-lookup"><span data-stu-id="6c758-654">1250 (0x4E2)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-655">Ein Domänen Controller mit dem angegebenen Namen ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6c758-655">A domain controller with the specified name already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-656"><span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**nur Fehler, \_ \_ Wenn eine \_ Verbindung besteht**</span><span class="sxs-lookup"><span data-stu-id="6c758-656"><span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**ERROR\_ONLY\_IF\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-657">1251 (0x4e3)</span><span class="sxs-lookup"><span data-stu-id="6c758-657">1251 (0x4E3)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-658">Dieser Vorgang wird nur unterstützt, wenn Sie mit dem Server verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="6c758-658">This operation is supported only when you are connected to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-659"><span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**Fehler beim über \_ Schreiben von \_ noChanges**</span><span class="sxs-lookup"><span data-stu-id="6c758-659"><span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**ERROR\_OVERRIDE\_NOCHANGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-660">1252 (0x4e4)</span><span class="sxs-lookup"><span data-stu-id="6c758-660">1252 (0x4E4)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-661">Das Gruppenrichtlinien Framework sollte die Erweiterung auch dann anrufen, wenn keine Änderungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6c758-661">The group policy framework should call the extension even if there are no changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-662"><span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**Fehler \_ beim \_ Benutzer \_ Profil.**</span><span class="sxs-lookup"><span data-stu-id="6c758-662"><span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**ERROR\_BAD\_USER\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-663">1253 (0x4e5)</span><span class="sxs-lookup"><span data-stu-id="6c758-663">1253 (0x4E5)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-664">Der angegebene Benutzer verfügt über kein gültiges Profil.</span><span class="sxs-lookup"><span data-stu-id="6c758-664">The specified user does not have a valid profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-665"><span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**\_der Fehler \_ wird \_ für \_ SSB nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="6c758-665"><span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**ERROR\_NOT\_SUPPORTED\_ON\_SBS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-666">1254 (0x4e6)</span><span class="sxs-lookup"><span data-stu-id="6c758-666">1254 (0x4E6)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-667">Dieser Vorgang wird auf Computern, auf denen Windows Server 2003 für Small Business Server ausgeführt wird, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c758-667">This operation is not supported on a computer running Windows Server 2003 for Small Business Server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-668"><span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**Fehler \_ Server wird \_ heruntergefahren \_ . \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-668"><span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**ERROR\_SERVER\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-669">1255 (0x4e7)</span><span class="sxs-lookup"><span data-stu-id="6c758-669">1255 (0x4E7)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-670">Der Server Computer wird heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="6c758-670">The server machine is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-671"><span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**Fehler \_ Host \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-671"><span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**ERROR\_HOST\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-672">1256 (0x4e8)</span><span class="sxs-lookup"><span data-stu-id="6c758-672">1256 (0x4E8)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-673">Das Remote System ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c758-673">The remote system is not available.</span></span> <span data-ttu-id="6c758-674">Informationen zur Netzwerkproblem Behandlung finden Sie in der Windows-Hilfe.</span><span class="sxs-lookup"><span data-stu-id="6c758-674">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-675"><span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**\_nicht- \_ Konto- \_ SID des Fehlers**</span><span class="sxs-lookup"><span data-stu-id="6c758-675"><span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**ERROR\_NON\_ACCOUNT\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-676">1257 (0x4e9)</span><span class="sxs-lookup"><span data-stu-id="6c758-676">1257 (0x4E9)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-677">Die angegebene Sicherheits-ID wird nicht von einer Konto Domäne abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6c758-677">The security identifier provided is not from an account domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-678"><span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**Fehler \_ nicht- \_ Domänen- \_ sid**</span><span class="sxs-lookup"><span data-stu-id="6c758-678"><span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**ERROR\_NON\_DOMAIN\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-679">1258 (0x4ea)</span><span class="sxs-lookup"><span data-stu-id="6c758-679">1258 (0x4EA)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-680">Die angegebene Sicherheits-ID verfügt über keine Domänen Komponente.</span><span class="sxs-lookup"><span data-stu-id="6c758-680">The security identifier provided does not have a domain component.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-681"><span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**Fehler " \_ AppHelp"- \_ Block**</span><span class="sxs-lookup"><span data-stu-id="6c758-681"><span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**ERROR\_APPHELP\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-682">1259 (0x4eb)</span><span class="sxs-lookup"><span data-stu-id="6c758-682">1259 (0x4EB)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-683">Das AppHelp-Dialogfeld wurde abgebrochen und verhindert somit das Starten der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6c758-683">AppHelp dialog canceled thus preventing the application from starting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-684"><span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**Fehler \_ Zugriff \_ \_ durch \_ Richtlinie deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="6c758-684"><span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**ERROR\_ACCESS\_DISABLED\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-685">1260 (0x4ec)</span><span class="sxs-lookup"><span data-stu-id="6c758-685">1260 (0x4EC)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-686">Dieses Programm wird durch die Gruppenrichtlinie blockiert.</span><span class="sxs-lookup"><span data-stu-id="6c758-686">This program is blocked by group policy.</span></span> <span data-ttu-id="6c758-687">Wenden Sie sich an Ihren Systemadministrator, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6c758-687">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-688"><span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**Fehler \_ beim \_ NAT- \_ Verbrauch.**</span><span class="sxs-lookup"><span data-stu-id="6c758-688"><span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**ERROR\_REG\_NAT\_CONSUMPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-689">1261 (0x4ed)</span><span class="sxs-lookup"><span data-stu-id="6c758-689">1261 (0x4ED)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-690">Ein Programm hat versucht, einen ungültigen Registerwert zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c758-690">A program attempt to use an invalid register value.</span></span> <span data-ttu-id="6c758-691">Wird normalerweise durch ein nicht initialisiertes Register verursacht.</span><span class="sxs-lookup"><span data-stu-id="6c758-691">Normally caused by an uninitialized register.</span></span> <span data-ttu-id="6c758-692">Dieser Fehler ist Itanium-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="6c758-692">This error is Itanium specific.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-693"><span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**Fehler " \_ cscshare" \_ Offline**</span><span class="sxs-lookup"><span data-stu-id="6c758-693"><span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**ERROR\_CSCSHARE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-694">1262 (0x4ee)</span><span class="sxs-lookup"><span data-stu-id="6c758-694">1262 (0x4EE)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-695">Die Freigabe ist zurzeit offline oder nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6c758-695">The share is currently offline or does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-696"><span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**\_PKINIT- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="6c758-696"><span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**ERROR\_PKINIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-697">1263 (0x4ef)</span><span class="sxs-lookup"><span data-stu-id="6c758-697">1263 (0x4EF)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-698">Im Kerberos-Protokoll ist ein Fehler aufgetreten, während das KDC-Zertifikat bei der Smartcard-Anmeldung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="6c758-698">The Kerberos protocol encountered an error while validating the KDC certificate during smartcard logon.</span></span> <span data-ttu-id="6c758-699">Weitere Informationen finden Sie im System Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="6c758-699">There is more information in the system event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-700"><span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**Fehler beim \_ Smartcard- \_ Subsystem. \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-700"><span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**ERROR\_SMARTCARD\_SUBSYSTEM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-701">1264 (0x4F 0)</span><span class="sxs-lookup"><span data-stu-id="6c758-701">1264 (0x4F0)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-702">Im Kerberos-Protokoll ist ein Fehler beim Versuch aufgetreten, das Smartcard-Subsystem zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c758-702">The Kerberos protocol encountered an error while attempting to utilize the smartcard subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-703"><span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**\_fehlerdowngrade \_ erkannt**</span><span class="sxs-lookup"><span data-stu-id="6c758-703"><span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**ERROR\_DOWNGRADE\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-704">1265 (0x4F 1)</span><span class="sxs-lookup"><span data-stu-id="6c758-704">1265 (0x4F1)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-705">Das System kann keine Verbindung mit einem Domänen Controller aufnehmen, um die Authentifizierungsanforderung zu bedienen.</span><span class="sxs-lookup"><span data-stu-id="6c758-705">The system cannot contact a domain controller to service the authentication request.</span></span> <span data-ttu-id="6c758-706">Versuchen Sie es später noch mal.</span><span class="sxs-lookup"><span data-stu-id="6c758-706">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-707"><span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**Fehler \_ Computer \_ gesperrt**</span><span class="sxs-lookup"><span data-stu-id="6c758-707"><span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**ERROR\_MACHINE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-708">1271 (0x4F)</span><span class="sxs-lookup"><span data-stu-id="6c758-708">1271 (0x4F7)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-709">Der Computer ist gesperrt und kann nicht ohne die Option "Force" heruntergefahren werden.</span><span class="sxs-lookup"><span data-stu-id="6c758-709">The machine is locked and cannot be shut down without the force option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-710"><span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**Fehler \_ Rückruf \_ hat \_ ungültige \_ Daten angegeben.**</span><span class="sxs-lookup"><span data-stu-id="6c758-710"><span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**ERROR\_CALLBACK\_SUPPLIED\_INVALID\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-711">1273 (0x4F 9)</span><span class="sxs-lookup"><span data-stu-id="6c758-711">1273 (0x4F9)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-712">Ein von der Anwendung definierter Rückruf hat beim Aufruf ungültige Daten angegeben.</span><span class="sxs-lookup"><span data-stu-id="6c758-712">An application-defined callback gave invalid data when called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-713"><span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**Fehler \_ Synchronisierungs- \_ Vordergrund \_ Aktualisierung \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="6c758-713"><span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**ERROR\_SYNC\_FOREGROUND\_REFRESH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-714">1274 (0x4fa)</span><span class="sxs-lookup"><span data-stu-id="6c758-714">1274 (0x4FA)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-715">Das Gruppenrichtlinien Framework sollte die Erweiterung bei der synchronen Aktualisierung der Vordergrund Richtlinie aufruft.</span><span class="sxs-lookup"><span data-stu-id="6c758-715">The group policy framework should call the extension in the synchronous foreground policy refresh.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-716"><span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**Fehler \_ Treiber \_ blockiert**</span><span class="sxs-lookup"><span data-stu-id="6c758-716"><span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**ERROR\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-717">1275 (0x4fb)</span><span class="sxs-lookup"><span data-stu-id="6c758-717">1275 (0x4FB)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-718">Das Laden dieses Treibers wurde blockiert.</span><span class="sxs-lookup"><span data-stu-id="6c758-718">This driver has been blocked from loading.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-719"><span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**Fehler \_ beim \_ importieren \_ der \_ nicht- \_ dll.**</span><span class="sxs-lookup"><span data-stu-id="6c758-719"><span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**ERROR\_INVALID\_IMPORT\_OF\_NON\_DLL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-720">1276 (0x4fc)</span><span class="sxs-lookup"><span data-stu-id="6c758-720">1276 (0x4FC)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-721">In einer Dynamic Link Library (dll) wurde auf ein Modul verwiesen, das weder eine DLL noch das ausführbare Image des Prozesses war.</span><span class="sxs-lookup"><span data-stu-id="6c758-721">A dynamic link library (DLL) referenced a module that was neither a DLL nor the process's executable image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-722"><span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**\_WebBlade für Fehler Zugriff \_ deaktiviert \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-722"><span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**ERROR\_ACCESS\_DISABLED\_WEBBLADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-723">1277 (0x4fd)</span><span class="sxs-lookup"><span data-stu-id="6c758-723">1277 (0x4FD)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-724">Dieses Programm kann nicht geöffnet werden, da es deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="6c758-724">Windows cannot open this program since it has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-725"><span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**Fehler \_ beim \_ Deaktivieren des \_ WebBlade- \_ Manipulations Diensts**</span><span class="sxs-lookup"><span data-stu-id="6c758-725"><span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**ERROR\_ACCESS\_DISABLED\_WEBBLADE\_TAMPER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-726">1278 (0x4fe)</span><span class="sxs-lookup"><span data-stu-id="6c758-726">1278 (0x4FE)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-727">Dieses Programm kann nicht geöffnet werden, da das Lizenz Erzwingungs System manipuliert oder beschädigt wurde.</span><span class="sxs-lookup"><span data-stu-id="6c758-727">Windows cannot open this program because the license enforcement system has been tampered with or become corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-728"><span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**Fehler beim Wiederherstellen. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-728"><span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**ERROR\_RECOVERY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-729">1279 (0x4ff)</span><span class="sxs-lookup"><span data-stu-id="6c758-729">1279 (0x4FF)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-730">Fehler beim Wiederherstellen einer Transaktion.</span><span class="sxs-lookup"><span data-stu-id="6c758-730">A transaction recover failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-731"><span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**Fehler \_ bereits \_ Fiber**</span><span class="sxs-lookup"><span data-stu-id="6c758-731"><span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**ERROR\_ALREADY\_FIBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-732">1280 (0x500)</span><span class="sxs-lookup"><span data-stu-id="6c758-732">1280 (0x500)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-733">Der aktuelle Thread wurde bereits in eine Fiber konvertiert.</span><span class="sxs-lookup"><span data-stu-id="6c758-733">The current thread has already been converted to a fiber.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-734"><span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**Fehler \_ bereits \_ Thread**</span><span class="sxs-lookup"><span data-stu-id="6c758-734"><span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**ERROR\_ALREADY\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-735">1281 (0x501)</span><span class="sxs-lookup"><span data-stu-id="6c758-735">1281 (0x501)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-736">Der aktuelle Thread wurde bereits aus einer Fiber konvertiert.</span><span class="sxs-lookup"><span data-stu-id="6c758-736">The current thread has already been converted from a fiber.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-737"><span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**Fehler \_ Stapel- \_ Puffer \_ Überlauf**</span><span class="sxs-lookup"><span data-stu-id="6c758-737"><span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**ERROR\_STACK\_BUFFER\_OVERRUN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-738">1282 (0x502)</span><span class="sxs-lookup"><span data-stu-id="6c758-738">1282 (0x502)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-739">Das System hat einen Überlauf eines Stapel basierten Puffers in dieser Anwendung erkannt.</span><span class="sxs-lookup"><span data-stu-id="6c758-739">The system detected an overrun of a stack-based buffer in this application.</span></span> <span data-ttu-id="6c758-740">Mit diesem Überlauf kann ein böswilliger Benutzer möglicherweise die Kontrolle über diese Anwendung erlangen.</span><span class="sxs-lookup"><span data-stu-id="6c758-740">This overrun could potentially allow a malicious user to gain control of this application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-741"><span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**Fehler \_ Parameter \_ Kontingent \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="6c758-741"><span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**ERROR\_PARAMETER\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-742">1283 (0x503)</span><span class="sxs-lookup"><span data-stu-id="6c758-742">1283 (0x503)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-743">Daten, die in einem der Parameter vorhanden sind, sind größer als die Funktion, die verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6c758-743">Data present in one of the parameters is more than the function can operate on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-744"><span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**Fehler \_ Debugger \_ inaktiv**</span><span class="sxs-lookup"><span data-stu-id="6c758-744"><span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**ERROR\_DEBUGGER\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-745">1284 (0x504)</span><span class="sxs-lookup"><span data-stu-id="6c758-745">1284 (0x504)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-746">Der Versuch, einen Vorgang für ein Debug-Objekt durchzuführen, ist fehlgeschlagen, da das Objekt gerade gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="6c758-746">An attempt to do an operation on a debug object failed because the object is in the process of being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-747"><span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**Fehler beim Laden der Fehler \_ Verzögerung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-747"><span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**ERROR\_DELAY\_LOAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-748">1285 (0x505)</span><span class="sxs-lookup"><span data-stu-id="6c758-748">1285 (0x505)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-749">Fehler beim Versuch, eine DLL oder eine Funktions Adresse in einer verzögert geladenen DLL zu laden.</span><span class="sxs-lookup"><span data-stu-id="6c758-749">An attempt to delay-load a .dll or get a function address in a delay-loaded .dll failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-750"><span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**VDM-Fehler ist unzulässig. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-750"><span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**ERROR\_VDM\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-751">1286 (0x506)</span><span class="sxs-lookup"><span data-stu-id="6c758-751">1286 (0x506)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-752">%1 ist eine 16-Bit-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6c758-752">%1 is a 16-bit application.</span></span> <span data-ttu-id="6c758-753">Sie verfügen nicht über die Berechtigungen zum Ausführen von 16-Bit-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="6c758-753">You do not have permissions to execute 16-bit applications.</span></span> <span data-ttu-id="6c758-754">Überprüfen Sie Ihre Berechtigungen mit dem Systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="6c758-754">Check your permissions with your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-755"><span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**\_unbekannter \_ Fehler.**</span><span class="sxs-lookup"><span data-stu-id="6c758-755"><span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**ERROR\_UNIDENTIFIED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-756">1287 (0x507)</span><span class="sxs-lookup"><span data-stu-id="6c758-756">1287 (0x507)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-757">Es sind nicht genügend Informationen vorhanden, um die Fehlerursache zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="6c758-757">Insufficient information exists to identify the cause of failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-758"><span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**Fehler \_ ungültiger \_ cruntime- \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="6c758-758"><span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**ERROR\_INVALID\_CRUNTIME\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-759">1288 (0x508)</span><span class="sxs-lookup"><span data-stu-id="6c758-759">1288 (0x508)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-760">Der an eine C-Lauf Zeitfunktion übergebenen Parameter ist falsch.</span><span class="sxs-lookup"><span data-stu-id="6c758-760">The parameter passed to a C runtime function is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-761"><span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**Fehler \_ über \_ VDL hinaus**</span><span class="sxs-lookup"><span data-stu-id="6c758-761"><span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**ERROR\_BEYOND\_VDL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-762">1289 (0x509)</span><span class="sxs-lookup"><span data-stu-id="6c758-762">1289 (0x509)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-763">Der Vorgang ist über die gültige Daten Länge der Datei hinaus aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6c758-763">The operation occurred beyond the valid data length of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-764"><span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**nicht \_ kompatibler \_ Dienst- \_ sid- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="6c758-764"><span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**ERROR\_INCOMPATIBLE\_SERVICE\_SID\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-765">1290 (0x50A)</span><span class="sxs-lookup"><span data-stu-id="6c758-765">1290 (0x50A)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-766">Fehler beim Starten des Diensts, da mindestens ein Dienst im selben Prozess über eine nicht kompatible Dienst-SID-Typ-Einstellung verfügt.</span><span class="sxs-lookup"><span data-stu-id="6c758-766">The service start failed since one or more services in the same process have an incompatible service SID type setting.</span></span> <span data-ttu-id="6c758-767">Ein Dienst mit dem SID-Typ "eingeschränkter Dienst" kann nur im gleichen Prozess mit anderen Diensten mit eingeschränktem SID-Typ vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6c758-767">A service with restricted service SID type can only coexist in the same process with other services with a restricted SID type.</span></span> <span data-ttu-id="6c758-768">Wenn der Dienst-SID-Typ für diesen Dienst soeben konfiguriert wurde, muss der Hostingprozess neu gestartet werden, um diesen Dienst zu starten.</span><span class="sxs-lookup"><span data-stu-id="6c758-768">If the service SID type for this service was just configured, the hosting process must be restarted in order to start this service.</span></span>

<span data-ttu-id="6c758-769">Unter Windows Server 2003 und Windows XP kann ein uneingeschränkter Dienst nicht in demselben Prozess wie andere Dienste nebeneinander vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6c758-769">On Windows Server 2003 and Windows XP, an unrestricted service cannot coexist in the same process with other services.</span></span> <span data-ttu-id="6c758-770">Der Dienst mit dem SID-Typ "uneingeschränkter Dienst" muss in einen eigenen Prozess verschoben werden, um diesen Dienst zu starten.</span><span class="sxs-lookup"><span data-stu-id="6c758-770">The service with the unrestricted service SID type must be moved to an owned process in order to start this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-771"><span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**Fehler \_ Treiber \_ Prozess \_ beendet**</span><span class="sxs-lookup"><span data-stu-id="6c758-771"><span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**ERROR\_DRIVER\_PROCESS\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-772">1291 (0x50B)</span><span class="sxs-lookup"><span data-stu-id="6c758-772">1291 (0x50B)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-773">Der Prozess, der den Treiber für dieses Gerät gehostet, wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="6c758-773">The process hosting the driver for this device has been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-774"><span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**Fehler \_ Implementierungs \_ Limit**</span><span class="sxs-lookup"><span data-stu-id="6c758-774"><span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**ERROR\_IMPLEMENTATION\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-775">1292 (0x50C)</span><span class="sxs-lookup"><span data-stu-id="6c758-775">1292 (0x50C)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-776">Ein Vorgang hat versucht, einen von der Implementierung definierten Grenzwert zu überschreiten.</span><span class="sxs-lookup"><span data-stu-id="6c758-776">An operation attempted to exceed an implementation-defined limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-777"><span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**der Fehler \_ Prozess \_ ist \_ geschützt.**</span><span class="sxs-lookup"><span data-stu-id="6c758-777"><span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**ERROR\_PROCESS\_IS\_PROTECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-778">1293 (0x50D)</span><span class="sxs-lookup"><span data-stu-id="6c758-778">1293 (0x50D)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-779">Entweder der Ziel Prozess oder der enthaltende Prozess des Zielthreads ist ein geschützter Prozess.</span><span class="sxs-lookup"><span data-stu-id="6c758-779">Either the target process, or the target thread's containing process, is a protected process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-780"><span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**Fehler \_ Dienst hat den \_ \_ Client \_ Rückstand benachrichtigt**</span><span class="sxs-lookup"><span data-stu-id="6c758-780"><span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**ERROR\_SERVICE\_NOTIFY\_CLIENT\_LAGGING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-781">1294 (0x50E)</span><span class="sxs-lookup"><span data-stu-id="6c758-781">1294 (0x50E)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-782">Der Dienst Benachrichtigungs Client geht zu weit hinter dem aktuellen Status der Dienste auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="6c758-782">The service notification client is lagging too far behind the current state of services in the machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-783"><span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**Fehler Datenträger \_ \_ Kontingent \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="6c758-783"><span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**ERROR\_DISK\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-784">1295 (0x50F)</span><span class="sxs-lookup"><span data-stu-id="6c758-784">1295 (0x50F)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-785">Fehler beim angeforderten Datei Vorgang, weil das Speicher Kontingent überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="6c758-785">The requested file operation failed because the storage quota was exceeded.</span></span> <span data-ttu-id="6c758-786">Verschieben Sie Dateien an einen anderen Speicherort, oder löschen Sie unnötige Dateien, um Speicherplatz freizugeben.</span><span class="sxs-lookup"><span data-stu-id="6c758-786">To free up disk space, move files to a different location or delete unnecessary files.</span></span> <span data-ttu-id="6c758-787">Wenden Sie sich an Ihren Systemadministrator, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6c758-787">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-788"><span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**Fehler \_ Inhalt \_ blockiert**</span><span class="sxs-lookup"><span data-stu-id="6c758-788"><span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**ERROR\_CONTENT\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-789">1296 (0x510)</span><span class="sxs-lookup"><span data-stu-id="6c758-789">1296 (0x510)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-790">Der angeforderte Datei Vorgang ist fehlgeschlagen, da die Speicher Richtlinie diese Art von Datei blockiert.</span><span class="sxs-lookup"><span data-stu-id="6c758-790">The requested file operation failed because the storage policy blocks that type of file.</span></span> <span data-ttu-id="6c758-791">Wenden Sie sich an Ihren Systemadministrator, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6c758-791">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-792"><span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**Fehler bei \_ inkompatibler \_ Dienst \_ Berechtigung**</span><span class="sxs-lookup"><span data-stu-id="6c758-792"><span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**ERROR\_INCOMPATIBLE\_SERVICE\_PRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-793">1297 (0x511)</span><span class="sxs-lookup"><span data-stu-id="6c758-793">1297 (0x511)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-794">Eine Berechtigung, die der Dienst benötigt, um ordnungsgemäß zu funktionieren, ist in der Dienst Konto Konfiguration nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6c758-794">A privilege that the service requires to function properly does not exist in the service account configuration.</span></span> <span data-ttu-id="6c758-795">Sie können das Microsoft Management Console (MMC)-Snap-in (Services. msc) und das lokale Sicherheitseinstellungen MMC-Snap-in (secpol. msc) verwenden, um die Dienst Konfiguration und die Konto Konfiguration anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6c758-795">You may use the Services Microsoft Management Console (MMC) snap-in (services.msc) and the Local Security Settings MMC snap-in (secpol.msc) to view the service configuration and the account configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-796"><span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**Fehler-App-Absturz \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c758-796"><span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**ERROR\_APP\_HANG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-797">1298 (0x512)</span><span class="sxs-lookup"><span data-stu-id="6c758-797">1298 (0x512)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-798">Ein Thread, der an diesem Vorgang beteiligt ist, reagiert anscheinend nicht.</span><span class="sxs-lookup"><span data-stu-id="6c758-798">A thread involved in this operation appears to be unresponsive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c758-799"><span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**\_ungültige \_ Bezeichnung.**</span><span class="sxs-lookup"><span data-stu-id="6c758-799"><span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**ERROR\_INVALID\_LABEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c758-800">1299 (0x513)</span><span class="sxs-lookup"><span data-stu-id="6c758-800">1299 (0x513)</span></span>
</dt> <dt>



<span data-ttu-id="6c758-801">Gibt an, dass eine bestimmte Sicherheits-ID nicht als Bezeichnung eines Objekts zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6c758-801">Indicates a particular Security ID may not be assigned as the label of an object.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="6c758-802">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c758-802">Requirements</span></span>



| <span data-ttu-id="6c758-803">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c758-803">Requirement</span></span> | <span data-ttu-id="6c758-804">Wert</span><span class="sxs-lookup"><span data-stu-id="6c758-804">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c758-805">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c758-805">Minimum supported client</span></span><br/> | <span data-ttu-id="6c758-806">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c758-806">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6c758-807">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c758-807">Minimum supported server</span></span><br/> | <span data-ttu-id="6c758-808">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c758-808">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c758-809">Header</span><span class="sxs-lookup"><span data-stu-id="6c758-809">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c758-810"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c758-810"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c758-811">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c758-811">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c758-812">System Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="6c758-812">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




