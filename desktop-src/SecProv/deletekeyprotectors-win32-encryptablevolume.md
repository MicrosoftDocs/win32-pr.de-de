---
description: Löscht alle Schlüssel Schutzvorrichtungen für das Volume.
ms.assetid: 46f61899-87ff-4e86-8409-635117cff4de
title: Deletekeyprotector-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0195a89884dcd9f9288cab020d9804dcc81b7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368773"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="84a4a-103">Deletekeyprotector-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="84a4a-103">DeleteKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="84a4a-104">Die **deletekeyprotector** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " löscht alle Schlüssel Schutzvorrichtungen für das Volume.</span><span class="sxs-lookup"><span data-stu-id="84a4a-104">The **DeleteKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class deletes all key protectors for the volume.</span></span>

<span data-ttu-id="84a4a-105">Wenn ein unverschlüsseltes Volume über Schlüssel Schutzvorrichtungen verfügt, wird das Volume in einem standardmäßigen NTFS-Dateisystem wieder hergestellt, wenn **deletekeyprotector** erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84a4a-105">If an unencrypted volume has key protectors, when **DeleteKeyProtectors** is run successfully the volume reverts to a standard NTFS file system.</span></span>

<span data-ttu-id="84a4a-106">Wenn das Volume noch nicht vollständig entschlüsselt ist, verwenden Sie [**disablekeyprotector**](disablekeyprotectors-win32-encryptablevolume.md) vor dem Ausführen von **deletekeyprotector** , um sicherzustellen, dass die verschlüsselten Teile des Volumes zugänglich bleiben.</span><span class="sxs-lookup"><span data-stu-id="84a4a-106">If the volume is not yet fully decrypted, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before running **DeleteKeyProtectors** to ensure that encrypted portions of the volume remain accessible.</span></span>

## <a name="syntax"></a><span data-ttu-id="84a4a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="84a4a-107">Syntax</span></span>


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a><span data-ttu-id="84a4a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="84a4a-108">Parameters</span></span>

<span data-ttu-id="84a4a-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="84a4a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="84a4a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84a4a-110">Return value</span></span>

<span data-ttu-id="84a4a-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84a4a-111">Type: **uint32**</span></span>

<span data-ttu-id="84a4a-112">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="84a4a-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="84a4a-113">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="84a4a-113">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="84a4a-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84a4a-114">Description</span></span>                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="84a4a-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="84a4a-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                          | <span data-ttu-id="84a4a-116">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="84a4a-116">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="84a4a-117"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="84a4a-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>         | <span data-ttu-id="84a4a-118">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="84a4a-118">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="84a4a-119"><dt>**F \_ E- \_ Taste \_ erforderlich**</dt> <dt>2150694941 (0x8031001d)</dt></span><span class="sxs-lookup"><span data-stu-id="84a4a-119"><dt>**FVE\_E\_KEY\_REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt></span></span> </dl>          | <span data-ttu-id="84a4a-120">Die letzte Schlüssel Schutzvorrichtung für ein teilweise oder vollständig verschlüsseltes Volume kann nicht entfernt werden, wenn Schlüssel Schutzvorrichtungen aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="84a4a-120">The last key protector for a partially or fully encrypted volume cannot be removed if key protectors are enabled.</span></span> <span data-ttu-id="84a4a-121">Verwenden Sie [**disablekeyprotector**](disablekeyprotectors-win32-encryptablevolume.md) , bevor Sie diese letzte Schlüssel Schutzvorrichtung entfernen, um sicherzustellen, dass die verschlüsselten Teile des Volumes zugänglich bleiben.</span><span class="sxs-lookup"><span data-stu-id="84a4a-121">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing this last key protector to ensure that encrypted portions of the volume remain accessible.</span></span> <br/> |
| <dl> <span data-ttu-id="84a4a-122"><dt>**F \_ E \_ Volume \_ \_ bereits**</dt> <dt>2150694943 (0x8031001f)</dt></span><span class="sxs-lookup"><span data-stu-id="84a4a-122"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="84a4a-123">Schlüssel Schutzvorrichtungen können nicht gelöscht werden, da eine von Ihnen zum automatischen Entsperren des Volumes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="84a4a-123">Key protectors cannot be deleted because one of them is being used to automatically unlock the volume.</span></span> <br/> <span data-ttu-id="84a4a-124">Verwenden Sie [**disableautounlock**](disableautounlock-win32-encryptablevolume.md) , um das automatische Entsperren zu deaktivieren, bevor Sie diese Methode ausführen.</span><span class="sxs-lookup"><span data-stu-id="84a4a-124">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) to disable automatic unlocking before running this method.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="84a4a-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84a4a-125">Remarks</span></span>

<span data-ttu-id="84a4a-126">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="84a4a-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="84a4a-127">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="84a4a-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="84a4a-128">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="84a4a-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="84a4a-129">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="84a4a-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84a4a-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84a4a-130">Requirements</span></span>



| <span data-ttu-id="84a4a-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84a4a-131">Requirement</span></span> | <span data-ttu-id="84a4a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="84a4a-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84a4a-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84a4a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="84a4a-134">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84a4a-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="84a4a-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84a4a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="84a4a-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84a4a-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84a4a-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="84a4a-137">Namespace</span></span><br/>                | <span data-ttu-id="84a4a-138">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="84a4a-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="84a4a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="84a4a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84a4a-140"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="84a4a-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84a4a-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84a4a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84a4a-142">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="84a4a-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
