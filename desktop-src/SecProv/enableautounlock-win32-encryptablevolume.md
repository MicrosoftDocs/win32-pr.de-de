---
description: Ermöglicht das automatische Entsperren eines Datenvolumens, wenn das Volume eingebunden wird.
ms.assetid: ec77b17f-545b-40a7-91b2-ff0b32b8370d
title: Enableautounlock-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 39456e9130081e52820cd91ba3e191ee40ab2374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865424"
---
# <a name="enableautounlock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b3526-103">Enableautounlock-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="b3526-103">EnableAutoUnlock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b3526-104">Die **enableautounlock** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " ermöglicht das automatische Entsperren eines Datenvolumens, wenn das Volume eingebunden wird.</span><span class="sxs-lookup"><span data-stu-id="b3526-104">The **EnableAutoUnlock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class allows a data volume to be automatically unlocked when the volume is mounted.</span></span>

<span data-ttu-id="b3526-105">Bei der automatischen Entsperrung wird ein externer Schlüssel im Betriebssystem gespeichert, mit dem das Volume automatisch auf dem momentan laufenden Betriebssystem Volume entsperrt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b3526-105">Automatic unlocking saves an external key to the operating system that can automatically unlock the volume onto the currently running operating system volume.</span></span>

<span data-ttu-id="b3526-106">Um diese Methode verwenden zu können, muss das Betriebssystem Volume bereits durch BitLocker-Laufwerkverschlüsselung geschützt werden, oder es muss eine Verschlüsselung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b3526-106">To use this method, the operating system volume must already be protected by BitLocker Drive Encryption or must have encryption in progress.</span></span> <span data-ttu-id="b3526-107">Außerdem muss bereits ein externer Schlüssel für das Datenvolumen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b3526-107">In addition, there must already exist an external key for the data volume.</span></span> <span data-ttu-id="b3526-108">Verwenden Sie [**protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md) , um den externen Schlüssel zu erstellen, mit dem das Volume automatisch entsperrt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b3526-108">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) to create the external key that can automatically unlock the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3526-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3526-109">Syntax</span></span>


```mof
uint32 EnableAutoUnlock(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="b3526-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3526-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3526-111">*Volumekeyprotectorid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3526-111">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3526-112">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b3526-112">Type: **string**</span></span>

<span data-ttu-id="b3526-113">Eine Zeichenfolge, die die Schlüssel Schutzvorrichtung des Typs "externer Schlüssel" identifiziert, der zum automatischen Entsperren des Volumes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b3526-113">A string that identifies the key protector of the type "External Key" used to automatically unlock the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3526-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3526-114">Return value</span></span>

<span data-ttu-id="b3526-115">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b3526-115">Type: **uint32**</span></span>

<span data-ttu-id="b3526-116">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="b3526-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="b3526-117">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="b3526-117">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="b3526-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3526-118">Description</span></span>                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3526-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b3526-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="b3526-120">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b3526-120">The method was successful.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="b3526-121"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="b3526-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>          | <span data-ttu-id="b3526-122">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="b3526-122">The volume is locked.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="b3526-123"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="b3526-123"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>          | <span data-ttu-id="b3526-124">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b3526-124">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="b3526-125">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="b3526-125">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                 |
| <dl> <span data-ttu-id="b3526-126"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="b3526-126"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                   | <span data-ttu-id="b3526-127">Der *volumekeyprotectorid-* Parameter verweist nicht auf eine gültige Schlüssel Schutzvorrichtung vom Typ "externer Schlüssel".</span><span class="sxs-lookup"><span data-stu-id="b3526-127">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector of the type "External Key".</span></span><br/>                                                          |
| <dl> <span data-ttu-id="b3526-128"><dt>**F \_ E \_ Not \_ Data \_ Volume**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="b3526-128"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl>       | <span data-ttu-id="b3526-129">Die Methode kann nicht für das aktuell laufende Betriebssystem Volume ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b3526-129">The method cannot be run for the currently running operating system volume.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="b3526-130"><dt>**F \_ E \_ OS \_ nicht \_ geschützt**</dt> <dt>2150694944 (0x80310020)</dt></span><span class="sxs-lookup"><span data-stu-id="b3526-130"><dt>**FVE\_E\_OS\_NOT\_PROTECTED**</dt> <dt>2150694944 (0x80310020)</dt></span></span> </dl>      | <span data-ttu-id="b3526-131">Die Methode kann nicht ausgeführt werden, wenn das derzeit ausgeführte Betriebssystem Volume nicht durch BitLocker-Laufwerkverschlüsselung geschützt ist oder keine Verschlüsselung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3526-131">The method cannot be run if the currently running operating system volume is not protected by BitLocker Drive Encryption or does not have encryption in progress.</span></span><br/> |
| <dl> <span data-ttu-id="b3526-132">Das <dt> **Volume \_ wurde \_ \_ \_ bereits**</dt> <dt>2150694943 (0x8031001f)</dt> gebunden.</span><span class="sxs-lookup"><span data-stu-id="b3526-132"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY** </dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="b3526-133">Das automatische Entsperren auf dem Volume wurde bereits aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b3526-133">Automatic unlocking on the volume has previously been enabled.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="b3526-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3526-134">Remarks</span></span>

<span data-ttu-id="b3526-135">Wenn eine gültige volumeschlüsselschutzvorrichtung vom Typ "externer Schlüssel" angegeben ist, wird der zugehörige externe 256-Bit-Schlüssel aus der Schutzvorrichtung extrahiert und in der Registrierung des aktuell ausgelaufenden Betriebssystems zusammen mit der volumeschlüsselschutzvorrichtung-ID gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b3526-135">Given a valid volume key protector of the type "External Key", the related 256-bit external key is extracted from the protector and stored into the registry of the currently running operating system, along with the volume key protector ID.</span></span>

<span data-ttu-id="b3526-136">Wenn der der volumeschlüsselschutzkennung zugeordnete externe Schlüssel gelöscht wird, wird die Funktion zum automatischen Entsperren des Volumes deaktiviert oder angehalten.</span><span class="sxs-lookup"><span data-stu-id="b3526-136">If the external key associated with the volume key protector ID is deleted, the functionality to automatically unlock the volume is disabled or suspended.</span></span>

> [!Note]  
> <span data-ttu-id="b3526-137">Wechselmedien werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b3526-137">Removable media is not currently supported.</span></span>

 

<span data-ttu-id="b3526-138">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="b3526-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b3526-139">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="b3526-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b3526-140">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b3526-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b3526-141">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b3526-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3526-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3526-142">Requirements</span></span>



| <span data-ttu-id="b3526-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3526-143">Requirement</span></span> | <span data-ttu-id="b3526-144">Wert</span><span class="sxs-lookup"><span data-stu-id="b3526-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3526-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3526-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b3526-146">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3526-146">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b3526-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3526-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b3526-148">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3526-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b3526-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="b3526-149">Namespace</span></span><br/>                | <span data-ttu-id="b3526-150">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="b3526-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b3526-151">MOF</span><span class="sxs-lookup"><span data-stu-id="b3526-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3526-152"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b3526-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3526-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3526-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3526-154">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="b3526-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
