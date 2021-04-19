---
description: Gibt an, ob externe Schlüssel oder zugehörige Informationen, die möglicherweise zum automatischen Entsperren von Datenvolumes verwendet werden, auf dem aktuell laufenden Betriebssystem Volume vorhanden sind.
ms.assetid: 37e7fe85-312d-49ff-aa6b-8c76c4fc4bba
title: Isautounlockkeygespeich-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockKeyStored
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: aedb834bdfd26ce4b348a41b4046c0c4e2c7e260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369738"
---
# <a name="isautounlockkeystored-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c3850-103">Isautounlockkeygespeicherte-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="c3850-103">IsAutoUnlockKeyStored method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c3850-104">Die **isautounlockkeygespeich-** Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt an, ob externe Schlüssel oder verwandte Informationen, die möglicherweise zum automatischen Entsperren von Datenvolumes verwendet werden, im aktuell ausgelaufenden Betriebssystem Volume vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c3850-104">The **IsAutoUnlockKeyStored** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether any external keys or related information that may be used to automatically unlock data volumes exist in the currently running operating system volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3850-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3850-105">Syntax</span></span>


```mof
uint32 IsAutoUnlockKeyStored(
  [out] boolean IsAutoUnlockKeyStored
);
```



## <a name="parameters"></a><span data-ttu-id="c3850-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3850-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3850-107">*Isautounlockkeygespeicherter* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c3850-107">*IsAutoUnlockKeyStored* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3850-108">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="c3850-108">Type: **boolean**</span></span>

<span data-ttu-id="c3850-109">Ist **true** , wenn alle Informationen, die zum automatischen Entsperren von Datenvolumes verwendet werden können, in der Registrierung des aktuell laufenden Betriebssystem Volume gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c3850-109">Is **true** if any information that can be used to automatically unlock data volumes is stored in the registry of the currently running operating system volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3850-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3850-110">Return value</span></span>

<span data-ttu-id="c3850-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3850-111">Type: **uint32**</span></span>

<span data-ttu-id="c3850-112">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="c3850-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c3850-113">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="c3850-113">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="c3850-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3850-114">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c3850-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c3850-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="c3850-116">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c3850-116">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="c3850-117"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="c3850-117"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="c3850-118">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c3850-118">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="c3850-119">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="c3850-119">Add a key protector to enable BitLocker.</span></span> <br/> |
| <dl> <span data-ttu-id="c3850-120"><dt>**F \_ E \_ Not \_ OS \_ Volume**</dt> <dt>2150694952 (0x80310028)</dt></span><span class="sxs-lookup"><span data-stu-id="c3850-120"><dt>**FVE\_E\_NOT\_OS\_VOLUME**</dt> <dt>2150694952 (0x80310028)</dt></span></span> </dl> | <span data-ttu-id="c3850-121">Die-Methode kann nur für das aktuell laufende Betriebssystem Volume ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c3850-121">The method can only be run for the currently running operating system volume.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="c3850-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3850-122">Remarks</span></span>

<span data-ttu-id="c3850-123">Verwenden Sie [**clearallautounlockkeys**](clearallautounlockkeys-win32-encryptablevolume.md) , um alle entsperrenden Informationen aus dem momentan ausgelaufenden Betriebssystem Volume zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="c3850-123">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) to remove all unlocking information from the currently running operating system volume.</span></span>

<span data-ttu-id="c3850-124">Die zum Entsperren eines Volumes verwendeten Informationen werden gespeichert, wenn [**enableautounlock**](enableautounlock-win32-encryptablevolume.md) für ein Daten Volume ausgeführt wird, während das aktuell laufende Betriebssystem Volume ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3850-124">Information used to unlock a volume is stored when [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) is run for a data volume while the currently running operating system volume is running.</span></span>

<span data-ttu-id="c3850-125">" **Isautounlockkey}** " unterscheidet sich von " [**isautounlockkey}**](isautounlockenabled-win32-encryptablevolume.md) " in "", dass auch dann, wenn die automatische Entsperrung für alle Daten Volumes deaktiviert ist, die mit dem Computer verbunden sind, möglicherweise weiterhin Informationen zu nicht mehr vorhandenen Datenvolumen oder Datenvolumes verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c3850-125">**IsAutoUnlockKeyStored** differs from [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) in that even if automatic unlocking is disabled for all data volumes currently connected to the computer, there may still be unlocking information associated with disconnected data volumes or data volumes that no longer exist.</span></span>

<span data-ttu-id="c3850-126">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="c3850-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c3850-127">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="c3850-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c3850-128">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c3850-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c3850-129">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c3850-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3850-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3850-130">Requirements</span></span>



| <span data-ttu-id="c3850-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3850-131">Requirement</span></span> | <span data-ttu-id="c3850-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c3850-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3850-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3850-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c3850-134">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3850-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c3850-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3850-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c3850-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3850-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c3850-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="c3850-137">Namespace</span></span><br/>                | <span data-ttu-id="c3850-138">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="c3850-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c3850-139">MOF</span><span class="sxs-lookup"><span data-stu-id="c3850-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3850-140"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c3850-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3850-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3850-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3850-142">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="c3850-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
