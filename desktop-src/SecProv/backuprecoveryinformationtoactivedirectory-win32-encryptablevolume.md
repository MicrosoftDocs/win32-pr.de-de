---
description: Sichert Wiederherstellungsdaten in Active Directory.
ms.assetid: 664562b3-5679-4185-8bbc-5d5350494707
title: Backuprecoveryinformationdeactivedirectory-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.BackupRecoveryInformationToActiveDirectory
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a04901139aa46f42e06eaea1c91af0e3bac202e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352603"
---
# <a name="backuprecoveryinformationtoactivedirectory-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="9396f-103">Backuprecoveryinformationdeactivedirectory-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="9396f-103">BackupRecoveryInformationToActiveDirectory method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="9396f-104">Die **backuprecoveryinformationdeactivedirectory** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " sichert Wiederherstellungsdaten in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9396f-104">The **BackupRecoveryInformationToActiveDirectory** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class backs up recovery data to Active Directory.</span></span> <span data-ttu-id="9396f-105">Diese Methode erfordert, dass auf dem Volume eine numerische Kenn Wort Schutzvorrichtung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9396f-105">This method requires a numerical password protector to be present on the volume.</span></span> <span data-ttu-id="9396f-106">Gruppenrichtlinie müssen auch konfiguriert werden, um die Sicherung von Wiederherstellungs Informationen in Active Directory zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="9396f-106">Group Policy must also be configured to enable backup of recovery information to Active Directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="9396f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9396f-107">Syntax</span></span>


```mof
uint32 BackupRecoveryInformationToActiveDirectory(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="9396f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9396f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9396f-109">*Volumekeyprotectorid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9396f-109">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9396f-110">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9396f-110">Type: **string**</span></span>

<span data-ttu-id="9396f-111">Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="9396f-111">A unique string identifier used to manage an encrypted volume key protector.</span></span> <span data-ttu-id="9396f-112">Diese Schlüssel Schutzvorrichtung muss eine numerische Kennwort-Schutzvorrichtung sein.</span><span class="sxs-lookup"><span data-stu-id="9396f-112">This key protector must be a numerical password protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9396f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9396f-113">Return value</span></span>

<span data-ttu-id="9396f-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9396f-114">Type: **uint32**</span></span>

<span data-ttu-id="9396f-115">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="9396f-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="9396f-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="9396f-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="9396f-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9396f-117">Description</span></span>                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9396f-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9396f-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="9396f-119">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9396f-119">The method was successful.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="9396f-120"><dt>**S \_ FALSE**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="9396f-120"><dt>**S\_FALSE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                         | <span data-ttu-id="9396f-121">In Gruppenrichtlinie ist das Speichern von Wiederherstellungs Informationen für Active Directory nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9396f-121">Group Policy does not permit the storage of recovery information to Active Directory.</span></span><br/>                         |
| <dl> <span data-ttu-id="9396f-122"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="9396f-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="9396f-123">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9396f-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="9396f-124">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="9396f-124">Add a key protector to enable BitLocker.</span></span> <br/>                             |
| <dl> <span data-ttu-id="9396f-125"><dt>**F \_ E \_ ungültiger \_ \_ schutzschutztyp**</dt> <dt>2150694970 (0x8031003a)</dt></span><span class="sxs-lookup"><span data-stu-id="9396f-125"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="9396f-126">Die angegebene Schlüssel Schutzvorrichtung ist keine numerische Schlüssel Schutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="9396f-126">The specified key protector is not a numerical key protector.</span></span> <span data-ttu-id="9396f-127">Sie müssen eine numerische Kennwort-Schutzvorrichtung eingeben.</span><span class="sxs-lookup"><span data-stu-id="9396f-127">You must enter a numerical password protector.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="9396f-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9396f-128">Requirements</span></span>



| <span data-ttu-id="9396f-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9396f-129">Requirement</span></span> | <span data-ttu-id="9396f-130">Wert</span><span class="sxs-lookup"><span data-stu-id="9396f-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9396f-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9396f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9396f-132">Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9396f-132">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9396f-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9396f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9396f-134">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9396f-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9396f-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="9396f-135">Namespace</span></span><br/>                | <span data-ttu-id="9396f-136">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="9396f-136">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="9396f-137">MOF</span><span class="sxs-lookup"><span data-stu-id="9396f-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9396f-138"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9396f-138"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9396f-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9396f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9396f-140">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="9396f-140">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




