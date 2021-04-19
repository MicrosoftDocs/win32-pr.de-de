---
description: Verwendet die Passphrase zum Abrufen des abgeleiteten Schlüssels.
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: Unlockwithpasspphrase-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 75c5522a0781b1cd229bf97d2549433a426fbfc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360809"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="da474-103">Unlockwithpasspphrase-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="da474-103">UnlockWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="da474-104">Die **unlockwithpasspphrase** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " verwendet die Passphrase zum Abrufen des abgeleiteten Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="da474-104">The **UnlockWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="da474-105">Nachdem der abgeleitete Schlüssel berechnet wurde, wird der abgeleitete Schlüssel verwendet, um den Hauptschlüssel des verschlüsselten Volumes zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="da474-105">After the derived key is calculated, the derived key is used to unlock the encrypted volume's master key.</span></span>

> [!Note]  
> <span data-ttu-id="da474-106">Wenn die Festplatte Hardware Verschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "entsperrt" fest.</span><span class="sxs-lookup"><span data-stu-id="da474-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="da474-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="da474-107">Syntax</span></span>


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a><span data-ttu-id="da474-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="da474-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da474-109">*Passphrase* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da474-109">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da474-110">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="da474-110">Type: **string**</span></span>

<span data-ttu-id="da474-111">Eine Zeichenfolge, die die Passphrase angibt.</span><span class="sxs-lookup"><span data-stu-id="da474-111">A string that specifies the passphrase.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da474-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da474-112">Return value</span></span>

<span data-ttu-id="da474-113">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da474-113">Type: **uint32**</span></span>

<span data-ttu-id="da474-114">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="da474-114">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="da474-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="da474-115">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="da474-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da474-116">Description</span></span>                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="da474-117"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="da474-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="da474-118">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="da474-118">The method was successful.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="da474-119"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="da474-119"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="da474-120">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="da474-120">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="da474-121">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="da474-121">Add a key protector to enable BitLocker.</span></span> <br/>                              |
| <dl> <span data-ttu-id="da474-122"><dt>**F \_ E-fi-Kenn \_ \_ \_ Wörter verhindern Passphrase**</dt> <dt>2150695020 (0x8031006c)</dt></span><span class="sxs-lookup"><span data-stu-id="da474-122"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>          | <span data-ttu-id="da474-123">Die Gruppenrichtlinien Einstellung, die die Kompatibilität mit der Konformität erfordert, verhindert, dass die Passphrase generiert oder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="da474-123">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span> <br/> |
| <dl> <span data-ttu-id="da474-124"><dt>**F \_ E \_ Richtlinie \_ ungültige \_ Passphrasen \_ Länge**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="da474-124"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl> | <span data-ttu-id="da474-125">Die angegebene Passphrase entspricht nicht den Anforderungen an die minimale oder maximale Länge.</span><span class="sxs-lookup"><span data-stu-id="da474-125">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                              |
| <dl> <span data-ttu-id="da474-126"><dt>**F \_ E \_ - \_ richtlinienpass Phrase \_ zu \_ einfach**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="da474-126"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>     | <span data-ttu-id="da474-127">Die Passphrase erfüllt nicht die Komplexitäts Anforderungen, die vom Administrator in der Gruppenrichtlinie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="da474-127">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>             |
| <dl> <span data-ttu-id="da474-128"><dt>**F \_ E \_ \_**</dt> -Fehler bei Authentifizierung <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="da474-128"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>              | <span data-ttu-id="da474-129">Das Volume kann mit den bereitgestellten Informationen nicht entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="da474-129">The volume cannot be unlocked with the provided information.</span></span> <br/>                                                  |
| <dl> <span data-ttu-id="da474-130"><dt>**F \_ E \_ Protector \_ nicht \_ gefunden**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="da474-130"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>               | <span data-ttu-id="da474-131">Die angegebene Schlüssel Schutzvorrichtung ist auf dem Volume nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="da474-131">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="da474-132">Sie müssen eine andere Schlüssel Schutzvorrichtung eingeben.</span><span class="sxs-lookup"><span data-stu-id="da474-132">You must enter another key protector.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="da474-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da474-133">Requirements</span></span>



| <span data-ttu-id="da474-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da474-134">Requirement</span></span> | <span data-ttu-id="da474-135">Wert</span><span class="sxs-lookup"><span data-stu-id="da474-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da474-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da474-136">Minimum supported client</span></span><br/> | <span data-ttu-id="da474-137">Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da474-137">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="da474-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da474-138">Minimum supported server</span></span><br/> | <span data-ttu-id="da474-139">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da474-139">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="da474-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="da474-140">Namespace</span></span><br/>                | <span data-ttu-id="da474-141">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="da474-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="da474-142">MOF</span><span class="sxs-lookup"><span data-stu-id="da474-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da474-143"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="da474-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da474-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da474-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da474-145">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="da474-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




