---
description: Startet die Entschlüsselung eines vollständig verschlüsselten Volumes oder setzt das Entschlüsseln eines teilweise verschlüsselten Volumes fort.
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
title: Entschlüsselungsmethode der Win32_EncryptableVolume-Klasse (InfoCard. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Decrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 96f7ab1c237879d83be25ddb54425ac31fcb855d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865436"
---
# <a name="decrypt-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="a0ac1-103">Entschlüsselungsmethode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="a0ac1-103">Decrypt method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="a0ac1-104">Die **Entschlüsselungs** Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " beginnt mit der Entschlüsselung eines vollständig verschlüsselten Volumes oder nimmt das Entschlüsseln eines teilweise verschlüsselten Volumes wieder auf.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-104">The **Decrypt** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins decryption of a fully encrypted volume, or resumes decryption of a partially encrypted volume.</span></span>

<span data-ttu-id="a0ac1-105">Wenn die Entschlüsselung angehalten oder ausgeführt wird, verhält sich diese Methode genauso wie " [**resumeconversion**](resumeconversion-win32-encryptablevolume.md)".</span><span class="sxs-lookup"><span data-stu-id="a0ac1-105">When decryption is paused or in-progress, this method behaves the same as [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span></span> <span data-ttu-id="a0ac1-106">Wenn die Verschlüsselung angehalten oder in Bearbeitung ist, wird die Verschlüsselung von dieser Methode wieder hergestellt, und die Entschlüsselung wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-106">When encryption is paused or in-progress, this method reverts the encryption and begins decryption.</span></span> <span data-ttu-id="a0ac1-107">Nachdem die Entschlüsselung abgeschlossen ist, werden alle Schlüssel Schutzvorrichtungen auf diesem Volume aus dem System entfernt, und das Volume wird in ein Standardmäßiges NTFS-Dateisystem konvertiert.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-107">After decryption completes, all key protectors on this volume are removed from the system and the volume converts to a standard NTFS file system.</span></span>

> [!Note]  
> <span data-ttu-id="a0ac1-108">Wenn die Festplatte Hardware verschlüsselt ist, legt die **entschlüsselte** Methode den Bandstatus auf "immer entsperrt" fest, entfernt alle zugeordneten Metadaten und Nullen die Sicherheits-ID für das Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-108">If the disc is hardware encrypted, the **Decrypt** method sets band status to "always unlocked", removes all associated metadata, and zeroes the security ID for the drive.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a0ac1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0ac1-109">Syntax</span></span>


```mof
uint32 Decrypt();
```



## <a name="parameters"></a><span data-ttu-id="a0ac1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0ac1-110">Parameters</span></span>

<span data-ttu-id="a0ac1-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0ac1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0ac1-112">Return value</span></span>

<span data-ttu-id="a0ac1-113">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0ac1-113">Type: **uint32**</span></span>

<span data-ttu-id="a0ac1-114">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-114">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="a0ac1-115">Diese Methode wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-115">This method returns immediately.</span></span> <span data-ttu-id="a0ac1-116">Wenn das Volume bereits vollständig entschlüsselt wurde und keine anderen Fehler vorhanden sind, gibt diese Methode 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-116">If the volume is already fully decrypted and no other errors exist, this method returns 0.</span></span>



| <span data-ttu-id="a0ac1-117">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="a0ac1-117">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="a0ac1-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ac1-118">Description</span></span>                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a0ac1-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="a0ac1-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                       | <span data-ttu-id="a0ac1-120">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-120">The method was successful.</span></span><br/>                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="a0ac1-121"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="a0ac1-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>      | <span data-ttu-id="a0ac1-122">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-122">The volume is locked.</span></span><br/>                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="a0ac1-123"><dt>**F \_ E \_ automatische Entsperrung \_ aktiviert**</dt> <dt>2150694953 (0x80310029)</dt></span><span class="sxs-lookup"><span data-stu-id="a0ac1-123"><dt>**FVE\_E\_AUTOUNLOCK\_ENABLED**</dt> <dt>2150694953 (0x80310029)</dt></span></span> </dl> | <span data-ttu-id="a0ac1-124">Dieses Volume kann nicht entschlüsselt werden, da zum automatischen Entsperren von Datenvolumes verwendete Schlüssel verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-124">This volume cannot be decrypted because keys used to automatically unlock data volumes are available.</span></span> <br/> <span data-ttu-id="a0ac1-125">Verwenden Sie [**clearallautounlockkeys**](clearallautounlockkeys-win32-encryptablevolume.md) , um diese Schlüssel zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-125">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) to remove these keys.</span></span><br/> |



 

## <a name="security-considerations"></a><span data-ttu-id="a0ac1-126">Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="a0ac1-126">Security Considerations</span></span>

<span data-ttu-id="a0ac1-127">Durch den Aufruf der **Entschlüsselungsmethode** bleiben Daten ungeschützt.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-127">Calling the **Decrypt** method leaves data unprotected.</span></span>

<span data-ttu-id="a0ac1-128">Wenn der Schutzstatus des Volumes 1 (Schutz vor) ist, bevor diese Methode verwendet wird, wird beim erfolgreichen Abschluss dieser Methode der Schutzstatus auf 0 (Schutz deaktiviert) festgestellt, da ein teilweise verschlüsseltes Volume definitionsgemäß nicht geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-128">If the protection status of the volume is 1 (PROTECTION ON) before this method is used, successful completion of this method changes the protection status to 0 (PROTECTION OFF), since by definition a partially encrypted volume is not protected.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0ac1-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0ac1-129">Remarks</span></span>

<span data-ttu-id="a0ac1-130">Wenn das Volume nicht bereits vollständig entschlüsselt wurde, bewirkt das Ausführen von **entschlüsseln** , dass " [**GetConfiguration Manager Status**](getconversionstatus-win32-encryptablevolume.md) " angibt, dass die Entschlüsselung fortgesetzt wird, und zeigt den Prozentsatz des Volumes an, der verschlüsselt bleiben soll.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-130">If the volume is not already fully decrypted, running **Decrypt** causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that decryption is progress and shows the percentage of the volume that remains encrypted.</span></span>

<span data-ttu-id="a0ac1-131">Wenn der Schutzstatus des Volumes "on" ist, bevor diese Methode ausgeführt wird, wird durch das Ausführen dieser Methode der Schutzstatus in "Off" geändert, da ein teilweise verschlüsseltes Volume in der Definition nicht geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-131">If the protection status of the volume is "on" before this method is run, running this method changes the protection status to "off", since by definition a partially encrypted volume is not protected.</span></span>

<span data-ttu-id="a0ac1-132">Wenn diese Methode auf dem momentan ausgelaufenden Betriebssystem Volume ausgeführt wird und das Betriebssystem Volume zum automatischen Entsperren von Datenvolumes verwendet wird (siehe Methode [**enableautounlock**](enableautounlock-win32-encryptablevolume.md)), müssen Sie zuerst die-Methode [**clearallautounlockkeys**](clearallautounlockkeys-win32-encryptablevolume.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-132">If this method is run on the currently running operating system volume and this operating system volume is being used to automatically unlock data volumes (see method [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)) you must first call the method [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md).</span></span>

<span data-ttu-id="a0ac1-133">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a0ac1-134">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-134">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="a0ac1-135">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a0ac1-136">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="a0ac1-136">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0ac1-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0ac1-137">Requirements</span></span>



| <span data-ttu-id="a0ac1-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0ac1-138">Requirement</span></span> | <span data-ttu-id="a0ac1-139">Wert</span><span class="sxs-lookup"><span data-stu-id="a0ac1-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ac1-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0ac1-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a0ac1-141">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0ac1-141">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a0ac1-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a0ac1-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a0ac1-143">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0ac1-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a0ac1-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="a0ac1-144">Namespace</span></span><br/>                | <span data-ttu-id="a0ac1-145">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="a0ac1-145">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="a0ac1-146">Header</span><span class="sxs-lookup"><span data-stu-id="a0ac1-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0ac1-147"><dt>InfoCard. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0ac1-147"><dt>Infocard.h</dt></span></span> </dl>                   |
| <span data-ttu-id="a0ac1-148">MOF</span><span class="sxs-lookup"><span data-stu-id="a0ac1-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0ac1-149"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a0ac1-149"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0ac1-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0ac1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0ac1-151">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="a0ac1-151">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
