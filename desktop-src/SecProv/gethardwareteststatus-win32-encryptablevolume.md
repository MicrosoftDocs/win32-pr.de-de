---
description: Stellt Statusinformationen zu einem Hardware Test eines vollständig entschlüsselten Betriebssystem Volumes bereit.
ms.assetid: d76bc266-3718-443e-94f9-dcaa0ec53151
title: Gethardwareteststatus-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareTestStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 26d1984a79edef5f00f7687260fda7b211153863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350810"
---
# <a name="gethardwareteststatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="5d1f3-103">Gethardwareteststatus-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="5d1f3-103">GetHardwareTestStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="5d1f3-104">Die **gethardwareteststatus** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " stellt Statusinformationen über einen Hardware Test eines vollständig entschlüsselten Betriebssystem Volumes bereit.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-104">The **GetHardwareTestStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class provides status information about a hardware test of a fully decrypted operating system volume.</span></span>

<span data-ttu-id="5d1f3-105">Verwenden Sie diese Methode, um anzuzeigen, ob ein Hardware Test aussteht, sowie den Erfolg oder Misserfolg eines Hardware Tests, der beim letzten Neustart des Computers abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-105">Use this method to show whether a hardware test is pending, as well as the success or failure of a hardware test that completed on the last computer restart.</span></span> <span data-ttu-id="5d1f3-106">Verwenden Sie die Methode " [**verschlüsseltafterhardwaretest**](encryptafterhardwaretest-win32-encryptablevolume.md) ", um einen Hardware Test anzufordern.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-106">To request a hardware test, use the [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d1f3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d1f3-107">Syntax</span></span>


```mof
uint32 GetHardwareTestStatus(
  [out] uint32 TestStatus,
  [out] uint32 TestError
);
```



## <a name="parameters"></a><span data-ttu-id="5d1f3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d1f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d1f3-109">*Teststatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5d1f3-109">*TestStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d1f3-110">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5d1f3-110">Type: **uint32**</span></span>

<span data-ttu-id="5d1f3-111">Gibt an, ob ein Hardware Test aussteht, sowie den Erfolg eines Fehlers eines Hardware Tests, der beim letzten Neustart des Computers abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-111">Specifies whether a hardware test is pending, as well as the success of failure of a hardware test that completed on the last computer restart.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5d1f3-112">Wert</span><span class="sxs-lookup"><span data-stu-id="5d1f3-112">Value</span></span></th>
<th><span data-ttu-id="5d1f3-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5d1f3-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="NotFailed_and_NonePending"></span><span id="notfailed_and_nonepending"></span><span id="NOTFAILED_AND_NONEPENDING"></span><dl> <span data-ttu-id="5d1f3-114"><dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="5d1f3-114"><dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="5d1f3-115">Wenn ein Test angefordert wurde, war der Test beim letzten Neustart des Computers erfolgreich, und die Volumeverschlüsselung wird jetzt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-115">If a test was requested, the test has succeeded on the last computer restart and volume encryption is now in progress.</span></span> <span data-ttu-id="5d1f3-116">Den Verschlüsselungs Status finden Sie unter der <a href="getconversionstatus-win32-encryptablevolume.md"><strong>getkonversionstatus</strong></a> -Methode.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-116">For the encryption status, see the <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus</strong></a> method.</span></span> <span data-ttu-id="5d1f3-117">Andernfalls wurde kein Test auf dem letzten Computer Neustart ausgeführt, und es ist kein ausstehend.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-117">Otherwise, no test ran on the last computer restart and none is pending.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="Failed"></span><span id="failed"></span><span id="FAILED"></span><dl> <span data-ttu-id="5d1f3-118"><dt><strong></strong></dt> Fehler <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="5d1f3-118"><dt><strong>Failed</strong></dt> <dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="5d1f3-119">Die Volumeverschlüsselung konnte nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-119">Volume encryption did not start.</span></span> <span data-ttu-id="5d1f3-120">Alle Schlüssel Schutzvorrichtungen wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-120">All key protectors were removed.</span></span><br/> <span data-ttu-id="5d1f3-121">So beheben Sie einen fehlgeschlagenen Test:</span><span class="sxs-lookup"><span data-stu-id="5d1f3-121">To resolve a failed test:</span></span><br/>
<ul>
<li><span data-ttu-id="5d1f3-122">Überprüfen Sie die Informationen im <em>testerror</em> -Parameter.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-122">Consult the information in the <em>TestError</em> parameter.</span></span></li>
<li><span data-ttu-id="5d1f3-123">Fügen Sie Schlüssel Schutzvorrichtungen hinzu, und verwenden Sie die Methode " <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>verschlüsseltafterhardwaretest</strong></a> " erneut.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-123">Add key protectors and use the <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest</strong></a> method again.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="Pending"></span><span id="pending"></span><span id="PENDING"></span><dl> <span data-ttu-id="5d1f3-124"><dt><strong>Ausstehende</strong></dt> <dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="5d1f3-124"><dt><strong>Pending</strong></dt> <dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="5d1f3-125">Ein Test wurde angefordert und wird beim nächsten Neustart des Computers ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-125">A test has been requested and will run on the next computer restart.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="5d1f3-126">" *Testerror* \[ " vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5d1f3-126">*TestError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d1f3-127">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5d1f3-127">Type: **uint32**</span></span>

<span data-ttu-id="5d1f3-128">Gibt den Fehler des letzten abgeschlossenen Hardware Tests an.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-128">Specifies the error from the last completed hardware test.</span></span>



| <span data-ttu-id="5d1f3-129">Wert</span><span class="sxs-lookup"><span data-stu-id="5d1f3-129">Value</span></span>                                                                                               | <span data-ttu-id="5d1f3-130">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5d1f3-130">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d1f3-131"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5d1f3-131"><dt>0</dt></span></span> </dl>                        | <span data-ttu-id="5d1f3-132">Es sind keine Fehler aufgetreten, oder es wurde kein Hardware Test auf dem letzten Neustart des Computers ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-132">No errors occurred or no hardware test ran on the last computer restart.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="5d1f3-133"><dt> 2150694972 (0x8031003c)</dt></span><span class="sxs-lookup"><span data-stu-id="5d1f3-133"><dt> 2150694972 (0x8031003C)</dt></span></span> </dl> | <span data-ttu-id="5d1f3-134">f- \_ E- \_ KeyFile \_ nicht \_ gefunden</span><span class="sxs-lookup"><span data-stu-id="5d1f3-134">FVE\_E\_KEYFILE\_NOT\_FOUND</span></span><br/> <span data-ttu-id="5d1f3-135">Ein USB-Speicherstick mit einer externen Schlüsseldatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-135">A USB flash drive with an external key file was not found.</span></span> <span data-ttu-id="5d1f3-136">Wenn dieser Fehler weiterhin auftritt, kann der Computer während des Neustarts keine USB-Laufwerke lesen.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-136">If this failure persists, the computer cannot read USB drives during restart.</span></span> <span data-ttu-id="5d1f3-137">Möglicherweise können Sie externe Schlüssel nicht verwenden, um das Betriebssystem Volume während des Neustarts zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-137">You may not be able to use external keys to unlock the operating system volume during restart.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="5d1f3-138"><dt> 2150694973 (0x8031003d)</dt></span><span class="sxs-lookup"><span data-stu-id="5d1f3-138"><dt> 2150694973 (0x8031003D)</dt></span></span> </dl> | <span data-ttu-id="5d1f3-139">\_ \_ ungültige E-Key-Datei \_</span><span class="sxs-lookup"><span data-stu-id="5d1f3-139">FVE\_E\_KEYFILE\_INVALID</span></span><br/> <span data-ttu-id="5d1f3-140">Die externe Schlüsseldatei auf dem USB-Speicherstick war beschädigt.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-140">The external key file on the USB flash drive was corrupt.</span></span> <span data-ttu-id="5d1f3-141">Probieren Sie einen anderen USB-Speicherstick zum Speichern der externen Schlüsseldatei aus.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-141">Try a different USB flash drive to store the external key file.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="5d1f3-142"><dt> 2150694975 (0x8031003f)</dt></span><span class="sxs-lookup"><span data-stu-id="5d1f3-142"><dt> 2150694975 (0x8031003F)</dt></span></span> </dl> | <span data-ttu-id="5d1f3-143">\_E \_ TPM \_ deaktiviert</span><span class="sxs-lookup"><span data-stu-id="5d1f3-143">FVE\_E\_TPM\_DISABLED</span></span><br/> <span data-ttu-id="5d1f3-144">Das TPM ist entweder deaktiviert oder deaktiviert oder deaktiviert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-144">The TPM is either disabled or deactivated or both disabled and deactivated.</span></span> <span data-ttu-id="5d1f3-145">Um das TPM zu aktivieren, verwenden Sie den [**Win32- \_ TPM**](win32-tpm.md) -WMI-Anbieter, oder führen Sie das TPM-Verwaltungs-Snap-in (TPM. msc) aus.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-145">To turn on the TPM, use the [**Win32\_Tpm**](win32-tpm.md) WMI provider or run the TPM management snap-in (Tpm.msc).</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="5d1f3-146"><dt> 2150694977 (0x80310041)</dt></span><span class="sxs-lookup"><span data-stu-id="5d1f3-146"><dt> 2150694977 (0x80310041)</dt></span></span> </dl> | <span data-ttu-id="5d1f3-147">\_ \_ ungültige E TPM-Datei \_ \_</span><span class="sxs-lookup"><span data-stu-id="5d1f3-147">FVE\_E\_TPM\_INVALID\_PCR</span></span><br/> <span data-ttu-id="5d1f3-148">Das TPM hat eine Änderung der Neustart Dienste des Betriebssystems im aktuellen Platt Form Validierungs Profil festgestellt.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-148">The TPM detected a change in operating system restart services within the current platform validation profile.</span></span> <span data-ttu-id="5d1f3-149">Entfernen Sie eine beliebige Start-CD oder DVD vom Computer.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-149">Remove any startup CD or DVD from the computer.</span></span> <span data-ttu-id="5d1f3-150">Wenn dieser Fehler weiterhin auftritt, überprüfen Sie, ob die neuesten Firmware-und BIOS-Upgrades installiert sind und ob das TPM andernfalls ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-150">If this failure persists, check that the latest firmware and BIOS upgrades are installed, and that the TPM is otherwise working properly.</span></span><br/> |
| <dl> <span data-ttu-id="5d1f3-151"><dt>2150694979 (0x80310043)</dt></span><span class="sxs-lookup"><span data-stu-id="5d1f3-151"><dt>2150694979 (0x80310043)</dt></span></span> </dl>  | <span data-ttu-id="5d1f3-152">\_ \_ ungültige E-Pin \_</span><span class="sxs-lookup"><span data-stu-id="5d1f3-152">FVE\_E\_PIN\_INVALID</span></span><br/> <span data-ttu-id="5d1f3-153">Die angegebene PIN war falsch.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-153">The provided PIN was incorrect.</span></span><br/>                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d1f3-154">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d1f3-154">Return value</span></span>

<span data-ttu-id="5d1f3-155">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5d1f3-155">Type: **uint32**</span></span>

<span data-ttu-id="5d1f3-156">In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-156">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="5d1f3-157">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="5d1f3-157">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="5d1f3-158">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d1f3-158">Description</span></span>                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5d1f3-159"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5d1f3-159"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="5d1f3-160">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-160">The method succeeded.</span></span><br/> |
| <dl> <span data-ttu-id="5d1f3-161"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="5d1f3-161"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="5d1f3-162">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-162">The volume is locked.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5d1f3-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d1f3-163">Remarks</span></span>

<span data-ttu-id="5d1f3-164">Verwenden Sie die Methode " [**verschlüsseltafterhardwaretest**](encryptafterhardwaretest-win32-encryptablevolume.md) ", um einen Hardware Test anzufordern.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-164">To request a hardware test, use the [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="5d1f3-165">Führen Sie die folgenden Schritte aus, um einen Hardware Test auszuführen, wenn der Status "Ausstehend" lautet:</span><span class="sxs-lookup"><span data-stu-id="5d1f3-165">To run a hardware test when its status is pending, follow these steps:</span></span>

1.  <span data-ttu-id="5d1f3-166">Fügen Sie einen USB-Speicherstick, der eine externe Schlüsseldatei enthält, in den Computer ein.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-166">Insert into the computer a USB flash drive that contains an external key file.</span></span> <span data-ttu-id="5d1f3-167">Dieser Schritt gilt nur, wenn das Volume über eine Schlüssel Schutzvorrichtung vom Typ "externer Schlüssel" oder "TPM und Systemstart Schlüssel" verfügt.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-167">This step applies only if the volume has a key protector of type "External Key" or "TPM And Startup Key".</span></span>
2.  <span data-ttu-id="5d1f3-168">Starten Sie den Computer neu.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-168">Restart the computer.</span></span> <span data-ttu-id="5d1f3-169">Beim Neustart des Computers wird der Hardware Test automatisch ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-169">On computer restart, the hardware test runs automatically.</span></span>

<span data-ttu-id="5d1f3-170">Verwenden Sie die Methode [**verschlüsseln**](encrypt-win32-encryptablevolume.md) , um den Hardware Test abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-170">To cancel the hardware test, use the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="5d1f3-171">Ein erfolgreicher Test bestimmt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5d1f3-171">A successful test determines that:</span></span>

-   <span data-ttu-id="5d1f3-172">Das TPM kann das Volume entsperren, wenn eine TPM-bezogene Schlüssel Schutzvorrichtung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-172">The TPM can unlock the volume if a TPM-related key protector exists.</span></span>
-   <span data-ttu-id="5d1f3-173">Der Computer kann einen USB-Speicherstick lesen, der eine externe Schlüsseldatei während des Starts enthält, wenn das Volume durch einen externen Schlüssel (einschließlich eines Systemstart Schlüssels) entsperrt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-173">The computer can read a USB flash drive that contains an external key file during startup if the volume can be unlocked by an external key (including a startup key).</span></span>

<span data-ttu-id="5d1f3-174">Die Hardware Testergebnisse sind nach Änderungen an der Konvertierung oder nach dem nächsten Computer Neustart nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-174">Hardware test results will not be available after any changes in conversion or after the next computer restart.</span></span> <span data-ttu-id="5d1f3-175">Überprüfen Sie das System Ereignisprotokoll auf die Informationen zu Hardware Tests, die zuvor auf dem Computer ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-175">Check the System event log for the information about any hardware tests that previously ran on the computer.</span></span>

<span data-ttu-id="5d1f3-176">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-176">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5d1f3-177">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-177">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5d1f3-178">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5d1f3-178">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5d1f3-179">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5d1f3-179">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d1f3-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d1f3-180">Requirements</span></span>



| <span data-ttu-id="5d1f3-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d1f3-181">Requirement</span></span> | <span data-ttu-id="5d1f3-182">Wert</span><span class="sxs-lookup"><span data-stu-id="5d1f3-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d1f3-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d1f3-183">Minimum supported client</span></span><br/> | <span data-ttu-id="5d1f3-184">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d1f3-184">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5d1f3-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d1f3-185">Minimum supported server</span></span><br/> | <span data-ttu-id="5d1f3-186">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d1f3-186">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5d1f3-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d1f3-187">Namespace</span></span><br/>                | <span data-ttu-id="5d1f3-188">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="5d1f3-188">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="5d1f3-189">MOF</span><span class="sxs-lookup"><span data-stu-id="5d1f3-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d1f3-190"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5d1f3-190"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d1f3-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d1f3-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d1f3-192">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="5d1f3-192">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
