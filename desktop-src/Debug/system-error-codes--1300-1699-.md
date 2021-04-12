---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 1300-1699 und ist für Entwickler bestimmt.
ms.assetid: 7b04a2ba-7bf9-4bff-93c8-cbb0060e069d
title: System Fehler Codes (1300-1699) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8fa0cbc312c8d82879322f0bc0c79533ddb961ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483318"
---
# <a name="system-error-codes-1300-1699"></a><span data-ttu-id="a0bac-103">System Fehler Codes (1300-1699)</span><span class="sxs-lookup"><span data-stu-id="a0bac-103">System Error Codes (1300-1699)</span></span>

> [!NOTE]
> <span data-ttu-id="a0bac-104">Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="a0bac-105">Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a0bac-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="a0bac-106">In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) für die Fehler 1300 bis 1699 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a0bac-106">The following list describes [system error codes](system-error-codes.md) for errors 1300 to 1699.</span></span> <span data-ttu-id="a0bac-107">Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="a0bac-108">Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".</span><span class="sxs-lookup"><span data-stu-id="a0bac-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="a0bac-109"><span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**Fehler \_ nicht \_ alle \_ zugewiesen**</span><span class="sxs-lookup"><span data-stu-id="a0bac-109"><span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**ERROR\_NOT\_ALL\_ASSIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-110">1300 (0x514)</span><span class="sxs-lookup"><span data-stu-id="a0bac-110">1300 (0x514)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-111">Nicht alle Berechtigungen oder Gruppen, auf die verwiesen wird, werden dem Aufrufer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-111">Not all privileges or groups referenced are assigned to the caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-112"><span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**Fehler \_ " \_ nicht \_ zugeordnet"**</span><span class="sxs-lookup"><span data-stu-id="a0bac-112"><span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**ERROR\_SOME\_NOT\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-113">1301 (0x515)</span><span class="sxs-lookup"><span data-stu-id="a0bac-113">1301 (0x515)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-114">Es wurde keine Zuordnung zwischen Kontonamen und Sicherheits-IDs vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-114">Some mapping between account names and security IDs was not done.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-115"><span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**Fehler " \_ keine \_ Kontingente \_ für \_ Konto"**</span><span class="sxs-lookup"><span data-stu-id="a0bac-115"><span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**ERROR\_NO\_QUOTAS\_FOR\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-116">1302 (0x516)</span><span class="sxs-lookup"><span data-stu-id="a0bac-116">1302 (0x516)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-117">Für dieses Konto sind keine System Kontingent Limits festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-117">No system quota limits are specifically set for this account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-118"><span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**Fehler beim \_ lokalen \_ Benutzer \_ Sitzungs \_ Schlüssel.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-118"><span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**ERROR\_LOCAL\_USER\_SESSION\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-119">1303 (0x517)</span><span class="sxs-lookup"><span data-stu-id="a0bac-119">1303 (0x517)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-120">Es ist kein Verschlüsselungsschlüssel verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a0bac-120">No encryption key is available.</span></span> <span data-ttu-id="a0bac-121">Es wurde ein bekannter Verschlüsselungsschlüssel zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a0bac-121">A well-known encryption key was returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-122"><span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**Fehler \_ NULL \_ LM- \_ Kennwort**</span><span class="sxs-lookup"><span data-stu-id="a0bac-122"><span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**ERROR\_NULL\_LM\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-123">1304 (0x518)</span><span class="sxs-lookup"><span data-stu-id="a0bac-123">1304 (0x518)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-124">Das Kennwort ist zu komplex, um in ein LAN-Manager-Kennwort konvertiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-124">The password is too complex to be converted to a LAN Manager password.</span></span> <span data-ttu-id="a0bac-125">Das zurückgegebene LAN Manager-Kennwort ist eine **null** -Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a0bac-125">The LAN Manager password returned is a **NULL** string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-126"><span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**Unbekannter Fehler. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-126"><span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**ERROR\_UNKNOWN\_REVISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-127">1305 (0x519)</span><span class="sxs-lookup"><span data-stu-id="a0bac-127">1305 (0x519)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-128">Die Revisions Ebene ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-128">The revision level is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-129"><span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**Fehler \_ Revision nicht übereinstimmende \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-129"><span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**ERROR\_REVISION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-130">1306 (0x51A)</span><span class="sxs-lookup"><span data-stu-id="a0bac-130">1306 (0x51A)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-131">Gibt an, dass zwei Revisions Ebenen nicht kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="a0bac-131">Indicates two revision levels are incompatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-132"><span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**Fehler \_ ungültiger \_ Besitzer**</span><span class="sxs-lookup"><span data-stu-id="a0bac-132"><span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**ERROR\_INVALID\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-133">1307 (0x51B)</span><span class="sxs-lookup"><span data-stu-id="a0bac-133">1307 (0x51B)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-134">Diese Sicherheits-ID kann nicht als Besitzer dieses Objekts zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-134">This security ID may not be assigned as the owner of this object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-135"><span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**Fehler \_ ungültige \_ primäre \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="a0bac-135"><span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**ERROR\_INVALID\_PRIMARY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-136">1308 (0x51C)</span><span class="sxs-lookup"><span data-stu-id="a0bac-136">1308 (0x51C)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-137">Diese Sicherheits-ID darf nicht als primäre Gruppe eines Objekts zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-137">This security ID may not be assigned as the primary group of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-138"><span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**Fehler \_ ohne Identitätswechsel \_ \_ Token**</span><span class="sxs-lookup"><span data-stu-id="a0bac-138"><span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**ERROR\_NO\_IMPERSONATION\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-139">1309 (0x51D)</span><span class="sxs-lookup"><span data-stu-id="a0bac-139">1309 (0x51D)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-140">Es wurde versucht, einen Identitätswechsel Token von einem Thread auszuführen, der derzeit nicht die Identität eines Clients annimmt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-140">An attempt has been made to operate on an impersonation token by a thread that is not currently impersonating a client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-141"><span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**Fehler \_ beim \_ Deaktivieren \_ obligatorisch.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-141"><span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ERROR\_CANT\_DISABLE\_MANDATORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-142">1310 (0x51E)</span><span class="sxs-lookup"><span data-stu-id="a0bac-142">1310 (0x51E)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-143">Die Gruppe ist möglicherweise nicht deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a0bac-143">The group may not be disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-144"><span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**Fehler \_ keine \_ Anmelde \_ Server**</span><span class="sxs-lookup"><span data-stu-id="a0bac-144"><span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**ERROR\_NO\_LOGON\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-145">1311 (0x51F)</span><span class="sxs-lookup"><span data-stu-id="a0bac-145">1311 (0x51F)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-146">Zurzeit stehen keine Anmelde Server zur Verfügung, um die Anmelde Anforderung zu bedienen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-146">There are currently no logon servers available to service the logon request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-147"><span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**Fehler \_ keine \_ solche \_ Anmelde \_ Sitzung.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-147"><span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**ERROR\_NO\_SUCH\_LOGON\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-148">1312 (0x520)</span><span class="sxs-lookup"><span data-stu-id="a0bac-148">1312 (0x520)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-149">Eine angegebene Anmeldesitzung ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-149">A specified logon session does not exist.</span></span> <span data-ttu-id="a0bac-150">Möglicherweise wurde Sie bereits beendet.</span><span class="sxs-lookup"><span data-stu-id="a0bac-150">It may already have been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-151"><span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**Fehler \_ keine \_ solche \_ Berechtigung**</span><span class="sxs-lookup"><span data-stu-id="a0bac-151"><span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**ERROR\_NO\_SUCH\_PRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-152">1313 (0x521)</span><span class="sxs-lookup"><span data-stu-id="a0bac-152">1313 (0x521)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-153">Es ist kein bestimmtes Privileg vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-153">A specified privilege does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-154"><span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**Fehler \_ Berechtigungen \_ nicht \_ gespeichert**</span><span class="sxs-lookup"><span data-stu-id="a0bac-154"><span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**ERROR\_PRIVILEGE\_NOT\_HELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-155">1314 (0x522)</span><span class="sxs-lookup"><span data-stu-id="a0bac-155">1314 (0x522)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-156">Dem Client fehlt ein erforderliches Privileg.</span><span class="sxs-lookup"><span data-stu-id="a0bac-156">A required privilege is not held by the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-157"><span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**\_ungültiger \_ \_ Kontoname.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-157"><span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**ERROR\_INVALID\_ACCOUNT\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-158">1315 (0x523)</span><span class="sxs-lookup"><span data-stu-id="a0bac-158">1315 (0x523)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-159">Der angegebene Name ist kein ordnungsgemäß formatierter Kontoname.</span><span class="sxs-lookup"><span data-stu-id="a0bac-159">The name provided is not a properly formed account name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-160"><span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**Fehler \_ Benutzer ist \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-160"><span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**ERROR\_USER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-161">1316 (0x524)</span><span class="sxs-lookup"><span data-stu-id="a0bac-161">1316 (0x524)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-162">Das angegebene Konto ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-162">The specified account already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-163"><span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**Fehler " \_ kein \_ solcher \_ Benutzer"**</span><span class="sxs-lookup"><span data-stu-id="a0bac-163"><span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**ERROR\_NO\_SUCH\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-164">1317 (0x525)</span><span class="sxs-lookup"><span data-stu-id="a0bac-164">1317 (0x525)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-165">Das angegebene Konto ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-165">The specified account does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-166"><span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**Fehler \_ Gruppe \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="a0bac-166"><span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**ERROR\_GROUP\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-167">1318 (0x526)</span><span class="sxs-lookup"><span data-stu-id="a0bac-167">1318 (0x526)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-168">Die angegebene Gruppe ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-168">The specified group already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-169"><span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**Fehler " \_ keine \_ solche \_ Gruppe"**</span><span class="sxs-lookup"><span data-stu-id="a0bac-169"><span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**ERROR\_NO\_SUCH\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-170">1319 (0x527)</span><span class="sxs-lookup"><span data-stu-id="a0bac-170">1319 (0x527)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-171">Die angegebene Gruppe ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-171">The specified group does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-172"><span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**Fehler \_ Mitglied \_ in \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="a0bac-172"><span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**ERROR\_MEMBER\_IN\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-173">1320 (0x528)</span><span class="sxs-lookup"><span data-stu-id="a0bac-173">1320 (0x528)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-174">Das angegebene Benutzerkonto ist bereits ein Mitglied der angegebenen Gruppe, oder die angegebene Gruppe kann nicht gelöscht werden, weil Sie ein Mitglied enthält.</span><span class="sxs-lookup"><span data-stu-id="a0bac-174">Either the specified user account is already a member of the specified group, or the specified group cannot be deleted because it contains a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-175"><span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**Fehler \_ Mitglied \_ nicht \_ in \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="a0bac-175"><span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**ERROR\_MEMBER\_NOT\_IN\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-176">1321 (0x529)</span><span class="sxs-lookup"><span data-stu-id="a0bac-176">1321 (0x529)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-177">Das angegebene Benutzerkonto ist kein Mitglied des angegebenen Gruppen Kontos.</span><span class="sxs-lookup"><span data-stu-id="a0bac-177">The specified user account is not a member of the specified group account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-178"><span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**\_Letzter \_ Administrator des Fehlers**</span><span class="sxs-lookup"><span data-stu-id="a0bac-178"><span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**ERROR\_LAST\_ADMIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-179">1322 (0x52A)</span><span class="sxs-lookup"><span data-stu-id="a0bac-179">1322 (0x52A)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-180">Dieser Vorgang ist unzulässig, da dies dazu führen könnte, dass ein Verwaltungskonto deaktiviert, gelöscht oder nicht mehr angemeldet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0bac-180">This operation is disallowed as it could result in an administration account being disabled, deleted or unable to log on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-181"><span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**\_falsches \_ Kennwort für Fehler**</span><span class="sxs-lookup"><span data-stu-id="a0bac-181"><span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**ERROR\_WRONG\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-182">1323 (0x52B)</span><span class="sxs-lookup"><span data-stu-id="a0bac-182">1323 (0x52B)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-183">Das Kennwort kann nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-183">Unable to update the password.</span></span> <span data-ttu-id="a0bac-184">Der als Aktuelles Kennwort angegebene Wert ist falsch.</span><span class="sxs-lookup"><span data-stu-id="a0bac-184">The value provided as the current password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-185"><span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**Fehler \_ Haft \_ geformtes \_ Kennwort**</span><span class="sxs-lookup"><span data-stu-id="a0bac-185"><span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**ERROR\_ILL\_FORMED\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-186">1324 (0x52C)</span><span class="sxs-lookup"><span data-stu-id="a0bac-186">1324 (0x52C)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-187">Das Kennwort kann nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-187">Unable to update the password.</span></span> <span data-ttu-id="a0bac-188">Der für das neue Kennwort angegebene Wert enthält Werte, die in Kenn Wörtern nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="a0bac-188">The value provided for the new password contains values that are not allowed in passwords.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-189"><span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**Einschränkung des Fehler \_ Kennworts \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-189"><span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**ERROR\_PASSWORD\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-190">1325 (0x52d)</span><span class="sxs-lookup"><span data-stu-id="a0bac-190">1325 (0x52D)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-191">Das Kennwort kann nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-191">Unable to update the password.</span></span> <span data-ttu-id="a0bac-192">Der für das neue Kennwort angegebene Wert entspricht nicht den Anforderungen für die Länge, Komplexität oder den Verlauf der Domäne.</span><span class="sxs-lookup"><span data-stu-id="a0bac-192">The value provided for the new password does not meet the length, complexity, or history requirements of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-193"><span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**Fehler beim \_ anmelden. \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-193"><span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**ERROR\_LOGON\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-194">1326 (0x52E)</span><span class="sxs-lookup"><span data-stu-id="a0bac-194">1326 (0x52E)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-195">Der Benutzername oder das Kennwort ist falsch.</span><span class="sxs-lookup"><span data-stu-id="a0bac-195">The user name or password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-196"><span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**Einschränkung des Fehler \_ Kontos \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-196"><span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**ERROR\_ACCOUNT\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-197">1327 (0x52F)</span><span class="sxs-lookup"><span data-stu-id="a0bac-197">1327 (0x52F)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-198">Konto Einschränkungen verhindern, dass dieser Benutzer sich anmeldet.</span><span class="sxs-lookup"><span data-stu-id="a0bac-198">Account restrictions are preventing this user from signing in.</span></span> <span data-ttu-id="a0bac-199">Beispiel: leere Kenn Wörter sind nicht zulässig, Anmeldezeiten sind beschränkt, oder es wurde eine Richtlinien Einschränkung erzwungen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-199">For example: blank passwords aren't allowed, sign-in times are limited, or a policy restriction has been enforced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-200"><span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**Fehler \_ ungültige \_ Anmelde \_ Zeiten.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-200"><span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**ERROR\_INVALID\_LOGON\_HOURS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-201">1328 (0x530)</span><span class="sxs-lookup"><span data-stu-id="a0bac-201">1328 (0x530)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-202">Ihr Konto verfügt über Zeitbeschränkungen, mit denen Sie sich momentan nicht anmelden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-202">Your account has time restrictions that keep you from signing in right now.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-203"><span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**Fehler \_ ungültige \_ Arbeitsstation**</span><span class="sxs-lookup"><span data-stu-id="a0bac-203"><span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**ERROR\_INVALID\_WORKSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-204">1329 (0x531)</span><span class="sxs-lookup"><span data-stu-id="a0bac-204">1329 (0x531)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-205">Dieser Benutzer darf sich nicht bei diesem Computer anmelden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-205">This user isn't allowed to sign in to this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-206"><span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**Fehler \_ Kennwort \_ abgelaufen**</span><span class="sxs-lookup"><span data-stu-id="a0bac-206"><span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**ERROR\_PASSWORD\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-207">1330 (0x532)</span><span class="sxs-lookup"><span data-stu-id="a0bac-207">1330 (0x532)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-208">Das Kennwort für dieses Konto ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-208">The password for this account has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-209"><span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**Fehler \_ Konto \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="a0bac-209"><span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**ERROR\_ACCOUNT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-210">1331 (0x533)</span><span class="sxs-lookup"><span data-stu-id="a0bac-210">1331 (0x533)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-211">Dieser Benutzer kann sich nicht anmelden, da dieses Konto zurzeit deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a0bac-211">This user can't sign in because this account is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-212"><span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**Fehler " \_ keine \_ zugeordnet"**</span><span class="sxs-lookup"><span data-stu-id="a0bac-212"><span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**ERROR\_NONE\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-213">1332 (0x534)</span><span class="sxs-lookup"><span data-stu-id="a0bac-213">1332 (0x534)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-214">Es wurde keine Zuordnung zwischen den Kontonamen und den Sicherheits-IDs vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-214">No mapping between account names and security IDs was done.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-215"><span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**Fehler \_ zu \_ viele \_ LUIDs \_ angefordert.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-215"><span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**ERROR\_TOO\_MANY\_LUIDS\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-216">1333 (0x535)</span><span class="sxs-lookup"><span data-stu-id="a0bac-216">1333 (0x535)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-217">Es wurden zu viele lokale Benutzer-IDs (LUIDs) gleichzeitig angefordert.</span><span class="sxs-lookup"><span data-stu-id="a0bac-217">Too many local user identifiers (LUIDs) were requested at one time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-218"><span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**Fehler- \_ LUIDs \_ aufgebraucht**</span><span class="sxs-lookup"><span data-stu-id="a0bac-218"><span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**ERROR\_LUIDS\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-219">1334 (0x536)</span><span class="sxs-lookup"><span data-stu-id="a0bac-219">1334 (0x536)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-220">Es sind keine weiteren lokalen Benutzer-IDs (LUIDs) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a0bac-220">No more local user identifiers (LUIDs) are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-221"><span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**Fehler \_ ungültige \_ untergeordnete \_ Autorität.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-221"><span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**ERROR\_INVALID\_SUB\_AUTHORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-222">1335 (0x537)</span><span class="sxs-lookup"><span data-stu-id="a0bac-222">1335 (0x537)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-223">Der Teil der untergeordneten Instanz einer Sicherheits-ID ist für diese bestimmte Verwendung ungültig.</span><span class="sxs-lookup"><span data-stu-id="a0bac-223">The subauthority part of a security ID is invalid for this particular use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-224"><span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**\_ungültige \_ ACL.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-224"><span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**ERROR\_INVALID\_ACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-225">1336 (0x538)</span><span class="sxs-lookup"><span data-stu-id="a0bac-225">1336 (0x538)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-226">Die Struktur der Zugriffs Steuerungs Liste (ACL) ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a0bac-226">The access control list (ACL) structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-227"><span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**Fehler \_ ungültige \_ SID.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-227"><span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**ERROR\_INVALID\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-228">1337 (0x539)</span><span class="sxs-lookup"><span data-stu-id="a0bac-228">1337 (0x539)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-229">Die Struktur der Sicherheits-ID ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a0bac-229">The security ID structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-230"><span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**Fehler \_ ungültige \_ Sicherheits- \_ descr**</span><span class="sxs-lookup"><span data-stu-id="a0bac-230"><span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**ERROR\_INVALID\_SECURITY\_DESCR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-231">1338 (0x53A)</span><span class="sxs-lookup"><span data-stu-id="a0bac-231">1338 (0x53A)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-232">Die Sicherheits deskriptorstruktur ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a0bac-232">The security descriptor structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-233"><span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**fehlerhafter \_ \_ Vererbungs- \_ ACL**</span><span class="sxs-lookup"><span data-stu-id="a0bac-233"><span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**ERROR\_BAD\_INHERITANCE\_ACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-234">1340 (0x53c)</span><span class="sxs-lookup"><span data-stu-id="a0bac-234">1340 (0x53C)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-235">Die geerbte Zugriffs Steuerungs Liste (Access Control List, ACL) oder der Zugriffs Steuerungs Eintrag (ACE) konnte nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-235">The inherited access control list (ACL) or access control entry (ACE) could not be built.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-236"><span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**Fehler \_ Server \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="a0bac-236"><span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**ERROR\_SERVER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-237">1341 (0x53D)</span><span class="sxs-lookup"><span data-stu-id="a0bac-237">1341 (0x53D)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-238">Der Server ist zurzeit deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a0bac-238">The server is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-239"><span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**Fehler \_ Server \_ nicht \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="a0bac-239"><span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**ERROR\_SERVER\_NOT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-240">1342 (0x53E)</span><span class="sxs-lookup"><span data-stu-id="a0bac-240">1342 (0x53E)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-241">Der Server ist zurzeit aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a0bac-241">The server is currently enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-242"><span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**\_ungültige \_ ID- \_ Autorität.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-242"><span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**ERROR\_INVALID\_ID\_AUTHORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-243">1343 (0x53F)</span><span class="sxs-lookup"><span data-stu-id="a0bac-243">1343 (0x53F)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-244">Der angegebene Wert war ein ungültiger Wert für eine bezeichnerzertifizierungs Stelle.</span><span class="sxs-lookup"><span data-stu-id="a0bac-244">The value provided was an invalid value for an identifier authority.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-245"><span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**nicht \_ zugewiesener \_ Speicherplatz \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="a0bac-245"><span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**ERROR\_ALLOTTED\_SPACE\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-246">1344 (0x540)</span><span class="sxs-lookup"><span data-stu-id="a0bac-246">1344 (0x540)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-247">Für Aktualisierungen der Sicherheitsinformationen ist kein Arbeitsspeicher mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a0bac-247">No more memory is available for security information updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-248"><span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**Fehler bei \_ ungültigen \_ Gruppen \_ Attributen.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-248"><span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**ERROR\_INVALID\_GROUP\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-249">1345 (0x541)</span><span class="sxs-lookup"><span data-stu-id="a0bac-249">1345 (0x541)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-250">Die angegebenen Attribute sind ungültig oder nicht kompatibel mit den Attributen für die Gruppe als Ganzes.</span><span class="sxs-lookup"><span data-stu-id="a0bac-250">The specified attributes are invalid, or incompatible with the attributes for the group as a whole.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-251"><span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**fehlerhafte Identitätswechsel \_ \_ \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="a0bac-251"><span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**ERROR\_BAD\_IMPERSONATION\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-252">1346 (0x542)</span><span class="sxs-lookup"><span data-stu-id="a0bac-252">1346 (0x542)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-253">Entweder wurde eine geforderte Identitätswechselebene nicht geliefert, oder die gelieferte Identitätswechselebene ist unzulässig.</span><span class="sxs-lookup"><span data-stu-id="a0bac-253">Either a required impersonation level was not provided, or the provided impersonation level is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-254"><span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**Fehler \_ beim \_ Öffnen von \_ anonym.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-254"><span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ERROR\_CANT\_OPEN\_ANONYMOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-255">1347 (0x543)</span><span class="sxs-lookup"><span data-stu-id="a0bac-255">1347 (0x543)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-256">Ein Sicherheits Token der anonymen Ebene kann nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-256">Cannot open an anonymous level security token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-257"><span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**Fehler \_ hafte \_ Validierungs \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="a0bac-257"><span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**ERROR\_BAD\_VALIDATION\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-258">1348 (0x544)</span><span class="sxs-lookup"><span data-stu-id="a0bac-258">1348 (0x544)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-259">Die angeforderte Validierungs Informations Klasse war ungültig.</span><span class="sxs-lookup"><span data-stu-id="a0bac-259">The validation information class requested was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-260"><span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**fehlerhafter \_ \_ \_ Tokentyp**</span><span class="sxs-lookup"><span data-stu-id="a0bac-260"><span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**ERROR\_BAD\_TOKEN\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-261">1349 (0x545)</span><span class="sxs-lookup"><span data-stu-id="a0bac-261">1349 (0x545)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-262">Der Tokentyp ist für die versuchte Verwendung ungeeignet.</span><span class="sxs-lookup"><span data-stu-id="a0bac-262">The type of the token is inappropriate for its attempted use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-263"><span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**Fehler \_ \_ \_ bei der Sicherheit des \_ Objekts.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-263"><span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**ERROR\_NO\_SECURITY\_ON\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-264">1350 (0x546)</span><span class="sxs-lookup"><span data-stu-id="a0bac-264">1350 (0x546)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-265">Ein Sicherheits Vorgang für ein Objekt ohne zugeordnete Sicherheit kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-265">Unable to perform a security operation on an object that has no associated security.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-266"><span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**Fehler \_ beim \_ Zugriff auf \_ Domänen \_ Informationen.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-266"><span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**ERROR\_CANT\_ACCESS\_DOMAIN\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-267">1351 (0x547)</span><span class="sxs-lookup"><span data-stu-id="a0bac-267">1351 (0x547)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-268">Die Konfigurationsinformationen konnten nicht vom Domänen Controller gelesen werden, weil der Computer nicht verfügbar ist oder der Zugriff verweigert wurde.</span><span class="sxs-lookup"><span data-stu-id="a0bac-268">Configuration information could not be read from the domain controller, either because the machine is unavailable, or access has been denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-269"><span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**Fehler \_ ungültiger \_ Server \_ Status**</span><span class="sxs-lookup"><span data-stu-id="a0bac-269"><span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**ERROR\_INVALID\_SERVER\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-270">1352 (0x548)</span><span class="sxs-lookup"><span data-stu-id="a0bac-270">1352 (0x548)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-271">Der Sicherheits Konto-Manager (Sam) oder der lokale Sicherheits Autorität (Local Security Authority, LSA) befand sich im falschen Zustand, um den Sicherheits Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-271">The security account manager (SAM) or local security authority (LSA) server was in the wrong state to perform the security operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-272"><span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**\_ungültiger \_ Domänen \_ Status**</span><span class="sxs-lookup"><span data-stu-id="a0bac-272"><span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**ERROR\_INVALID\_DOMAIN\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-273">1353 (0x549)</span><span class="sxs-lookup"><span data-stu-id="a0bac-273">1353 (0x549)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-274">Die Domäne befand sich im falschen Zustand, um den Sicherheits Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-274">The domain was in the wrong state to perform the security operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-275"><span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**\_ungültige \_ Domänen \_ Rolle.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-275"><span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**ERROR\_INVALID\_DOMAIN\_ROLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-276">1354 (0x54A)</span><span class="sxs-lookup"><span data-stu-id="a0bac-276">1354 (0x54A)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-277">Dieser Vorgang ist nur für den primären Domänen Controller der Domäne zulässig.</span><span class="sxs-lookup"><span data-stu-id="a0bac-277">This operation is only allowed for the Primary Domain Controller of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-278"><span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**Fehler bei \_ keiner \_ solchen \_ Domäne**</span><span class="sxs-lookup"><span data-stu-id="a0bac-278"><span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**ERROR\_NO\_SUCH\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-279">1355 (0x54b)</span><span class="sxs-lookup"><span data-stu-id="a0bac-279">1355 (0x54B)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-280">Die angegebene Domäne ist entweder nicht vorhanden, oder es konnte keine Verbindung mit ihr hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-280">The specified domain either does not exist or could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-281"><span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**Fehler \_ Domäne \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="a0bac-281"><span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**ERROR\_DOMAIN\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-282">1356 (0x54C)</span><span class="sxs-lookup"><span data-stu-id="a0bac-282">1356 (0x54C)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-283">Die angegebene Domäne ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-283">The specified domain already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-284"><span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**Fehler \_ Domänen \_ Limit \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="a0bac-284"><span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**ERROR\_DOMAIN\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-285">1357 (0x54d)</span><span class="sxs-lookup"><span data-stu-id="a0bac-285">1357 (0x54D)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-286">Es wurde versucht, den Grenzwert für die Anzahl von Domänen pro Server zu überschreiten.</span><span class="sxs-lookup"><span data-stu-id="a0bac-286">An attempt was made to exceed the limit on the number of domains per server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-287"><span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**Fehler bei \_ interner \_ DB- \_ Datenbank.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-287"><span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**ERROR\_INTERNAL\_DB\_CORRUPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-288">1358 (0x54e)</span><span class="sxs-lookup"><span data-stu-id="a0bac-288">1358 (0x54E)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-289">Der angeforderte Vorgang kann aufgrund eines schwerwiegenden Medien Fehlers oder einer Beschädigung der Datenstruktur auf dem Datenträger nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-289">Unable to complete the requested operation because of either a catastrophic media failure or a data structure corruption on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-290"><span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**\_Interner Fehler \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-290"><span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**ERROR\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-291">1359 (0x54f)</span><span class="sxs-lookup"><span data-stu-id="a0bac-291">1359 (0x54F)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-292">Interner Fehler.</span><span class="sxs-lookup"><span data-stu-id="a0bac-292">An internal error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-293"><span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**Fehler \_ generisch \_ nicht \_ zugeordnet**</span><span class="sxs-lookup"><span data-stu-id="a0bac-293"><span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**ERROR\_GENERIC\_NOT\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-294">1360 (0x550)</span><span class="sxs-lookup"><span data-stu-id="a0bac-294">1360 (0x550)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-295">Generische Zugriffs Typen waren in einer Zugriffs Maske enthalten, die bereits nicht generischen Typen zugeordnet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="a0bac-295">Generic access types were contained in an access mask which should already be mapped to nongeneric types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-296"><span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**fehlerhaftes \_ \_ \_ deskriptorformat**</span><span class="sxs-lookup"><span data-stu-id="a0bac-296"><span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**ERROR\_BAD\_DESCRIPTOR\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-297">1361 (0x551)</span><span class="sxs-lookup"><span data-stu-id="a0bac-297">1361 (0x551)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-298">Eine Sicherheits Beschreibung weist nicht das richtige Format auf (absolut oder selbst bezogen).</span><span class="sxs-lookup"><span data-stu-id="a0bac-298">A security descriptor is not in the right format (absolute or self-relative).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-299"><span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**Fehler \_ beim \_ Anmelde \_ Vorgang.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-299"><span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**ERROR\_NOT\_LOGON\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-300">1362 (0x552)</span><span class="sxs-lookup"><span data-stu-id="a0bac-300">1362 (0x552)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-301">Die angeforderte Aktion ist nur für die Verwendung durch Anmelde Prozesse eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-301">The requested action is restricted for use by logon processes only.</span></span> <span data-ttu-id="a0bac-302">Der aufrufende Prozess ist nicht als Anmeldevorgang registriert.</span><span class="sxs-lookup"><span data-stu-id="a0bac-302">The calling process has not registered as a logon process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-303"><span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**Fehler \_ Anmelde \_ Sitzung ist \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-303"><span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**ERROR\_LOGON\_SESSION\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-304">1363 (0x553)</span><span class="sxs-lookup"><span data-stu-id="a0bac-304">1363 (0x553)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-305">Es kann keine neue Anmelde Sitzung mit einer bereits verwendeten ID gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-305">Cannot start a new logon session with an ID that is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-306"><span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**Fehler " \_ kein \_ solches \_ Paket"**</span><span class="sxs-lookup"><span data-stu-id="a0bac-306"><span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**ERROR\_NO\_SUCH\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-307">1364 (0x554)</span><span class="sxs-lookup"><span data-stu-id="a0bac-307">1364 (0x554)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-308">Ein angegebenes Authentifizierungs Paket ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-308">A specified authentication package is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-309"><span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**Fehler bei fehlerhafter \_ \_ Anmelde \_ Sitzung \_ .**</span><span class="sxs-lookup"><span data-stu-id="a0bac-309"><span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**ERROR\_BAD\_LOGON\_SESSION\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-310">1365 (0x555)</span><span class="sxs-lookup"><span data-stu-id="a0bac-310">1365 (0x555)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-311">Die Anmelde Sitzung befindet sich nicht in einem Zustand, der mit dem angeforderten Vorgang konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="a0bac-311">The logon session is not in a state that is consistent with the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-312"><span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**Fehler beim \_ Protokollierung der \_ Sitzung. \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-312"><span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**ERROR\_LOGON\_SESSION\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-313">1366 (0x556)</span><span class="sxs-lookup"><span data-stu-id="a0bac-313">1366 (0x556)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-314">Die Anmelde Sitzungs-ID wird bereits verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0bac-314">The logon session ID is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-315"><span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**\_ungültiger \_ \_ Anmeldetyp.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-315"><span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**ERROR\_INVALID\_LOGON\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-316">1367 (0x557)</span><span class="sxs-lookup"><span data-stu-id="a0bac-316">1367 (0x557)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-317">Eine Anmelde Anforderung enthielt einen ungültigen anmeldetypwert.</span><span class="sxs-lookup"><span data-stu-id="a0bac-317">A logon request contained an invalid logon type value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-318"><span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**Fehler beim Annehmen der Identität \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-318"><span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**ERROR\_CANNOT\_IMPERSONATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-319">1368 (0x558)</span><span class="sxs-lookup"><span data-stu-id="a0bac-319">1368 (0x558)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-320">Die Identität kann nicht mithilfe einer Named Pipe angenommen werden, bis die Daten aus dieser Pipe gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-320">Unable to impersonate using a named pipe until data has been read from that pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-321"><span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**Fehler " \_ rxact" ist \_ ungültig. \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-321"><span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**ERROR\_RXACT\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-322">1369 (0x559)</span><span class="sxs-lookup"><span data-stu-id="a0bac-322">1369 (0x559)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-323">Der Transaktionsstatus einer Registrierungs Unterstruktur ist mit dem angeforderten Vorgang nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a0bac-323">The transaction state of a registry subtree is incompatible with the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-324"><span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**Fehler beim \_ rxact- \_ Commit. \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-324"><span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**ERROR\_RXACT\_COMMIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-325">1370 (0x55a)</span><span class="sxs-lookup"><span data-stu-id="a0bac-325">1370 (0x55A)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-326">Es ist eine interne Beschädigung der Sicherheitsdatenbank aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a0bac-326">An internal security database corruption has been encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-327"><span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**\_Sonderkonto für Fehler \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-327"><span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**ERROR\_SPECIAL\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-328">1371 (0x55b)</span><span class="sxs-lookup"><span data-stu-id="a0bac-328">1371 (0x55B)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-329">Dieser Vorgang kann nicht für integrierte Konten durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-329">Cannot perform this operation on built-in accounts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-330"><span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**Fehler \_ spezielle \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="a0bac-330"><span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**ERROR\_SPECIAL\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-331">1372 (0x55c)</span><span class="sxs-lookup"><span data-stu-id="a0bac-331">1372 (0x55C)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-332">Dieser Vorgang kann für diese integrierte spezielle Gruppe nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-332">Cannot perform this operation on this built-in special group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-333"><span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**\_spezieller Fehler \_ Benutzer**</span><span class="sxs-lookup"><span data-stu-id="a0bac-333"><span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**ERROR\_SPECIAL\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-334">1373 (0x55D)</span><span class="sxs-lookup"><span data-stu-id="a0bac-334">1373 (0x55D)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-335">Dieser Vorgang kann für diesen integrierten speziellen Benutzer nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-335">Cannot perform this operation on this built-in special user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-336"><span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**Fehler \_ Mitglieder \_ primäre \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="a0bac-336"><span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**ERROR\_MEMBERS\_PRIMARY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-337">1374 (0x55E)</span><span class="sxs-lookup"><span data-stu-id="a0bac-337">1374 (0x55E)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-338">Der Benutzer kann nicht aus einer Gruppe entfernt werden, da es sich bei der Gruppe derzeit um die primäre Gruppe des Benutzers handelt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-338">The user cannot be removed from a group because the group is currently the user's primary group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-339"><span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**das Fehler \_ Token wird \_ bereits \_ \_ verwendet.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-339"><span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**ERROR\_TOKEN\_ALREADY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-340">1375 (0x55f)</span><span class="sxs-lookup"><span data-stu-id="a0bac-340">1375 (0x55F)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-341">Das Token wird bereits als primäres Token verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0bac-341">The token is already in use as a primary token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-342"><span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**Fehler " \_ kein \_ solcher \_ Alias"**</span><span class="sxs-lookup"><span data-stu-id="a0bac-342"><span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**ERROR\_NO\_SUCH\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-343">1376 (0x560)</span><span class="sxs-lookup"><span data-stu-id="a0bac-343">1376 (0x560)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-344">Die angegebene lokale Gruppe ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-344">The specified local group does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-345"><span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**\_fehlermember \_ nicht \_ im \_ Alias**</span><span class="sxs-lookup"><span data-stu-id="a0bac-345"><span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**ERROR\_MEMBER\_NOT\_IN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-346">1377 (0x561)</span><span class="sxs-lookup"><span data-stu-id="a0bac-346">1377 (0x561)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-347">Der angegebene Kontoname ist kein Mitglied der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a0bac-347">The specified account name is not a member of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-348"><span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**\_fehlermember \_ in \_ Alias**</span><span class="sxs-lookup"><span data-stu-id="a0bac-348"><span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**ERROR\_MEMBER\_IN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-349">1378 (0x562)</span><span class="sxs-lookup"><span data-stu-id="a0bac-349">1378 (0x562)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-350">Der angegebene Kontoname ist bereits Mitglied der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a0bac-350">The specified account name is already a member of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-351"><span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**\_fehleralias \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="a0bac-351"><span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**ERROR\_ALIAS\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-352">1379 (0x563)</span><span class="sxs-lookup"><span data-stu-id="a0bac-352">1379 (0x563)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-353">Die angegebene lokale Gruppe ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-353">The specified local group already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-354"><span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**Fehler \_ Anmeldung \_ nicht \_ erteilt**</span><span class="sxs-lookup"><span data-stu-id="a0bac-354"><span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**ERROR\_LOGON\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-355">1380 (0x564)</span><span class="sxs-lookup"><span data-stu-id="a0bac-355">1380 (0x564)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-356">Anmeldefehler: dem Benutzer wurde der angeforderte Anmeldetyp auf diesem Computer nicht erteilt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-356">Logon failure: the user has not been granted the requested logon type at this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-357"><span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**Fehler bei \_ zu \_ vielen \_ geheimen Schlüsseln.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-357"><span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**ERROR\_TOO\_MANY\_SECRETS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-358">1381 (0x565)</span><span class="sxs-lookup"><span data-stu-id="a0bac-358">1381 (0x565)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-359">Die maximale Anzahl von Geheimnissen, die in einem einzelnen System gespeichert werden können, wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="a0bac-359">The maximum number of secrets that may be stored in a single system has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-360"><span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**Fehler \_ Geheimnis \_ zu \_ lang**</span><span class="sxs-lookup"><span data-stu-id="a0bac-360"><span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**ERROR\_SECRET\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-361">1382 (0x566)</span><span class="sxs-lookup"><span data-stu-id="a0bac-361">1382 (0x566)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-362">Die Länge eines geheimen Schlüssels überschreitet die maximal zulässige Länge.</span><span class="sxs-lookup"><span data-stu-id="a0bac-362">The length of a secret exceeds the maximum length allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-363"><span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**Fehler \_ interner \_ DB- \_ Fehler.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-363"><span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**ERROR\_INTERNAL\_DB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-364">1383 (0x567)</span><span class="sxs-lookup"><span data-stu-id="a0bac-364">1383 (0x567)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-365">Die Datenbank der lokalen Sicherheits Autorität enthält interne Inkonsistenzen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-365">The local security authority database contains an internal inconsistency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-366"><span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**Fehler \_ zu \_ viele \_ Kontext- \_ IDs.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-366"><span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**ERROR\_TOO\_MANY\_CONTEXT\_IDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-367">1384 (0x568)</span><span class="sxs-lookup"><span data-stu-id="a0bac-367">1384 (0x568)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-368">Während eines Anmelde Versuchs hat der Sicherheitskontext des Benutzers zu viele Sicherheits-IDs gesammelt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-368">During a logon attempt, the user's security context accumulated too many security IDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-369"><span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**Fehler \_ \_ Anmeldetyp \_ nicht \_ erteilt**</span><span class="sxs-lookup"><span data-stu-id="a0bac-369"><span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**ERROR\_LOGON\_TYPE\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-370">1385 (0x569)</span><span class="sxs-lookup"><span data-stu-id="a0bac-370">1385 (0x569)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-371">Anmeldefehler: dem Benutzer wurde der angeforderte Anmeldetyp auf diesem Computer nicht erteilt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-371">Logon failure: the user has not been granted the requested logon type at this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-372"><span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**Fehler bei \_ NT- \_ Kreuz \_ Verschlüsselung \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="a0bac-372"><span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**ERROR\_NT\_CROSS\_ENCRYPTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-373">1386 (0x56A)</span><span class="sxs-lookup"><span data-stu-id="a0bac-373">1386 (0x56A)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-374">Ein Kreuz verschlüsseltes Kennwort ist erforderlich, um ein Benutzer Kennwort zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a0bac-374">A cross-encrypted password is necessary to change a user password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-375"><span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**Fehler " \_ kein \_ solcher \_ Member"**</span><span class="sxs-lookup"><span data-stu-id="a0bac-375"><span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**ERROR\_NO\_SUCH\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-376">1387 (0x56B)</span><span class="sxs-lookup"><span data-stu-id="a0bac-376">1387 (0x56B)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-377">Ein Mitglied konnte der lokalen Gruppe nicht hinzugefügt oder daraus entfernt werden, da das Element nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a0bac-377">A member could not be added to or removed from the local group because the member does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-378"><span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**\_ungültiger \_ Member**</span><span class="sxs-lookup"><span data-stu-id="a0bac-378"><span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**ERROR\_INVALID\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-379">1388 (0x56C)</span><span class="sxs-lookup"><span data-stu-id="a0bac-379">1388 (0x56C)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-380">Ein neuer Member konnte einer lokalen Gruppe nicht hinzugefügt werden, weil der Member den falschen Kontotyp aufweist.</span><span class="sxs-lookup"><span data-stu-id="a0bac-380">A new member could not be added to a local group because the member has the wrong account type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-381"><span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**Fehler \_ zu \_ viele \_ SIDs.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-381"><span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**ERROR\_TOO\_MANY\_SIDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-382">1389 (0x56D)</span><span class="sxs-lookup"><span data-stu-id="a0bac-382">1389 (0x56D)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-383">Es wurden zu viele Sicherheits-IDs angegeben.</span><span class="sxs-lookup"><span data-stu-id="a0bac-383">Too many security IDs have been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-384"><span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**Fehler \_ LM- \_ Kreuz \_ Verschlüsselung \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="a0bac-384"><span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**ERROR\_LM\_CROSS\_ENCRYPTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-385">1390 (0x56E)</span><span class="sxs-lookup"><span data-stu-id="a0bac-385">1390 (0x56E)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-386">Ein Kreuz verschlüsseltes Kennwort ist erforderlich, um dieses Benutzer Kennwort zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a0bac-386">A cross-encrypted password is necessary to change this user password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-387"><span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**Fehler \_ keine \_ Vererbung**</span><span class="sxs-lookup"><span data-stu-id="a0bac-387"><span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**ERROR\_NO\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-388">1391 (0x56f)</span><span class="sxs-lookup"><span data-stu-id="a0bac-388">1391 (0x56F)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-389">Gibt an, dass eine ACL keine vererbbaren Komponenten enthält.</span><span class="sxs-lookup"><span data-stu-id="a0bac-389">Indicates an ACL contains no inheritable components.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-390"><span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**Fehler \_ Datei \_ beschädigt**</span><span class="sxs-lookup"><span data-stu-id="a0bac-390"><span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**ERROR\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-391">1392 (0x570)</span><span class="sxs-lookup"><span data-stu-id="a0bac-391">1392 (0x570)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-392">Die Datei oder das Verzeichnis ist beschädigt und kann nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-392">The file or directory is corrupted and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-393"><span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**Fehler Datenträger \_ \_ beschädigt**</span><span class="sxs-lookup"><span data-stu-id="a0bac-393"><span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**ERROR\_DISK\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-394">1393 (0x571)</span><span class="sxs-lookup"><span data-stu-id="a0bac-394">1393 (0x571)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-395">Die Datenträger Struktur ist beschädigt und kann nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-395">The disk structure is corrupted and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-396"><span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**Fehler " \_ kein \_ Benutzer \_ Sitzungs \_ Schlüssel"**</span><span class="sxs-lookup"><span data-stu-id="a0bac-396"><span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**ERROR\_NO\_USER\_SESSION\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-397">1394 (0x572)</span><span class="sxs-lookup"><span data-stu-id="a0bac-397">1394 (0x572)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-398">Es ist kein Benutzer Sitzungsschlüssel für die angegebene Anmelde Sitzung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-398">There is no user session key for the specified logon session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-399"><span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**Fehler \_ Lizenz \_ Kontingent \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="a0bac-399"><span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**ERROR\_LICENSE\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-400">1395 (0x573)</span><span class="sxs-lookup"><span data-stu-id="a0bac-400">1395 (0x573)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-401">Der Dienst, auf den zugegriffen wird, ist für eine bestimmte Anzahl von Verbindungen lizenziert.</span><span class="sxs-lookup"><span data-stu-id="a0bac-401">The service being accessed is licensed for a particular number of connections.</span></span> <span data-ttu-id="a0bac-402">Zurzeit können keine weiteren Verbindungen mit dem Dienst hergestellt werden, da bereits so viele Verbindungen vorhanden sind, wie der Dienst annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="a0bac-402">No more connections can be made to the service at this time because there are already as many connections as the service can accept.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-403"><span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**\_falscher \_ \_ Zielname für Fehler**</span><span class="sxs-lookup"><span data-stu-id="a0bac-403"><span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**ERROR\_WRONG\_TARGET\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-404">1396 (0x574)</span><span class="sxs-lookup"><span data-stu-id="a0bac-404">1396 (0x574)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-405">Der Name des Ziel Kontos ist falsch.</span><span class="sxs-lookup"><span data-stu-id="a0bac-405">The target account name is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-406"><span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**Fehler bei \_ gegenseitiger Authentifizierung \_ . \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-406"><span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**ERROR\_MUTUAL\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-407">1397 (0x575)</span><span class="sxs-lookup"><span data-stu-id="a0bac-407">1397 (0x575)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-408">Gegenseitige Authentifizierung ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-408">Mutual Authentication failed.</span></span> <span data-ttu-id="a0bac-409">Das Server Kennwort ist auf dem Domänen Controller veraltet.</span><span class="sxs-lookup"><span data-stu-id="a0bac-409">The server's password is out of date at the domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-410"><span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**Fehler \_ Zeit \_ Abweichung**</span><span class="sxs-lookup"><span data-stu-id="a0bac-410"><span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**ERROR\_TIME\_SKEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-411">1398 (0x576)</span><span class="sxs-lookup"><span data-stu-id="a0bac-411">1398 (0x576)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-412">Zwischen dem Client und dem Server liegt ein Zeit-und/oder Datums Unterschied vor.</span><span class="sxs-lookup"><span data-stu-id="a0bac-412">There is a time and/or date difference between the client and server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-413"><span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**Fehler die \_ aktuelle \_ Domäne ist \_ nicht \_ zulässig.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-413"><span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**ERROR\_CURRENT\_DOMAIN\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-414">1399 (0x577)</span><span class="sxs-lookup"><span data-stu-id="a0bac-414">1399 (0x577)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-415">Dieser Vorgang kann für die aktuelle Domäne nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-415">This operation cannot be performed on the current domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-416"><span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**Fehler bei \_ ungültigem \_ Fenster \_ handle.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-416"><span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**ERROR\_INVALID\_WINDOW\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-417">1400 (0x578)</span><span class="sxs-lookup"><span data-stu-id="a0bac-417">1400 (0x578)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-418">Ungültiges Fenster handle.</span><span class="sxs-lookup"><span data-stu-id="a0bac-418">Invalid window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-419"><span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**Fehler bei \_ ungültigem \_ Menü \_ handle.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-419"><span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**ERROR\_INVALID\_MENU\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-420">1401 (0x579)</span><span class="sxs-lookup"><span data-stu-id="a0bac-420">1401 (0x579)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-421">Ungültiges Menü handle.</span><span class="sxs-lookup"><span data-stu-id="a0bac-421">Invalid menu handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-422"><span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**Fehler bei \_ ungültigem \_ Cursor \_ handle.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-422"><span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**ERROR\_INVALID\_CURSOR\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-423">1402 (0x57A)</span><span class="sxs-lookup"><span data-stu-id="a0bac-423">1402 (0x57A)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-424">Ungültiges Cursor handle.</span><span class="sxs-lookup"><span data-stu-id="a0bac-424">Invalid cursor handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-425"><span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**\_ungültiger \_ Accel- \_ handle.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-425"><span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**ERROR\_INVALID\_ACCEL\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-426">1403 (0x57B)</span><span class="sxs-lookup"><span data-stu-id="a0bac-426">1403 (0x57B)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-427">Ungültiges Zugriffstasten-Tabellen handle.</span><span class="sxs-lookup"><span data-stu-id="a0bac-427">Invalid accelerator table handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-428"><span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**Fehler \_ ungültiges \_ Hook- \_ handle.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-428"><span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**ERROR\_INVALID\_HOOK\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-429">1404 (0x57c)</span><span class="sxs-lookup"><span data-stu-id="a0bac-429">1404 (0x57C)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-430">Ungültiges Hook-handle.</span><span class="sxs-lookup"><span data-stu-id="a0bac-430">Invalid hook handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-431"><span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**\_ungültiger \_ DWP- \_ handle.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-431"><span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**ERROR\_INVALID\_DWP\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-432">1405 (0x57D)</span><span class="sxs-lookup"><span data-stu-id="a0bac-432">1405 (0x57D)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-433">Ungültiges Handle für eine Positions Struktur mit mehreren Fenstern.</span><span class="sxs-lookup"><span data-stu-id="a0bac-433">Invalid handle to a multiple-window position structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-434"><span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**Fehler- \_ TLW \_ mit \_ wschild**</span><span class="sxs-lookup"><span data-stu-id="a0bac-434"><span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**ERROR\_TLW\_WITH\_WSCHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-435">1406 (0x57e)</span><span class="sxs-lookup"><span data-stu-id="a0bac-435">1406 (0x57E)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-436">Ein untergeordnetes Fenster der obersten Ebene kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-436">Cannot create a top-level child window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-437"><span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**Fehler \_ beim \_ Suchen der \_ WND- \_ Klasse.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-437"><span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**ERROR\_CANNOT\_FIND\_WND\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-438">1407 (0x57f)</span><span class="sxs-lookup"><span data-stu-id="a0bac-438">1407 (0x57F)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-439">Die Fenster Klasse kann nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-439">Cannot find window class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-440"><span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**Fehler \_ Fenster \_ des \_ anderen \_ Threads**</span><span class="sxs-lookup"><span data-stu-id="a0bac-440"><span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**ERROR\_WINDOW\_OF\_OTHER\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-441">1408 (0x580)</span><span class="sxs-lookup"><span data-stu-id="a0bac-441">1408 (0x580)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-442">Ungültiges Fenster Sie gehört zu einem anderen Thread.</span><span class="sxs-lookup"><span data-stu-id="a0bac-442">Invalid window; it belongs to other thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-443"><span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**Fehler \_ Hotkey \_ bereits \_ registriert**</span><span class="sxs-lookup"><span data-stu-id="a0bac-443"><span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**ERROR\_HOTKEY\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-444">1409 (0x581)</span><span class="sxs-lookup"><span data-stu-id="a0bac-444">1409 (0x581)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-445">Die Hot-Taste ist bereits registriert.</span><span class="sxs-lookup"><span data-stu-id="a0bac-445">Hot key is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-446"><span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**die Fehler \_ Klasse ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-446"><span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**ERROR\_CLASS\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-447">1410 (0x582)</span><span class="sxs-lookup"><span data-stu-id="a0bac-447">1410 (0x582)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-448">Die Klasse ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-448">Class already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-449"><span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**die Fehler \_ Klasse \_ ist \_ nicht \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-449"><span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**ERROR\_CLASS\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-450">1411 (0x583)</span><span class="sxs-lookup"><span data-stu-id="a0bac-450">1411 (0x583)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-451">Die Klasse ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-451">Class does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-452"><span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**Error- \_ Klasse \_ hat \_ Windows**</span><span class="sxs-lookup"><span data-stu-id="a0bac-452"><span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**ERROR\_CLASS\_HAS\_WINDOWS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-453">1412 (0x584)</span><span class="sxs-lookup"><span data-stu-id="a0bac-453">1412 (0x584)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-454">Die Klasse hat weiterhin geöffnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="a0bac-454">Class still has open windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-455"><span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**\_ungültiger \_ Index**</span><span class="sxs-lookup"><span data-stu-id="a0bac-455"><span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**ERROR\_INVALID\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-456">1413 (0x585)</span><span class="sxs-lookup"><span data-stu-id="a0bac-456">1413 (0x585)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-457">Ungültiger Index.</span><span class="sxs-lookup"><span data-stu-id="a0bac-457">Invalid index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-458"><span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**Fehler bei \_ ungültigem \_ Symbol \_ handle.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-458"><span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**ERROR\_INVALID\_ICON\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-459">1414 (0x586)</span><span class="sxs-lookup"><span data-stu-id="a0bac-459">1414 (0x586)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-460">Ungültiges Symbol handle.</span><span class="sxs-lookup"><span data-stu-id="a0bac-460">Invalid icon handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-461"><span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**Fehler beim \_ privaten \_ Dialog Feld \_ Index**</span><span class="sxs-lookup"><span data-stu-id="a0bac-461"><span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**ERROR\_PRIVATE\_DIALOG\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-462">1415 (0x587)</span><span class="sxs-lookup"><span data-stu-id="a0bac-462">1415 (0x587)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-463">Verwenden von privaten Dialog Feld Fenster Wörtern.</span><span class="sxs-lookup"><span data-stu-id="a0bac-463">Using private DIALOG window words.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-464"><span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**Fehler \_ ListBox- \_ ID wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-464"><span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**ERROR\_LISTBOX\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-465">1416 (0x588)</span><span class="sxs-lookup"><span data-stu-id="a0bac-465">1416 (0x588)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-466">Der Listenfeld Bezeichner wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-466">The list box identifier was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-467"><span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**Fehler \_ keine Platzhalter \_ \_ Zeichen**</span><span class="sxs-lookup"><span data-stu-id="a0bac-467"><span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**ERROR\_NO\_WILDCARD\_CHARACTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-468">1417 (0x589)</span><span class="sxs-lookup"><span data-stu-id="a0bac-468">1417 (0x589)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-469">Es wurden keine Platzhalter gefunden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-469">No wildcards were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-470"><span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**Fehler \_ Zwischenablage \_ nicht \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="a0bac-470"><span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**ERROR\_CLIPBOARD\_NOT\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-471">1418 (0x58a)</span><span class="sxs-lookup"><span data-stu-id="a0bac-471">1418 (0x58A)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-472">Für den Thread ist keine Zwischenablage geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a0bac-472">Thread does not have a clipboard open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-473"><span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**Fehler \_ Hotkey \_ nicht \_ registriert**</span><span class="sxs-lookup"><span data-stu-id="a0bac-473"><span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**ERROR\_HOTKEY\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-474">1419 (0x58b)</span><span class="sxs-lookup"><span data-stu-id="a0bac-474">1419 (0x58B)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-475">Die Hot-Taste ist nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="a0bac-475">Hot key is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-476"><span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**Fehler \_ Fenster \_ nicht \_ Dialogfeld**</span><span class="sxs-lookup"><span data-stu-id="a0bac-476"><span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**ERROR\_WINDOW\_NOT\_DIALOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-477">1420 (0x58c)</span><span class="sxs-lookup"><span data-stu-id="a0bac-477">1420 (0x58C)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-478">Das Fenster ist kein gültiges Dialogfeld Fenster.</span><span class="sxs-lookup"><span data-stu-id="a0bac-478">The window is not a valid dialog window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-479"><span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**Fehler \_ Steuerungs- \_ ID wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-479"><span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**ERROR\_CONTROL\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-480">1421 (0x58d)</span><span class="sxs-lookup"><span data-stu-id="a0bac-480">1421 (0x58D)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-481">Die Kontroll-ID wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-481">Control ID not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-482"><span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**Fehler \_ ungültige \_ ComboBox- \_ Nachricht.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-482"><span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**ERROR\_INVALID\_COMBOBOX\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-483">1422 (0x58e)</span><span class="sxs-lookup"><span data-stu-id="a0bac-483">1422 (0x58E)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-484">Ungültige Meldung für ein Kombinations Feld, weil Sie nicht über ein Bearbeitungs Steuerelement verfügt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-484">Invalid message for a combo box because it does not have an edit control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-485"><span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**Fehler \_ Fenster \_ nicht \_ ComboBox**</span><span class="sxs-lookup"><span data-stu-id="a0bac-485"><span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**ERROR\_WINDOW\_NOT\_COMBOBOX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-486">1423 (0x58f)</span><span class="sxs-lookup"><span data-stu-id="a0bac-486">1423 (0x58F)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-487">Das Fenster ist kein Kombinations Feld.</span><span class="sxs-lookup"><span data-stu-id="a0bac-487">The window is not a combo box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-488"><span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**Fehler \_ beim \_ Bearbeiten der \_ Höhe.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-488"><span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**ERROR\_INVALID\_EDIT\_HEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-489">1424 (0x590)</span><span class="sxs-lookup"><span data-stu-id="a0bac-489">1424 (0x590)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-490">Die Höhe muss kleiner als 256 sein.</span><span class="sxs-lookup"><span data-stu-id="a0bac-490">Height must be less than 256.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-491"><span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**Fehler Domänen Controller \_ \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="a0bac-491"><span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**ERROR\_DC\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-492">1425 (0x591)</span><span class="sxs-lookup"><span data-stu-id="a0bac-492">1425 (0x591)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-493">Ungültiges Handle des Geräte Kontexts (DC).</span><span class="sxs-lookup"><span data-stu-id="a0bac-493">Invalid device context (DC) handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-494"><span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**\_ungültiger \_ Hook- \_ Filter**</span><span class="sxs-lookup"><span data-stu-id="a0bac-494"><span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**ERROR\_INVALID\_HOOK\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-495">1426 (0x592)</span><span class="sxs-lookup"><span data-stu-id="a0bac-495">1426 (0x592)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-496">Ungültiger Hook-Prozedurtyp.</span><span class="sxs-lookup"><span data-stu-id="a0bac-496">Invalid hook procedure type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-497"><span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**Fehler \_ ungültige Filter Prozedur. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-497"><span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**ERROR\_INVALID\_FILTER\_PROC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-498">1427 (0x593)</span><span class="sxs-lookup"><span data-stu-id="a0bac-498">1427 (0x593)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-499">Ungültige Hook-Prozedur.</span><span class="sxs-lookup"><span data-stu-id="a0bac-499">Invalid hook procedure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-500"><span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**der Fehler \_ Hook \_ benötigt \_ hMod.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-500"><span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**ERROR\_HOOK\_NEEDS\_HMOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-501">1428 (0x594)</span><span class="sxs-lookup"><span data-stu-id="a0bac-501">1428 (0x594)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-502">Der nicht lokale Hook kann nicht ohne ein Modul handle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-502">Cannot set nonlocal hook without a module handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-503"><span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**Fehler beim globalen reinen Fehler \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-503"><span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**ERROR\_GLOBAL\_ONLY\_HOOK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-504">1429 (0x595)</span><span class="sxs-lookup"><span data-stu-id="a0bac-504">1429 (0x595)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-505">Diese Hook-Prozedur kann nur global festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-505">This hook procedure can only be set globally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-506"><span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**Fehler \_ Journal- \_ Hook- \_ Satz**</span><span class="sxs-lookup"><span data-stu-id="a0bac-506"><span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**ERROR\_JOURNAL\_HOOK\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-507">1430 (0x596)</span><span class="sxs-lookup"><span data-stu-id="a0bac-507">1430 (0x596)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-508">Die Journal Hook-Prozedur ist bereits installiert.</span><span class="sxs-lookup"><span data-stu-id="a0bac-508">The journal hook procedure is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-509"><span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**Fehler \_ Hook \_ nicht \_ installiert**</span><span class="sxs-lookup"><span data-stu-id="a0bac-509"><span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**ERROR\_HOOK\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-510">1431 (0x597)</span><span class="sxs-lookup"><span data-stu-id="a0bac-510">1431 (0x597)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-511">Die Hook-Prozedur ist nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="a0bac-511">The hook procedure is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-512"><span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**Fehler \_ ungültige \_ lb- \_ Nachricht.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-512"><span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**ERROR\_INVALID\_LB\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-513">1432 (0x598)</span><span class="sxs-lookup"><span data-stu-id="a0bac-513">1432 (0x598)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-514">Ungültige Meldung für das Listenfeld für die Einzel Auswahl.</span><span class="sxs-lookup"><span data-stu-id="a0bac-514">Invalid message for single-selection list box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-515"><span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**Fehler \_ bei SetCount bei fehlerhafter \_ \_ \_ lb**</span><span class="sxs-lookup"><span data-stu-id="a0bac-515"><span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**ERROR\_SETCOUNT\_ON\_BAD\_LB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-516">1433 (0x599)</span><span class="sxs-lookup"><span data-stu-id="a0bac-516">1433 (0x599)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-517">\_Die an das nicht verzögerte Listenfeld gesendete lb-SetCount.</span><span class="sxs-lookup"><span data-stu-id="a0bac-517">LB\_SETCOUNT sent to non-lazy list box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-518"><span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**Fehler- \_ lb \_ ohne \_ Tabstopps**</span><span class="sxs-lookup"><span data-stu-id="a0bac-518"><span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**ERROR\_LB\_WITHOUT\_TABSTOPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-519">1434 (0x59a)</span><span class="sxs-lookup"><span data-stu-id="a0bac-519">1434 (0x59A)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-520">Dieses Listenfeld unterstützt keine Tabstopps.</span><span class="sxs-lookup"><span data-stu-id="a0bac-520">This list box does not support tab stops.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-521"><span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**Fehler \_ beim \_ zerstören \_ des Objekts eines \_ anderen \_ Threads.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-521"><span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**ERROR\_DESTROY\_OBJECT\_OF\_OTHER\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-522">1435 (0x59b)</span><span class="sxs-lookup"><span data-stu-id="a0bac-522">1435 (0x59B)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-523">Das von einem anderen Thread erstellte Objekt kann nicht zerstört werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-523">Cannot destroy object created by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-524"><span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**Menü "Fehler untergeordneter \_ \_ Fenster" \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-524"><span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**ERROR\_CHILD\_WINDOW\_MENU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-525">1436 (0x59c)</span><span class="sxs-lookup"><span data-stu-id="a0bac-525">1436 (0x59C)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-526">Untergeordnete Fenster dürfen keine Menüs enthalten.</span><span class="sxs-lookup"><span data-stu-id="a0bac-526">Child windows cannot have menus.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-527"><span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**Fehler " \_ kein \_ System" \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-527"><span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**ERROR\_NO\_SYSTEM\_MENU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-528">1437 (0x59d)</span><span class="sxs-lookup"><span data-stu-id="a0bac-528">1437 (0x59D)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-529">Das Fenster verfügt über kein Systemmenü.</span><span class="sxs-lookup"><span data-stu-id="a0bac-529">The window does not have a system menu.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-530"><span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**\_ungültiger \_ MsgBox- \_ Stil.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-530"><span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**ERROR\_INVALID\_MSGBOX\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-531">1438 (0x59e)</span><span class="sxs-lookup"><span data-stu-id="a0bac-531">1438 (0x59E)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-532">Ungültiger Stil für Meldungs Feld.</span><span class="sxs-lookup"><span data-stu-id="a0bac-532">Invalid message box style.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-533"><span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**\_ungültiger \_ SPI- \_ Wert**</span><span class="sxs-lookup"><span data-stu-id="a0bac-533"><span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**ERROR\_INVALID\_SPI\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-534">1439 (0x59f)</span><span class="sxs-lookup"><span data-stu-id="a0bac-534">1439 (0x59F)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-535">Ungültiger systemweite (SPI \_ \* )-Parameter.</span><span class="sxs-lookup"><span data-stu-id="a0bac-535">Invalid system-wide (SPI\_\*) parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-536"><span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**der Fehler \_ Bildschirm ist \_ bereits \_ gesperrt.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-536"><span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**ERROR\_SCREEN\_ALREADY\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-537">1440 (0x5a0)</span><span class="sxs-lookup"><span data-stu-id="a0bac-537">1440 (0x5A0)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-538">Der Bildschirm ist bereits gesperrt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-538">Screen already locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-539"><span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**Fehler \_ HWNDs \_ verfügen über ein über \_ \_ geordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="a0bac-539"><span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**ERROR\_HWNDS\_HAVE\_DIFF\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-540">1441 (0x5a1)</span><span class="sxs-lookup"><span data-stu-id="a0bac-540">1441 (0x5A1)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-541">Alle Handles für Windows in einer Positions Struktur mit mehreren Fenstern müssen über das gleiche übergeordnete Element verfügen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-541">All handles to windows in a multiple-window position structure must have the same parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-542"><span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**Fehler \_ nicht untergeordnetes \_ \_ Fenster**</span><span class="sxs-lookup"><span data-stu-id="a0bac-542"><span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**ERROR\_NOT\_CHILD\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-543">1442 (0x5a2)</span><span class="sxs-lookup"><span data-stu-id="a0bac-543">1442 (0x5A2)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-544">Das Fenster ist kein untergeordnetes Fenster.</span><span class="sxs-lookup"><span data-stu-id="a0bac-544">The window is not a child window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-545"><span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**Fehler \_ ungültiger \_ GW- \_ Befehl.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-545"><span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**ERROR\_INVALID\_GW\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-546">1443 (0x5a3)</span><span class="sxs-lookup"><span data-stu-id="a0bac-546">1443 (0x5A3)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-547">Ungültiger GW- \_ \* Befehl.</span><span class="sxs-lookup"><span data-stu-id="a0bac-547">Invalid GW\_\* command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-548"><span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**Fehler \_ ungültige \_ Thread- \_ ID.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-548"><span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**ERROR\_INVALID\_THREAD\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-549">1444 (0x5a4)</span><span class="sxs-lookup"><span data-stu-id="a0bac-549">1444 (0x5A4)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-550">Ungültiger Thread Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a0bac-550">Invalid thread identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-551"><span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**\_nicht- \_ MDIChild-Fehler \_ Fenster**</span><span class="sxs-lookup"><span data-stu-id="a0bac-551"><span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**ERROR\_NON\_MDICHILD\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-552">1445 (0x5a5)</span><span class="sxs-lookup"><span data-stu-id="a0bac-552">1445 (0x5A5)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-553">Eine Nachricht kann nicht von einem Fenster verarbeitet werden, das kein MDI-Fenster (Multiple Document Interface) ist.</span><span class="sxs-lookup"><span data-stu-id="a0bac-553">Cannot process a message from a window that is not a multiple document interface (MDI) window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-554"><span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**Fehler- \_ Popup ist \_ bereits \_ aktiv.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-554"><span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**ERROR\_POPUP\_ALREADY\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-555">1446 (0x5a6)</span><span class="sxs-lookup"><span data-stu-id="a0bac-555">1446 (0x5A6)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-556">Das Popup Menü ist bereits aktiv.</span><span class="sxs-lookup"><span data-stu-id="a0bac-556">Popup menu already active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-557"><span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**Fehler \_ keine \_ Scrollleisten**</span><span class="sxs-lookup"><span data-stu-id="a0bac-557"><span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**ERROR\_NO\_SCROLLBARS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-558">1447 (0x5a7)</span><span class="sxs-lookup"><span data-stu-id="a0bac-558">1447 (0x5A7)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-559">Das Fenster verfügt über keine Scrollleisten.</span><span class="sxs-lookup"><span data-stu-id="a0bac-559">The window does not have scroll bars.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-560"><span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**\_ungültiger \_ ScrollBar- \_ Bereich.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-560"><span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**ERROR\_INVALID\_SCROLLBAR\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-561">1448 (0x5a8)</span><span class="sxs-lookup"><span data-stu-id="a0bac-561">1448 (0x5A8)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-562">Der Schiebe Leistenbereich darf nicht größer sein als MAXLONG.</span><span class="sxs-lookup"><span data-stu-id="a0bac-562">Scroll bar range cannot be greater than MAXLONG.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-563"><span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**Fehler \_ ungültiger \_ ShowWin- \_ Befehl.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-563"><span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**ERROR\_INVALID\_SHOWWIN\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-564">1449 (0x5a9)</span><span class="sxs-lookup"><span data-stu-id="a0bac-564">1449 (0x5A9)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-565">Das Fenster kann nicht in der angegebenen Weise angezeigt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-565">Cannot show or remove the window in the way specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-566"><span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**Fehler \_ keine \_ System \_ Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="a0bac-566"><span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**ERROR\_NO\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-567">1450 (0x5aa)</span><span class="sxs-lookup"><span data-stu-id="a0bac-567">1450 (0x5AA)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-568">Es sind nicht genügend Systemressourcen vorhanden, um den angeforderten Dienst abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-568">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-569"><span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**nicht auslagerbare \_ \_ System \_ Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="a0bac-569"><span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**ERROR\_NONPAGED\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-570">1451 (0x5ab)</span><span class="sxs-lookup"><span data-stu-id="a0bac-570">1451 (0x5AB)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-571">Es sind nicht genügend Systemressourcen vorhanden, um den angeforderten Dienst abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-571">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-572"><span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**Fehler beim auslageres \_ \_ System \_ Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-572"><span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**ERROR\_PAGED\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-573">1452 (0x5ac)</span><span class="sxs-lookup"><span data-stu-id="a0bac-573">1452 (0x5AC)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-574">Es sind nicht genügend Systemressourcen vorhanden, um den angeforderten Dienst abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-574">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-575"><span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**Fehler beim \_ Arbeits \_ Satz \_ Kontingent.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-575"><span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**ERROR\_WORKING\_SET\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-576">1453 (0x5ad)</span><span class="sxs-lookup"><span data-stu-id="a0bac-576">1453 (0x5AD)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-577">Nicht genügend Kontingent zum Durchführen des angeforderten Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="a0bac-577">Insufficient quota to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-578"><span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**Fehlerseiten \_ Datei- \_ Kontingent**</span><span class="sxs-lookup"><span data-stu-id="a0bac-578"><span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**ERROR\_PAGEFILE\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-579">1454 (0x5ae)</span><span class="sxs-lookup"><span data-stu-id="a0bac-579">1454 (0x5AE)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-580">Nicht genügend Kontingent zum Durchführen des angeforderten Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="a0bac-580">Insufficient quota to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-581"><span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**Fehler \_ Verpflichtungs \_ Limit**</span><span class="sxs-lookup"><span data-stu-id="a0bac-581"><span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**ERROR\_COMMITMENT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-582">1455 (0x5af)</span><span class="sxs-lookup"><span data-stu-id="a0bac-582">1455 (0x5AF)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-583">Die Auslagerungs Datei ist zu klein, um diesen Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-583">The paging file is too small for this operation to complete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-584"><span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**Fehler \_ Menü \_ Element wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-584"><span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**ERROR\_MENU\_ITEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-585">1456 (0x5b0)</span><span class="sxs-lookup"><span data-stu-id="a0bac-585">1456 (0x5B0)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-586">Ein Menü Element wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-586">A menu item was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-587"><span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**Fehler bei \_ ungültigem \_ Tastatur \_ handle.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-587"><span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**ERROR\_INVALID\_KEYBOARD\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-588">1457 (0x5b1)</span><span class="sxs-lookup"><span data-stu-id="a0bac-588">1457 (0x5B1)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-589">Ungültiges Tastaturlayout-handle.</span><span class="sxs-lookup"><span data-stu-id="a0bac-589">Invalid keyboard layout handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-590"><span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**Fehler- \_ Hook- \_ Typ \_ nicht \_ zulässig**</span><span class="sxs-lookup"><span data-stu-id="a0bac-590"><span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**ERROR\_HOOK\_TYPE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-591">1458 (0x5b2)</span><span class="sxs-lookup"><span data-stu-id="a0bac-591">1458 (0x5B2)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-592">Der Hooks ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="a0bac-592">Hook type not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-593"><span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**Fehler \_ erfordert \_ interaktive \_ Fenster Station**</span><span class="sxs-lookup"><span data-stu-id="a0bac-593"><span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**ERROR\_REQUIRES\_INTERACTIVE\_WINDOWSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-594">1459 (0x5b3)</span><span class="sxs-lookup"><span data-stu-id="a0bac-594">1459 (0x5B3)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-595">Für diesen Vorgang ist eine interaktive Fenster Station erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a0bac-595">This operation requires an interactive window station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-596"><span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**Fehler \_ Timeout**</span><span class="sxs-lookup"><span data-stu-id="a0bac-596"><span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**ERROR\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-597">1460 (0x5b4)</span><span class="sxs-lookup"><span data-stu-id="a0bac-597">1460 (0x5B4)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-598">Dieser Vorgang wurde wegen Zeitüberschreitung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a0bac-598">This operation returned because the timeout period expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-599"><span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**Fehler bei \_ ungültigem \_ Monitor \_ handle.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-599"><span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**ERROR\_INVALID\_MONITOR\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-600">1461 (0x5b5)</span><span class="sxs-lookup"><span data-stu-id="a0bac-600">1461 (0x5B5)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-601">Ungültiges Monitor handle.</span><span class="sxs-lookup"><span data-stu-id="a0bac-601">Invalid monitor handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-602"><span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**Fehler \_ hafte \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="a0bac-602"><span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**ERROR\_INCORRECT\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-603">1462 (0x5b6)</span><span class="sxs-lookup"><span data-stu-id="a0bac-603">1462 (0x5B6)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-604">Falsches Größen Argument.</span><span class="sxs-lookup"><span data-stu-id="a0bac-604">Incorrect size argument.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-605"><span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**Fehler- \_ symlink- \_ Klasse \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="a0bac-605"><span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**ERROR\_SYMLINK\_CLASS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-606">1463 (0x5b7)</span><span class="sxs-lookup"><span data-stu-id="a0bac-606">1463 (0x5B7)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-607">Die symbolische Verknüpfung kann nicht befolgt werden, da ihr Typ deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a0bac-607">The symbolic link cannot be followed because its type is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-608"><span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**Fehler \_ symlink \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-608"><span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**ERROR\_SYMLINK\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-609">1464 (0x5b8)</span><span class="sxs-lookup"><span data-stu-id="a0bac-609">1464 (0x5B8)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-610">Diese Anwendung unterstützt nicht den aktuellen Vorgang auf symbolischen Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-610">This application does not support the current operation on symbolic links.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-611"><span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**Fehler beim \_ Analysieren der XML-Analyse. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-611"><span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**ERROR\_XML\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-612">1465 (0x5b9)</span><span class="sxs-lookup"><span data-stu-id="a0bac-612">1465 (0x5B9)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-613">Die angeforderten XML-Daten konnten von Windows nicht analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-613">Windows was unable to parse the requested XML data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-614"><span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**Fehler bei \_ XMLDSIG. \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-614"><span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**ERROR\_XMLDSIG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-615">1466 (0x5ba)</span><span class="sxs-lookup"><span data-stu-id="a0bac-615">1466 (0x5BA)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-616">Fehler beim Verarbeiten einer digitalen XML-Signatur.</span><span class="sxs-lookup"><span data-stu-id="a0bac-616">An error was encountered while processing an XML digital signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-617"><span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**Fehler beim \_ Neustart der \_ Anwendung**</span><span class="sxs-lookup"><span data-stu-id="a0bac-617"><span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**ERROR\_RESTART\_APPLICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-618">1467 (0x5bb)</span><span class="sxs-lookup"><span data-stu-id="a0bac-618">1467 (0x5BB)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-619">Diese Anwendung muss neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-619">This application must be restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-620"><span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**Fehler beim \_ falschen Depot \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-620"><span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**ERROR\_WRONG\_COMPARTMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-621">1468 (0x5bc)</span><span class="sxs-lookup"><span data-stu-id="a0bac-621">1468 (0x5BC)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-622">Der Aufrufer hat die Verbindungsanforderung im falschen Routing Depot vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-622">The caller made the connection request in the wrong routing compartment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-623"><span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**Fehler \_ AuthIP- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="a0bac-623"><span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**ERROR\_AUTHIP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-624">1469 (0x5bd)</span><span class="sxs-lookup"><span data-stu-id="a0bac-624">1469 (0x5BD)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-625">AuthIP-Fehler beim Versuch, eine Verbindung mit dem Remote Host herzustellen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-625">There was an AuthIP failure when attempting to connect to the remote host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-626"><span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**Fehler \_ keine \_ NVRAM- \_ Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="a0bac-626"><span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**ERROR\_NO\_NVRAM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-627">1470 (0x5be)</span><span class="sxs-lookup"><span data-stu-id="a0bac-627">1470 (0x5BE)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-628">Für den angeforderten Dienst sind nicht genügend NVRAM-Ressourcen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-628">Insufficient NVRAM resources exist to complete the requested service.</span></span> <span data-ttu-id="a0bac-629">Möglicherweise ist ein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a0bac-629">A reboot might be required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-630"><span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**Fehler \_ nicht \_ GUI- \_ Prozess**</span><span class="sxs-lookup"><span data-stu-id="a0bac-630"><span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**ERROR\_NOT\_GUI\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-631">1471 (0x5bf)</span><span class="sxs-lookup"><span data-stu-id="a0bac-631">1471 (0x5BF)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-632">Der angeforderte Vorgang kann nicht abgeschlossen werden, da es sich beim angegebenen Prozess nicht um einen GUI-Prozess handelt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-632">Unable to finish the requested operation because the specified process is not a GUI process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-633"><span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**fehlerhafte \_ Ereignisprotokoll \_ Datei \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-633"><span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**ERROR\_EVENTLOG\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-634">1500 (0x5dc)</span><span class="sxs-lookup"><span data-stu-id="a0bac-634">1500 (0x5DC)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-635">Die Ereignisprotokoll Datei ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-635">The event log file is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-636"><span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**Fehler beim \_ Starten von EventLog. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-636"><span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**ERROR\_EVENTLOG\_CANT\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-637">1501 (0x5dd)</span><span class="sxs-lookup"><span data-stu-id="a0bac-637">1501 (0x5DD)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-638">Es konnte keine Ereignisprotokoll Datei geöffnet werden, sodass der Ereignis Protokollierungs Dienst nicht gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="a0bac-638">No event log file could be opened, so the event logging service did not start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-639"><span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**Fehler \_ Protokoll \_ Datei \_ voll**</span><span class="sxs-lookup"><span data-stu-id="a0bac-639"><span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**ERROR\_LOG\_FILE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-640">1502 (0x5de)</span><span class="sxs-lookup"><span data-stu-id="a0bac-640">1502 (0x5DE)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-641">Die Ereignisprotokolldatei ist voll.</span><span class="sxs-lookup"><span data-stu-id="a0bac-641">The event log file is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-642"><span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**Fehler beim \_ Ändern der Ereignisprotokoll \_ Datei \_ .**</span><span class="sxs-lookup"><span data-stu-id="a0bac-642"><span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**ERROR\_EVENTLOG\_FILE\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-643">1503 (0x5df)</span><span class="sxs-lookup"><span data-stu-id="a0bac-643">1503 (0x5DF)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-644">Die Ereignisprotokoll Datei wurde zwischen Lesevorgängen geändert.</span><span class="sxs-lookup"><span data-stu-id="a0bac-644">The event log file has changed between read operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-645"><span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**Fehler \_ ungültiger \_ \_ Taskname.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-645"><span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**ERROR\_INVALID\_TASK\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-646">1550 (0x60E)</span><span class="sxs-lookup"><span data-stu-id="a0bac-646">1550 (0x60E)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-647">Der angegebene TaskName ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a0bac-647">The specified task name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-648"><span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**Fehler bei \_ ungültigem \_ Task \_ Index.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-648"><span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**ERROR\_INVALID\_TASK\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-649">1551 (0x60F)</span><span class="sxs-lookup"><span data-stu-id="a0bac-649">1551 (0x60F)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-650">Der angegebene Task Index ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a0bac-650">The specified task index is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-651"><span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**\_der Fehler Thread ist \_ bereits \_ in der \_ Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="a0bac-651"><span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**ERROR\_THREAD\_ALREADY\_IN\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-652">1552 (0x610)</span><span class="sxs-lookup"><span data-stu-id="a0bac-652">1552 (0x610)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-653">Der angegebene Thread wird bereits einer Aufgabe beitreten.</span><span class="sxs-lookup"><span data-stu-id="a0bac-653">The specified thread is already joining a task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-654"><span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**Fehler beim \_ Installieren des \_ Dienst \_ Fehlers.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-654"><span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**ERROR\_INSTALL\_SERVICE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-655">1601 (0x641)</span><span class="sxs-lookup"><span data-stu-id="a0bac-655">1601 (0x641)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-656">Auf den Windows Installer Dienst konnte nicht zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-656">The Windows Installer Service could not be accessed.</span></span> <span data-ttu-id="a0bac-657">Dies kann vorkommen, wenn die Windows Installer nicht ordnungsgemäß installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a0bac-657">This can occur if the Windows Installer is not correctly installed.</span></span> <span data-ttu-id="a0bac-658">Wenden Sie sich an den Support, um Hilfe zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0bac-658">Contact your support personnel for assistance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-659"><span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**Fehler beim \_ Installieren von \_ Userexit.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-659"><span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**ERROR\_INSTALL\_USEREXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-660">1602 (0x642)</span><span class="sxs-lookup"><span data-stu-id="a0bac-660">1602 (0x642)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-661">Benutzer hat die Installation abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-661">User cancelled installation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-662"><span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**Fehler bei der \_ Installation. \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-662"><span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**ERROR\_INSTALL\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-663">1603 (0x643)</span><span class="sxs-lookup"><span data-stu-id="a0bac-663">1603 (0x643)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-664">Schwerwiegender Fehler bei der Installation.</span><span class="sxs-lookup"><span data-stu-id="a0bac-664">Fatal error during installation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-665"><span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**Fehler beim \_ Installieren von \_ Suspend**</span><span class="sxs-lookup"><span data-stu-id="a0bac-665"><span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**ERROR\_INSTALL\_SUSPEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-666">1604 (0x644)</span><span class="sxs-lookup"><span data-stu-id="a0bac-666">1604 (0x644)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-667">Die Installation wurde angehalten, unvollständig.</span><span class="sxs-lookup"><span data-stu-id="a0bac-667">Installation suspended, incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-668"><span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**Unbekannter Fehler. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-668"><span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**ERROR\_UNKNOWN\_PRODUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-669">1605 (0x645)</span><span class="sxs-lookup"><span data-stu-id="a0bac-669">1605 (0x645)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-670">Diese Aktion ist nur für Produkte gültig, die zurzeit installiert sind.</span><span class="sxs-lookup"><span data-stu-id="a0bac-670">This action is only valid for products that are currently installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-671"><span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**Unbekannter Fehler. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-671"><span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**ERROR\_UNKNOWN\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-672">1606 (0x646)</span><span class="sxs-lookup"><span data-stu-id="a0bac-672">1606 (0x646)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-673">Die Funktions-ID ist nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="a0bac-673">Feature ID not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-674"><span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**\_unbekannter Fehler \_ Komponente.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-674"><span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**ERROR\_UNKNOWN\_COMPONENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-675">1607 (0x647)</span><span class="sxs-lookup"><span data-stu-id="a0bac-675">1607 (0x647)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-676">Die Komponenten-ID ist nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="a0bac-676">Component ID not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-677"><span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**\_unbekannter Fehler \_ Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-677"><span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**ERROR\_UNKNOWN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-678">1608 (0x648)</span><span class="sxs-lookup"><span data-stu-id="a0bac-678">1608 (0x648)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-679">Unbekannte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a0bac-679">Unknown property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-680"><span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**Fehler bei \_ ungültigem \_ handle- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="a0bac-680"><span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**ERROR\_INVALID\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-681">1609 (0x649)</span><span class="sxs-lookup"><span data-stu-id="a0bac-681">1609 (0x649)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-682">Das Handle befindet sich in einem ungültigen Zustand.</span><span class="sxs-lookup"><span data-stu-id="a0bac-682">Handle is in an invalid state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-683"><span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**Fehler \_ hafte \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="a0bac-683"><span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**ERROR\_BAD\_CONFIGURATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-684">1610 (0x64a)</span><span class="sxs-lookup"><span data-stu-id="a0bac-684">1610 (0x64A)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-685">Die Konfigurationsdaten für dieses Produkt sind beschädigt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-685">The configuration data for this product is corrupt.</span></span> <span data-ttu-id="a0bac-686">Wenden Sie sich an das Support Personal.</span><span class="sxs-lookup"><span data-stu-id="a0bac-686">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-687"><span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**Fehler \_ Index \_ fehlt.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-687"><span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**ERROR\_INDEX\_ABSENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-688">1611 (0x64b)</span><span class="sxs-lookup"><span data-stu-id="a0bac-688">1611 (0x64B)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-689">Komponenten Qualifizierer ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-689">Component qualifier not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-690"><span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**Fehler beim \_ Installieren der \_ Quelle. \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-690"><span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**ERROR\_INSTALL\_SOURCE\_ABSENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-691">1612 (0x64c)</span><span class="sxs-lookup"><span data-stu-id="a0bac-691">1612 (0x64C)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-692">Die Installationsquelle für dieses Produkt ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a0bac-692">The installation source for this product is not available.</span></span> <span data-ttu-id="a0bac-693">Vergewissern Sie sich, dass die Quelle vorhanden ist und Sie darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="a0bac-693">Verify that the source exists and that you can access it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-694"><span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**Fehler beim \_ Installieren der \_ Paket \_ Version.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-694"><span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**ERROR\_INSTALL\_PACKAGE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-695">1613 (0x64d)</span><span class="sxs-lookup"><span data-stu-id="a0bac-695">1613 (0x64D)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-696">Dieses Installationspaket kann nicht vom Windows Installer-Dienst installiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-696">This installation package cannot be installed by the Windows Installer service.</span></span> <span data-ttu-id="a0bac-697">Sie müssen eine Windows-Service Pack installieren, die eine neuere Version des Windows Installer Dienstanbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="a0bac-697">You must install a Windows service pack that contains a newer version of the Windows Installer service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-698"><span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**Fehler \_ Produkt \_ deinstalliert**</span><span class="sxs-lookup"><span data-stu-id="a0bac-698"><span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**ERROR\_PRODUCT\_UNINSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-699">1614 (0x64e)</span><span class="sxs-lookup"><span data-stu-id="a0bac-699">1614 (0x64E)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-700">Produkt wird deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="a0bac-700">Product is uninstalled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-701"><span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**Syntax für ungültige \_ \_ Abfrage Fehler \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-701"><span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**ERROR\_BAD\_QUERY\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-702">1615 (0x64f)</span><span class="sxs-lookup"><span data-stu-id="a0bac-702">1615 (0x64F)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-703">Die SQL-Abfrage Syntax ist ungültig oder nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-703">SQL query syntax invalid or unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-704"><span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**\_ungültiges \_ Feld für Fehler**</span><span class="sxs-lookup"><span data-stu-id="a0bac-704"><span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**ERROR\_INVALID\_FIELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-705">1616 (0x650)</span><span class="sxs-lookup"><span data-stu-id="a0bac-705">1616 (0x650)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-706">Das Daten Satz Feld ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-706">Record field does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-707"><span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**Fehler \_ Gerät \_ entfernt**</span><span class="sxs-lookup"><span data-stu-id="a0bac-707"><span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**ERROR\_DEVICE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-708">1617 (0x651)</span><span class="sxs-lookup"><span data-stu-id="a0bac-708">1617 (0x651)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-709">Das Gerät wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-709">The device has been removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-710"><span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**Fehler \_ Installation wird \_ bereits \_ ausgeführt.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-710"><span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**ERROR\_INSTALL\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-711">1618 (0x652)</span><span class="sxs-lookup"><span data-stu-id="a0bac-711">1618 (0x652)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-712">Es wird bereits eine andere Installation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-712">Another installation is already in progress.</span></span> <span data-ttu-id="a0bac-713">Schließen Sie diese Installation ab, bevor Sie mit der Installation fortfahren.</span><span class="sxs-lookup"><span data-stu-id="a0bac-713">Complete that installation before proceeding with this install.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-714"><span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**Fehler \_ beim \_ Öffnen des Pakets beim \_ Öffnen \_ .**</span><span class="sxs-lookup"><span data-stu-id="a0bac-714"><span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**ERROR\_INSTALL\_PACKAGE\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-715">1619 (0x653)</span><span class="sxs-lookup"><span data-stu-id="a0bac-715">1619 (0x653)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-716">Dieses Installationspaket konnte nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-716">This installation package could not be opened.</span></span> <span data-ttu-id="a0bac-717">Vergewissern Sie sich, dass das Paket vorhanden ist und Sie darauf zugreifen können, oder wenden Sie sich an den Hersteller der Anwendung, um zu überprüfen, ob dies ein gültiges Windows Installer Paket</span><span class="sxs-lookup"><span data-stu-id="a0bac-717">Verify that the package exists and that you can access it, or contact the application vendor to verify that this is a valid Windows Installer package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-718"><span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**Fehler beim \_ Installieren des \_ Pakets. \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-718"><span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**ERROR\_INSTALL\_PACKAGE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-719">1620 (0x654)</span><span class="sxs-lookup"><span data-stu-id="a0bac-719">1620 (0x654)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-720">Dieses Installationspaket konnte nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-720">This installation package could not be opened.</span></span> <span data-ttu-id="a0bac-721">Wenden Sie sich an den Hersteller der Anwendung, um sicherzustellen, dass dies ein gültiges Windows Installer Paket ist</span><span class="sxs-lookup"><span data-stu-id="a0bac-721">Contact the application vendor to verify that this is a valid Windows Installer package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-722"><span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**Fehler beim \_ Installieren des \_ Benutzer \_ Oberflächen Fehlers**</span><span class="sxs-lookup"><span data-stu-id="a0bac-722"><span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**ERROR\_INSTALL\_UI\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-723">1621 (0x655)</span><span class="sxs-lookup"><span data-stu-id="a0bac-723">1621 (0x655)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-724">Fehler beim Starten der Benutzeroberfläche des Windows Installer Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="a0bac-724">There was an error starting the Windows Installer service user interface.</span></span> <span data-ttu-id="a0bac-725">Wenden Sie sich an das Support Personal.</span><span class="sxs-lookup"><span data-stu-id="a0bac-725">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-726"><span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**Fehler beim \_ Installieren des \_ Protokolls \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-726"><span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**ERROR\_INSTALL\_LOG\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-727">1622 (0x656)</span><span class="sxs-lookup"><span data-stu-id="a0bac-727">1622 (0x656)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-728">Fehler beim Öffnen der Installationsprotokoll Datei.</span><span class="sxs-lookup"><span data-stu-id="a0bac-728">Error opening installation log file.</span></span> <span data-ttu-id="a0bac-729">Vergewissern Sie sich, dass der angegebene Speicherort der Protokolldatei vorhanden ist und Sie darauf schreiben können.</span><span class="sxs-lookup"><span data-stu-id="a0bac-729">Verify that the specified log file location exists and that you can write to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-730"><span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**Fehler beim \_ Installieren der \_ Sprache \_ nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="a0bac-730"><span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**ERROR\_INSTALL\_LANGUAGE\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-731">1623 (0x657)</span><span class="sxs-lookup"><span data-stu-id="a0bac-731">1623 (0x657)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-732">Die Sprache dieses Installationspakets wird von Ihrem System nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-732">The language of this installation package is not supported by your system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-733"><span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**Fehler beim \_ Installieren der \_ Transformation. \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-733"><span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**ERROR\_INSTALL\_TRANSFORM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-734">1624 (0x658)</span><span class="sxs-lookup"><span data-stu-id="a0bac-734">1624 (0x658)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-735">Fehler beim Anwenden von Transformationen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-735">Error applying transforms.</span></span> <span data-ttu-id="a0bac-736">Überprüfen Sie, ob die angegebenen Transformationspfade gültig sind.</span><span class="sxs-lookup"><span data-stu-id="a0bac-736">Verify that the specified transform paths are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-737"><span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**Fehler beim \_ Installieren des \_ Pakets. \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-737"><span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**ERROR\_INSTALL\_PACKAGE\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-738">1625 (0x659)</span><span class="sxs-lookup"><span data-stu-id="a0bac-738">1625 (0x659)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-739">Diese Installation ist durch die System Richtlinie unzulässig.</span><span class="sxs-lookup"><span data-stu-id="a0bac-739">This installation is forbidden by system policy.</span></span> <span data-ttu-id="a0bac-740">Wenden Sie sich an Ihren Systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="a0bac-740">Contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-741"><span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**Fehler \_ Funktion \_ nicht \_ aufgerufen**</span><span class="sxs-lookup"><span data-stu-id="a0bac-741"><span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**ERROR\_FUNCTION\_NOT\_CALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-742">1626 (0x65a)</span><span class="sxs-lookup"><span data-stu-id="a0bac-742">1626 (0x65A)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-743">Die Funktion konnte nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-743">Function could not be executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-744"><span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**Fehler bei Fehler \_ Funktion \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-744"><span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**ERROR\_FUNCTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-745">1627 (0x65b)</span><span class="sxs-lookup"><span data-stu-id="a0bac-745">1627 (0x65B)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-746">Fehler bei der Ausführung der Funktion.</span><span class="sxs-lookup"><span data-stu-id="a0bac-746">Function failed during execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-747"><span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**Fehler \_ ungültige \_ Tabelle**</span><span class="sxs-lookup"><span data-stu-id="a0bac-747"><span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**ERROR\_INVALID\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-748">1628 (0x65c)</span><span class="sxs-lookup"><span data-stu-id="a0bac-748">1628 (0x65C)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-749">Es wurde eine ungültige oder unbekannte Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="a0bac-749">Invalid or unknown table specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-750"><span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**Fehler bei \_ DataType-Konflikt. \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-750"><span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**ERROR\_DATATYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-751">1629 (0x65d)</span><span class="sxs-lookup"><span data-stu-id="a0bac-751">1629 (0x65D)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-752">Die bereitgestellten Daten haben einen falschen Typ.</span><span class="sxs-lookup"><span data-stu-id="a0bac-752">Data supplied is of wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-753"><span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**\_nicht unterstützter Typ des Fehlers. \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-753"><span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**ERROR\_UNSUPPORTED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-754">1630 (0x65e)</span><span class="sxs-lookup"><span data-stu-id="a0bac-754">1630 (0x65E)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-755">Daten dieses Typs werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-755">Data of this type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-756"><span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**Fehler beim \_ erstellen. \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-756"><span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**ERROR\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-757">1631 (0x65f)</span><span class="sxs-lookup"><span data-stu-id="a0bac-757">1631 (0x65F)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-758">Der Windows Installer-Dienst konnte nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-758">The Windows Installer service failed to start.</span></span> <span data-ttu-id="a0bac-759">Wenden Sie sich an das Support Personal.</span><span class="sxs-lookup"><span data-stu-id="a0bac-759">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-760"><span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**Fehler beim Installieren der temporären \_ \_ \_ nicht Schreib baren Datei**</span><span class="sxs-lookup"><span data-stu-id="a0bac-760"><span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**ERROR\_INSTALL\_TEMP\_UNWRITABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-761">1632 (0x660)</span><span class="sxs-lookup"><span data-stu-id="a0bac-761">1632 (0x660)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-762">Der Temp-Ordner befindet sich auf einem Laufwerk, das voll ist oder nicht zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="a0bac-762">The Temp folder is on a drive that is full or is inaccessible.</span></span> <span data-ttu-id="a0bac-763">Geben Sie Speicherplatz auf dem Laufwerk frei, oder überprüfen Sie, ob Sie über Schreibberechtigungen für den temporären Ordner verfügen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-763">Free up space on the drive or verify that you have write permission on the Temp folder.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-764"><span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**Fehler beim \_ Installieren der \_ Plattform \_ nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="a0bac-764"><span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**ERROR\_INSTALL\_PLATFORM\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-765">1633 (0x661)</span><span class="sxs-lookup"><span data-stu-id="a0bac-765">1633 (0x661)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-766">Dieses Installationspaket wird von diesem Prozessortyp nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-766">This installation package is not supported by this processor type.</span></span> <span data-ttu-id="a0bac-767">Wenden Sie sich an Ihren Produkthersteller.</span><span class="sxs-lookup"><span data-stu-id="a0bac-767">Contact your product vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-768"><span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**Fehler beim \_ Installieren von \_ notused**</span><span class="sxs-lookup"><span data-stu-id="a0bac-768"><span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**ERROR\_INSTALL\_NOTUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-769">1634 (0x662)</span><span class="sxs-lookup"><span data-stu-id="a0bac-769">1634 (0x662)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-770">Die Komponente wird auf diesem Computer nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0bac-770">Component not used on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-771"><span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**Fehler beim \_ Öffnen des Patch- \_ Pakets \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-771"><span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**ERROR\_PATCH\_PACKAGE\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-772">1635 (0x663)</span><span class="sxs-lookup"><span data-stu-id="a0bac-772">1635 (0x663)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-773">Dieses Update Paket konnte nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-773">This update package could not be opened.</span></span> <span data-ttu-id="a0bac-774">Vergewissern Sie sich, dass das Update Paket vorhanden ist und Sie darauf zugreifen können, oder wenden Sie sich an den Hersteller der Anwendung, um zu überprüfen, ob es sich um ein gültiges Windows Installer Update</span><span class="sxs-lookup"><span data-stu-id="a0bac-774">Verify that the update package exists and that you can access it, or contact the application vendor to verify that this is a valid Windows Installer update package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-775"><span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**Fehler beim \_ Patch- \_ Paket \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="a0bac-775"><span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**ERROR\_PATCH\_PACKAGE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-776">1636 (0x664)</span><span class="sxs-lookup"><span data-stu-id="a0bac-776">1636 (0x664)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-777">Dieses Update Paket konnte nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-777">This update package could not be opened.</span></span> <span data-ttu-id="a0bac-778">Wenden Sie sich an den Hersteller der Anwendung, um zu überprüfen, ob es sich um ein gültiges Windows Installer Update</span><span class="sxs-lookup"><span data-stu-id="a0bac-778">Contact the application vendor to verify that this is a valid Windows Installer update package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-779"><span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**Fehler beim \_ Patch- \_ Paket \_ nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="a0bac-779"><span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**ERROR\_PATCH\_PACKAGE\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-780">1637 (0x665)</span><span class="sxs-lookup"><span data-stu-id="a0bac-780">1637 (0x665)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-781">Dieses Update Paket kann nicht vom Windows Installer-Dienst verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-781">This update package cannot be processed by the Windows Installer service.</span></span> <span data-ttu-id="a0bac-782">Sie müssen eine Windows-Service Pack installieren, die eine neuere Version des Windows Installer Dienstanbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="a0bac-782">You must install a Windows service pack that contains a newer version of the Windows Installer service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-783"><span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**Fehler \_ Produkt \_ Version**</span><span class="sxs-lookup"><span data-stu-id="a0bac-783"><span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**ERROR\_PRODUCT\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-784">1638 (0x666)</span><span class="sxs-lookup"><span data-stu-id="a0bac-784">1638 (0x666)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-785">Eine andere Version dieses Produkts ist bereits installiert.</span><span class="sxs-lookup"><span data-stu-id="a0bac-785">Another version of this product is already installed.</span></span> <span data-ttu-id="a0bac-786">Die Installation dieser Version kann nicht fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-786">Installation of this version cannot continue.</span></span> <span data-ttu-id="a0bac-787">Um die vorhandene Version dieses Produkts zu konfigurieren oder zu entfernen, verwenden Sie die Option Software in der Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="a0bac-787">To configure or remove the existing version of this product, use Add/Remove Programs on the Control Panel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-788"><span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**Fehler \_ ungültige \_ Befehls \_ Zeile.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-788"><span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**ERROR\_INVALID\_COMMAND\_LINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-789">1639 (0x667)</span><span class="sxs-lookup"><span data-stu-id="a0bac-789">1639 (0x667)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-790">Ungültiges Befehlszeilenargument.</span><span class="sxs-lookup"><span data-stu-id="a0bac-790">Invalid command line argument.</span></span> <span data-ttu-id="a0bac-791">Ausführliche Hilfe zur Befehlszeile finden Sie im Windows Installer SDK.</span><span class="sxs-lookup"><span data-stu-id="a0bac-791">Consult the Windows Installer SDK for detailed command line help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-792"><span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**Fehler beim \_ Installieren von \_ Remote. \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-792"><span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**ERROR\_INSTALL\_REMOTE\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-793">1640 (0x668)</span><span class="sxs-lookup"><span data-stu-id="a0bac-793">1640 (0x668)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-794">Nur Administratoren verfügen über die Berechtigung zum Hinzufügen, entfernen oder Konfigurieren von Server Software während einer Terminal Dienste-Remote Sitzung.</span><span class="sxs-lookup"><span data-stu-id="a0bac-794">Only administrators have permission to add, remove, or configure server software during a Terminal services remote session.</span></span> <span data-ttu-id="a0bac-795">Wenn Sie Software auf dem Server installieren oder konfigurieren möchten, wenden Sie sich an Ihren Netzwerkadministrator.</span><span class="sxs-lookup"><span data-stu-id="a0bac-795">If you want to install or configure software on the server, contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-796"><span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**Fehler \_ beim \_ Neustart \_ wurde initiiert.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-796"><span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**ERROR\_SUCCESS\_REBOOT\_INITIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-797">1641 (0x669)</span><span class="sxs-lookup"><span data-stu-id="a0bac-797">1641 (0x669)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-798">Der angeforderte Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-798">The requested operation completed successfully.</span></span> <span data-ttu-id="a0bac-799">Das System wird neu gestartet, damit die Änderungen wirksam werden können.</span><span class="sxs-lookup"><span data-stu-id="a0bac-799">The system will be restarted so the changes can take effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-800"><span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**Das \_ \_ fehlerpatchziel wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-800"><span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**ERROR\_PATCH\_TARGET\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-801">1642 (0x66a)</span><span class="sxs-lookup"><span data-stu-id="a0bac-801">1642 (0x66A)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-802">Das Upgrade kann nicht vom Windows Installer-Dienst installiert werden, weil das zu Aktualisier Ende Programm möglicherweise fehlt, oder das Upgrade kann eine andere Version des Programms aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a0bac-802">The upgrade cannot be installed by the Windows Installer service because the program to be upgraded may be missing, or the upgrade may update a different version of the program.</span></span> <span data-ttu-id="a0bac-803">Vergewissern Sie sich, dass das zu Aktualisier Ende Programm auf dem Computer vorhanden ist und dass Sie über das richtige Upgrade verfügen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-803">Verify that the program to be upgraded exists on your computer and that you have the correct upgrade.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-804"><span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**Fehler beim \_ Patch- \_ Paket \_ abgelehnt**</span><span class="sxs-lookup"><span data-stu-id="a0bac-804"><span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**ERROR\_PATCH\_PACKAGE\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-805">1643 (0x66b)</span><span class="sxs-lookup"><span data-stu-id="a0bac-805">1643 (0x66B)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-806">Das Update Paket ist von der Software Einschränkungs Richtlinie nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="a0bac-806">The update package is not permitted by software restriction policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-807"><span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**Fehler beim \_ Installieren der \_ Transformation. \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-807"><span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**ERROR\_INSTALL\_TRANSFORM\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-808">1644 (0x66c)</span><span class="sxs-lookup"><span data-stu-id="a0bac-808">1644 (0x66C)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-809">Eine oder mehrere Anpassungen sind von der Software Einschränkungs Richtlinie nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="a0bac-809">One or more customizations are not permitted by software restriction policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-810"><span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**Fehler beim \_ Installieren der \_ Remote Installation. \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-810"><span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**ERROR\_INSTALL\_REMOTE\_PROHIBITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-811">1645 (0x66D)</span><span class="sxs-lookup"><span data-stu-id="a0bac-811">1645 (0x66D)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-812">In der Windows Installer ist die Installation von einem Remotedesktopverbindung nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="a0bac-812">The Windows Installer does not permit installation from a Remote Desktop Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-813"><span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**Entfernen des Fehler \_ Patches \_ \_ nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="a0bac-813"><span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**ERROR\_PATCH\_REMOVAL\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-814">1646 (0x66E)</span><span class="sxs-lookup"><span data-stu-id="a0bac-814">1646 (0x66E)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-815">Die Installation des Update Pakets wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-815">Uninstallation of the update package is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-816"><span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**Unbekannter Fehler beim \_ \_ Patch.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-816"><span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**ERROR\_UNKNOWN\_PATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-817">1647 (0x66f)</span><span class="sxs-lookup"><span data-stu-id="a0bac-817">1647 (0x66F)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-818">Das Update wird nicht auf dieses Produkt angewendet.</span><span class="sxs-lookup"><span data-stu-id="a0bac-818">The update is not applied to this product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-819"><span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**Fehler \_ Patch \_ keine \_ Sequenz**</span><span class="sxs-lookup"><span data-stu-id="a0bac-819"><span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**ERROR\_PATCH\_NO\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-820">1648 (0x670)</span><span class="sxs-lookup"><span data-stu-id="a0bac-820">1648 (0x670)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-821">Für den Satz von Updates konnte keine gültige Sequenz gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-821">No valid sequence could be found for the set of updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-822"><span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**Fehler beim Entfernen des Fehler \_ Patches. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a0bac-822"><span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**ERROR\_PATCH\_REMOVAL\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-823">1649 (0x671)</span><span class="sxs-lookup"><span data-stu-id="a0bac-823">1649 (0x671)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-824">Das Entfernen von Updates wurde durch die Richtlinie nicht zugelassen.</span><span class="sxs-lookup"><span data-stu-id="a0bac-824">Update removal was disallowed by policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-825"><span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**Fehler \_ ungültige \_ Patch- \_ XML.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-825"><span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**ERROR\_INVALID\_PATCH\_XML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-826">1650 (0x672)</span><span class="sxs-lookup"><span data-stu-id="a0bac-826">1650 (0x672)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-827">Die XML-Update Daten sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="a0bac-827">The XML update data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-828"><span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**Fehler \_ Patch für \_ verwaltete \_ angekündigte \_ Produkte**</span><span class="sxs-lookup"><span data-stu-id="a0bac-828"><span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**ERROR\_PATCH\_MANAGED\_ADVERTISED\_PRODUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-829">1651 (0x673)</span><span class="sxs-lookup"><span data-stu-id="a0bac-829">1651 (0x673)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-830">Windows Installer lässt keine Aktualisierung von verwalteten angekündigten Produkten zu.</span><span class="sxs-lookup"><span data-stu-id="a0bac-830">Windows Installer does not permit updating of managed advertised products.</span></span> <span data-ttu-id="a0bac-831">Vor dem Anwenden des Updates muss mindestens eine Produkt Funktion installiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0bac-831">At least one feature of the product must be installed before applying the update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-832"><span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**Fehler beim \_ Installieren von \_ Dienst- \_ SafeBoot**</span><span class="sxs-lookup"><span data-stu-id="a0bac-832"><span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**ERROR\_INSTALL\_SERVICE\_SAFEBOOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-833">1652 (0x674)</span><span class="sxs-lookup"><span data-stu-id="a0bac-833">1652 (0x674)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-834">Der Windows Installer-Dienst ist im abgesicherten Modus nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a0bac-834">The Windows Installer service is not accessible in Safe Mode.</span></span> <span data-ttu-id="a0bac-835">Versuchen Sie es erneut, wenn sich Ihr Computer nicht im abgesicherten Modus befindet, oder Sie können die System Wiederherstellung verwenden, um den Computer in einen früheren Zustand zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="a0bac-835">Please try again when your computer is not in Safe Mode or you can use System Restore to return your machine to a previous good state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-836"><span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**Fehler \_ bei \_ schneller \_ Ausnahme bei Fehler.**</span><span class="sxs-lookup"><span data-stu-id="a0bac-836"><span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**ERROR\_FAIL\_FAST\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-837">1653 (0x675)</span><span class="sxs-lookup"><span data-stu-id="a0bac-837">1653 (0x675)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-838">Es ist eine fehlerhafte Ausnahme aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a0bac-838">A fail fast exception occurred.</span></span> <span data-ttu-id="a0bac-839">Ausnahmehandler werden nicht aufgerufen, und der Prozess wird sofort beendet.</span><span class="sxs-lookup"><span data-stu-id="a0bac-839">Exception handlers will not be invoked and the process will be terminated immediately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a0bac-840"><span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**Fehler \_ Installation \_ abgelehnt**</span><span class="sxs-lookup"><span data-stu-id="a0bac-840"><span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**ERROR\_INSTALL\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bac-841">1654 (0x676)</span><span class="sxs-lookup"><span data-stu-id="a0bac-841">1654 (0x676)</span></span>
</dt> <dt>



<span data-ttu-id="a0bac-842">Die APP, die Sie ausführen möchten, wird in dieser Windows-Version nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0bac-842">The app that you are trying to run is not supported on this version of Windows.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0bac-843">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0bac-843">Requirements</span></span>



| <span data-ttu-id="a0bac-844">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0bac-844">Requirement</span></span> | <span data-ttu-id="a0bac-845">Wert</span><span class="sxs-lookup"><span data-stu-id="a0bac-845">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0bac-846">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0bac-846">Minimum supported client</span></span><br/> | <span data-ttu-id="a0bac-847">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0bac-847">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a0bac-848">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a0bac-848">Minimum supported server</span></span><br/> | <span data-ttu-id="a0bac-849">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0bac-849">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0bac-850">Header</span><span class="sxs-lookup"><span data-stu-id="a0bac-850">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0bac-851"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0bac-851"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0bac-852">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0bac-852">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0bac-853">System Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="a0bac-853">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




