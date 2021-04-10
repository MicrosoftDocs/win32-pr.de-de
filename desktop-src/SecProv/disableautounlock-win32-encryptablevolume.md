---
description: Entfernt den externen Schlüssel, der auf dem momentan laufenden Betriebssystem Volume gespeichert ist.
ms.assetid: a8c4bb3b-6566-4173-b550-e89740f1cba6
title: Disableautounlock-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6dd4e11e2ff4906627c2d790987500062136d56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865435"
---
# <a name="disableautounlock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="60e11-103">Disableautounlock-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="60e11-103">DisableAutoUnlock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="60e11-104">Die **disableautounlock** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " entfernt den externen Schlüssel, der auf dem momentan laufenden Betriebssystem Volume gespeichert ist, sodass ein Daten Volume bei der Bereitstellung nicht automatisch entsperrt wird, z. b. wenn Wechsel Speichergeräte mit dem Computer verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="60e11-104">The **DisableAutoUnlock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class removes the external key saved onto the currently running operating system volume so that a data volume is not automatically unlocked when it is mounted, such as when removable memory devices are connected to the computer.</span></span>

<span data-ttu-id="60e11-105">Wenn das automatische Entsperren deaktiviert oder angehalten wird, müssen die Methoden " [**unlockwithexternalkey**](unlockwithexternalkey-win32-encryptablevolume.md) " oder " [**unlockwithnumericalpassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) " verwendet werden, um das Volume zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="60e11-105">If automatic unlocking is disabled or suspended, the methods [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) or [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) must be used to unlock the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="60e11-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="60e11-106">Syntax</span></span>


```mof
uint32 DisableAutoUnlock();
```



## <a name="parameters"></a><span data-ttu-id="60e11-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="60e11-107">Parameters</span></span>

<span data-ttu-id="60e11-108">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="60e11-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="60e11-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60e11-109">Return value</span></span>

<span data-ttu-id="60e11-110">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60e11-110">Type: **uint32**</span></span>

<span data-ttu-id="60e11-111">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="60e11-111">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="60e11-112">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="60e11-112">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="60e11-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60e11-113">Description</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="60e11-114"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="60e11-114"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                       | <span data-ttu-id="60e11-115">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="60e11-115">The method was successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="60e11-116">Laufwerk <dt> **\_ E \_ \_ nicht \_ gebunden**</dt> <dt>2150694935 (0x80310017)</dt></span><span class="sxs-lookup"><span data-stu-id="60e11-116"><dt>**FVE\_E\_VOLUME\_NOT\_BOUND** </dt> <dt>2150694935 (0x80310017)</dt></span></span> </dl> | <span data-ttu-id="60e11-117">Das automatische Entsperren auf dem Volume ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="60e11-117">Automatic unlocking on the volume is disabled.</span></span><br/>                                   |
| <dl> <span data-ttu-id="60e11-118"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="60e11-118"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>      | <span data-ttu-id="60e11-119">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="60e11-119">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="60e11-120">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="60e11-120">Add a key protector to enable BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="60e11-121"><dt>**F \_ E \_ Not \_ Data \_ Volume**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="60e11-121"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl>   | <span data-ttu-id="60e11-122">Die Methode kann nicht für das aktuell laufende Betriebssystem Volume ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="60e11-122">The method cannot be run for the currently running operating system volume.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="60e11-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60e11-123">Remarks</span></span>

<span data-ttu-id="60e11-124">Wenn keine Fehler zurückgegeben werden, entfernt diese Methode alle volumeschutzvorrichtungen und externen Schlüssel aus der Registrierung, die zum automatischen Entsperren des Volumes verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60e11-124">If no errors are returned, this method removes from the registry any volume protector IDs and external keys used to automatically unlock the volume.</span></span>

<span data-ttu-id="60e11-125">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="60e11-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="60e11-126">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="60e11-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="60e11-127">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="60e11-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="60e11-128">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="60e11-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60e11-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60e11-129">Requirements</span></span>



| <span data-ttu-id="60e11-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60e11-130">Requirement</span></span> | <span data-ttu-id="60e11-131">Wert</span><span class="sxs-lookup"><span data-stu-id="60e11-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60e11-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60e11-132">Minimum supported client</span></span><br/> | <span data-ttu-id="60e11-133">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60e11-133">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="60e11-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60e11-134">Minimum supported server</span></span><br/> | <span data-ttu-id="60e11-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60e11-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="60e11-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="60e11-136">Namespace</span></span><br/>                | <span data-ttu-id="60e11-137">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="60e11-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="60e11-138">MOF</span><span class="sxs-lookup"><span data-stu-id="60e11-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60e11-139"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="60e11-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60e11-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60e11-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e11-141">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="60e11-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
