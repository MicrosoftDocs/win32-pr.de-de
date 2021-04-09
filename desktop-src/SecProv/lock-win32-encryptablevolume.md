---
description: Hebt die Bereitstellung des Volumes auf und entfernt den Verschlüsselungsschlüssel des Volumes aus dem System Arbeitsspeicher.
ms.assetid: 8d6e42a0-7b43-46d2-aa5e-941567ef2842
title: Lock-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Lock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 8fb6cd7b4134f4921cdaf57414843fb6522c5823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862287"
---
# <a name="lock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="1715d-103">Lock-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="1715d-103">Lock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="1715d-104">Mit der **Lock** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " wird das Volume getrennt, und der Verschlüsselungsschlüssel des Volumes wird aus dem Systemspeicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="1715d-104">The **Lock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class dismounts the volume and removes the volume's encryption key from system memory.</span></span> <span data-ttu-id="1715d-105">Der Inhalt des Volumes bleibt so lange nicht zugänglich, bis er entweder durch die [**unlockwithexternalkey**](unlockwithexternalkey-win32-encryptablevolume.md) -Methode oder die [**unlockwithnumericalpassword-Methode entsperrt**](unlockwithnumericalpassword-win32-encryptablevolume.md) wird.</span><span class="sxs-lookup"><span data-stu-id="1715d-105">The contents of the volume remain inaccessible until it is unlocked by either the [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) method or the [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="1715d-106">Diese Methode kann für das aktuell laufende Betriebssystem Volume nicht erfolgreich ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1715d-106">This method cannot be successfully run for the currently running operating system volume.</span></span>

> [!Note]  
> <span data-ttu-id="1715d-107">Wenn die Festplatte die Hardware Verschlüsselung unterstützt, wird das Band auf "gesperrt" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1715d-107">If the disc supports hardware encryption, the band is set to "locked".</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1715d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1715d-108">Syntax</span></span>


```mof
uint32 Lock(
  [in, optional] boolean ForceDismount
);
```



## <a name="parameters"></a><span data-ttu-id="1715d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1715d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1715d-110">*ForceDismount* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1715d-110">*ForceDismount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1715d-111">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="1715d-111">Type: **boolean**</span></span>

<span data-ttu-id="1715d-112">**True** gibt an, dass die Bereitstellung des Datenträgers erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="1715d-112">If **true** the disk is forcibly dismounted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1715d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1715d-113">Return value</span></span>

<span data-ttu-id="1715d-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1715d-114">Type: **uint32**</span></span>

<span data-ttu-id="1715d-115">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="1715d-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="1715d-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="1715d-116">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="1715d-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1715d-117">Description</span></span>                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1715d-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1715d-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="1715d-119">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1715d-119">The method was successful.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="1715d-120"><dt>**E \_ Zugriff \_ verweigert**</dt> <dt>2147942405 (0x80070005)</dt></span><span class="sxs-lookup"><span data-stu-id="1715d-120"><dt>**E\_ACCESS\_DENIED**</dt> <dt>2147942405 (0x80070005)</dt></span></span> </dl>               | <span data-ttu-id="1715d-121">Anwendungen greifen auf dieses Volume zu.</span><span class="sxs-lookup"><span data-stu-id="1715d-121">Applications are accessing this volume.</span></span> <span data-ttu-id="1715d-122">Wenn der gesamte Zugriff nicht exklusiv ist, kann die-Methode erfolgreich ausgeführt werden, wenn der *ForceDismount* -Parameter als true angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1715d-122">If all access is nonexclusive, specifying the *ForceDismount* parameter as true allows the method to run successfully.</span></span><br/> |
| <dl> <span data-ttu-id="1715d-123"><dt>**F \_ E \_ nicht \_ verschlüsselt**</dt> <dt>2150694913 (0x80310001)</dt></span><span class="sxs-lookup"><span data-stu-id="1715d-123"><dt>**FVE\_E\_NOT\_ENCRYPTED**</dt> <dt>2150694913 (0x80310001)</dt></span></span> </dl>          | <span data-ttu-id="1715d-124">Das Volume wird vollständig entschlüsselt und kann nicht gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="1715d-124">The volume is fully decrypted and cannot be locked.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="1715d-125"><dt>**F \_ E- \_ Schutz \_ deaktiviert**</dt> <dt>2150694945 (0x80310021)</dt></span><span class="sxs-lookup"><span data-stu-id="1715d-125"><dt>**FVE\_E\_PROTECTION\_DISABLED**</dt> <dt>2150694945 (0x80310021)</dt></span></span> </dl>    | <span data-ttu-id="1715d-126">Der Verschlüsselungsschlüssel für das Volume ist auf dem Datenträger im Klartext verfügbar, sodass das Volume nicht gesperrt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1715d-126">The volume's encryption key is available in the clear on the disk, preventing the volume from being locked.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="1715d-127"><dt>**F \_ E \_ Wiederherstellungs \_ Schlüssel \_ erforderlich**</dt> <dt>2150694946 (0x80310022)</dt></span><span class="sxs-lookup"><span data-stu-id="1715d-127"><dt>**FVE\_E\_RECOVERY\_KEY\_REQUIRED**</dt> <dt>2150694946 (0x80310022)</dt></span></span> </dl> | <span data-ttu-id="1715d-128">Das Volume weist keine Schlüssel Schutzvorrichtungen des Typs "numerisches Kennwort" oder "externer Schlüssel" auf, die zum Entsperren des Volumes erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1715d-128">The volume does not have key protectors of the type "Numerical Password" or "External Key" that are necessary to unlock the volume.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="1715d-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1715d-129">Remarks</span></span>

<span data-ttu-id="1715d-130">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="1715d-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1715d-131">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="1715d-131">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1715d-132">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1715d-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1715d-133">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="1715d-133">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1715d-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1715d-134">Requirements</span></span>



| <span data-ttu-id="1715d-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1715d-135">Requirement</span></span> | <span data-ttu-id="1715d-136">Wert</span><span class="sxs-lookup"><span data-stu-id="1715d-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1715d-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1715d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1715d-138">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1715d-138">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1715d-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1715d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1715d-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1715d-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1715d-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="1715d-141">Namespace</span></span><br/>                | <span data-ttu-id="1715d-142">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="1715d-142">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="1715d-143">MOF</span><span class="sxs-lookup"><span data-stu-id="1715d-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1715d-144"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1715d-144"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1715d-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1715d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1715d-146">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="1715d-146">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
