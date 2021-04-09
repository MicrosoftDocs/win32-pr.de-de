---
description: Aktualisiert ein Volume vom Windows Vista-Format auf das Windows 7-Format.
ms.assetid: d6654e92-8176-471b-b8e5-815dd9512240
title: UpgradeVolume-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UpgradeVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6769e8a4a480becc5a5584826f60cdb85f8b90e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958830"
---
# <a name="upgradevolume-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="3ca44-103">UpgradeVolume-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="3ca44-103">UpgradeVolume method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="3ca44-104">Die **UpgradeVolume** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " aktualisiert ein Volume vom Windows Vista-Format auf das Windows 7-Format.</span><span class="sxs-lookup"><span data-stu-id="3ca44-104">The **UpgradeVolume** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class upgrades a volume from the Windows Vista format to the Windows 7 format.</span></span> <span data-ttu-id="3ca44-105">Dies ist ein nicht umkehrbarer Vorgang.</span><span class="sxs-lookup"><span data-stu-id="3ca44-105">This is a nonreversible operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ca44-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ca44-106">Syntax</span></span>


```mof
uint32 UpgradeVolume();
```



## <a name="parameters"></a><span data-ttu-id="3ca44-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ca44-107">Parameters</span></span>

<span data-ttu-id="3ca44-108">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3ca44-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3ca44-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ca44-109">Return value</span></span>

<span data-ttu-id="3ca44-110">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ca44-110">Type: **uint32**</span></span>

<span data-ttu-id="3ca44-111">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="3ca44-111">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="3ca44-112">Wenn das Volume bereits entsperrt ist und keine weiteren Fehler auftreten, gibt diese Methode 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="3ca44-112">If the volume is already unlocked and no other errors occur, this method returns zero.</span></span>



| <span data-ttu-id="3ca44-113">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="3ca44-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="3ca44-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ca44-114">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3ca44-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="3ca44-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="3ca44-116">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3ca44-116">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3ca44-117"><dt>**E \_ InvalidArg**</dt> <dt>214794287 (0xccd802f)</dt></span><span class="sxs-lookup"><span data-stu-id="3ca44-117"><dt>**E\_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span></span> </dl>            | <span data-ttu-id="3ca44-118">Mindestens eines der Argumente ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="3ca44-118">One or more of the arguments are not valid.</span></span><br/>                                       |
| <dl> <span data-ttu-id="3ca44-119"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="3ca44-119"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="3ca44-120">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="3ca44-120">The volume is locked.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="3ca44-121"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="3ca44-121"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="3ca44-122">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ca44-122">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="3ca44-123">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="3ca44-123">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="3ca44-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ca44-124">Remarks</span></span>

<span data-ttu-id="3ca44-125">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="3ca44-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3ca44-126">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="3ca44-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="3ca44-127">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3ca44-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3ca44-128">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="3ca44-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ca44-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ca44-129">Requirements</span></span>



| <span data-ttu-id="3ca44-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ca44-130">Requirement</span></span> | <span data-ttu-id="3ca44-131">Wert</span><span class="sxs-lookup"><span data-stu-id="3ca44-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca44-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ca44-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3ca44-133">Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ca44-133">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3ca44-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ca44-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3ca44-135">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ca44-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3ca44-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ca44-136">Namespace</span></span><br/>                | <span data-ttu-id="3ca44-137">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="3ca44-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="3ca44-138">MOF</span><span class="sxs-lookup"><span data-stu-id="3ca44-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ca44-139"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3ca44-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ca44-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ca44-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ca44-141">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="3ca44-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
