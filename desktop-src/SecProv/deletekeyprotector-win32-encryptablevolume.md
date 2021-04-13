---
description: Löscht eine angegebene Schlüssel Schutzvorrichtung für das Volume.
ms.assetid: fa6b89b0-83b6-4be2-8b7b-61b0501747d2
title: Deletekeyprotector-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtector
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b1f539683bb76559d08066d01de6aeca0394ced3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343078"
---
# <a name="deletekeyprotector-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="5762b-103">Deletekeyprotector-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="5762b-103">DeleteKeyProtector method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="5762b-104">Die **deletekeyprotector** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " löscht eine bestimmte Schlüssel Schutzvorrichtung für das Volume.</span><span class="sxs-lookup"><span data-stu-id="5762b-104">The **DeleteKeyProtector** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class deletes a given key protector for the volume.</span></span>

<span data-ttu-id="5762b-105">Wenn ein unverschlüsseltes Volume über Schlüssel Schutzvorrichtungen verfügt und die letzte Schlüssel Schutzvorrichtung von **deletekeyprotector** entfernt wird, wird das Volume auf ein Standardmäßiges NTFS-Dateisystem zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="5762b-105">If an unencrypted volume has key protectors, when **DeleteKeyProtector** removes the last key protector, the volume reverts to a standard NTFS file system.</span></span>

<span data-ttu-id="5762b-106">Wenn ein Volume nie verschlüsselt wurde, wird das Löschen der Schlüssel Schutzvorrichtung auf NTFS zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="5762b-106">If a volume has never been encrypted, deleting the key protector will revert to NTFS.</span></span>

<span data-ttu-id="5762b-107">Wenn das Volume noch nicht vollständig entschlüsselt ist, verwenden Sie [**disablekeyprotector**](disablekeyprotectors-win32-encryptablevolume.md) , bevor Sie die letzte Schlüssel Schutzvorrichtung des Volumes entfernen, um sicherzustellen, dass die verschlüsselten Teile des Volumes zugänglich bleiben.</span><span class="sxs-lookup"><span data-stu-id="5762b-107">If the volume is not yet fully decrypted, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing the volume's last key protector to ensure that encrypted portions of the volume remain accessible.</span></span>

## <a name="syntax"></a><span data-ttu-id="5762b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5762b-108">Syntax</span></span>


```mof
uint32 DeleteKeyProtector(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="5762b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5762b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5762b-110">*Volumekeyprotectorid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5762b-110">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5762b-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5762b-111">Type: **string**</span></span>

<span data-ttu-id="5762b-112">Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="5762b-112">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5762b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5762b-113">Return value</span></span>

<span data-ttu-id="5762b-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5762b-114">Type: **uint32**</span></span>

<span data-ttu-id="5762b-115">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="5762b-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="5762b-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="5762b-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="5762b-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5762b-117">Description</span></span>                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5762b-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5762b-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                          | <span data-ttu-id="5762b-119">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5762b-119">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="5762b-120"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="5762b-120"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>         | <span data-ttu-id="5762b-121">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="5762b-121">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="5762b-122"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="5762b-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>         | <span data-ttu-id="5762b-123">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5762b-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="5762b-124">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="5762b-124">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="5762b-125"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="5762b-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                  | <span data-ttu-id="5762b-126">Der *volumekeyprotectorid-* Parameter verweist nicht auf eine gültige Schlüssel Schutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="5762b-126">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="5762b-127"><dt>**F \_ E- \_ Taste \_ erforderlich**</dt> <dt>2150694941 (0x8031001d)</dt></span><span class="sxs-lookup"><span data-stu-id="5762b-127"><dt>**FVE\_E\_KEY\_REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt></span></span> </dl>          | <span data-ttu-id="5762b-128">Die letzte Schlüssel Schutzvorrichtung für ein teilweise oder vollständig verschlüsseltes Volume kann nicht entfernt werden, wenn Schlüssel Schutzvorrichtungen aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="5762b-128">The last key protector for a partially or fully encrypted volume cannot be removed if key protectors are enabled.</span></span> <span data-ttu-id="5762b-129">Verwenden Sie [**disablekeyprotector**](disablekeyprotectors-win32-encryptablevolume.md) , bevor Sie diese letzte Schlüssel Schutzvorrichtung entfernen, um sicherzustellen, dass die verschlüsselten Teile des Volumes zugänglich bleiben.</span><span class="sxs-lookup"><span data-stu-id="5762b-129">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing this last key protector to ensure that encrypted portions of the volume remain accessible.</span></span> <br/> |
| <dl> <span data-ttu-id="5762b-130"><dt>**F \_ E \_ Volume \_ \_ bereits**</dt> <dt>2150694943 (0x8031001f)</dt></span><span class="sxs-lookup"><span data-stu-id="5762b-130"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="5762b-131">Diese Schlüssel Schutzvorrichtung kann nicht gelöscht werden, da Sie zum automatischen Entsperren des Volumes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5762b-131">This key protector cannot be deleted because it is being used to automatically unlock the volume.</span></span> <br/> <span data-ttu-id="5762b-132">Verwenden Sie [**disableautounlock**](disableautounlock-win32-encryptablevolume.md) , um das automatische Entsperren zu deaktivieren, bevor Sie diese Schlüssel Schutzvorrichtung löschen.</span><span class="sxs-lookup"><span data-stu-id="5762b-132">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) to disable automatic unlocking before deleting this key protector.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="5762b-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5762b-133">Remarks</span></span>

<span data-ttu-id="5762b-134">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="5762b-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5762b-135">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="5762b-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5762b-136">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5762b-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5762b-137">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5762b-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5762b-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5762b-138">Requirements</span></span>



| <span data-ttu-id="5762b-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5762b-139">Requirement</span></span> | <span data-ttu-id="5762b-140">Wert</span><span class="sxs-lookup"><span data-stu-id="5762b-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5762b-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5762b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5762b-142">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5762b-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5762b-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5762b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5762b-144">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5762b-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5762b-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="5762b-145">Namespace</span></span><br/>                | <span data-ttu-id="5762b-146">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="5762b-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="5762b-147">MOF</span><span class="sxs-lookup"><span data-stu-id="5762b-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5762b-148"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5762b-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5762b-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5762b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5762b-150">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="5762b-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
