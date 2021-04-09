---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 0-499 und ist für Entwickler bestimmt.
ms.assetid: cacb0aec-d438-4875-a96e-4e0239fdc6ba
title: System Fehler Codes (0-499) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 413d9674f511bd49df12267b60d6c6c3dac366aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861204"
---
# <a name="system-error-codes-0-499"></a><span data-ttu-id="af045-103">System Fehler Codes (0-499)</span><span class="sxs-lookup"><span data-stu-id="af045-103">System Error Codes (0-499)</span></span>

> [!NOTE]
> <span data-ttu-id="af045-104">Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen.</span><span class="sxs-lookup"><span data-stu-id="af045-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="af045-105">Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="af045-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="af045-106">In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) (Fehler 0 bis 499) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="af045-106">The following list describes [system error codes](system-error-codes.md) (errors 0 to 499).</span></span> <span data-ttu-id="af045-107">Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="af045-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="af045-108">Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".</span><span class="sxs-lookup"><span data-stu-id="af045-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="af045-109"><span id="ERROR_SUCCESS"></span><span id="error_success"></span>**Fehler \_ erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="af045-109"><span id="ERROR_SUCCESS"></span><span id="error_success"></span>**ERROR\_SUCCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-110">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="af045-110">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="af045-111">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="af045-111">The operation completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-112"><span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**\_ungültige \_ Funktion.**</span><span class="sxs-lookup"><span data-stu-id="af045-112"><span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**ERROR\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="af045-113">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="af045-114">Falsche Funktion.</span><span class="sxs-lookup"><span data-stu-id="af045-114">Incorrect function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-115"><span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**Fehler \_ Datei \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="af045-115"><span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**ERROR\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-116">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="af045-116">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="af045-117">Die angegebene Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="af045-117">The system cannot find the file specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-118"><span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**der Fehler \_ Pfad wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="af045-118"><span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**ERROR\_PATH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-119">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="af045-119">3 (0x3)</span></span>
</dt> <dt>



<span data-ttu-id="af045-120">Das System kann den angegebenen Pfad nicht finden.</span><span class="sxs-lookup"><span data-stu-id="af045-120">The system cannot find the path specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-121"><span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**Fehler \_ zu \_ viele \_ geöffnete \_ Dateien**</span><span class="sxs-lookup"><span data-stu-id="af045-121"><span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**ERROR\_TOO\_MANY\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-122">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="af045-122">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="af045-123">Das System kann die Datei nicht öffnen.</span><span class="sxs-lookup"><span data-stu-id="af045-123">The system cannot open the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-124"><span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**Fehler \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="af045-124"><span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-125">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="af045-125">5 (0x5)</span></span>
</dt> <dt>



<span data-ttu-id="af045-126">Zugriff verweigert.“</span><span class="sxs-lookup"><span data-stu-id="af045-126">Access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-127"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**Fehler bei \_ ungültigem \_ handle**</span><span class="sxs-lookup"><span data-stu-id="af045-127"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-128">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="af045-128">6 (0x6)</span></span>
</dt> <dt>



<span data-ttu-id="af045-129">Das Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="af045-129">The handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-130"><span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**Fehler-Arena wurde durchlaufen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="af045-130"><span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**ERROR\_ARENA\_TRASHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-131">7 (0x7)</span><span class="sxs-lookup"><span data-stu-id="af045-131">7 (0x7)</span></span>
</dt> <dt>



<span data-ttu-id="af045-132">Die Speicher Kontroll Blöcke wurden zerstört.</span><span class="sxs-lookup"><span data-stu-id="af045-132">The storage control blocks were destroyed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-133"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="af045-133"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-134">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="af045-134">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="af045-135">Für die Verarbeitung dieses Befehls sind nicht genügend Speicherressourcen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af045-135">Not enough memory resources are available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-136"><span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**\_ungültiger \_ Block**</span><span class="sxs-lookup"><span data-stu-id="af045-136"><span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**ERROR\_INVALID\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-137">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="af045-137">9 (0x9)</span></span>
</dt> <dt>



<span data-ttu-id="af045-138">Die Speicher Steuerungs Block-Adresse ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="af045-138">The storage control block address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-139"><span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**Fehler \_ hafte \_ Umgebung**</span><span class="sxs-lookup"><span data-stu-id="af045-139"><span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**ERROR\_BAD\_ENVIRONMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-140">10 (0xa)</span><span class="sxs-lookup"><span data-stu-id="af045-140">10 (0xA)</span></span>
</dt> <dt>



<span data-ttu-id="af045-141">Die Umgebung ist falsch.</span><span class="sxs-lookup"><span data-stu-id="af045-141">The environment is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-142"><span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**fehlerhaftes \_ \_ Format**</span><span class="sxs-lookup"><span data-stu-id="af045-142"><span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**ERROR\_BAD\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-143">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="af045-143">11 (0xB)</span></span>
</dt> <dt>



<span data-ttu-id="af045-144">Es wurde versucht, ein Programm mit einem falschen Format zu laden.</span><span class="sxs-lookup"><span data-stu-id="af045-144">An attempt was made to load a program with an incorrect format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-145"><span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**Fehler bei \_ ungültigem \_ Zugriff**</span><span class="sxs-lookup"><span data-stu-id="af045-145"><span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**ERROR\_INVALID\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-146">12 (0xc)</span><span class="sxs-lookup"><span data-stu-id="af045-146">12 (0xC)</span></span>
</dt> <dt>



<span data-ttu-id="af045-147">Der Zugriffs Code ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="af045-147">The access code is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-148"><span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**\_ungültige \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="af045-148"><span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**ERROR\_INVALID\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-149">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="af045-149">13 (0xD)</span></span>
</dt> <dt>



<span data-ttu-id="af045-150">Die Daten sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="af045-150">The data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-151"><span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**Fehler beim \_ outo-Memory**</span><span class="sxs-lookup"><span data-stu-id="af045-151"><span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**ERROR\_OUTOFMEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-152">14 (0xe)</span><span class="sxs-lookup"><span data-stu-id="af045-152">14 (0xE)</span></span>
</dt> <dt>



<span data-ttu-id="af045-153">Für diesen Vorgang ist nicht genügend Speicher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af045-153">Not enough storage is available to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-154"><span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**\_ungültiges \_ Laufwerk**</span><span class="sxs-lookup"><span data-stu-id="af045-154"><span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**ERROR\_INVALID\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-155">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="af045-155">15 (0xF)</span></span>
</dt> <dt>



<span data-ttu-id="af045-156">Das angegebene Laufwerk kann nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="af045-156">The system cannot find the drive specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-157"><span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**\_Aktuelles \_ Verzeichnis für Fehler**</span><span class="sxs-lookup"><span data-stu-id="af045-157"><span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**ERROR\_CURRENT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-158">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="af045-158">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="af045-159">Das Verzeichnis kann nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="af045-159">The directory cannot be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-160"><span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**Fehler \_ beim \_ gleichen \_ Gerät**</span><span class="sxs-lookup"><span data-stu-id="af045-160"><span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**ERROR\_NOT\_SAME\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-161">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="af045-161">17 (0x11)</span></span>
</dt> <dt>



<span data-ttu-id="af045-162">Das System kann die Datei nicht auf ein anderes Laufwerk verschieben.</span><span class="sxs-lookup"><span data-stu-id="af045-162">The system cannot move the file to a different disk drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-163"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**Fehler \_ keine \_ weiteren \_ Dateien**</span><span class="sxs-lookup"><span data-stu-id="af045-163"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-164">18 (0x12)</span><span class="sxs-lookup"><span data-stu-id="af045-164">18 (0x12)</span></span>
</dt> <dt>



<span data-ttu-id="af045-165">Es sind keine weiteren Dateien vorhanden.</span><span class="sxs-lookup"><span data-stu-id="af045-165">There are no more files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-166"><span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**Fehler beim \_ schreiben \_ schützen**</span><span class="sxs-lookup"><span data-stu-id="af045-166"><span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**ERROR\_WRITE\_PROTECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-167">19 (0x13)</span><span class="sxs-lookup"><span data-stu-id="af045-167">19 (0x13)</span></span>
</dt> <dt>



<span data-ttu-id="af045-168">Das Medium ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="af045-168">The media is write protected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-169"><span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**Fehler \_ hafte \_ Einheit**</span><span class="sxs-lookup"><span data-stu-id="af045-169"><span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**ERROR\_BAD\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-170">20 (0x14)</span><span class="sxs-lookup"><span data-stu-id="af045-170">20 (0x14)</span></span>
</dt> <dt>



<span data-ttu-id="af045-171">Das angegebene Gerät kann nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="af045-171">The system cannot find the device specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-172"><span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**Fehler \_ nicht \_ bereit**</span><span class="sxs-lookup"><span data-stu-id="af045-172"><span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**ERROR\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-173">21 (0x15)</span><span class="sxs-lookup"><span data-stu-id="af045-173">21 (0x15)</span></span>
</dt> <dt>



<span data-ttu-id="af045-174">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="af045-174">The device is not ready.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-175"><span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**fehlerhafter \_ \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="af045-175"><span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**ERROR\_BAD\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-176">22 (0x16)</span><span class="sxs-lookup"><span data-stu-id="af045-176">22 (0x16)</span></span>
</dt> <dt>



<span data-ttu-id="af045-177">Das Gerät erkennt den Befehl nicht.</span><span class="sxs-lookup"><span data-stu-id="af045-177">The device does not recognize the command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-178"><span id="ERROR_CRC"></span><span id="error_crc"></span>**Fehler \_ CRC**</span><span class="sxs-lookup"><span data-stu-id="af045-178"><span id="ERROR_CRC"></span><span id="error_crc"></span>**ERROR\_CRC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-179">23 (0x17)</span><span class="sxs-lookup"><span data-stu-id="af045-179">23 (0x17)</span></span>
</dt> <dt>



<span data-ttu-id="af045-180">Datenfehler (zyklische Redundanz Überprüfung).</span><span class="sxs-lookup"><span data-stu-id="af045-180">Data error (cyclic redundancy check).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-181"><span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**Fehler \_ hafte \_ Länge**</span><span class="sxs-lookup"><span data-stu-id="af045-181"><span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**ERROR\_BAD\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-182">24 (0x18)</span><span class="sxs-lookup"><span data-stu-id="af045-182">24 (0x18)</span></span>
</dt> <dt>



<span data-ttu-id="af045-183">Das Programm hat einen Befehl ausgegeben, aber die Befehls Länge ist falsch.</span><span class="sxs-lookup"><span data-stu-id="af045-183">The program issued a command but the command length is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-184"><span id="ERROR_SEEK"></span><span id="error_seek"></span>**Fehler \_ Suche**</span><span class="sxs-lookup"><span data-stu-id="af045-184"><span id="ERROR_SEEK"></span><span id="error_seek"></span>**ERROR\_SEEK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-185">25 (0x19)</span><span class="sxs-lookup"><span data-stu-id="af045-185">25 (0x19)</span></span>
</dt> <dt>



<span data-ttu-id="af045-186">Das Laufwerk kann keinen bestimmten Bereich oder Nachverfolgung auf dem Datenträger finden.</span><span class="sxs-lookup"><span data-stu-id="af045-186">The drive cannot locate a specific area or track on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-187"><span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**Fehler \_ nicht \_ DOS-Datenträger \_**</span><span class="sxs-lookup"><span data-stu-id="af045-187"><span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERROR\_NOT\_DOS\_DISK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-188">26 (0x1A)</span><span class="sxs-lookup"><span data-stu-id="af045-188">26 (0x1A)</span></span>
</dt> <dt>



<span data-ttu-id="af045-189">Auf den angegebenen Datenträger oder die angegebene Diskette kann nicht zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="af045-189">The specified disk or diskette cannot be accessed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-190"><span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**Fehler \_ Sektor \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="af045-190"><span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**ERROR\_SECTOR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-191">27 (0x1B)</span><span class="sxs-lookup"><span data-stu-id="af045-191">27 (0x1B)</span></span>
</dt> <dt>



<span data-ttu-id="af045-192">Das Laufwerk kann den angeforderten Sektor nicht finden.</span><span class="sxs-lookup"><span data-stu-id="af045-192">The drive cannot find the sector requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-193"><span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**Fehler \_ \_ in \_ Papier**</span><span class="sxs-lookup"><span data-stu-id="af045-193"><span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**ERROR\_OUT\_OF\_PAPER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-194">28 (0x1C)</span><span class="sxs-lookup"><span data-stu-id="af045-194">28 (0x1C)</span></span>
</dt> <dt>



<span data-ttu-id="af045-195">Der Drucker ist nicht mehr im Papier.</span><span class="sxs-lookup"><span data-stu-id="af045-195">The printer is out of paper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-196"><span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**Fehler \_ Schreib \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="af045-196"><span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**ERROR\_WRITE\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-197">29 (0x1D)</span><span class="sxs-lookup"><span data-stu-id="af045-197">29 (0x1D)</span></span>
</dt> <dt>



<span data-ttu-id="af045-198">Das System kann nicht auf das angegebene Gerät schreiben.</span><span class="sxs-lookup"><span data-stu-id="af045-198">The system cannot write to the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-199"><span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**Fehler beim \_ Lesen \_ des Fehlers**</span><span class="sxs-lookup"><span data-stu-id="af045-199"><span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**ERROR\_READ\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-200">30 (0x1E)</span><span class="sxs-lookup"><span data-stu-id="af045-200">30 (0x1E)</span></span>
</dt> <dt>



<span data-ttu-id="af045-201">Das System kann das angegebene Gerät nicht lesen.</span><span class="sxs-lookup"><span data-stu-id="af045-201">The system cannot read from the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-202"><span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**Fehler \_ gen \_ fehlgeschlagen**</span><span class="sxs-lookup"><span data-stu-id="af045-202"><span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**ERROR\_GEN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-203">31 (0x1F)</span><span class="sxs-lookup"><span data-stu-id="af045-203">31 (0x1F)</span></span>
</dt> <dt>



<span data-ttu-id="af045-204">Ein an das System angefügtes Gerät funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="af045-204">A device attached to the system is not functioning.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-205"><span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**Verletzung der Fehler \_ Freigabe \_**</span><span class="sxs-lookup"><span data-stu-id="af045-205"><span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**ERROR\_SHARING\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-206">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="af045-206">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="af045-207">Der Prozess kann nicht auf die Datei zugreifen, da sie bereits von einem anderen Prozess verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="af045-207">The process cannot access the file because it is being used by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-208"><span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**Fehler \_ Sperr \_ Verletzung**</span><span class="sxs-lookup"><span data-stu-id="af045-208"><span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**ERROR\_LOCK\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-209">33 (0x21)</span><span class="sxs-lookup"><span data-stu-id="af045-209">33 (0x21)</span></span>
</dt> <dt>



<span data-ttu-id="af045-210">Der Prozess kann nicht auf die Datei zugreifen, da sie teilweise von einem anderen Prozess gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="af045-210">The process cannot access the file because another process has locked a portion of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-211"><span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**Fehler \_ hafte \_ Festplatte**</span><span class="sxs-lookup"><span data-stu-id="af045-211"><span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**ERROR\_WRONG\_DISK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-212">34 (0x22)</span><span class="sxs-lookup"><span data-stu-id="af045-212">34 (0x22)</span></span>
</dt> <dt>



<span data-ttu-id="af045-213">Die falsche Diskette befindet sich im Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="af045-213">The wrong diskette is in the drive.</span></span> <span data-ttu-id="af045-214">Fügen Sie %2 (Volumeseriennummer: %3) in Laufwerk %1 ein.</span><span class="sxs-lookup"><span data-stu-id="af045-214">Insert %2 (Volume Serial Number: %3) into drive %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-215"><span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**Fehler \_ Freigabe \_ Puffer \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="af045-215"><span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**ERROR\_SHARING\_BUFFER\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-216">36 (0x24)</span><span class="sxs-lookup"><span data-stu-id="af045-216">36 (0x24)</span></span>
</dt> <dt>



<span data-ttu-id="af045-217">Zu viele Dateien für die Freigabe geöffnet.</span><span class="sxs-lookup"><span data-stu-id="af045-217">Too many files opened for sharing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-218"><span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**Fehler \_ handle \_ EOF**</span><span class="sxs-lookup"><span data-stu-id="af045-218"><span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**ERROR\_HANDLE\_EOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-219">38 (0x26)</span><span class="sxs-lookup"><span data-stu-id="af045-219">38 (0x26)</span></span>
</dt> <dt>



<span data-ttu-id="af045-220">Das Ende der Datei wurde erreicht.</span><span class="sxs-lookup"><span data-stu-id="af045-220">Reached the end of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-221"><span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**Fehler \_ beim \_ \_ vollständigen Datenträger.**</span><span class="sxs-lookup"><span data-stu-id="af045-221"><span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**ERROR\_HANDLE\_DISK\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-222">39 (0x27)</span><span class="sxs-lookup"><span data-stu-id="af045-222">39 (0x27)</span></span>
</dt> <dt>



<span data-ttu-id="af045-223">Der Datenträger ist voll.</span><span class="sxs-lookup"><span data-stu-id="af045-223">The disk is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-224"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**Fehler \_ nicht \_ unterstützt**</span><span class="sxs-lookup"><span data-stu-id="af045-224"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-225">50 (0x32)</span><span class="sxs-lookup"><span data-stu-id="af045-225">50 (0x32)</span></span>
</dt> <dt>



<span data-ttu-id="af045-226">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="af045-226">The request is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-227"><span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**Fehler- \_ REM \_ nicht \_ auflisten**</span><span class="sxs-lookup"><span data-stu-id="af045-227"><span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERROR\_REM\_NOT\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-228">51 (0x33)</span><span class="sxs-lookup"><span data-stu-id="af045-228">51 (0x33)</span></span>
</dt> <dt>



<span data-ttu-id="af045-229">Der Netzwerkpfad kann nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="af045-229">Windows cannot find the network path.</span></span> <span data-ttu-id="af045-230">Überprüfen Sie, ob der Netzwerkpfad richtig ist und der Zielcomputer nicht ausgelastet oder ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="af045-230">Verify that the network path is correct and the destination computer is not busy or turned off.</span></span> <span data-ttu-id="af045-231">Wenn Windows den Netzwerkpfad noch immer nicht finden kann, wenden Sie sich an Ihren Netzwerkadministrator.</span><span class="sxs-lookup"><span data-stu-id="af045-231">If Windows still cannot find the network path, contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-232"><span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**Fehler beim \_ DUP- \_ Namen**</span><span class="sxs-lookup"><span data-stu-id="af045-232"><span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**ERROR\_DUP\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-233">52 (0x34)</span><span class="sxs-lookup"><span data-stu-id="af045-233">52 (0x34)</span></span>
</dt> <dt>



<span data-ttu-id="af045-234">Sie waren nicht verbunden, weil im Netzwerk ein doppelter Name vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="af045-234">You were not connected because a duplicate name exists on the network.</span></span> <span data-ttu-id="af045-235">Wechseln Sie beim beitreten zu einer Domäne in der Systemsteuerung zum System, um den Computernamen zu ändern, und versuchen Sie es noch mal.</span><span class="sxs-lookup"><span data-stu-id="af045-235">If joining a domain, go to System in Control Panel to change the computer name and try again.</span></span> <span data-ttu-id="af045-236">Wenn Sie einer Arbeitsgruppe beitreten, wählen Sie einen anderen Arbeitsgruppen Namen aus.</span><span class="sxs-lookup"><span data-stu-id="af045-236">If joining a workgroup, choose another workgroup name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-237"><span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**Fehler \_ beim \_ netpath.**</span><span class="sxs-lookup"><span data-stu-id="af045-237"><span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**ERROR\_BAD\_NETPATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-238">53 (0x35)</span><span class="sxs-lookup"><span data-stu-id="af045-238">53 (0x35)</span></span>
</dt> <dt>



<span data-ttu-id="af045-239">Der Netzwerkpfad wurde nicht gefunden.“</span><span class="sxs-lookup"><span data-stu-id="af045-239">The network path was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-240"><span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**Fehler \_ Netzwerk \_ ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="af045-240"><span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**ERROR\_NETWORK\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-241">54 (0x36)</span><span class="sxs-lookup"><span data-stu-id="af045-241">54 (0x36)</span></span>
</dt> <dt>



<span data-ttu-id="af045-242">Das Netzwerk ist ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="af045-242">The network is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-243"><span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**Fehler \_ dev ist \_ nicht \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="af045-243"><span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**ERROR\_DEV\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-244">55 (0x37)</span><span class="sxs-lookup"><span data-stu-id="af045-244">55 (0x37)</span></span>
</dt> <dt>



<span data-ttu-id="af045-245">Die angegebene Netzwerkressource oder das angegebene Gerät ist nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af045-245">The specified network resource or device is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-246"><span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**Fehler \_ zu \_ viele \_ cmds**</span><span class="sxs-lookup"><span data-stu-id="af045-246"><span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**ERROR\_TOO\_MANY\_CMDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-247">56 (0x38)</span><span class="sxs-lookup"><span data-stu-id="af045-247">56 (0x38)</span></span>
</dt> <dt>



<span data-ttu-id="af045-248">Der Netzwerk-BIOS-Befehls Grenzwert wurde erreicht.</span><span class="sxs-lookup"><span data-stu-id="af045-248">The network BIOS command limit has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-249"><span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**Fehler beim \_ ADAP- \_ HDW. \_**</span><span class="sxs-lookup"><span data-stu-id="af045-249"><span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**ERROR\_ADAP\_HDW\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-250">57 (0x39)</span><span class="sxs-lookup"><span data-stu-id="af045-250">57 (0x39)</span></span>
</dt> <dt>



<span data-ttu-id="af045-251">Es ist ein Hardwarefehler im Netzwerkadapter aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="af045-251">A network adapter hardware error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-252"><span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**Fehler bei fehlerhafter Netzwerk Zuweisung. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="af045-252"><span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**ERROR\_BAD\_NET\_RESP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-253">58 (0x3a)</span><span class="sxs-lookup"><span data-stu-id="af045-253">58 (0x3A)</span></span>
</dt> <dt>



<span data-ttu-id="af045-254">Der angegebene Server kann den angeforderten Vorgang nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="af045-254">The specified server cannot perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-255"><span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**Fehler beim \_ unexp \_ net \_ Err.**</span><span class="sxs-lookup"><span data-stu-id="af045-255"><span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**ERROR\_UNEXP\_NET\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-256">59 (0x3B)</span><span class="sxs-lookup"><span data-stu-id="af045-256">59 (0x3B)</span></span>
</dt> <dt>



<span data-ttu-id="af045-257">Unerwarteter Netzwerkfehler.</span><span class="sxs-lookup"><span data-stu-id="af045-257">An unexpected network error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-258"><span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**Fehler \_ hafte \_ REM- \_ ADAP**</span><span class="sxs-lookup"><span data-stu-id="af045-258"><span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ERROR\_BAD\_REM\_ADAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-259">60 (0x3C)</span><span class="sxs-lookup"><span data-stu-id="af045-259">60 (0x3C)</span></span>
</dt> <dt>



<span data-ttu-id="af045-260">Der Remote Adapter ist nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="af045-260">The remote adapter is not compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-261"><span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**Fehler \_ printq \_ Full**</span><span class="sxs-lookup"><span data-stu-id="af045-261"><span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**ERROR\_PRINTQ\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-262">61 (0x3D)</span><span class="sxs-lookup"><span data-stu-id="af045-262">61 (0x3D)</span></span>
</dt> <dt>



<span data-ttu-id="af045-263">Die Drucker Warteschlange ist voll.</span><span class="sxs-lookup"><span data-stu-id="af045-263">The printer queue is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-264"><span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**Fehler \_ kein \_ \_ spoolspeicher.**</span><span class="sxs-lookup"><span data-stu-id="af045-264"><span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**ERROR\_NO\_SPOOL\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-265">62 (0x3e)</span><span class="sxs-lookup"><span data-stu-id="af045-265">62 (0x3E)</span></span>
</dt> <dt>



<span data-ttu-id="af045-266">Der Speicherplatz zum Speichern der Datei, die gedruckt werden soll, ist auf dem Server nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af045-266">Space to store the file waiting to be printed is not available on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-267"><span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**Fehler beim \_ Drucken \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="af045-267"><span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**ERROR\_PRINT\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-268">63 (0x3f)</span><span class="sxs-lookup"><span data-stu-id="af045-268">63 (0x3F)</span></span>
</dt> <dt>



<span data-ttu-id="af045-269">Die Datei, die darauf wartet, gedruckt zu werden, wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="af045-269">Your file waiting to be printed was deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-270"><span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**NetName-Fehler wurde \_ \_ gelöscht.**</span><span class="sxs-lookup"><span data-stu-id="af045-270"><span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**ERROR\_NETNAME\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-271">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="af045-271">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="af045-272">Der angegebene Netzwerkname ist nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af045-272">The specified network name is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-273"><span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**Fehler beim \_ Netzwerk \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="af045-273"><span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**ERROR\_NETWORK\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-274">65 (0x41)</span><span class="sxs-lookup"><span data-stu-id="af045-274">65 (0x41)</span></span>
</dt> <dt>



<span data-ttu-id="af045-275">Der Netzwerk Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="af045-275">Network access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-276"><span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**fehlerhafter \_ \_ \_ Entwicklungstyp**</span><span class="sxs-lookup"><span data-stu-id="af045-276"><span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**ERROR\_BAD\_DEV\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-277">66 (0x42)</span><span class="sxs-lookup"><span data-stu-id="af045-277">66 (0x42)</span></span>
</dt> <dt>



<span data-ttu-id="af045-278">Der Netzwerk Ressourcentyp ist nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="af045-278">The network resource type is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-279"><span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**Fehler bei fehlerhafter \_ \_ Netzwerk \_ Name**</span><span class="sxs-lookup"><span data-stu-id="af045-279"><span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**ERROR\_BAD\_NET\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-280">67 (0x43)</span><span class="sxs-lookup"><span data-stu-id="af045-280">67 (0x43)</span></span>
</dt> <dt>



<span data-ttu-id="af045-281">„Der Netzwerkname wurde nicht gefunden.“</span><span class="sxs-lookup"><span data-stu-id="af045-281">The network name cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-282"><span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**Fehler \_ zu \_ viele \_ Namen.**</span><span class="sxs-lookup"><span data-stu-id="af045-282"><span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**ERROR\_TOO\_MANY\_NAMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-283">68 (0x44)</span><span class="sxs-lookup"><span data-stu-id="af045-283">68 (0x44)</span></span>
</dt> <dt>



<span data-ttu-id="af045-284">Das namens Limit für die Karte des Netzwerkadapters für den lokalen Computer wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="af045-284">The name limit for the local computer network adapter card was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-285"><span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**Fehler \_ zu \_ viele \_ Sess**</span><span class="sxs-lookup"><span data-stu-id="af045-285"><span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**ERROR\_TOO\_MANY\_SESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-286">69 (0x45)</span><span class="sxs-lookup"><span data-stu-id="af045-286">69 (0x45)</span></span>
</dt> <dt>



<span data-ttu-id="af045-287">Das Limit der Netzwerk-BIOS-Sitzung wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="af045-287">The network BIOS session limit was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-288"><span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**Fehler \_ Freigabe \_ angehalten**</span><span class="sxs-lookup"><span data-stu-id="af045-288"><span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**ERROR\_SHARING\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-289">70 (0x46)</span><span class="sxs-lookup"><span data-stu-id="af045-289">70 (0x46)</span></span>
</dt> <dt>



<span data-ttu-id="af045-290">Der Remote Server wurde angehalten oder gerade gestartet.</span><span class="sxs-lookup"><span data-stu-id="af045-290">The remote server has been paused or is in the process of being started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-291"><span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**Fehler beim Zurücksetzen des Fehlers. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="af045-291"><span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**ERROR\_REQ\_NOT\_ACCEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-292">71 (0x47)</span><span class="sxs-lookup"><span data-stu-id="af045-292">71 (0x47)</span></span>
</dt> <dt>



<span data-ttu-id="af045-293">Zurzeit können keine weiteren Verbindungen mit diesem Remote Computer hergestellt werden, da es bereits so viele Verbindungen gibt, wie der Computer annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="af045-293">No more connections can be made to this remote computer at this time because there are already as many connections as the computer can accept.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-294"><span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**Fehler beim \_ redir \_ angehalten**</span><span class="sxs-lookup"><span data-stu-id="af045-294"><span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**ERROR\_REDIR\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-295">72 (0x48)</span><span class="sxs-lookup"><span data-stu-id="af045-295">72 (0x48)</span></span>
</dt> <dt>



<span data-ttu-id="af045-296">Der angegebene Drucker oder das angegebene Datenträger Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="af045-296">The specified printer or disk device has been paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-297"><span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**Fehler \_ Datei \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="af045-297"><span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**ERROR\_FILE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-298">80 (0x50)</span><span class="sxs-lookup"><span data-stu-id="af045-298">80 (0x50)</span></span>
</dt> <dt>



<span data-ttu-id="af045-299">Die Datei ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="af045-299">The file exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-300"><span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**Fehler \_ beim \_ Erstellen**</span><span class="sxs-lookup"><span data-stu-id="af045-300"><span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**ERROR\_CANNOT\_MAKE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-301">82 (0x52)</span><span class="sxs-lookup"><span data-stu-id="af045-301">82 (0x52)</span></span>
</dt> <dt>



<span data-ttu-id="af045-302">Das Verzeichnis oder die Datei kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="af045-302">The directory or file cannot be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-303"><span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**Fehler \_ \_ i24**</span><span class="sxs-lookup"><span data-stu-id="af045-303"><span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**ERROR\_FAIL\_I24**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-304">83 (0x53)</span><span class="sxs-lookup"><span data-stu-id="af045-304">83 (0x53)</span></span>
</dt> <dt>



<span data-ttu-id="af045-305">Fehler bei int 24.</span><span class="sxs-lookup"><span data-stu-id="af045-305">Fail on INT 24.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-306"><span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**Fehler \_ aus \_ \_ Strukturen**</span><span class="sxs-lookup"><span data-stu-id="af045-306"><span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**ERROR\_OUT\_OF\_STRUCTURES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-307">84 (0x54)</span><span class="sxs-lookup"><span data-stu-id="af045-307">84 (0x54)</span></span>
</dt> <dt>



<span data-ttu-id="af045-308">Der Speicher zum Verarbeiten dieser Anforderung ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af045-308">Storage to process this request is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-309"><span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**Fehler \_ bereits \_ zugewiesen**</span><span class="sxs-lookup"><span data-stu-id="af045-309"><span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**ERROR\_ALREADY\_ASSIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-310">85 (0x55)</span><span class="sxs-lookup"><span data-stu-id="af045-310">85 (0x55)</span></span>
</dt> <dt>



<span data-ttu-id="af045-311">Der Name des lokalen Geräts wird bereits verwendet.</span><span class="sxs-lookup"><span data-stu-id="af045-311">The local device name is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-312"><span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**Fehler \_ ungültiges \_ Kennwort**</span><span class="sxs-lookup"><span data-stu-id="af045-312"><span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**ERROR\_INVALID\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-313">86 (0x56)</span><span class="sxs-lookup"><span data-stu-id="af045-313">86 (0x56)</span></span>
</dt> <dt>



<span data-ttu-id="af045-314">Das angegebene Netzwerkkennwort ist falsch.</span><span class="sxs-lookup"><span data-stu-id="af045-314">The specified network password is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-315"><span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**Fehler bei \_ ungültigem \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="af045-315"><span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-316">87 (0x57)</span><span class="sxs-lookup"><span data-stu-id="af045-316">87 (0x57)</span></span>
</dt> <dt>



<span data-ttu-id="af045-317">„Der Parameter ist falsch.“</span><span class="sxs-lookup"><span data-stu-id="af045-317">The parameter is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-318"><span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**Fehler beim \_ net- \_ Schreib \_ Fehler.**</span><span class="sxs-lookup"><span data-stu-id="af045-318"><span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**ERROR\_NET\_WRITE\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-319">88 (0x58)</span><span class="sxs-lookup"><span data-stu-id="af045-319">88 (0x58)</span></span>
</dt> <dt>



<span data-ttu-id="af045-320">Im Netzwerk ist ein Schreibfehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="af045-320">A write fault occurred on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-321"><span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**Fehler " \_ keine \_ proc \_ Slots"**</span><span class="sxs-lookup"><span data-stu-id="af045-321"><span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**ERROR\_NO\_PROC\_SLOTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-322">89 (0x59)</span><span class="sxs-lookup"><span data-stu-id="af045-322">89 (0x59)</span></span>
</dt> <dt>



<span data-ttu-id="af045-323">Das System kann zurzeit keinen anderen Prozess starten.</span><span class="sxs-lookup"><span data-stu-id="af045-323">The system cannot start another process at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-324"><span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**Fehler \_ zu \_ viele \_ Semaphoren**</span><span class="sxs-lookup"><span data-stu-id="af045-324"><span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**ERROR\_TOO\_MANY\_SEMAPHORES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-325">100 (0x64)</span><span class="sxs-lookup"><span data-stu-id="af045-325">100 (0x64)</span></span>
</dt> <dt>



<span data-ttu-id="af045-326">Ein weiteres System Semaphor kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="af045-326">Cannot create another system semaphore.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-327"><span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**Fehler durch die \_ \_ \_ bereits \_ im Besitz von SEM**</span><span class="sxs-lookup"><span data-stu-id="af045-327"><span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**ERROR\_EXCL\_SEM\_ALREADY\_OWNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-328">101 (0x65)</span><span class="sxs-lookup"><span data-stu-id="af045-328">101 (0x65)</span></span>
</dt> <dt>



<span data-ttu-id="af045-329">Das exklusive Semaphor ist im Besitz eines anderen Prozesses.</span><span class="sxs-lookup"><span data-stu-id="af045-329">The exclusive semaphore is owned by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-330"><span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**Fehler " \_ SEM" \_ ist \_ festgelegt**</span><span class="sxs-lookup"><span data-stu-id="af045-330"><span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**ERROR\_SEM\_IS\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-331">102 (0x66)</span><span class="sxs-lookup"><span data-stu-id="af045-331">102 (0x66)</span></span>
</dt> <dt>



<span data-ttu-id="af045-332">Das Semaphor ist festgelegt und kann nicht geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="af045-332">The semaphore is set and cannot be closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-333"><span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**Fehler \_ zu \_ viele \_ \_ Anforderungen für das Angleichen**</span><span class="sxs-lookup"><span data-stu-id="af045-333"><span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**ERROR\_TOO\_MANY\_SEM\_REQUESTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-334">103 (0x67)</span><span class="sxs-lookup"><span data-stu-id="af045-334">103 (0x67)</span></span>
</dt> <dt>



<span data-ttu-id="af045-335">Das Semaphor kann nicht erneut festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="af045-335">The semaphore cannot be set again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-336"><span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**Fehler \_ \_ beim \_ \_ Interruptzeit ungültig**</span><span class="sxs-lookup"><span data-stu-id="af045-336"><span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**ERROR\_INVALID\_AT\_INTERRUPT\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-337">104 (0x68)</span><span class="sxs-lookup"><span data-stu-id="af045-337">104 (0x68)</span></span>
</dt> <dt>



<span data-ttu-id="af045-338">Exklusive Semaphoren können zur Interruptzeit nicht angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="af045-338">Cannot request exclusive semaphores at interrupt time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-339"><span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**Fehler beim "-Besitzer". \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="af045-339"><span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**ERROR\_SEM\_OWNER\_DIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-340">105 (0x69)</span><span class="sxs-lookup"><span data-stu-id="af045-340">105 (0x69)</span></span>
</dt> <dt>



<span data-ttu-id="af045-341">Der vorherige Besitz dieses Semaphors wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="af045-341">The previous ownership of this semaphore has ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-342"><span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**Fehler \_ - \_ Benutzer \_ Limit für Benutzer**</span><span class="sxs-lookup"><span data-stu-id="af045-342"><span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**ERROR\_SEM\_USER\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-343">106 (0x6a)</span><span class="sxs-lookup"><span data-stu-id="af045-343">106 (0x6A)</span></span>
</dt> <dt>



<span data-ttu-id="af045-344">Fügen Sie die Diskette für das Laufwerk %1 ein.</span><span class="sxs-lookup"><span data-stu-id="af045-344">Insert the diskette for drive %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-345"><span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**Fehler Datenträger \_ \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="af045-345"><span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**ERROR\_DISK\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-346">107 (0x6b)</span><span class="sxs-lookup"><span data-stu-id="af045-346">107 (0x6B)</span></span>
</dt> <dt>



<span data-ttu-id="af045-347">Das Programm wurde beendet, weil keine Alternative Diskette eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="af045-347">The program stopped because an alternate diskette was not inserted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-348"><span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**Fehler \_ Laufwerk \_ gesperrt**</span><span class="sxs-lookup"><span data-stu-id="af045-348"><span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**ERROR\_DRIVE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-349">108 (0x6C)</span><span class="sxs-lookup"><span data-stu-id="af045-349">108 (0x6C)</span></span>
</dt> <dt>



<span data-ttu-id="af045-350">Der Datenträger wird von einem anderen Prozess verwendet oder gesperrt.</span><span class="sxs-lookup"><span data-stu-id="af045-350">The disk is in use or locked by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-351"><span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**Fehler bei der \_ \_ Pipe.**</span><span class="sxs-lookup"><span data-stu-id="af045-351"><span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**ERROR\_BROKEN\_PIPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-352">109 (0x6d)</span><span class="sxs-lookup"><span data-stu-id="af045-352">109 (0x6D)</span></span>
</dt> <dt>



<span data-ttu-id="af045-353">Die Pipe wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="af045-353">The pipe has been ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-354"><span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**Fehler beim \_ Öffnen. \_**</span><span class="sxs-lookup"><span data-stu-id="af045-354"><span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**ERROR\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-355">110 (0x6e)</span><span class="sxs-lookup"><span data-stu-id="af045-355">110 (0x6E)</span></span>
</dt> <dt>



<span data-ttu-id="af045-356">Das System kann das angegebene Gerät oder die angegebene Datei nicht öffnen.</span><span class="sxs-lookup"><span data-stu-id="af045-356">The system cannot open the device or file specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-357"><span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**Fehler \_ Puffer \_ Überlauf**</span><span class="sxs-lookup"><span data-stu-id="af045-357"><span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**ERROR\_BUFFER\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-358">111 (0x6F)</span><span class="sxs-lookup"><span data-stu-id="af045-358">111 (0x6F)</span></span>
</dt> <dt>



<span data-ttu-id="af045-359">Der Dateiname ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="af045-359">The file name is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-360"><span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**Fehler Datenträger \_ \_ voll**</span><span class="sxs-lookup"><span data-stu-id="af045-360"><span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**ERROR\_DISK\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-361">112 (0x70)</span><span class="sxs-lookup"><span data-stu-id="af045-361">112 (0x70)</span></span>
</dt> <dt>



<span data-ttu-id="af045-362">There is not enough space on the disk.</span><span class="sxs-lookup"><span data-stu-id="af045-362">There is not enough space on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-363"><span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**Fehler \_ keine \_ weiteren \_ Such \_ Handles**</span><span class="sxs-lookup"><span data-stu-id="af045-363"><span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**ERROR\_NO\_MORE\_SEARCH\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-364">113 (0x71)</span><span class="sxs-lookup"><span data-stu-id="af045-364">113 (0x71)</span></span>
</dt> <dt>



<span data-ttu-id="af045-365">Es sind keine weiteren internen Datei Bezeichner verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af045-365">No more internal file identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-366"><span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**Fehler \_ ungültiges \_ Ziel \_ handle**</span><span class="sxs-lookup"><span data-stu-id="af045-366"><span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**ERROR\_INVALID\_TARGET\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-367">114 (0x72)</span><span class="sxs-lookup"><span data-stu-id="af045-367">114 (0x72)</span></span>
</dt> <dt>



<span data-ttu-id="af045-368">Der Bezeichner der internen Ziel Datei ist falsch.</span><span class="sxs-lookup"><span data-stu-id="af045-368">The target internal file identifier is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-369"><span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**\_ungültige \_ Kategorie**</span><span class="sxs-lookup"><span data-stu-id="af045-369"><span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**ERROR\_INVALID\_CATEGORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-370">117 (0x75)</span><span class="sxs-lookup"><span data-stu-id="af045-370">117 (0x75)</span></span>
</dt> <dt>



<span data-ttu-id="af045-371">Der IOCTL-Befehl, der vom Anwendungsprogramm durchgeführt wird, ist nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="af045-371">The IOCTL call made by the application program is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-372"><span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**Fehler \_ beim \_ Überprüfen des \_ Schalters**</span><span class="sxs-lookup"><span data-stu-id="af045-372"><span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**ERROR\_INVALID\_VERIFY\_SWITCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-373">118 (0x76)</span><span class="sxs-lookup"><span data-stu-id="af045-373">118 (0x76)</span></span>
</dt> <dt>



<span data-ttu-id="af045-374">Der Wert für den Schalter Parameter "Verify-on-Write" ist falsch.</span><span class="sxs-lookup"><span data-stu-id="af045-374">The verify-on-write switch parameter value is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-375"><span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**Fehler \_ hafte \_ Treiber \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="af045-375"><span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ERROR\_BAD\_DRIVER\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-376">119 (0x77)</span><span class="sxs-lookup"><span data-stu-id="af045-376">119 (0x77)</span></span>
</dt> <dt>



<span data-ttu-id="af045-377">Der angeforderte Befehl wird vom System nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="af045-377">The system does not support the command requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-378"><span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**Fehler-Befehl \_ \_ nicht \_ implementiert**</span><span class="sxs-lookup"><span data-stu-id="af045-378"><span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**ERROR\_CALL\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-379">120 (0x78)</span><span class="sxs-lookup"><span data-stu-id="af045-379">120 (0x78)</span></span>
</dt> <dt>



<span data-ttu-id="af045-380">Diese Funktion wird auf diesem System nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="af045-380">This function is not supported on this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-381"><span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**Fehler \_ - \_ buildtimeout**</span><span class="sxs-lookup"><span data-stu-id="af045-381"><span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**ERROR\_SEM\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-382">121 (0x79)</span><span class="sxs-lookup"><span data-stu-id="af045-382">121 (0x79)</span></span>
</dt> <dt>



<span data-ttu-id="af045-383">Der Timeout Zeitraum für das Semaphor ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="af045-383">The semaphore timeout period has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-384"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**Fehler \_ beim \_ Puffer.**</span><span class="sxs-lookup"><span data-stu-id="af045-384"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-385">122 (0x7a)</span><span class="sxs-lookup"><span data-stu-id="af045-385">122 (0x7A)</span></span>
</dt> <dt>



<span data-ttu-id="af045-386">Der an einen System Rückruf über gegebene Datenbereich ist zu klein.</span><span class="sxs-lookup"><span data-stu-id="af045-386">The data area passed to a system call is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-387"><span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**\_ungültiger \_ Name.**</span><span class="sxs-lookup"><span data-stu-id="af045-387"><span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**ERROR\_INVALID\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-388">123 (0x7B)</span><span class="sxs-lookup"><span data-stu-id="af045-388">123 (0x7B)</span></span>
</dt> <dt>



<span data-ttu-id="af045-389">Die Syntax für den Dateinamen, den Verzeichnisnamen oder die Volumebezeichnung ist falsch.</span><span class="sxs-lookup"><span data-stu-id="af045-389">The filename, directory name, or volume label syntax is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-390"><span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**\_ungültige \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="af045-390"><span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**ERROR\_INVALID\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-391">124 (0x7c)</span><span class="sxs-lookup"><span data-stu-id="af045-391">124 (0x7C)</span></span>
</dt> <dt>



<span data-ttu-id="af045-392">Die System-aufrufsebene ist nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="af045-392">The system call level is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-393"><span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**Fehler \_ " \_ keine \_ Volumebezeichnung"**</span><span class="sxs-lookup"><span data-stu-id="af045-393"><span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**ERROR\_NO\_VOLUME\_LABEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-394">125 (0x7D)</span><span class="sxs-lookup"><span data-stu-id="af045-394">125 (0x7D)</span></span>
</dt> <dt>



<span data-ttu-id="af045-395">Der Datenträger weist keine Volumebezeichnung auf.</span><span class="sxs-lookup"><span data-stu-id="af045-395">The disk has no volume label.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-396"><span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**Fehler \_ mod \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="af045-396"><span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**ERROR\_MOD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-397">126 (0x7E)</span><span class="sxs-lookup"><span data-stu-id="af045-397">126 (0x7E)</span></span>
</dt> <dt>



<span data-ttu-id="af045-398">Das angegebene Modul wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="af045-398">The specified module could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-399"><span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**Fehler \_ proc \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="af045-399"><span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**ERROR\_PROC\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-400">127 (0x7f)</span><span class="sxs-lookup"><span data-stu-id="af045-400">127 (0x7F)</span></span>
</dt> <dt>



<span data-ttu-id="af045-401">Die angegebene Prozedur wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="af045-401">The specified procedure could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-402"><span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**Fehler beim \_ warten auf \_ kein \_ Kind**</span><span class="sxs-lookup"><span data-stu-id="af045-402"><span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERROR\_WAIT\_NO\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-403">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="af045-403">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="af045-404">Es sind keine untergeordneten Prozesse vorhanden, auf die gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="af045-404">There are no child processes to wait for.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-405"><span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**Fehler untergeordnetes Element \_ \_ nicht \_ fertiggestellt**</span><span class="sxs-lookup"><span data-stu-id="af045-405"><span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**ERROR\_CHILD\_NOT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-406">129 (0x81)</span><span class="sxs-lookup"><span data-stu-id="af045-406">129 (0x81)</span></span>
</dt> <dt>



<span data-ttu-id="af045-407">Die Anwendung "%1" kann nicht im Win32-Modus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="af045-407">The %1 application cannot be run in Win32 mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-408"><span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**Fehler beim \_ direkt \_ Zugriffs \_ handle**</span><span class="sxs-lookup"><span data-stu-id="af045-408"><span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**ERROR\_DIRECT\_ACCESS\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-409">130 (0x82)</span><span class="sxs-lookup"><span data-stu-id="af045-409">130 (0x82)</span></span>
</dt> <dt>



<span data-ttu-id="af045-410">Es wurde versucht, ein Datei Handle für eine geöffnete Datenträger Partition für einen anderen Vorgang als eine unformatierte Datenträger-e/a zu verwenden</span><span class="sxs-lookup"><span data-stu-id="af045-410">Attempt to use a file handle to an open disk partition for an operation other than raw disk I/O.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-411"><span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**Fehler bei \_ negativer \_ Suche**</span><span class="sxs-lookup"><span data-stu-id="af045-411"><span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**ERROR\_NEGATIVE\_SEEK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-412">131 (0x83)</span><span class="sxs-lookup"><span data-stu-id="af045-412">131 (0x83)</span></span>
</dt> <dt>



<span data-ttu-id="af045-413">Es wurde versucht, den Dateizeiger vor dem Anfang der Datei zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="af045-413">An attempt was made to move the file pointer before the beginning of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-414"><span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**Fehler \_ Suche \_ auf \_ Gerät**</span><span class="sxs-lookup"><span data-stu-id="af045-414"><span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**ERROR\_SEEK\_ON\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-415">132 (0x84)</span><span class="sxs-lookup"><span data-stu-id="af045-415">132 (0x84)</span></span>
</dt> <dt>



<span data-ttu-id="af045-416">Der Dateizeiger kann für das angegebene Gerät oder die angegebene Datei nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="af045-416">The file pointer cannot be set on the specified device or file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-417"><span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**Fehler \_ ist \_ \_ joinziel**</span><span class="sxs-lookup"><span data-stu-id="af045-417"><span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**ERROR\_IS\_JOIN\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-418">133 (0x85)</span><span class="sxs-lookup"><span data-stu-id="af045-418">133 (0x85)</span></span>
</dt> <dt>



<span data-ttu-id="af045-419">Ein Join-Befehl oder ein SUBST-Befehl kann nicht für ein Laufwerk verwendet werden, das zuvor verknüpfte Laufwerke enthält.</span><span class="sxs-lookup"><span data-stu-id="af045-419">A JOIN or SUBST command cannot be used for a drive that contains previously joined drives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-420"><span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**Fehler \_ ist \_ verknüpft**</span><span class="sxs-lookup"><span data-stu-id="af045-420"><span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**ERROR\_IS\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-421">134 (0x86)</span><span class="sxs-lookup"><span data-stu-id="af045-421">134 (0x86)</span></span>
</dt> <dt>



<span data-ttu-id="af045-422">Es wurde versucht, einen Join-oder SUBST-Befehl auf einem Laufwerk zu verwenden, das bereits verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="af045-422">An attempt was made to use a JOIN or SUBST command on a drive that has already been joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-423"><span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**Fehler \_ ist \_ substed**</span><span class="sxs-lookup"><span data-stu-id="af045-423"><span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**ERROR\_IS\_SUBSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-424">135 (0x87)</span><span class="sxs-lookup"><span data-stu-id="af045-424">135 (0x87)</span></span>
</dt> <dt>



<span data-ttu-id="af045-425">Es wurde versucht, einen Join-oder SUBST-Befehl auf einem Laufwerk zu verwenden, das bereits ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="af045-425">An attempt was made to use a JOIN or SUBST command on a drive that has already been substituted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-426"><span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**Fehler \_ nicht \_ verknüpft**</span><span class="sxs-lookup"><span data-stu-id="af045-426"><span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**ERROR\_NOT\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-427">136 (0x88)</span><span class="sxs-lookup"><span data-stu-id="af045-427">136 (0x88)</span></span>
</dt> <dt>



<span data-ttu-id="af045-428">Das System hat versucht, den Join eines Laufwerks zu löschen, das nicht verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="af045-428">The system tried to delete the JOIN of a drive that is not joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-429"><span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**Fehler \_ nicht \_ unterteilt**</span><span class="sxs-lookup"><span data-stu-id="af045-429"><span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERROR\_NOT\_SUBSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-430">137 (0x89)</span><span class="sxs-lookup"><span data-stu-id="af045-430">137 (0x89)</span></span>
</dt> <dt>



<span data-ttu-id="af045-431">Das System hat versucht, die Ersetzung eines nicht ersetzten Laufwerks zu löschen.</span><span class="sxs-lookup"><span data-stu-id="af045-431">The system tried to delete the substitution of a drive that is not substituted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-432"><span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**Fehler \_ Verknüpfung \_ für \_ Join**</span><span class="sxs-lookup"><span data-stu-id="af045-432"><span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**ERROR\_JOIN\_TO\_JOIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-433">138 (0x8a)</span><span class="sxs-lookup"><span data-stu-id="af045-433">138 (0x8A)</span></span>
</dt> <dt>



<span data-ttu-id="af045-434">Das System hat versucht, ein Laufwerk einem Verzeichnis auf einem verknüpften Laufwerk beizutreten.</span><span class="sxs-lookup"><span data-stu-id="af045-434">The system tried to join a drive to a directory on a joined drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-435"><span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**Fehler " \_ subst" \_ in " \_ subst"**</span><span class="sxs-lookup"><span data-stu-id="af045-435"><span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERROR\_SUBST\_TO\_SUBST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-436">139 (0x8B)</span><span class="sxs-lookup"><span data-stu-id="af045-436">139 (0x8B)</span></span>
</dt> <dt>



<span data-ttu-id="af045-437">Das System hat versucht, ein Laufwerk zu einem Verzeichnis auf einem ersetzte Laufwerk zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="af045-437">The system tried to substitute a drive to a directory on a substituted drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-438"><span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**Fehler \_ \_ bei Join mit \_ subst**</span><span class="sxs-lookup"><span data-stu-id="af045-438"><span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**ERROR\_JOIN\_TO\_SUBST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-439">140 (0x8c)</span><span class="sxs-lookup"><span data-stu-id="af045-439">140 (0x8C)</span></span>
</dt> <dt>



<span data-ttu-id="af045-440">Das System hat versucht, ein Laufwerk einem Verzeichnis auf einem Ersatz Laufwerk beizutreten.</span><span class="sxs-lookup"><span data-stu-id="af045-440">The system tried to join a drive to a directory on a substituted drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-441"><span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**Fehler- \_ subst \_ zum \_ beitreten**</span><span class="sxs-lookup"><span data-stu-id="af045-441"><span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERROR\_SUBST\_TO\_JOIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-442">141 (0x8d)</span><span class="sxs-lookup"><span data-stu-id="af045-442">141 (0x8D)</span></span>
</dt> <dt>



<span data-ttu-id="af045-443">Das System hat versucht, ein Laufwerk zu einem Verzeichnis auf einem verbundenen Laufwerk zu unterteilen.</span><span class="sxs-lookup"><span data-stu-id="af045-443">The system tried to SUBST a drive to a directory on a joined drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-444"><span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**Fehler \_ ausgelastet- \_ Laufwerk**</span><span class="sxs-lookup"><span data-stu-id="af045-444"><span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**ERROR\_BUSY\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-445">142 (0x8e)</span><span class="sxs-lookup"><span data-stu-id="af045-445">142 (0x8E)</span></span>
</dt> <dt>



<span data-ttu-id="af045-446">Das System kann zurzeit keine Verknüpfung oder teilst ausführen.</span><span class="sxs-lookup"><span data-stu-id="af045-446">The system cannot perform a JOIN or SUBST at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-447"><span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**Fehler beim \_ gleichen \_ Laufwerk**</span><span class="sxs-lookup"><span data-stu-id="af045-447"><span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**ERROR\_SAME\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-448">143 (0x8F)</span><span class="sxs-lookup"><span data-stu-id="af045-448">143 (0x8F)</span></span>
</dt> <dt>



<span data-ttu-id="af045-449">Das System kann ein Laufwerk oder ein Verzeichnis auf dem gleichen Laufwerk nicht einem Verzeichnis hinzufügen oder dieses ersetzen.</span><span class="sxs-lookup"><span data-stu-id="af045-449">The system cannot join or substitute a drive to or for a directory on the same drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-450"><span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**Fehler \_ Verzeichnis \_ nicht \_ root**</span><span class="sxs-lookup"><span data-stu-id="af045-450"><span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**ERROR\_DIR\_NOT\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-451">144 (0x90)</span><span class="sxs-lookup"><span data-stu-id="af045-451">144 (0x90)</span></span>
</dt> <dt>



<span data-ttu-id="af045-452">Das Verzeichnis ist kein Unterverzeichnis des Stamm Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="af045-452">The directory is not a subdirectory of the root directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-453"><span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**Fehler \_ Verzeichnis \_ nicht \_ leer**</span><span class="sxs-lookup"><span data-stu-id="af045-453"><span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**ERROR\_DIR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-454">145 (0x91)</span><span class="sxs-lookup"><span data-stu-id="af045-454">145 (0x91)</span></span>
</dt> <dt>



<span data-ttu-id="af045-455">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="af045-455">The directory is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-456"><span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**Fehler \_ ist ein \_ subst- \_ Pfad.**</span><span class="sxs-lookup"><span data-stu-id="af045-456"><span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**ERROR\_IS\_SUBST\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-457">146 (0x92)</span><span class="sxs-lookup"><span data-stu-id="af045-457">146 (0x92)</span></span>
</dt> <dt>



<span data-ttu-id="af045-458">Der angegebene Pfad wird in einem Ersatz verwendet.</span><span class="sxs-lookup"><span data-stu-id="af045-458">The path specified is being used in a substitute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-459"><span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**Fehler \_ ist \_ \_ Joinpfad**</span><span class="sxs-lookup"><span data-stu-id="af045-459"><span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**ERROR\_IS\_JOIN\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-460">147 (0x93)</span><span class="sxs-lookup"><span data-stu-id="af045-460">147 (0x93)</span></span>
</dt> <dt>



<span data-ttu-id="af045-461">Zum Verarbeiten dieses Befehls sind nicht genügend Ressourcen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af045-461">Not enough resources are available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-462"><span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**Fehler \_ Pfad \_ ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="af045-462"><span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**ERROR\_PATH\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-463">148 (0x94)</span><span class="sxs-lookup"><span data-stu-id="af045-463">148 (0x94)</span></span>
</dt> <dt>



<span data-ttu-id="af045-464">Der angegebene Pfad kann zurzeit nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af045-464">The path specified cannot be used at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-465"><span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**Fehler \_ ist \_ subst- \_ Ziel**</span><span class="sxs-lookup"><span data-stu-id="af045-465"><span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**ERROR\_IS\_SUBST\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-466">149 (0x95)</span><span class="sxs-lookup"><span data-stu-id="af045-466">149 (0x95)</span></span>
</dt> <dt>



<span data-ttu-id="af045-467">Es wurde versucht, ein Laufwerk beizutreten oder zu ersetzen, für das ein Verzeichnis auf dem Laufwerk das Ziel eines vorherigen Ersatz ist.</span><span class="sxs-lookup"><span data-stu-id="af045-467">An attempt was made to join or substitute a drive for which a directory on the drive is the target of a previous substitute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-468"><span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**Fehler \_ System-Ablauf \_ Verfolgung**</span><span class="sxs-lookup"><span data-stu-id="af045-468"><span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**ERROR\_SYSTEM\_TRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-469">150 (0x96)</span><span class="sxs-lookup"><span data-stu-id="af045-469">150 (0x96)</span></span>
</dt> <dt>



<span data-ttu-id="af045-470">In ihrer CONFIG.SYS Datei wurden keine System Ablauf Verfolgungs Informationen angegeben, oder die Ablauf Verfolgung ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="af045-470">System trace information was not specified in your CONFIG.SYS file, or tracing is disallowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-471"><span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**Fehler \_ bei ungültiger \_ Ereignis \_ Anzahl**</span><span class="sxs-lookup"><span data-stu-id="af045-471"><span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**ERROR\_INVALID\_EVENT\_COUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-472">151 (0x97)</span><span class="sxs-lookup"><span data-stu-id="af045-472">151 (0x97)</span></span>
</dt> <dt>



<span data-ttu-id="af045-473">Die Anzahl der angegebenen Semaphor-Ereignisse für DosMuxSemWait ist nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="af045-473">The number of specified semaphore events for DosMuxSemWait is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-474"><span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**Fehler \_ zu \_ viele \_ muxkellner**</span><span class="sxs-lookup"><span data-stu-id="af045-474"><span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**ERROR\_TOO\_MANY\_MUXWAITERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-475">152 (0x98)</span><span class="sxs-lookup"><span data-stu-id="af045-475">152 (0x98)</span></span>
</dt> <dt>



<span data-ttu-id="af045-476">DosMuxSemWait wurde nicht ausgeführt. zu viele Semaphoren wurden bereits festgelegt.</span><span class="sxs-lookup"><span data-stu-id="af045-476">DosMuxSemWait did not execute; too many semaphores are already set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-477"><span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**Fehler bei \_ ungültigem \_ Listen \_ Format**</span><span class="sxs-lookup"><span data-stu-id="af045-477"><span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**ERROR\_INVALID\_LIST\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-478">153 (0x99)</span><span class="sxs-lookup"><span data-stu-id="af045-478">153 (0x99)</span></span>
</dt> <dt>



<span data-ttu-id="af045-479">Die DosMuxSemWait-Liste ist nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="af045-479">The DosMuxSemWait list is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-480"><span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**Fehler \_ Bezeichnung \_ zu \_ lang**</span><span class="sxs-lookup"><span data-stu-id="af045-480"><span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**ERROR\_LABEL\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-481">154 (0x9a)</span><span class="sxs-lookup"><span data-stu-id="af045-481">154 (0x9A)</span></span>
</dt> <dt>



<span data-ttu-id="af045-482">Die von Ihnen eingegebene Volumebezeichnung überschreitet die Bezeichnung für das Zeichenlimit des Ziel Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="af045-482">The volume label you entered exceeds the label character limit of the target file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-483"><span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**Fehler \_ zu \_ viele \_ TCBS**</span><span class="sxs-lookup"><span data-stu-id="af045-483"><span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**ERROR\_TOO\_MANY\_TCBS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-484">155 (0x9b)</span><span class="sxs-lookup"><span data-stu-id="af045-484">155 (0x9B)</span></span>
</dt> <dt>



<span data-ttu-id="af045-485">Ein anderer Thread kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="af045-485">Cannot create another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-486"><span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**Fehler \_ Signal \_ abgelehnt**</span><span class="sxs-lookup"><span data-stu-id="af045-486"><span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**ERROR\_SIGNAL\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-487">156 (0x9C)</span><span class="sxs-lookup"><span data-stu-id="af045-487">156 (0x9C)</span></span>
</dt> <dt>



<span data-ttu-id="af045-488">Der Empfänger Prozess hat das Signal abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="af045-488">The recipient process has refused the signal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-489"><span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**Fehler \_ verworfen**</span><span class="sxs-lookup"><span data-stu-id="af045-489"><span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**ERROR\_DISCARDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-490">157 (0x9d)</span><span class="sxs-lookup"><span data-stu-id="af045-490">157 (0x9D)</span></span>
</dt> <dt>



<span data-ttu-id="af045-491">Das Segment wurde bereits verworfen und kann nicht gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="af045-491">The segment is already discarded and cannot be locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-492"><span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**Fehler \_ nicht \_ gesperrt**</span><span class="sxs-lookup"><span data-stu-id="af045-492"><span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**ERROR\_NOT\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-493">158 (0x9E)</span><span class="sxs-lookup"><span data-stu-id="af045-493">158 (0x9E)</span></span>
</dt> <dt>



<span data-ttu-id="af045-494">Das Segment ist bereits entsperrt.</span><span class="sxs-lookup"><span data-stu-id="af045-494">The segment is already unlocked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-495"><span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**Fehler \_ hafte \_ ThreadId \_ addr**</span><span class="sxs-lookup"><span data-stu-id="af045-495"><span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**ERROR\_BAD\_THREADID\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-496">159 (0x9F)</span><span class="sxs-lookup"><span data-stu-id="af045-496">159 (0x9F)</span></span>
</dt> <dt>



<span data-ttu-id="af045-497">Die Adresse für die Thread-ID ist nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="af045-497">The address for the thread ID is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-498"><span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**Ungültige Argumente für Fehler \_ \_**</span><span class="sxs-lookup"><span data-stu-id="af045-498"><span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ERROR\_BAD\_ARGUMENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-499">160 (0xa0)</span><span class="sxs-lookup"><span data-stu-id="af045-499">160 (0xA0)</span></span>
</dt> <dt>



<span data-ttu-id="af045-500">Mindestens ein Argument ist nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="af045-500">One or more arguments are not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-501"><span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**Fehler Ungültiger \_ \_ Pfadname.**</span><span class="sxs-lookup"><span data-stu-id="af045-501"><span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ERROR\_BAD\_PATHNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-502">161 (0xA1)</span><span class="sxs-lookup"><span data-stu-id="af045-502">161 (0xA1)</span></span>
</dt> <dt>



<span data-ttu-id="af045-503">Der angegebene Pfad ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="af045-503">The specified path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-504"><span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**Fehler \_ Signal \_ Ausstehend**</span><span class="sxs-lookup"><span data-stu-id="af045-504"><span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**ERROR\_SIGNAL\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-505">162 (0xA2)</span><span class="sxs-lookup"><span data-stu-id="af045-505">162 (0xA2)</span></span>
</dt> <dt>



<span data-ttu-id="af045-506">Ein Signal steht bereits aus.</span><span class="sxs-lookup"><span data-stu-id="af045-506">A signal is already pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-507"><span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**Fehler beim maximalen Anzahl von \_ \_ thrds. \_**</span><span class="sxs-lookup"><span data-stu-id="af045-507"><span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**ERROR\_MAX\_THRDS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-508">164 (0xa4)</span><span class="sxs-lookup"><span data-stu-id="af045-508">164 (0xA4)</span></span>
</dt> <dt>



<span data-ttu-id="af045-509">Im System können keine weiteren Threads erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="af045-509">No more threads can be created in the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-510"><span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**Fehler beim \_ Sperren \_**</span><span class="sxs-lookup"><span data-stu-id="af045-510"><span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**ERROR\_LOCK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-511">167 (0xA7)</span><span class="sxs-lookup"><span data-stu-id="af045-511">167 (0xA7)</span></span>
</dt> <dt>



<span data-ttu-id="af045-512">Ein Bereich einer Datei kann nicht gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="af045-512">Unable to lock a region of a file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-513"><span id="ERROR_BUSY"></span><span id="error_busy"></span>**Fehler \_ ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="af045-513"><span id="ERROR_BUSY"></span><span id="error_busy"></span>**ERROR\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-514">170 (0xaa)</span><span class="sxs-lookup"><span data-stu-id="af045-514">170 (0xAA)</span></span>
</dt> <dt>



<span data-ttu-id="af045-515">Die angeforderte Ressource wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="af045-515">The requested resource is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-516"><span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**Fehler \_ \_ beim unterstützen \_ des \_ Geräts.**</span><span class="sxs-lookup"><span data-stu-id="af045-516"><span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**ERROR\_DEVICE\_SUPPORT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-517">171 (0xAB)</span><span class="sxs-lookup"><span data-stu-id="af045-517">171 (0xAB)</span></span>
</dt> <dt>



<span data-ttu-id="af045-518">Die Erkennung der Befehls Unterstützung für das Gerät wird durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="af045-518">Device's command support detection is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-519"><span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**Fehler \_ Abbruch \_ Verletzung**</span><span class="sxs-lookup"><span data-stu-id="af045-519"><span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**ERROR\_CANCEL\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-520">173 (0xAD)</span><span class="sxs-lookup"><span data-stu-id="af045-520">173 (0xAD)</span></span>
</dt> <dt>



<span data-ttu-id="af045-521">Eine Sperranforderung war für den angegebenen Abbruchbereich nicht ausstehend.</span><span class="sxs-lookup"><span data-stu-id="af045-521">A lock request was not outstanding for the supplied cancel region.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-522"><span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**Fehler \_ atomarische \_ Sperren \_ \_ werden nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="af045-522"><span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ERROR\_ATOMIC\_LOCKS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-523">174 (0xae)</span><span class="sxs-lookup"><span data-stu-id="af045-523">174 (0xAE)</span></span>
</dt> <dt>



<span data-ttu-id="af045-524">Das Dateisystem unterstützt keine atomaren Änderungen am Sperrentyp.</span><span class="sxs-lookup"><span data-stu-id="af045-524">The file system does not support atomic changes to the lock type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-525"><span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**Fehler \_ ungültige \_ Segment \_ Nummer.**</span><span class="sxs-lookup"><span data-stu-id="af045-525"><span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**ERROR\_INVALID\_SEGMENT\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-526">180 (0xB4)</span><span class="sxs-lookup"><span data-stu-id="af045-526">180 (0xB4)</span></span>
</dt> <dt>



<span data-ttu-id="af045-527">Das System hat eine nicht korrekte Segment Nummer erkannt.</span><span class="sxs-lookup"><span data-stu-id="af045-527">The system detected a segment number that was not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-528"><span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**Fehler \_ ungültige \_ Ordnungszahl**</span><span class="sxs-lookup"><span data-stu-id="af045-528"><span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ERROR\_INVALID\_ORDINAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-529">182 (0xB6)</span><span class="sxs-lookup"><span data-stu-id="af045-529">182 (0xB6)</span></span>
</dt> <dt>



<span data-ttu-id="af045-530">Das Betriebssystem kann "%1" nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="af045-530">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-531"><span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**Fehler ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="af045-531"><span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**ERROR\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-532">183 (0xb7)</span><span class="sxs-lookup"><span data-stu-id="af045-532">183 (0xB7)</span></span>
</dt> <dt>



<span data-ttu-id="af045-533">Eine Datei kann nicht erstellt werden, wenn die Datei bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="af045-533">Cannot create a file when that file already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-534"><span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**\_ungültige \_ Flag- \_ Nummer.**</span><span class="sxs-lookup"><span data-stu-id="af045-534"><span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**ERROR\_INVALID\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-535">186 (0xba)</span><span class="sxs-lookup"><span data-stu-id="af045-535">186 (0xBA)</span></span>
</dt> <dt>



<span data-ttu-id="af045-536">Das über gegebene Flag ist nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="af045-536">The flag passed is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-537"><span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**Fehler " \_ SEM" \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="af045-537"><span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**ERROR\_SEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-538">187 (0xBB)</span><span class="sxs-lookup"><span data-stu-id="af045-538">187 (0xBB)</span></span>
</dt> <dt>



<span data-ttu-id="af045-539">Der angegebene Name des System Semaphors wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="af045-539">The specified system semaphore name was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-540"><span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**Fehler \_ beim \_ Starten von \_ Codel.**</span><span class="sxs-lookup"><span data-stu-id="af045-540"><span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**ERROR\_INVALID\_STARTING\_CODESEG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-541">188 (0xBC)</span><span class="sxs-lookup"><span data-stu-id="af045-541">188 (0xBC)</span></span>
</dt> <dt>



<span data-ttu-id="af045-542">Das Betriebssystem kann "%1" nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="af045-542">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-543"><span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**\_ungültiger \_ Stackl-Fehler.**</span><span class="sxs-lookup"><span data-stu-id="af045-543"><span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**ERROR\_INVALID\_STACKSEG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-544">189 (0xbd)</span><span class="sxs-lookup"><span data-stu-id="af045-544">189 (0xBD)</span></span>
</dt> <dt>



<span data-ttu-id="af045-545">Das Betriebssystem kann "%1" nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="af045-545">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-546"><span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**\_ungültiger \_ ModuleType.**</span><span class="sxs-lookup"><span data-stu-id="af045-546"><span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERROR\_INVALID\_MODULETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-547">190 (0xBE)</span><span class="sxs-lookup"><span data-stu-id="af045-547">190 (0xBE)</span></span>
</dt> <dt>



<span data-ttu-id="af045-548">Das Betriebssystem kann "%1" nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="af045-548">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-549"><span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**Fehler \_ ungültige \_ exe- \_ Signatur.**</span><span class="sxs-lookup"><span data-stu-id="af045-549"><span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**ERROR\_INVALID\_EXE\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-550">191 (0xBF)</span><span class="sxs-lookup"><span data-stu-id="af045-550">191 (0xBF)</span></span>
</dt> <dt>



<span data-ttu-id="af045-551">%1 kann nicht im Win32-Modus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="af045-551">Cannot run %1 in Win32 mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-552"><span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**Fehler- \_ exe als \_ \_ ungültig markiert**</span><span class="sxs-lookup"><span data-stu-id="af045-552"><span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**ERROR\_EXE\_MARKED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-553">192 (0xC0)</span><span class="sxs-lookup"><span data-stu-id="af045-553">192 (0xC0)</span></span>
</dt> <dt>



<span data-ttu-id="af045-554">Das Betriebssystem kann "%1" nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="af045-554">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-555"><span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**Fehler fehlerhaftes \_ \_ exe- \_ Format**</span><span class="sxs-lookup"><span data-stu-id="af045-555"><span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**ERROR\_BAD\_EXE\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-556">193 (0xC1)</span><span class="sxs-lookup"><span data-stu-id="af045-556">193 (0xC1)</span></span>
</dt> <dt>



<span data-ttu-id="af045-557">%1 ist keine gültige Win32-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="af045-557">%1 is not a valid Win32 application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-558"><span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**Fehler bei \_ iterierten \_ Daten über \_ schreiten \_ 64 KB.**</span><span class="sxs-lookup"><span data-stu-id="af045-558"><span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**ERROR\_ITERATED\_DATA\_EXCEEDS\_64k**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-559">194 (0xC2)</span><span class="sxs-lookup"><span data-stu-id="af045-559">194 (0xC2)</span></span>
</dt> <dt>



<span data-ttu-id="af045-560">Das Betriebssystem kann "%1" nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="af045-560">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-561"><span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**Fehler \_ ungültige \_ minzuweisung.**</span><span class="sxs-lookup"><span data-stu-id="af045-561"><span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**ERROR\_INVALID\_MINALLOCSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-562">195 (0xc3)</span><span class="sxs-lookup"><span data-stu-id="af045-562">195 (0xC3)</span></span>
</dt> <dt>



<span data-ttu-id="af045-563">Das Betriebssystem kann "%1" nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="af045-563">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-564"><span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**Fehler \_ beim Dynlink \_ aus \_ ungültigem \_ Ring.**</span><span class="sxs-lookup"><span data-stu-id="af045-564"><span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**ERROR\_DYNLINK\_FROM\_INVALID\_RING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-565">196 (0xc4)</span><span class="sxs-lookup"><span data-stu-id="af045-565">196 (0xC4)</span></span>
</dt> <dt>



<span data-ttu-id="af045-566">Das Betriebssystem kann dieses Anwendungsprogramm nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="af045-566">The operating system cannot run this application program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-567"><span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**Fehler ' \_ IOPL ' ist \_ nicht \_ aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="af045-567"><span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**ERROR\_IOPL\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-568">197 (0xC5)</span><span class="sxs-lookup"><span data-stu-id="af045-568">197 (0xC5)</span></span>
</dt> <dt>



<span data-ttu-id="af045-569">Das Betriebssystem ist zurzeit nicht für das Ausführen dieser Anwendung konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="af045-569">The operating system is not presently configured to run this application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-570"><span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**Fehler \_ ungültige \_ SEGDPL.**</span><span class="sxs-lookup"><span data-stu-id="af045-570"><span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**ERROR\_INVALID\_SEGDPL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-571">198 (0xc6)</span><span class="sxs-lookup"><span data-stu-id="af045-571">198 (0xC6)</span></span>
</dt> <dt>



<span data-ttu-id="af045-572">Das Betriebssystem kann "%1" nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="af045-572">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-573"><span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**Der Fehler " \_ autodataseg" über \_ schreitet \_ 64K.**</span><span class="sxs-lookup"><span data-stu-id="af045-573"><span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**ERROR\_AUTODATASEG\_EXCEEDS\_64k**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-574">199 (0xc7)</span><span class="sxs-lookup"><span data-stu-id="af045-574">199 (0xC7)</span></span>
</dt> <dt>



<span data-ttu-id="af045-575">Das Betriebssystem kann dieses Anwendungsprogramm nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="af045-575">The operating system cannot run this application program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-576"><span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**Fehler \_ RING2SEG \_ muss \_ \_ verschiebbar sein.**</span><span class="sxs-lookup"><span data-stu-id="af045-576"><span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**ERROR\_RING2SEG\_MUST\_BE\_MOVABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-577">200 (0xc8)</span><span class="sxs-lookup"><span data-stu-id="af045-577">200 (0xC8)</span></span>
</dt> <dt>



<span data-ttu-id="af045-578">Das Codesegment darf nicht größer als oder gleich 64 KB sein.</span><span class="sxs-lookup"><span data-stu-id="af045-578">The code segment cannot be greater than or equal to 64K.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-579"><span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**Fehler \_ reloc- \_ Kette \_ xeeds \_ seglim**</span><span class="sxs-lookup"><span data-stu-id="af045-579"><span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERROR\_RELOC\_CHAIN\_XEEDS\_SEGLIM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-580">201 (0xC9)</span><span class="sxs-lookup"><span data-stu-id="af045-580">201 (0xC9)</span></span>
</dt> <dt>



<span data-ttu-id="af045-581">Das Betriebssystem kann "%1" nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="af045-581">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-582"><span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**Fehler \_ bei infloop \_ in \_ reloc- \_ Kette**</span><span class="sxs-lookup"><span data-stu-id="af045-582"><span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**ERROR\_INFLOOP\_IN\_RELOC\_CHAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-583">202 (0xca)</span><span class="sxs-lookup"><span data-stu-id="af045-583">202 (0xCA)</span></span>
</dt> <dt>



<span data-ttu-id="af045-584">Das Betriebssystem kann "%1" nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="af045-584">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-585"><span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**Fehler bei " \_ \_ nicht \_ gefunden".**</span><span class="sxs-lookup"><span data-stu-id="af045-585"><span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**ERROR\_ENVVAR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-586">203 (0xCB)</span><span class="sxs-lookup"><span data-stu-id="af045-586">203 (0xCB)</span></span>
</dt> <dt>



<span data-ttu-id="af045-587">Die eingegebene Umgebungs Option konnte vom System nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="af045-587">The system could not find the environment option that was entered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-588"><span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**Fehler " \_ kein \_ Signal \_ gesendet"**</span><span class="sxs-lookup"><span data-stu-id="af045-588"><span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**ERROR\_NO\_SIGNAL\_SENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-589">205 (0xCD)</span><span class="sxs-lookup"><span data-stu-id="af045-589">205 (0xCD)</span></span>
</dt> <dt>



<span data-ttu-id="af045-590">Kein Prozess in der Befehls Teilstruktur verfügt über einen Signalhandler.</span><span class="sxs-lookup"><span data-stu-id="af045-590">No process in the command subtree has a signal handler.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-591"><span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**Fehler Name des \_ \_ ausgenommenen \_ Bereichs**</span><span class="sxs-lookup"><span data-stu-id="af045-591"><span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**ERROR\_FILENAME\_EXCED\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-592">206 (0xce)</span><span class="sxs-lookup"><span data-stu-id="af045-592">206 (0xCE)</span></span>
</dt> <dt>



<span data-ttu-id="af045-593">Der Dateiname oder die Erweiterung ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="af045-593">The filename or extension is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-594"><span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**Fehler \_ RING2 \_ Stapel \_ wird \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="af045-594"><span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**ERROR\_RING2\_STACK\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-595">207 (0xCF)</span><span class="sxs-lookup"><span data-stu-id="af045-595">207 (0xCF)</span></span>
</dt> <dt>



<span data-ttu-id="af045-596">Der Stapel 2 wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="af045-596">The ring 2 stack is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-597"><span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**Fehler- \_ Meta- \_ Erweiterung \_ zu \_ lang**</span><span class="sxs-lookup"><span data-stu-id="af045-597"><span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**ERROR\_META\_EXPANSION\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-598">208 (0xd0)</span><span class="sxs-lookup"><span data-stu-id="af045-598">208 (0xD0)</span></span>
</dt> <dt>



<span data-ttu-id="af045-599">Die globalen Dateinamen Zeichen, \* oder?, werden falsch eingegeben, oder es werden zu viele globale Dateinamen Zeichen angegeben.</span><span class="sxs-lookup"><span data-stu-id="af045-599">The global filename characters, \* or ?, are entered incorrectly or too many global filename characters are specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-600"><span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**Fehler \_ ungültige \_ Signal \_ Nummer**</span><span class="sxs-lookup"><span data-stu-id="af045-600"><span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**ERROR\_INVALID\_SIGNAL\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-601">209 (0xD1)</span><span class="sxs-lookup"><span data-stu-id="af045-601">209 (0xD1)</span></span>
</dt> <dt>



<span data-ttu-id="af045-602">Das Signal, das gesendet wird, ist nicht richtig.</span><span class="sxs-lookup"><span data-stu-id="af045-602">The signal being posted is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-603"><span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**Fehler \_ Thread \_ 1 \_ inaktiv**</span><span class="sxs-lookup"><span data-stu-id="af045-603"><span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**ERROR\_THREAD\_1\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-604">210 (0xD2)</span><span class="sxs-lookup"><span data-stu-id="af045-604">210 (0xD2)</span></span>
</dt> <dt>



<span data-ttu-id="af045-605">Der Signalhandler kann nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="af045-605">The signal handler cannot be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-606"><span id="ERROR_LOCKED"></span><span id="error_locked"></span>**Fehler \_ gesperrt**</span><span class="sxs-lookup"><span data-stu-id="af045-606"><span id="ERROR_LOCKED"></span><span id="error_locked"></span>**ERROR\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-607">212 (0xd4)</span><span class="sxs-lookup"><span data-stu-id="af045-607">212 (0xD4)</span></span>
</dt> <dt>



<span data-ttu-id="af045-608">Das Segment ist gesperrt und kann nicht neu zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="af045-608">The segment is locked and cannot be reallocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-609"><span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**Fehler \_ zu \_ viele \_ Module**</span><span class="sxs-lookup"><span data-stu-id="af045-609"><span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**ERROR\_TOO\_MANY\_MODULES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-610">214 (0xd6)</span><span class="sxs-lookup"><span data-stu-id="af045-610">214 (0xD6)</span></span>
</dt> <dt>



<span data-ttu-id="af045-611">An dieses Programm oder Dynamic-Link-Modul sind zu viele Dynamic-Link-Module angefügt.</span><span class="sxs-lookup"><span data-stu-id="af045-611">Too many dynamic-link modules are attached to this program or dynamic-link module.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-612"><span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**Fehler Schachtelung \_ \_ nicht \_ zulässig**</span><span class="sxs-lookup"><span data-stu-id="af045-612"><span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**ERROR\_NESTING\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-613">215 (0xd7)</span><span class="sxs-lookup"><span data-stu-id="af045-613">215 (0xD7)</span></span>
</dt> <dt>



<span data-ttu-id="af045-614">Aufrufe von LoadModule können nicht geschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="af045-614">Cannot nest calls to LoadModule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-615"><span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**Fehler beim \_ exe- \_ Computer \_ Typen \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="af045-615"><span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**ERROR\_EXE\_MACHINE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-616">216 (0xD8)</span><span class="sxs-lookup"><span data-stu-id="af045-616">216 (0xD8)</span></span>
</dt> <dt>



<span data-ttu-id="af045-617">Diese Version von %1 ist nicht kompatibel mit der Windows-Version, die Sie ausführen.</span><span class="sxs-lookup"><span data-stu-id="af045-617">This version of %1 is not compatible with the version of Windows you're running.</span></span> <span data-ttu-id="af045-618">Überprüfen Sie die Systeminformationen Ihres Computers, und wenden Sie sich an den Hersteller der Software.</span><span class="sxs-lookup"><span data-stu-id="af045-618">Check your computer's system information and then contact the software publisher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-619"><span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**Fehler \_ exe \_ kann \_ die \_ signierte \_ Binärdatei nicht ändern**</span><span class="sxs-lookup"><span data-stu-id="af045-619"><span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**ERROR\_EXE\_CANNOT\_MODIFY\_SIGNED\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-620">217 (0xD9)</span><span class="sxs-lookup"><span data-stu-id="af045-620">217 (0xD9)</span></span>
</dt> <dt>



<span data-ttu-id="af045-621">Die Bilddatei "%1" ist signiert und kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="af045-621">The image file %1 is signed, unable to modify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-622"><span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**Fehler \_ exe \_ kann \_ die \_ starke \_ \_ binäre Binärdatei nicht ändern**</span><span class="sxs-lookup"><span data-stu-id="af045-622"><span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**ERROR\_EXE\_CANNOT\_MODIFY\_STRONG\_SIGNED\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-623">218 (0xda)</span><span class="sxs-lookup"><span data-stu-id="af045-623">218 (0xDA)</span></span>
</dt> <dt>



<span data-ttu-id="af045-624">Die Bilddatei "%1" ist stark signiert und kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="af045-624">The image file %1 is strong signed, unable to modify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-625"><span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**Fehler \_ Datei \_ ausgecheckt \_**</span><span class="sxs-lookup"><span data-stu-id="af045-625"><span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**ERROR\_FILE\_CHECKED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-626">220 (0xdc)</span><span class="sxs-lookup"><span data-stu-id="af045-626">220 (0xDC)</span></span>
</dt> <dt>



<span data-ttu-id="af045-627">Diese Datei ist ausgecheckt oder für die Bearbeitung durch einen anderen Benutzer gesperrt.</span><span class="sxs-lookup"><span data-stu-id="af045-627">This file is checked out or locked for editing by another user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-628"><span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**Fehler Auschecken \_ \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="af045-628"><span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**ERROR\_CHECKOUT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-629">221 (0xDD)</span><span class="sxs-lookup"><span data-stu-id="af045-629">221 (0xDD)</span></span>
</dt> <dt>



<span data-ttu-id="af045-630">Die Datei muss vor dem Speichern der Änderungen ausgecheckt werden.</span><span class="sxs-lookup"><span data-stu-id="af045-630">The file must be checked out before saving changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-631"><span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**fehlerhafter \_ \_ \_ Dateityp**</span><span class="sxs-lookup"><span data-stu-id="af045-631"><span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**ERROR\_BAD\_FILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-632">222 (0xde)</span><span class="sxs-lookup"><span data-stu-id="af045-632">222 (0xDE)</span></span>
</dt> <dt>



<span data-ttu-id="af045-633">Der Dateityp, der gespeichert oder abgerufen wird, wurde blockiert.</span><span class="sxs-lookup"><span data-stu-id="af045-633">The file type being saved or retrieved has been blocked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-634"><span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**Fehler \_ Datei \_ zu \_ groß**</span><span class="sxs-lookup"><span data-stu-id="af045-634"><span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**ERROR\_FILE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-635">223 (0xDF)</span><span class="sxs-lookup"><span data-stu-id="af045-635">223 (0xDF)</span></span>
</dt> <dt>



<span data-ttu-id="af045-636">Die Dateigröße überschreitet das zulässige Limit und kann nicht gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="af045-636">The file size exceeds the limit allowed and cannot be saved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-637"><span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**Fehler \_ Formular Authentifizierung \_ \_ erforderlich.**</span><span class="sxs-lookup"><span data-stu-id="af045-637"><span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**ERROR\_FORMS\_AUTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-638">224 (0xE0)</span><span class="sxs-lookup"><span data-stu-id="af045-638">224 (0xE0)</span></span>
</dt> <dt>



<span data-ttu-id="af045-639">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="af045-639">Access Denied.</span></span> <span data-ttu-id="af045-640">Vor dem Öffnen von Dateien an diesem Speicherort müssen Sie zuerst die Website zur Liste vertrauenswürdiger Sites hinzufügen, die Website aufrufen und die Option zum automatischen Anmelden auswählen.</span><span class="sxs-lookup"><span data-stu-id="af045-640">Before opening files in this location, you must first add the web site to your trusted sites list, browse to the web site, and select the option to login automatically.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-641"><span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**Fehler \_ Virus \_ infiziert**</span><span class="sxs-lookup"><span data-stu-id="af045-641"><span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**ERROR\_VIRUS\_INFECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-642">225 (0xe1)</span><span class="sxs-lookup"><span data-stu-id="af045-642">225 (0xE1)</span></span>
</dt> <dt>



<span data-ttu-id="af045-643">Der Vorgang wurde nicht erfolgreich abgeschlossen, weil die Datei einen Virus oder potenziell unerwünschte Software enthält.</span><span class="sxs-lookup"><span data-stu-id="af045-643">Operation did not complete successfully because the file contains a virus or potentially unwanted software.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-644"><span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**Fehler \_ Virus \_ gelöscht**</span><span class="sxs-lookup"><span data-stu-id="af045-644"><span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**ERROR\_VIRUS\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-645">226 (0xe2)</span><span class="sxs-lookup"><span data-stu-id="af045-645">226 (0xE2)</span></span>
</dt> <dt>



<span data-ttu-id="af045-646">Diese Datei enthält einen Virus oder potenziell unerwünschte Software und kann nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="af045-646">This file contains a virus or potentially unwanted software and cannot be opened.</span></span> <span data-ttu-id="af045-647">Aufgrund der Art dieses Virus oder potenziell unerwünschter Software wurde die Datei von diesem Speicherort entfernt.</span><span class="sxs-lookup"><span data-stu-id="af045-647">Due to the nature of this virus or potentially unwanted software, the file has been removed from this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-648"><span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**Fehler \_ Pipe \_ lokal**</span><span class="sxs-lookup"><span data-stu-id="af045-648"><span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**ERROR\_PIPE\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-649">229 (0xE5)</span><span class="sxs-lookup"><span data-stu-id="af045-649">229 (0xE5)</span></span>
</dt> <dt>



<span data-ttu-id="af045-650">Die Pipe ist lokal.</span><span class="sxs-lookup"><span data-stu-id="af045-650">The pipe is local.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-651"><span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**Fehler \_ hafte \_ Pipe**</span><span class="sxs-lookup"><span data-stu-id="af045-651"><span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**ERROR\_BAD\_PIPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-652">230 (0xe6)</span><span class="sxs-lookup"><span data-stu-id="af045-652">230 (0xE6)</span></span>
</dt> <dt>



<span data-ttu-id="af045-653">Der Pipe-Zustand ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="af045-653">The pipe state is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-654"><span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**Fehler \_ Pipe \_ ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="af045-654"><span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**ERROR\_PIPE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-655">231 (0xE7)</span><span class="sxs-lookup"><span data-stu-id="af045-655">231 (0xE7)</span></span>
</dt> <dt>



<span data-ttu-id="af045-656">Alle Pipeinstanzen sind ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="af045-656">All pipe instances are busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-657"><span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**Fehler \_ \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="af045-657"><span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**ERROR\_NO\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-658">232 (0xe8)</span><span class="sxs-lookup"><span data-stu-id="af045-658">232 (0xE8)</span></span>
</dt> <dt>



<span data-ttu-id="af045-659">Die Pipe wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="af045-659">The pipe is being closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-660"><span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**Fehler \_ Pipe ist \_ nicht \_ verbunden.**</span><span class="sxs-lookup"><span data-stu-id="af045-660"><span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**ERROR\_PIPE\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-661">233 (0xE9)</span><span class="sxs-lookup"><span data-stu-id="af045-661">233 (0xE9)</span></span>
</dt> <dt>



<span data-ttu-id="af045-662">Kein Prozess ist am anderen Ende der Pipe.</span><span class="sxs-lookup"><span data-stu-id="af045-662">No process is on the other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-663"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**Fehler \_ Weitere \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="af045-663"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-664">234 (0xEA)</span><span class="sxs-lookup"><span data-stu-id="af045-664">234 (0xEA)</span></span>
</dt> <dt>



<span data-ttu-id="af045-665">Weitere Daten sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af045-665">More data is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-666"><span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**Fehler- \_ VC- \_ getrennt**</span><span class="sxs-lookup"><span data-stu-id="af045-666"><span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**ERROR\_VC\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-667">240 (0xF)</span><span class="sxs-lookup"><span data-stu-id="af045-667">240 (0xF0)</span></span>
</dt> <dt>



<span data-ttu-id="af045-668">Die Sitzung wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="af045-668">The session was canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-669"><span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**\_ungültiger \_ EA- \_ Name.**</span><span class="sxs-lookup"><span data-stu-id="af045-669"><span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**ERROR\_INVALID\_EA\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-670">254 (0xFE)</span><span class="sxs-lookup"><span data-stu-id="af045-670">254 (0xFE)</span></span>
</dt> <dt>



<span data-ttu-id="af045-671">Der angegebene erweiterte Attribut Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="af045-671">The specified extended attribute name was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-672"><span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**Fehler- \_ EA- \_ Liste \_ inkonsistent**</span><span class="sxs-lookup"><span data-stu-id="af045-672"><span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**ERROR\_EA\_LIST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-673">255 (0xFF)</span><span class="sxs-lookup"><span data-stu-id="af045-673">255 (0xFF)</span></span>
</dt> <dt>



<span data-ttu-id="af045-674">Die erweiterten Attribute sind inkonsistent.</span><span class="sxs-lookup"><span data-stu-id="af045-674">The extended attributes are inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-675"><span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**Timeout für Wartezeit \_**</span><span class="sxs-lookup"><span data-stu-id="af045-675"><span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**WAIT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-676">258 (0x102)</span><span class="sxs-lookup"><span data-stu-id="af045-676">258 (0x102)</span></span>
</dt> <dt>



<span data-ttu-id="af045-677">Timeout bei Wartevorgang.</span><span class="sxs-lookup"><span data-stu-id="af045-677">The wait operation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-678"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**Fehler \_ keine \_ weiteren \_ Elemente**</span><span class="sxs-lookup"><span data-stu-id="af045-678"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-679">259 (0x103)</span><span class="sxs-lookup"><span data-stu-id="af045-679">259 (0x103)</span></span>
</dt> <dt>



<span data-ttu-id="af045-680">Es sind keine weiteren Daten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af045-680">No more data is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-681"><span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**Fehler \_ beim \_ Kopieren**</span><span class="sxs-lookup"><span data-stu-id="af045-681"><span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**ERROR\_CANNOT\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-682">266 (0x10A)</span><span class="sxs-lookup"><span data-stu-id="af045-682">266 (0x10A)</span></span>
</dt> <dt>



<span data-ttu-id="af045-683">Die Kopierfunktionen können nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af045-683">The copy functions cannot be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-684"><span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**Fehler \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="af045-684"><span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**ERROR\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-685">267 (0x10B)</span><span class="sxs-lookup"><span data-stu-id="af045-685">267 (0x10B)</span></span>
</dt> <dt>



<span data-ttu-id="af045-686">Der Verzeichnisname ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="af045-686">The directory name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-687"><span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**Fehler ( \_ EAS) \_ \_**</span><span class="sxs-lookup"><span data-stu-id="af045-687"><span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**ERROR\_EAS\_DIDNT\_FIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-688">275 (0x113)</span><span class="sxs-lookup"><span data-stu-id="af045-688">275 (0x113)</span></span>
</dt> <dt>



<span data-ttu-id="af045-689">Die erweiterten Attribute passten nicht in den Puffer.</span><span class="sxs-lookup"><span data-stu-id="af045-689">The extended attributes did not fit in the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-690"><span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**Fehler- \_ EA- \_ Datei \_ beschädigt**</span><span class="sxs-lookup"><span data-stu-id="af045-690"><span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**ERROR\_EA\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-691">276 (0x114)</span><span class="sxs-lookup"><span data-stu-id="af045-691">276 (0x114)</span></span>
</dt> <dt>



<span data-ttu-id="af045-692">Die erweiterte Attribut Datei im bereitgestellten Dateisystem ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="af045-692">The extended attribute file on the mounted file system is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-693"><span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**Fehler- \_ EA- \_ Tabelle \_ voll**</span><span class="sxs-lookup"><span data-stu-id="af045-693"><span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**ERROR\_EA\_TABLE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-694">277 (0x115)</span><span class="sxs-lookup"><span data-stu-id="af045-694">277 (0x115)</span></span>
</dt> <dt>



<span data-ttu-id="af045-695">Die Tabellen Datei für das erweiterte Attribut ist voll.</span><span class="sxs-lookup"><span data-stu-id="af045-695">The extended attribute table file is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-696"><span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**Fehler \_ ungültiges \_ EA- \_ handle.**</span><span class="sxs-lookup"><span data-stu-id="af045-696"><span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**ERROR\_INVALID\_EA\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-697">278 (0x116)</span><span class="sxs-lookup"><span data-stu-id="af045-697">278 (0x116)</span></span>
</dt> <dt>



<span data-ttu-id="af045-698">Das angegebene erweiterte Attribut Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="af045-698">The specified extended attribute handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-699"><span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**Fehler \_ EAS \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="af045-699"><span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**ERROR\_EAS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-700">282 (0x11A)</span><span class="sxs-lookup"><span data-stu-id="af045-700">282 (0x11A)</span></span>
</dt> <dt>



<span data-ttu-id="af045-701">Das bereitgestellte Dateisystem unterstützt keine erweiterten Attribute.</span><span class="sxs-lookup"><span data-stu-id="af045-701">The mounted file system does not support extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-702"><span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**Fehler \_ nicht \_ Besitzer**</span><span class="sxs-lookup"><span data-stu-id="af045-702"><span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**ERROR\_NOT\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-703">288 (0x120)</span><span class="sxs-lookup"><span data-stu-id="af045-703">288 (0x120)</span></span>
</dt> <dt>



<span data-ttu-id="af045-704">Es wurde versucht, Mutex freizugeben.</span><span class="sxs-lookup"><span data-stu-id="af045-704">Attempt to release mutex not owned by caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-705"><span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**Fehler \_ zu \_ viele \_ Beiträge**</span><span class="sxs-lookup"><span data-stu-id="af045-705"><span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**ERROR\_TOO\_MANY\_POSTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-706">298 (0x12A)</span><span class="sxs-lookup"><span data-stu-id="af045-706">298 (0x12A)</span></span>
</dt> <dt>



<span data-ttu-id="af045-707">Es wurden zu viele Beiträge an einem Semaphor vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="af045-707">Too many posts were made to a semaphore.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-708"><span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**Fehler \_ Teil \_ Kopie**</span><span class="sxs-lookup"><span data-stu-id="af045-708"><span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**ERROR\_PARTIAL\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-709">299 (0x12B)</span><span class="sxs-lookup"><span data-stu-id="af045-709">299 (0x12B)</span></span>
</dt> <dt>



<span data-ttu-id="af045-710">Nur ein Teil einer "Read processmemory"-oder "Write-processmemory"-Anforderung wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="af045-710">Only part of a ReadProcessMemory or WriteProcessMemory request was completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-711"><span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**Fehler " \_ Oplock" \_ nicht \_ erteilt**</span><span class="sxs-lookup"><span data-stu-id="af045-711"><span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**ERROR\_OPLOCK\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-712">300 (0x12C)</span><span class="sxs-lookup"><span data-stu-id="af045-712">300 (0x12C)</span></span>
</dt> <dt>



<span data-ttu-id="af045-713">Die Oplock-Anforderung wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="af045-713">The oplock request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-714"><span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**Fehler \_ beim \_ Oplock- \_ Protokoll.**</span><span class="sxs-lookup"><span data-stu-id="af045-714"><span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**ERROR\_INVALID\_OPLOCK\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-715">301 (0x12D)</span><span class="sxs-lookup"><span data-stu-id="af045-715">301 (0x12D)</span></span>
</dt> <dt>



<span data-ttu-id="af045-716">Vom System wurde eine ungültige Oplock-Bestätigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="af045-716">An invalid oplock acknowledgment was received by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-717"><span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**Fehler \_ Festplatte \_ zu \_ fragmentiert**</span><span class="sxs-lookup"><span data-stu-id="af045-717"><span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**ERROR\_DISK\_TOO\_FRAGMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-718">302 (0x12E)</span><span class="sxs-lookup"><span data-stu-id="af045-718">302 (0x12E)</span></span>
</dt> <dt>



<span data-ttu-id="af045-719">Das Volume ist zu fragmentiert, um diesen Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="af045-719">The volume is too fragmented to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-720"><span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**Fehler beim \_ Löschen \_ Ausstehend**</span><span class="sxs-lookup"><span data-stu-id="af045-720"><span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**ERROR\_DELETE\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-721">303 (0x12F)</span><span class="sxs-lookup"><span data-stu-id="af045-721">303 (0x12F)</span></span>
</dt> <dt>



<span data-ttu-id="af045-722">Die Datei kann nicht geöffnet werden, da Sie gerade gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="af045-722">The file cannot be opened because it is in the process of being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-723"><span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**Fehler nicht \_ kompatibel \_ mit der \_ \_ \_ \_ Registrierungs \_ Einstellung "globaler Kurzname"**</span><span class="sxs-lookup"><span data-stu-id="af045-723"><span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**ERROR\_INCOMPATIBLE\_WITH\_GLOBAL\_SHORT\_NAME\_REGISTRY\_SETTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-724">304 (0x130)</span><span class="sxs-lookup"><span data-stu-id="af045-724">304 (0x130)</span></span>
</dt> <dt>



<span data-ttu-id="af045-725">Auf diesem Volume können aufgrund der globalen Registrierungs Einstellung keine Kurznamen Einstellungen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="af045-725">Short name settings may not be changed on this volume due to the global registry setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-726"><span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**Fehler \_ \_ Kurznamen \_ sind \_ \_ auf dem \_ Volume nicht aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="af045-726"><span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**ERROR\_SHORT\_NAMES\_NOT\_ENABLED\_ON\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-727">305 (0x131)</span><span class="sxs-lookup"><span data-stu-id="af045-727">305 (0x131)</span></span>
</dt> <dt>



<span data-ttu-id="af045-728">Kurznamen sind auf diesem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="af045-728">Short names are not enabled on this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-729"><span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**Fehler \_ Sicherheitsdaten \_ Strom \_ ist \_ inkonsistent**</span><span class="sxs-lookup"><span data-stu-id="af045-729"><span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**ERROR\_SECURITY\_STREAM\_IS\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-730">306 (0x132)</span><span class="sxs-lookup"><span data-stu-id="af045-730">306 (0x132)</span></span>
</dt> <dt>



<span data-ttu-id="af045-731">Der Sicherheitsstream für das angegebene Volume befindet sich in einem inkonsistenten Zustand.</span><span class="sxs-lookup"><span data-stu-id="af045-731">The security stream for the given volume is in an inconsistent state.</span></span> <span data-ttu-id="af045-732">Führen Sie CHKDSK auf dem Volume aus.</span><span class="sxs-lookup"><span data-stu-id="af045-732">Please run CHKDSK on the volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-733"><span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**\_ungültiger \_ Sperr \_ Bereich.**</span><span class="sxs-lookup"><span data-stu-id="af045-733"><span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**ERROR\_INVALID\_LOCK\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-734">307 (0x133)</span><span class="sxs-lookup"><span data-stu-id="af045-734">307 (0x133)</span></span>
</dt> <dt>



<span data-ttu-id="af045-735">Ein angeforderter Vorgang zum Sperren von Dateien kann aufgrund eines ungültigen Byte Bereichs nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="af045-735">A requested file lock operation cannot be processed due to an invalid byte range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-736"><span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**Fehler \_ Bild- \_ Subsystem \_ nicht \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="af045-736"><span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**ERROR\_IMAGE\_SUBSYSTEM\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-737">308 (0x134)</span><span class="sxs-lookup"><span data-stu-id="af045-737">308 (0x134)</span></span>
</dt> <dt>



<span data-ttu-id="af045-738">Das für die Unterstützung des Image Typs erforderliche Subsystem ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="af045-738">The subsystem needed to support the image type is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-739"><span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**Fehler \_ Benachrichtigungs- \_ GUID \_ bereits \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="af045-739"><span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**ERROR\_NOTIFICATION\_GUID\_ALREADY\_DEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-740">309 (0x135)</span><span class="sxs-lookup"><span data-stu-id="af045-740">309 (0x135)</span></span>
</dt> <dt>



<span data-ttu-id="af045-741">Der angegebenen Datei ist bereits eine Benachrichtigungs-GUID zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="af045-741">The specified file already has a notification GUID associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-742"><span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**Fehler bei \_ ungültigem \_ Ausnahme \_ Handler.**</span><span class="sxs-lookup"><span data-stu-id="af045-742"><span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**ERROR\_INVALID\_EXCEPTION\_HANDLER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-743">310 (0x136)</span><span class="sxs-lookup"><span data-stu-id="af045-743">310 (0x136)</span></span>
</dt> <dt>



<span data-ttu-id="af045-744">Es wurde eine ungültige ausnahmehandlerroutine erkannt.</span><span class="sxs-lookup"><span data-stu-id="af045-744">An invalid exception handler routine has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-745"><span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**Fehler \_ doppelte \_ Berechtigungen**</span><span class="sxs-lookup"><span data-stu-id="af045-745"><span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**ERROR\_DUPLICATE\_PRIVILEGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-746">311 (0x137)</span><span class="sxs-lookup"><span data-stu-id="af045-746">311 (0x137)</span></span>
</dt> <dt>



<span data-ttu-id="af045-747">Doppelte Berechtigungen wurden für das Token angegeben.</span><span class="sxs-lookup"><span data-stu-id="af045-747">Duplicate privileges were specified for the token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-748"><span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**Fehler " \_ keine \_ Bereiche \_ verarbeitet"**</span><span class="sxs-lookup"><span data-stu-id="af045-748"><span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**ERROR\_NO\_RANGES\_PROCESSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-749">312 (0x138)</span><span class="sxs-lookup"><span data-stu-id="af045-749">312 (0x138)</span></span>
</dt> <dt>



<span data-ttu-id="af045-750">Es konnten keine Bereiche für den angegebenen Vorgang verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="af045-750">No ranges for the specified operation were able to be processed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-751"><span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**\_der Fehler \_ ist \_ in der \_ System \_ Datei nicht zulässig.**</span><span class="sxs-lookup"><span data-stu-id="af045-751"><span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**ERROR\_NOT\_ALLOWED\_ON\_SYSTEM\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-752">313 (0x139)</span><span class="sxs-lookup"><span data-stu-id="af045-752">313 (0x139)</span></span>
</dt> <dt>



<span data-ttu-id="af045-753">Der Vorgang ist für eine interne Dateisystem Datei nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="af045-753">Operation is not allowed on a file system internal file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-754"><span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**Fehler Datenträger \_ \_ Ressourcen \_ aufgebraucht**</span><span class="sxs-lookup"><span data-stu-id="af045-754"><span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**ERROR\_DISK\_RESOURCES\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-755">314 (0x13a)</span><span class="sxs-lookup"><span data-stu-id="af045-755">314 (0x13A)</span></span>
</dt> <dt>



<span data-ttu-id="af045-756">Die physischen Ressourcen dieses Datenträgers sind erschöpft.</span><span class="sxs-lookup"><span data-stu-id="af045-756">The physical resources of this disk have been exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-757"><span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**\_ungültiges \_ Token.**</span><span class="sxs-lookup"><span data-stu-id="af045-757"><span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**ERROR\_INVALID\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-758">315 (0x13B)</span><span class="sxs-lookup"><span data-stu-id="af045-758">315 (0x13B)</span></span>
</dt> <dt>



<span data-ttu-id="af045-759">Das Token, das die Daten darstellt, ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="af045-759">The token representing the data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-760"><span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**Fehler \_ Geräte \_ Funktion \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="af045-760"><span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**ERROR\_DEVICE\_FEATURE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-761">316 (0x13C)</span><span class="sxs-lookup"><span data-stu-id="af045-761">316 (0x13C)</span></span>
</dt> <dt>



<span data-ttu-id="af045-762">Das Gerät unterstützt die Befehls Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="af045-762">The device does not support the command feature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-763"><span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**Fehler "Mid" wurde \_ \_ \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="af045-763"><span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**ERROR\_MR\_MID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-764">317 (0x13D)</span><span class="sxs-lookup"><span data-stu-id="af045-764">317 (0x13D)</span></span>
</dt> <dt>



<span data-ttu-id="af045-765">Der Nachrichtentext für die Meldungs Nummer 0x %1 kann nicht in der Nachrichtendatei für %2 gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="af045-765">The system cannot find message text for message number 0x%1 in the message file for %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-766"><span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**Fehler \_ Bereich wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="af045-766"><span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**ERROR\_SCOPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-767">318 (0x13E)</span><span class="sxs-lookup"><span data-stu-id="af045-767">318 (0x13E)</span></span>
</dt> <dt>



<span data-ttu-id="af045-768">Der angegebene Bereich wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="af045-768">The scope specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-769"><span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**Fehler beim \_ undefinierten \_ Bereich**</span><span class="sxs-lookup"><span data-stu-id="af045-769"><span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**ERROR\_UNDEFINED\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-770">319 (0x13F)</span><span class="sxs-lookup"><span data-stu-id="af045-770">319 (0x13F)</span></span>
</dt> <dt>



<span data-ttu-id="af045-771">Die angegebene zentrale Zugriffs Richtlinie ist auf dem Zielcomputer nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="af045-771">The Central Access Policy specified is not defined on the target machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-772"><span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**\_ungültige \_ Obergrenze**</span><span class="sxs-lookup"><span data-stu-id="af045-772"><span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**ERROR\_INVALID\_CAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-773">320 (0x140)</span><span class="sxs-lookup"><span data-stu-id="af045-773">320 (0x140)</span></span>
</dt> <dt>



<span data-ttu-id="af045-774">Die von Active Directory erhaltene zentrale Zugriffs Richtlinie ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="af045-774">The Central Access Policy obtained from Active Directory is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-775"><span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**Fehler \_ Gerät \_ nicht erreichbar**</span><span class="sxs-lookup"><span data-stu-id="af045-775"><span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**ERROR\_DEVICE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-776">321 (0x141)</span><span class="sxs-lookup"><span data-stu-id="af045-776">321 (0x141)</span></span>
</dt> <dt>



<span data-ttu-id="af045-777">Das Gerät ist nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="af045-777">The device is unreachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-778"><span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**Fehler \_ Gerät " \_ keine \_ Ressourcen"**</span><span class="sxs-lookup"><span data-stu-id="af045-778"><span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**ERROR\_DEVICE\_NO\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-779">322 (0x142)</span><span class="sxs-lookup"><span data-stu-id="af045-779">322 (0x142)</span></span>
</dt> <dt>



<span data-ttu-id="af045-780">Das Zielgerät verfügt nicht über genügend Ressourcen, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="af045-780">The target device has insufficient resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-781"><span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**\_ \_ Prüfsummen \_ Fehler bei Fehler Daten.**</span><span class="sxs-lookup"><span data-stu-id="af045-781"><span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**ERROR\_DATA\_CHECKSUM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-782">323 (0x143)</span><span class="sxs-lookup"><span data-stu-id="af045-782">323 (0x143)</span></span>
</dt> <dt>



<span data-ttu-id="af045-783">Ein Prüfsummen Fehler bei der Datenintegrität ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="af045-783">A data integrity checksum error occurred.</span></span> <span data-ttu-id="af045-784">Die Daten im Dateistream sind beschädigt.</span><span class="sxs-lookup"><span data-stu-id="af045-784">Data in the file stream is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-785"><span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**Fehler \_ intergemischter \_ Kernel- \_ EA- \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="af045-785"><span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**ERROR\_INTERMIXED\_KERNEL\_EA\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-786">324 (0x144)</span><span class="sxs-lookup"><span data-stu-id="af045-786">324 (0x144)</span></span>
</dt> <dt>



<span data-ttu-id="af045-787">Es wurde versucht, einen Kernel und ein normales Erweitertes Attribut (EA) im selben Vorgang zu ändern.</span><span class="sxs-lookup"><span data-stu-id="af045-787">An attempt was made to modify both a KERNEL and normal Extended Attribute (EA) in the same operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-788"><span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**Trim-Fehler \_ Datei \_ Ebene \_ \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="af045-788"><span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**ERROR\_FILE\_LEVEL\_TRIM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-789">326 (0x146)</span><span class="sxs-lookup"><span data-stu-id="af045-789">326 (0x146)</span></span>
</dt> <dt>



<span data-ttu-id="af045-790">Das Gerät unterstützt keine Trim auf Dateiebene.</span><span class="sxs-lookup"><span data-stu-id="af045-790">Device does not support file-level TRIM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-791"><span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**Fehler \_ Offset- \_ Ausrichtungs \_ Verletzung**</span><span class="sxs-lookup"><span data-stu-id="af045-791"><span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**ERROR\_OFFSET\_ALIGNMENT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-792">327 (0x147)</span><span class="sxs-lookup"><span data-stu-id="af045-792">327 (0x147)</span></span>
</dt> <dt>



<span data-ttu-id="af045-793">Der Befehl hat einen Daten Offset angegeben, der nicht an der Granularität/Ausrichtung des Geräts ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="af045-793">The command specified a data offset that does not align to the device's granularity/alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-794"><span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**\_ungültiges \_ Feld \_ in \_ Parameter \_ Liste.**</span><span class="sxs-lookup"><span data-stu-id="af045-794"><span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**ERROR\_INVALID\_FIELD\_IN\_PARAMETER\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-795">328 (0x148)</span><span class="sxs-lookup"><span data-stu-id="af045-795">328 (0x148)</span></span>
</dt> <dt>



<span data-ttu-id="af045-796">Der Befehl hat ein ungültiges Feld in der Parameterliste angegeben.</span><span class="sxs-lookup"><span data-stu-id="af045-796">The command specified an invalid field in its parameter list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-797"><span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**Fehler Vorgang wird ausgeführt. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="af045-797"><span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**ERROR\_OPERATION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-798">329 (0x149)</span><span class="sxs-lookup"><span data-stu-id="af045-798">329 (0x149)</span></span>
</dt> <dt>



<span data-ttu-id="af045-799">Zurzeit wird ein Vorgang mit dem Gerät ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="af045-799">An operation is currently in progress with the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-800"><span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**fehlerhafter \_ \_ Geräte \_ Pfad**</span><span class="sxs-lookup"><span data-stu-id="af045-800"><span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**ERROR\_BAD\_DEVICE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-801">330 (0x14a)</span><span class="sxs-lookup"><span data-stu-id="af045-801">330 (0x14A)</span></span>
</dt> <dt>



<span data-ttu-id="af045-802">Es wurde versucht, den Befehl über einen ungültigen Pfad zum Zielgerät zu senden.</span><span class="sxs-lookup"><span data-stu-id="af045-802">An attempt was made to send down the command via an invalid path to the target device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-803"><span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**Fehler \_ zu \_ viele \_ Deskriptoren.**</span><span class="sxs-lookup"><span data-stu-id="af045-803"><span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**ERROR\_TOO\_MANY\_DESCRIPTORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-804">331 (0x14B)</span><span class="sxs-lookup"><span data-stu-id="af045-804">331 (0x14B)</span></span>
</dt> <dt>



<span data-ttu-id="af045-805">Der Befehl hat eine Reihe von Deskriptoren angegeben, die das vom Gerät unterstützte Maximum überschreiten.</span><span class="sxs-lookup"><span data-stu-id="af045-805">The command specified a number of descriptors that exceeded the maximum supported by the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-806"><span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**Fehler beim Bereinigen der \_ \_ Daten. \_**</span><span class="sxs-lookup"><span data-stu-id="af045-806"><span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**ERROR\_SCRUB\_DATA\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-807">332 (0x14c)</span><span class="sxs-lookup"><span data-stu-id="af045-807">332 (0x14C)</span></span>
</dt> <dt>



<span data-ttu-id="af045-808">Das Bereinigen ist für die angegebene Datei deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="af045-808">Scrub is disabled on the specified file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-809"><span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**Fehler \_ nicht \_ redundanter \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="af045-809"><span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**ERROR\_NOT\_REDUNDANT\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-810">333 (0x14d)</span><span class="sxs-lookup"><span data-stu-id="af045-810">333 (0x14D)</span></span>
</dt> <dt>



<span data-ttu-id="af045-811">Das Speichergerät bietet keine Redundanz.</span><span class="sxs-lookup"><span data-stu-id="af045-811">The storage device does not provide redundancy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-812"><span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**Fehler bei \_ Residenter \_ Datei \_ nicht \_ unterstützt**</span><span class="sxs-lookup"><span data-stu-id="af045-812"><span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**ERROR\_RESIDENT\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-813">334 (0x14E)</span><span class="sxs-lookup"><span data-stu-id="af045-813">334 (0x14E)</span></span>
</dt> <dt>



<span data-ttu-id="af045-814">Ein Vorgang wird für eine residente Datei nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="af045-814">An operation is not supported on a resident file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-815"><span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**Fehler \_ komprimierte \_ Datei \_ nicht \_ unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="af045-815"><span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**ERROR\_COMPRESSED\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-816">335 (0x14f)</span><span class="sxs-lookup"><span data-stu-id="af045-816">335 (0x14F)</span></span>
</dt> <dt>



<span data-ttu-id="af045-817">Ein Vorgang wird für eine komprimierte Datei nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="af045-817">An operation is not supported on a compressed file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-818"><span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**Fehler \_ Verzeichnis \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="af045-818"><span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**ERROR\_DIRECTORY\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-819">336 (0x150)</span><span class="sxs-lookup"><span data-stu-id="af045-819">336 (0x150)</span></span>
</dt> <dt>



<span data-ttu-id="af045-820">Ein Vorgang wird in einem Verzeichnis nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="af045-820">An operation is not supported on a directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-821"><span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**Fehler \_ \_ beim Lesen \_ aus der \_ Kopie.**</span><span class="sxs-lookup"><span data-stu-id="af045-821"><span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**ERROR\_NOT\_READ\_FROM\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-822">337 (0x151)</span><span class="sxs-lookup"><span data-stu-id="af045-822">337 (0x151)</span></span>
</dt> <dt>



<span data-ttu-id="af045-823">Die angegebene Kopie der angeforderten Daten konnte nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="af045-823">The specified copy of the requested data could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-824"><span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**Fehler \_ beim \_ NoAction- \_ Neustart**</span><span class="sxs-lookup"><span data-stu-id="af045-824"><span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**ERROR\_FAIL\_NOACTION\_REBOOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-825">350 (0x15e)</span><span class="sxs-lookup"><span data-stu-id="af045-825">350 (0x15E)</span></span>
</dt> <dt>



<span data-ttu-id="af045-826">Es wurde keine Aktion durchgeführt, da ein Systemneustart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="af045-826">No action was taken as a system reboot is required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-827"><span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**Fehler beim Herunterfahren. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="af045-827"><span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**ERROR\_FAIL\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-828">351 (0x15f)</span><span class="sxs-lookup"><span data-stu-id="af045-828">351 (0x15F)</span></span>
</dt> <dt>



<span data-ttu-id="af045-829">Fehler beim Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="af045-829">The shutdown operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-830"><span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**Fehler \_ beim \_ Neustart.**</span><span class="sxs-lookup"><span data-stu-id="af045-830"><span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**ERROR\_FAIL\_RESTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-831">352 (0x160)</span><span class="sxs-lookup"><span data-stu-id="af045-831">352 (0x160)</span></span>
</dt> <dt>



<span data-ttu-id="af045-832">Der Neustart Vorgang ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="af045-832">The restart operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-833"><span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**maximale Anzahl von Sitzungen des Fehlers \_ \_ \_ erreicht**</span><span class="sxs-lookup"><span data-stu-id="af045-833"><span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**ERROR\_MAX\_SESSIONS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-834">353 (0x161)</span><span class="sxs-lookup"><span data-stu-id="af045-834">353 (0x161)</span></span>
</dt> <dt>



<span data-ttu-id="af045-835">Die maximale Anzahl von Sitzungen wurde erreicht.</span><span class="sxs-lookup"><span data-stu-id="af045-835">The maximum number of sessions has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-836"><span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**Fehler \_ Thread \_ Modus \_ bereits im \_ Hintergrund**</span><span class="sxs-lookup"><span data-stu-id="af045-836"><span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**ERROR\_THREAD\_MODE\_ALREADY\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-837">400 (0x190)</span><span class="sxs-lookup"><span data-stu-id="af045-837">400 (0x190)</span></span>
</dt> <dt>



<span data-ttu-id="af045-838">Der Thread befindet sich bereits im Hintergrund Verarbeitungsmodus.</span><span class="sxs-lookup"><span data-stu-id="af045-838">The thread is already in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-839"><span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**Fehler im \_ Thread \_ Modus nicht im \_ \_ Hintergrund.**</span><span class="sxs-lookup"><span data-stu-id="af045-839"><span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**ERROR\_THREAD\_MODE\_NOT\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-840">401 (0x191)</span><span class="sxs-lookup"><span data-stu-id="af045-840">401 (0x191)</span></span>
</dt> <dt>



<span data-ttu-id="af045-841">Der Thread befindet sich nicht im Hintergrund Verarbeitungsmodus.</span><span class="sxs-lookup"><span data-stu-id="af045-841">The thread is not in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-842"><span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**Fehler \_ Prozess \_ Modus \_ bereits \_ Hintergrund**</span><span class="sxs-lookup"><span data-stu-id="af045-842"><span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**ERROR\_PROCESS\_MODE\_ALREADY\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-843">402 (0x192)</span><span class="sxs-lookup"><span data-stu-id="af045-843">402 (0x192)</span></span>
</dt> <dt>



<span data-ttu-id="af045-844">Der Prozess befindet sich bereits im Hintergrund Verarbeitungsmodus.</span><span class="sxs-lookup"><span data-stu-id="af045-844">The process is already in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-845"><span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**Fehler \_ Prozess \_ Modus \_ nicht im \_ Hintergrund**</span><span class="sxs-lookup"><span data-stu-id="af045-845"><span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**ERROR\_PROCESS\_MODE\_NOT\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-846">403 (0x193)</span><span class="sxs-lookup"><span data-stu-id="af045-846">403 (0x193)</span></span>
</dt> <dt>



<span data-ttu-id="af045-847">Der Prozess befindet sich nicht im Hintergrund Verarbeitungsmodus.</span><span class="sxs-lookup"><span data-stu-id="af045-847">The process is not in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af045-848"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**\_ungültige \_ Adresse.**</span><span class="sxs-lookup"><span data-stu-id="af045-848"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af045-849">487 (0x1e7)</span><span class="sxs-lookup"><span data-stu-id="af045-849">487 (0x1E7)</span></span>
</dt> <dt>



<span data-ttu-id="af045-850">Versuchen Sie, auf eine ungültige Adresse zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="af045-850">Attempt to access invalid address.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="af045-851">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af045-851">Requirements</span></span>



| <span data-ttu-id="af045-852">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af045-852">Requirement</span></span> | <span data-ttu-id="af045-853">Wert</span><span class="sxs-lookup"><span data-stu-id="af045-853">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af045-854">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af045-854">Minimum supported client</span></span><br/> | <span data-ttu-id="af045-855">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af045-855">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="af045-856">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af045-856">Minimum supported server</span></span><br/> | <span data-ttu-id="af045-857">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af045-857">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="af045-858">Header</span><span class="sxs-lookup"><span data-stu-id="af045-858">Header</span></span><br/>                   | <dl> <span data-ttu-id="af045-859"><dt>Winerror. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af045-859"><dt>WinError.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af045-860">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af045-860">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af045-861">System Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="af045-861">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




