---
description: Gibt den Status der Verschlüsselung oder Entschlüsselung auf dem Volume an.
ms.assetid: b292a380-1b4a-4dff-948b-6494ec3b400b
title: Getkonversionstatus-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetConversionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 9357db3397b04639329c1afd502d9da30cbb39be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862291"
---
# <a name="getconversionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="82011-103">Getkonversionstatus-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="82011-103">GetConversionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="82011-104">Die **getkonversionstatus** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt den Status der Verschlüsselung oder Entschlüsselung auf dem Volume an.</span><span class="sxs-lookup"><span data-stu-id="82011-104">The **GetConversionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the status of the encryption or decryption on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="82011-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="82011-105">Syntax</span></span>


```mof
uint32 GetConversionStatus(
  [out] uint32 ConversionStatus,
  [out] uint32 EncryptionPercentage,
  [out] uint32 EncryptionFlags,
  [out] uint32 WipingStatus,
  [out] uint32 WipingPercentage,
  [in]  uint32 PrecisionFactor
);
```



## <a name="parameters"></a><span data-ttu-id="82011-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="82011-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82011-107">Configuration Manager- *Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="82011-107">*ConversionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82011-108">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82011-108">Type: **uint32**</span></span>

<span data-ttu-id="82011-109">Volumeverschlüsselungs-oder Entschlüsselungs Status.</span><span class="sxs-lookup"><span data-stu-id="82011-109">Volume encryption or decryption status.</span></span> <span data-ttu-id="82011-110">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="82011-110">This can be one of the following values.</span></span>



| <span data-ttu-id="82011-111">Wert</span><span class="sxs-lookup"><span data-stu-id="82011-111">Value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="82011-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="82011-112">Meaning</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FullyDecrypted"></span><span id="fullydecrypted"></span><span id="FULLYDECRYPTED"></span><dl> <span data-ttu-id="82011-113"><dt>**Fullydecrypted**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="82011-113"><dt>**FullyDecrypted**</dt> <dt>0</dt></span></span> </dl>                         | <span data-ttu-id="82011-114">Bei einer Standard Festplatte (HDD) wird das Volume vollständig entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="82011-114">For a standard hard drive (HDD), the volume is fully decrypted.</span></span><br/> <span data-ttu-id="82011-115">Für eine Hardware verschlüsselte Festplatte (ehdd) wird das Volume dauerhaft entsperrt.</span><span class="sxs-lookup"><span data-stu-id="82011-115">For a hardware encrypted hard drive (EHDD), the volume is perpetually unlocked.</span></span><br/>     |
| <span id="FullyEncrypted"></span><span id="fullyencrypted"></span><span id="FULLYENCRYPTED"></span><dl> <span data-ttu-id="82011-116"><dt>**Fullyverschlüsselt**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="82011-116"><dt>**FullyEncrypted**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="82011-117">Für eine Standard Festplatte (HDD) ist das Volume vollständig verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="82011-117">For a standard hard drive (HDD), the volume is fully encrypted.</span></span><br/> <span data-ttu-id="82011-118">Für eine Hardware verschlüsselte Festplatte (ehdd) wird das Volume nicht dauerhaft entsperrt.</span><span class="sxs-lookup"><span data-stu-id="82011-118">For a hardware encrypted hard drive (EHDD), the volume is not perpetually unlocked.</span></span><br/> |
| <span id="EncryptionInProgress"></span><span id="encryptioninprogress"></span><span id="ENCRYPTIONINPROGRESS"></span><dl> <span data-ttu-id="82011-119"><dt>**Verschlüsselungsinprogress**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="82011-119"><dt>**EncryptionInProgress**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="82011-120">Das Volume ist teilweise verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="82011-120">The volume is partially encrypted.</span></span><br/>                                                                                                                             |
| <span id="DecryptionInProgress"></span><span id="decryptioninprogress"></span><span id="DECRYPTIONINPROGRESS"></span><dl> <span data-ttu-id="82011-121"><dt>**Decryptioninprogress**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="82011-121"><dt>**DecryptionInProgress**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="82011-122">Das Volume ist teilweise verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="82011-122">The volume is partially encrypted.</span></span><br/>                                                                                                                             |
| <span id="EncryptionPaused"></span><span id="encryptionpaused"></span><span id="ENCRYPTIONPAUSED"></span><dl> <span data-ttu-id="82011-123"><dt>**Verschlüsselter angehaltene**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="82011-123"><dt>**EncryptionPaused**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="82011-124">Das Volume wurde während des Verschlüsselungs Fortschritts angehalten.</span><span class="sxs-lookup"><span data-stu-id="82011-124">The volume has been paused during the encryption progress.</span></span> <span data-ttu-id="82011-125">Das Volume ist teilweise verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="82011-125">The volume is partially encrypted.</span></span><br/>                                                                  |
| <span id="DecryptionPaused"></span><span id="decryptionpaused"></span><span id="DECRYPTIONPAUSED"></span><dl> <span data-ttu-id="82011-126"><dt>**Entschlüsselte**</dt> Ausführung <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="82011-126"><dt>**DecryptionPaused**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="82011-127">Das Volume wurde während des Entschlüsselungs Fortschritts angehalten.</span><span class="sxs-lookup"><span data-stu-id="82011-127">The volume has been paused during the decryption progress.</span></span> <span data-ttu-id="82011-128">Das Volume ist teilweise verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="82011-128">The volume is partially encrypted.</span></span><br/>                                                                  |



 

</dd> <dt>

<span data-ttu-id="82011-129">*Verschlüsselungs Prozentsatz* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="82011-129">*EncryptionPercentage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82011-130">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82011-130">Type: **uint32**</span></span>

<span data-ttu-id="82011-131">Prozentsatz des verschlüsselten Volumes.</span><span class="sxs-lookup"><span data-stu-id="82011-131">Percentage of the volume that is encrypted.</span></span> <span data-ttu-id="82011-132">Dies ist eine ganze Zahl zwischen 0 und 100 einschließlich.</span><span class="sxs-lookup"><span data-stu-id="82011-132">This is an integer from 0 to 100 inclusive.</span></span>

<span data-ttu-id="82011-133">Aufgrund der Rundung von Zahlen weist der Verschlüsselungs Prozentsatz 0 oder 100 nicht notwendigerweise darauf hin, dass der Datenträger vollständig entschlüsselt oder vollständig verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="82011-133">Due to rounding of numbers, an encryption percentage of 0 or 100 does not necessarily indicate that the disk is fully decrypted or fully encrypted.</span></span> <span data-ttu-id="82011-134">Verwenden Sie immer "Configuration Manager *Status* ", um zu bestimmen, ob der Datenträger tatsächlich vollständig entschlüsselt oder vollständig verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="82011-134">Always use *ConversionStatus* to determine whether the disk is in fact fully decrypted or fully encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="82011-135">*Verschlüsselungsflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="82011-135">*EncryptionFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82011-136">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82011-136">Type: **uint32**</span></span>

<span data-ttu-id="82011-137">Flags, die das Verschlüsselungs Verhalten beschreiben.</span><span class="sxs-lookup"><span data-stu-id="82011-137">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="82011-138">Eine Kombination von 32 Bits mit folgenden Bits, die aktuell definiert sind.</span><span class="sxs-lookup"><span data-stu-id="82011-138">A combination of 32 bits with following bits currently defined.</span></span>



| <span data-ttu-id="82011-139">Wert</span><span class="sxs-lookup"><span data-stu-id="82011-139">Value</span></span>                                                                                  | <span data-ttu-id="82011-140">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="82011-140">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="82011-141"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="82011-141"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="82011-142">Führen Sie die Volumeverschlüsselung im reinen Daten Verschlüsselungs Modus aus, wenn Sie den neuen Verschlüsselungsprozess starten.</span><span class="sxs-lookup"><span data-stu-id="82011-142">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="82011-143">Wenn die Verschlüsselung angehalten oder beendet wurde, wird die Konvertierung durch Aufrufen der Methode " [**verschlüsseln**](encrypt-win32-encryptablevolume.md) " wirksam fortgesetzt, und der Wert dieses Bits wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="82011-143">If encryption has been paused or stopped, calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="82011-144">Dieses Bit ist nur wirksam, wenn die Verschlüsselungs-oder [**verschlüsseltafterhardwaretest**](encryptafterhardwaretest-win32-encryptablevolume.md) - **Methoden die Verschlüsselung** aus dem vollständig entschlüsselten Zustand, dem Entschlüsselungs Status oder dem Status der entschlüsselten Entschlüsselung starten.</span><span class="sxs-lookup"><span data-stu-id="82011-144">This bit only has effect when either the **Encrypt** or [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="82011-145">Wenn dieses Bit 0 (null) ist, was bedeutet, dass es beim Starten des neuen Verschlüsselungs Vorgangs nicht festgelegt ist, wird die vollständige Modus-Konvertierung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82011-145">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="82011-146"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="82011-146"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="82011-147">Ausführen einer bedarfsgesteuerten Löschung des freien Speicherplatzes auf dem Volume.</span><span class="sxs-lookup"><span data-stu-id="82011-147">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="82011-148">Das Aufrufen der [**Verschlüsselungs**](encrypt-win32-encryptablevolume.md) Methode mit diesem Bitset ist nur zulässig, wenn das Volume derzeit nicht in den Status "verschlüsselt" versetzt wird und sich im Status "verschlüsselt" befindet.</span><span class="sxs-lookup"><span data-stu-id="82011-148">Calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="82011-149"><dt>0x00010000 bis </dt></span><span class="sxs-lookup"><span data-stu-id="82011-149"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="82011-150">Führt den angeforderten Vorgang synchron aus.</span><span class="sxs-lookup"><span data-stu-id="82011-150">Perform the requested operation synchronously.</span></span> <span data-ttu-id="82011-151">Der-Befehl wird blockiert, bis der angeforderte Vorgang abgeschlossen ist oder unterbrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="82011-151">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="82011-152">Dieses Flag wird nur mit der Methode " [**verschlüsseln**](encrypt-win32-encryptablevolume.md) " unterstützt.</span><span class="sxs-lookup"><span data-stu-id="82011-152">This flag is only supported with the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="82011-153">Dieses Flag kann angegeben werden, wenn " **verschlüsseln** " aufgerufen wird, um die beendete oder unterbrochene Verschlüsselung oder das Zurücksetzen oder Löschen von Verschlüsselung oder Zurücksetzen zu beenden.</span><span class="sxs-lookup"><span data-stu-id="82011-153">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="82011-154">Dies ermöglicht dem Aufrufer, synchron zu warten, bis der Prozess abgeschlossen oder unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="82011-154">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="82011-155">*Wipingstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="82011-155">*WipingStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82011-156">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82011-156">Type: **uint32**</span></span>

<span data-ttu-id="82011-157">Status der Freigabe für freien Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="82011-157">Free space wiping status.</span></span> <span data-ttu-id="82011-158">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="82011-158">This can be one of the following values.</span></span>



| <span data-ttu-id="82011-159">Wert</span><span class="sxs-lookup"><span data-stu-id="82011-159">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="82011-160">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="82011-160">Meaning</span></span>                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="FreeSpaceNotWiped"></span><span id="freespacenotwiped"></span><span id="FREESPACENOTWIPED"></span><dl> <span data-ttu-id="82011-161"><dt>**Freespacenotgelöschte**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="82011-161"><dt>**FreeSpaceNotWiped**</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="82011-162">Der freie Speicherplatz wurde nicht zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="82011-162">The free space has not been wiped.</span></span><br/>          |
| <span id="FreeSpaceWiped"></span><span id="freespacewiped"></span><span id="FREESPACEWIPED"></span><dl> <span data-ttu-id="82011-163"><dt>**Freespacewipt**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="82011-163"><dt>**FreeSpaceWiped**</dt> <dt>1</dt></span></span> </dl>                                             | <span data-ttu-id="82011-164">Der freie Speicherplatz wurde zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="82011-164">The free space has been wiped.</span></span><br/>              |
| <span id="FreeSpaceWipingInProgress"></span><span id="freespacewipinginprogress"></span><span id="FREESPACEWIPINGINPROGRESS"></span><dl> <span data-ttu-id="82011-165"><dt>**Freespacewipinginprogress**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="82011-165"><dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="82011-166">Der freie Speicherplatz wird zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82011-166">Free space wiping is currently in progress.</span></span><br/> |
| <span id="FreeSpaceWipingPaused"></span><span id="freespacewipingpaused"></span><span id="FREESPACEWIPINGPAUSED"></span><dl> <span data-ttu-id="82011-167"><dt>**Freespacewipingangeh**</dt> alten <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="82011-167"><dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt></span></span> </dl>                 | <span data-ttu-id="82011-168">Der freie Speicherplatz wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="82011-168">Free space wiping has been paused.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="82011-169">*Wipingprozentsatz* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="82011-169">*WipingPercentage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82011-170">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82011-170">Type: **uint32**</span></span>

<span data-ttu-id="82011-171">Ein Wert zwischen 0 und 100, der den Prozentsatz des freien Speicherplatzes angibt, der zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="82011-171">A value from 0 to 100 that specifies the percentage of free space that has been wiped.</span></span>

</dd> <dt>

<span data-ttu-id="82011-172">*Precisionfactor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82011-172">*PrecisionFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82011-173">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82011-173">Type: **uint32**</span></span>

<span data-ttu-id="82011-174">Ein Wert zwischen 0 und 4, der die Genauigkeits Ebene angibt.</span><span class="sxs-lookup"><span data-stu-id="82011-174">A value from 0 to 4 that specifies the precision level</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82011-175">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82011-175">Return value</span></span>

<span data-ttu-id="82011-176">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82011-176">Type: **uint32**</span></span>

<span data-ttu-id="82011-177">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="82011-177">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="82011-178">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="82011-178">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="82011-179">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82011-179">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="82011-180"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="82011-180"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="82011-181">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="82011-181">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="82011-182"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="82011-182"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="82011-183">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="82011-183">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="82011-184">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82011-184">Remarks</span></span>

<span data-ttu-id="82011-185">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="82011-185">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="82011-186">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="82011-186">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="82011-187">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="82011-187">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="82011-188">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="82011-188">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="82011-189">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82011-189">Requirements</span></span>



| <span data-ttu-id="82011-190">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82011-190">Requirement</span></span> | <span data-ttu-id="82011-191">Wert</span><span class="sxs-lookup"><span data-stu-id="82011-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82011-192">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82011-192">Minimum supported client</span></span><br/> | <span data-ttu-id="82011-193">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82011-193">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="82011-194">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82011-194">Minimum supported server</span></span><br/> | <span data-ttu-id="82011-195">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82011-195">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82011-196">Namespace</span><span class="sxs-lookup"><span data-stu-id="82011-196">Namespace</span></span><br/>                | <span data-ttu-id="82011-197">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="82011-197">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="82011-198">MOF</span><span class="sxs-lookup"><span data-stu-id="82011-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82011-199"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="82011-199"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82011-200">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82011-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82011-201">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="82011-201">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
