---
description: Aktiviert oder setzt alle deaktivierten oder angehaltenen Schlüsselschutz Vorrichtungen fort.
ms.assetid: 6f5a17a3-84f2-43a0-a85f-1037cd52439a
title: Enablekeyprotector-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 78f8502ae141458f1ae46a48d21c110b9434acd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354451"
---
# <a name="enablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="1f40a-103">Enablekeyprotector-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="1f40a-103">EnableKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="1f40a-104">Die **enablekeyprotector** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " aktiviert oder setzt alle deaktivierten oder angehaltenen Schlüsselschutz Vorrichtungen fort.</span><span class="sxs-lookup"><span data-stu-id="1f40a-104">The **EnableKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class enables or resumes all disabled or suspended key protectors.</span></span> <span data-ttu-id="1f40a-105">Mit dieser Methode können Sie den BitLocker-Schutz auf einem verschlüsselten Volume erneut aktivieren oder fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="1f40a-105">You can use this method to reenable or resume BitLocker protection on an encrypted volume.</span></span> <span data-ttu-id="1f40a-106">Mit dieser Methode wird sichergestellt, dass der Verschlüsselungsschlüssel des Volumes nicht im Klartext auf der Festplatte verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="1f40a-106">This method ensures that the volume's encryption key is not exposed in the clear on the hard disk.</span></span>

> [!Note]  
> <span data-ttu-id="1f40a-107">Wenn die Festplatte die Hardware Verschlüsselung unterstützt, wechselt der Status des Bands von "immer entsperrt" in "entsperrt".</span><span class="sxs-lookup"><span data-stu-id="1f40a-107">If the disc supports hardware encryption, the band state transitions to "unlocked" from "always unlocked".</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1f40a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f40a-108">Syntax</span></span>


```mof
uint32 EnableKeyProtectors();
```



## <a name="parameters"></a><span data-ttu-id="1f40a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f40a-109">Parameters</span></span>

<span data-ttu-id="1f40a-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1f40a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1f40a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f40a-111">Return value</span></span>

<span data-ttu-id="1f40a-112">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1f40a-112">Type: **uint32**</span></span>

<span data-ttu-id="1f40a-113">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="1f40a-113">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="1f40a-114">Wenn die Schlüssel Schutzvorrichtungen bereits aktiviert sind und keine weiteren Fehler auftreten, gibt diese Methode 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="1f40a-114">If key protectors are already enabled and no other errors occur, this method returns zero.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f40a-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="1f40a-115">Return code/value</span></span></th>
<th><span data-ttu-id="1f40a-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f40a-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="1f40a-117"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span><span class="sxs-lookup"><span data-stu-id="1f40a-117"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="1f40a-118">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1f40a-118">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="1f40a-119"><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt> <dt>2150694919 (0x80310007)</dt> </span><span class="sxs-lookup"><span data-stu-id="1f40a-119"><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt> <dt>2150694919 (0x80310007)</dt> </span></span></dl></td>
<td><span data-ttu-id="1f40a-120">Auf dem Volume sind keine Schlüssel Schutzvorrichtungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1f40a-120">No key protectors exist on the volume.</span></span> <span data-ttu-id="1f40a-121">Verwenden Sie eine der folgenden Methoden, um Schlüssel Schutzvorrichtungen für das Volume anzugeben:</span><span class="sxs-lookup"><span data-stu-id="1f40a-121">Use one of the following methods to specify key protectors for the volume:</span></span><br/>
<ul>
<li><span data-ttu-id="1f40a-122"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>Protectkeywithcertificatefile</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f40a-122"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span></span></li>
<li><span data-ttu-id="1f40a-123"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>Protectkeywithcertifierkeybibprint</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f40a-123"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span></span></li>
<li><span data-ttu-id="1f40a-124"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>Protectkeywithexternalkey</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f40a-124"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="1f40a-125"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>Protectkeywithnumericalpassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f40a-125"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="1f40a-126"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>Protectkeywithpasspphrase</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f40a-126"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span></span></li>
<li><span data-ttu-id="1f40a-127"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>Protectkeywithtpm</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f40a-127"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="1f40a-128"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpin</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f40a-128"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="1f40a-129"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpinandstartupkey</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f40a-129"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="1f40a-130"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandstartupkey</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f40a-130"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="1f40a-131"><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt> <dt>2150694920 (0x80310008)</dt> </span><span class="sxs-lookup"><span data-stu-id="1f40a-131"><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt> <dt>2150694920 (0x80310008)</dt> </span></span></dl></td>
<td><span data-ttu-id="1f40a-132">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1f40a-132">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="1f40a-133">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="1f40a-133">Add a key protector to enable BitLocker.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="1f40a-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f40a-134">Remarks</span></span>

<span data-ttu-id="1f40a-135">Wenn das Volume vollständig verschlüsselt ist, wird durch das erfolgreiche Ausführen dieser Methode sichergestellt, dass das Volume geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="1f40a-135">If the volume is fully encrypted, successfully running this method ensures that the volume is protected.</span></span> <span data-ttu-id="1f40a-136">Wenn das Volume teilweise verschlüsselt ist, bedeutet eine erfolgreiche Ausführung dieser Methode, dass das Volume geschützt wird, sobald es vollständig verschlüsselt wird.</span><span class="sxs-lookup"><span data-stu-id="1f40a-136">If the volume is partially encrypted, successfully running this method implies that the volume will be protected when it becomes fully encrypted.</span></span> <span data-ttu-id="1f40a-137">Weitere Informationen finden Sie unter der [**getschutzstatus**](getprotectionstatus-win32-encryptablevolume.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1f40a-137">For more information, see the [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="1f40a-138">Wenn TPM-basierte Schlüssel Schutzvorrichtungen für das Volume vorhanden sind, werden diese Schutzvorrichtungen beim erfolgreichen Ausführen dieser Methode ebenfalls aktualisiert, damit das TPM die aktuellen Start Dienste auf der Plattform überprüft.</span><span class="sxs-lookup"><span data-stu-id="1f40a-138">If TPM-based key protectors exist for the volume, successfully running this method also refreshes these protectors so that the TPM validates against the current startup services on the platform.</span></span> <span data-ttu-id="1f40a-139">Anders ausgedrückt: Sie bestätigen, dass der Status des aktuellen Computers der richtige Zustand ist, den das TPM bei zukünftigen Neustarts des Computers prüft.</span><span class="sxs-lookup"><span data-stu-id="1f40a-139">In other words, you are asserting that the current computer state is the correct state that the TPM will check against on future computer restarts.</span></span>

<span data-ttu-id="1f40a-140">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="1f40a-140">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1f40a-141">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="1f40a-141">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1f40a-142">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1f40a-142">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1f40a-143">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="1f40a-143">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f40a-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f40a-144">Requirements</span></span>



| <span data-ttu-id="1f40a-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f40a-145">Requirement</span></span> | <span data-ttu-id="1f40a-146">Wert</span><span class="sxs-lookup"><span data-stu-id="1f40a-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f40a-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f40a-147">Minimum supported client</span></span><br/> | <span data-ttu-id="1f40a-148">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f40a-148">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1f40a-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f40a-149">Minimum supported server</span></span><br/> | <span data-ttu-id="1f40a-150">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f40a-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1f40a-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f40a-151">Namespace</span></span><br/>                | <span data-ttu-id="1f40a-152">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="1f40a-152">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="1f40a-153">MOF</span><span class="sxs-lookup"><span data-stu-id="1f40a-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f40a-154"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1f40a-154"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f40a-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f40a-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f40a-156">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="1f40a-156">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="1f40a-157">**Disablekeyprotector**</span><span class="sxs-lookup"><span data-stu-id="1f40a-157">**DisableKeyProtectors**</span></span>](disablekeyprotectors-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="1f40a-158">**Protectkeywithcertificatefile**</span><span class="sxs-lookup"><span data-stu-id="1f40a-158">**ProtectKeyWithCertificateFile**</span></span>](protectkeywithcertificatefile-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="1f40a-159">**Protectkeywithcertifierkeybibprint**</span><span class="sxs-lookup"><span data-stu-id="1f40a-159">**ProtectKeyWithCertificateThumbprint**</span></span>](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="1f40a-160">**Protectkeywithexternalkey**</span><span class="sxs-lookup"><span data-stu-id="1f40a-160">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="1f40a-161">**Protectkeywithnumericalpassword**</span><span class="sxs-lookup"><span data-stu-id="1f40a-161">**ProtectKeyWithNumericalPassword**</span></span>](protectkeywithnumericalpassword-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="1f40a-162">**Protectkeywithpasspphrase**</span><span class="sxs-lookup"><span data-stu-id="1f40a-162">**ProtectKeyWithPassphrase**</span></span>](protectkeywithpassphrase-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="1f40a-163">**Protectkeywithtpm**</span><span class="sxs-lookup"><span data-stu-id="1f40a-163">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="1f40a-164">**Protectkeywithtpmandpin**</span><span class="sxs-lookup"><span data-stu-id="1f40a-164">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="1f40a-165">**Protectkeywithtpmandpinandstartupkey**</span><span class="sxs-lookup"><span data-stu-id="1f40a-165">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="1f40a-166">**Protectkeywithtpmandstartupkey**</span><span class="sxs-lookup"><span data-stu-id="1f40a-166">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)
</dt> </dl>

 

 
