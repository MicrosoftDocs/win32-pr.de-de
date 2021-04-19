---
description: Gibt an, ob der Inhalt des Volumes von Windows aus zugänglich ist.
ms.assetid: 54b2a41b-11c6-40ec-97fa-74996c15554e
title: Getlockstatus-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetLockStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3e81f77c37904f26e87f22b8e2b3b88763fe86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342838"
---
# <a name="getlockstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="26f91-103">Getlockstatus-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="26f91-103">GetLockStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="26f91-104">Die **getlockstatus** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt an, ob der Inhalt des Volumes von Windows aus zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="26f91-104">The **GetLockStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the contents of the volume are accessible from Windows.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f91-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="26f91-105">Syntax</span></span>


```mof
uint32 GetLockStatus(
  [out] uint32 LockStatus
);
```



## <a name="parameters"></a><span data-ttu-id="26f91-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="26f91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f91-107">*Sperr Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="26f91-107">*LockStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26f91-108">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26f91-108">Type: **uint32**</span></span>

<span data-ttu-id="26f91-109">Gibt an, ob der Inhalt des Volumes von Windows aus zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="26f91-109">Specifies whether the contents of the volume are accessible from Windows.</span></span>



| <span data-ttu-id="26f91-110">Wert</span><span class="sxs-lookup"><span data-stu-id="26f91-110">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="26f91-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="26f91-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unlocked"></span><span id="unlocked"></span><span id="UNLOCKED"></span><dl> <span data-ttu-id="26f91-112"><dt>**Entsperrt**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="26f91-112"><dt>**Unlocked**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="26f91-113">Für eine Standard-HDD:</span><span class="sxs-lookup"><span data-stu-id="26f91-113">For a standard HDD:</span></span><br/> <span data-ttu-id="26f91-114">Der gesamte Inhalt des Volumes ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="26f91-114">The full contents of the volume are accessible.</span></span> <span data-ttu-id="26f91-115">Ein entsperrtes Volume wird entweder vollständig entschlüsselt, oder der Verschlüsselungsschlüssel ist auf dem Datenträger Clear (Löschen) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="26f91-115">An unlocked volume is either fully decrypted or has the encryption key available in the clear on disk.</span></span> <span data-ttu-id="26f91-116">Das Volume mit dem aktuell ausgelaufenden Betriebssystem (z. b. dem ausgelaufenden Windows-Volume) ist immer verfügbar und kann nicht gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="26f91-116">The volume containing the current running operating system (for example, the running Windows volume) is always accessible and cannot be locked.</span></span><br/> <span data-ttu-id="26f91-117">Für einen ehdd:</span><span class="sxs-lookup"><span data-stu-id="26f91-117">For an EHDD:</span></span><br/> <span data-ttu-id="26f91-118">Das Band ist dauerhaft entsperrt.</span><span class="sxs-lookup"><span data-stu-id="26f91-118">The band is perpetually unlocked.</span></span><br/> |
| <span id="Locked"></span><span id="locked"></span><span id="LOCKED"></span><dl> <span data-ttu-id="26f91-119"><dt>**Gesperrt**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="26f91-119"><dt>**Locked**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="26f91-120">Für eine Standard-HDD:</span><span class="sxs-lookup"><span data-stu-id="26f91-120">For a standard HDD:</span></span><br/> <span data-ttu-id="26f91-121">Auf alle oder einen Teil des Inhalts des Volumes kann nicht zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="26f91-121">All or a portion of the contents of the volume are not accessible.</span></span> <span data-ttu-id="26f91-122">Ein gesperrtes Volume muss teilweise oder vollständig verschlüsselt sein, und der Verschlüsselungsschlüssel darf nicht auf dem Datenträger "Clear on" verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="26f91-122">A locked volume must be partially or fully encrypted and must not have the encryption key available in the clear on disk.</span></span><br/> <span data-ttu-id="26f91-123">Für einen ehdd:</span><span class="sxs-lookup"><span data-stu-id="26f91-123">For an EHDD:</span></span><br/> <span data-ttu-id="26f91-124">Das Band ist entsperrt oder gesperrt.</span><span class="sxs-lookup"><span data-stu-id="26f91-124">The band is unlocked or locked.</span></span><br/>                                                                                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26f91-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26f91-125">Return value</span></span>

<span data-ttu-id="26f91-126">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26f91-126">Type: **uint32**</span></span>

<span data-ttu-id="26f91-127">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="26f91-127">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="26f91-128">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="26f91-128">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="26f91-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26f91-129">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="26f91-130"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="26f91-130"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="26f91-131">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="26f91-131">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="26f91-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26f91-132">Remarks</span></span>

<span data-ttu-id="26f91-133">Verwenden Sie [**unlockwithexternalkey**](unlockwithexternalkey-win32-encryptablevolume.md) und [**unlockwithnumericalpassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) , um Zugriff auf die volumeinhalte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="26f91-133">Use the [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) and [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) to get access to the volume contents.</span></span> <span data-ttu-id="26f91-134">Verwenden Sie die [**Lock**](lock-win32-encryptablevolume.md) -Methode, um den Zugriff auf den volumeinhalt zu</span><span class="sxs-lookup"><span data-stu-id="26f91-134">Use the [**Lock**](lock-win32-encryptablevolume.md) method to relinquish access to volume contents.</span></span>

<span data-ttu-id="26f91-135">Das Volume mit dem aktuell ausgelaufenden Betriebssystem ist immer erreichbar und kann nicht gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="26f91-135">The volume that contains the currently running operating system is always accessible and cannot be locked.</span></span>

<span data-ttu-id="26f91-136">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="26f91-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="26f91-137">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="26f91-137">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="26f91-138">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="26f91-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="26f91-139">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="26f91-139">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="26f91-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26f91-140">Requirements</span></span>



| <span data-ttu-id="26f91-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26f91-141">Requirement</span></span> | <span data-ttu-id="26f91-142">Wert</span><span class="sxs-lookup"><span data-stu-id="26f91-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26f91-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26f91-143">Minimum supported client</span></span><br/> | <span data-ttu-id="26f91-144">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26f91-144">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="26f91-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26f91-145">Minimum supported server</span></span><br/> | <span data-ttu-id="26f91-146">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26f91-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="26f91-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="26f91-147">Namespace</span></span><br/>                | <span data-ttu-id="26f91-148">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="26f91-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="26f91-149">MOF</span><span class="sxs-lookup"><span data-stu-id="26f91-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26f91-150"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="26f91-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26f91-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26f91-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f91-152">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="26f91-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
