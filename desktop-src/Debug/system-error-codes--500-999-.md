---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 500-999 und ist für Entwickler bestimmt.
ms.assetid: 8d8b427b-b761-4023-a834-a6eff96d6ba1
title: System Fehler Codes (500-999) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 02b35374fcb68f9b416948d5e39b2182f573b60f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214225"
---
# <a name="system-error-codes-500-999"></a><span data-ttu-id="d9ca0-103">System Fehler Codes (500-999)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-103">System Error Codes (500-999)</span></span>

> [!NOTE]
> <span data-ttu-id="d9ca0-104">Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="d9ca0-105">Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d9ca0-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="d9ca0-106">In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) (Fehler 500 bis 999) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-106">The following list describes [system error codes](system-error-codes.md) (errors 500 to 999).</span></span> <span data-ttu-id="d9ca0-107">Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="d9ca0-108">Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".</span><span class="sxs-lookup"><span data-stu-id="d9ca0-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="d9ca0-109"><span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**Fehler beim \_ Laden des Benutzer \_ Profils. \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-109"><span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**ERROR\_USER\_PROFILE\_LOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-110">500 (0x1F)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-110">500 (0x1F4)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-111">Das Benutzerprofil kann nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-111">User profile cannot be loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-112"><span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**Fehler \_ arithmetischer \_ Überlauf**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-112"><span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**ERROR\_ARITHMETIC\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-113">534 (0x216)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-113">534 (0x216)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-114">Arithmetisches Ergebnis hat 32 Bits überschritten.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-114">Arithmetic result exceeded 32 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-115"><span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**Fehler \_ Pipeline \_ verbunden**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-115"><span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**ERROR\_PIPE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-116">535 (0x217)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-116">535 (0x217)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-117">Es gibt einen Prozess an einem anderen Ende der Pipe.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-117">There is a process on other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-118"><span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**fehlerpipe-Überwachung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-118"><span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**ERROR\_PIPE\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-119">536 (0x218)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-119">536 (0x218)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-120">Warten, bis ein Prozess das andere Ende der Pipe öffnet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-120">Waiting for a process to open the other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-121"><span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**Fehler \_ Überprüfung \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-121"><span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**ERROR\_VERIFIER\_STOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-122">537 (0x219)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-122">537 (0x219)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-123">Der Anwendungs Verifier hat einen Fehler im aktuellen Prozess festgestellt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-123">Application verifier has found an error in the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-124"><span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**Fehler \_ bei der Fehlermeldung. \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-124"><span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**ERROR\_ABIOS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-125">538 (0x21a)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-125">538 (0x21A)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-126">Im ABIOS-Subsystem ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-126">An error occurred in the ABIOS subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-127"><span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**Fehler \_ WX86 \_ Warnung**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-127"><span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**ERROR\_WX86\_WARNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-128">539 (0x21b)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-128">539 (0x21B)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-129">Im WX86-Subsystem ist eine Warnung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-129">A warning occurred in the WX86 subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-130"><span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**Fehler \_ WX86 \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-130"><span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**ERROR\_WX86\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-131">540 (0x21c)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-131">540 (0x21C)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-132">Fehler im WX86-Subsystem.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-132">An error occurred in the WX86 subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-133"><span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**Fehler Zeit Geber \_ \_ nicht \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-133"><span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**ERROR\_TIMER\_NOT\_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-134">541 (0x21d)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-134">541 (0x21D)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-135">Es wurde versucht, einen Timer abzubrechen oder festzulegen, dem ein APC zugeordnet ist, und der Subjekt Thread ist nicht der Thread, der den Timer ursprünglich mit einer zugeordneten APC-Routine festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-135">An attempt was made to cancel or set a timer that has an associated APC and the subject thread is not the thread that originally set the timer with an associated APC routine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-136"><span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**Fehler \_ beim Entladen**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-136"><span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**ERROR\_UNWIND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-137">542 (0x21e)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-137">542 (0x21E)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-138">Entladen Sie den Ausnahme Code.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-138">Unwind exception code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-139"><span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**fehlerhafter \_ \_ Stapelfehler**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-139"><span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**ERROR\_BAD\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-140">543 (0x21f)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-140">543 (0x21F)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-141">Während eines Entladevorgangs wurde ein ungültiger oder nicht ausgerichteter Stapel gefunden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-141">An invalid or unaligned stack was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-142"><span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**Fehler beim Entladen des \_ \_ \_ Ziels.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-142"><span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**ERROR\_INVALID\_UNWIND\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-143">544 (0x220)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-143">544 (0x220)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-144">Während eines Entladevorgangs wurde ein ungültiges Entlade Ziel gefunden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-144">An invalid unwind target was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-145"><span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**\_ungültige \_ Port \_ Attribute.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-145"><span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**ERROR\_INVALID\_PORT\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-146">545 (0x221)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-146">545 (0x221)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-147">Ungültige Objekt Attribute für ntkreateport angegeben, oder für NtConnectPort wurden ungültige Port Attribute angegeben.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-147">Invalid Object Attributes specified to NtCreatePort or invalid Port Attributes specified to NtConnectPort</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-148"><span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**\_fehlerport \_ Meldung \_ zu \_ lang**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-148"><span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**ERROR\_PORT\_MESSAGE\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-149">546 (0x222)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-149">546 (0x222)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-150">Die Länge der an ntrequestport oder ntrequestwaitreplyport übergebenen Nachricht ist länger als die vom Port zulässige maximale Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-150">Length of message passed to NtRequestPort or NtRequestWaitReplyPort was longer than the maximum message allowed by the port.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-151"><span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**Fehler \_ ungültiges \_ Kontingent \_ niedriger.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-151"><span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**ERROR\_INVALID\_QUOTA\_LOWER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-152">547 (0x223)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-152">547 (0x223)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-153">Es wurde versucht, eine Kontingent Grenze unterhalb der aktuellen Nutzung zu verringern.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-153">An attempt was made to lower a quota limit below the current usage.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-154"><span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**Fehler \_ Gerät \_ bereits \_ angefügt**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-154"><span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**ERROR\_DEVICE\_ALREADY\_ATTACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-155">548 (0x224)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-155">548 (0x224)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-156">Es wurde versucht, eine Verbindung mit einem Gerät anzufügen, das bereits an ein anderes Gerät angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-156">An attempt was made to attach to a device that was already attached to another device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-157"><span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**\_ \_ Fehlausrichtung der Fehler Anweisung**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-157"><span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**ERROR\_INSTRUCTION\_MISALIGNMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-158">549 (0x225)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-158">549 (0x225)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-159">Es wurde versucht, eine Anweisung an einer nicht ausgerichteten Adresse auszuführen, und das Host System unterstützt keine nicht ausgerichteten Anweisungs Verweise.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-159">An attempt was made to execute an instruction at an unaligned address and the host system does not support unaligned instruction references.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-160"><span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**Fehler \_ Profilerstellung \_ nicht \_ gestartet**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-160"><span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**ERROR\_PROFILING\_NOT\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-161">550 (0x226)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-161">550 (0x226)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-162">Die Profilerstellung wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-162">Profiling not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-163"><span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**Fehler \_ Profilerstellung \_ nicht \_ beendet**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-163"><span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**ERROR\_PROFILING\_NOT\_STOPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-164">551 (0x227)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-164">551 (0x227)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-165">Die Profilerstellung wurde nicht beendet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-165">Profiling not stopped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-166"><span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**Fehler \_ beim \_ \_ interpretieren**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-166"><span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**ERROR\_COULD\_NOT\_INTERPRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-167">552 (0x228)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-167">552 (0x228)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-168">Die bestandene ACL enthielt nicht die erforderlichen Mindestinformationen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-168">The passed ACL did not contain the minimum required information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-169"><span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**Fehler \_ Profilerstellung \_ bei \_ Limit**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-169"><span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**ERROR\_PROFILING\_AT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-170">553 (0x229)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-170">553 (0x229)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-171">Die Anzahl aktiver Profil Erstellungs Objekte hat den Höchstwert, und es können keine weiteren Objekte gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-171">The number of active profiling objects is at the maximum and no more may be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-172"><span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**Fehler \_ beim \_ warten.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-172"><span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ERROR\_CANT\_WAIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-173">554 (0x22a)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-173">554 (0x22A)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-174">Wird verwendet, um anzugeben, dass ein Vorgang ohne Blockierung für e/a nicht fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-174">Used to indicate that an operation cannot continue without blocking for I/O.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-175"><span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**Fehler \_ beim \_ Beenden von \_ Self.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-175"><span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ERROR\_CANT\_TERMINATE\_SELF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-176">555 (0x22b)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-176">555 (0x22B)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-177">Gibt an, dass ein Thread standardmäßig versucht hat, sich selbst zu beenden (mit dem Namen NtTerminateThread mit **null**) und dem letzten Thread im aktuellen Prozess.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-177">Indicates that a thread attempted to terminate itself by default (called NtTerminateThread with **NULL**) and it was the last thread in the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-178"><span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**Fehler \_ unerwartetes mm-Fehler beim \_ \_ Erstellen \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-178"><span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**ERROR\_UNEXPECTED\_MM\_CREATE\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-179">556 (0x22c)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-179">556 (0x22C)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-180">Wenn ein mm-Fehler zurückgegeben wird, der nicht im standardmäßigen FsRtl-Filter definiert ist, wird er in einen der folgenden Fehler konvertiert, der im Filter garantiert ist.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-180">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="d9ca0-181">In diesem Fall gehen die Informationen verloren, der Filter behandelt die Ausnahme jedoch ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-181">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-182"><span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**\_unerwarteter Fehler bei \_ mm- \_ Zuordnung. \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-182"><span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**ERROR\_UNEXPECTED\_MM\_MAP\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-183">557 (0x22d)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-183">557 (0x22D)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-184">Wenn ein mm-Fehler zurückgegeben wird, der nicht im standardmäßigen FsRtl-Filter definiert ist, wird er in einen der folgenden Fehler konvertiert, der im Filter garantiert ist.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-184">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="d9ca0-185">In diesem Fall gehen die Informationen verloren, der Filter behandelt die Ausnahme jedoch ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-185">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-186"><span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**Fehler \_ unerwartetes \_ mm- \_ Erweitern von \_ Err**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-186"><span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**ERROR\_UNEXPECTED\_MM\_EXTEND\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-187">558 (0x22e)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-187">558 (0x22E)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-188">Wenn ein mm-Fehler zurückgegeben wird, der nicht im standardmäßigen FsRtl-Filter definiert ist, wird er in einen der folgenden Fehler konvertiert, der im Filter garantiert ist.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-188">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="d9ca0-189">In diesem Fall gehen die Informationen verloren, der Filter behandelt die Ausnahme jedoch ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-189">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-190"><span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**Fehler \_ hafte \_ Funktions \_ Tabelle**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-190"><span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**ERROR\_BAD\_FUNCTION\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-191">559 (0x22f)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-191">559 (0x22F)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-192">Bei einem Entladevorgang wurde eine falsch formatierte Funktions Tabelle gefunden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-192">A malformed function table was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-193"><span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**Fehler \_ keine \_ GUID- \_ Übersetzung**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-193"><span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**ERROR\_NO\_GUID\_TRANSLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-194">560 (0x230)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-194">560 (0x230)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-195">Gibt an, dass versucht wurde, eine Datei oder ein Verzeichnis des Dateisystems zu schützen. eine der SIDs in der Sicherheits Beschreibung konnte nicht in eine GUID übersetzt werden, die vom Dateisystem gespeichert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-195">Indicates that an attempt was made to assign protection to a file system file or directory and one of the SIDs in the security descriptor could not be translated into a GUID that could be stored by the file system.</span></span> <span data-ttu-id="d9ca0-196">Dies bewirkt, dass der Schutz Versuch fehlschlägt, was dazu führen kann, dass bei der Dateierstellung ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-196">This causes the protection attempt to fail, which may cause a file creation attempt to fail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-197"><span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**Fehler \_ ungültige \_ LDT- \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-197"><span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**ERROR\_INVALID\_LDT\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-198">561 (0x231)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-198">561 (0x231)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-199">Gibt an, dass versucht wurde, einen LDT zu vergrößern, indem er seine Größe festgelegt hat, oder dass die Größe keine gerade Anzahl von Selektoren war.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-199">Indicates that an attempt was made to grow an LDT by setting its size, or that the size was not an even number of selectors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-200"><span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**Fehler \_ beim \_ LDT- \_ Offset.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-200"><span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**ERROR\_INVALID\_LDT\_OFFSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-201">563 (0x233)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-201">563 (0x233)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-202">Gibt an, dass der Startwert für die LDT-Informationen kein ganzzahliges Vielfaches der Auswahl Größe war.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-202">Indicates that the starting value for the LDT information was not an integral multiple of the selector size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-203"><span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**Fehler \_ ungültiger \_ LDT- \_ Deskriptor.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-203"><span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**ERROR\_INVALID\_LDT\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-204">564 (0x234)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-204">564 (0x234)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-205">Gibt an, dass der Benutzer beim Einrichten von LDT-Deskriptoren einen ungültigen Deskriptor bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-205">Indicates that the user supplied an invalid descriptor when trying to set up Ldt descriptors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-206"><span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**Fehler \_ zu \_ viele \_ Threads.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-206"><span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**ERROR\_TOO\_MANY\_THREADS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-207">565 (0x235)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-207">565 (0x235)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-208">Gibt an, dass ein Prozess zu viele Threads enthält, um die angeforderte Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-208">Indicates a process has too many threads to perform the requested action.</span></span> <span data-ttu-id="d9ca0-209">Beispielsweise kann die Zuweisung eines primären Tokens nur ausgeführt werden, wenn ein Prozess über keinen oder einen Thread verfügt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-209">For example, assignment of a primary token may only be performed when a process has zero or one threads.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-210"><span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**Fehler \_ Thread \_ nicht \_ in \_ Verarbeitung**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-210"><span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**ERROR\_THREAD\_NOT\_IN\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-211">566 (0x236)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-211">566 (0x236)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-212">Es wurde versucht, einen Thread in einem bestimmten Prozess auszuführen, aber der angegebene Thread befindet sich nicht im angegebenen Prozess.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-212">An attempt was made to operate on a thread within a specific process, but the thread specified is not in the process specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-213"><span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**Fehler beim Seiten \_ Datei \_ Kontingent \_ überschritten.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-213"><span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**ERROR\_PAGEFILE\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-214">567 (0x237)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-214">567 (0x237)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-215">Das Seiten Datei Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-215">Page file quota was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-216"><span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**Fehler beim \_ Anmelden des \_ Servers. \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-216"><span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**ERROR\_LOGON\_SERVER\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-217">568 (0x238)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-217">568 (0x238)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-218">Der Netlogon-Dienst kann nicht gestartet werden, da ein anderer in der Domäne laufender Anmeldedienst mit der angegebenen Rolle in Konflikt steht.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-218">The Netlogon service cannot start because another Netlogon service running in the domain conflicts with the specified role.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-219"><span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**Fehler \_ Synchronisierung \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-219"><span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**ERROR\_SYNCHRONIZATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-220">569 (0x239)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-220">569 (0x239)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-221">Die SAM-Datenbank auf einem Windows-Server ist deutlich nicht mit der Kopie auf dem Domänen Controller synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-221">The SAM database on a Windows Server is significantly out of synchronization with the copy on the Domain Controller.</span></span> <span data-ttu-id="d9ca0-222">Eine komplette Synchronisierung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-222">A complete synchronization is required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-223"><span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**Fehler \_ beim \_ Öffnen von NET Open \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-223"><span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**ERROR\_NET\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-224">570 (0x23a)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-224">570 (0x23A)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-225">Fehler bei der ntkreatefile-API.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-225">The NtCreateFile API failed.</span></span> <span data-ttu-id="d9ca0-226">Dieser Fehler sollte niemals an eine Anwendung zurückgegeben werden. er ist ein Platzhalter, den der Windows-LAN-Manager-Redirector in seinen internen Fehler zuordnungsroutinen verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-226">This error should never be returned to an application, it is a place holder for the Windows Lan Manager Redirector to use in its internal error mapping routines.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-227"><span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**Fehler bei \_ IO- \_ Berechtigung \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-227"><span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**ERROR\_IO\_PRIVILEGE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-228">571 (0x23b)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-228">571 (0x23B)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-229">{Berechtigungs Fehler} Die e/a-Berechtigungen für den Prozess konnten nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-229">{Privilege Failed} The I/O permissions for the process could not be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-230"><span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**Fehler \_ Steuerung \_ C \_ Beenden**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-230"><span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**ERROR\_CONTROL\_C\_EXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-231">572 (0x23c)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-231">572 (0x23C)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-232">{Beenden der Anwendung durch STRG + C} Die Anwendung wurde als Ergebnis von STRG + C beendet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-232">{Application Exit by CTRL+C} The application terminated as a result of a CTRL+C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-233"><span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**Fehler \_ bei \_ Systemdatei.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-233"><span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**ERROR\_MISSING\_SYSTEMFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-234">573 (0x23d)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-234">573 (0x23D)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-235">{System Datei fehlt} Die erforderliche Systemdatei "% hs" ist nicht vorhanden oder fehlt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-235">{Missing System File} The required system file %hs is bad or missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-236"><span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**\_nicht behandelte \_ Ausnahme Fehler.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-236"><span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**ERROR\_UNHANDLED\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-237">574 (0x23e)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-237">574 (0x23E)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-238">{Anwendungsfehler} Die Ausnahme '% s ' (0x% 08lx) ist in der Anwendung an Speicherort 0x% 08lX aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-238">{Application Error} The exception %s (0x%08lx) occurred in the application at location 0x%08lx.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-239"><span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**Fehler- \_ App- \_ Init \_ -Fehler**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-239"><span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**ERROR\_APP\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-240">575 (0x23f)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-240">575 (0x23F)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-241">{Anwendungsfehler} Die Anwendung konnte nicht ordnungsgemäß gestartet werden (0x% LX).</span><span class="sxs-lookup"><span data-stu-id="d9ca0-241">{Application Error} The application was unable to start correctly (0x%lx).</span></span> <span data-ttu-id="d9ca0-242">Klicken Sie auf OK, um die Anwendung zu schließen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-242">Click OK to close the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-243"><span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**Fehler beim Erstellen der Fehler \_ Datei. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-243"><span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**ERROR\_PAGEFILE\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-244">576 (0x240)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-244">576 (0x240)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-245">{Paging-Datei konnte nicht erstellt werden.} Fehler beim Erstellen der Auslagerungs Datei "% hs" (% LX).</span><span class="sxs-lookup"><span data-stu-id="d9ca0-245">{Unable to Create Paging File} The creation of the paging file %hs failed (%lx).</span></span> <span data-ttu-id="d9ca0-246">Die angeforderte Größe war% LD.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-246">The requested size was %ld.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-247"><span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**\_ungültiger \_ \_ bildhash.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-247"><span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**ERROR\_INVALID\_IMAGE\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-248">577 (0x241)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-248">577 (0x241)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-249">Die digitale Signatur für diese Datei kann nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-249">Windows cannot verify the digital signature for this file.</span></span> <span data-ttu-id="d9ca0-250">Bei einer aktuellen Hardware-oder Software Änderung wurde möglicherweise eine beschädigte oder beschädigte Datei oder Schadsoftware aus einer unbekannten Quelle installiert.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-250">A recent hardware or software change might have installed a file that is signed incorrectly or damaged, or that might be malicious software from an unknown source.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-251"><span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**Fehler " \_ keine \_ Pagefile"**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-251"><span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**ERROR\_NO\_PAGEFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-252">578 (0x242)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-252">578 (0x242)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-253">{Keine Auslagerungs Datei angegeben} In der Systemkonfiguration wurde keine Auslagerungs Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-253">{No Paging File Specified} No paging file was specified in the system configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-254"><span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**Ungültiger \_ \_ float- \_ Kontext.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-254"><span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**ERROR\_ILLEGAL\_FLOAT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-255">579 (0x243)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-255">579 (0x243)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-256">Distanzieren Eine Anwendung im realen Modus hat eine Gleit Komma Anweisung ausgegeben, und es ist keine Gleit Komma Hardware vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-256">{EXCEPTION} A real-mode application issued a floating-point instruction and floating-point hardware is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-257"><span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**Fehler " \_ kein \_ Ereignis \_ Paar"**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-257"><span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**ERROR\_NO\_EVENT\_PAIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-258">580 (0x244)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-258">580 (0x244)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-259">Ein Ereignispaar-Synchronisierungs Vorgang wurde mithilfe des Thread spezifischen Client/Server-Ereignispaar Objekts durchgeführt, aber es wurde kein Ereignispaar Objekt mit dem Thread verknüpft.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-259">An event pair synchronization operation was performed using the thread specific client/server event pair object, but no event pair object was associated with the thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-260"><span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**Fehler \_ Domäne \_ ctrlr- \_ Konfigurations \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-260"><span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**ERROR\_DOMAIN\_CTRLR\_CONFIG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-261">581 (0x245)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-261">581 (0x245)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-262">Ein Windows-Server weist eine falsche Konfiguration auf.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-262">A Windows Server has an incorrect configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-263"><span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**Ungültiges \_ \_ Zeichen.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-263"><span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**ERROR\_ILLEGAL\_CHARACTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-264">582 (0x246)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-264">582 (0x246)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-265">Ein ungültiges Zeichen wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-265">An illegal character was encountered.</span></span> <span data-ttu-id="d9ca0-266">Bei einem Multibyte-Zeichensatz enthält dies ein führendes Byte ohne nachfolgende nachfolgende Byte.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-266">For a multi-byte character set this includes a lead byte without a succeeding trail byte.</span></span> <span data-ttu-id="d9ca0-267">Für den Unicode-Zeichensatz enthält dies die Zeichen 0xFFFF und 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-267">For the Unicode character set this includes the characters 0xFFFF and 0xFFFE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-268"><span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**Fehler nicht \_ definiertes \_ Zeichen**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-268"><span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**ERROR\_UNDEFINED\_CHARACTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-269">583 (0x247)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-269">583 (0x247)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-270">Das Unicode-Zeichen ist nicht im Unicode-Zeichensatz definiert, der auf dem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-270">The Unicode character is not defined in the Unicode character set installed on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-271"><span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**Fehler \_ Disketten \_ Volume**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-271"><span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**ERROR\_FLOPPY\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-272">584 (0x248)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-272">584 (0x248)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-273">Die Auslagerungs Datei kann nicht auf einer Disketten Diskette erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-273">The paging file cannot be created on a floppy diskette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-274"><span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**Fehler-BIOS-Fehler beim \_ \_ \_ \_ Verbinden von \_ Interrupt**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-274"><span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**ERROR\_BIOS\_FAILED\_TO\_CONNECT\_INTERRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-275">585 (0x249)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-275">585 (0x249)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-276">Das System-BIOS konnte einen System Interrupt nicht mit dem Gerät oder dem Bus verbinden, für das das Gerät angeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-276">The system BIOS failed to connect a system interrupt to the device or bus for which the device is connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-277"><span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**Fehler \_ Sicherungs \_ Controller**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-277"><span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**ERROR\_BACKUP\_CONTROLLER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-278">586 (0x24a)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-278">586 (0x24A)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-279">Dieser Vorgang ist nur für den primären Domänen Controller der Domäne zulässig.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-279">This operation is only allowed for the Primary Domain Controller of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-280"><span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**Fehler \_ Mutant \_ Limit \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-280"><span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**ERROR\_MUTANT\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-281">587 (0x24b)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-281">587 (0x24B)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-282">Es wurde versucht, eine muant so zu erhalten, dass die maximale Anzahl überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-282">An attempt was made to acquire a mutant such that its maximum count would have been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-283"><span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**Fehler- \_ FS- \_ Treiber \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-283"><span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**ERROR\_FS\_DRIVER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-284">588 (0x24c)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-284">588 (0x24C)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-285">Es wurde auf ein Volume zugegriffen, für das ein Dateisystem Treiber erforderlich ist, der noch nicht geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-285">A volume has been accessed for which a file system driver is required that has not yet been loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-286"><span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**Fehler \_ beim \_ Laden der \_ Registrierungs \_ Datei.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-286"><span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**ERROR\_CANNOT\_LOAD\_REGISTRY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-287">589 (0x24d)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-287">589 (0x24D)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-288">{Fehler bei der Registrierungsdatei} Die Registrierung kann die Hive (Datei) nicht laden:% HS oder Ihr Protokoll oder eine Alternative.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-288">{Registry File Failure} The registry cannot load the hive (file): %hs or its log or alternate.</span></span> <span data-ttu-id="d9ca0-289">Er ist beschädigt, fehlt oder ist nicht beschreibbar.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-289">It is corrupt, absent, or not writable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-290"><span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**Fehler beim \_ Debuggen des Fehlers \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-290"><span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**ERROR\_DEBUG\_ATTACH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-291">590 (0x24e)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-291">590 (0x24E)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-292">{Unerwarteter Fehler in [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} Unerwarteter Fehler beim Verarbeiten einer **DebugActiveProcess** -API-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-292">{Unexpected Failure in [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} An unexpected failure occurred while processing a **DebugActiveProcess** API request.</span></span> <span data-ttu-id="d9ca0-293">Sie können OK auswählen, um den Prozess zu beenden, oder Abbrechen, um den Fehler zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-293">You may choose OK to terminate the process, or Cancel to ignore the error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-294"><span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**Fehler \_ System \_ Prozess wurde \_ beendet.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-294"><span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**ERROR\_SYSTEM\_PROCESS\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-295">591 (0x24f)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-295">591 (0x24F)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-296">{Schwerwiegender System Fehler} Der% HS-System Prozess wurde unerwartet mit dem Status 0x% 08x (0x% 08x 0x% 08x) beendet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-296">{Fatal System Error} The %hs system process terminated unexpectedly with a status of 0x%08x (0x%08x 0x%08x).</span></span> <span data-ttu-id="d9ca0-297">Das System wurde heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-297">The system has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-298"><span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**Fehler \_ Daten wurden \_ nicht \_ akzeptiert.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-298"><span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**ERROR\_DATA\_NOT\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-299">592 (0x250)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-299">592 (0x250)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-300">{Daten nicht akzeptiert} Der TDI-Client konnte die während einer Angabe empfangenen Daten nicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-300">{Data Not Accepted} The TDI client could not handle the data received during an indication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-301"><span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**VDM-Fehler mit \_ \_ hartem \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-301"><span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**ERROR\_VDM\_HARD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-302">593 (0x251)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-302">593 (0x251)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-303">Fehler bei ntvdm.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-303">NTVDM encountered a hard error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-304"><span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**Timeout beim Abbrechen des Fehler \_ Treibers \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-304"><span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**ERROR\_DRIVER\_CANCEL\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-305">594 (0x252)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-305">594 (0x252)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-306">{Abbruch Timeout} Der Treiber% HS konnte eine abgebrochene e/a-Anforderung in der vorgesehenen Zeit nicht beenden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-306">{Cancel Timeout} The driver %hs failed to complete a cancelled I/O request in the allotted time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-307"><span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**Fehler beim Antworten auf die Fehler \_ \_ Meldung. \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-307"><span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**ERROR\_REPLY\_MESSAGE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-308">595 (0x253)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-308">595 (0x253)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-309">{Antwort Nachrichten stimmen nicht überein. Es wurde versucht, auf eine LPC-Nachricht zu antworten, aber der Thread, der von der Client-ID in der Nachricht angegeben wurde, hat nicht auf diese Nachricht gewartet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-309">{Reply Message Mismatch} An attempt was made to reply to an LPC message, but the thread specified by the client ID in the message was not waiting on that message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-310"><span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**Fehler \_ beim \_ Zurückschreiben von \_ Daten.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-310"><span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-311">596 (0x254)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-311">596 (0x254)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-312">{Verzögertes Schreiben fehlgeschlagen} Es konnten nicht alle Daten für die Datei "% hs" gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-312">{Delayed Write Failed} Windows was unable to save all the data for the file %hs.</span></span> <span data-ttu-id="d9ca0-313">Die Daten sind verloren gegangen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-313">The data has been lost.</span></span> <span data-ttu-id="d9ca0-314">Dieser Fehler kann durch einen Ausfall der Computer Hardware oder Netzwerkverbindung verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-314">This error may be caused by a failure of your computer hardware or network connection.</span></span> <span data-ttu-id="d9ca0-315">Versuchen Sie, diese Datei an anderer Stelle zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-315">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-316"><span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**Fehler bei \_ Client \_ Server \_ Parametern \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-316"><span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**ERROR\_CLIENT\_SERVER\_PARAMETERS\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-317">597 (0x255)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-317">597 (0x255)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-318">Die Parameter, die im Fenster "Shared Memory" für Client/Server an den Server übergeben wurden, waren ungültig.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-318">The parameter(s) passed to the server in the client/server shared memory window were invalid.</span></span> <span data-ttu-id="d9ca0-319">Möglicherweise wurden zu viele Daten im freigegebenen Speicherfenster abgelegt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-319">Too much data may have been put in the shared memory window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-320"><span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**Fehler ist \_ kein \_ kleiner Daten \_ Strom.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-320"><span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**ERROR\_NOT\_TINY\_STREAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-321">598 (0x256)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-321">598 (0x256)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-322">Der Stream ist kein kleiner Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-322">The stream is not a tiny stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-323"><span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**Fehler \_ Stapel \_ Überlauf \_ Lesevorgang**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-323"><span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**ERROR\_STACK\_OVERFLOW\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-324">599 (0x257)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-324">599 (0x257)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-325">Die Anforderung muss vom Stapelüberlauf Code verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-325">The request must be handled by the stack overflow code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-326"><span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**Fehler \_ \_ in " \_ groß" konvertieren**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-326"><span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**ERROR\_CONVERT\_TO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-327">600 (0x258)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-327">600 (0x258)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-328">Interne OFS-Statuscodes, die angeben, wie eine Zuordnungs Operation verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-328">Internal OFS status codes indicating how an allocation operation is handled.</span></span> <span data-ttu-id="d9ca0-329">Der Vorgang wird wiederholt, nachdem der enthaltende onode verschoben oder der Blockdaten Strom in einen großen Stream konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-329">Either it is retried after the containing onode is moved or the extent stream is converted to a large stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-330"><span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**Fehler \_ im Gültigkeits \_ \_ \_ Bereich gefunden**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-330"><span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**ERROR\_FOUND\_OUT\_OF\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-331">601 (0x259)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-331">601 (0x259)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-332">Beim Versuch, das Objekt zu finden, wurde ein Objekt gefunden, das anhand der ID auf dem Volume übereinstimmt, aber es liegt außerhalb des Gültigkeits Bereichs des für den Vorgang verwendeten Handles.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-332">The attempt to find the object found an object matching by ID on the volume but it is out of the scope of the handle used for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-333"><span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**Fehler beim \_ Zuordnen von \_ Bucket**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-333"><span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**ERROR\_ALLOCATE\_BUCKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-334">602 (0x25a)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-334">602 (0x25A)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-335">Das Bucket-Array muss vergrößert werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-335">The bucket array must be grown.</span></span> <span data-ttu-id="d9ca0-336">Wiederholen Sie die Transaktion.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-336">Retry transaction after doing so.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-337"><span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**Fehler \_ Mars Hall \_ Überlauf**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-337"><span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**ERROR\_MARSHALL\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-338">603 (0x25b)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-338">603 (0x25B)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-339">Überlauf des Benutzer-/kernelmarshalling-Puffers.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-339">The user/kernel marshalling buffer has overflowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-340"><span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**Fehler \_ ungültige \_ Variante**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-340"><span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**ERROR\_INVALID\_VARIANT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-341">604 (0x25c)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-341">604 (0x25C)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-342">Die bereitgestellte VARIANT-Struktur enthält ungültige Daten.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-342">The supplied variant structure contains invalid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-343"><span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**Fehler \_ beim \_ Komprimierungs \_ Puffer.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-343"><span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**ERROR\_BAD\_COMPRESSION\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-344">605 (0x25d)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-344">605 (0x25D)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-345">Der angegebene Puffer enthält falsch formatierte Daten.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-345">The specified buffer contains ill-formed data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-346"><span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**Fehler bei der Überwachung. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-346"><span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**ERROR\_AUDIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-347">606 (0x25e)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-347">606 (0x25E)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-348">{Audit failed} Fehler beim Versuch, eine Sicherheitsüberwachung zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-348">{Audit Failed} An attempt to generate a security audit failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-349"><span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**Fehler- \_ Timer- \_ Auflösung \_ nicht \_ festgelegt**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-349"><span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**ERROR\_TIMER\_RESOLUTION\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-350">607 (0x25f)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-350">607 (0x25F)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-351">Die Zeit Geber Auflösung wurde zuvor nicht durch den aktuellen Prozess festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-351">The timer resolution was not previously set by the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-352"><span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**Fehler aufgrund \_ unzureichender \_ Anmelde \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-352"><span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**ERROR\_INSUFFICIENT\_LOGON\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-353">608 (0x260)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-353">608 (0x260)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-354">Es sind nicht genügend Kontoinformationen zum Anmelden vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-354">There is insufficient account information to log you on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-355"><span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**Fehler \_ beim \_ dll- \_ Einstiegspunkt.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-355"><span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**ERROR\_BAD\_DLL\_ENTRYPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-356">609 (0x261)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-356">609 (0x261)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-357">{Ungültige DLL-Einstiegspunkt} Die Dynamic Link Library% HS wurde nicht ordnungsgemäß geschrieben.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-357">{Invalid DLL Entrypoint} The dynamic link library %hs is not written correctly.</span></span> <span data-ttu-id="d9ca0-358">Der Stapelzeiger wurde in einem inkonsistenten Zustand belassen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-358">The stack pointer has been left in an inconsistent state.</span></span> <span data-ttu-id="d9ca0-359">Der EntryPoint sollte als WINAPI oder stdcalldeklariert werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-359">The entrypoint should be declared as WINAPI or STDCALL.</span></span> <span data-ttu-id="d9ca0-360">Wählen Sie ja aus, um die dll-Auslastung zu deaktivieren</span><span class="sxs-lookup"><span data-stu-id="d9ca0-360">Select YES to fail the DLL load.</span></span> <span data-ttu-id="d9ca0-361">Wählen Sie Nein, um die Ausführung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-361">Select NO to continue execution.</span></span> <span data-ttu-id="d9ca0-362">Wenn Sie Nein auswählen, funktioniert die Anwendung möglicherweise nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-362">Selecting NO may cause the application to operate incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-363"><span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**fehlerhafter \_ \_ Dienst \_ Einstiegspunkt**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-363"><span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**ERROR\_BAD\_SERVICE\_ENTRYPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-364">610 (0x262)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-364">610 (0x262)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-365">{Ungültiger Dienst Rückruf Einstiegspunkt} Der Dienst "% hs" wurde nicht ordnungsgemäß geschrieben.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-365">{Invalid Service Callback Entrypoint} The %hs service is not written correctly.</span></span> <span data-ttu-id="d9ca0-366">Der Stapelzeiger wurde in einem inkonsistenten Zustand belassen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-366">The stack pointer has been left in an inconsistent state.</span></span> <span data-ttu-id="d9ca0-367">Der Callback-EntryPoint sollte als WINAPI oder stdcalldeklariert werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-367">The callback entrypoint should be declared as WINAPI or STDCALL.</span></span> <span data-ttu-id="d9ca0-368">Wenn Sie OK auswählen, wird der Dienst fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-368">Selecting OK will cause the service to continue operation.</span></span> <span data-ttu-id="d9ca0-369">Der Dienst Prozess funktioniert jedoch möglicherweise nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-369">However, the service process may operate incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-370"><span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**Fehler \_ -IP- \_ Adresse \_ CONFLICT1**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-370"><span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**ERROR\_IP\_ADDRESS\_CONFLICT1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-371">611 (0x263)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-371">611 (0x263)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-372">Es gibt einen IP-Adress Konflikt mit einem anderen System im Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-372">There is an IP address conflict with another system on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-373"><span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**Fehler \_ -IP- \_ Adresse \_ CONFLICT2**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-373"><span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**ERROR\_IP\_ADDRESS\_CONFLICT2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-374">612 (0x264)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-374">612 (0x264)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-375">Es gibt einen IP-Adress Konflikt mit einem anderen System im Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-375">There is an IP address conflict with another system on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-376"><span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**\_ \_ Kontingent \_ Limit für Fehler Registrierung**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-376"><span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**ERROR\_REGISTRY\_QUOTA\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-377">613 (0x265)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-377">613 (0x265)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-378">{Wenig Registrierungsbereich} Das System hat die maximal zulässige Größe für den System Teil der Registrierung erreicht.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-378">{Low On Registry Space} The system has reached the maximum size allowed for the system part of the registry.</span></span> <span data-ttu-id="d9ca0-379">Zusätzliche Speicheranforderungen werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-379">Additional storage requests will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-380"><span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**Fehler " \_ kein \_ Rückruf \_ aktiv"**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-380"><span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**ERROR\_NO\_CALLBACK\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-381">614 (0x266)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-381">614 (0x266)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-382">Ein Rückruf Rückgabesystem Dienst kann nicht ausgeführt werden, wenn kein Rückruf aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-382">A callback return system service cannot be executed when no callback is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-383"><span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**Fehler \_ pwd \_ zu \_ kurz**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-383"><span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**ERROR\_PWD\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-384">615 (0x267)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-384">615 (0x267)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-385">Das angegebene Kennwort ist zu kurz, um die Richtlinie Ihres Benutzerkontos zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-385">The password provided is too short to meet the policy of your user account.</span></span> <span data-ttu-id="d9ca0-386">Wählen Sie ein längeres Kennwort aus.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-386">Please choose a longer password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-387"><span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**Fehler \_ pwd \_ zu \_ aktuell**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-387"><span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**ERROR\_PWD\_TOO\_RECENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-388">616 (0x268)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-388">616 (0x268)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-389">Die Richtlinie Ihres Benutzerkontos ermöglicht nicht das Ändern von Kenn Wörtern zu häufig.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-389">The policy of your user account does not allow you to change passwords too frequently.</span></span> <span data-ttu-id="d9ca0-390">Dies geschieht, um zu verhindern, dass Benutzer zu einem vertrauten, aber potenziell ermittelten Kennwort zurück wechseln.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-390">This is done to prevent users from changing back to a familiar, but potentially discovered, password.</span></span> <span data-ttu-id="d9ca0-391">Wenn Ihr Kennwort kompromittiert wurde, wenden Sie sich umgehend an Ihren Administrator, um ein neues Kennwort zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-391">If you feel your password has been compromised then please contact your administrator immediately to have a new one assigned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-392"><span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**Fehler \_ pwd-Verlaufs \_ \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-392"><span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**ERROR\_PWD\_HISTORY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-393">617 (0x269)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-393">617 (0x269)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-394">Sie haben versucht, Ihr Kennwort in ein solches Kennwort zu ändern, das Sie in der Vergangenheit verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-394">You have attempted to change your password to one that you have used in the past.</span></span> <span data-ttu-id="d9ca0-395">Die Richtlinie Ihres Benutzerkontos lässt dies nicht zu.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-395">The policy of your user account does not allow this.</span></span> <span data-ttu-id="d9ca0-396">Wählen Sie ein Kennwort aus, das Sie zuvor nicht verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-396">Please select a password that you have not previously used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-397"><span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**\_nicht unterstützte \_ Komprimierung.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-397"><span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**ERROR\_UNSUPPORTED\_COMPRESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-398">618 (0x26a)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-398">618 (0x26A)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-399">Das angegebene Komprimierungs Format wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-399">The specified compression format is unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-400"><span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**Fehler \_ ungültiges \_ HW- \_ Profil**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-400"><span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**ERROR\_INVALID\_HW\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-401">619 (0x26b)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-401">619 (0x26B)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-402">Die angegebene Hardwareprofil Konfiguration ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-402">The specified hardware profile configuration is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-403"><span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**Fehler \_ ungültiger \_ plugplay- \_ Geräte \_ Pfad**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-403"><span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**ERROR\_INVALID\_PLUGPLAY\_DEVICE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-404">620 (0x26c)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-404">620 (0x26C)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-405">Der angegebene Plug & Play Registrierungs Gerätepfad ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-405">The specified Plug and Play registry device path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-406"><span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**Fehler \_ Kontingent \_ Liste \_ inkonsistent**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-406"><span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**ERROR\_QUOTA\_LIST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-407">621 (0x26d)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-407">621 (0x26D)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-408">Die angegebene Kontingent Liste ist intern inkonsistent mit dem Deskriptor.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-408">The specified quota list is internally inconsistent with its descriptor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-409"><span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**Ablauf der Fehler \_ Auswertung \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-409"><span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**ERROR\_EVALUATION\_EXPIRATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-410">622 (0x26e)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-410">622 (0x26E)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-411">{Windows-Evaluierungs Benachrichtigung} Der Evaluierungszeitraum für diese Installation von Windows ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-411">{Windows Evaluation Notification} The evaluation period for this installation of Windows has expired.</span></span> <span data-ttu-id="d9ca0-412">Dieses System wird innerhalb einer Stunde heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-412">This system will shutdown in 1 hour.</span></span> <span data-ttu-id="d9ca0-413">Um den Zugriff auf diese Installation von Windows wiederherzustellen, aktualisieren Sie diese Installation mithilfe einer lizenzierten Distribution dieses Produkts.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-413">To restore access to this installation of Windows, please upgrade this installation using a licensed distribution of this product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-414"><span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**Fehler bei ungültiger \_ \_ dll- \_ Verlagerung**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-414"><span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**ERROR\_ILLEGAL\_DLL\_RELOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-415">623 (0x26f)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-415">623 (0x26F)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-416">{Illegale System-DLL-Verschiebung} Die System-dll "% hs" wurde im Arbeitsspeicher verschoben.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-416">{Illegal System DLL Relocation} The system DLL %hs was relocated in memory.</span></span> <span data-ttu-id="d9ca0-417">Die Anwendung wird nicht ordnungsgemäß ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-417">The application will not run properly.</span></span> <span data-ttu-id="d9ca0-418">Die Verschiebung ist aufgetreten, da die dll "% hs" einen für Windows-System-DLLs reservierten Adressbereich belegt hat.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-418">The relocation occurred because the DLL %hs occupied an address range reserved for Windows system DLLs.</span></span> <span data-ttu-id="d9ca0-419">Der Hersteller, der die dll bereitstellt, sollte für eine neue dll kontaktiert werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-419">The vendor supplying the DLL should be contacted for a new DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-420"><span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**Fehler-dll-Fehler beim Abmelden \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-420"><span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**ERROR\_DLL\_INIT\_FAILED\_LOGOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-421">624 (0x270)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-421">624 (0x270)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-422">{DLL-Initialisierung ist fehlgeschlagen. Die Anwendung konnte nicht initialisiert werden, da die Fenster Station heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-422">{DLL Initialization Failed} The application failed to initialize because the window station is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-423"><span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**Fehler \_ beim \_ fortfahren**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-423"><span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**ERROR\_VALIDATE\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-424">625 (0x271)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-424">625 (0x271)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-425">Der Überprüfungs Vorgang muss mit dem nächsten Schritt fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-425">The validation process needs to continue on to the next step.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-426"><span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**Fehler \_ keine \_ weiteren \_ Übereinstimmungen**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-426"><span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**ERROR\_NO\_MORE\_MATCHES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-427">626 (0x272)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-427">626 (0x272)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-428">Es sind keine weiteren Übereinstimmungen für die aktuelle indexenumeration vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-428">There are no more matches for the current index enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-429"><span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**Fehler \_ Bereich- \_ Listen \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-429"><span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**ERROR\_RANGE\_LIST\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-430">627 (0x273)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-430">627 (0x273)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-431">Der Bereich konnte aufgrund eines Konflikts nicht zur Bereichs Liste hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-431">The range could not be added to the range list because of a conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-432"><span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**Fehler \_ Server- \_ sid \_ stimmt nicht überein.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-432"><span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**ERROR\_SERVER\_SID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-433">628 (0x274)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-433">628 (0x274)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-434">Der Server Prozess wird unter einer anderen sid ausgeführt als die für den Client erforderliche sid.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-434">The server process is running under a SID different than that required by client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-435"><span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**Fehler \_ " \_ \_ nur verweigern" aktivieren \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-435"><span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**ERROR\_CANT\_ENABLE\_DENY\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-436">629 (0x275)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-436">629 (0x275)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-437">Eine Gruppe, die nur für Deny gekennzeichnet ist, kann nicht aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-437">A group marked use for deny only cannot be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-438"><span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**Fehler beim \_ float von \_ mehreren \_ Fehlern**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-438"><span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**ERROR\_FLOAT\_MULTIPLE\_FAULTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-439">630 (0x276)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-439">630 (0x276)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-440">Distanzieren Mehrere Gleit Komma Fehler.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-440">{EXCEPTION} Multiple floating point faults.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-441"><span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**Fehler beim \_ float \_ mehrerer \_ Traps**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-441"><span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ERROR\_FLOAT\_MULTIPLE\_TRAPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-442">631 (0x277)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-442">631 (0x277)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-443">Distanzieren Mehrere Gleit Komma Traps.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-443">{EXCEPTION} Multiple floating point traps.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-444"><span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**Fehler- \_ nointerface**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-444"><span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**ERROR\_NOINTERFACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-445">632 (0x278)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-445">632 (0x278)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-446">Die angeforderte Schnittstelle wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-446">The requested interface is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-447"><span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**Fehler Treiber Fehler beim Standbymodus \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-447"><span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**ERROR\_DRIVER\_FAILED\_SLEEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-448">633 (0x279)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-448">633 (0x279)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-449">{System Standby-Fehler Der% HS-Treiber unterstützt den Standbymodus nicht.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-449">{System Standby Failed} The driver %hs does not support standby mode.</span></span> <span data-ttu-id="d9ca0-450">Durch Aktualisieren dieses Treibers kann das System in den Standbymodus wechseln.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-450">Updating this driver may allow the system to go to standby mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-451"><span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**Fehler beim \_ beschädigen der \_ System \_ Datei.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-451"><span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**ERROR\_CORRUPT\_SYSTEM\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-452">634 (0x27a)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-452">634 (0x27A)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-453">Die Systemdatei "%1" ist beschädigt und wurde ersetzt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-453">The system file %1 has become corrupt and has been replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-454"><span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**\_mindestens fehlerverpflichtung \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-454"><span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**ERROR\_COMMITMENT\_MINIMUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-455">635 (0x27b)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-455">635 (0x27B)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-456">{Minimaler virtueller Arbeitsspeicher zu niedrig} Das System verfügt über wenig virtuellen Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-456">{Virtual Memory Minimum Too Low} Your system is low on virtual memory.</span></span> <span data-ttu-id="d9ca0-457">Die Größe der Auslagerungs Datei des virtuellen Speichers wird von Windows vergrößert.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-457">Windows is increasing the size of your virtual memory paging file.</span></span> <span data-ttu-id="d9ca0-458">Während dieses Vorgangs werden Arbeitsspeicher Anforderungen für einige Anwendungen möglicherweise verweigert.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-458">During this process, memory requests for some applications may be denied.</span></span> <span data-ttu-id="d9ca0-459">Weitere Informationen finden Sie in der Hilfe.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-459">For more information, see Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-460"><span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**Fehler \_ pnp- \_ Neustart- \_ Enumeration**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-460"><span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**ERROR\_PNP\_RESTART\_ENUMERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-461">636 (0x27c)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-461">636 (0x27C)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-462">Ein Gerät wurde entfernt, sodass die Enumeration neu gestartet werden muss.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-462">A device was removed so enumeration must be restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-463"><span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**Fehler bei der Signatur des \_ System \_ Images. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-463"><span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**ERROR\_SYSTEM\_IMAGE\_BAD\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-464">637 (0x27d)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-464">637 (0x27D)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-465">{Schwerwiegender System Fehler} Das System Image "% s" ist nicht ordnungsgemäß signiert.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-465">{Fatal System Error} The system image %s is not properly signed.</span></span> <span data-ttu-id="d9ca0-466">Die Datei wurde durch die signierte Datei ersetzt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-466">The file has been replaced with the signed file.</span></span> <span data-ttu-id="d9ca0-467">Das System wurde heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-467">The system has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-468"><span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**Fehler \_ pnp- \_ Neustart \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-468"><span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**ERROR\_PNP\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-469">638 (0x27e)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-469">638 (0x27E)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-470">Das Gerät wird ohne Neustart nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-470">Device will not start without a reboot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-471"><span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**Fehler bei \_ unzureichender \_ Stromversorgung**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-471"><span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**ERROR\_INSUFFICIENT\_POWER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-472">639 (0x27f)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-472">639 (0x27F)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-473">Es ist nicht genügend Strom vorhanden, um den angeforderten Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-473">There is not enough power to complete the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-474"><span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**Fehler bei \_ mehrerer Fehler \_ \_ Verletzung**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-474"><span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**ERROR\_MULTIPLE\_FAULT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-475">640 (0x280)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-475">640 (0x280)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-476">Fehler bei \_ mehrerer Fehler \_ \_ Verletzung</span><span class="sxs-lookup"><span data-stu-id="d9ca0-476">ERROR\_MULTIPLE\_FAULT\_VIOLATION</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-477"><span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**Fehler \_ System \_ Herunterfahren**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-477"><span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**ERROR\_SYSTEM\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-478">641 (0x281)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-478">641 (0x281)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-479">Das System wird gerade heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-479">The system is in the process of shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-480"><span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**\_fehlerport \_ nicht \_ festgelegt**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-480"><span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**ERROR\_PORT\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-481">642 (0x282)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-481">642 (0x282)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-482">Es wurde versucht, einen Debugport für Prozesse zu entfernen, aber es wurde noch kein Port mit dem Prozess verknüpft.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-482">An attempt to remove a processes DebugPort was made, but a port was not already associated with the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-483"><span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**Fehler bei der \_ \_ Versions \_ Überprüfung \_ des Fehlers.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-483"><span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**ERROR\_DS\_VERSION\_CHECK\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-484">643 (0x283)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-484">643 (0x283)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-485">Diese Windows-Version ist nicht kompatibel mit der Verhaltens Version der Verzeichnis Gesamtstruktur, der Domäne oder des Domänen Controllers.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-485">This version of Windows is not compatible with the behavior version of directory forest, domain or domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-486"><span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**der Fehler \_ Bereich wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-486"><span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**ERROR\_RANGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-487">644 (0x284)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-487">644 (0x284)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-488">Der angegebene Bereich wurde nicht in der Bereichs Liste gefunden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-488">The specified range could not be found in the range list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-489"><span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**Fehler \_ " \_ Treiber nicht sicher \_ Modus \_ "**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-489"><span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**ERROR\_NOT\_SAFE\_MODE\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-490">646 (0x286)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-490">646 (0x286)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-491">Der Treiber wurde nicht geladen, da das System im abgesicherten Modus gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-491">The driver was not loaded because the system is booting into safe mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-492"><span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**Fehler \_ beim \_ Treiber \_ Eintrag.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-492"><span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**ERROR\_FAILED\_DRIVER\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-493">647 (0x287)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-493">647 (0x287)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-494">Der Treiber wurde nicht geladen, da der Initialisierungs Befehl nicht ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-494">The driver was not loaded because it failed its initialization call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-495"><span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**Fehler bei \_ Geräte \_ Enumeration. \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-495"><span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**ERROR\_DEVICE\_ENUMERATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-496">648 (0x288)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-496">648 (0x288)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-497">"% Hs" hat einen Fehler beim Anwenden von Energie oder Lesen der Gerätekonfiguration ermittelt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-497">The "%hs" encountered an error while applying power or reading the device configuration.</span></span> <span data-ttu-id="d9ca0-498">Dies kann durch einen Ausfall der Hardware oder durch eine schlechte Verbindung verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-498">This may be caused by a failure of your hardware or by a poor connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-499"><span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**Fehler \_ \_ Einfügepunkt \_ nicht \_ aufgelöst**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-499"><span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**ERROR\_MOUNT\_POINT\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-500">649 (0x289)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-500">649 (0x289)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-501">Fehler beim Erstellungs Vorgang, da der Name mindestens einen Einfügepunkt enthielt, der zu einem Volume aufgelöst wird, an das das angegebene Geräte Objekt nicht angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-501">The create operation failed because the name contained at least one mount point which resolves to a volume to which the specified device object is not attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-502"><span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**Fehler bei \_ ungültigem \_ Geräte \_ Objekt \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-502"><span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**ERROR\_INVALID\_DEVICE\_OBJECT\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-503">650 (0x28a)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-503">650 (0x28A)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-504">Der Geräte Objekt Parameter ist entweder kein gültiges Geräte Objekt oder ist nicht an das durch den Dateinamen angegebene Volume angefügt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-504">The device object parameter is either not a valid device object or is not attached to the volume specified by the file name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-505"><span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**Fehler- \_ MCA \_ aufgetreten**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-505"><span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**ERROR\_MCA\_OCCURED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-506">651 (0x28b)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-506">651 (0x28B)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-507">Fehler bei der Computer Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-507">A Machine Check Error has occurred.</span></span> <span data-ttu-id="d9ca0-508">Überprüfen Sie das System Ereignisprotokoll, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-508">Please check the system eventlog for additional information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-509"><span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**Fehler \_ Treiber- \_ Daten Bank \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-509"><span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**ERROR\_DRIVER\_DATABASE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-510">652 (0x28c)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-510">652 (0x28C)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-511">Fehler \[ %2 \] beim Verarbeiten der Treiberdatenbank.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-511">There was error \[%2\] processing the driver database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-512"><span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**Fehler \_ System \_ Hive \_ zu \_ groß**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-512"><span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**ERROR\_SYSTEM\_HIVE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-513">653 (0x28d)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-513">653 (0x28D)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-514">Die Größe des System Hive hat das Limit überschritten.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-514">System hive size has exceeded its limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-515"><span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**Fehler \_ Treiber \_ Fehler \_ vor dem \_ entladen.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-515"><span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**ERROR\_DRIVER\_FAILED\_PRIOR\_UNLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-516">654 (0x28e)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-516">654 (0x28E)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-517">Der Treiber konnte nicht geladen werden, da sich eine frühere Version des Treibers noch im Speicher befindet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-517">The driver could not be loaded because a previous version of the driver is still in memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-518"><span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**Fehler beim Vorbereiten des Ruhe Zustands für " \_ Volsnap". \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-518"><span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**ERROR\_VOLSNAP\_PREPARE\_HIBERNATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-519">655 (0x28f)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-519">655 (0x28F)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-520">{Volumeschattenkopie-Dienst} Warten Sie, während das Volumeschattenkopie-Dienst Volume% HS für den Ruhezustand vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-520">{Volume Shadow Copy Service} Please wait while the Volume Shadow Copy Service prepares volume %hs for hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-521"><span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**Fehler im Ruhezustand \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-521"><span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**ERROR\_HIBERNATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-522">656 (0x290)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-522">656 (0x290)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-523">Das System konnte nicht in den Ruhezustand versetzt werden (der Fehlercode lautet% HS).</span><span class="sxs-lookup"><span data-stu-id="d9ca0-523">The system has failed to hibernate (The error code is %hs).</span></span> <span data-ttu-id="d9ca0-524">Der Ruhezustand wird deaktiviert, bis das System neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-524">Hibernation will be disabled until the system is restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-525"><span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**Fehler \_ pwd \_ zu \_ lang**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-525"><span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**ERROR\_PWD\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-526">657 (0x291)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-526">657 (0x291)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-527">Das angegebene Kennwort ist zu lang, um die Richtlinie Ihres Benutzerkontos zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-527">The password provided is too long to meet the policy of your user account.</span></span> <span data-ttu-id="d9ca0-528">Wählen Sie ein kürzeres Kennwort aus.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-528">Please choose a shorter password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-529"><span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**\_ \_ System \_ Einschränkung für Fehler Datei**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-529"><span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**ERROR\_FILE\_SYSTEM\_LIMITATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-530">665 (0x299)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-530">665 (0x299)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-531">Der angeforderte Vorgang konnte aufgrund einer Dateisystemeinschränkung nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-531">The requested operation could not be completed due to a file system limitation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-532"><span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**Fehler bei der Fehler \_ Behauptung \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-532"><span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**ERROR\_ASSERTION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-533">668 (0x29c)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-533">668 (0x29C)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-534">Ein Fehler bei der Übersetzung ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-534">An assertion failure has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-535"><span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**Fehler- \_ ACPI- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-535"><span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**ERROR\_ACPI\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-536">669 (0x29d)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-536">669 (0x29D)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-537">Im ACPI-Subsystem ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-537">An error occurred in the ACPI subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-538"><span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**Fehler WOW-Assertion \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-538"><span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**ERROR\_WOW\_ASSERTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-539">670 (0x29e)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-539">670 (0x29E)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-540">WOW-Assertionsfehler.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-540">WOW Assertion Error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-541"><span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**Fehler PNP-Tabelle für ungültige \_ \_ \_ MPS \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-541"><span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**ERROR\_PNP\_BAD\_MPS\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-542">671 (0x29f)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-542">671 (0x29F)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-543">In der MPS-Tabelle des System-BIOS fehlt ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-543">A device is missing in the system BIOS MPS table.</span></span> <span data-ttu-id="d9ca0-544">Dieses Gerät wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-544">This device will not be used.</span></span> <span data-ttu-id="d9ca0-545">Wenden Sie sich für das System-BIOS-Update an Ihren Systemanbieter.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-545">Please contact your system vendor for system BIOS update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-546"><span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**Fehler bei \_ pnp- \_ Übersetzung \_ .**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-546"><span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**ERROR\_PNP\_TRANSLATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-547">672 (0x2a0)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-547">672 (0x2A0)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-548">Ein Konvertierer konnte Ressourcen nicht übersetzen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-548">A translator failed to translate resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-549"><span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**Fehler bei PNP-Fehler bei der \_ \_ \_ Übersetzung. \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-549"><span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**ERROR\_PNP\_IRQ\_TRANSLATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-550">673 (0x2a1)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-550">673 (0x2A1)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-551">Ein iriq-Konvertierer konnte Ressourcen nicht übersetzen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-551">A IRQ translator failed to translate resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-552"><span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**Fehler \_ pnp \_ - \_ ID ist ungültig.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-552"><span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**ERROR\_PNP\_INVALID\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-553">674 (0x2a2)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-553">674 (0x2A2)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-554">Treiber "%2" hat eine ungültige ID für ein untergeordnetes Gerät (%3) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-554">Driver %2 returned invalid ID for a child device (%3).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-555"><span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**Fehler Reaktivierungs \_ \_ System \_ Debugger**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-555"><span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**ERROR\_WAKE\_SYSTEM\_DEBUGGER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-556">675 (0x2a3)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-556">675 (0x2A3)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-557">{Kernel Debugger erwacht}. der System Debugger wurde durch einen Interrupt aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-557">{Kernel Debugger Awakened} the system debugger was awakened by an interrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-558"><span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**Fehler \_ Handles \_ geschlossen**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-558"><span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**ERROR\_HANDLES\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-559">676 (0x2a4)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-559">676 (0x2A4)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-560">{Handles geschlossen} Handles zu Objekten wurden aufgrund des angeforderten Vorgangs automatisch geschlossen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-560">{Handles Closed} Handles to objects have been automatically closed as a result of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-561"><span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**Fehler über \_ flüssige \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-561"><span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**ERROR\_EXTRANEOUS\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-562">677 (0x2a5)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-562">677 (0x2A5)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-563">{Zu viele Informationen} Die angegebene Zugriffs Steuerungs Liste (Access Control List, ACL) enthielt mehr Informationen als erwartet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-563">{Too Much Information} The specified access control list (ACL) contained more information than was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-564"><span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**Fehler- \_ rxact- \_ Commit \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-564"><span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**ERROR\_RXACT\_COMMIT\_NECESSARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-565">678 (0x2a6)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-565">678 (0x2A6)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-566">Dieser warnebenenstatus gibt an, dass der Transaktionsstatus bereits für die Registrierungs Unterstruktur vorhanden ist, dass jedoch bereits ein Transaktionscommit abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-566">This warning level status indicates that the transaction state already exists for the registry sub-tree, but that a transaction commit was previously aborted.</span></span> <span data-ttu-id="d9ca0-567">Der Commit wurde nicht abgeschlossen, aber es wurde kein Rollback ausgeführt (es kann sein, dass ggf. ein Commit ausgeführt wird).</span><span class="sxs-lookup"><span data-stu-id="d9ca0-567">The commit has NOT been completed, but has not been rolled back either (so it may still be committed if desired).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-568"><span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**Fehler \_ Medien \_ Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-568"><span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**ERROR\_MEDIA\_CHECK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-569">679 (0x2a7)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-569">679 (0x2A7)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-570">{Media Changed} Die Medien haben sich möglicherweise geändert.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-570">{Media Changed} The media may have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-571"><span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**Fehler- \_ GUID- \_ Ersetzung \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-571"><span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**ERROR\_GUID\_SUBSTITUTION\_MADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-572">680 (0x2a8)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-572">680 (0x2A8)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-573">{GUID-Ersetzung} Während der Übersetzung eines globalen Bezeichners (GUID) in eine Windows-Sicherheits-ID (SID) wurde kein administrativ definiertes GUID-Präfix gefunden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-573">{GUID Substitution} During the translation of a global identifier (GUID) to a Windows security ID (SID), no administratively-defined GUID prefix was found.</span></span> <span data-ttu-id="d9ca0-574">Ein Ersatz Präfix wurde verwendet, wodurch die Systemsicherheit nicht beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-574">A substitute prefix was used, which will not compromise system security.</span></span> <span data-ttu-id="d9ca0-575">Dies bietet jedoch möglicherweise einen restriktiveren Zugriff als beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-575">However, this may provide a more restrictive access than intended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-576"><span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**Fehler \_ \_ bei \_ symlink.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-576"><span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**ERROR\_STOPPED\_ON\_SYMLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-577">681 (0x2a9)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-577">681 (0x2A9)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-578">Der Erstellungs Vorgang wurde beendet, nachdem eine symbolische Verknüpfung erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-578">The create operation stopped after reaching a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-579"><span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**Fehler beim \_ longjump**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-579"><span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**ERROR\_LONGJUMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-580">682 (0x2aa)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-580">682 (0x2AA)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-581">Ein langer Sprung wurde ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-581">A long jump has been executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-582"><span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**Fehler beim \_ plugplay der \_ Abfrage. \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-582"><span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**ERROR\_PLUGPLAY\_QUERY\_VETOED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-583">683 (0x2ab)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-583">683 (0x2AB)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-584">Der Plug & Play Abfrage Vorgang war nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-584">The Plug and Play query operation was not successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-585"><span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**Fehler \_ entladen \_ konsolidieren**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-585"><span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**ERROR\_UNWIND\_CONSOLIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-586">684 (0x2ac)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-586">684 (0x2AC)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-587">Eine Frame Konsolidierung wurde ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-587">A frame consolidation has been executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-588"><span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**Fehler \_ Registrierungs \_ Struktur \_ wieder hergestellt**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-588"><span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**ERROR\_REGISTRY\_HIVE\_RECOVERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-589">685 (0x2ad)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-589">685 (0x2AD)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-590">{Registrierungs Struktur wieder hergestellt} Registrierungs Struktur (Datei):% HS war beschädigt und wurde wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-590">{Registry Hive Recovered} Registry hive (file): %hs was corrupted and it has been recovered.</span></span> <span data-ttu-id="d9ca0-591">Einige Daten sind möglicherweise verloren gegangen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-591">Some data might have been lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-592"><span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**Fehler- \_ dll ist \_ möglicherweise \_ \_ unsicher**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-592"><span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**ERROR\_DLL\_MIGHT\_BE\_INSECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-593">686 (0x2ae)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-593">686 (0x2AE)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-594">Die Anwendung versucht, ausführbaren Code aus dem Modul% HS auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-594">The application is attempting to run executable code from the module %hs.</span></span> <span data-ttu-id="d9ca0-595">Dies kann unsicher sein.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-595">This may be insecure.</span></span> <span data-ttu-id="d9ca0-596">Eine Alternative,% HS, ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-596">An alternative, %hs, is available.</span></span> <span data-ttu-id="d9ca0-597">Sollte die Anwendung das sichere Modul% HS verwenden?</span><span class="sxs-lookup"><span data-stu-id="d9ca0-597">Should the application use the secure module %hs?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-598"><span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**Fehler- \_ dll ist \_ möglicherweise nicht \_ \_ kompatibel**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-598"><span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**ERROR\_DLL\_MIGHT\_BE\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-599">687 (0x2af)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-599">687 (0x2AF)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-600">Die Anwendung lädt ausführbaren Code aus dem Modul% HS.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-600">The application is loading executable code from the module %hs.</span></span> <span data-ttu-id="d9ca0-601">Dies ist sicher, kann jedoch mit früheren Versionen des Betriebssystems nicht kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-601">This is secure, but may be incompatible with previous releases of the operating system.</span></span> <span data-ttu-id="d9ca0-602">Eine Alternative,% HS, ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-602">An alternative, %hs, is available.</span></span> <span data-ttu-id="d9ca0-603">Sollte die Anwendung das sichere Modul% HS verwenden?</span><span class="sxs-lookup"><span data-stu-id="d9ca0-603">Should the application use the secure module %hs?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-604"><span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**Fehler bei \_ dbg- \_ Ausnahme \_ nicht \_ behandelt.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-604"><span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**ERROR\_DBG\_EXCEPTION\_NOT\_HANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-605">688 (0x2b0)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-605">688 (0x2B0)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-606">Der Debugger hat die Ausnahme nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-606">Debugger did not handle the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-607"><span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**Fehler \_ dbg- \_ Antwort \_ später**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-607"><span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**ERROR\_DBG\_REPLY\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-608">689 (0x2b1)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-608">689 (0x2B1)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-609">Der Debugger antwortet später.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-609">Debugger will reply later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-610"><span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**Fehler \_ dbg \_ kann \_ \_ Handle nicht bereitstellen \_ .**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-610"><span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**ERROR\_DBG\_UNABLE\_TO\_PROVIDE\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-611">690 (0x2b2)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-611">690 (0x2B2)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-612">Der Debugger kann kein Handle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-612">Debugger cannot provide handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-613"><span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**Fehler \_ dbg \_ - \_ Thread beenden**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-613"><span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**ERROR\_DBG\_TERMINATE\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-614">691 (0x2b3)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-614">691 (0x2B3)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-615">Der Debugger hat den Thread beendet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-615">Debugger terminated thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-616"><span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**Fehler \_ dbg-Beendigungs \_ \_ Prozess**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-616"><span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**ERROR\_DBG\_TERMINATE\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-617">692 (0x2b4)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-617">692 (0x2B4)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-618">Der Debugger hat den Prozess beendet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-618">Debugger terminated process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-619"><span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**Fehler- \_ dbg- \_ Steuerelement \_ C**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-619"><span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**ERROR\_DBG\_CONTROL\_C**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-620">693 (0x2b5)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-620">693 (0x2B5)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-621">Der Debugger hat die Steuerung C erhalten.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-621">Debugger got control C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-622"><span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**Fehler \_ dbg \_ PrintException \_ C**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-622"><span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**ERROR\_DBG\_PRINTEXCEPTION\_C**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-623">694 (0x2b6)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-623">694 (0x2B6)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-624">Der Debugger hat eine Ausnahme für das Steuerelement C ausgegeben</span><span class="sxs-lookup"><span data-stu-id="d9ca0-624">Debugger printed exception on control C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-625"><span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**Fehler \_ dbg- \_ ripexception**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-625"><span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**ERROR\_DBG\_RIPEXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-626">695 (0x2b7)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-626">695 (0x2B7)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-627">Der Debugger hat eine RIP-Ausnahme empfangen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-627">Debugger received RIP exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-628"><span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**Fehler beim \_ dbg- \_ Steuerungs \_ Umbruch.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-628"><span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**ERROR\_DBG\_CONTROL\_BREAK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-629">696 (0x2b8)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-629">696 (0x2B8)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-630">Der Debugger hat die Steuerungs Pause empfangen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-630">Debugger received control break.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-631"><span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**Fehler \_ dbg- \_ Befehls \_ Ausnahme**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-631"><span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**ERROR\_DBG\_COMMAND\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-632">697 (0x2b9)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-632">697 (0x2B9)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-633">Ausnahme bei der Kommunikation mit dem Debugger.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-633">Debugger command communication exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-634"><span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**der Fehler \_ Objekt \_ Name ist \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-634"><span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**ERROR\_OBJECT\_NAME\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-635">698 (0x2ba)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-635">698 (0x2BA)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-636">{Object ist vorhanden} Es wurde versucht, ein Objekt zu erstellen, und der Objektname war bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-636">{Object Exists} An attempt was made to create an object and the object name already existed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-637"><span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**der Fehler \_ Thread \_ wurde angeh \_ alten.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-637"><span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**ERROR\_THREAD\_WAS\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-638">699 (0x2bb)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-638">699 (0x2BB)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-639">{Thread angehalten} Eine Thread Beendigung ist aufgetreten, während der Thread angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-639">{Thread Suspended} A thread termination occurred while the thread was suspended.</span></span> <span data-ttu-id="d9ca0-640">Der Thread wurde fortgesetzt, und die Beendigung wurde fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-640">The thread was resumed, and termination proceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-641"><span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**Fehler \_ Bild \_ nicht \_ auf \_ Basis**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-641"><span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**ERROR\_IMAGE\_NOT\_AT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-642">700 (0x2bc)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-642">700 (0x2BC)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-643">{Image verschoben} Eine Bilddatei konnte nicht an der in der Bilddatei angegebenen Adresse zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-643">{Image Relocated} An image file could not be mapped at the address specified in the image file.</span></span> <span data-ttu-id="d9ca0-644">Lokale Fixups müssen für dieses Image ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-644">Local fixups must be performed on this image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-645"><span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**Fehler \_ rxact- \_ Status \_ erstellt**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-645"><span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**ERROR\_RXACT\_STATE\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-646">701 (0x2bd)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-646">701 (0x2BD)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-647">Dieser Status der Informations Stufe gibt an, dass ein angegebener Transaktionsstatus der Registrierungs Teilstruktur noch nicht vorhanden war und erstellt werden musste.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-647">This informational level status indicates that a specified registry sub-tree transaction state did not yet exist and had to be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-648"><span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**Fehler \_ Segment \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-648"><span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**ERROR\_SEGMENT\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-649">702 (0x2be)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-649">702 (0x2BE)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-650">{Segment laden} Ein VDM (Virtual DOS Machine) lädt, entladen oder verschiebt ein MS-DOS-oder Win16-Programm Segment Image.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-650">{Segment Load} A virtual DOS machine (VDM) is loading, unloading, or moving an MS-DOS or Win16 program segment image.</span></span> <span data-ttu-id="d9ca0-651">Eine Ausnahme wird ausgelöst, sodass ein Debugger Symbole und Breakpoints innerhalb dieser 16-Bit-Segmente laden, entladen oder nachverfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-651">An exception is raised so a debugger can load, unload or track symbols and breakpoints within these 16-bit segments.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-652"><span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**Fehler \_ beim \_ aktuellen \_ Verzeichnis.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-652"><span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**ERROR\_BAD\_CURRENT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-653">703 (0x2bf)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-653">703 (0x2BF)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-654">{Ungültiges Aktuelles Verzeichnis} Der Prozess kann nicht zum aktuellen Start Verzeichnis% HS wechseln.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-654">{Invalid Current Directory} The process cannot switch to the startup current directory %hs.</span></span> <span data-ttu-id="d9ca0-655">Wählen Sie OK aus, um das aktuelle Verzeichnis auf% HS festzulegen, oder wählen Sie Abbrechen aus, um die</span><span class="sxs-lookup"><span data-stu-id="d9ca0-655">Select OK to set current directory to %hs, or select CANCEL to exit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-656"><span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**Fehler \_ \_ beim Lesen \_ der Wiederherstellung \_ aus der \_ Sicherung**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-656"><span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**ERROR\_FT\_READ\_RECOVERY\_FROM\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-657">704 (0x2c0)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-657">704 (0x2C0)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-658">{Redundant Read} Um eine Lese Anforderung zu erfüllen, liest das NT-fehlertolerante Dateisystem die angeforderten Daten erfolgreich aus einer redundanten Kopie.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-658">{Redundant Read} To satisfy a read request, the NT fault-tolerant file system successfully read the requested data from a redundant copy.</span></span> <span data-ttu-id="d9ca0-659">Der Grund hierfür ist, dass das Dateisystem auf einem Mitglied des fehlertoleranten Volumes fehlgeschlagen ist, den Fehlerbereich des Geräts jedoch nicht neu zuweisen konnte.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-659">This was done because the file system encountered a failure on a member of the fault-tolerant volume, but was unable to reassign the failing area of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-660"><span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**Fehler- \_ ft- \_ Schreib \_ Wiederherstellung**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-660"><span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**ERROR\_FT\_WRITE\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-661">705 (0x2c1)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-661">705 (0x2C1)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-662">{Redundanter Schreibvorgang} Zum erfüllen einer Schreib Anforderung hat das NT-fehlertolerante Dateisystem erfolgreich eine redundante Kopie der Informationen geschrieben.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-662">{Redundant Write} To satisfy a write request, the NT fault-tolerant file system successfully wrote a redundant copy of the information.</span></span> <span data-ttu-id="d9ca0-663">Dies wurde durchgeführt, weil das Dateisystem auf einem Mitglied des fehlertoleranten Volumes einen Fehler feststellt, den Fehlerbereich des Geräts jedoch nicht neu zuweisen konnte.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-663">This was done because the file system encountered a failure on a member of the fault-tolerant volume, but was not able to reassign the failing area of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-664"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**Fehler beim \_ Abbild des \_ Computer \_ Typs \_ .**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-664"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**ERROR\_IMAGE\_MACHINE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-665">706 (0x2c2)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-665">706 (0x2C2)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-666">{Nicht übereinstimmende Computertypen} Die Abbild Datei "% hs" ist gültig, aber für einen anderen Computertyp als den aktuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-666">{Machine Type Mismatch} The image file %hs is valid, but is for a machine type other than the current machine.</span></span> <span data-ttu-id="d9ca0-667">Wählen Sie OK aus, um den Vorgang fortzusetzen, oder Abbrechen, um die dll-Auslastung</span><span class="sxs-lookup"><span data-stu-id="d9ca0-667">Select OK to continue, or CANCEL to fail the DLL load.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-668"><span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**Fehler beim \_ Empfang \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-668"><span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**ERROR\_RECEIVE\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-669">707 (0x2c3)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-669">707 (0x2C3)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-670">{Partielle Daten empfangen} Der Netzwerk Transport hat partielle Daten an den Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-670">{Partial Data Received} The network transport returned partial data to its client.</span></span> <span data-ttu-id="d9ca0-671">Die verbleibenden Daten werden später gesendet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-671">The remaining data will be sent later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-672"><span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**Fehler beim \_ empfangen. \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-672"><span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**ERROR\_RECEIVE\_EXPEDITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-673">708 (0x2c4)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-673">708 (0x2C4)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-674">{Beschleunigte empfangene Daten} Der Netzwerk Transport hat Daten an den Client zurückgegeben, der vom Remote System als beschleunigt gekennzeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-674">{Expedited Data Received} The network transport returned data to its client that was marked as expedited by the remote system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-675"><span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**Fehler beim \_ Empfang \_ teilweise \_ beschleunigt**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-675"><span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**ERROR\_RECEIVE\_PARTIAL\_EXPEDITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-676">709 (0x2c5)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-676">709 (0x2C5)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-677">{Teilweise beschleunigte Daten empfangen} Der Netzwerk Transport hat partielle Daten an den Client zurückgegeben, und diese Daten wurden vom Remote System als beschleunigt gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-677">{Partial Expedited Data Received} The network transport returned partial data to its client and this data was marked as expedited by the remote system.</span></span> <span data-ttu-id="d9ca0-678">Die verbleibenden Daten werden später gesendet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-678">The remaining data will be sent later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-679"><span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**Fehler \_ Ereignis \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-679"><span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**ERROR\_EVENT\_DONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-680">710 (0x2c6)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-680">710 (0x2C6)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-681">{TDI-Ereignis abgeschlossen} Die TDI-Anzeige wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-681">{TDI Event Done} The TDI indication has completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-682"><span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**Fehler \_ Ereignis \_ Ausstehend**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-682"><span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**ERROR\_EVENT\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-683">711 (0x2c7)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-683">711 (0x2C7)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-684">{TDI-Ereignis steht aus. Der TDI-Hinweis wurde in den Status "Ausstehend" versetzt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-684">{TDI Event Pending} The TDI indication has entered the pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-685"><span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**Fehler beim über \_ prüfen des \_ Datei \_ Systems**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-685"><span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**ERROR\_CHECKING\_FILE\_SYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-686">712 (0x2c8)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-686">712 (0x2C8)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-687">Das Dateisystem auf% WZ wird überprüft.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-687">Checking file system on %wZ.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-688"><span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**Fehler \_ beim \_ Beenden der app. \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-688"><span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**ERROR\_FATAL\_APP\_EXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-689">713 (0x2c9)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-689">713 (0x2C9)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-690">{Schwerwiegender Anwendungs Exit}% HS.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-690">{Fatal Application Exit} %hs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-691"><span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**Fehler \_ vordefiniertes \_ handle**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-691"><span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**ERROR\_PREDEFINED\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-692">714 (0x2ca)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-692">714 (0x2CA)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-693">Auf den angegebenen Registrierungsschlüssel wird von einem vordefinierten Handle verwiesen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-693">The specified registry key is referenced by a predefined handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-694"><span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**Fehler \_ wurde \_ entsperrt.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-694"><span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**ERROR\_WAS\_UNLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-695">715 (0x2cb)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-695">715 (0x2CB)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-696">{Seite entsperrt} Der Seitenschutz einer gesperrten Seite wurde in "kein Zugriff" geändert, und die Seite wurde aus dem Arbeitsspeicher und aus dem Prozess entsperrt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-696">{Page Unlocked} The page protection of a locked page was changed to 'No Access' and the page was unlocked from memory and from the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-697"><span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**Fehler \_ Dienst \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-697"><span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**ERROR\_SERVICE\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-698">716 (0x2cc)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-698">716 (0x2CC)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-699">% HS</span><span class="sxs-lookup"><span data-stu-id="d9ca0-699">%hs</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-700"><span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**der Fehler \_ wurde \_ gesperrt.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-700"><span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**ERROR\_WAS\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-701">717 (0x2cd)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-701">717 (0x2CD)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-702">{Seite gesperrt} Eine der zu Sperr enden Seiten war bereits gesperrt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-702">{Page Locked} One of the pages to lock was already locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-703"><span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**\_ \_ schwer Fehlerprotokoll \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-703"><span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**ERROR\_LOG\_HARD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-704">718 (0x2ce)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-704">718 (0x2CE)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-705">Anwendungs Popup: %1: %2</span><span class="sxs-lookup"><span data-stu-id="d9ca0-705">Application popup: %1 : %2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-706"><span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**Fehler \_ bereits \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-706"><span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**ERROR\_ALREADY\_WIN32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-707">719 (0x2cf)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-707">719 (0x2CF)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-708">Fehler \_ bereits \_ Win32</span><span class="sxs-lookup"><span data-stu-id="d9ca0-708">ERROR\_ALREADY\_WIN32</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-709"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**Fehler \_ Bild des \_ Computer Typs nicht übereinstimmende \_ \_ \_ exe-Datei**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-709"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**ERROR\_IMAGE\_MACHINE\_TYPE\_MISMATCH\_EXE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-710">720 (0x2d0)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-710">720 (0x2D0)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-711">{Nicht übereinstimmende Computertypen} Die Abbild Datei "% hs" ist gültig, aber für einen anderen Computertyp als den aktuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-711">{Machine Type Mismatch} The image file %hs is valid, but is for a machine type other than the current machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-712"><span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**Fehler \_ keine \_ Yield- \_ Ausführung**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-712"><span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**ERROR\_NO\_YIELD\_PERFORMED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-713">721 (0x2d1)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-713">721 (0x2D1)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-714">Eine Yield-Ausführung wurde ausgeführt, und es konnte kein Thread ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-714">A yield execution was performed and no thread was available to run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-715"><span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**Fehler Zeit Geber-Fortsetzung \_ \_ \_ ignoriert**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-715"><span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**ERROR\_TIMER\_RESUME\_IGNORED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-716">722 (0x2d2)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-716">722 (0x2D2)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-717">Das Fort Setz Bare Flag für eine Timer-API wurde ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-717">The resumable flag to a timer API was ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-718"><span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**Fehler bei der \_ Schiedsgerichtsbarkeit \_ nicht behandelt**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-718"><span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**ERROR\_ARBITRATION\_UNHANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-719">723 (0x2d3)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-719">723 (0x2D3)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-720">Der Arbiter hat die Vermittlung dieser Ressourcen für das übergeordnete Element verzögert.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-720">The arbiter has deferred arbitration of these resources to its parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-721"><span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**Fehler \_ CardBus \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-721"><span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**ERROR\_CARDBUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-722">724 (0x2d4)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-722">724 (0x2D4)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-723">Das eingefügte CardBus-Gerät kann aufgrund eines Konfigurations Fehlers auf "% hs" nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-723">The inserted CardBus device cannot be started because of a configuration error on "%hs".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-724"><span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**Fehler- \_ MP- \_ Prozessor Konflikt \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-724"><span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**ERROR\_MP\_PROCESSOR\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-725">725 (0x2d5)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-725">725 (0x2D5)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-726">Die CPUs in diesem Multiprozessorsystem weisen nicht die gleiche Revisions Ebene auf.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-726">The CPUs in this multiprocessor system are not all the same revision level.</span></span> <span data-ttu-id="d9ca0-727">Um alle Prozessoren zu verwenden, schränkt das Betriebssystem die Funktionen des am wenigsten leistungsfähigen Prozessors im System ein.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-727">To use all processors the operating system restricts itself to the features of the least capable processor in the system.</span></span> <span data-ttu-id="d9ca0-728">Sollten Probleme mit diesem System auftreten, wenden Sie sich an den CPU-Hersteller, um festzustellen, ob diese Kombination von Prozessoren unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="d9ca0-728">Should problems occur with this system, contact the CPU manufacturer to see if this mix of processors is supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-729"><span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**Fehler im Ruhezustand \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-729"><span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**ERROR\_HIBERNATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-730">726 (0x2d6)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-730">726 (0x2D6)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-731">Das System wurde in den Ruhezustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-731">The system was put into hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-732"><span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**Fehler beim Fortsetzen des Ruhe Zustands \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-732"><span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**ERROR\_RESUME\_HIBERNATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-733">727 (0x2d7)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-733">727 (0x2D7)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-734">Das System wurde aus dem Ruhezustand fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-734">The system was resumed from hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-735"><span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**Fehler \_ Firmware \_ aktualisiert**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-735"><span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**ERROR\_FIRMWARE\_UPDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-736">728 (0x2d8)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-736">728 (0x2D8)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-737">Es wurde festgestellt, dass das \[ vorherige Firmwareupdate = %2, Aktuelles Firmwareupdate %3, aktualisiert wurde \] .</span><span class="sxs-lookup"><span data-stu-id="d9ca0-737">Windows has detected that the system firmware (BIOS) was updated \[previous firmware date = %2, current firmware date %3\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-738"><span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**Fehler Treiber, die auf \_ \_ \_ Gesperrte \_ Seiten weichen**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-738"><span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**ERROR\_DRIVERS\_LEAKING\_LOCKED\_PAGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-739">729 (0x2d9)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-739">729 (0x2D9)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-740">Ein Gerätetreiber entfernt gesperrte e/A-Seiten, die eine Beeinträchtigung des Systems verursachen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-740">A device driver is leaking locked I/O pages causing system degradation.</span></span> <span data-ttu-id="d9ca0-741">Das System hat den Verfolgungs Code automatisch aktiviert, um zu versuchen, den Übeltäter abzufangen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-741">The system has automatically enabled tracking code in order to try and catch the culprit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-742"><span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**Fehler Reaktivierungs \_ \_ System**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-742"><span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**ERROR\_WAKE\_SYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-743">730 (0x2da)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-743">730 (0x2DA)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-744">Das System wurde reaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-744">The system has awoken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-745"><span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**Fehler \_ Wartezeit \_ 1**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-745"><span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**ERROR\_WAIT\_1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-746">731 (0x2db)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-746">731 (0x2DB)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-747">Fehler \_ Wartezeit \_ 1</span><span class="sxs-lookup"><span data-stu-id="d9ca0-747">ERROR\_WAIT\_1</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-748"><span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**Fehler \_ Wartezeit \_ 2**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-748"><span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**ERROR\_WAIT\_2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-749">732 (0x2dc)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-749">732 (0x2DC)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-750">Fehler \_ Wartezeit \_ 2</span><span class="sxs-lookup"><span data-stu-id="d9ca0-750">ERROR\_WAIT\_2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-751"><span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**Fehler \_ Wartezeit \_ 3**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-751"><span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**ERROR\_WAIT\_3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-752">733 (0x2dd)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-752">733 (0x2DD)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-753">Fehler \_ Wartezeit \_ 3</span><span class="sxs-lookup"><span data-stu-id="d9ca0-753">ERROR\_WAIT\_3</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-754"><span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**Fehler \_ Wartezeit \_ 63**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-754"><span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**ERROR\_WAIT\_63**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-755">734 (0x2de)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-755">734 (0x2DE)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-756">Fehler \_ Wartezeit \_ 63</span><span class="sxs-lookup"><span data-stu-id="d9ca0-756">ERROR\_WAIT\_63</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-757"><span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**Fehler \_ abgebrochen, \_ Wartezeit \_ 0**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-757"><span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**ERROR\_ABANDONED\_WAIT\_0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-758">735 (0x2df)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-758">735 (0x2DF)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-759">Fehler \_ abgebrochen, \_ Wartezeit \_ 0</span><span class="sxs-lookup"><span data-stu-id="d9ca0-759">ERROR\_ABANDONED\_WAIT\_0</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-760"><span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**Fehler \_ abgebrochen, \_ Wartezeit \_ 63**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-760"><span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**ERROR\_ABANDONED\_WAIT\_63**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-761">736 (0x2e0)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-761">736 (0x2E0)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-762">Fehler \_ abgebrochen, \_ Wartezeit \_ 63</span><span class="sxs-lookup"><span data-stu-id="d9ca0-762">ERROR\_ABANDONED\_WAIT\_63</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-763"><span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**Fehler \_ Benutzer- \_ APC**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-763"><span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**ERROR\_USER\_APC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-764">737 (0x2e1)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-764">737 (0x2E1)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-765">Fehler \_ Benutzer- \_ APC</span><span class="sxs-lookup"><span data-stu-id="d9ca0-765">ERROR\_USER\_APC</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-766"><span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**Fehler \_ Kernel- \_ APC**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-766"><span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**ERROR\_KERNEL\_APC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-767">738 (0x2e2)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-767">738 (0x2E2)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-768">Fehler \_ Kernel- \_ APC</span><span class="sxs-lookup"><span data-stu-id="d9ca0-768">ERROR\_KERNEL\_APC</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-769"><span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**Fehler \_ gewarnt**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-769"><span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**ERROR\_ALERTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-770">739 (0x2e3)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-770">739 (0x2E3)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-771">Fehler \_ gewarnt</span><span class="sxs-lookup"><span data-stu-id="d9ca0-771">ERROR\_ALERTED</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-772"><span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**Fehler \_ Erhöhung \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-772"><span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**ERROR\_ELEVATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-773">740 (0x2e4)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-773">740 (0x2E4)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-774">Der angeforderte Vorgang erfordert eine Erhöhung der Rechte.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-774">The requested operation requires elevation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-775"><span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**Fehler \_ Analyse**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-775"><span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**ERROR\_REPARSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-776">741 (0x2e5)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-776">741 (0x2E5)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-777">Vom Objekt-Manager sollte eine Analyse ausgeführt werden, da der Name der Datei zu einem symbolischen Link geführt hat.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-777">A reparse should be performed by the Object Manager since the name of the file resulted in a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-778"><span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**Fehler \_ beim Oplock-Vorgang \_ \_ in Bearbeitung. \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-778"><span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**ERROR\_OPLOCK\_BREAK\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-779">742 (0x2e6)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-779">742 (0x2E6)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-780">Ein Open/Create-Vorgang wurde abgeschlossen, während eine Unterbrechung der Sperre ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-780">An open/create operation completed while an oplock break is underway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-781"><span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**Fehler \_ Volume bereitgestellt \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-781"><span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**ERROR\_VOLUME\_MOUNTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-782">743 (0x2e7)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-782">743 (0x2E7)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-783">Ein neues Volume wurde von einem Dateisystem bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-783">A new volume has been mounted by a file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-784"><span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**Fehler beim Ausführen von \_ rxact. \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-784"><span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**ERROR\_RXACT\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-785">744 (0x2E8)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-785">744 (0x2E8)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-786">Dieser Status der Erfolgs Stufe gibt an, dass der Transaktionsstatus für die Registrierungs Unterstruktur bereits vorhanden ist, dass jedoch bereits ein Transaktionscommit abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-786">This success level status indicates that the transaction state already exists for the registry sub-tree, but that a transaction commit was previously aborted.</span></span> <span data-ttu-id="d9ca0-787">Der Commit ist nun abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-787">The commit has now been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-788"><span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**Fehler \_ beim \_ Cleanup der Fehler Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-788"><span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**ERROR\_NOTIFY\_CLEANUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-789">745 (0x2e9)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-789">745 (0x2E9)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-790">Dies weist darauf hin, dass ein Benachrichtigungs Change Request durch Schließen des Handles abgeschlossen wurde, das die Benachrichtigung Change Request.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-790">This indicates that a notify change request has been completed due to closing the handle which made the notify change request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-791"><span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**Fehler bei \_ primärer \_ Transport \_ Verbindung \_ .**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-791"><span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**ERROR\_PRIMARY\_TRANSPORT\_CONNECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-792">746 (0x2ea)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-792">746 (0x2EA)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-793">{Connect-Fehler beim primären Transport} Es wurde versucht, eine Verbindung mit dem Remote Server "% hs" auf dem primären Transport herzustellen, aber die Verbindung konnte nicht hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-793">{Connect Failure on Primary Transport} An attempt was made to connect to the remote server %hs on the primary transport, but the connection failed.</span></span> <span data-ttu-id="d9ca0-794">Der Computer konnte über einen sekundären Transport eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-794">The computer WAS able to connect on a secondary transport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-795"><span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**Fehler \_ Seiten-Fehler \_ \_ Übergang**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-795"><span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**ERROR\_PAGE\_FAULT\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-796">747 (0x2eb)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-796">747 (0x2EB)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-797">Der Seiten Fehler war ein Übergangs Fehler.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-797">Page fault was a transition fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-798"><span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**Fehler \_ Seiten-Fehler \_ \_ Anforderung \_ null**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-798"><span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**ERROR\_PAGE\_FAULT\_DEMAND\_ZERO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-799">748 (0x2ec)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-799">748 (0x2EC)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-800">Der Seiten Fehler war ein Fehler, der NULL ist.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-800">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-801"><span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**Fehler \_ Seiten-Fehler \_ \_ Kopie \_ beim \_ schreiben**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-801"><span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**ERROR\_PAGE\_FAULT\_COPY\_ON\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-802">749 (0x2ed)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-802">749 (0x2ED)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-803">Der Seiten Fehler war ein Fehler, der NULL ist.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-803">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-804"><span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**Fehler \_ Seite \_ \_ Fehlerschutz ( \_ Seite)**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-804"><span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**ERROR\_PAGE\_FAULT\_GUARD\_PAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-805">750 (0x2ee)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-805">750 (0x2EE)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-806">Der Seiten Fehler war ein Fehler, der NULL ist.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-806">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-807"><span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**Fehler \_ Seiten \_ - \_ Paging- \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-807"><span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**ERROR\_PAGE\_FAULT\_PAGING\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-808">751 (0x2ef)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-808">751 (0x2EF)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-809">Der Seiten Fehler wurde durchlesen von einem sekundären Speichergerät erfüllt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-809">Page fault was satisfied by reading from a secondary storage device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-810"><span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**Fehler \_ Cache \_ Seite \_ gesperrt**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-810"><span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**ERROR\_CACHE\_PAGE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-811">752 (0x2F 0)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-811">752 (0x2F0)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-812">Die zwischengespeicherte Seite wurde während des Vorgangs gesperrt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-812">Cached page was locked during operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-813"><span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**Fehler \_ Absturz Abbild \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-813"><span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**ERROR\_CRASH\_DUMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-814">753 (0x2F)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-814">753 (0x2F1)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-815">Absturz Abbild ist in Auslagerungs Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-815">Crash dump exists in paging file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-816"><span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**Fehler \_ Puffer \_ alle \_ Nullen**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-816"><span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**ERROR\_BUFFER\_ALL\_ZEROS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-817">754 (0x2F 2)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-817">754 (0x2F2)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-818">Der angegebene Puffer enthält alle Nullen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-818">Specified buffer contains all zeros.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-819"><span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**Fehleranalyse \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-819"><span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**ERROR\_REPARSE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-820">755 (0x2F)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-820">755 (0x2F3)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-821">Vom Objekt-Manager sollte eine Analyse ausgeführt werden, da der Name der Datei zu einem symbolischen Link geführt hat.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-821">A reparse should be performed by the Object Manager since the name of the file resulted in a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-822"><span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**Fehler beim \_ Ändern der Ressourcen \_ Anforderungen. \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-822"><span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**ERROR\_RESOURCE\_REQUIREMENTS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-823">756 (0x2F)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-823">756 (0x2F4)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-824">Das Gerät hat eine Abfrage beendet, und die zugehörigen Ressourcenanforderungen wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-824">The device has succeeded a query-stop and its resource requirements have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-825"><span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**Fehler \_ Übersetzung ist \_ beendet**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-825"><span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**ERROR\_TRANSLATION\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-826">757 (0x2F)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-826">757 (0x2F5)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-827">Der Konvertierer hat diese Ressourcen in den globalen Bereich übersetzt, und es sollten keine weiteren Übersetzungen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-827">The translator has translated these resources into the global space and no further translations should be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-828"><span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**Fehler \_ beim \_ \_ beenden.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-828"><span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**ERROR\_NOTHING\_TO\_TERMINATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-829">758 (0x2F)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-829">758 (0x2F6)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-830">Ein Prozess, der beendet wird, verfügt über keine zu beendenden Threads.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-830">A process being terminated has no threads to terminate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-831"><span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**Fehler \_ Prozess \_ nicht \_ in \_ Auftrag**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-831"><span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**ERROR\_PROCESS\_NOT\_IN\_JOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-832">759 (0x2F)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-832">759 (0x2F7)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-833">Der angegebene Prozess ist nicht Teil eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-833">The specified process is not part of a job.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-834"><span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**Fehler \_ Prozess \_ in \_ Auftrag**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-834"><span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**ERROR\_PROCESS\_IN\_JOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-835">760 (0x2F 8)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-835">760 (0x2F8)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-836">Der angegebene Prozess ist Teil eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-836">The specified process is part of a job.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-837"><span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**Fehler beim Volsnap-in- \_ \_ \_ Ready-Zustand.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-837"><span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**ERROR\_VOLSNAP\_HIBERNATE\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-838">761 (0x2F)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-838">761 (0x2F9)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-839">{Volumeschattenkopie-Dienst} Das System ist nun bereit für den Ruhezustand.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-839">{Volume Shadow Copy Service} The system is now ready for hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-840"><span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**Fehler " \_ fsfilter op" wurde \_ \_ \_ erfolgreich abgeschlossen.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-840"><span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**ERROR\_FSFILTER\_OP\_COMPLETED\_SUCCESSFULLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-841">762 (0x2fa)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-841">762 (0x2FA)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-842">Ein Dateisystem-oder Dateisystem Filter-Treiber hat einen fsfilter-Vorgang erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-842">A file system or file system filter driver has successfully completed an FsFilter operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-843"><span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**Fehler \_ Interrupt- \_ Vektor \_ bereits \_ verbunden**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-843"><span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**ERROR\_INTERRUPT\_VECTOR\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-844">763 (0x2fb)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-844">763 (0x2FB)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-845">Der angegebene Interrupt-Vektor war bereits verbunden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-845">The specified interrupt vector was already connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-846"><span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**Fehler \_ Interrupt ist \_ weiterhin \_ verbunden.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-846"><span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**ERROR\_INTERRUPT\_STILL\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-847">764 (0x2fc)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-847">764 (0x2FC)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-848">Der angegebene Interrupt-Vektor ist weiterhin verbunden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-848">The specified interrupt vector is still connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-849"><span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**Fehler beim \_ warten \_ auf \_ Oplock.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-849"><span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**ERROR\_WAIT\_FOR\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-850">765 (0x2fd)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-850">765 (0x2FD)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-851">Ein Vorgang wird blockiert, wenn auf eine Oplock-Sperre gewartet wird.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-851">An operation is blocked waiting for an oplock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-852"><span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**Fehler bei \_ dbg- \_ Ausnahme. \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-852"><span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**ERROR\_DBG\_EXCEPTION\_HANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-853">766 (0x2fe)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-853">766 (0x2FE)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-854">Vom Debugger behandelte Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-854">Debugger handled exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-855"><span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**Fehler \_ dbg \_ fortsetzen**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-855"><span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**ERROR\_DBG\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-856">767 (0x2ff)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-856">767 (0x2FF)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-857">Der Debugger wurde fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-857">Debugger continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-858"><span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**Fehler \_ Rückruf- \_ Pop- \_ Stapel**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-858"><span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**ERROR\_CALLBACK\_POP\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-859">768 (0x300)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-859">768 (0x300)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-860">Eine Ausnahme ist in einem Benutzermodus-Rückruf aufgetreten, und der Kernel Rückruf Frame sollte entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-860">An exception occurred in a user mode callback and the kernel callback frame should be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-861"><span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**Fehler \_ Komprimierung \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-861"><span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**ERROR\_COMPRESSION\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-862">769 (0x301)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-862">769 (0x301)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-863">Die Komprimierung ist für dieses Volume deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-863">Compression is disabled for this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-864"><span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**Fehler beim \_ kanfetchrückwärts**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-864"><span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**ERROR\_CANTFETCHBACKWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-865">770 (0x302)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-865">770 (0x302)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-866">Der Datenanbieter kann ein Resultset nicht rückwärts abrufen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-866">The data provider cannot fetch backwards through a result set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-867"><span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**Fehler beim \_ kanscrollrückwärts**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-867"><span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**ERROR\_CANTSCROLLBACKWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-868">771 (0x303)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-868">771 (0x303)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-869">Der Datenanbieter kann nicht rückwärts durch ein Resultset scrollen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-869">The data provider cannot scroll backwards through a result set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-870"><span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**Fehler \_ rowsnotregeleast**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-870"><span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**ERROR\_ROWSNOTRELEASED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-871">772 (0x304)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-871">772 (0x304)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-872">Der Datenanbieter erfordert, dass zuvor abgerufene Daten freigegeben werden, bevor Sie weitere Daten anfordern.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-872">The data provider requires that previously fetched data is released before asking for more data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-873"><span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**Fehler \_ hafte \_ Accessor- \_ Flags**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-873"><span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**ERROR\_BAD\_ACCESSOR\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-874">773 (0x305)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-874">773 (0x305)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-875">Der Datenanbieter konnte die Flags, die für eine Spalten Bindung in einem Accessor festgelegt wurden, nicht interpretieren.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-875">The data provider was not able to interpret the flags set for a column binding in an accessor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-876"><span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**Fehler \_ Fehler \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-876"><span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**ERROR\_ERRORS\_ENCOUNTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-877">774 (0x306)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-877">774 (0x306)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-878">Beim Verarbeiten der Anforderung ist mindestens ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-878">One or more errors occurred while processing the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-879"><span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**Fehler \_ nicht \_ möglich**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-879"><span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**ERROR\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-880">775 (0x307)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-880">775 (0x307)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-881">Die-Implementierung ist nicht in der Lage, die Anforderung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-881">The implementation is not capable of performing the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-882"><span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**Fehler \_ Anforderung \_ außerhalb \_ der \_ Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-882"><span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**ERROR\_REQUEST\_OUT\_OF\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-883">776 (0x308)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-883">776 (0x308)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-884">Der Client einer Komponente hat einen Vorgang angefordert, der aufgrund des Status der Komponenteninstanz nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-884">The client of a component requested an operation which is not valid given the state of the component instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-885"><span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**Fehler beim Analysieren der Fehler \_ Version. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-885"><span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**ERROR\_VERSION\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-886">777 (0x309)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-886">777 (0x309)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-887">Eine Versionsnummer konnte nicht analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-887">A version number could not be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-888"><span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**Fehler \_ badstartposition**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-888"><span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**ERROR\_BADSTARTPOSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-889">778 (0x30a)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-889">778 (0x30A)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-890">Die Startposition des Iterators ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-890">The iterator's start position is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-891"><span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**Hardware des Fehler \_ Speichers \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-891"><span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**ERROR\_MEMORY\_HARDWARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-892">779 (0x30b)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-892">779 (0x30B)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-893">Die Hardware hat einen nicht korrigierbaren Speicherfehler gemeldet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-893">The hardware has reported an uncorrectable memory error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-894"><span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**Fehler Datenträger \_ \_ Reparatur \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-894"><span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**ERROR\_DISK\_REPAIR\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-895">780 (0x30c)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-895">780 (0x30C)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-896">Für den versuchten Vorgang musste die Selbstreparatur aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-896">The attempted operation required self healing to be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-897"><span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**Fehler \_ \_ bei unzureichender Ressource \_ für \_ angegebene Größe des frei \_ gegebenen \_ Abschnitts \_ .**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-897"><span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ERROR\_INSUFFICIENT\_RESOURCE\_FOR\_SPECIFIED\_SHARED\_SECTION\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-898">781 (0x30d)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-898">781 (0x30D)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-899">Der Desktop Heap hat beim Zuordnen des Sitzungs Speichers einen Fehler gefunden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-899">The Desktop heap encountered an error while allocating session memory.</span></span> <span data-ttu-id="d9ca0-900">Weitere Informationen finden Sie im System Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-900">There is more information in the system event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-901"><span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**Fehler \_ System- \_ PowerState- \_ Übergang**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-901"><span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**ERROR\_SYSTEM\_POWERSTATE\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-902">782 (0x30e)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-902">782 (0x30E)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-903">Der System Energiezustand wechselt von "%2" in "%3".</span><span class="sxs-lookup"><span data-stu-id="d9ca0-903">The system power state is transitioning from %2 to %3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-904"><span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**Fehler \_ System- \_ PowerState- \_ komplexer \_ Übergang**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-904"><span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**ERROR\_SYSTEM\_POWERSTATE\_COMPLEX\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-905">783 (0x30f)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-905">783 (0x30F)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-906">Der System Energiezustand wechselt von "%2" in "%3", kann jedoch "%4" eingeben.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-906">The system power state is transitioning from %2 to %3 but could enter %4.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-907"><span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**Fehler bei \_ MCA- \_ Ausnahme.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-907"><span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**ERROR\_MCA\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-908">784 (0x310)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-908">784 (0x310)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-909">Ein Thread wird aufgrund von MCA mit der MCA-Ausnahme versendet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-909">A thread is getting dispatched with MCA EXCEPTION because of MCA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-910"><span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**Fehler \_ Zugriffs \_ Überwachung \_ nach \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-910"><span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**ERROR\_ACCESS\_AUDIT\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-911">785 (0x311)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-911">785 (0x311)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-912">Der Zugriff auf "%1" wird von der Richtlinien Regel "%2" überwacht.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-912">Access to %1 is monitored by policy rule %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-913"><span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**Fehler \_ Zugriff \_ \_ ohne \_ sicherere \_ Benutzeroberfläche \_ nach \_ Richtlinie deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-913"><span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**ERROR\_ACCESS\_DISABLED\_NO\_SAFER\_UI\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-914">786 (0x312)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-914">786 (0x312)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-915">Der Zugriff auf "%1" wurde durch den Administrator durch die Richtlinien Regel "%2" eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-915">Access to %1 has been restricted by your Administrator by policy rule %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-916"><span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**Fehler beim Abbrechen der Ruhe Zustands \_ \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-916"><span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**ERROR\_ABANDON\_HIBERFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-917">787 (0x313)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-917">787 (0x313)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-918">Eine gültige Ruhe Zustands Datei wurde für ungültig erklärt und sollte abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-918">A valid hibernation file has been invalidated and should be abandoned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-919"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**Fehler beim Rück Schreiben von \_ \_ Daten im \_ \_ Netzwerk \_ .**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-919"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_NETWORK\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-920">788 (0x314)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-920">788 (0x314)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-921">{Verzögertes Schreiben fehlgeschlagen} In Windows konnten nicht alle Daten für die Datei "% hs;" gespeichert werden. die Daten sind verloren gegangen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-921">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="d9ca0-922">Dieser Fehler kann durch Probleme mit der Netzwerk Konnektivität verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-922">This error may be caused by network connectivity issues.</span></span> <span data-ttu-id="d9ca0-923">Versuchen Sie, diese Datei an anderer Stelle zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-923">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-924"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**Fehler \_ beim \_ \_ Daten \_ Netzwerk \_ Server- \_ Fehler beim Rück Schreiben von Daten.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-924"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_NETWORK\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-925">789 (0x315)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-925">789 (0x315)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-926">{Verzögertes Schreiben fehlgeschlagen} In Windows konnten nicht alle Daten für die Datei "% hs;" gespeichert werden. die Daten sind verloren gegangen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-926">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="d9ca0-927">Dieser Fehler wurde vom Server zurückgegeben, auf dem die Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-927">This error was returned by the server on which the file exists.</span></span> <span data-ttu-id="d9ca0-928">Versuchen Sie, diese Datei an anderer Stelle zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-928">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-929"><span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**Fehler beim Zugriff auf \_ \_ \_ \_ den lokalen Daten \_ Träger des Schreibvorgangs \_ .**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-929"><span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_LOCAL\_DISK\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-930">790 (0x316)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-930">790 (0x316)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-931">{Verzögertes Schreiben fehlgeschlagen} In Windows konnten nicht alle Daten für die Datei "% hs;" gespeichert werden. die Daten sind verloren gegangen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-931">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="d9ca0-932">Dieser Fehler kann darauf zurückzuführen sein, dass das Gerät entfernt wurde oder das Medium schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-932">This error may be caused if the device has been removed or the media is write-protected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-933"><span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**Fehler \_ hafte \_ MCFG- \_ Tabelle**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-933"><span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**ERROR\_BAD\_MCFG\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-934">791 (0x317)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-934">791 (0x317)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-935">Die für dieses Gerät erforderlichen Ressourcen stehen in Konflikt mit der MCFG-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-935">The resources required for this device conflict with the MCFG table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-936"><span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**Fehler Datenträger \_ \_ Reparatur \_ umgeleitet**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-936"><span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**ERROR\_DISK\_REPAIR\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-937">792 (0x318)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-937">792 (0x318)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-938">Die volumereparatur konnte nicht durchgeführt werden, während Sie online ist.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-938">The volume repair could not be performed while it is online.</span></span> <span data-ttu-id="d9ca0-939">Bitte planen Sie, das Volume offline zu schalten, damit es repariert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-939">Please schedule to take the volume offline so that it can be repaired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-940"><span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**Fehler beim Reparieren des Datenträgers. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-940"><span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**ERROR\_DISK\_REPAIR\_UNSUCCESSFUL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-941">793 (0x319)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-941">793 (0x319)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-942">Die volumereparatur war nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-942">The volume repair was not successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-943"><span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**Fehler \_ beschädigte \_ Protokoll \_ Überschreitung**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-943"><span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**ERROR\_CORRUPT\_LOG\_OVERFULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-944">794 (0x31a)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-944">794 (0x31A)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-945">Eines der volumebeschädigungsprotokolle ist voll.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-945">One of the volume corruption logs is full.</span></span> <span data-ttu-id="d9ca0-946">Weitere beschädigte Beschädigungen werden nicht protokolliert.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-946">Further corruptions that may be detected won't be logged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-947"><span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**Fehler \_ \_ beschädigte Protokoll \_ beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-947"><span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**ERROR\_CORRUPT\_LOG\_CORRUPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-948">795 (0x31b)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-948">795 (0x31B)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-949">Eines der Protokolle der Volumebeschädigung ist intern beschädigt und muss neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-949">One of the volume corruption logs is internally corrupted and needs to be recreated.</span></span> <span data-ttu-id="d9ca0-950">Das Volume kann nicht erkannte Beschädigungen enthalten und muss gescannt werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-950">The volume may contain undetected corruptions and must be scanned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-951"><span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**Fehler \_ beschädigte \_ Protokoll nicht \_ verfügbar.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-951"><span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**ERROR\_CORRUPT\_LOG\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-952">796 (0x31c)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-952">796 (0x31C)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-953">Eines der Protokolle der Volumebeschädigung ist nicht für die Verwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-953">One of the volume corruption logs is unavailable for being operated on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-954"><span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**Fehler \_ beim \_ Löschen des Protokolls \_ \_ vollständig.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-954"><span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**ERROR\_CORRUPT\_LOG\_DELETED\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-955">797 (0x31d)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-955">797 (0x31D)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-956">Eines der volumebeschädigungsprotokolle wurde gelöscht, und es wurden weiterhin beschädigte Datensätze angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-956">One of the volume corruption logs was deleted while still having corruption records in them.</span></span> <span data-ttu-id="d9ca0-957">Das Volume enthält erkannte Beschädigungen und muss gescannt werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-957">The volume contains detected corruptions and must be scanned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-958"><span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**Fehler \_ beim \_ Löschen des Protokolls. \_**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-958"><span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**ERROR\_CORRUPT\_LOG\_CLEARED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-959">798 (0x31e)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-959">798 (0x31E)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-960">Eines der Protokolle der Volumebeschädigung wurde von CHKDSK gelöscht und enthält keine echten Beschädigungen mehr.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-960">One of the volume corruption logs was cleared by chkdsk and no longer contains real corruptions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-961"><span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**Fehler \_ verwaister \_ Name \_ aufgebraucht**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-961"><span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**ERROR\_ORPHAN\_NAME\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-962">799 (0x31f)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-962">799 (0x31F)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-963">Auf dem Volume sind verwaiste Dateien vorhanden, Sie konnten jedoch nicht wieder hergestellt werden, da im Wiederherstellungs Verzeichnis keine weiteren neuen Namen erstellt werden konnten.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-963">Orphaned files exist on the volume but could not be recovered because no more new names could be created in the recovery directory.</span></span> <span data-ttu-id="d9ca0-964">Dateien müssen aus dem Wiederherstellungs Verzeichnis verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-964">Files must be moved from the recovery directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-965"><span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**Fehler- \_ Oplock \_ \_ zum \_ neuen \_ handle gewechselt**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-965"><span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**ERROR\_OPLOCK\_SWITCHED\_TO\_NEW\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-966">800 (0x320)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-966">800 (0x320)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-967">Die Oplock, die diesem Handle zugeordnet war, ist jetzt einem anderen Handle zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-967">The oplock that was associated with this handle is now associated with a different handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-968"><span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**Fehler \_ beim \_ erteilen der \_ angeforderten \_ Oplock.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-968"><span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**ERROR\_CANNOT\_GRANT\_REQUESTED\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-969">801 (0x321)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-969">801 (0x321)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-970">Eine Oplock der angeforderten Ebene kann nicht erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-970">An oplock of the requested level cannot be granted.</span></span> <span data-ttu-id="d9ca0-971">Möglicherweise ist eine Oplock einer niedrigeren Ebene verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-971">An oplock of a lower level may be available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-972"><span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**Fehler \_ beim \_ Abbrechen der \_ Oplock-Taste**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-972"><span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**ERROR\_CANNOT\_BREAK\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-973">802 (0x322)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-973">802 (0x322)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-974">Der Vorgang wurde nicht erfolgreich abgeschlossen, da er dazu führen würde, dass ein Oplock-Vorgang abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-974">The operation did not complete successfully because it would cause an oplock to be broken.</span></span> <span data-ttu-id="d9ca0-975">Der Aufrufer hat angefordert, dass vorhandene oplocks nicht beschädigt sind.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-975">The caller has requested that existing oplocks not be broken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-976"><span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**Fehler " \_ Oplock \_ handle" \_ geschlossen**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-976"><span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**ERROR\_OPLOCK\_HANDLE\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-977">803 (0x323)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-977">803 (0x323)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-978">Das Handle, dem diese Oplock zugeordnet war, wurde geschlossen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-978">The handle with which this oplock was associated has been closed.</span></span> <span data-ttu-id="d9ca0-979">Die Oplock ist nun beschädigt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-979">The oplock is now broken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-980"><span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**Error \_ No \_ ACE- \_ Bedingung**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-980"><span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**ERROR\_NO\_ACE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-981">804 (0x324)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-981">804 (0x324)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-982">Der angegebene ACE (Access Control Entry, Zugriffs Steuerungs Eintrag) enthält keine Bedingung.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-982">The specified access control entry (ACE) does not contain a condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-983"><span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**\_ungültige \_ ACE- \_ Bedingung.**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-983"><span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**ERROR\_INVALID\_ACE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-984">805 (0x325)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-984">805 (0x325)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-985">Der angegebene ACE (Access Control Entry, Zugriffs Steuerungs Eintrag) enthält eine ungültige Bedingung.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-985">The specified access control entry (ACE) contains an invalid condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-986"><span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**Fehler \_ Datei \_ handle \_ gesperrt**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-986"><span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**ERROR\_FILE\_HANDLE\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-987">806 (0x326)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-987">806 (0x326)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-988">Der Zugriff auf das angegebene Datei Handle wurde widerrufen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-988">Access to the specified file handle has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-989"><span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**Fehler \_ Bild \_ an \_ unterschiedlicher \_ Basis**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-989"><span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**ERROR\_IMAGE\_AT\_DIFFERENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-990">807 (0x327)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-990">807 (0x327)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-991">Eine Bilddatei wurde an einer anderen Adresse als der in der Bilddatei angegebenen Adresse zugeordnet, aber Fixups werden weiterhin automatisch für das Image ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-991">An image file was mapped at a different address from the one specified in the image file but fixups will still be automatically performed on the image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-992"><span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**Fehler- \_ EA- \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-992"><span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**ERROR\_EA\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-993">994 (0x3e2)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-993">994 (0x3E2)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-994">Der Zugriff auf das erweiterte Attribut wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-994">Access to the extended attribute was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-995"><span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**Fehler \_ Vorgang \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-995"><span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**ERROR\_OPERATION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-996">995 (0x3e3)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-996">995 (0x3E3)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-997">Der e/a-Vorgang wurde aufgrund eines Thread Beendigungs-oder einer Anwendungsanforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-997">The I/O operation has been aborted because of either a thread exit or an application request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-998"><span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**Fehler- \_ IO \_ unvollständig**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-998"><span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**ERROR\_IO\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-999">996 (0x3e4)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-999">996 (0x3E4)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-1000">Das überlappende e/a-Ereignis ist nicht in einem signalisierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1000">Overlapped I/O event is not in a signaled state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-1001"><span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**Fehler- \_ IO steht \_ aus**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1001"><span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**ERROR\_IO\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-1002">997 (0x3e5)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1002">997 (0x3E5)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-1003">Überlappende e/a-Vorgänge werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1003">Overlapped I/O operation is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-1004"><span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**Fehler \_ NoAccess**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1004"><span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**ERROR\_NOACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-1005">998 (0x3e6)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1005">998 (0x3E6)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-1006">Ungültiger Zugriff auf den Speicherort des Speichers.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1006">Invalid access to memory location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9ca0-1007"><span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**Fehler " \_ swaperror"**</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1007"><span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**ERROR\_SWAPERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9ca0-1008">999 (0x3e7)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1008">999 (0x3E7)</span></span>
</dt> <dt>



<span data-ttu-id="d9ca0-1009">Fehler beim Ausführen des InPage-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1009">Error performing inpage operation.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="d9ca0-1010">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1010">Requirements</span></span>



| <span data-ttu-id="d9ca0-1011">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1011">Requirement</span></span> | <span data-ttu-id="d9ca0-1012">Wert</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1012">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9ca0-1013">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1013">Minimum supported client</span></span><br/> | <span data-ttu-id="d9ca0-1014">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1014">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d9ca0-1015">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1015">Minimum supported server</span></span><br/> | <span data-ttu-id="d9ca0-1016">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1016">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9ca0-1017">Header</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1017">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9ca0-1018"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9ca0-1018"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9ca0-1019">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1019">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9ca0-1020">System Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="d9ca0-1020">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 
