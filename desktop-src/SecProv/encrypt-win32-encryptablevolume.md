---
description: Startet die Verschlüsselung eines vollständig entschlüsselten Volumes oder nimmt die Verschlüsselung eines teilweise verschlüsselten Volumes wieder auf.
ms.assetid: bba8b800-309b-4268-8278-db69827bbdf6
title: Methode Verschlüsseln der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Encrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 463f13c250404e9a66095144166e74dbfae933ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050472"
---
# <a name="encrypt-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="e13bd-103">Methode Verschlüsseln der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="e13bd-103">Encrypt method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="e13bd-104">Die **Verschlüsselungsmethode der** Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " beginnt mit der Verschlüsselung eines vollständig entschlüsselten Volumes oder nimmt die Verschlüsselung eines teilweise verschlüsselten Volumes wieder auf.</span><span class="sxs-lookup"><span data-stu-id="e13bd-104">The **Encrypt** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins encryption of a fully decrypted volume, or resumes encryption of a partially encrypted volume.</span></span> <span data-ttu-id="e13bd-105">Wenn die Verschlüsselung angehalten oder ausgeführt wird, verhält sich diese Methode genauso wie " [**resumeconversion**](resumeconversion-win32-encryptablevolume.md)".</span><span class="sxs-lookup"><span data-stu-id="e13bd-105">When encryption is paused or in-progress, this method behaves the same as [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span></span> <span data-ttu-id="e13bd-106">Wenn die Entschlüsselung angehalten oder in Bearbeitung ist, beendet diese Methode das Entschlüsseln und beginnt mit der Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="e13bd-106">When decryption is paused or in-progress, this method stops the decryption and begins encryption.</span></span>

> [!Note]  
> <span data-ttu-id="e13bd-107">Wenn das Laufwerk Hardware verschlüsselt ist, werden die Daten von dieser Methode nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="e13bd-107">If the drive is hardware encrypted, this method does not encrypt data.</span></span> <span data-ttu-id="e13bd-108">Stattdessen wird der Band Status von "immer entsperrt" auf "nicht gesperrt" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e13bd-108">Instead, it sets the band status to "unlocked" from "always unlocked".</span></span> <span data-ttu-id="e13bd-109">Wenn das Band gesperrt ist, entsperrt oder schreibgeschützt ist, wird das Laufwerk als verschlüsselt eingestuft.</span><span class="sxs-lookup"><span data-stu-id="e13bd-109">If the band is locked, unlocked or is read-only, the drive is considered to be encrypted.</span></span>

 

<span data-ttu-id="e13bd-110">**Windows Vista:** Die Verschlüsselung eines anderen Volumes als dem aktuell aktuell laufenden Betriebssystem Volume wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e13bd-110">**Windows Vista:** Encryption of a volume other than the currently running operating system volume is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="e13bd-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e13bd-111">Syntax</span></span>


```mof
uint32 Encrypt(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e13bd-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e13bd-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e13bd-113">*Verschlüsselungsmethode* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e13bd-113">*EncryptionMethod* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e13bd-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e13bd-114">Type: **uint32**</span></span>

<span data-ttu-id="e13bd-115">Eine ganze Zahl ohne Vorzeichen, die den Verschlüsselungsalgorithmus und die Schlüsselgröße angibt, die zum Verschlüsseln des Volumes verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e13bd-115">An unsigned integer that specifies the encryption algorithm and key size used to encrypt the volume.</span></span> <span data-ttu-id="e13bd-116">Wenn dieser Parameter größer als 0 (null) ist und das Volume teilweise oder vollständig verschlüsselt ist, muss " *verschlüsselungmethod* " der vorhandenen Verschlüsselungsmethode des Volumes entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e13bd-116">If this parameter is greater than zero and the volume is partially or fully encrypted, *EncryptionMethod* must match the volume's existing encryption method.</span></span> <span data-ttu-id="e13bd-117">Wenn dieser Parameter größer als 0 (null) ist und die entsprechende Gruppenrichtlinie Einstellung mit einem gültigen Wert aktiviert ist, muss " *verschlüsselungsmethod* " mit der Gruppenrichtlinie Einstellung übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e13bd-117">If this parameter is greater than zero and the corresponding Group Policy setting is enabled with a valid value, *EncryptionMethod* must match the Group Policy setting.</span></span>

<span data-ttu-id="e13bd-118">Eine Liste möglicher Verschlüsselungsmethoden Werte finden Sie unter der [**getencryptionmethod**](getencryptionmethod-win32-encryptablevolume.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e13bd-118">For a list of possible EncryptionMethod values, see the [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="e13bd-119">Der Standardwert für Windows 7 oder niedriger ist: 1 (AES \_ 128 \_ mit \_ diffuser).</span><span class="sxs-lookup"><span data-stu-id="e13bd-119">Default value for Windows 7 or below is: 1 (AES\_128\_WITH\_DIFFUSER).</span></span>

<span data-ttu-id="e13bd-120">Der Standardwert für Windows 8, Windows 8.1 oder Windows 10, Version 1507 ist: 3 (AES \_ 128).</span><span class="sxs-lookup"><span data-stu-id="e13bd-120">Default value for Windows 8, Windows 8.1 or Windows 10, version 1507 is: 3 (AES\_128).</span></span>

<span data-ttu-id="e13bd-121">Der Standardwert für Windows 10, Version 1511 oder höher, ist: 6 (XTS \_ AES \_ 128).</span><span class="sxs-lookup"><span data-stu-id="e13bd-121">Default value for Windows 10, version 1511 or above is: 6 (XTS\_AES\_128).</span></span>

</dd> <dt>

<span data-ttu-id="e13bd-122">*Verschlüsselungsflags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e13bd-122">*EncryptionFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e13bd-123">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e13bd-123">Type: **uint32**</span></span>

<span data-ttu-id="e13bd-124">Flags, die das Verschlüsselungs Verhalten beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e13bd-124">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="e13bd-125">**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise und Windows Server 2008:** Dieser Parameter ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e13bd-125">**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise and Windows Server 2008:** This parameter is not available.</span></span>

<span data-ttu-id="e13bd-126">Eine Kombination von 32 Bits mit folgenden Bits, die aktuell definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e13bd-126">A combination of 32 bits with following bits currently defined.</span></span>



| <span data-ttu-id="e13bd-127">Wert</span><span class="sxs-lookup"><span data-stu-id="e13bd-127">Value</span></span>                                                                                  | <span data-ttu-id="e13bd-128">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e13bd-128">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e13bd-129"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="e13bd-129"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="e13bd-130">Führen Sie die Volumeverschlüsselung im reinen Daten Verschlüsselungs Modus aus, wenn Sie den neuen Verschlüsselungsprozess starten.</span><span class="sxs-lookup"><span data-stu-id="e13bd-130">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="e13bd-131">Wenn die Verschlüsselung angehalten oder beendet wurde, wird die Konvertierung durch Aufrufen der Methode " **verschlüsseln** " wirksam fortgesetzt, und der Wert dieses Bits wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e13bd-131">If encryption has been paused or stopped, calling the **Encrypt** method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="e13bd-132">Dieses Bit ist nur wirksam, wenn die Verschlüsselungs-oder [**verschlüsseltafterhardwaretest**](encryptafterhardwaretest-win32-encryptablevolume.md) - **Methoden die Verschlüsselung** aus dem vollständig entschlüsselten Zustand, dem Entschlüsselungs Status oder dem Status der entschlüsselten Entschlüsselung starten.</span><span class="sxs-lookup"><span data-stu-id="e13bd-132">This bit only has effect when either the **Encrypt** or [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="e13bd-133">Wenn dieses Bit 0 (null) ist, was bedeutet, dass es beim Starten des neuen Verschlüsselungs Vorgangs nicht festgelegt ist, wird die vollständige Modus-Konvertierung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e13bd-133">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="e13bd-134"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="e13bd-134"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="e13bd-135">Ausführen einer bedarfsgesteuerten Löschung des freien Speicherplatzes auf dem Volume.</span><span class="sxs-lookup"><span data-stu-id="e13bd-135">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="e13bd-136">Das Aufrufen der **Verschlüsselungs** Methode mit diesem Bitset ist nur zulässig, wenn das Volume derzeit nicht in den Status "verschlüsselt" versetzt wird und sich im Status "verschlüsselt" befindet.</span><span class="sxs-lookup"><span data-stu-id="e13bd-136">Calling the **Encrypt** method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="e13bd-137"><dt>0x00010000 bis </dt></span><span class="sxs-lookup"><span data-stu-id="e13bd-137"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="e13bd-138">Führt den angeforderten Vorgang synchron aus.</span><span class="sxs-lookup"><span data-stu-id="e13bd-138">Perform the requested operation synchronously.</span></span> <span data-ttu-id="e13bd-139">Der-Befehl wird blockiert, bis der angeforderte Vorgang abgeschlossen ist oder unterbrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="e13bd-139">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="e13bd-140">Dieses Flag wird nur mit der Methode " **verschlüsseln** " unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e13bd-140">This flag is only supported with the **Encrypt** method.</span></span> <span data-ttu-id="e13bd-141">Dieses Flag kann angegeben werden, wenn " **verschlüsseln** " aufgerufen wird, um die beendete oder unterbrochene Verschlüsselung oder das Zurücksetzen oder Löschen von Verschlüsselung oder Zurücksetzen zu beenden.</span><span class="sxs-lookup"><span data-stu-id="e13bd-141">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="e13bd-142">Dies ermöglicht dem Aufrufer, synchron zu warten, bis der Prozess abgeschlossen oder unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="e13bd-142">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e13bd-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e13bd-143">Return value</span></span>

<span data-ttu-id="e13bd-144">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e13bd-144">Type: **uint32**</span></span>

<span data-ttu-id="e13bd-145">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="e13bd-145">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="e13bd-146">Diese Methode wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e13bd-146">This method returns immediately.</span></span> <span data-ttu-id="e13bd-147">Wenn das Volume bereits vollständig verschlüsselt ist und keine anderen Fehler zurückgegeben werden, gibt diese Methode 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="e13bd-147">If the volume is already fully encrypted and no other errors are returned, this method returns 0.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e13bd-148">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="e13bd-148">Return code/value</span></span></th>
<th><span data-ttu-id="e13bd-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e13bd-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="e13bd-150"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span><span class="sxs-lookup"><span data-stu-id="e13bd-150"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="e13bd-151">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e13bd-151">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e13bd-152"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span><span class="sxs-lookup"><span data-stu-id="e13bd-152"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span></span></dl></td>
<td><span data-ttu-id="e13bd-153">Der Parameter " <em>verschlüsselungmethod</em> " wird bereitgestellt, befindet sich jedoch nicht im bekannten Bereich oder entspricht nicht der aktuellen Gruppenrichtlinie Einstellung.</span><span class="sxs-lookup"><span data-stu-id="e13bd-153">The <em>EncryptionMethod</em> parameter is provided but is not within the known range or does not match the current Group Policy setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="e13bd-154"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span><span class="sxs-lookup"><span data-stu-id="e13bd-154"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span></span></dl></td>
<td><span data-ttu-id="e13bd-155">Für das Volume ist kein Verschlüsselungsschlüssel vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e13bd-155">No encryption key exists for the volume.</span></span> <span data-ttu-id="e13bd-156">Deaktivieren Sie entweder die Schlüssel Schutzvorrichtungen mithilfe der <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>disablekeyprotector</strong></a> -Methode, oder verwenden Sie eine der folgenden Methoden, um Schlüssel Schutzvorrichtungen für das Volume anzugeben:</span><span class="sxs-lookup"><span data-stu-id="e13bd-156">Either disable key protectors by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method or use one of the following methods to specify key protectors for the volume:</span></span><br/>
<ul>
<li><span data-ttu-id="e13bd-157"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>Protectkeywithexternalkey</strong></a></span><span class="sxs-lookup"><span data-stu-id="e13bd-157"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="e13bd-158"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>Protectkeywithnumericalpassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="e13bd-158"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="e13bd-159"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>Protectkeywithtpm</strong></a></span><span class="sxs-lookup"><span data-stu-id="e13bd-159"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="e13bd-160"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpin</strong></a></span><span class="sxs-lookup"><span data-stu-id="e13bd-160"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="e13bd-161"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpinandstartupkey</strong></a></span><span class="sxs-lookup"><span data-stu-id="e13bd-161"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="e13bd-162"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandstartupkey</strong></a></span><span class="sxs-lookup"><span data-stu-id="e13bd-162"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul><span data-ttu-id="e13bd-163">
<strong>Windows Vista:</strong> Wenn kein Verschlüsselungsschlüssel für das Volume vorhanden ist, wird stattdessen ERROR_INVALID_OPERATION zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e13bd-163">
<strong>Windows Vista:</strong> When no encryption key exists for the volume, ERROR_INVALID_OPERATION is returned instead.</span></span> <span data-ttu-id="e13bd-164">Der Dezimalwert ist 4317, und der hexadezimale Wert ist 0x10dd.</span><span class="sxs-lookup"><span data-stu-id="e13bd-164">The decimal value is 4317 and the hexadecimal value is 0x10DD.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e13bd-165"><dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002d)</dt> </span><span class="sxs-lookup"><span data-stu-id="e13bd-165"><dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D)</dt> </span></span></dl></td>
<td><span data-ttu-id="e13bd-166">Die bereitgestellte Verschlüsselungsmethode entspricht nicht der des teilweise oder vollständig verschlüsselten Volumes.</span><span class="sxs-lookup"><span data-stu-id="e13bd-166">The provided encryption method does not match that of the partially or fully encrypted volume.</span></span> <span data-ttu-id="e13bd-167">Wenn Sie die Verschlüsselung fortsetzen möchten, lassen Sie den Parameter " <em>verschlüsselungmethod</em> " leer, oder verwenden Sie den Wert 0</span><span class="sxs-lookup"><span data-stu-id="e13bd-167">To continue encryption, leave the <em>EncryptionMethod</em> parameter blank or use a value of zero.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="e13bd-168"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span><span class="sxs-lookup"><span data-stu-id="e13bd-168"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span></span></dl></td>
<td><span data-ttu-id="e13bd-169">Das Volume kann nicht verschlüsselt werden, da dieser Computer als Teil eines Server Clusters konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="e13bd-169">The volume cannot be encrypted because this computer is configured to be part of a server cluster.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e13bd-170"><dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </span><span class="sxs-lookup"><span data-stu-id="e13bd-170"><dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </span></span></dl></td>
<td><span data-ttu-id="e13bd-171">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="e13bd-171">The volume is locked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="e13bd-172"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002c)</dt> </span><span class="sxs-lookup"><span data-stu-id="e13bd-172"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span></span></dl></td>
<td><span data-ttu-id="e13bd-173">Es wurden keine Schlüssel Schutzvorrichtungen des &quot; typnumerischen Kennworts &quot; angegeben.</span><span class="sxs-lookup"><span data-stu-id="e13bd-173">No key protectors of the type &quot;Numerical Password&quot; are specified.</span></span> <span data-ttu-id="e13bd-174">Für den Gruppenrichtlinie ist eine Sicherung der Wiederherstellungs Informationen erforderlich, um Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="e13bd-174">The Group Policy requires a backup of recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="e13bd-175">Um mindestens eine Schlüssel Schutzvorrichtung dieses Typs hinzuzufügen, verwenden Sie die <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>protectkeywithnumericalpassword</strong></a> -Methode.</span><span class="sxs-lookup"><span data-stu-id="e13bd-175">To add at least one key protector of that type, use the <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> method.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="e13bd-176">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e13bd-176">Remarks</span></span>

<span data-ttu-id="e13bd-177">Wenn Sie diese Methode ohne den zweiten optionalen Parameter verwenden (gemäß der Definition von Windows 7 und Windows Vista Enterprise), initiiert die Methode immer die Konvertierung im vollständigen Modus, um das abwärts kompatible Verhalten beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="e13bd-177">When you use this method without the second optional parameter (according to the Windows 7 and Windows Vista Enterprise definition), the method will always initiate full mode conversion in order to keep backward compatible behavior.</span></span> <span data-ttu-id="e13bd-178">Auf diese Weise wird die Sicherheits Erwartung vorhandener Anwendungen und Skripts nicht durch das Hinzufügen des zweiten optionalen Parameters in Windows 8 und Windows Server 2012 beschädigt.</span><span class="sxs-lookup"><span data-stu-id="e13bd-178">This way the security expectation of existing applications and scripts will not be broken with the addition of the second optional parameter in Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="e13bd-179">Sie können [**getdeversionstatus**](getconversionstatus-win32-encryptablevolume.md) aufrufen, um zu bestimmen, ob die Verschlüsselung ausgeführt wird, und den Prozentsatz des Volumes, das verschlüsselt wurde.</span><span class="sxs-lookup"><span data-stu-id="e13bd-179">You can call [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to determine whether encryption is in progress and the percentage of the volume that has been encrypted.</span></span>

<span data-ttu-id="e13bd-180">Wenn das Volume vollständig verschlüsselt ist und Schlüssel Schutzvorrichtungen hinzugefügt und aktiviert wurden, ändert sich der Schutzstatus für das Volume in "ein".</span><span class="sxs-lookup"><span data-stu-id="e13bd-180">After the volume is fully encrypted and if key protectors have been added and enabled, the protection status for the volume changes to "on".</span></span>

<span data-ttu-id="e13bd-181">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="e13bd-181">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e13bd-182">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="e13bd-182">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="e13bd-183">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e13bd-183">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e13bd-184">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="e13bd-184">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e13bd-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e13bd-185">Requirements</span></span>



| <span data-ttu-id="e13bd-186">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e13bd-186">Requirement</span></span> | <span data-ttu-id="e13bd-187">Wert</span><span class="sxs-lookup"><span data-stu-id="e13bd-187">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e13bd-188">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e13bd-188">Minimum supported client</span></span><br/> | <span data-ttu-id="e13bd-189">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e13bd-189">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e13bd-190">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e13bd-190">Minimum supported server</span></span><br/> | <span data-ttu-id="e13bd-191">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e13bd-191">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e13bd-192">Namespace</span><span class="sxs-lookup"><span data-stu-id="e13bd-192">Namespace</span></span><br/>                | <span data-ttu-id="e13bd-193">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="e13bd-193">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="e13bd-194">MOF</span><span class="sxs-lookup"><span data-stu-id="e13bd-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e13bd-195"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e13bd-195"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e13bd-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e13bd-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13bd-197">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="e13bd-197">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
