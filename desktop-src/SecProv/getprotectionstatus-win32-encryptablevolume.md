---
description: Gibt an, ob das Volume und der zugehörige Verschlüsselungsschlüssel geschützt sind.
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: Getschutzstatus-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetProtectionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5f3fa2aaa019097a01a6e6d1628d7c4fe9b82710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750841"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="3efa4-103">Getschutzstatus-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="3efa4-103">GetProtectionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="3efa4-104">Die **getschutzstatus** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt an, ob das Volume und der zugehörige Verschlüsselungsschlüssel (sofern vorhanden) gesichert sind.</span><span class="sxs-lookup"><span data-stu-id="3efa4-104">The **GetProtectionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the volume and its encryption key (if any) are secured.</span></span>

<span data-ttu-id="3efa4-105">Der Schutz ist deaktiviert, wenn ein Volume unverschlüsselt oder teilweise verschlüsselt ist, oder wenn der Verschlüsselungsschlüssel des Volumes im Klartext auf der Festplatte verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3efa4-105">Protection is off if a volume is unencrypted or partially encrypted, or if the volume's encryption key is available in the clear on the hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="3efa4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3efa4-106">Syntax</span></span>


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="3efa4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3efa4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3efa4-108">Schutz *Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3efa4-108">*ProtectionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3efa4-109">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3efa4-109">Type: **uint32**</span></span>

<span data-ttu-id="3efa4-110">Gibt an, ob das Volume und der Verschlüsselungsschlüssel (sofern vorhanden) gesichert sind.</span><span class="sxs-lookup"><span data-stu-id="3efa4-110">Specifies whether the volume and the encryption key (if any) are secured.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3efa4-111">Wert</span><span class="sxs-lookup"><span data-stu-id="3efa4-111">Value</span></span></th>
<th><span data-ttu-id="3efa4-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3efa4-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl> <span data-ttu-id="3efa4-113"><dt><strong>Ungeschützt</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="3efa4-113"><dt><strong>Unprotected</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="3efa4-114">Schutz deaktiviert</span><span class="sxs-lookup"><span data-stu-id="3efa4-114">PROTECTION OFF</span></span><br/> <span data-ttu-id="3efa4-115">Für eine Standard-HDD:</span><span class="sxs-lookup"><span data-stu-id="3efa4-115">For a standard HDD:</span></span><br/> <span data-ttu-id="3efa4-116">Das Volume ist unverschlüsselt, teilweise verschlüsselt, oder der Verschlüsselungsschlüssel des Volumes ist im Klartext auf der Festplatte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3efa4-116">The volume is unencrypted, partially encrypted, or the volume's encryption key is available in the clear on the hard disk.</span></span> <span data-ttu-id="3efa4-117">Der Verschlüsselungsschlüssel ist im Klartext auf der Festplatte verfügbar, wenn die Schlüssel Schutzvorrichtungen mithilfe der <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>disablekeyprotector</strong></a> -Methode deaktiviert wurden oder wenn keine Schlüssel Schutzvorrichtungen mithilfe der folgenden Methoden angegeben wurden:</span><span class="sxs-lookup"><span data-stu-id="3efa4-117">The encryption key is available in the clear on the hard disk if key protectors have been disabled by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method or if no key protectors have been specified by using the following methods:</span></span>
<ul>
<li><span data-ttu-id="3efa4-118"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>Protectkeywithcertificatefile</strong></a></span><span class="sxs-lookup"><span data-stu-id="3efa4-118"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span></span></li>
<li><span data-ttu-id="3efa4-119"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>Protectkeywithcertifierkeybibprint</strong></a></span><span class="sxs-lookup"><span data-stu-id="3efa4-119"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span></span></li>
<li><span data-ttu-id="3efa4-120"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>Protectkeywithexternalkey</strong></a></span><span class="sxs-lookup"><span data-stu-id="3efa4-120"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="3efa4-121"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>Protectkeywithnumericalpassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="3efa4-121"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="3efa4-122"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>Protectkeywithpasspphrase</strong></a></span><span class="sxs-lookup"><span data-stu-id="3efa4-122"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span></span></li>
<li><span data-ttu-id="3efa4-123"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>Protectkeywithtpm</strong></a></span><span class="sxs-lookup"><span data-stu-id="3efa4-123"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="3efa4-124"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpin</strong></a></span><span class="sxs-lookup"><span data-stu-id="3efa4-124"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="3efa4-125"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpinandstartupkey</strong></a></span><span class="sxs-lookup"><span data-stu-id="3efa4-125"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="3efa4-126"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandstartupkey</strong></a></span><span class="sxs-lookup"><span data-stu-id="3efa4-126"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="3efa4-127">Für einen ehdd:</span><span class="sxs-lookup"><span data-stu-id="3efa4-127">For an EHDD:</span></span><br/> <span data-ttu-id="3efa4-128">Das Band für das Volume ist dauerhaft entsperrt, verfügt über keinen Schlüssel Manager oder wird von einem Drittanbieter-Schlüssel-Manager verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3efa4-128">The band for the volume is perpetually unlocked, has no key manager, or is managed by a third party key manager.</span></span><br/> <span data-ttu-id="3efa4-129">Dies kann auch bedeuten, dass das Band von BitLocker verwaltet wird, aber die <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>disablekeyprotector</strong></a> -Methode aufgerufen wurde und das Laufwerk angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="3efa4-129">This can also mean that the band is managed by BitLocker but the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method has been called and the drive is suspended.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl> <span data-ttu-id="3efa4-130"><dt><strong>Geschützt</strong></dt> <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="3efa4-130"><dt><strong>Protected</strong></dt> <dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="3efa4-131">Schutz für</span><span class="sxs-lookup"><span data-stu-id="3efa4-131">PROTECTION ON</span></span><br/> <span data-ttu-id="3efa4-132">Für eine Standard-HDD:</span><span class="sxs-lookup"><span data-stu-id="3efa4-132">For a standard HDD:</span></span><br/> <span data-ttu-id="3efa4-133">Das Volume ist vollständig verschlüsselt, und der Verschlüsselungsschlüssel für das Volume ist nicht im Klartext auf der Festplatte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3efa4-133">The volume is fully encrypted and the encryption key for the volume is not available in the clear on the hard disk.</span></span><br/> <span data-ttu-id="3efa4-134">Für einen ehdd:</span><span class="sxs-lookup"><span data-stu-id="3efa4-134">For an EHDD:</span></span><br/> <span data-ttu-id="3efa4-135">BitLocker ist der Schlüssel-Manager für das Band.</span><span class="sxs-lookup"><span data-stu-id="3efa4-135">BitLocker is the key manager for the band.</span></span> <span data-ttu-id="3efa4-136">Das Laufwerk kann gesperrt oder entsperrt, aber nicht dauerhaft entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="3efa4-136">The drive can be locked or unlocked but cannot be perpetually unlocked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="3efa4-137"><dt><strong>Unbekannt</strong></dt> <dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="3efa4-137"><dt><strong>Unknown</strong></dt> <dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="3efa4-138">Der volumeschutzstatus kann nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="3efa4-138">The volume protection status cannot be determined.</span></span> <span data-ttu-id="3efa4-139">Dies kann dadurch verursacht werden, dass sich das Volume im gesperrten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="3efa4-139">This can be caused by the volume being in a locked state.</span></span><br/> <span data-ttu-id="3efa4-140"><strong>Windows Vista Ultimate, Windows Vista Enterprise und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3efa4-140"><strong>Windows Vista Ultimate, Windows Vista Enterprise and Windows Server 2008:</strong> This value is not supported.</span></span> <span data-ttu-id="3efa4-141">Dieser Wert wird ab Windows 7 und Windows Server 2008 R2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3efa4-141">This value is supported beginning with Windows 7 and Windows Server 2008 R2.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3efa4-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3efa4-142">Return value</span></span>

<span data-ttu-id="3efa4-143">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3efa4-143">Type: **uint32**</span></span>

<span data-ttu-id="3efa4-144">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="3efa4-144">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="3efa4-145">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="3efa4-145">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="3efa4-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3efa4-146">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="3efa4-147"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="3efa4-147"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="3efa4-148">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3efa4-148">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3efa4-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3efa4-149">Remarks</span></span>

<span data-ttu-id="3efa4-150">Sie können ein Volume nur verschlüsseln, wenn Sie zuerst [**disablekeyprotector**](disablekeyprotectors-win32-encryptablevolume.md) oder eine der folgenden Methoden verwenden:</span><span class="sxs-lookup"><span data-stu-id="3efa4-150">You can encrypt a volume only if you either call [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) first or use one of the following methods:</span></span>

-   [<span data-ttu-id="3efa4-151">**Protectkeywithcertificatefile**</span><span class="sxs-lookup"><span data-stu-id="3efa4-151">**ProtectKeyWithCertificateFile**</span></span>](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [<span data-ttu-id="3efa4-152">**Protectkeywithcertifierkeybibprint**</span><span class="sxs-lookup"><span data-stu-id="3efa4-152">**ProtectKeyWithCertificateThumbprint**</span></span>](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [<span data-ttu-id="3efa4-153">**Protectkeywithexternalkey**</span><span class="sxs-lookup"><span data-stu-id="3efa4-153">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="3efa4-154">**Protectkeywithnumericalpassword**</span><span class="sxs-lookup"><span data-stu-id="3efa4-154">**ProtectKeyWithNumericalPassword**</span></span>](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [<span data-ttu-id="3efa4-155">**Protectkeywithpasspphrase**</span><span class="sxs-lookup"><span data-stu-id="3efa4-155">**ProtectKeyWithPassphrase**</span></span>](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [<span data-ttu-id="3efa4-156">**Protectkeywithtpm**</span><span class="sxs-lookup"><span data-stu-id="3efa4-156">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
-   [<span data-ttu-id="3efa4-157">**Protectkeywithtpmandpin**</span><span class="sxs-lookup"><span data-stu-id="3efa4-157">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [<span data-ttu-id="3efa4-158">**Protectkeywithtpmandpinandstartupkey**</span><span class="sxs-lookup"><span data-stu-id="3efa4-158">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="3efa4-159">**Protectkeywithtpmandstartupkey**</span><span class="sxs-lookup"><span data-stu-id="3efa4-159">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

<span data-ttu-id="3efa4-160">Wenn der Datenträger verschlüsselt ist und der Schutz *Status* NULL (Schutz deaktiviert) zurückgibt, werden die Schlüssel daher deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3efa4-160">Therefore, if the disk is encrypted and *ProtectionStatus* returns zero (PROTECTION OFF), keys are disabled.</span></span>

<span data-ttu-id="3efa4-161">Verwenden Sie [**getkeyprotector**](getkeyprotectors-win32-encryptablevolume.md) , um die Schlüssel Schutzvorrichtungen aufzulisten, die angegeben wurden, um den Verschlüsselungsschlüssel des Volumes zu sichern.</span><span class="sxs-lookup"><span data-stu-id="3efa4-161">Use [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) to list the key protectors that have been specified to secure the volume's encryption key.</span></span> <span data-ttu-id="3efa4-162">Wenn Schlüssel Schutzvorrichtungen vorhanden sind, der Schutz aber 0 (null) ist, verwenden Sie [**enablekeyprotector**](enablekeyprotectors-win32-encryptablevolume.md) , um den volumeschutz zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3efa4-162">If key protectors exist but protection is zero (PROTECTION OFF), use [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) to turn on volume protection.</span></span>

<span data-ttu-id="3efa4-163">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="3efa4-163">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3efa4-164">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="3efa4-164">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="3efa4-165">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3efa4-165">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3efa4-166">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="3efa4-166">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3efa4-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3efa4-167">Requirements</span></span>



| <span data-ttu-id="3efa4-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3efa4-168">Requirement</span></span> | <span data-ttu-id="3efa4-169">Wert</span><span class="sxs-lookup"><span data-stu-id="3efa4-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3efa4-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3efa4-170">Minimum supported client</span></span><br/> | <span data-ttu-id="3efa4-171">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3efa4-171">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3efa4-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3efa4-172">Minimum supported server</span></span><br/> | <span data-ttu-id="3efa4-173">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3efa4-173">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3efa4-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="3efa4-174">Namespace</span></span><br/>                | <span data-ttu-id="3efa4-175">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="3efa4-175">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="3efa4-176">MOF</span><span class="sxs-lookup"><span data-stu-id="3efa4-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3efa4-177"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3efa4-177"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3efa4-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3efa4-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3efa4-179">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="3efa4-179">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
