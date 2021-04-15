---
description: Startet die Verschlüsselung eines vollständig entschlüsselten Betriebssystem Volume nach einem Hardware Test.
ms.assetid: 216c96bb-7737-4421-8b16-1ce295342266
title: Verschlüsseltashardwaretest-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EncryptAfterHardwareTest
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f356b9adda5e1b25fdd3d9fc39ace5cf8028da32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525688"
---
# <a name="encryptafterhardwaretest-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="38d78-103">Verschlüsseltaberterhardwaretest-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="38d78-103">EncryptAfterHardwareTest method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="38d78-104">Die **verschlüsseltafterhardwaretest** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " beginnt nach einem Hardware Test mit der Verschlüsselung eines vollständig entschlüsselten Betriebssystem Volume.</span><span class="sxs-lookup"><span data-stu-id="38d78-104">The **EncryptAfterHardwareTest** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins encryption of a fully decrypted operating system volume after a hardware test.</span></span> <span data-ttu-id="38d78-105">Zum Durchführen dieses Hardware Tests ist ein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="38d78-105">A reboot is required to perform this hardware test.</span></span> <span data-ttu-id="38d78-106">Verwenden Sie diese Methode anstelle der Methode " [**verschlüsseln**](encrypt-win32-encryptablevolume.md) ", um zu überprüfen, ob BitLocker erwartungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="38d78-106">Use this method instead of the [**Encrypt**](encrypt-win32-encryptablevolume.md) method to check that BitLocker will work as expected.</span></span>

> [!Note]  
> <span data-ttu-id="38d78-107">Wenn die Festplatte Hardware verschlüsselt ist, werden die Daten von dieser Methode nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="38d78-107">If the hard drive is hardware encrypted, this method does not encrypt data.</span></span> <span data-ttu-id="38d78-108">Stattdessen wird der Band Status von "dauerhaft entsperrt" auf "entsperrt" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="38d78-108">Instead, it sets the band status to unlocked from "perpetually unlocked".</span></span> <span data-ttu-id="38d78-109">Wenn das Band gesperrt ist, entsperrt oder schreibgeschützt ist, wird das Laufwerk als verschlüsselt eingestuft.</span><span class="sxs-lookup"><span data-stu-id="38d78-109">If the band is locked, unlocked or is read-only, the drive is considered to be encrypted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="38d78-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="38d78-110">Syntax</span></span>


```mof
uint32 EncryptAfterHardwareTest(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a><span data-ttu-id="38d78-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="38d78-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38d78-112">*Verschlüsselungsmethode* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="38d78-112">*EncryptionMethod* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="38d78-113">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38d78-113">Type: **uint32**</span></span>

<span data-ttu-id="38d78-114">Gibt den Verschlüsselungsalgorithmus und die Schlüsselgröße an, die zum Verschlüsseln des Volumes verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38d78-114">Specifies the encryption algorithm and key size used to encrypt the volume.</span></span> <span data-ttu-id="38d78-115">Lassen Sie diesen Parameter leer, um den Standardwert 0 (null) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="38d78-115">Leave this parameter blank to use the default value of zero.</span></span> <span data-ttu-id="38d78-116">Wenn das Volume teilweise oder vollständig verschlüsselt ist, muss der Wert dieses Parameters 0 sein oder mit der vorhandenen Verschlüsselungsmethode des Volumes identisch sein.</span><span class="sxs-lookup"><span data-stu-id="38d78-116">If the volume is partially or fully encrypted, the value of this parameter must be 0 or match the volume's existing encryption method.</span></span> <span data-ttu-id="38d78-117">Wenn die entsprechende Gruppenrichtlinie Einstellung mit einem gültigen Wert aktiviert wurde, muss der Wert dieses Parameters 0 sein oder mit der Gruppenrichtlinie Einstellung übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="38d78-117">If the corresponding Group Policy setting has been enabled with a valid value, the value of this parameter must be 0 or match the Group Policy setting.</span></span>

<span data-ttu-id="38d78-118">Wenn die entsprechende Gruppenrichtlinie Einstellung ungültig ist, wird der Standardwert von AES 128 mit Diffuser verwendet.</span><span class="sxs-lookup"><span data-stu-id="38d78-118">If the corresponding Group Policy setting is invalid, the default of AES 128 with diffuser is used.</span></span>



| <span data-ttu-id="38d78-119">Wert</span><span class="sxs-lookup"><span data-stu-id="38d78-119">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="38d78-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="38d78-120">Meaning</span></span>                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <span data-ttu-id="38d78-121"><dt>**Nicht angegeben**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="38d78-121"><dt>**Unspecified**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="38d78-122">Verwenden Sie die aktuelle Gruppenrichtlinie Einstellung, falls verfügbar und gültig, oder andernfalls die Standard Verschlüsselungsmethode.</span><span class="sxs-lookup"><span data-stu-id="38d78-122">Use the current Group Policy setting, if available and valid, or the default encryption method otherwise.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="38d78-123"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="38d78-123"><dt>1</dt></span></span> </dl>                                                                                                                                                                | <span data-ttu-id="38d78-124">AES 128 mit diffuser</span><span class="sxs-lookup"><span data-stu-id="38d78-124">AES 128 WITH DIFFUSER</span></span><br/> <span data-ttu-id="38d78-125">Verschlüsseln Sie das Volume mit dem Advanced Encryption Standard (AES)-Algorithmus, der mit einer diffuser-Schicht erweitert wurde, und verwenden Sie eine AES-Schlüsselgröße von 128 Bits.</span><span class="sxs-lookup"><span data-stu-id="38d78-125">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer and by using an AES key size of 128 bits.</span></span><br/> |
| <dl> <span data-ttu-id="38d78-126"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="38d78-126"><dt>2</dt></span></span> </dl>                                                                                                                                                                | <span data-ttu-id="38d78-127">AES 256 mit diffuser</span><span class="sxs-lookup"><span data-stu-id="38d78-127">AES 256 WITH DIFFUSER</span></span><br/> <span data-ttu-id="38d78-128">Verschlüsseln Sie das Volume mit dem Advanced Encryption Standard (AES)-Algorithmus, der mit einer diffuser-Schicht erweitert wurde, und verwenden Sie eine AES-Schlüsselgröße von 256 Bits.</span><span class="sxs-lookup"><span data-stu-id="38d78-128">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer and by using an AES key size of 256 bits.</span></span><br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <span data-ttu-id="38d78-129"><dt>**AES \_ 128**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="38d78-129"><dt>**AES\_128**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="38d78-130">Verschlüsseln Sie das Volume mit dem Advanced Encryption Standard-Algorithmus (AES) und mit einer AES-Schlüsselgröße von 128 Bits.</span><span class="sxs-lookup"><span data-stu-id="38d78-130">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm and by using an AES key size of 128 bits.</span></span><br/>                                                                 |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <span data-ttu-id="38d78-131"><dt>**AES \_ 256**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="38d78-131"><dt>**AES\_256**</dt> <dt>4</dt></span></span> </dl>                                          | <span data-ttu-id="38d78-132">Verschlüsseln Sie das Volume mit dem Advanced Encryption Standard-Algorithmus (AES) und mit einer AES-Schlüsselgröße von 256 Bits.</span><span class="sxs-lookup"><span data-stu-id="38d78-132">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm and by using an AES key size of 256 bits.</span></span><br/>                                                                 |



 

</dd> <dt>

<span data-ttu-id="38d78-133">*Verschlüsselungsflags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="38d78-133">*EncryptionFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="38d78-134">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38d78-134">Type: **uint32**</span></span>

<span data-ttu-id="38d78-135">Flags, die das Verschlüsselungs Verhalten beschreiben.</span><span class="sxs-lookup"><span data-stu-id="38d78-135">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="38d78-136">**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise und Windows Server 2008:** Dieser Parameter ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="38d78-136">**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise and Windows Server 2008:** This parameter is not available.</span></span>

<span data-ttu-id="38d78-137">Eine Kombination von 32 Bits mit den folgenden Bits, die aktuell definiert sind.</span><span class="sxs-lookup"><span data-stu-id="38d78-137">A combination of 32 bits with the following bits currently defined.</span></span>



| <span data-ttu-id="38d78-138">Wert</span><span class="sxs-lookup"><span data-stu-id="38d78-138">Value</span></span>                                                                                  | <span data-ttu-id="38d78-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="38d78-139">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="38d78-140"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="38d78-140"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="38d78-141">Führen Sie die Volumeverschlüsselung im reinen Daten Verschlüsselungs Modus aus, wenn Sie den neuen Verschlüsselungsprozess starten.</span><span class="sxs-lookup"><span data-stu-id="38d78-141">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="38d78-142">Wenn die Verschlüsselung angehalten oder beendet wurde, wird die Konvertierung durch Aufrufen der Methode " [**verschlüsseln**](encrypt-win32-encryptablevolume.md) " wirksam fortgesetzt, und der Wert dieses Bits wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="38d78-142">If encryption has been paused or stopped, calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="38d78-143">Dieses Bit ist nur wirksam, wenn die Verschlüsselungs-oder **verschlüsseltafterhardwaretest** - **Methoden die Verschlüsselung** aus dem vollständig entschlüsselten Zustand, dem Entschlüsselungs Status oder dem Status der entschlüsselten Entschlüsselung starten.</span><span class="sxs-lookup"><span data-stu-id="38d78-143">This bit only has effect when either the **Encrypt** or **EncryptAfterHardwareTest** methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="38d78-144">Wenn dieses Bit 0 (null) ist, was bedeutet, dass es beim Starten des neuen Verschlüsselungs Vorgangs nicht festgelegt ist, wird die vollständige Modus-Konvertierung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38d78-144">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="38d78-145"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="38d78-145"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="38d78-146">Ausführen einer bedarfsgesteuerten Löschung des freien Speicherplatzes auf dem Volume.</span><span class="sxs-lookup"><span data-stu-id="38d78-146">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="38d78-147">Das Aufrufen der [**Verschlüsselungs**](encrypt-win32-encryptablevolume.md) Methode mit diesem Bitset ist nur zulässig, wenn das Volume derzeit nicht in den Status "verschlüsselt" versetzt wird und sich im Status "verschlüsselt" befindet.</span><span class="sxs-lookup"><span data-stu-id="38d78-147">Calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="38d78-148"><dt>0x00010000 bis </dt></span><span class="sxs-lookup"><span data-stu-id="38d78-148"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="38d78-149">Führt den angeforderten Vorgang synchron aus.</span><span class="sxs-lookup"><span data-stu-id="38d78-149">Perform the requested operation synchronously.</span></span> <span data-ttu-id="38d78-150">Der-Befehl wird blockiert, bis der angeforderte Vorgang abgeschlossen ist oder unterbrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="38d78-150">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="38d78-151">Dieses Flag wird nur mit der Methode " [**verschlüsseln**](encrypt-win32-encryptablevolume.md) " unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38d78-151">This flag is only supported with the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="38d78-152">Dieses Flag kann angegeben werden, wenn " **verschlüsseln** " aufgerufen wird, um die beendete oder unterbrochene Verschlüsselung oder das Zurücksetzen oder Löschen von Verschlüsselung oder Zurücksetzen zu beenden.</span><span class="sxs-lookup"><span data-stu-id="38d78-152">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="38d78-153">Dies ermöglicht dem Aufrufer, synchron zu warten, bis der Prozess abgeschlossen oder unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="38d78-153">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38d78-154">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38d78-154">Return value</span></span>

<span data-ttu-id="38d78-155">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38d78-155">Type: **uint32**</span></span>

<span data-ttu-id="38d78-156">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="38d78-156">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="38d78-157">Diese Methode wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="38d78-157">This method returns immediately.</span></span> <span data-ttu-id="38d78-158">Wenn das Volume bereits vollständig verschlüsselt ist und keine anderen Fehler zurückgegeben werden, gibt diese Methode 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="38d78-158">If the volume is already fully encrypted and no other errors are returned, this method returns zero.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="38d78-159">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="38d78-159">Return code/value</span></span></th>
<th><span data-ttu-id="38d78-160">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38d78-160">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="38d78-161"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span><span class="sxs-lookup"><span data-stu-id="38d78-161"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="38d78-162">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="38d78-162">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="38d78-163"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span><span class="sxs-lookup"><span data-stu-id="38d78-163"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span></span></dl></td>
<td><span data-ttu-id="38d78-164">Der Parameter " <em>verschlüsselungmethod</em> " wird bereitgestellt, befindet sich jedoch nicht im bekannten Bereich oder entspricht nicht der aktuellen Gruppenrichtlinie Einstellung.</span><span class="sxs-lookup"><span data-stu-id="38d78-164">The <em>EncryptionMethod</em> parameter is provided but is not within the known range or does not match the current Group Policy setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="38d78-165"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span><span class="sxs-lookup"><span data-stu-id="38d78-165"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span></span></dl></td>
<td><span data-ttu-id="38d78-166">Für das Volume ist kein Verschlüsselungsschlüssel vorhanden.</span><span class="sxs-lookup"><span data-stu-id="38d78-166">No encryption key exists for the volume.</span></span><br/> <span data-ttu-id="38d78-167">Deaktivieren Sie entweder die Schlüssel Schutzvorrichtungen mithilfe der <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>disablekeyprotector</strong></a> -Methode, oder verwenden Sie eine der folgenden Methoden, um Schlüssel Schutzvorrichtungen für das Volume anzugeben:</span><span class="sxs-lookup"><span data-stu-id="38d78-167">Either disable key protectors by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method, or use one of the following methods to specify key protectors for the volume:</span></span>
<ul>
<li><span data-ttu-id="38d78-168"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>Protectkeywithexternalkey</strong></a></span><span class="sxs-lookup"><span data-stu-id="38d78-168"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="38d78-169"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>Protectkeywithnumericalpassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="38d78-169"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="38d78-170"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>Protectkeywithtpm</strong></a></span><span class="sxs-lookup"><span data-stu-id="38d78-170"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="38d78-171"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpin</strong></a></span><span class="sxs-lookup"><span data-stu-id="38d78-171"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="38d78-172"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpinandstartupkey</strong></a></span><span class="sxs-lookup"><span data-stu-id="38d78-172"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="38d78-173"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandstartupkey</strong></a></span><span class="sxs-lookup"><span data-stu-id="38d78-173"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="38d78-174"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span><span class="sxs-lookup"><span data-stu-id="38d78-174"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span></span></dl></td>
<td><span data-ttu-id="38d78-175">Das Volume kann nicht verschlüsselt werden, da dieser Computer als Teil eines Server Clusters konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="38d78-175">The volume cannot be encrypted because this computer is configured to be part of a server cluster.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="38d78-176"><dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003b)</dt> </span><span class="sxs-lookup"><span data-stu-id="38d78-176"><dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B)</dt> </span></span></dl></td>
<td><span data-ttu-id="38d78-177">Es wurden keine Schlüssel Schutzvorrichtungen für den Typ &quot; TPM &quot; , &quot; TPM und PIN &quot; , &quot; TPM und PIN sowie den Systemstart Schlüssel &quot; , das &quot; TPM und den Systemstart Schlüssel &quot; oder den &quot; externen Schlüssel &quot; gefunden.</span><span class="sxs-lookup"><span data-stu-id="38d78-177">No key protectors of the type &quot;TPM&quot;, &quot;TPM And PIN&quot;, &quot;TPM And PIN And Startup Key&quot;, &quot;TPM And Startup Key&quot;, or &quot;External Key&quot; can be found.</span></span> <span data-ttu-id="38d78-178">Der Hardware Test umfasst nur die vorherigen Schlüsselschutz Vorrichtungen.</span><span class="sxs-lookup"><span data-stu-id="38d78-178">The hardware test only involves the previous key protectors.</span></span><br/> <span data-ttu-id="38d78-179">Wenn Sie trotzdem einen Hardware Test ausführen möchten, müssen Sie eine der folgenden Methoden verwenden, um die Schlüssel Schutzvorrichtungen für das Volume anzugeben:</span><span class="sxs-lookup"><span data-stu-id="38d78-179">If you still want to run a hardware test, you must use one of the following methods to specify key protectors for the volume:</span></span>
<ul>
<li><span data-ttu-id="38d78-180"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>Protectkeywithexternalkey</strong></a></span><span class="sxs-lookup"><span data-stu-id="38d78-180"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="38d78-181"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>Protectkeywithnumericalpassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="38d78-181"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="38d78-182"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>Protectkeywithtpm</strong></a></span><span class="sxs-lookup"><span data-stu-id="38d78-182"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="38d78-183"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpin</strong></a></span><span class="sxs-lookup"><span data-stu-id="38d78-183"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="38d78-184"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpinandstartupkey</strong></a></span><span class="sxs-lookup"><span data-stu-id="38d78-184"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="38d78-185"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandstartupkey</strong></a></span><span class="sxs-lookup"><span data-stu-id="38d78-185"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="38d78-186"><dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </span><span class="sxs-lookup"><span data-stu-id="38d78-186"><dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </span></span></dl></td>
<td><span data-ttu-id="38d78-187">Das Volume ist teilweise oder vollständig verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="38d78-187">The volume is partially or fully encrypted.</span></span><br/> <span data-ttu-id="38d78-188">Der Hardware Test wird angewendet, bevor die Verschlüsselung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="38d78-188">The hardware test applies before encryption occurs.</span></span> <span data-ttu-id="38d78-189">Wenn Sie den Test trotzdem ausführen möchten, verwenden Sie zunächst die <a href="decrypt-win32-encryptablevolume.md"><strong>Entschlüsselungsmethode</strong></a> , und verwenden Sie dann eine der folgenden Methoden, um Schlüssel Schutzvorrichtungen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="38d78-189">If you still want to run the test, first use the <a href="decrypt-win32-encryptablevolume.md"><strong>Decrypt</strong></a> method and then use one of the following methods to add key protectors:</span></span>
<ul>
<li><span data-ttu-id="38d78-190"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>Protectkeywithexternalkey</strong></a></span><span class="sxs-lookup"><span data-stu-id="38d78-190"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="38d78-191"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>Protectkeywithnumericalpassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="38d78-191"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="38d78-192"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>Protectkeywithtpm</strong></a></span><span class="sxs-lookup"><span data-stu-id="38d78-192"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="38d78-193"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpin</strong></a></span><span class="sxs-lookup"><span data-stu-id="38d78-193"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="38d78-194"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandstartupkey</strong></a></span><span class="sxs-lookup"><span data-stu-id="38d78-194"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="38d78-195"><dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </span><span class="sxs-lookup"><span data-stu-id="38d78-195"><dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </span></span></dl></td>
<td><span data-ttu-id="38d78-196">Das Volume ist ein Datenvolumen.</span><span class="sxs-lookup"><span data-stu-id="38d78-196">The volume is a data volume.</span></span><br/> <span data-ttu-id="38d78-197">Der Hardware Test gilt nur für Volumes, die das Betriebssystem starten können.</span><span class="sxs-lookup"><span data-stu-id="38d78-197">The hardware test applies only to volumes that can start the operating system.</span></span> <span data-ttu-id="38d78-198">Führen Sie diese Methode auf dem aktuell gestarteten Betriebssystem Volume aus.</span><span class="sxs-lookup"><span data-stu-id="38d78-198">Run this method on the currently started operating system volume.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="38d78-199"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002c)</dt> </span><span class="sxs-lookup"><span data-stu-id="38d78-199"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span></span></dl></td>
<td><span data-ttu-id="38d78-200">Es wurden keine Schlüssel Schutzvorrichtungen des &quot; typnumerischen Kennworts &quot; angegeben.</span><span class="sxs-lookup"><span data-stu-id="38d78-200">No key protectors of the type &quot;Numerical Password&quot; are specified.</span></span> <span data-ttu-id="38d78-201">Für den Gruppenrichtlinie ist eine Sicherung der Wiederherstellungs Informationen erforderlich, um Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="38d78-201">The Group Policy requires a backup of recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="38d78-202">Um mindestens eine Schlüssel Schutzvorrichtung dieses Typs hinzuzufügen, verwenden Sie die <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>protectkeywithnumericalpassword</strong></a> -Methode.</span><span class="sxs-lookup"><span data-stu-id="38d78-202">To add at least one key protector of that type, use the <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> method.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="38d78-203">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38d78-203">Remarks</span></span>

<span data-ttu-id="38d78-204">Wenn Sie diese Methode ohne den zweiten optionalen Parameter verwenden (gemäß der Definition von Windows 7 und Windows Vista Enterprise), initiiert die Methode immer die Konvertierung im vollständigen Modus, um das abwärts kompatible Verhalten beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="38d78-204">When you use this method without the second optional parameter (according to the Windows 7 and Windows Vista Enterprise definition), the method will always initiate full mode conversion in order to keep backward compatible behavior.</span></span> <span data-ttu-id="38d78-205">Auf diese Weise wird die Sicherheits Erwartung vorhandener Anwendungen und Skripts nicht durch das Hinzufügen des zweiten optionalen Parameters in Windows 8 und Windows Server 2012 beschädigt.</span><span class="sxs-lookup"><span data-stu-id="38d78-205">This way the security expectation of existing applications and scripts will not be broken with the addition of the second optional parameter in Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="38d78-206">Anders als bei der [**Verschlüsselungs**](encrypt-win32-encryptablevolume.md) Methode führt diese Methode Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="38d78-206">Unlike the [**Encrypt**](encrypt-win32-encryptablevolume.md) method, this method does the following:</span></span>

-   <span data-ttu-id="38d78-207">Testet, ob das TPM das Volume entsperren kann, wenn eine TPM-bezogene Schlüssel Schutzvorrichtung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="38d78-207">Tests whether the TPM will be able to unlock the volume, if a TPM-related key protector exists.</span></span>
-   <span data-ttu-id="38d78-208">Testet, ob der Computer einen USB-Speicherstick lesen kann, der eine externe Schlüsseldatei während des Starts enthält, wenn das Volume durch einen externen Schlüssel (einschließlich eines Systemstart Schlüssels) entsperrt wird.</span><span class="sxs-lookup"><span data-stu-id="38d78-208">Tests whether the computer can read a USB flash drive that contains an external key file during start, if the volume will be unlocked by an external key (including a startup key).</span></span>
-   <span data-ttu-id="38d78-209">Erfordert einen Computer Neustart, um den Hardware Test auszuführen.</span><span class="sxs-lookup"><span data-stu-id="38d78-209">Requires a computer restart to run the hardware test.</span></span>
-   <span data-ttu-id="38d78-210">Startet die Verschlüsselung nur dann, wenn der Hardware Test erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="38d78-210">Begins encryption only if the hardware test succeeds.</span></span>
-   <span data-ttu-id="38d78-211">Kann nicht auf einem Daten Volume, auf einem teilweise oder vollständig verschlüsselten Volume oder zum Fortsetzen der Verschlüsselung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38d78-211">Cannot be used on a data volume, on a partially or fully encrypted volume, or to resume encryption.</span></span>

<span data-ttu-id="38d78-212">Verwenden Sie vor dem Ausführen dieser Methode die folgenden Methoden, um die zugehörigen Schlüsselschutz Vorrichtungen zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="38d78-212">Before running this method, use the following methods to create the related key protectors:</span></span>

-   [<span data-ttu-id="38d78-213">**Protectkeywithexternalkey**</span><span class="sxs-lookup"><span data-stu-id="38d78-213">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="38d78-214">**Protectkeywithtpm**</span><span class="sxs-lookup"><span data-stu-id="38d78-214">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
-   [<span data-ttu-id="38d78-215">**Protectkeywithtpmandpin**</span><span class="sxs-lookup"><span data-stu-id="38d78-215">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [<span data-ttu-id="38d78-216">**Protectkeywithtpmandpinandstartupkey**</span><span class="sxs-lookup"><span data-stu-id="38d78-216">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="38d78-217">**Protectkeywithtpmandstartupkey**</span><span class="sxs-lookup"><span data-stu-id="38d78-217">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

<span data-ttu-id="38d78-218">Führen Sie nach dem Ausführen dieser Methode die folgenden zusätzlichen Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="38d78-218">After running this method, take these additional steps:</span></span>

1.  <span data-ttu-id="38d78-219">Fügen Sie einen USB-Speicherstick, der eine externe Schlüsseldatei enthält, in den Computer ein.</span><span class="sxs-lookup"><span data-stu-id="38d78-219">Insert into the computer a USB flash drive that contains an external key file.</span></span> <span data-ttu-id="38d78-220">Dieser Schritt gilt nur, wenn das Volume über eine Schlüssel Schutzvorrichtung vom Typ "externer Schlüssel" oder "TPM und Systemstart Schlüssel" verfügt.</span><span class="sxs-lookup"><span data-stu-id="38d78-220">This step applies only if the volume has a key protector of type "External Key" or "TPM And Startup Key".</span></span>
2.  <span data-ttu-id="38d78-221">Starten Sie den Computer neu.</span><span class="sxs-lookup"><span data-stu-id="38d78-221">Restart the computer.</span></span>

<span data-ttu-id="38d78-222">Beim Neustart des Computers wird der Hardware Test automatisch ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38d78-222">On computer restart, the hardware test runs automatically.</span></span>

<span data-ttu-id="38d78-223">Die Verschlüsselung beginnt, wenn der Hardware Test erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="38d78-223">Encryption begins if the hardware test succeeds.</span></span> <span data-ttu-id="38d78-224">Versuchen Sie andernfalls, Hardwarefehler zu beheben.</span><span class="sxs-lookup"><span data-stu-id="38d78-224">Otherwise, attempt to resolve any hardware failures.</span></span> <span data-ttu-id="38d78-225">Führen Sie [**gethardwareteststatus**](gethardwareteststatus-win32-encryptablevolume.md) nach dem Neustart des Computers aus, um die Testergebnisse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="38d78-225">Run [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md) after restarting the computer to get test results.</span></span>

<span data-ttu-id="38d78-226">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="38d78-226">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="38d78-227">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="38d78-227">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="38d78-228">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="38d78-228">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="38d78-229">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="38d78-229">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38d78-230">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38d78-230">Requirements</span></span>



| <span data-ttu-id="38d78-231">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38d78-231">Requirement</span></span> | <span data-ttu-id="38d78-232">Wert</span><span class="sxs-lookup"><span data-stu-id="38d78-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38d78-233">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="38d78-233">Minimum supported client</span></span><br/> | <span data-ttu-id="38d78-234">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38d78-234">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="38d78-235">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="38d78-235">Minimum supported server</span></span><br/> | <span data-ttu-id="38d78-236">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38d78-236">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="38d78-237">Namespace</span><span class="sxs-lookup"><span data-stu-id="38d78-237">Namespace</span></span><br/>                | <span data-ttu-id="38d78-238">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="38d78-238">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="38d78-239">MOF</span><span class="sxs-lookup"><span data-stu-id="38d78-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38d78-240"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="38d78-240"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38d78-241">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38d78-241">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38d78-242">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="38d78-242">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
