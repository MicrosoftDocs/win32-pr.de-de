---
description: Entfernt alle externen Schlüssel und zugehörigen Informationen, die auf dem momentan laufenden Betriebssystem Volume gespeichert sind, das zum automatischen Entsperren von Datenvolumes verwendet wird.
ms.assetid: a5fef793-0634-493d-b62d-cb842844b1e8
title: Clearallautounlockkeys-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ClearAllAutoUnlockKeys
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b7f7e68891865893c1444a2c5de2370799b74426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345034"
---
# <a name="clearallautounlockkeys-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="7e8d7-103">Clearallautounlockkeys-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="7e8d7-103">ClearAllAutoUnlockKeys method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="7e8d7-104">Die **clearallautounlockkeys** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " entfernt alle externen Schlüssel und zugehörigen Informationen, die auf dem momentan ausgelaufenden Betriebssystem Volume gespeichert sind, das zum automatischen Entsperren von Datenvolumes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7e8d7-104">The **ClearAllAutoUnlockKeys** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class removes all external keys and related information saved onto the currently running operating system volume that are used to automatically unlock data volumes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e8d7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e8d7-105">Syntax</span></span>


```mof
uint32 ClearAllAutoUnlockKeys();
```



## <a name="parameters"></a><span data-ttu-id="7e8d7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e8d7-106">Parameters</span></span>

<span data-ttu-id="7e8d7-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7e8d7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7e8d7-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e8d7-108">Return value</span></span>

<span data-ttu-id="7e8d7-109">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e8d7-109">Type: **uint32**</span></span>

<span data-ttu-id="7e8d7-110">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="7e8d7-110">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="7e8d7-111">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="7e8d7-111">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="7e8d7-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e8d7-112">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7e8d7-113"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7e8d7-113"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="7e8d7-114">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7e8d7-114">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="7e8d7-115"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="7e8d7-115"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="7e8d7-116">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7e8d7-116">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="7e8d7-117">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="7e8d7-117">Add a key protector to enable BitLocker.</span></span> <br/> |
| <dl> <span data-ttu-id="7e8d7-118"><dt>**F \_ E \_ Not \_ OS \_ Volume**</dt> <dt>2150694952 (0x80310028)</dt></span><span class="sxs-lookup"><span data-stu-id="7e8d7-118"><dt>**FVE\_E\_NOT\_OS\_VOLUME**</dt> <dt>2150694952 (0x80310028)</dt></span></span> </dl> | <span data-ttu-id="7e8d7-119">Die-Methode kann nur für das aktuell laufende Betriebssystem Volume ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7e8d7-119">The method can only be run for the currently running operating system volume.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="7e8d7-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e8d7-120">Remarks</span></span>

<span data-ttu-id="7e8d7-121">**Clearallautounlockkeys** erreicht die gleiche Funktionalität wie das Ausführen von [**disableautounlock**](disableautounlock-win32-encryptablevolume.md) für jedes Daten Volume, das jemals dem aktuell ausgelaufenden Betriebssystem zugeordnet ist. Dies gilt auch für Datenvolumes, die derzeit nicht mit dem Computer verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="7e8d7-121">**ClearAllAutoUnlockKeys** achieves the same functionality as running [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) for every data volume that has ever been associated with the currently running operating system, even data volumes that are not currently connected to the computer.</span></span> <span data-ttu-id="7e8d7-122">Außerdem werden alle veralteten entsperrinformationen entfernt, die Daten Volumes zugeordnet sind, die nicht mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7e8d7-122">It also removes any stale unlocking information associated with data volumes that no longer exist.</span></span>

<span data-ttu-id="7e8d7-123">Verwenden Sie vor dem Aufrufen von " [**entschlüsseln**](decrypt-win32-encryptablevolume.md) " auf dem derzeit ausgelaufenden Betriebssystem Volume " **clearallautounlockkeys** ", um sicherzustellen, dass die Informationen in der Registrierung des Betriebssystems zum automatischen Entsperren von Datenvolumes nicht auf der Festplatte zugänglich sind.</span><span class="sxs-lookup"><span data-stu-id="7e8d7-123">Before calling [**Decrypt**](decrypt-win32-encryptablevolume.md) on the currently running operating system volume, use **ClearAllAutoUnlockKeys** to ensure that information placed in the operating system registry to automatically unlock data volumes is not accessible in the clear on disk.</span></span>

<span data-ttu-id="7e8d7-124">Nachdem **clearallautounlockkeys** erfolgreich ausgeführt wurde, können die Methoden " [**unlockwithexternalkey**](unlockwithexternalkey-win32-encryptablevolume.md) " oder " [**unlockwithnumericalpassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) " verwendet werden, um alle Datenvolumes auf diesem Computer zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="7e8d7-124">After **ClearAllAutoUnlockKeys** runs successfully, the methods [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) or [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) can be used to unlock all data volumes on this computer.</span></span> <span data-ttu-id="7e8d7-125">Verwenden Sie [**enableautounlock**](enableautounlock-win32-encryptablevolume.md) zum erneuten Aktivieren des automatischen Entsperrens eines Datenvolumens.</span><span class="sxs-lookup"><span data-stu-id="7e8d7-125">Use [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) to re-enable automatic unlocking of a data volume.</span></span>

<span data-ttu-id="7e8d7-126">Wenn keine anderen Fehler zurückgegeben werden, entfernt **clearallautounlockkeys** alle volumeschutzvorrichtungen und externen Schlüssel aus der Registrierung, die zum automatischen Entsperren von Datenvolumen verwendet werden, die jemals dem aktuell ausgelaufenden Betriebssystem Volume zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="7e8d7-126">If no other errors are returned, **ClearAllAutoUnlockKeys** removes from the registry any volume protector IDs and external keys used to automatically unlock any data volume that has ever been associated with the currently running operating system volume.</span></span>

<span data-ttu-id="7e8d7-127">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="7e8d7-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7e8d7-128">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="7e8d7-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7e8d7-129">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7e8d7-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7e8d7-130">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7e8d7-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e8d7-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e8d7-131">Requirements</span></span>



| <span data-ttu-id="7e8d7-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e8d7-132">Requirement</span></span> | <span data-ttu-id="7e8d7-133">Wert</span><span class="sxs-lookup"><span data-stu-id="7e8d7-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e8d7-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e8d7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7e8d7-135">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e8d7-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7e8d7-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e8d7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7e8d7-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e8d7-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7e8d7-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e8d7-138">Namespace</span></span><br/>                | <span data-ttu-id="7e8d7-139">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="7e8d7-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="7e8d7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="7e8d7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e8d7-141"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7e8d7-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e8d7-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e8d7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e8d7-143">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="7e8d7-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
