---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 6000-8199 und ist für Entwickler bestimmt.
ms.assetid: eaaf9f65-e8ff-4e54-90a9-04252cdd773a
title: System Fehler Codes (6000-8199) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 0660009411224673481e9b65bcb62d7b194ab71f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861376"
---
# <a name="system-error-codes-6000-8199"></a><span data-ttu-id="95627-103">System Fehler Codes (6000-8199)</span><span class="sxs-lookup"><span data-stu-id="95627-103">System Error Codes (6000-8199)</span></span>

> [!NOTE]
> <span data-ttu-id="95627-104">Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen.</span><span class="sxs-lookup"><span data-stu-id="95627-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="95627-105">Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="95627-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="95627-106">In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) (Fehler 6000 bis 8199) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="95627-106">The following list describes [system error codes](system-error-codes.md) (errors 6000 to 8199).</span></span> <span data-ttu-id="95627-107">Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="95627-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="95627-108">Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".</span><span class="sxs-lookup"><span data-stu-id="95627-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="95627-109"><span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**Fehler beim \_ verschlüsseln. \_**</span><span class="sxs-lookup"><span data-stu-id="95627-109"><span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**ERROR\_ENCRYPTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-110">6000 (0x1770)</span><span class="sxs-lookup"><span data-stu-id="95627-110">6000 (0x1770)</span></span>
</dt> <dt>



<span data-ttu-id="95627-111">Die angegebene Datei konnte nicht verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="95627-111">The specified file could not be encrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-112"><span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**Fehler beim \_ entschlüsseln \_ .**</span><span class="sxs-lookup"><span data-stu-id="95627-112"><span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**ERROR\_DECRYPTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-113">6001 (0x1771)</span><span class="sxs-lookup"><span data-stu-id="95627-113">6001 (0x1771)</span></span>
</dt> <dt>



<span data-ttu-id="95627-114">Die angegebene Datei konnte nicht entschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="95627-114">The specified file could not be decrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-115"><span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**Fehler \_ Datei \_ verschlüsselt**</span><span class="sxs-lookup"><span data-stu-id="95627-115"><span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**ERROR\_FILE\_ENCRYPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-116">6002 (0x1772)</span><span class="sxs-lookup"><span data-stu-id="95627-116">6002 (0x1772)</span></span>
</dt> <dt>



<span data-ttu-id="95627-117">Die angegebene Datei ist verschlüsselt, und der Benutzer ist nicht in der Lage, Sie zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="95627-117">The specified file is encrypted and the user does not have the ability to decrypt it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-118"><span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**Fehler \_ keine \_ Wiederherstellungs \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="95627-118"><span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**ERROR\_NO\_RECOVERY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-119">6003 (0x1773)</span><span class="sxs-lookup"><span data-stu-id="95627-119">6003 (0x1773)</span></span>
</dt> <dt>



<span data-ttu-id="95627-120">Für dieses System ist keine gültige Verschlüsselungs Wiederherstellungs Richtlinie konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="95627-120">There is no valid encryption recovery policy configured for this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-121"><span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**Fehler " \_ keine \_ EFS"**</span><span class="sxs-lookup"><span data-stu-id="95627-121"><span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**ERROR\_NO\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-122">6004 (0x1774)</span><span class="sxs-lookup"><span data-stu-id="95627-122">6004 (0x1774)</span></span>
</dt> <dt>



<span data-ttu-id="95627-123">Der erforderliche Verschlüsselungs Treiber ist für dieses System nicht geladen.</span><span class="sxs-lookup"><span data-stu-id="95627-123">The required encryption driver is not loaded for this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-124"><span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**\_falscher Fehler \_ EFS**</span><span class="sxs-lookup"><span data-stu-id="95627-124"><span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**ERROR\_WRONG\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-125">6005 (0x1775)</span><span class="sxs-lookup"><span data-stu-id="95627-125">6005 (0x1775)</span></span>
</dt> <dt>



<span data-ttu-id="95627-126">Die Datei wurde mit einem anderen Verschlüsselungs Treiber verschlüsselt, als gerade geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="95627-126">The file was encrypted with a different encryption driver than is currently loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-127"><span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**Fehler \_ keine \_ Benutzer \_ Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="95627-127"><span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**ERROR\_NO\_USER\_KEYS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-128">6006 (0x1776)</span><span class="sxs-lookup"><span data-stu-id="95627-128">6006 (0x1776)</span></span>
</dt> <dt>



<span data-ttu-id="95627-129">Für den Benutzer sind keine EFS-Schlüssel definiert.</span><span class="sxs-lookup"><span data-stu-id="95627-129">There are no EFS keys defined for the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-130"><span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**Fehler \_ Datei \_ nicht \_ verschlüsselt**</span><span class="sxs-lookup"><span data-stu-id="95627-130"><span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**ERROR\_FILE\_NOT\_ENCRYPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-131">6007 (0x1777)</span><span class="sxs-lookup"><span data-stu-id="95627-131">6007 (0x1777)</span></span>
</dt> <dt>



<span data-ttu-id="95627-132">Die angegebene Datei ist nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="95627-132">The specified file is not encrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-133"><span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**Fehler \_ beim \_ Exportieren des \_ Formats.**</span><span class="sxs-lookup"><span data-stu-id="95627-133"><span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**ERROR\_NOT\_EXPORT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-134">6008 (0x1778)</span><span class="sxs-lookup"><span data-stu-id="95627-134">6008 (0x1778)</span></span>
</dt> <dt>



<span data-ttu-id="95627-135">Die angegebene Datei weist nicht das definierte EFS-Exportformat auf.</span><span class="sxs-lookup"><span data-stu-id="95627-135">The specified file is not in the defined EFS export format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-136"><span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**Fehler \_ Datei schreibgeschützt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="95627-136"><span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**ERROR\_FILE\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-137">6009 (0x1779)</span><span class="sxs-lookup"><span data-stu-id="95627-137">6009 (0x1779)</span></span>
</dt> <dt>



<span data-ttu-id="95627-138">Die angegebene Datei ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="95627-138">The specified file is read only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-139"><span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**Fehler Verzeichnis- \_ \_ EFS nicht \_ zulässig**</span><span class="sxs-lookup"><span data-stu-id="95627-139"><span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**ERROR\_DIR\_EFS\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-140">6010 (0x177a)</span><span class="sxs-lookup"><span data-stu-id="95627-140">6010 (0x177A)</span></span>
</dt> <dt>



<span data-ttu-id="95627-141">Das Verzeichnis wurde für die Verschlüsselung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="95627-141">The directory has been disabled for encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-142"><span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**Fehler \_ EFS- \_ Server \_ nicht \_ vertrauenswürdig**</span><span class="sxs-lookup"><span data-stu-id="95627-142"><span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**ERROR\_EFS\_SERVER\_NOT\_TRUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-143">6011 (0x177b)</span><span class="sxs-lookup"><span data-stu-id="95627-143">6011 (0x177B)</span></span>
</dt> <dt>



<span data-ttu-id="95627-144">Der Server ist für den Remote Verschlüsselungs Vorgang nicht vertrauenswürdig.</span><span class="sxs-lookup"><span data-stu-id="95627-144">The server is not trusted for remote encryption operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-145"><span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**fehlerhafter \_ \_ Wiederherstellungs \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="95627-145"><span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**ERROR\_BAD\_RECOVERY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-146">6012 (0x177c)</span><span class="sxs-lookup"><span data-stu-id="95627-146">6012 (0x177C)</span></span>
</dt> <dt>



<span data-ttu-id="95627-147">Für dieses System konfigurierte Wiederherstellungs Richtlinie enthält ein ungültiges Wiederherstellungs Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="95627-147">Recovery policy configured for this system contains invalid recovery certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-148"><span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**Fehler \_ EFS \_ ALG \_ BLOB \_ zu \_ groß**</span><span class="sxs-lookup"><span data-stu-id="95627-148"><span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**ERROR\_EFS\_ALG\_BLOB\_TOO\_BIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-149">6013 (0x177d)</span><span class="sxs-lookup"><span data-stu-id="95627-149">6013 (0x177D)</span></span>
</dt> <dt>



<span data-ttu-id="95627-150">Der Verschlüsselungsalgorithmus, der in der Quelldatei verwendet wird, benötigt einen größeren Schlüsselpuffer als der in der Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="95627-150">The encryption algorithm used on the source file needs a bigger key buffer than the one on the destination file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-151"><span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**Fehler \_ Volume \_ \_ unterstützt \_ EFS nicht**</span><span class="sxs-lookup"><span data-stu-id="95627-151"><span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**ERROR\_VOLUME\_NOT\_SUPPORT\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-152">6014 (0x177e)</span><span class="sxs-lookup"><span data-stu-id="95627-152">6014 (0x177E)</span></span>
</dt> <dt>



<span data-ttu-id="95627-153">Die Datenträger Partition unterstützt keine Dateiverschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="95627-153">The disk partition does not support file encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-154"><span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**Fehler \_ EFS \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="95627-154"><span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**ERROR\_EFS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-155">6015 (0x177f)</span><span class="sxs-lookup"><span data-stu-id="95627-155">6015 (0x177F)</span></span>
</dt> <dt>



<span data-ttu-id="95627-156">Dieser Computer ist für die Dateiverschlüsselung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="95627-156">This machine is disabled for file encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-157"><span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**Fehler \_ EFS- \_ Version wird \_ nicht \_ unterstützt**</span><span class="sxs-lookup"><span data-stu-id="95627-157"><span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**ERROR\_EFS\_VERSION\_NOT\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-158">6016 (0x1780)</span><span class="sxs-lookup"><span data-stu-id="95627-158">6016 (0x1780)</span></span>
</dt> <dt>



<span data-ttu-id="95627-159">Ein neueres System ist erforderlich, um diese verschlüsselte Datei zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="95627-159">A newer system is required to decrypt this encrypted file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-160"><span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**Fehler bei \_ CS- \_ Verschlüsselung \_ ungültige \_ Server \_ Antwort.**</span><span class="sxs-lookup"><span data-stu-id="95627-160"><span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**ERROR\_CS\_ENCRYPTION\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-161">6017 (0x1781)</span><span class="sxs-lookup"><span data-stu-id="95627-161">6017 (0x1781)</span></span>
</dt> <dt>



<span data-ttu-id="95627-162">Der Remote Server hat eine ungültige Antwort für eine Datei gesendet, die mit der Client seitigen Verschlüsselung geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="95627-162">The remote server sent an invalid response for a file being opened with Client Side Encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-163"><span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**Fehler bei \_ CS- \_ Verschlüsselung \_ nicht unterstützter \_ Server**</span><span class="sxs-lookup"><span data-stu-id="95627-163"><span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**ERROR\_CS\_ENCRYPTION\_UNSUPPORTED\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-164">6018 (0x1782)</span><span class="sxs-lookup"><span data-stu-id="95627-164">6018 (0x1782)</span></span>
</dt> <dt>



<span data-ttu-id="95627-165">Die Client seitige Verschlüsselung wird vom Remote Server nicht unterstützt, obwohl Sie von der Anwendung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="95627-165">Client Side Encryption is not supported by the remote server even though it claims to support it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-166"><span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**Fehler- \_ CS- \_ Verschlüsselung \_ vorhanden \_ verschlüsselte \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="95627-166"><span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**ERROR\_CS\_ENCRYPTION\_EXISTING\_ENCRYPTED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-167">6019 (0x1783)</span><span class="sxs-lookup"><span data-stu-id="95627-167">6019 (0x1783)</span></span>
</dt> <dt>



<span data-ttu-id="95627-168">Die Datei ist verschlüsselt und sollte im Client seitigen Verschlüsselungs Modus geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="95627-168">File is encrypted and should be opened in Client Side Encryption mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-169"><span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**Fehler bei \_ CS- \_ Verschlüsselung \_ neue \_ verschlüsselte \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="95627-169"><span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**ERROR\_CS\_ENCRYPTION\_NEW\_ENCRYPTED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-170">6020 (0x1784)</span><span class="sxs-lookup"><span data-stu-id="95627-170">6020 (0x1784)</span></span>
</dt> <dt>



<span data-ttu-id="95627-171">Eine neue verschlüsselte Datei wird erstellt, und ein $EFS muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="95627-171">A new encrypted file is being created and a $EFS needs to be provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-172"><span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**Fehler- \_ CS- \_ Verschlüsselungs \_ Datei \_ nicht \_ CSE**</span><span class="sxs-lookup"><span data-stu-id="95627-172"><span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**ERROR\_CS\_ENCRYPTION\_FILE\_NOT\_CSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-173">6021 (0x1785)</span><span class="sxs-lookup"><span data-stu-id="95627-173">6021 (0x1785)</span></span>
</dt> <dt>



<span data-ttu-id="95627-174">Der SMB-Client hat eine Client seitige Erweiterung für eine nicht-CSE-Datei angefordert.</span><span class="sxs-lookup"><span data-stu-id="95627-174">The SMB client requested a CSE FSCTL on a non-CSE file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-175"><span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**Fehler \_ Verschlüsselungs \_ Richtlinie \_ verweigert \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="95627-175"><span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**ERROR\_ENCRYPTION\_POLICY\_DENIES\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-176">6022 (0x1786)</span><span class="sxs-lookup"><span data-stu-id="95627-176">6022 (0x1786)</span></span>
</dt> <dt>



<span data-ttu-id="95627-177">Der angeforderte Vorgang wurde durch die Richtlinie blockiert.</span><span class="sxs-lookup"><span data-stu-id="95627-177">The requested operation was blocked by policy.</span></span> <span data-ttu-id="95627-178">Wenden Sie sich an Ihren Systemadministrator, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="95627-178">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-179"><span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**Fehler \_ keine \_ Browser \_ Server \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="95627-179"><span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**ERROR\_NO\_BROWSER\_SERVERS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-180">6118 (0x17e6)</span><span class="sxs-lookup"><span data-stu-id="95627-180">6118 (0x17E6)</span></span>
</dt> <dt>



<span data-ttu-id="95627-181">Die Liste der Server für diese Arbeitsgruppe ist zurzeit nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="95627-181">The list of servers for this workgroup is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-182"><span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**sched \_ E \_ Dienst \_ nicht \_ LocalSystem**</span><span class="sxs-lookup"><span data-stu-id="95627-182"><span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**SCHED\_E\_SERVICE\_NOT\_LOCALSYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-183">6200 (0x1838)</span><span class="sxs-lookup"><span data-stu-id="95627-183">6200 (0x1838)</span></span>
</dt> <dt>



<span data-ttu-id="95627-184">Der Taskplaner-Dienst muss so konfiguriert werden, dass er im System Konto ausgeführt wird, damit er ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="95627-184">The Task Scheduler service must be configured to run in the System account to function properly.</span></span> <span data-ttu-id="95627-185">Einzelne Tasks können so konfiguriert werden, dass Sie in anderen Konten ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="95627-185">Individual tasks may be configured to run in other accounts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-186"><span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**Fehler \_ Protokoll \_ Sektor \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="95627-186"><span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**ERROR\_LOG\_SECTOR\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-187">6600 (0x19c8)</span><span class="sxs-lookup"><span data-stu-id="95627-187">6600 (0x19C8)</span></span>
</dt> <dt>



<span data-ttu-id="95627-188">Der Protokolldienst hat einen ungültigen Protokoll Sektor gefunden.</span><span class="sxs-lookup"><span data-stu-id="95627-188">Log service encountered an invalid log sector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-189"><span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**\_sektorparität des Fehler Protokolls \_ \_ \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="95627-189"><span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**ERROR\_LOG\_SECTOR\_PARITY\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-190">6601 (0x19c9)</span><span class="sxs-lookup"><span data-stu-id="95627-190">6601 (0x19C9)</span></span>
</dt> <dt>



<span data-ttu-id="95627-191">Protokolldienst hat einen Protokoll Sektor mit ungültiger Block Parität gefunden.</span><span class="sxs-lookup"><span data-stu-id="95627-191">Log service encountered a log sector with invalid block parity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-192"><span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**Fehler \_ Protokoll \_ Sektor neu zugeordnet \_**</span><span class="sxs-lookup"><span data-stu-id="95627-192"><span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**ERROR\_LOG\_SECTOR\_REMAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-193">6602 (0x19ca)</span><span class="sxs-lookup"><span data-stu-id="95627-193">6602 (0x19CA)</span></span>
</dt> <dt>



<span data-ttu-id="95627-194">Der Protokolldienst hat einen neu zugeordnete Protokoll Sektor gefunden.</span><span class="sxs-lookup"><span data-stu-id="95627-194">Log service encountered a remapped log sector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-195"><span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**Fehler \_ Protokoll \_ Block \_ unvollständig**</span><span class="sxs-lookup"><span data-stu-id="95627-195"><span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**ERROR\_LOG\_BLOCK\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-196">6603 (0x19cb)</span><span class="sxs-lookup"><span data-stu-id="95627-196">6603 (0x19CB)</span></span>
</dt> <dt>



<span data-ttu-id="95627-197">Der Protokolldienst hat einen partiellen oder unvollständigen Protokoll Block gefunden.</span><span class="sxs-lookup"><span data-stu-id="95627-197">Log service encountered a partial or incomplete log block.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-198"><span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**\_ \_ Ungültiger Bereich im Fehlerprotokoll. \_**</span><span class="sxs-lookup"><span data-stu-id="95627-198"><span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**ERROR\_LOG\_INVALID\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-199">6604 (0x19cc)</span><span class="sxs-lookup"><span data-stu-id="95627-199">6604 (0x19CC)</span></span>
</dt> <dt>



<span data-ttu-id="95627-200">Der Protokolldienst hat versucht, auf Daten außerhalb des aktiven Protokoll Bereichs zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="95627-200">Log service encountered an attempt access data outside the active log range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-201"><span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**Fehler \_ Protokoll \_ Blöcke \_ aufgebraucht**</span><span class="sxs-lookup"><span data-stu-id="95627-201"><span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**ERROR\_LOG\_BLOCKS\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-202">6605 (0x19cd)</span><span class="sxs-lookup"><span data-stu-id="95627-202">6605 (0x19CD)</span></span>
</dt> <dt>



<span data-ttu-id="95627-203">Protokolldienst-Benutzer Marshalling Puffer sind erschöpft.</span><span class="sxs-lookup"><span data-stu-id="95627-203">Log service user marshalling buffers are exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-204"><span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**Fehler \_ Protokoll- \_ Lese \_ Kontext \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="95627-204"><span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**ERROR\_LOG\_READ\_CONTEXT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-205">6606 (0x19ce)</span><span class="sxs-lookup"><span data-stu-id="95627-205">6606 (0x19CE)</span></span>
</dt> <dt>



<span data-ttu-id="95627-206">Der Protokolldienst hat versucht, einen Lesevorgang aus einem Marshalling Bereich mit einem ungültigen Lese Kontext durchführen.</span><span class="sxs-lookup"><span data-stu-id="95627-206">Log service encountered an attempt read from a marshalling area with an invalid read context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-207"><span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**Fehler \_ Protokoll- \_ Neustart \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="95627-207"><span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**ERROR\_LOG\_RESTART\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-208">6607 (0x19cf)</span><span class="sxs-lookup"><span data-stu-id="95627-208">6607 (0x19CF)</span></span>
</dt> <dt>



<span data-ttu-id="95627-209">Der Protokolldienst hat einen ungültigen Protokoll Neustart Bereich gefunden.</span><span class="sxs-lookup"><span data-stu-id="95627-209">Log service encountered an invalid log restart area.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-210"><span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**Version des Fehler \_ Protokoll \_ Blocks \_**</span><span class="sxs-lookup"><span data-stu-id="95627-210"><span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**ERROR\_LOG\_BLOCK\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-211">6608 (0x19d0)</span><span class="sxs-lookup"><span data-stu-id="95627-211">6608 (0x19D0)</span></span>
</dt> <dt>



<span data-ttu-id="95627-212">Der Protokolldienst hat eine ungültige Protokoll Block Version gefunden.</span><span class="sxs-lookup"><span data-stu-id="95627-212">Log service encountered an invalid log block version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-213"><span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**der Fehler \_ Protokoll \_ Block ist \_ ungültig.**</span><span class="sxs-lookup"><span data-stu-id="95627-213"><span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**ERROR\_LOG\_BLOCK\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-214">6609 (0x19d1)</span><span class="sxs-lookup"><span data-stu-id="95627-214">6609 (0x19D1)</span></span>
</dt> <dt>



<span data-ttu-id="95627-215">Der Protokolldienst hat einen ungültigen Protokoll Block gefunden.</span><span class="sxs-lookup"><span data-stu-id="95627-215">Log service encountered an invalid log block.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-216"><span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**Fehler \_ Protokoll \_ - \_ Lesemodus \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="95627-216"><span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**ERROR\_LOG\_READ\_MODE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-217">6610 (0x19d2)</span><span class="sxs-lookup"><span data-stu-id="95627-217">6610 (0x19D2)</span></span>
</dt> <dt>



<span data-ttu-id="95627-218">Der Protokolldienst hat versucht, das Protokoll mit einem ungültigen Lesemodus zu lesen.</span><span class="sxs-lookup"><span data-stu-id="95627-218">Log service encountered an attempt to read the log with an invalid read mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-219"><span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**Fehler \_ Protokoll \_ kein \_ Neustart**</span><span class="sxs-lookup"><span data-stu-id="95627-219"><span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**ERROR\_LOG\_NO\_RESTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-220">6611 (0x19d3)</span><span class="sxs-lookup"><span data-stu-id="95627-220">6611 (0x19D3)</span></span>
</dt> <dt>



<span data-ttu-id="95627-221">Protokolldienst hat einen Protokolldaten Strom ohne Neustart Bereich gefunden.</span><span class="sxs-lookup"><span data-stu-id="95627-221">Log service encountered a log stream with no restart area.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-222"><span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**Fehler \_ Protokoll \_ Metadaten sind \_ beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="95627-222"><span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**ERROR\_LOG\_METADATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-223">6612 (0x19d4)</span><span class="sxs-lookup"><span data-stu-id="95627-223">6612 (0x19D4)</span></span>
</dt> <dt>



<span data-ttu-id="95627-224">Protokolldienst hat eine beschädigte Metadatendatei gefunden.</span><span class="sxs-lookup"><span data-stu-id="95627-224">Log service encountered a corrupted metadata file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-225"><span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**Fehler \_ Protokoll \_ Metadaten sind \_ ungültig.**</span><span class="sxs-lookup"><span data-stu-id="95627-225"><span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**ERROR\_LOG\_METADATA\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-226">6613 (0x19d5)</span><span class="sxs-lookup"><span data-stu-id="95627-226">6613 (0x19D5)</span></span>
</dt> <dt>



<span data-ttu-id="95627-227">Der Protokolldienst hat eine Metadatendatei gefunden, die nicht vom Protokolldatei System erstellt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="95627-227">Log service encountered a metadata file that could not be created by the log file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-228"><span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**Fehler \_ Protokoll \_ Metadaten \_ inkonsistent**</span><span class="sxs-lookup"><span data-stu-id="95627-228"><span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**ERROR\_LOG\_METADATA\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-229">6614 (0x19d6)</span><span class="sxs-lookup"><span data-stu-id="95627-229">6614 (0x19D6)</span></span>
</dt> <dt>



<span data-ttu-id="95627-230">Der Protokolldienst hat eine Metadatendatei mit inkonsistenten Daten gefunden.</span><span class="sxs-lookup"><span data-stu-id="95627-230">Log service encountered a metadata file with inconsistent data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-231"><span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**Fehler \_ Protokoll \_ Reservierung \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="95627-231"><span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**ERROR\_LOG\_RESERVATION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-232">6615 (0x19d7)</span><span class="sxs-lookup"><span data-stu-id="95627-232">6615 (0x19D7)</span></span>
</dt> <dt>



<span data-ttu-id="95627-233">Der Protokolldienst hat versucht, den Reservierungsbereich zu löschen oder zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="95627-233">Log service encountered an attempt to erroneous allocate or dispose reservation space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-234"><span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**Fehler \_ Protokoll \_ nicht \_ Löschen**</span><span class="sxs-lookup"><span data-stu-id="95627-234"><span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**ERROR\_LOG\_CANT\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-235">6616 (0x19d8)</span><span class="sxs-lookup"><span data-stu-id="95627-235">6616 (0x19D8)</span></span>
</dt> <dt>



<span data-ttu-id="95627-236">Der Protokolldienst kann die Protokolldatei oder den Dateisystem Container nicht löschen.</span><span class="sxs-lookup"><span data-stu-id="95627-236">Log service cannot delete log file or file system container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-237"><span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**Fehler \_ Protokoll- \_ Container \_ Limit \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="95627-237"><span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**ERROR\_LOG\_CONTAINER\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-238">6617 (0x19d9)</span><span class="sxs-lookup"><span data-stu-id="95627-238">6617 (0x19D9)</span></span>
</dt> <dt>



<span data-ttu-id="95627-239">Der Protokolldienst hat die maximal zulässige Anzahl von Containern erreicht, die einer Protokolldatei zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="95627-239">Log service has reached the maximum allowable containers allocated to a log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-240"><span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**\_ \_ \_ Protokoll Anfang des \_ Fehler Protokolls**</span><span class="sxs-lookup"><span data-stu-id="95627-240"><span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**ERROR\_LOG\_START\_OF\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-241">6618 (0x19da)</span><span class="sxs-lookup"><span data-stu-id="95627-241">6618 (0x19DA)</span></span>
</dt> <dt>



<span data-ttu-id="95627-242">Der Protokolldienst hat versucht, einen Rückstand nach dem Beginn des Protokolls zu lesen oder zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="95627-242">Log service has attempted to read or write backward past the start of the log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-243"><span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**die Fehler \_ Protokoll \_ Richtlinie ist \_ bereits \_ installiert.**</span><span class="sxs-lookup"><span data-stu-id="95627-243"><span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**ERROR\_LOG\_POLICY\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-244">6619 (0x19db)</span><span class="sxs-lookup"><span data-stu-id="95627-244">6619 (0x19DB)</span></span>
</dt> <dt>



<span data-ttu-id="95627-245">Die Protokoll Richtlinie konnte nicht installiert werden, da bereits eine Richtlinie desselben Typs vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="95627-245">Log policy could not be installed because a policy of the same type is already present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-246"><span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**die Fehler \_ Protokoll \_ Richtlinie ist \_ nicht \_ installiert.**</span><span class="sxs-lookup"><span data-stu-id="95627-246"><span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**ERROR\_LOG\_POLICY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-247">6620 (0x19dc)</span><span class="sxs-lookup"><span data-stu-id="95627-247">6620 (0x19DC)</span></span>
</dt> <dt>



<span data-ttu-id="95627-248">Die betreffende Protokoll Richtlinie wurde zum Zeitpunkt der Anforderung nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="95627-248">Log policy in question was not installed at the time of the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-249"><span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**die Fehler \_ Protokoll \_ Richtlinie ist \_ ungültig.**</span><span class="sxs-lookup"><span data-stu-id="95627-249"><span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**ERROR\_LOG\_POLICY\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-250">6621 (0x19dd)</span><span class="sxs-lookup"><span data-stu-id="95627-250">6621 (0x19DD)</span></span>
</dt> <dt>



<span data-ttu-id="95627-251">Der installierte Satz von Richtlinien für das Protokoll ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="95627-251">The installed set of policies on the log is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-252"><span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**Fehler \_ Protokoll- \_ Richtlinien \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="95627-252"><span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**ERROR\_LOG\_POLICY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-253">6622 (0x19de)</span><span class="sxs-lookup"><span data-stu-id="95627-253">6622 (0x19DE)</span></span>
</dt> <dt>



<span data-ttu-id="95627-254">Eine Richtlinie für das betreffende Protokoll hat verhindert, dass der Vorgang abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="95627-254">A policy on the log in question prevented the operation from completing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-255"><span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**Fehler \_ Protokoll- \_ fixierte \_ Archiv \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="95627-255"><span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**ERROR\_LOG\_PINNED\_ARCHIVE\_TAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-256">6623 (0x19df)</span><span class="sxs-lookup"><span data-stu-id="95627-256">6623 (0x19DF)</span></span>
</dt> <dt>



<span data-ttu-id="95627-257">Der Protokoll Speicher kann nicht freigegeben werden, da das Protokoll durch das Archiv Ende fixiert wird.</span><span class="sxs-lookup"><span data-stu-id="95627-257">Log space cannot be reclaimed because the log is pinned by the archive tail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-258"><span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**Fehler \_ Protokoll \_ Daten Satz \_ nicht vorhanden**</span><span class="sxs-lookup"><span data-stu-id="95627-258"><span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**ERROR\_LOG\_RECORD\_NONEXISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-259">6624 (0x19e0)</span><span class="sxs-lookup"><span data-stu-id="95627-259">6624 (0x19E0)</span></span>
</dt> <dt>



<span data-ttu-id="95627-260">Der Protokolldaten Satz ist kein Datensatz in der Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="95627-260">Log record is not a record in the log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-261"><span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**\_ \_ ungültige Fehlerprotokoll Datensätze \_ \_**</span><span class="sxs-lookup"><span data-stu-id="95627-261"><span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**ERROR\_LOG\_RECORDS\_RESERVED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-262">6625 (0x19e1)</span><span class="sxs-lookup"><span data-stu-id="95627-262">6625 (0x19E1)</span></span>
</dt> <dt>



<span data-ttu-id="95627-263">Die Anzahl der reservierten Protokolldaten Sätze oder die Anpassung der Anzahl der reservierten Protokolldaten Sätze ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="95627-263">Number of reserved log records or the adjustment of the number of reserved log records is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-264"><span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**\_ \_ Ungültiger Fehlerprotokoll Speicher. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="95627-264"><span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**ERROR\_LOG\_SPACE\_RESERVED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-265">6626 (0x19e2)</span><span class="sxs-lookup"><span data-stu-id="95627-265">6626 (0x19E2)</span></span>
</dt> <dt>



<span data-ttu-id="95627-266">Der reservierte Protokoll Speicher oder die Anpassung des Protokoll Speicherplatzes ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="95627-266">Reserved log space or the adjustment of the log space is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-267"><span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**Fehler \_ Protokoll \_ Ende \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="95627-267"><span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**ERROR\_LOG\_TAIL\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-268">6627 (0x19e3)</span><span class="sxs-lookup"><span data-stu-id="95627-268">6627 (0x19E3)</span></span>
</dt> <dt>



<span data-ttu-id="95627-269">Ein neues oder vorhandenes Archiv Ende oder eine Basis des aktiven Protokolls ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="95627-269">An new or existing archive tail or base of the active log is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-270"><span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**Fehler \_ Protokoll \_ voll**</span><span class="sxs-lookup"><span data-stu-id="95627-270"><span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**ERROR\_LOG\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-271">6628 (0x19e4)</span><span class="sxs-lookup"><span data-stu-id="95627-271">6628 (0x19E4)</span></span>
</dt> <dt>



<span data-ttu-id="95627-272">Der Protokoll Speicher ist erschöpft.</span><span class="sxs-lookup"><span data-stu-id="95627-272">Log space is exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-273"><span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**Fehler \_ beim \_ Ändern der Größe des \_ \_ Protokolls.**</span><span class="sxs-lookup"><span data-stu-id="95627-273"><span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**ERROR\_COULD\_NOT\_RESIZE\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-274">6629 (0x19e5)</span><span class="sxs-lookup"><span data-stu-id="95627-274">6629 (0x19E5)</span></span>
</dt> <dt>



<span data-ttu-id="95627-275">Das Protokoll konnte nicht auf die angeforderte Größe festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="95627-275">The log could not be set to the requested size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-276"><span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**Fehler \_ Protokoll \_ multiplexed**</span><span class="sxs-lookup"><span data-stu-id="95627-276"><span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**ERROR\_LOG\_MULTIPLEXED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-277">6630 (0x19e6)</span><span class="sxs-lookup"><span data-stu-id="95627-277">6630 (0x19E6)</span></span>
</dt> <dt>



<span data-ttu-id="95627-278">Das Protokoll ist multiplext, es sind keine direkten Schreibvorgänge in das physische Protokoll zulässig.</span><span class="sxs-lookup"><span data-stu-id="95627-278">Log is multiplexed, no direct writes to the physical log is allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-279"><span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**Fehler \_ Protokoll \_ dediziert**</span><span class="sxs-lookup"><span data-stu-id="95627-279"><span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**ERROR\_LOG\_DEDICATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-280">6631 (0x19e7)</span><span class="sxs-lookup"><span data-stu-id="95627-280">6631 (0x19E7)</span></span>
</dt> <dt>



<span data-ttu-id="95627-281">Der Vorgang ist fehlgeschlagen, da es sich um ein dediziertes Protokoll handelt.</span><span class="sxs-lookup"><span data-stu-id="95627-281">The operation failed because the log is a dedicated log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-282"><span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**Fehler \_ Protokoll \_ Archiv \_ wird \_ nicht \_ ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="95627-282"><span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**ERROR\_LOG\_ARCHIVE\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-283">6632 (0x19e8)</span><span class="sxs-lookup"><span data-stu-id="95627-283">6632 (0x19E8)</span></span>
</dt> <dt>



<span data-ttu-id="95627-284">Für den Vorgang ist ein Archiv Kontext erforderlich.</span><span class="sxs-lookup"><span data-stu-id="95627-284">The operation requires an archive context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-285"><span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**Fehler \_ Protokoll \_ Archiv \_ wird \_ ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="95627-285"><span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**ERROR\_LOG\_ARCHIVE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-286">6633 (0x19e9)</span><span class="sxs-lookup"><span data-stu-id="95627-286">6633 (0x19E9)</span></span>
</dt> <dt>



<span data-ttu-id="95627-287">Die Protokoll Archivierung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95627-287">Log archival is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-288"><span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**\_ \_ kurzlebige Fehlerprotokoll**</span><span class="sxs-lookup"><span data-stu-id="95627-288"><span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**ERROR\_LOG\_EPHEMERAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-289">6634 (0x19ea)</span><span class="sxs-lookup"><span data-stu-id="95627-289">6634 (0x19EA)</span></span>
</dt> <dt>



<span data-ttu-id="95627-290">Der Vorgang erfordert ein nicht kurzlebiges Protokoll, aber das Protokoll ist kurzlebig.</span><span class="sxs-lookup"><span data-stu-id="95627-290">The operation requires a non-ephemeral log, but the log is ephemeral.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-291"><span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**Fehler \_ Protokoll \_ nicht \_ genügend \_ Container**</span><span class="sxs-lookup"><span data-stu-id="95627-291"><span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**ERROR\_LOG\_NOT\_ENOUGH\_CONTAINERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-292">6635 (0x19eb)</span><span class="sxs-lookup"><span data-stu-id="95627-292">6635 (0x19EB)</span></span>
</dt> <dt>



<span data-ttu-id="95627-293">Das Protokoll muss mindestens zwei Container aufweisen, bevor es gelesen oder in das Protokoll geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="95627-293">The log must have at least two containers before it can be read from or written to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-294"><span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**der Fehler \_ Protokoll \_ Client wurde \_ bereits \_ registriert.**</span><span class="sxs-lookup"><span data-stu-id="95627-294"><span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**ERROR\_LOG\_CLIENT\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-295">6636 (0x19ec)</span><span class="sxs-lookup"><span data-stu-id="95627-295">6636 (0x19EC)</span></span>
</dt> <dt>



<span data-ttu-id="95627-296">Ein Protokoll Client wurde bereits im Stream registriert.</span><span class="sxs-lookup"><span data-stu-id="95627-296">A log client has already registered on the stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-297"><span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**Fehler \_ Protokoll \_ Client \_ nicht \_ registriert**</span><span class="sxs-lookup"><span data-stu-id="95627-297"><span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**ERROR\_LOG\_CLIENT\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-298">6637 (0x19ed)</span><span class="sxs-lookup"><span data-stu-id="95627-298">6637 (0x19ED)</span></span>
</dt> <dt>



<span data-ttu-id="95627-299">Ein Protokoll Client wurde nicht im Stream registriert.</span><span class="sxs-lookup"><span data-stu-id="95627-299">A log client has not been registered on the stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-300"><span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**Fehler \_ Protokoll \_ Vollständiger \_ Handler \_ in \_ Bearbeitung**</span><span class="sxs-lookup"><span data-stu-id="95627-300"><span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**ERROR\_LOG\_FULL\_HANDLER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-301">6638 (0x19ee)</span><span class="sxs-lookup"><span data-stu-id="95627-301">6638 (0x19EE)</span></span>
</dt> <dt>



<span data-ttu-id="95627-302">Es wurde bereits eine Anforderung zum Verarbeiten der vollständigen Protokolldatei vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="95627-302">A request has already been made to handle the log full condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-303"><span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**Fehler \_ Protokoll- \_ Container \_ Lese \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="95627-303"><span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**ERROR\_LOG\_CONTAINER\_READ\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-304">6639 (0x19ef)</span><span class="sxs-lookup"><span data-stu-id="95627-304">6639 (0x19EF)</span></span>
</dt> <dt>



<span data-ttu-id="95627-305">Fehler beim Protokolldienst beim Lesen aus einem Protokoll Container.</span><span class="sxs-lookup"><span data-stu-id="95627-305">Log service encountered an error when attempting to read from a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-306"><span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**Fehler beim Schreiben des Fehler \_ Protokoll \_ Containers. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="95627-306"><span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**ERROR\_LOG\_CONTAINER\_WRITE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-307">6640 (0x19f 0)</span><span class="sxs-lookup"><span data-stu-id="95627-307">6640 (0x19F0)</span></span>
</dt> <dt>



<span data-ttu-id="95627-308">Der Protokolldienst hat beim Schreiben in einen Protokoll Container einen Fehler gefunden.</span><span class="sxs-lookup"><span data-stu-id="95627-308">Log service encountered an error when attempting to write to a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-309"><span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**Fehler \_ Protokoll \_ Container \_ geöffnet \_**</span><span class="sxs-lookup"><span data-stu-id="95627-309"><span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**ERROR\_LOG\_CONTAINER\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-310">6641 (0x19f 1)</span><span class="sxs-lookup"><span data-stu-id="95627-310">6641 (0x19F1)</span></span>
</dt> <dt>



<span data-ttu-id="95627-311">Protokolldienst hat beim Versuch, einen Protokoll Container zu öffnen, einen Fehler ermittelt.</span><span class="sxs-lookup"><span data-stu-id="95627-311">Log service encountered an error when attempting open a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-312"><span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**Fehler \_ Protokoll- \_ Container \_ Status \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="95627-312"><span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**ERROR\_LOG\_CONTAINER\_STATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-313">6642 (0x19f 2)</span><span class="sxs-lookup"><span data-stu-id="95627-313">6642 (0x19F2)</span></span>
</dt> <dt>



<span data-ttu-id="95627-314">Der Protokolldienst hat beim Versuch einer angeforderten Aktion einen ungültigen Container Zustand fest.</span><span class="sxs-lookup"><span data-stu-id="95627-314">Log service encountered an invalid container state when attempting a requested action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-315"><span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**Fehler \_ Protokoll \_ Status \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="95627-315"><span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**ERROR\_LOG\_STATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-316">6643 (0x19f 3)</span><span class="sxs-lookup"><span data-stu-id="95627-316">6643 (0x19F3)</span></span>
</dt> <dt>



<span data-ttu-id="95627-317">Der Protokolldienst weist nicht den richtigen Status auf, um eine angeforderte Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="95627-317">Log service is not in the correct state to perform a requested action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-318"><span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**Fehler \_ Protokoll \_ fixiert**</span><span class="sxs-lookup"><span data-stu-id="95627-318"><span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**ERROR\_LOG\_PINNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-319">6644 (0x19f 4)</span><span class="sxs-lookup"><span data-stu-id="95627-319">6644 (0x19F4)</span></span>
</dt> <dt>



<span data-ttu-id="95627-320">Der Protokoll Speicher kann nicht freigegeben werden, da das Protokoll fixiert ist.</span><span class="sxs-lookup"><span data-stu-id="95627-320">Log space cannot be reclaimed because the log is pinned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-321"><span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**Fehler beim Leeren der Fehler \_ Protokoll \_ Metadaten. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="95627-321"><span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**ERROR\_LOG\_METADATA\_FLUSH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-322">6645 (0x19f 5)</span><span class="sxs-lookup"><span data-stu-id="95627-322">6645 (0x19F5)</span></span>
</dt> <dt>



<span data-ttu-id="95627-323">Fehler beim Leeren der Protokoll Metadaten.</span><span class="sxs-lookup"><span data-stu-id="95627-323">Log metadata flush failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-324"><span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**Fehler \_ Protokoll \_ inkonsistente \_ Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="95627-324"><span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**ERROR\_LOG\_INCONSISTENT\_SECURITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-325">6646 (0x19f 6)</span><span class="sxs-lookup"><span data-stu-id="95627-325">6646 (0x19F6)</span></span>
</dt> <dt>



<span data-ttu-id="95627-326">Die Sicherheitseinstellungen für das Protokoll und seine Container sind inkonsistent.</span><span class="sxs-lookup"><span data-stu-id="95627-326">Security on the log and its containers is inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-327"><span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**Fehler beim Anhängen des Fehler \_ Protokolls \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="95627-327"><span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**ERROR\_LOG\_APPENDED\_FLUSH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-328">6647 (0x19f)</span><span class="sxs-lookup"><span data-stu-id="95627-328">6647 (0x19F7)</span></span>
</dt> <dt>



<span data-ttu-id="95627-329">Es wurden Datensätze an das Protokoll angehängt, oder es wurden Reservierungs Änderungen vorgenommen, aber das Protokoll konnte nicht geleert werden.</span><span class="sxs-lookup"><span data-stu-id="95627-329">Records were appended to the log or reservation changes were made, but the log could not be flushed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-330"><span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**Fehler \_ Protokoll-feste \_ \_ Reservierung**</span><span class="sxs-lookup"><span data-stu-id="95627-330"><span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**ERROR\_LOG\_PINNED\_RESERVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-331">6648 (0x19f 8)</span><span class="sxs-lookup"><span data-stu-id="95627-331">6648 (0x19F8)</span></span>
</dt> <dt>



<span data-ttu-id="95627-332">Das Protokoll wird aufgrund einer Reservierung fixiert, die den größten Teil des Protokoll Speicherplatzes beansprucht.</span><span class="sxs-lookup"><span data-stu-id="95627-332">The log is pinned due to reservation consuming most of the log space.</span></span> <span data-ttu-id="95627-333">Freigeben von reservierten Datensätzen, um Speicherplatz verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="95627-333">Free some reserved records to make space available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-334"><span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**\_ungültige \_ Transaktion.**</span><span class="sxs-lookup"><span data-stu-id="95627-334"><span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**ERROR\_INVALID\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-335">6700 (0x1a2c)</span><span class="sxs-lookup"><span data-stu-id="95627-335">6700 (0x1A2C)</span></span>
</dt> <dt>



<span data-ttu-id="95627-336">Das diesem Vorgang zugeordnete Transaktions Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="95627-336">The transaction handle associated with this operation is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-337"><span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**Fehler \_ Transaktion \_ nicht \_ aktiv**</span><span class="sxs-lookup"><span data-stu-id="95627-337"><span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**ERROR\_TRANSACTION\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-338">6701 (0x1a2d)</span><span class="sxs-lookup"><span data-stu-id="95627-338">6701 (0x1A2D)</span></span>
</dt> <dt>



<span data-ttu-id="95627-339">Der angeforderte Vorgang wurde im Kontext einer Transaktion durchgeführt, die nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="95627-339">The requested operation was made in the context of a transaction that is no longer active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-340"><span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**Fehler \_ Transaktions \_ Anforderung \_ ist \_ ungültig.**</span><span class="sxs-lookup"><span data-stu-id="95627-340"><span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**ERROR\_TRANSACTION\_REQUEST\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-341">6702 (0x1a2e)</span><span class="sxs-lookup"><span data-stu-id="95627-341">6702 (0x1A2E)</span></span>
</dt> <dt>



<span data-ttu-id="95627-342">Der angeforderte Vorgang ist für das Transaktions Objekt im aktuellen Zustand ungültig.</span><span class="sxs-lookup"><span data-stu-id="95627-342">The requested operation is not valid on the Transaction object in its current state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-343"><span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**Fehler \_ Transaktion \_ nicht \_ angefordert**</span><span class="sxs-lookup"><span data-stu-id="95627-343"><span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**ERROR\_TRANSACTION\_NOT\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-344">6703 (0x1a2f)</span><span class="sxs-lookup"><span data-stu-id="95627-344">6703 (0x1A2F)</span></span>
</dt> <dt>



<span data-ttu-id="95627-345">Der Aufrufer hat eine Antwort-API aufgerufen, aber die Antwort wird nicht erwartet, da der TM die entsprechende Anforderung an den Aufrufer nicht ausgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="95627-345">The caller has called a response API, but the response is not expected because the TM did not issue the corresponding request to the caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-346"><span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**Fehler \_ Transaktion wurde \_ bereits \_ abgebrochen.**</span><span class="sxs-lookup"><span data-stu-id="95627-346"><span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**ERROR\_TRANSACTION\_ALREADY\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-347">6704 (0x1A30)</span><span class="sxs-lookup"><span data-stu-id="95627-347">6704 (0x1A30)</span></span>
</dt> <dt>



<span data-ttu-id="95627-348">Es ist zu spät, den angeforderten Vorgang auszuführen, da die Transaktion bereits abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="95627-348">It is too late to perform the requested operation, since the Transaction has already been aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-349"><span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**Fehler \_ Transaktion \_ bereits committet \_**</span><span class="sxs-lookup"><span data-stu-id="95627-349"><span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**ERROR\_TRANSACTION\_ALREADY\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-350">6705 (0x1a31)</span><span class="sxs-lookup"><span data-stu-id="95627-350">6705 (0x1A31)</span></span>
</dt> <dt>



<span data-ttu-id="95627-351">Es ist zu spät, den angeforderten Vorgang auszuführen, da für die Transaktion bereits ein Commit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="95627-351">It is too late to perform the requested operation, since the Transaction has already been committed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-352"><span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**Fehler bei der \_ \_ Initialisierung des Fehlers TM \_**</span><span class="sxs-lookup"><span data-stu-id="95627-352"><span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**ERROR\_TM\_INITIALIZATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-353">6706 (0x1a32)</span><span class="sxs-lookup"><span data-stu-id="95627-353">6706 (0x1A32)</span></span>
</dt> <dt>



<span data-ttu-id="95627-354">Der Transaktions-Manager konnte nicht erfolgreich initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="95627-354">The Transaction Manager was unable to be successfully initialized.</span></span> <span data-ttu-id="95627-355">Transaktive Vorgänge werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95627-355">Transacted operations are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-356"><span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**Fehler \_ ResourceManager schreibgeschützt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="95627-356"><span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ERROR\_RESOURCEMANAGER\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-357">6707 (0x1a33)</span><span class="sxs-lookup"><span data-stu-id="95627-357">6707 (0x1A33)</span></span>
</dt> <dt>



<span data-ttu-id="95627-358">Der angegebene ResourceManager hat keine Änderungen oder Aktualisierungen an der Ressource in dieser Transaktion vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="95627-358">The specified ResourceManager made no changes or updates to the resource under this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-359"><span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**Fehler \_ Transaktion \_ nicht \_ verknüpft**</span><span class="sxs-lookup"><span data-stu-id="95627-359"><span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**ERROR\_TRANSACTION\_NOT\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-360">6708 (0x1a34)</span><span class="sxs-lookup"><span data-stu-id="95627-360">6708 (0x1A34)</span></span>
</dt> <dt>



<span data-ttu-id="95627-361">Der Ressourcen-Manager hat versucht, eine Transaktion vorzubereiten, der er nicht erfolgreich hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="95627-361">The resource manager has attempted to prepare a transaction that it has not successfully joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-362"><span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**Fehler bei der über \_ \_ geordneten Transaktion \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="95627-362"><span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**ERROR\_TRANSACTION\_SUPERIOR\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-363">6709 (0x1a35)</span><span class="sxs-lookup"><span data-stu-id="95627-363">6709 (0x1A35)</span></span>
</dt> <dt>



<span data-ttu-id="95627-364">Das Transaktions Objekt weist bereits eine übergeordnete Eintragung auf, und der Aufrufer hat versucht, einen Vorgang auszuführen, der einen neuen übergeordneten erstellt hätte.</span><span class="sxs-lookup"><span data-stu-id="95627-364">The Transaction object already has a superior enlistment, and the caller attempted an operation that would have created a new superior.</span></span> <span data-ttu-id="95627-365">Nur eine einzige übergeordnete Eintragung ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="95627-365">Only a single superior enlistment is allow.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-366"><span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**Error \_ CRM- \_ Protokoll ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="95627-366"><span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**ERROR\_CRM\_PROTOCOL\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-367">6710 (0x1a36)</span><span class="sxs-lookup"><span data-stu-id="95627-367">6710 (0x1A36)</span></span>
</dt> <dt>



<span data-ttu-id="95627-368">Der RM hat versucht, ein bereits vorhandener Protokoll zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="95627-368">The RM tried to register a protocol that already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-369"><span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**Fehler bei Transaktions Weitergabe \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="95627-369"><span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**ERROR\_TRANSACTION\_PROPAGATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-370">6711 (0x1a37)</span><span class="sxs-lookup"><span data-stu-id="95627-370">6711 (0x1A37)</span></span>
</dt> <dt>



<span data-ttu-id="95627-371">Fehler beim Übertragen der Transaktion.</span><span class="sxs-lookup"><span data-stu-id="95627-371">The attempt to propagate the Transaction failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-372"><span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**Fehler- \_ CRM- \_ Protokoll \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="95627-372"><span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**ERROR\_CRM\_PROTOCOL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-373">6712 (0x1a38)</span><span class="sxs-lookup"><span data-stu-id="95627-373">6712 (0x1A38)</span></span>
</dt> <dt>



<span data-ttu-id="95627-374">Das angeforderte propagierungs Protokoll wurde nicht als CRM registriert.</span><span class="sxs-lookup"><span data-stu-id="95627-374">The requested propagation protocol was not registered as a CRM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-375"><span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**Fehler \_ Transaktion \_ ungültiger \_ Mars Hall \_ Puffer.**</span><span class="sxs-lookup"><span data-stu-id="95627-375"><span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**ERROR\_TRANSACTION\_INVALID\_MARSHALL\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-376">6713 (0x1a39)</span><span class="sxs-lookup"><span data-stu-id="95627-376">6713 (0x1A39)</span></span>
</dt> <dt>



<span data-ttu-id="95627-377">Der an PushTransaction oder PullTransaction weiter gegebene Puffer weist kein gültiges Format auf.</span><span class="sxs-lookup"><span data-stu-id="95627-377">The buffer passed in to PushTransaction or PullTransaction is not in a valid format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-378"><span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**Fehler der \_ aktuellen \_ Transaktion ist \_ \_ ungültig.**</span><span class="sxs-lookup"><span data-stu-id="95627-378"><span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**ERROR\_CURRENT\_TRANSACTION\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-379">6714 (0x1a3a)</span><span class="sxs-lookup"><span data-stu-id="95627-379">6714 (0x1A3A)</span></span>
</dt> <dt>



<span data-ttu-id="95627-380">Der dem Thread zugeordnete aktuelle Transaktionskontext ist kein gültiges Handle für ein Transaktions Objekt.</span><span class="sxs-lookup"><span data-stu-id="95627-380">The current transaction context associated with the thread is not a valid handle to a transaction object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-381"><span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**Fehler \_ Transaktion \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="95627-381"><span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**ERROR\_TRANSACTION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-382">6715 (0x1a3b)</span><span class="sxs-lookup"><span data-stu-id="95627-382">6715 (0x1A3B)</span></span>
</dt> <dt>



<span data-ttu-id="95627-383">Das angegebene Transaktions Objekt konnte nicht geöffnet werden, da es nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="95627-383">The specified Transaction object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-384"><span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**Fehler \_ ResourceManager \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="95627-384"><span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**ERROR\_RESOURCEMANAGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-385">6716 (0x1a3c)</span><span class="sxs-lookup"><span data-stu-id="95627-385">6716 (0x1A3C)</span></span>
</dt> <dt>



<span data-ttu-id="95627-386">Das angegebene ResourceManager-Objekt konnte nicht geöffnet werden, da es nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="95627-386">The specified ResourceManager object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-387"><span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**Fehler \_ Eintragung \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="95627-387"><span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**ERROR\_ENLISTMENT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-388">6717 (0x1a3d)</span><span class="sxs-lookup"><span data-stu-id="95627-388">6717 (0x1A3D)</span></span>
</dt> <dt>



<span data-ttu-id="95627-389">Das angegebene Enlistment-Objekt konnte nicht geöffnet werden, da es nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="95627-389">The specified Enlistment object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-390"><span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**Fehler " \_ transaktionmanager" \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="95627-390"><span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**ERROR\_TRANSACTIONMANAGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-391">6718 (0x1a3e)</span><span class="sxs-lookup"><span data-stu-id="95627-391">6718 (0x1A3E)</span></span>
</dt> <dt>



<span data-ttu-id="95627-392">Das angegebene transaktionmanager-Objekt konnte nicht geöffnet werden, da es nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="95627-392">The specified TransactionManager object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-393"><span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**Fehler " \_ transaktionmanager" ist \_ nicht \_ Online.**</span><span class="sxs-lookup"><span data-stu-id="95627-393"><span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**ERROR\_TRANSACTIONMANAGER\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-394">6719 (0x1a3f)</span><span class="sxs-lookup"><span data-stu-id="95627-394">6719 (0x1A3F)</span></span>
</dt> <dt>



<span data-ttu-id="95627-395">Das angegebene Objekt konnte nicht erstellt oder geöffnet werden, da der zugehörige transaktionmanager nicht online ist.</span><span class="sxs-lookup"><span data-stu-id="95627-395">The object specified could not be created or opened, because its associated TransactionManager is not online.</span></span> <span data-ttu-id="95627-396">Der Transaktionsmanager muss vollständig online geschaltet werden, indem wieder herstelltransaktionsmanager aufgerufen wird, um das Ende der Protokolldatei wiederherzustellen, bevor Objekte in den zugehörigen Transaktions-oder ResourceManager-Namespaces geöffnet werden können.</span><span class="sxs-lookup"><span data-stu-id="95627-396">The TransactionManager must be brought fully Online by calling RecoverTransactionManager to recover to the end of its LogFile before objects in its Transaction or ResourceManager namespaces can be opened.</span></span> <span data-ttu-id="95627-397">Außerdem können Fehler beim Schreiben von Datensätzen in die Protokolldatei bewirken, dass ein transaktionmanager offline geschaltet wird.</span><span class="sxs-lookup"><span data-stu-id="95627-397">In addition, errors in writing records to its LogFile can cause a TransactionManager to go offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-398"><span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**Fehler beim \_ Transaktions-Manager- \_ Wiederherstellungs \_ namens \_ Konflikt.**</span><span class="sxs-lookup"><span data-stu-id="95627-398"><span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERROR\_TRANSACTIONMANAGER\_RECOVERY\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-399">6720 (0x1a40)</span><span class="sxs-lookup"><span data-stu-id="95627-399">6720 (0x1A40)</span></span>
</dt> <dt>



<span data-ttu-id="95627-400">Der angegebene transaktionmanager konnte die Objekte, die in der Protokolldatei enthalten sind, nicht im ob-Namespace erstellen.</span><span class="sxs-lookup"><span data-stu-id="95627-400">The specified TransactionManager was unable to create the objects contained in its logfile in the Ob namespace.</span></span> <span data-ttu-id="95627-401">Daher konnte transaktionmanager nicht wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="95627-401">Therefore, the TransactionManager was unable to recover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-402"><span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**Fehler \_ Transaktion \_ nicht \_ root**</span><span class="sxs-lookup"><span data-stu-id="95627-402"><span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**ERROR\_TRANSACTION\_NOT\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-403">6721 (0x1a41)</span><span class="sxs-lookup"><span data-stu-id="95627-403">6721 (0x1A41)</span></span>
</dt> <dt>



<span data-ttu-id="95627-404">Der-Befehl zum Erstellen einer übergeordneten Eintragung für dieses Transaktions Objekt konnte nicht abgeschlossen werden, da das für die Eintragung angegebene Transaktions Objekt eine untergeordnete Verzweigung der Transaktion ist.</span><span class="sxs-lookup"><span data-stu-id="95627-404">The call to create a superior Enlistment on this Transaction object could not be completed, because the Transaction object specified for the enlistment is a subordinate branch of the Transaction.</span></span> <span data-ttu-id="95627-405">Nur der Stamm der Transaktion kann als übergeordnetes Element eingetragen werden.</span><span class="sxs-lookup"><span data-stu-id="95627-405">Only the root of the Transaction can be enlisted on as a superior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-406"><span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**Fehler \_ Transaktions \_ Objekt ist \_ abgelaufen.**</span><span class="sxs-lookup"><span data-stu-id="95627-406"><span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**ERROR\_TRANSACTION\_OBJECT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-407">6722 (0x1a42)</span><span class="sxs-lookup"><span data-stu-id="95627-407">6722 (0x1A42)</span></span>
</dt> <dt>



<span data-ttu-id="95627-408">Da der zugeordnete Transaktions-Manager oder der zugehörige Ressourcen-Manager geschlossen wurde, ist das Handle nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="95627-408">Because the associated transaction manager or resource manager has been closed, the handle is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-409"><span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**Fehler \_ Transaktions \_ Antwort \_ nicht \_ eingetragen**</span><span class="sxs-lookup"><span data-stu-id="95627-409"><span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**ERROR\_TRANSACTION\_RESPONSE\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-410">6723 (0x1a43)</span><span class="sxs-lookup"><span data-stu-id="95627-410">6723 (0x1A43)</span></span>
</dt> <dt>



<span data-ttu-id="95627-411">Der angegebene Vorgang konnte für diese übergeordnete Eintragung nicht ausgeführt werden, da die Eintragung nicht mit der entsprechenden Vervollständigungs Antwort in notificationmask erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="95627-411">The specified operation could not be performed on this Superior enlistment, because the enlistment was not created with the corresponding completion response in the NotificationMask.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-412"><span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**Fehler \_ Transaktions \_ Daten Satz \_ zu \_ lang**</span><span class="sxs-lookup"><span data-stu-id="95627-412"><span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**ERROR\_TRANSACTION\_RECORD\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-413">6724 (0x1a44)</span><span class="sxs-lookup"><span data-stu-id="95627-413">6724 (0x1A44)</span></span>
</dt> <dt>



<span data-ttu-id="95627-414">Der angegebene Vorgang konnte nicht ausgeführt werden, da der zu protokollierende Datensatz zu lang war.</span><span class="sxs-lookup"><span data-stu-id="95627-414">The specified operation could not be performed, because the record that would be logged was too long.</span></span> <span data-ttu-id="95627-415">Dies kann auf zwei Bedingungen auftreten: entweder gibt es zu viele Einfügungen für diese Transaktion, oder die kombinierten Wiederherstellungsinformationen, die im Auftrag dieser Eintragung protokolliert werden, sind zu lang.</span><span class="sxs-lookup"><span data-stu-id="95627-415">This can occur because of two conditions: either there are too many Enlistments on this Transaction, or the combined RecoveryInformation being logged on behalf of those Enlistments is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-416"><span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**die \_ implizite \_ Transaktion \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="95627-416"><span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**ERROR\_IMPLICIT\_TRANSACTION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-417">6725 (0x1a45)</span><span class="sxs-lookup"><span data-stu-id="95627-417">6725 (0x1A45)</span></span>
</dt> <dt>



<span data-ttu-id="95627-418">Implizite Transaktionen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95627-418">Implicit transaction are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-419"><span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**Fehler \_ Transaktions \_ Integrität \_ verletzt**</span><span class="sxs-lookup"><span data-stu-id="95627-419"><span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**ERROR\_TRANSACTION\_INTEGRITY\_VIOLATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-420">6726 (0x1a46)</span><span class="sxs-lookup"><span data-stu-id="95627-420">6726 (0x1A46)</span></span>
</dt> <dt>



<span data-ttu-id="95627-421">Der Kerneltransaktions-Manager musste die Transaktion abbrechen oder vergessen, da der Fortschritt des Vorgangs blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="95627-421">The kernel transaction manager had to abort or forget the transaction because it blocked forward progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-422"><span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**Fehler bei der \_ transaktionmanager- \_ Identitäts \_ Übereinstimmung.**</span><span class="sxs-lookup"><span data-stu-id="95627-422"><span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERROR\_TRANSACTIONMANAGER\_IDENTITY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-423">6727 (0x1a47)</span><span class="sxs-lookup"><span data-stu-id="95627-423">6727 (0x1A47)</span></span>
</dt> <dt>



<span data-ttu-id="95627-424">Die bereitgestellte transaktionmanager-Identität entsprach nicht der in der Protokolldatei des Transaktions-Managers aufgezeichneten.</span><span class="sxs-lookup"><span data-stu-id="95627-424">The TransactionManager identity that was supplied did not match the one recorded in the TransactionManager's log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-425"><span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**Fehler \_ RM \_ kann \_ \_ für die \_ \_ Momentaufnahme nicht eingefroren werden.**</span><span class="sxs-lookup"><span data-stu-id="95627-425"><span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**ERROR\_RM\_CANNOT\_BE\_FROZEN\_FOR\_SNAPSHOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-426">6728 (0x1a48)</span><span class="sxs-lookup"><span data-stu-id="95627-426">6728 (0x1A48)</span></span>
</dt> <dt>



<span data-ttu-id="95627-427">Dieser Momentaufnahme Vorgang kann nicht fortgesetzt werden, da ein transaktionaler Ressourcen-Manager im aktuellen Zustand nicht fixiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="95627-427">This snapshot operation cannot continue because a transactional resource manager cannot be frozen in its current state.</span></span> <span data-ttu-id="95627-428">Versuchen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="95627-428">Please try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-429"><span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**Fehler beim Überschreiben der \_ Transaktion \_ \_**</span><span class="sxs-lookup"><span data-stu-id="95627-429"><span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**ERROR\_TRANSACTION\_MUST\_WRITETHROUGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-430">6729 (0x1a49)</span><span class="sxs-lookup"><span data-stu-id="95627-430">6729 (0x1A49)</span></span>
</dt> <dt>



<span data-ttu-id="95627-431">Die Transaktion kann nicht mit der angegebenen enlistmentmask eingetragen werden, weil die Transaktion die vorvorbereitungs Phase bereits abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="95627-431">The transaction cannot be enlisted on with the specified EnlistmentMask, because the transaction has already completed the PrePrepare phase.</span></span> <span data-ttu-id="95627-432">Um die Richtigkeit sicherzustellen, muss der ResourceManager zu einem Lese-/Schreibmodus wechseln und das Zwischenspeichern von Daten innerhalb dieser Transaktion beenden.</span><span class="sxs-lookup"><span data-stu-id="95627-432">In order to ensure correctness, the ResourceManager must switch to a write- through mode and cease caching data within this transaction.</span></span> <span data-ttu-id="95627-433">Die Eintragung nur für nachfolgende Transaktions Phasen ist möglicherweise dennoch erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="95627-433">Enlisting for only subsequent transaction phases may still succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-434"><span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**Fehler \_ Transaktion \_ keine über \_ geordnete Transaktion**</span><span class="sxs-lookup"><span data-stu-id="95627-434"><span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**ERROR\_TRANSACTION\_NO\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-435">6730 (0x1a4a)</span><span class="sxs-lookup"><span data-stu-id="95627-435">6730 (0x1A4A)</span></span>
</dt> <dt>



<span data-ttu-id="95627-436">Die Transaktion weist keine übergeordnete Eintragung auf.</span><span class="sxs-lookup"><span data-stu-id="95627-436">The transaction does not have a superior enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-437"><span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**Fehler \_ heuristischer \_ Schaden \_**</span><span class="sxs-lookup"><span data-stu-id="95627-437"><span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**ERROR\_HEURISTIC\_DAMAGE\_POSSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-438">6731 (0x1a4b)</span><span class="sxs-lookup"><span data-stu-id="95627-438">6731 (0x1A4B)</span></span>
</dt> <dt>



<span data-ttu-id="95627-439">Der Versuch, einen Commit für die Transaktion durchzuführen, wurde abgeschlossen, es ist jedoch möglich, dass ein Teil der Transaktionsstruktur aufgrund der Heuristik nicht erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="95627-439">The attempt to commit the Transaction completed, but it is possible that some portion of the transaction tree did not commit successfully due to heuristics.</span></span> <span data-ttu-id="95627-440">Daher ist es möglich, dass für einige Daten, die in der Transaktion geändert wurden, möglicherweise kein Commit ausgeführt wurde, was zu Transaktions Inkonsistenz führt.</span><span class="sxs-lookup"><span data-stu-id="95627-440">Therefore it is possible that some data modified in the transaction may not have committed, resulting in transactional inconsistency.</span></span> <span data-ttu-id="95627-441">Überprüfen Sie nach Möglichkeit die Konsistenz der zugehörigen Daten.</span><span class="sxs-lookup"><span data-stu-id="95627-441">If possible, check the consistency of the associated data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-442"><span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**Fehler \_ Transaktions \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="95627-442"><span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**ERROR\_TRANSACTIONAL\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-443">6800 (0x1a90)</span><span class="sxs-lookup"><span data-stu-id="95627-443">6800 (0x1A90)</span></span>
</dt> <dt>



<span data-ttu-id="95627-444">Die Funktion hat versucht, einen Namen zu verwenden, der für die Verwendung durch eine andere Transaktion reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="95627-444">The function attempted to use a name that is reserved for use by another transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-445"><span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**Fehler \_ RM \_ nicht \_ aktiv**</span><span class="sxs-lookup"><span data-stu-id="95627-445"><span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**ERROR\_RM\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-446">6801 (0x1a91)</span><span class="sxs-lookup"><span data-stu-id="95627-446">6801 (0x1A91)</span></span>
</dt> <dt>



<span data-ttu-id="95627-447">Die Transaktionsunterstützung innerhalb des angegebenen Ressourcen-Managers wurde nicht gestartet oder wurde aufgrund eines Fehlers heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="95627-447">Transaction support within the specified resource manager is not started or was shut down due to an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-448"><span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**Fehler \_ RM- \_ Metadaten \_ beschädigt**</span><span class="sxs-lookup"><span data-stu-id="95627-448"><span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**ERROR\_RM\_METADATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-449">6802 (0x1a92)</span><span class="sxs-lookup"><span data-stu-id="95627-449">6802 (0x1A92)</span></span>
</dt> <dt>



<span data-ttu-id="95627-450">Die Metadaten des RM sind beschädigt.</span><span class="sxs-lookup"><span data-stu-id="95627-450">The metadata of the RM has been corrupted.</span></span> <span data-ttu-id="95627-451">Der RM funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="95627-451">The RM will not function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-452"><span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**Fehler \_ Verzeichnis \_ nicht \_ RM**</span><span class="sxs-lookup"><span data-stu-id="95627-452"><span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**ERROR\_DIRECTORY\_NOT\_RM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-453">6803 (0x1a93)</span><span class="sxs-lookup"><span data-stu-id="95627-453">6803 (0x1A93)</span></span>
</dt> <dt>



<span data-ttu-id="95627-454">Das angegebene Verzeichnis enthält keinen Ressourcen-Manager.</span><span class="sxs-lookup"><span data-stu-id="95627-454">The specified directory does not contain a resource manager.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-455"><span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**\_ \_ nicht unterstützte Remote Fehler Transaktionen \_**</span><span class="sxs-lookup"><span data-stu-id="95627-455"><span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**ERROR\_TRANSACTIONS\_UNSUPPORTED\_REMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-456">6805 (0x1a95)</span><span class="sxs-lookup"><span data-stu-id="95627-456">6805 (0x1A95)</span></span>
</dt> <dt>



<span data-ttu-id="95627-457">Der Remote Server oder die Freigabe unterstützt keine transaktiven Datei Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="95627-457">The remote server or share does not support transacted file operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-458"><span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**Größe des Fehler \_ Protokoll- \_ Größenänderung ist \_ ungültig \_ .**</span><span class="sxs-lookup"><span data-stu-id="95627-458"><span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**ERROR\_LOG\_RESIZE\_INVALID\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-459">6806 (0x1a96)</span><span class="sxs-lookup"><span data-stu-id="95627-459">6806 (0x1A96)</span></span>
</dt> <dt>



<span data-ttu-id="95627-460">Die angeforderte Protokoll Größe ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="95627-460">The requested log size is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-461"><span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**das Fehler \_ Objekt ist \_ nicht \_ mehr \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="95627-461"><span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**ERROR\_OBJECT\_NO\_LONGER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-462">6807 (0x1a97)</span><span class="sxs-lookup"><span data-stu-id="95627-462">6807 (0x1A97)</span></span>
</dt> <dt>



<span data-ttu-id="95627-463">Das Objekt (Datei, Stream, Link), das dem Handle entspricht, wurde durch ein Sicherungspunkt-Rollback für die Transaktion gelöscht.</span><span class="sxs-lookup"><span data-stu-id="95627-463">The object (file, stream, link) corresponding to the handle has been deleted by a Transaction Savepoint Rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-464"><span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**Fehler Daten \_ Strom- \_ Miniversion wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="95627-464"><span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**ERROR\_STREAM\_MINIVERSION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-465">6808 (0x1a98)</span><span class="sxs-lookup"><span data-stu-id="95627-465">6808 (0x1A98)</span></span>
</dt> <dt>



<span data-ttu-id="95627-466">Die angegebene Triggerszenarios der Datei wurde für die geöffnete Transaktions Datei nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="95627-466">The specified file miniversion was not found for this transacted file open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-467"><span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**Fehler Daten \_ Strom- \_ Miniversion ist \_ \_ ungültig.**</span><span class="sxs-lookup"><span data-stu-id="95627-467"><span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**ERROR\_STREAM\_MINIVERSION\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-468">6809 (0x1a99)</span><span class="sxs-lookup"><span data-stu-id="95627-468">6809 (0x1A99)</span></span>
</dt> <dt>



<span data-ttu-id="95627-469">Die angegebene Triggerszenarios der Datei wurde gefunden, Sie wurde jedoch für ungültig erklärt.</span><span class="sxs-lookup"><span data-stu-id="95627-469">The specified file miniversion was found but has been invalidated.</span></span> <span data-ttu-id="95627-470">Die wahrscheinlichste Ursache ist ein Sicherungspunkt-Rollback für die Transaktion.</span><span class="sxs-lookup"><span data-stu-id="95627-470">Most likely cause is a transaction savepoint rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-471"><span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**Fehler \_ Miniversion \_ \_ von der \_ angegebenen Transaktion aus nicht zugänglich \_**</span><span class="sxs-lookup"><span data-stu-id="95627-471"><span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**ERROR\_MINIVERSION\_INACCESSIBLE\_FROM\_SPECIFIED\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-472">6810 (0x1a9a)</span><span class="sxs-lookup"><span data-stu-id="95627-472">6810 (0x1A9A)</span></span>
</dt> <dt>



<span data-ttu-id="95627-473">Eine Triggerszenarios kann nur im Kontext der Transaktion geöffnet werden, von der Sie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="95627-473">A miniversion may only be opened in the context of the transaction that created it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-474"><span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**Fehler \_ \_ beim Öffnen \_ von Miniversion \_ mit Änderungs \_ \_ Absicht.**</span><span class="sxs-lookup"><span data-stu-id="95627-474"><span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ERROR\_CANT\_OPEN\_MINIVERSION\_WITH\_MODIFY\_INTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-475">6811 (0x1a9b)</span><span class="sxs-lookup"><span data-stu-id="95627-475">6811 (0x1A9B)</span></span>
</dt> <dt>



<span data-ttu-id="95627-476">Es ist nicht möglich, eine Triggerszenarios mit Änderungs Zugriff zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="95627-476">It is not possible to open a miniversion with modify access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-477"><span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**Fehler \_ beim \_ Erstellen von \_ weiteren \_ Stream- \_ Miniversionen.**</span><span class="sxs-lookup"><span data-stu-id="95627-477"><span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**ERROR\_CANT\_CREATE\_MORE\_STREAM\_MINIVERSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-478">6812 (0x1a9c)</span><span class="sxs-lookup"><span data-stu-id="95627-478">6812 (0x1A9C)</span></span>
</dt> <dt>



<span data-ttu-id="95627-479">Es ist nicht möglich, weitere miniversions für diesen Stream zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="95627-479">It is not possible to create any more miniversions for this stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-480"><span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**Fehler bei \_ Remote \_ Datei \_ Version \_ .**</span><span class="sxs-lookup"><span data-stu-id="95627-480"><span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**ERROR\_REMOTE\_FILE\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-481">6814 (0x1a9e)</span><span class="sxs-lookup"><span data-stu-id="95627-481">6814 (0x1A9E)</span></span>
</dt> <dt>



<span data-ttu-id="95627-482">Der Remote Server hat eine nicht übereinstimmende Versionsnummer oder FID für eine Datei gesendet, die mit Transaktionen geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="95627-482">The remote server sent mismatching version number or Fid for a file opened with transactions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-483"><span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**Fehler \_ handle ist \_ nicht \_ mehr \_ gültig.**</span><span class="sxs-lookup"><span data-stu-id="95627-483"><span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**ERROR\_HANDLE\_NO\_LONGER\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-484">6815 (0x1a9f)</span><span class="sxs-lookup"><span data-stu-id="95627-484">6815 (0x1A9F)</span></span>
</dt> <dt>



<span data-ttu-id="95627-485">Das Handle wurde durch eine Transaktion für ungültig erklärt.</span><span class="sxs-lookup"><span data-stu-id="95627-485">The handle has been invalidated by a transaction.</span></span> <span data-ttu-id="95627-486">Die wahrscheinlichste Ursache ist das vorhanden sein einer Speicher Zuordnung für eine Datei oder ein geöffnetes Handle, wenn die Transaktion beendet oder auf Sicherungspunkt zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="95627-486">The most likely cause is the presence of memory mapping on a file or an open handle when the transaction ended or rolled back to savepoint.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-487"><span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**Fehler \_ keine \_ TxF- \_ Metadaten.**</span><span class="sxs-lookup"><span data-stu-id="95627-487"><span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**ERROR\_NO\_TXF\_METADATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-488">6816 (0x1aa0)</span><span class="sxs-lookup"><span data-stu-id="95627-488">6816 (0x1AA0)</span></span>
</dt> <dt>



<span data-ttu-id="95627-489">Es sind keine Transaktions Metadaten für die Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="95627-489">There is no transaction metadata on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-490"><span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**Fehler \_ Protokoll \_ Beschädigung \_ erkannt**</span><span class="sxs-lookup"><span data-stu-id="95627-490"><span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**ERROR\_LOG\_CORRUPTION\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-491">6817 (0x1aa1)</span><span class="sxs-lookup"><span data-stu-id="95627-491">6817 (0x1AA1)</span></span>
</dt> <dt>



<span data-ttu-id="95627-492">Die Protokolldaten sind beschädigt.</span><span class="sxs-lookup"><span data-stu-id="95627-492">The log data is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-493"><span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**Fehler \_ \_ bei der Wiederherstellung \_ mit dem \_ \_ geöffneten handle.**</span><span class="sxs-lookup"><span data-stu-id="95627-493"><span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**ERROR\_CANT\_RECOVER\_WITH\_HANDLE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-494">6818 (0x1aa2)</span><span class="sxs-lookup"><span data-stu-id="95627-494">6818 (0x1AA2)</span></span>
</dt> <dt>



<span data-ttu-id="95627-495">Die Datei kann nicht wieder hergestellt werden, da noch ein Handle geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="95627-495">The file can't be recovered because there is a handle still open on it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-496"><span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**Fehler \_ RM \_ getrennt**</span><span class="sxs-lookup"><span data-stu-id="95627-496"><span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**ERROR\_RM\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-497">6819 (0x1aa3)</span><span class="sxs-lookup"><span data-stu-id="95627-497">6819 (0x1AA3)</span></span>
</dt> <dt>



<span data-ttu-id="95627-498">Das Transaktions Ergebnis ist nicht verfügbar, da der für die IT Verantwortliche Ressourcen-Manager getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="95627-498">The transaction outcome is unavailable because the resource manager responsible for it has disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-499"><span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**Fehler \_ Eintragung ist \_ nicht über \_ geordneter Name**</span><span class="sxs-lookup"><span data-stu-id="95627-499"><span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**ERROR\_ENLISTMENT\_NOT\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-500">6820 (0x1aa4)</span><span class="sxs-lookup"><span data-stu-id="95627-500">6820 (0x1AA4)</span></span>
</dt> <dt>



<span data-ttu-id="95627-501">Die Anforderung wurde zurückgewiesen, weil es sich bei der fraglichen Eintragung nicht um eine überragende Eintragung handelt.</span><span class="sxs-lookup"><span data-stu-id="95627-501">The request was rejected because the enlistment in question is not a superior enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-502"><span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**Fehler \_ Wiederherstellung \_ nicht \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="95627-502"><span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**ERROR\_RECOVERY\_NOT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-503">6821 (0x1aa5)</span><span class="sxs-lookup"><span data-stu-id="95627-503">6821 (0x1AA5)</span></span>
</dt> <dt>



<span data-ttu-id="95627-504">Der transaktionale Ressourcen-Manager ist bereits konsistent.</span><span class="sxs-lookup"><span data-stu-id="95627-504">The transactional resource manager is already consistent.</span></span> <span data-ttu-id="95627-505">Die Wiederherstellung ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="95627-505">Recovery is not needed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-506"><span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**Fehler \_ RM \_ bereits \_ gestartet**</span><span class="sxs-lookup"><span data-stu-id="95627-506"><span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**ERROR\_RM\_ALREADY\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-507">6822 (0x1aa6)</span><span class="sxs-lookup"><span data-stu-id="95627-507">6822 (0x1AA6)</span></span>
</dt> <dt>



<span data-ttu-id="95627-508">Der transaktionale Ressourcen-Manager wurde bereits gestartet.</span><span class="sxs-lookup"><span data-stu-id="95627-508">The transactional resource manager has already been started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-509"><span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**Fehler \_ Datei \_ Identität \_ nicht \_ persistent**</span><span class="sxs-lookup"><span data-stu-id="95627-509"><span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**ERROR\_FILE\_IDENTITY\_NOT\_PERSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-510">6823 (0x1aa7)</span><span class="sxs-lookup"><span data-stu-id="95627-510">6823 (0x1AA7)</span></span>
</dt> <dt>



<span data-ttu-id="95627-511">Die Datei kann nicht transaktional geöffnet werden, da ihre Identität vom Ergebnis einer nicht aufgelösten Transaktion abhängt.</span><span class="sxs-lookup"><span data-stu-id="95627-511">The file cannot be opened transactionally, because its identity depends on the outcome of an unresolved transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-512"><span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**Fehler \_ beim \_ Abbrechen der \_ Transaktions \_ Abhängigkeit.**</span><span class="sxs-lookup"><span data-stu-id="95627-512"><span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**ERROR\_CANT\_BREAK\_TRANSACTIONAL\_DEPENDENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-513">6824 (0x1aa8)</span><span class="sxs-lookup"><span data-stu-id="95627-513">6824 (0x1AA8)</span></span>
</dt> <dt>



<span data-ttu-id="95627-514">Der Vorgang kann nicht ausgeführt werden, da eine andere Transaktion von der Tatsache abhängig ist, dass diese Eigenschaft nicht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="95627-514">The operation cannot be performed because another transaction is depending on the fact that this property will not change.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-515"><span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**Fehler \_ beim \_ überschreiten der \_ \_ Grenze.**</span><span class="sxs-lookup"><span data-stu-id="95627-515"><span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**ERROR\_CANT\_CROSS\_RM\_BOUNDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-516">6825 (0x1aa9)</span><span class="sxs-lookup"><span data-stu-id="95627-516">6825 (0x1AA9)</span></span>
</dt> <dt>



<span data-ttu-id="95627-517">Der Vorgang würde eine einzelne Datei mit zwei transaktionalen Ressourcen-Managern einschließen und ist daher nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="95627-517">The operation would involve a single file with two transactional resource managers and is therefore not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-518"><span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**Fehler \_ TxF-Verzeichnis \_ \_ nicht \_ leer**</span><span class="sxs-lookup"><span data-stu-id="95627-518"><span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**ERROR\_TXF\_DIR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-519">6826 (0x1aaa)</span><span class="sxs-lookup"><span data-stu-id="95627-519">6826 (0x1AAA)</span></span>
</dt> <dt>



<span data-ttu-id="95627-520">Das $TxF Verzeichnis muss leer sein, damit dieser Vorgang erfolgreich ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="95627-520">The $Txf directory must be empty for this operation to succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-521"><span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**fehlerhafte \_ \_ Transaktionen sind \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="95627-521"><span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**ERROR\_INDOUBT\_TRANSACTIONS\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-522">6827 (0x1aab)</span><span class="sxs-lookup"><span data-stu-id="95627-522">6827 (0x1AAB)</span></span>
</dt> <dt>



<span data-ttu-id="95627-523">Der Vorgang würde einen transaktionalen Ressourcen-Manager in einem inkonsistenten Zustand belassen und ist daher nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="95627-523">The operation would leave a transactional resource manager in an inconsistent state and is therefore not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-524"><span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**Fehler \_ TM \_ flüchtig**</span><span class="sxs-lookup"><span data-stu-id="95627-524"><span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**ERROR\_TM\_VOLATILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-525">6828 (0x1aac)</span><span class="sxs-lookup"><span data-stu-id="95627-525">6828 (0x1AAC)</span></span>
</dt> <dt>



<span data-ttu-id="95627-526">Der Vorgang konnte nicht abgeschlossen werden, da der Transaktions-Manager kein Protokoll hat.</span><span class="sxs-lookup"><span data-stu-id="95627-526">The operation could not be completed because the transaction manager does not have a log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-527"><span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**Fehler beim \_ Rollback- \_ Zeitgeber. \_**</span><span class="sxs-lookup"><span data-stu-id="95627-527"><span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**ERROR\_ROLLBACK\_TIMER\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-528">6829 (0x1aad)</span><span class="sxs-lookup"><span data-stu-id="95627-528">6829 (0x1AAD)</span></span>
</dt> <dt>



<span data-ttu-id="95627-529">Ein Rollback konnte nicht geplant werden, da ein zuvor geplanter Rollback bereits ausgeführt wurde oder für die Ausführung in die Warteschlange eingereiht wurde.</span><span class="sxs-lookup"><span data-stu-id="95627-529">A rollback could not be scheduled because a previously scheduled rollback has already executed or been queued for execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-530"><span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**Fehler \_ TxF- \_ Attribut ist \_ beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="95627-530"><span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**ERROR\_TXF\_ATTRIBUTE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-531">6830 (0x1aae)</span><span class="sxs-lookup"><span data-stu-id="95627-531">6830 (0x1AAE)</span></span>
</dt> <dt>



<span data-ttu-id="95627-532">Das transaktionale Metadatenattribut für die Datei oder das Verzeichnis ist beschädigt und kann nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="95627-532">The transactional metadata attribute on the file or directory is corrupt and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-533"><span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**Fehler \_ EFS \_ \_ \_ in Transaktion nicht \_ zulässig**</span><span class="sxs-lookup"><span data-stu-id="95627-533"><span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**ERROR\_EFS\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-534">6831 (0x1aaf)</span><span class="sxs-lookup"><span data-stu-id="95627-534">6831 (0x1AAF)</span></span>
</dt> <dt>



<span data-ttu-id="95627-535">Der Verschlüsselungs Vorgang konnte nicht abgeschlossen werden, da eine Transaktion aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="95627-535">The encryption operation could not be completed because a transaction is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-536"><span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**Fehler beim \_ Öffnen der Transaktion ist \_ \_ nicht \_ zulässig.**</span><span class="sxs-lookup"><span data-stu-id="95627-536"><span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERROR\_TRANSACTIONAL\_OPEN\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-537">6832 (0x1ab0)</span><span class="sxs-lookup"><span data-stu-id="95627-537">6832 (0x1AB0)</span></span>
</dt> <dt>



<span data-ttu-id="95627-538">Dieses Objekt darf nicht in einer Transaktion geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="95627-538">This object is not allowed to be opened in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-539"><span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**Fehler beim Vergrößern des Fehler \_ Protokolls \_ \_**</span><span class="sxs-lookup"><span data-stu-id="95627-539"><span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**ERROR\_LOG\_GROWTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-540">6833 (0x1ab1)</span><span class="sxs-lookup"><span data-stu-id="95627-540">6833 (0x1AB1)</span></span>
</dt> <dt>



<span data-ttu-id="95627-541">Fehler beim Erstellen von Speicherplatz im Protokoll des Transaktions Ressourcen-Managers.</span><span class="sxs-lookup"><span data-stu-id="95627-541">An attempt to create space in the transactional resource manager's log failed.</span></span> <span data-ttu-id="95627-542">Der Fehlerstatus wurde im Ereignisprotokoll aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="95627-542">The failure status has been recorded in the event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-543"><span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**Fehler bei der \_ Transaktions Zuordnung, die \_ \_ nicht unterstützt wird \_ .**</span><span class="sxs-lookup"><span data-stu-id="95627-543"><span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**ERROR\_TRANSACTED\_MAPPING\_UNSUPPORTED\_REMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-544">6834 (0x1ab2)</span><span class="sxs-lookup"><span data-stu-id="95627-544">6834 (0x1AB2)</span></span>
</dt> <dt>



<span data-ttu-id="95627-545">Speicher Zuordnung (Erstellen eines zugeordneten Abschnitts) eine Remote Datei unter einer Transaktion wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95627-545">Memory mapping (creating a mapped section) a remote file under a transaction is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-546"><span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**Fehler \_ TxF- \_ Metadaten sind \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="95627-546"><span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**ERROR\_TXF\_METADATA\_ALREADY\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-547">6835 (0x1ab3)</span><span class="sxs-lookup"><span data-stu-id="95627-547">6835 (0x1AB3)</span></span>
</dt> <dt>



<span data-ttu-id="95627-548">Transaktions Metadaten sind bereits in dieser Datei vorhanden und können nicht abgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="95627-548">Transaction metadata is already present on this file and cannot be superseded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-549"><span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**Fehler \_ Transaktions \_ Bereichs- \_ Rückrufe \_ nicht \_ festgelegt**</span><span class="sxs-lookup"><span data-stu-id="95627-549"><span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**ERROR\_TRANSACTION\_SCOPE\_CALLBACKS\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-550">6836 (0x1ab4)</span><span class="sxs-lookup"><span data-stu-id="95627-550">6836 (0x1AB4)</span></span>
</dt> <dt>



<span data-ttu-id="95627-551">Ein Transaktions Bereich konnte nicht eingegeben werden, da der Bereichs Handler nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="95627-551">A transaction scope could not be entered because the scope handler has not been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-552"><span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**herauf Stufung der Fehler \_ Transaktion \_ erforderlich \_**</span><span class="sxs-lookup"><span data-stu-id="95627-552"><span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**ERROR\_TRANSACTION\_REQUIRED\_PROMOTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-553">6837 (0x1ab5)</span><span class="sxs-lookup"><span data-stu-id="95627-553">6837 (0x1AB5)</span></span>
</dt> <dt>



<span data-ttu-id="95627-554">Die herauf Stufung war erforderlich, damit sich der Ressourcen-Manager eintragen kann, aber die Transaktion wurde so festgelegt, dass Sie nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="95627-554">Promotion was required in order to allow the resource manager to enlist, but the transaction was set to disallow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-555"><span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**Fehler \_ \_ beim Ausführen \_ \_ der Datei in der \_ Transaktion.**</span><span class="sxs-lookup"><span data-stu-id="95627-555"><span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**ERROR\_CANNOT\_EXECUTE\_FILE\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-556">6838 (0x1ab6)</span><span class="sxs-lookup"><span data-stu-id="95627-556">6838 (0x1AB6)</span></span>
</dt> <dt>



<span data-ttu-id="95627-557">Diese Datei ist für Änderungen in einer nicht aufgelösten Transaktion geöffnet und kann nur für die Ausführung durch einen transaktiven Reader geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="95627-557">This file is open for modification in an unresolved transaction and may be opened for execute only by a transacted reader.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-558"><span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**Fehler \_ Transaktionen \_ nicht \_ eingefroren**</span><span class="sxs-lookup"><span data-stu-id="95627-558"><span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**ERROR\_TRANSACTIONS\_NOT\_FROZEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-559">6839 (0x1ab7)</span><span class="sxs-lookup"><span data-stu-id="95627-559">6839 (0x1AB7)</span></span>
</dt> <dt>



<span data-ttu-id="95627-560">Die Anforderung zum Aktivieren von fixierten Transaktionen wurde ignoriert, da Transaktionen zuvor nicht eingefroren wurden.</span><span class="sxs-lookup"><span data-stu-id="95627-560">The request to thaw frozen transactions was ignored because transactions had not previously been frozen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-561"><span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**Fehler \_ \_ beim Einfrieren \_ der Transaktion. \_**</span><span class="sxs-lookup"><span data-stu-id="95627-561"><span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**ERROR\_TRANSACTION\_FREEZE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-562">6840 (0x1ab8)</span><span class="sxs-lookup"><span data-stu-id="95627-562">6840 (0x1AB8)</span></span>
</dt> <dt>



<span data-ttu-id="95627-563">Transaktionen können nicht eingefroren werden, weil bereits eine Sperre ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95627-563">Transactions cannot be frozen because a freeze is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-564"><span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**Fehler beim Erstellen eines \_ \_ Momentaufnahme \_ Volumens**</span><span class="sxs-lookup"><span data-stu-id="95627-564"><span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**ERROR\_NOT\_SNAPSHOT\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-565">6841 (0x1ab9)</span><span class="sxs-lookup"><span data-stu-id="95627-565">6841 (0x1AB9)</span></span>
</dt> <dt>



<span data-ttu-id="95627-566">Das Ziel Volume ist kein momentaufnahmenvolume.</span><span class="sxs-lookup"><span data-stu-id="95627-566">The target volume is not a snapshot volume.</span></span> <span data-ttu-id="95627-567">Dieser Vorgang gilt nur für ein Volume, das als Momentaufnahme bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="95627-567">This operation is only valid on a volume mounted as a snapshot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-568"><span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**Fehler " \_ kein Sicherungs \_ Punkt" \_ mit \_ geöffneten \_ Dateien**</span><span class="sxs-lookup"><span data-stu-id="95627-568"><span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**ERROR\_NO\_SAVEPOINT\_WITH\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-569">6842 (0x1aba)</span><span class="sxs-lookup"><span data-stu-id="95627-569">6842 (0x1ABA)</span></span>
</dt> <dt>



<span data-ttu-id="95627-570">Fehler beim Sicherungspunkt-Vorgang, da Dateien für die Transaktion geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="95627-570">The savepoint operation failed because files are open on the transaction.</span></span> <span data-ttu-id="95627-571">Dies ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="95627-571">This is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-572"><span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**Fehler beim Reparieren von Fehler \_ Daten. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="95627-572"><span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**ERROR\_DATA\_LOST\_REPAIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-573">6843 (0x1abb)</span><span class="sxs-lookup"><span data-stu-id="95627-573">6843 (0x1ABB)</span></span>
</dt> <dt>



<span data-ttu-id="95627-574">Windows hat Beschädigungen in einer Datei erkannt, und diese Datei wurde seit der Reparatur repariert.</span><span class="sxs-lookup"><span data-stu-id="95627-574">Windows has discovered corruption in a file, and that file has since been repaired.</span></span> <span data-ttu-id="95627-575">Möglicherweise ist ein Datenverlust aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="95627-575">Data loss may have occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-576"><span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**Fehler \_ Sparse \_ ist \_ \_ in der \_ Transaktion nicht zulässig.**</span><span class="sxs-lookup"><span data-stu-id="95627-576"><span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**ERROR\_SPARSE\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-577">6844 (0x1abc)</span><span class="sxs-lookup"><span data-stu-id="95627-577">6844 (0x1ABC)</span></span>
</dt> <dt>



<span data-ttu-id="95627-578">Der sparsesvorgang konnte nicht abgeschlossen werden, da eine Transaktion in der Datei aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="95627-578">The sparse operation could not be completed because a transaction is active on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-579"><span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**Fehler- \_ TM- \_ Identitätskonflikt \_**</span><span class="sxs-lookup"><span data-stu-id="95627-579"><span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**ERROR\_TM\_IDENTITY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-580">6845 (0x1abd)</span><span class="sxs-lookup"><span data-stu-id="95627-580">6845 (0x1ABD)</span></span>
</dt> <dt>



<span data-ttu-id="95627-581">Fehler beim Erstellen eines transaktionmanager-Objekts, weil die in der Protokolldatei gespeicherte TM-Identität nicht mit der als Argument übergebenen TM-Identität identisch ist.</span><span class="sxs-lookup"><span data-stu-id="95627-581">The call to create a TransactionManager object failed because the Tm Identity stored in the logfile does not match the Tm Identity that was passed in as an argument.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-582"><span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**Fehler \_ im \_ Abschnitt**</span><span class="sxs-lookup"><span data-stu-id="95627-582"><span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**ERROR\_FLOATED\_SECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-583">6846 (0x1abe)</span><span class="sxs-lookup"><span data-stu-id="95627-583">6846 (0x1ABE)</span></span>
</dt> <dt>



<span data-ttu-id="95627-584">Es wurde versucht, auf einem Abschnitts Objekt einen e/a-Vorgang auszuführen, der als Ergebnis einer Transaktions Ende aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="95627-584">I/O was attempted on a section object that has been floated as a result of a transaction ending.</span></span> <span data-ttu-id="95627-585">Es sind keine gültigen Daten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="95627-585">There is no valid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-586"><span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**Fehler \_ kann \_ keine \_ transaktive \_ Arbeit annehmen.**</span><span class="sxs-lookup"><span data-stu-id="95627-586"><span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**ERROR\_CANNOT\_ACCEPT\_TRANSACTED\_WORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-587">6847 (0x1abf)</span><span class="sxs-lookup"><span data-stu-id="95627-587">6847 (0x1ABF)</span></span>
</dt> <dt>



<span data-ttu-id="95627-588">Der Transaktions Ressourcen-Manager kann derzeit keine transaktiven Arbeiten aufgrund eines vorübergehenden Zustands, wie z. b. geringer Ressourcen, akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="95627-588">The transactional resource manager cannot currently accept transacted work due to a transient condition such as low resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-589"><span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**Fehler \_ beim \_ Abbrechen der \_ Transaktionen.**</span><span class="sxs-lookup"><span data-stu-id="95627-589"><span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**ERROR\_CANNOT\_ABORT\_TRANSACTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-590">6848 (0x1ac0)</span><span class="sxs-lookup"><span data-stu-id="95627-590">6848 (0x1AC0)</span></span>
</dt> <dt>



<span data-ttu-id="95627-591">Für den transaktionalen Ressourcen-Manager waren zu viele ausstehende Zuweisungs Vorgänge möglich, die nicht abgebrochen werden konnten.</span><span class="sxs-lookup"><span data-stu-id="95627-591">The transactional resource manager had too many tranactions outstanding that could not be aborted.</span></span> <span data-ttu-id="95627-592">Der transaktionale Ressourcen-Manager wurde heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="95627-592">The transactional resource manger has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-593"><span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**Fehler \_ hafte \_ Cluster**</span><span class="sxs-lookup"><span data-stu-id="95627-593"><span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ERROR\_BAD\_CLUSTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-594">6849 (0x1ac1)</span><span class="sxs-lookup"><span data-stu-id="95627-594">6849 (0x1AC1)</span></span>
</dt> <dt>



<span data-ttu-id="95627-595">Der Vorgang konnte aufgrund von fehlerhaften Clustern auf dem Datenträger nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="95627-595">The operation could not be completed due to bad clusters on disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-596"><span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**Fehler \_ Komprimierung \_ \_ \_ in \_ Transaktion nicht zulässig.**</span><span class="sxs-lookup"><span data-stu-id="95627-596"><span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**ERROR\_COMPRESSION\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-597">6850 (0x1ac2)</span><span class="sxs-lookup"><span data-stu-id="95627-597">6850 (0x1AC2)</span></span>
</dt> <dt>



<span data-ttu-id="95627-598">Der Komprimierungs Vorgang konnte nicht abgeschlossen werden, da für die Datei eine Transaktion aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="95627-598">The compression operation could not be completed because a transaction is active on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-599"><span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**Fehler \_ Volume \_ geändert**</span><span class="sxs-lookup"><span data-stu-id="95627-599"><span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**ERROR\_VOLUME\_DIRTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-600">6851 (0x1ac3)</span><span class="sxs-lookup"><span data-stu-id="95627-600">6851 (0x1AC3)</span></span>
</dt> <dt>



<span data-ttu-id="95627-601">Der Vorgang konnte nicht abgeschlossen werden, da das Volume geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="95627-601">The operation could not be completed because the volume is dirty.</span></span> <span data-ttu-id="95627-602">Führen Sie Chkdsk aus, und versuchen Sie es noch mal.</span><span class="sxs-lookup"><span data-stu-id="95627-602">Please run chkdsk and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-603"><span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**Fehler \_ \_ beim Nachverfolgen von Verbindungen \_ \_ in der \_ Transaktion.**</span><span class="sxs-lookup"><span data-stu-id="95627-603"><span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**ERROR\_NO\_LINK\_TRACKING\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-604">6852 (0x1ac4)</span><span class="sxs-lookup"><span data-stu-id="95627-604">6852 (0x1AC4)</span></span>
</dt> <dt>



<span data-ttu-id="95627-605">Der Link nach Verfolgungs Vorgang konnte nicht abgeschlossen werden, da eine Transaktion aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="95627-605">The link tracking operation could not be completed because a transaction is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-606"><span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**Fehler \_ Vorgang \_ \_ wird \_ in der \_ Transaktion nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="95627-606"><span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**ERROR\_OPERATION\_NOT\_SUPPORTED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-607">6853 (0x1ac5)</span><span class="sxs-lookup"><span data-stu-id="95627-607">6853 (0x1AC5)</span></span>
</dt> <dt>



<span data-ttu-id="95627-608">Dieser Vorgang kann nicht in einer Transaktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="95627-608">This operation cannot be performed in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-609"><span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**Fehler \_ abgelaufenes \_ handle**</span><span class="sxs-lookup"><span data-stu-id="95627-609"><span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**ERROR\_EXPIRED\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-610">6854 (0x1ac6)</span><span class="sxs-lookup"><span data-stu-id="95627-610">6854 (0x1AC6)</span></span>
</dt> <dt>



<span data-ttu-id="95627-611">Das Handle ist nicht mehr ordnungsgemäß mit der zugehörigen Transaktion verknüpft.</span><span class="sxs-lookup"><span data-stu-id="95627-611">The handle is no longer properly associated with its transaction.</span></span> <span data-ttu-id="95627-612">Möglicherweise wurde Sie in einem transaktionalen Ressourcen-Manager geöffnet, der später neu gestartet werden musste.</span><span class="sxs-lookup"><span data-stu-id="95627-612">It may have been opened in a transactional resource manager that was subsequently forced to restart.</span></span> <span data-ttu-id="95627-613">Schließen Sie das Handle, und öffnen Sie ein neues.</span><span class="sxs-lookup"><span data-stu-id="95627-613">Please close the handle and open a new one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-614"><span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**Fehler \_ Transaktion \_ nicht \_ eingetragen.**</span><span class="sxs-lookup"><span data-stu-id="95627-614"><span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**ERROR\_TRANSACTION\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-615">6855 (0x1ac7)</span><span class="sxs-lookup"><span data-stu-id="95627-615">6855 (0x1AC7)</span></span>
</dt> <dt>



<span data-ttu-id="95627-616">Der angegebene Vorgang konnte nicht ausgeführt werden, da der Ressourcen-Manager nicht in der Transaktion eingetragen ist.</span><span class="sxs-lookup"><span data-stu-id="95627-616">The specified operation could not be performed because the resource manager is not enlisted in the transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-617"><span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**Fehler \_ ctx- \_ Winstations \_ Name \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="95627-617"><span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**ERROR\_CTX\_WINSTATION\_NAME\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-618">7001 (0x1b59)</span><span class="sxs-lookup"><span data-stu-id="95627-618">7001 (0x1B59)</span></span>
</dt> <dt>



<span data-ttu-id="95627-619">Der angegebene Sitzungsname ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="95627-619">The specified session name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-620"><span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**Fehler \_ ctx \_ ungültige \_ PD.**</span><span class="sxs-lookup"><span data-stu-id="95627-620"><span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**ERROR\_CTX\_INVALID\_PD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-621">7002 (0x1b5a)</span><span class="sxs-lookup"><span data-stu-id="95627-621">7002 (0x1B5A)</span></span>
</dt> <dt>



<span data-ttu-id="95627-622">Der angegebene Protokoll Treiber ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="95627-622">The specified protocol driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-623"><span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**Fehler \_ ctx- \_ PD \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="95627-623"><span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**ERROR\_CTX\_PD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-624">7003 (0x1b5b)</span><span class="sxs-lookup"><span data-stu-id="95627-624">7003 (0x1B5B)</span></span>
</dt> <dt>



<span data-ttu-id="95627-625">Der angegebene Protokoll Treiber wurde nicht im Systempfad gefunden.</span><span class="sxs-lookup"><span data-stu-id="95627-625">The specified protocol driver was not found in the system path.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-626"><span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**Fehler \_ ctx \_ WD \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="95627-626"><span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**ERROR\_CTX\_WD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-627">7004 (0x1b5c)</span><span class="sxs-lookup"><span data-stu-id="95627-627">7004 (0x1B5C)</span></span>
</dt> <dt>



<span data-ttu-id="95627-628">Der angegebene terminalverbindungs-Treiber wurde nicht im Systempfad gefunden.</span><span class="sxs-lookup"><span data-stu-id="95627-628">The specified terminal connection driver was not found in the system path.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-629"><span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**Fehler \_ ctx \_ kann \_ \_ EventLog- \_ Eintrag nicht erstellen**</span><span class="sxs-lookup"><span data-stu-id="95627-629"><span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**ERROR\_CTX\_CANNOT\_MAKE\_EVENTLOG\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-630">7005 (0x1b5d)</span><span class="sxs-lookup"><span data-stu-id="95627-630">7005 (0x1B5D)</span></span>
</dt> <dt>



<span data-ttu-id="95627-631">Für diese Sitzung konnte kein Registrierungsschlüssel für die Ereignisprotokollierung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="95627-631">A registry key for event logging could not be created for this session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-632"><span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**Fehler \_ ctx- \_ Dienst \_ namens \_ Kollision**</span><span class="sxs-lookup"><span data-stu-id="95627-632"><span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**ERROR\_CTX\_SERVICE\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-633">7006 (0x1b5e)</span><span class="sxs-lookup"><span data-stu-id="95627-633">7006 (0x1B5E)</span></span>
</dt> <dt>



<span data-ttu-id="95627-634">Ein Dienst mit diesem Namen ist bereits im System vorhanden.</span><span class="sxs-lookup"><span data-stu-id="95627-634">A service with the same name already exists on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-635"><span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**Fehler beim \_ Schließen der ctx-Datei \_ \_**</span><span class="sxs-lookup"><span data-stu-id="95627-635"><span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**ERROR\_CTX\_CLOSE\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-636">7007 (0x1b5f)</span><span class="sxs-lookup"><span data-stu-id="95627-636">7007 (0x1B5F)</span></span>
</dt> <dt>



<span data-ttu-id="95627-637">Ein Schließvorgang steht in der Sitzung aus.</span><span class="sxs-lookup"><span data-stu-id="95627-637">A close operation is pending on the session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-638"><span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**Fehler \_ ctx \_ No \_ outbuf**</span><span class="sxs-lookup"><span data-stu-id="95627-638"><span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**ERROR\_CTX\_NO\_OUTBUF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-639">7008 (0x1b60)</span><span class="sxs-lookup"><span data-stu-id="95627-639">7008 (0x1B60)</span></span>
</dt> <dt>



<span data-ttu-id="95627-640">Es sind keine freien Ausgabepuffer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="95627-640">There are no free output buffers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-641"><span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**Fehler " \_ ctx \_ Modem \_ INF" \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="95627-641"><span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**ERROR\_CTX\_MODEM\_INF\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-642">7009 (0x1b61)</span><span class="sxs-lookup"><span data-stu-id="95627-642">7009 (0x1B61)</span></span>
</dt> <dt>



<span data-ttu-id="95627-643">Das Modem. Die INF-Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="95627-643">The MODEM.INF file was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-644"><span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**Fehler \_ ctx \_ ungültige " \_ mudemname".**</span><span class="sxs-lookup"><span data-stu-id="95627-644"><span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**ERROR\_CTX\_INVALID\_MODEMNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-645">7010 (0x1b62)</span><span class="sxs-lookup"><span data-stu-id="95627-645">7010 (0x1B62)</span></span>
</dt> <dt>



<span data-ttu-id="95627-646">Der Modem Name wurde in "Modem. inf" nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="95627-646">The modem name was not found in MODEM.INF.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-647"><span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**Fehler \_ ctx- \_ Modem \_ Antwort \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="95627-647"><span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-648">7011 (0x1b63)</span><span class="sxs-lookup"><span data-stu-id="95627-648">7011 (0x1B63)</span></span>
</dt> <dt>



<span data-ttu-id="95627-649">Das Modem hat den an ihn gesendeten Befehl nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="95627-649">The modem did not accept the command sent to it.</span></span> <span data-ttu-id="95627-650">Überprüfen Sie, ob der konfigurierte Modem Name mit dem angeschlossenen Modem übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="95627-650">Verify that the configured modem name matches the attached modem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-651"><span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**Fehler \_ ctx- \_ Modem \_ Antwort \_ Timeout**</span><span class="sxs-lookup"><span data-stu-id="95627-651"><span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-652">7012 (0x1b64)</span><span class="sxs-lookup"><span data-stu-id="95627-652">7012 (0x1B64)</span></span>
</dt> <dt>



<span data-ttu-id="95627-653">Das Modem hat nicht auf den an ihn gesendeten Befehl geantwortet.</span><span class="sxs-lookup"><span data-stu-id="95627-653">The modem did not respond to the command sent to it.</span></span> <span data-ttu-id="95627-654">Vergewissern Sie sich, dass das Modem ordnungsgemäß verkabelt und eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="95627-654">Verify that the modem is properly cabled and powered on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-655"><span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**Fehler \_ ctx- \_ Modem \_ Antwort kein Netz \_ \_ Betreiber**</span><span class="sxs-lookup"><span data-stu-id="95627-655"><span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_NO\_CARRIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-656">7013 (0x1b65)</span><span class="sxs-lookup"><span data-stu-id="95627-656">7013 (0x1B65)</span></span>
</dt> <dt>



<span data-ttu-id="95627-657">Fehler bei der Träger Erkennung, oder der Netzbetreiber wurde aufgrund einer Trennung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="95627-657">Carrier detect has failed or carrier has been dropped due to disconnect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-658"><span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**Fehler " \_ ctx \_ Modem \_ Response \_ No \_ Dialtone"**</span><span class="sxs-lookup"><span data-stu-id="95627-658"><span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_NO\_DIALTONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-659">7014 (0x1b66)</span><span class="sxs-lookup"><span data-stu-id="95627-659">7014 (0x1B66)</span></span>
</dt> <dt>



<span data-ttu-id="95627-660">Der Wählton wurde innerhalb der erforderlichen Zeit nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="95627-660">Dial tone not detected within the required time.</span></span> <span data-ttu-id="95627-661">Stellen Sie sicher, dass das Telefonkabel ordnungsgemäß angeschlossen und funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="95627-661">Verify that the phone cable is properly attached and functional.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-662"><span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**Fehler \_ ctx- \_ Modem \_ Antwort \_ ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="95627-662"><span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-663">7015 (0x1b67)</span><span class="sxs-lookup"><span data-stu-id="95627-663">7015 (0x1B67)</span></span>
</dt> <dt>



<span data-ttu-id="95627-664">Das ausgelastete Signal wurde an der Remote Site beim Rückruf erkannt.</span><span class="sxs-lookup"><span data-stu-id="95627-664">Busy signal detected at remote site on callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-665"><span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**Fehler \_ ctx- \_ Modem \_ Antwort \_ Sprache**</span><span class="sxs-lookup"><span data-stu-id="95627-665"><span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_VOICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-666">7016 (0x1b68)</span><span class="sxs-lookup"><span data-stu-id="95627-666">7016 (0x1B68)</span></span>
</dt> <dt>



<span data-ttu-id="95627-667">Die Stimme wurde bei einem Rückruf an der Remote Site erkannt.</span><span class="sxs-lookup"><span data-stu-id="95627-667">Voice detected at remote site on callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-668"><span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**Fehler \_ ctx- \_ TD- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="95627-668"><span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**ERROR\_CTX\_TD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-669">7017 (0x1b69)</span><span class="sxs-lookup"><span data-stu-id="95627-669">7017 (0x1B69)</span></span>
</dt> <dt>



<span data-ttu-id="95627-670">Transport Treiber Fehler.</span><span class="sxs-lookup"><span data-stu-id="95627-670">Transport driver error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-671"><span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**Fehler \_ ctx- \_ WinStation \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="95627-671"><span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**ERROR\_CTX\_WINSTATION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-672">7022 (0x1b6e)</span><span class="sxs-lookup"><span data-stu-id="95627-672">7022 (0x1B6E)</span></span>
</dt> <dt>



<span data-ttu-id="95627-673">Die angegebene Sitzung wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="95627-673">The specified session cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-674"><span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**Fehler \_ ctx- \_ WinStation ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="95627-674"><span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**ERROR\_CTX\_WINSTATION\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-675">7023 (0x1b6f)</span><span class="sxs-lookup"><span data-stu-id="95627-675">7023 (0x1B6F)</span></span>
</dt> <dt>



<span data-ttu-id="95627-676">Der angegebene Sitzungsname wird bereits verwendet.</span><span class="sxs-lookup"><span data-stu-id="95627-676">The specified session name is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-677"><span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**Fehler \_ ctx- \_ WinStation \_ ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="95627-677"><span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**ERROR\_CTX\_WINSTATION\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-678">7024 (0x1b70)</span><span class="sxs-lookup"><span data-stu-id="95627-678">7024 (0x1B70)</span></span>
</dt> <dt>



<span data-ttu-id="95627-679">Der Task, den Sie ausführen möchten, kann nicht abgeschlossen werden, da Remotedesktopdienste aktuell ausgelastet ist.</span><span class="sxs-lookup"><span data-stu-id="95627-679">The task you are trying to do can't be completed because Remote Desktop Services is currently busy.</span></span> <span data-ttu-id="95627-680">Wiederholen Sie den Vorgang in einigen Minuten.</span><span class="sxs-lookup"><span data-stu-id="95627-680">Please try again in a few minutes.</span></span> <span data-ttu-id="95627-681">Andere Benutzer sollten sich weiterhin anmelden können.</span><span class="sxs-lookup"><span data-stu-id="95627-681">Other users should still be able to log on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-682"><span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**fehlerhafter \_ ctx- \_ \_ Video \_ Modus (falsch)**</span><span class="sxs-lookup"><span data-stu-id="95627-682"><span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**ERROR\_CTX\_BAD\_VIDEO\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-683">7025 (0x1b71)</span><span class="sxs-lookup"><span data-stu-id="95627-683">7025 (0x1B71)</span></span>
</dt> <dt>



<span data-ttu-id="95627-684">Es wurde versucht, eine Verbindung mit einer Sitzung herzustellen, deren Videomodus vom aktuellen Client nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="95627-684">An attempt has been made to connect to a session whose video mode is not supported by the current client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-685"><span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**Fehler \_ ctx- \_ Grafik \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="95627-685"><span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**ERROR\_CTX\_GRAPHICS\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-686">7035 (0x1b7b)</span><span class="sxs-lookup"><span data-stu-id="95627-686">7035 (0x1B7B)</span></span>
</dt> <dt>



<span data-ttu-id="95627-687">Die Anwendung hat versucht, den DOS-Grafikmodus zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="95627-687">The application attempted to enable DOS graphics mode.</span></span> <span data-ttu-id="95627-688">Der DOS-Grafikmodus wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95627-688">DOS graphics mode is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-689"><span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**Fehler bei \_ ctx- \_ Anmeldung \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="95627-689"><span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**ERROR\_CTX\_LOGON\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-690">7037 (0x1b7d)</span><span class="sxs-lookup"><span data-stu-id="95627-690">7037 (0x1B7D)</span></span>
</dt> <dt>



<span data-ttu-id="95627-691">Ihre interaktive Anmelde Berechtigung wurde deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="95627-691">Your interactive logon privilege has been disabled.</span></span> <span data-ttu-id="95627-692">Wenden Sie sich an den Administrator.</span><span class="sxs-lookup"><span data-stu-id="95627-692">Please contact your administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-693"><span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**Fehler \_ ctx \_ nicht \_ Konsole**</span><span class="sxs-lookup"><span data-stu-id="95627-693"><span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**ERROR\_CTX\_NOT\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-694">7038 (0x1b7e)</span><span class="sxs-lookup"><span data-stu-id="95627-694">7038 (0x1B7E)</span></span>
</dt> <dt>



<span data-ttu-id="95627-695">Der angeforderte Vorgang kann nur in der Systemkonsole ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="95627-695">The requested operation can be performed only on the system console.</span></span> <span data-ttu-id="95627-696">Dies ist meistens das Ergebnis eines Treibers oder einer System-DLL, die direkten Zugriff auf die Konsole benötigt.</span><span class="sxs-lookup"><span data-stu-id="95627-696">This is most often the result of a driver or system DLL requiring direct console access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-697"><span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**Fehler \_ ctx- \_ Client \_ Abfrage \_ Timeout**</span><span class="sxs-lookup"><span data-stu-id="95627-697"><span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**ERROR\_CTX\_CLIENT\_QUERY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-698">7040 (0x1b80)</span><span class="sxs-lookup"><span data-stu-id="95627-698">7040 (0x1B80)</span></span>
</dt> <dt>



<span data-ttu-id="95627-699">Der Client konnte nicht auf die Verbindungs Nachricht des Servers Antworten.</span><span class="sxs-lookup"><span data-stu-id="95627-699">The client failed to respond to the server connect message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-700"><span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**Fehler beim \_ Trennen der ctx- \_ Konsole \_**</span><span class="sxs-lookup"><span data-stu-id="95627-700"><span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**ERROR\_CTX\_CONSOLE\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-701">7041 (0x1b81)</span><span class="sxs-lookup"><span data-stu-id="95627-701">7041 (0x1B81)</span></span>
</dt> <dt>



<span data-ttu-id="95627-702">Das Trennen der Konsolen Sitzung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95627-702">Disconnecting the console session is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-703"><span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**Fehler \_ ctx- \_ Konsolen \_ Verbindung**</span><span class="sxs-lookup"><span data-stu-id="95627-703"><span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**ERROR\_CTX\_CONSOLE\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-704">7042 (0x1b82)</span><span class="sxs-lookup"><span data-stu-id="95627-704">7042 (0x1B82)</span></span>
</dt> <dt>



<span data-ttu-id="95627-705">Die erneute Verbindung einer getrennten Sitzung mit der Konsole wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95627-705">Reconnecting a disconnected session to the console is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-706"><span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**Fehler \_ ctx, \_ Schatten \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="95627-706"><span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**ERROR\_CTX\_SHADOW\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-707">7044 (0x1b84)</span><span class="sxs-lookup"><span data-stu-id="95627-707">7044 (0x1B84)</span></span>
</dt> <dt>



<span data-ttu-id="95627-708">Die Anforderung, eine andere Sitzung Remote zu steuern, wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="95627-708">The request to control another session remotely was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-709"><span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**Fehler \_ ctx- \_ WinStation- \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="95627-709"><span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**ERROR\_CTX\_WINSTATION\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-710">7045 (0x1b85)</span><span class="sxs-lookup"><span data-stu-id="95627-710">7045 (0x1B85)</span></span>
</dt> <dt>



<span data-ttu-id="95627-711">Der angeforderte Sitzungs Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="95627-711">The requested session access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-712"><span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**Fehler " \_ ctx" ist \_ ungültig. \_**</span><span class="sxs-lookup"><span data-stu-id="95627-712"><span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**ERROR\_CTX\_INVALID\_WD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-713">7049 (0x1b89)</span><span class="sxs-lookup"><span data-stu-id="95627-713">7049 (0x1B89)</span></span>
</dt> <dt>



<span data-ttu-id="95627-714">Der angegebene terminalverbindungs-Treiber ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="95627-714">The specified terminal connection driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-715"><span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**Fehler \_ ctx, \_ Schatten ist \_ ungültig.**</span><span class="sxs-lookup"><span data-stu-id="95627-715"><span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**ERROR\_CTX\_SHADOW\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-716">7050 (0x1b8a)</span><span class="sxs-lookup"><span data-stu-id="95627-716">7050 (0x1B8A)</span></span>
</dt> <dt>



<span data-ttu-id="95627-717">Die angeforderte Sitzung kann nicht remote gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="95627-717">The requested session cannot be controlled remotely.</span></span> <span data-ttu-id="95627-718">Dies kann daran liegen, dass die Sitzung getrennt ist oder zurzeit kein Benutzer angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="95627-718">This may be because the session is disconnected or does not currently have a user logged on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-719"><span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**Fehler \_ ctx- \_ Schatten \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="95627-719"><span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**ERROR\_CTX\_SHADOW\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-720">7051 (0x1b8b)</span><span class="sxs-lookup"><span data-stu-id="95627-720">7051 (0x1B8B)</span></span>
</dt> <dt>



<span data-ttu-id="95627-721">Die angeforderte Sitzung ist nicht für die Remote Steuerung konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="95627-721">The requested session is not configured to allow remote control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-722"><span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**Fehler \_ ctx- \_ Client \_ Lizenz wird \_ \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="95627-722"><span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**ERROR\_CTX\_CLIENT\_LICENSE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-723">7052 (0x1b8c)</span><span class="sxs-lookup"><span data-stu-id="95627-723">7052 (0x1B8C)</span></span>
</dt> <dt>



<span data-ttu-id="95627-724">Ihre Anforderung zum Herstellen einer Verbindung mit diesem Terminal Server wurde abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="95627-724">Your request to connect to this Terminal Server has been rejected.</span></span> <span data-ttu-id="95627-725">Ihre Terminal Server-Client Lizenznummer wird derzeit von einem anderen Benutzer verwendet.</span><span class="sxs-lookup"><span data-stu-id="95627-725">Your Terminal Server client license number is currently being used by another user.</span></span> <span data-ttu-id="95627-726">Wenden Sie sich an Ihren Systemadministrator, um eine eindeutige Lizenznummer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="95627-726">Please call your system administrator to obtain a unique license number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-727"><span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**Fehler \_ ctx- \_ Client \_ Lizenz \_ nicht \_ festgelegt**</span><span class="sxs-lookup"><span data-stu-id="95627-727"><span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**ERROR\_CTX\_CLIENT\_LICENSE\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-728">7053 (0x1b8d)</span><span class="sxs-lookup"><span data-stu-id="95627-728">7053 (0x1B8D)</span></span>
</dt> <dt>



<span data-ttu-id="95627-729">Ihre Anforderung zum Herstellen einer Verbindung mit diesem Terminal Server wurde abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="95627-729">Your request to connect to this Terminal Server has been rejected.</span></span> <span data-ttu-id="95627-730">Die Lizenznummer des Terminal Server-Clients wurde für diese Kopie des Terminal Server Clients nicht eingegeben.</span><span class="sxs-lookup"><span data-stu-id="95627-730">Your Terminal Server client license number has not been entered for this copy of the Terminal Server client.</span></span> <span data-ttu-id="95627-731">Wenden Sie sich an Ihren Systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="95627-731">Please contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-732"><span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**Fehler- \_ ctx- \_ Lizenz \_ nicht \_ verfügbar.**</span><span class="sxs-lookup"><span data-stu-id="95627-732"><span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**ERROR\_CTX\_LICENSE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-733">7054 (0x1b8e)</span><span class="sxs-lookup"><span data-stu-id="95627-733">7054 (0x1B8E)</span></span>
</dt> <dt>



<span data-ttu-id="95627-734">Die Anzahl der Verbindungen mit diesem Computer ist begrenzt, und alle Verbindungen werden momentan verwendet.</span><span class="sxs-lookup"><span data-stu-id="95627-734">The number of connections to this computer is limited and all connections are in use right now.</span></span> <span data-ttu-id="95627-735">Versuchen Sie, später eine Verbindung herzustellen, oder wenden Sie sich an den</span><span class="sxs-lookup"><span data-stu-id="95627-735">Try connecting later or contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-736"><span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**Fehler \_ ctx- \_ Lizenz \_ Client \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="95627-736"><span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**ERROR\_CTX\_LICENSE\_CLIENT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-737">7055 (0x1b8f)</span><span class="sxs-lookup"><span data-stu-id="95627-737">7055 (0x1B8F)</span></span>
</dt> <dt>



<span data-ttu-id="95627-738">Der von Ihnen verwendete Client ist nicht für die Verwendung dieses Systems lizenziert.</span><span class="sxs-lookup"><span data-stu-id="95627-738">The client you are using is not licensed to use this system.</span></span> <span data-ttu-id="95627-739">Ihre Anmelde Anforderung wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="95627-739">Your logon request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-740"><span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**Fehler- \_ ctx- \_ Lizenz \_ abgelaufen**</span><span class="sxs-lookup"><span data-stu-id="95627-740"><span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**ERROR\_CTX\_LICENSE\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-741">7056 (0x1b90)</span><span class="sxs-lookup"><span data-stu-id="95627-741">7056 (0x1B90)</span></span>
</dt> <dt>



<span data-ttu-id="95627-742">Die System Lizenz ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="95627-742">The system license has expired.</span></span> <span data-ttu-id="95627-743">Ihre Anmelde Anforderung wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="95627-743">Your logon request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-744"><span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**Fehler \_ ctx- \_ Schatten wird \_ nicht \_ ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="95627-744"><span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**ERROR\_CTX\_SHADOW\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-745">7057 (0x1b91)</span><span class="sxs-lookup"><span data-stu-id="95627-745">7057 (0x1B91)</span></span>
</dt> <dt>



<span data-ttu-id="95627-746">Die Remote Steuerung konnte nicht beendet werden, da die angegebene Sitzung zurzeit nicht remote gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="95627-746">Remote control could not be terminated because the specified session is not currently being remotely controlled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-747"><span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**Fehler \_ ctx \_ - \_ Schatten \_ wurde durch \_ Modusänderung beendet \_**</span><span class="sxs-lookup"><span data-stu-id="95627-747"><span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**ERROR\_CTX\_SHADOW\_ENDED\_BY\_MODE\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-748">7058 (0x1b92)</span><span class="sxs-lookup"><span data-stu-id="95627-748">7058 (0x1B92)</span></span>
</dt> <dt>



<span data-ttu-id="95627-749">Die Remote Steuerung der Konsole wurde beendet, weil der Anzeigemodus geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="95627-749">The remote control of the console was terminated because the display mode was changed.</span></span> <span data-ttu-id="95627-750">Das Ändern des Anzeigemodus in einer Remote Steuerungs Sitzung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95627-750">Changing the display mode in a remote control session is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-751"><span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**Fehler \_ Aktivierungs \_ Anzahl \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="95627-751"><span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**ERROR\_ACTIVATION\_COUNT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-752">7059 (0x1b93)</span><span class="sxs-lookup"><span data-stu-id="95627-752">7059 (0x1B93)</span></span>
</dt> <dt>



<span data-ttu-id="95627-753">Die Aktivierung der maximalen Anzahl von Wiederholungen für diese Installation wurde bereits zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="95627-753">Activation has already been reset the maximum number of times for this installation.</span></span> <span data-ttu-id="95627-754">Der Aktivierungszeit Geber wird nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="95627-754">Your activation timer will not be cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-755"><span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**Fehler \_ ctx- \_ Winstations \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="95627-755"><span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**ERROR\_CTX\_WINSTATIONS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-756">7060 (0x1b94)</span><span class="sxs-lookup"><span data-stu-id="95627-756">7060 (0x1B94)</span></span>
</dt> <dt>



<span data-ttu-id="95627-757">Remote Anmeldungen sind zurzeit deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="95627-757">Remote logins are currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-758"><span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**Fehler \_ ctx- \_ Verschlüsselungs \_ Stufe \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="95627-758"><span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**ERROR\_CTX\_ENCRYPTION\_LEVEL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-759">7061 (0x1b95)</span><span class="sxs-lookup"><span data-stu-id="95627-759">7061 (0x1B95)</span></span>
</dt> <dt>



<span data-ttu-id="95627-760">Sie verfügen nicht über die richtige Verschlüsselungs Stufe für den Zugriff auf diese Sitzung.</span><span class="sxs-lookup"><span data-stu-id="95627-760">You do not have the proper encryption level to access this Session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-761"><span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**Fehler- \_ ctx- \_ Sitzung wird \_ \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="95627-761"><span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**ERROR\_CTX\_SESSION\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-762">7062 (0x1b96)</span><span class="sxs-lookup"><span data-stu-id="95627-762">7062 (0x1B96)</span></span>
</dt> <dt>



<span data-ttu-id="95627-763">Der Benutzer "% s \\ \\ % s" ist zurzeit an diesem Computer angemeldet.</span><span class="sxs-lookup"><span data-stu-id="95627-763">The user %s\\\\%s is currently logged on to this computer.</span></span> <span data-ttu-id="95627-764">Nur der aktuelle Benutzer oder ein Administrator kann sich an diesem Computer anmelden.</span><span class="sxs-lookup"><span data-stu-id="95627-764">Only the current user or an administrator can log on to this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-765"><span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**Fehler \_ ctx \_ keine Abmeldung \_ erzwingen \_**</span><span class="sxs-lookup"><span data-stu-id="95627-765"><span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**ERROR\_CTX\_NO\_FORCE\_LOGOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-766">7063 (0x1b97)</span><span class="sxs-lookup"><span data-stu-id="95627-766">7063 (0x1B97)</span></span>
</dt> <dt>



<span data-ttu-id="95627-767">Der Benutzer "% s \\ \\ % s" ist bereits in der Konsole dieses Computers angemeldet.</span><span class="sxs-lookup"><span data-stu-id="95627-767">The user %s\\\\%s is already logged on to the console of this computer.</span></span> <span data-ttu-id="95627-768">Sie verfügen zurzeit nicht über die Berechtigung, sich anzumelden.</span><span class="sxs-lookup"><span data-stu-id="95627-768">You do not have permission to log in at this time.</span></span> <span data-ttu-id="95627-769">Um dieses Problem zu beheben, wenden Sie sich an% s \\ \\ % s, und melden Sie sich ab.</span><span class="sxs-lookup"><span data-stu-id="95627-769">To resolve this issue, contact %s\\\\%s and have them log off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-770"><span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**Fehler- \_ ctx- \_ Konto \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="95627-770"><span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**ERROR\_CTX\_ACCOUNT\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-771">7064 (0x1b98)</span><span class="sxs-lookup"><span data-stu-id="95627-771">7064 (0x1B98)</span></span>
</dt> <dt>



<span data-ttu-id="95627-772">Sie können sich aufgrund einer Konto Einschränkung nicht anmelden.</span><span class="sxs-lookup"><span data-stu-id="95627-772">Unable to log you on because of an account restriction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-773"><span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**Fehler beim \_ RDP- \_ Protokoll. \_**</span><span class="sxs-lookup"><span data-stu-id="95627-773"><span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**ERROR\_RDP\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-774">7065 (0x1b99)</span><span class="sxs-lookup"><span data-stu-id="95627-774">7065 (0x1B99)</span></span>
</dt> <dt>



<span data-ttu-id="95627-775">Die RDP-Protokoll Komponente "%2" hat einen Fehler im Protokolldaten Strom erkannt und hat den Client getrennt.</span><span class="sxs-lookup"><span data-stu-id="95627-775">The RDP protocol component %2 detected an error in the protocol stream and has disconnected the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-776"><span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**Fehler \_ ctx \_ CDM \_ Connect**</span><span class="sxs-lookup"><span data-stu-id="95627-776"><span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**ERROR\_CTX\_CDM\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-777">7066 (0x1b9a)</span><span class="sxs-lookup"><span data-stu-id="95627-777">7066 (0x1B9A)</span></span>
</dt> <dt>



<span data-ttu-id="95627-778">Der Client Laufwerk Zuordnungsdienst hat eine Verbindung mit der Terminal Verbindung hergestellt.</span><span class="sxs-lookup"><span data-stu-id="95627-778">The Client Drive Mapping Service Has Connected on Terminal Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-779"><span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**Fehler \_ ctx- \_ CDM- \_ Trennung**</span><span class="sxs-lookup"><span data-stu-id="95627-779"><span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**ERROR\_CTX\_CDM\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-780">7067 (0x1b9b)</span><span class="sxs-lookup"><span data-stu-id="95627-780">7067 (0x1B9B)</span></span>
</dt> <dt>



<span data-ttu-id="95627-781">Der Client Laufwerk Zuordnungsdienst hat die Verbindung mit der Terminal Verbindung getrennt.</span><span class="sxs-lookup"><span data-stu-id="95627-781">The Client Drive Mapping Service Has Disconnected on Terminal Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-782"><span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**Fehler \_ ctx- \_ Sicherheits \_ Schicht \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="95627-782"><span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**ERROR\_CTX\_SECURITY\_LAYER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-783">7068 (0x1b9c)</span><span class="sxs-lookup"><span data-stu-id="95627-783">7068 (0x1B9C)</span></span>
</dt> <dt>



<span data-ttu-id="95627-784">Die Sicherheitsschicht des Terminal Servers hat einen Fehler im Protokolldaten Strom festgestellt und den Client getrennt.</span><span class="sxs-lookup"><span data-stu-id="95627-784">The Terminal Server security layer detected an error in the protocol stream and has disconnected the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-785"><span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**Fehler \_ TS \_ inkompatible \_ Sitzungen**</span><span class="sxs-lookup"><span data-stu-id="95627-785"><span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**ERROR\_TS\_INCOMPATIBLE\_SESSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-786">7069 (0x1b9d)</span><span class="sxs-lookup"><span data-stu-id="95627-786">7069 (0x1B9D)</span></span>
</dt> <dt>



<span data-ttu-id="95627-787">Die Ziel Sitzung ist mit der aktuellen Sitzung nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="95627-787">The target session is incompatible with the current session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-788"><span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**Fehler \_ TS- \_ Video \_ Subsystem \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="95627-788"><span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**ERROR\_TS\_VIDEO\_SUBSYSTEM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-789">7070 (0x1b9e)</span><span class="sxs-lookup"><span data-stu-id="95627-789">7070 (0x1B9E)</span></span>
</dt> <dt>



<span data-ttu-id="95627-790">Windows kann keine Verbindung mit ihrer Sitzung herstellen, da im Windows-Video Subsystem ein Problem aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="95627-790">Windows can't connect to your session because a problem occurred in the Windows video subsystem.</span></span> <span data-ttu-id="95627-791">Versuchen Sie später erneut, eine Verbindung herzustellen, oder wenden Sie sich an den Server Administrator.</span><span class="sxs-lookup"><span data-stu-id="95627-791">Try connecting again later, or contact the server administrator for assistance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-792"><span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**FRS \_ Err \_ ungültige \_ API- \_ Sequenz**</span><span class="sxs-lookup"><span data-stu-id="95627-792"><span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**FRS\_ERR\_INVALID\_API\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-793">8001 (0x1F)</span><span class="sxs-lookup"><span data-stu-id="95627-793">8001 (0x1F41)</span></span>
</dt> <dt>



<span data-ttu-id="95627-794">Die Datei Replikations Dienst-API wurde falsch aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="95627-794">The file replication service API was called incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-795"><span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**FRS \_ Err- \_ Start \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="95627-795"><span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**FRS\_ERR\_STARTING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-796">8002 (0x1F 42)</span><span class="sxs-lookup"><span data-stu-id="95627-796">8002 (0x1F42)</span></span>
</dt> <dt>



<span data-ttu-id="95627-797">Der Datei Replikations Dienst kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="95627-797">The file replication service cannot be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-798"><span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**FRS \_ Err \_ Dienst wird angehalten \_**</span><span class="sxs-lookup"><span data-stu-id="95627-798"><span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**FRS\_ERR\_STOPPING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-799">8003 (0x1F 43)</span><span class="sxs-lookup"><span data-stu-id="95627-799">8003 (0x1F43)</span></span>
</dt> <dt>



<span data-ttu-id="95627-800">Der Datei Replikations Dienst kann nicht beendet werden.</span><span class="sxs-lookup"><span data-stu-id="95627-800">The file replication service cannot be stopped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-801"><span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**\_interne FRS \_ - \_ API**</span><span class="sxs-lookup"><span data-stu-id="95627-801"><span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**FRS\_ERR\_INTERNAL\_API**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-802">8004 (0x1F 44)</span><span class="sxs-lookup"><span data-stu-id="95627-802">8004 (0x1F44)</span></span>
</dt> <dt>



<span data-ttu-id="95627-803">Die Datei Replikations Dienst-API hat die Anforderung beendet.</span><span class="sxs-lookup"><span data-stu-id="95627-803">The file replication service API terminated the request.</span></span> <span data-ttu-id="95627-804">Das Ereignisprotokoll kann weitere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="95627-804">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-805"><span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**FRS \_ , \_ intern**</span><span class="sxs-lookup"><span data-stu-id="95627-805"><span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**FRS\_ERR\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-806">8005 (0x1F)</span><span class="sxs-lookup"><span data-stu-id="95627-806">8005 (0x1F45)</span></span>
</dt> <dt>



<span data-ttu-id="95627-807">Der Datei Replikations Dienst hat die Anforderung beendet.</span><span class="sxs-lookup"><span data-stu-id="95627-807">The file replication service terminated the request.</span></span> <span data-ttu-id="95627-808">Das Ereignisprotokoll kann weitere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="95627-808">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-809"><span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**FRS \_ Err- \_ Dienst- \_ comm**</span><span class="sxs-lookup"><span data-stu-id="95627-809"><span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**FRS\_ERR\_SERVICE\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-810">8006 (0x1F 46)</span><span class="sxs-lookup"><span data-stu-id="95627-810">8006 (0x1F46)</span></span>
</dt> <dt>



<span data-ttu-id="95627-811">Der Datei Replikations Dienst kann nicht kontaktiert werden.</span><span class="sxs-lookup"><span data-stu-id="95627-811">The file replication service cannot be contacted.</span></span> <span data-ttu-id="95627-812">Das Ereignisprotokoll kann weitere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="95627-812">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-813"><span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**FRS \_ Err \_ nicht ausreichend \_ PRIV**</span><span class="sxs-lookup"><span data-stu-id="95627-813"><span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**FRS\_ERR\_INSUFFICIENT\_PRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-814">8007 (0x1F 47)</span><span class="sxs-lookup"><span data-stu-id="95627-814">8007 (0x1F47)</span></span>
</dt> <dt>



<span data-ttu-id="95627-815">Der Datei Replikations Dienst kann die Anforderung nicht erfüllen, da der Benutzer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="95627-815">The file replication service cannot satisfy the request because the user has insufficient privileges.</span></span> <span data-ttu-id="95627-816">Das Ereignisprotokoll kann weitere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="95627-816">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-817"><span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**FRS \_ Err- \_ Authentifizierung**</span><span class="sxs-lookup"><span data-stu-id="95627-817"><span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**FRS\_ERR\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-818">8008 (0x1F 48)</span><span class="sxs-lookup"><span data-stu-id="95627-818">8008 (0x1F48)</span></span>
</dt> <dt>



<span data-ttu-id="95627-819">Der Datei Replikations Dienst kann die Anforderung nicht erfüllen, da der authentifizierte RPC nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="95627-819">The file replication service cannot satisfy the request because authenticated RPC is not available.</span></span> <span data-ttu-id="95627-820">Das Ereignisprotokoll kann weitere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="95627-820">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-821"><span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**FRS \_ Err \_ Parent \_ nicht ausreichend \_ PRIV**</span><span class="sxs-lookup"><span data-stu-id="95627-821"><span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**FRS\_ERR\_PARENT\_INSUFFICIENT\_PRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-822">8009 (0x1F 49)</span><span class="sxs-lookup"><span data-stu-id="95627-822">8009 (0x1F49)</span></span>
</dt> <dt>



<span data-ttu-id="95627-823">Der Datei Replikations Dienst kann die Anforderung nicht erfüllen, da der Benutzer nicht über ausreichende Berechtigungen auf dem Domänen Controller verfügt.</span><span class="sxs-lookup"><span data-stu-id="95627-823">The file replication service cannot satisfy the request because the user has insufficient privileges on the domain controller.</span></span> <span data-ttu-id="95627-824">Das Ereignisprotokoll kann weitere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="95627-824">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-825"><span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**FRS \_ Err \_ Parent- \_ Authentifizierung**</span><span class="sxs-lookup"><span data-stu-id="95627-825"><span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**FRS\_ERR\_PARENT\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-826">8010 (0x1F 4a)</span><span class="sxs-lookup"><span data-stu-id="95627-826">8010 (0x1F4A)</span></span>
</dt> <dt>



<span data-ttu-id="95627-827">Der Datei Replikations Dienst kann die Anforderung nicht erfüllen, da das authentifizierte RPC auf dem Domänen Controller nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="95627-827">The file replication service cannot satisfy the request because authenticated RPC is not available on the domain controller.</span></span> <span data-ttu-id="95627-828">Das Ereignisprotokoll kann weitere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="95627-828">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-829"><span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**FRS \_ Err \_ - \_ untergeordnetes Element zum über \_ geordneten \_ Element**</span><span class="sxs-lookup"><span data-stu-id="95627-829"><span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**FRS\_ERR\_CHILD\_TO\_PARENT\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-830">8011 (0x1F 4B)</span><span class="sxs-lookup"><span data-stu-id="95627-830">8011 (0x1F4B)</span></span>
</dt> <dt>



<span data-ttu-id="95627-831">Der Datei Replikations Dienst kann nicht mit dem Datei Replikations Dienst auf dem Domänen Controller kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="95627-831">The file replication service cannot communicate with the file replication service on the domain controller.</span></span> <span data-ttu-id="95627-832">Das Ereignisprotokoll kann weitere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="95627-832">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-833"><span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS \_ Err \_ übergeordnetes Element \_ zu untergeordnetem \_ \_ comm**</span><span class="sxs-lookup"><span data-stu-id="95627-833"><span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS\_ERR\_PARENT\_TO\_CHILD\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-834">8012 (0x1F 4C)</span><span class="sxs-lookup"><span data-stu-id="95627-834">8012 (0x1F4C)</span></span>
</dt> <dt>



<span data-ttu-id="95627-835">Der Datei Replikations Dienst auf dem Domänen Controller kann nicht mit dem Datei Replikations Dienst auf diesem Computer kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="95627-835">The file replication service on the domain controller cannot communicate with the file replication service on this computer.</span></span> <span data-ttu-id="95627-836">Das Ereignisprotokoll kann weitere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="95627-836">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-837"><span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**FRS \_ Err \_ Sysvol \_ Auffüllen**</span><span class="sxs-lookup"><span data-stu-id="95627-837"><span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**FRS\_ERR\_SYSVOL\_POPULATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-838">8013 (0x1F 4D)</span><span class="sxs-lookup"><span data-stu-id="95627-838">8013 (0x1F4D)</span></span>
</dt> <dt>



<span data-ttu-id="95627-839">Der Datei Replikations Dienst kann das System Volume aufgrund eines internen Fehlers nicht auffüllen.</span><span class="sxs-lookup"><span data-stu-id="95627-839">The file replication service cannot populate the system volume because of an internal error.</span></span> <span data-ttu-id="95627-840">Das Ereignisprotokoll kann weitere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="95627-840">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-841"><span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**FRS \_ - \_ Timeout für SYSVOL- \_ Auffüllen \_**</span><span class="sxs-lookup"><span data-stu-id="95627-841"><span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**FRS\_ERR\_SYSVOL\_POPULATE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-842">8014 (0x1F 4E)</span><span class="sxs-lookup"><span data-stu-id="95627-842">8014 (0x1F4E)</span></span>
</dt> <dt>



<span data-ttu-id="95627-843">Der Datei Replikations Dienst kann das System Volume aufgrund eines internen Timeouts nicht auffüllen.</span><span class="sxs-lookup"><span data-stu-id="95627-843">The file replication service cannot populate the system volume because of an internal timeout.</span></span> <span data-ttu-id="95627-844">Das Ereignisprotokoll kann weitere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="95627-844">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-845"><span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**FRS \_ Err \_ Sysvol \_ ist \_ ausgelastet.**</span><span class="sxs-lookup"><span data-stu-id="95627-845"><span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**FRS\_ERR\_SYSVOL\_IS\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-846">8015 (0x1F 4)</span><span class="sxs-lookup"><span data-stu-id="95627-846">8015 (0x1F4F)</span></span>
</dt> <dt>



<span data-ttu-id="95627-847">Der Datei Replikations Dienst kann die Anforderung nicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="95627-847">The file replication service cannot process the request.</span></span> <span data-ttu-id="95627-848">Das System Volume ist mit einer vorherigen Anforderung ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="95627-848">The system volume is busy with a previous request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-849"><span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS \_ Err \_ Sysvol \_ Demote**</span><span class="sxs-lookup"><span data-stu-id="95627-849"><span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS\_ERR\_SYSVOL\_DEMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-850">8016 (0x1F 50)</span><span class="sxs-lookup"><span data-stu-id="95627-850">8016 (0x1F50)</span></span>
</dt> <dt>



<span data-ttu-id="95627-851">Der Datei Replikations Dienst kann die Replikation des Systemvolumes aufgrund eines internen Fehlers nicht beenden.</span><span class="sxs-lookup"><span data-stu-id="95627-851">The file replication service cannot stop replicating the system volume because of an internal error.</span></span> <span data-ttu-id="95627-852">Das Ereignisprotokoll kann weitere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="95627-852">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95627-853"><span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**FRS \_ Err ( \_ ungültiger \_ Dienst \_ Parameter)**</span><span class="sxs-lookup"><span data-stu-id="95627-853"><span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**FRS\_ERR\_INVALID\_SERVICE\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95627-854">8017 (0x1F 51)</span><span class="sxs-lookup"><span data-stu-id="95627-854">8017 (0x1F51)</span></span>
</dt> <dt>



<span data-ttu-id="95627-855">Der Datei Replikations Dienst hat einen ungültigen Parameter erkannt.</span><span class="sxs-lookup"><span data-stu-id="95627-855">The file replication service detected an invalid parameter.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95627-856">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95627-856">Requirements</span></span>



| <span data-ttu-id="95627-857">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95627-857">Requirement</span></span> | <span data-ttu-id="95627-858">Wert</span><span class="sxs-lookup"><span data-stu-id="95627-858">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95627-859">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95627-859">Minimum supported client</span></span><br/> | <span data-ttu-id="95627-860">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95627-860">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="95627-861">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95627-861">Minimum supported server</span></span><br/> | <span data-ttu-id="95627-862">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95627-862">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95627-863">Header</span><span class="sxs-lookup"><span data-stu-id="95627-863">Header</span></span><br/>                   | <dl> <span data-ttu-id="95627-864"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="95627-864"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95627-865">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95627-865">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95627-866">System Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="95627-866">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




