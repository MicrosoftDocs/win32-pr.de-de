---
description: Verwendet die Passphrase zum Abrufen des abgeleiteten Schlüssels.
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: Protectkeywithpasspphrase-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f97806652d86b104a0f333d40d299cfa9502cf3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356724"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="38a12-103">Protectkeywithpasspphrase-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="38a12-103">ProtectKeyWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="38a12-104">Die **protectkeywithpasspphrase** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " verwendet die Passphrase zum Abrufen des abgeleiteten Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="38a12-104">The **ProtectKeyWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="38a12-105">Nachdem der abgeleitete Schlüssel berechnet wurde, wird der abgeleitete Schlüssel verwendet, um den Hauptschlüssel des verschlüsselten Volumes zu sichern.</span><span class="sxs-lookup"><span data-stu-id="38a12-105">After the derived key is calculated, the derived key is used to secure the encrypted volume's master key.</span></span>

## <a name="syntax"></a><span data-ttu-id="38a12-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="38a12-106">Syntax</span></span>


```mof
uint32 ProtectKeyWithPassphrase(
  [in, optional] string FriendlyName,
  [in]           string Passphrase,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="38a12-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="38a12-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38a12-108">*FriendlyName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="38a12-108">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="38a12-109">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="38a12-109">Type: **string**</span></span>

<span data-ttu-id="38a12-110">Eine Zeichenfolge, die einen vom Benutzer zugewiesenen Zeichen folgen Bezeichner für diese Schlüssel Schutzvorrichtung angibt.</span><span class="sxs-lookup"><span data-stu-id="38a12-110">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="38a12-111">Wenn dieser Parameter nicht angegeben wird, wird ein leerer Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="38a12-111">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="38a12-112">*Passphrase* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38a12-112">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38a12-113">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="38a12-113">Type: **string**</span></span>

<span data-ttu-id="38a12-114">Eine Zeichenfolge, die die Passphrase angibt.</span><span class="sxs-lookup"><span data-stu-id="38a12-114">A string that specifies the passphrase.</span></span>

</dd> <dt>

<span data-ttu-id="38a12-115">*Volumekeyprotectorid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="38a12-115">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38a12-116">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="38a12-116">Type: **string**</span></span>

<span data-ttu-id="38a12-117">Eine Zeichenfolge, die die erstellte Schlüssel Schutzvorrichtung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="38a12-117">A string that uniquely identifies the created key protector.</span></span>

<span data-ttu-id="38a12-118">Wenn das Laufwerk die Hardware Verschlüsselung unterstützt und BitLocker keinen bandbesitz hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüssel Schutzvorrichtung wird in die pro-Band-Metadaten geschrieben.</span><span class="sxs-lookup"><span data-stu-id="38a12-118">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38a12-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38a12-119">Return value</span></span>

<span data-ttu-id="38a12-120">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38a12-120">Type: **uint32**</span></span>

<span data-ttu-id="38a12-121">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="38a12-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="38a12-122">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="38a12-122">Return code/value</span></span>                                                                                                                                                                                        | <span data-ttu-id="38a12-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38a12-123">Description</span></span>                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="38a12-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="38a12-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                        | <span data-ttu-id="38a12-125">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="38a12-125">The method was successful.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="38a12-126"><dt>**F \_ E ist im abgesicherten \_ \_ \_ \_ \_ Modus**</dt> <dt>2150694976 (0x80310040)</dt> nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="38a12-126"><dt>**FVE\_E\_NOT\_ALLOWED\_IN\_SAFE\_MODE**</dt> <dt>2150694976 (0x80310040)</dt></span></span> </dl>         | <span data-ttu-id="38a12-127">BitLocker-Laufwerkverschlüsselung können nur für Wiederherstellungs Zwecke verwendet werden, wenn Sie im abgesicherten Modus verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38a12-127">BitLocker Drive Encryption can only be used for recovery purposes when used in Safe Mode.</span></span><br/>                     |
| <dl> <span data-ttu-id="38a12-128"><dt>**F \_ E \_ - \_ richtlinienpasspphrase \_ nicht \_ zulässig**</dt> <dt>2150695018 (0x8031006a)</dt></span><span class="sxs-lookup"><span data-stu-id="38a12-128"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695018 (0x8031006A)</dt></span></span> </dl>     | <span data-ttu-id="38a12-129">Die Erstellung einer Passphrase wird von der Gruppenrichtlinie nicht zugelassen.</span><span class="sxs-lookup"><span data-stu-id="38a12-129">Group policy does not permit the creation of a passphrase.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="38a12-130"><dt>**F \_ E-fi-Kenn \_ \_ \_ Wörter verhindern Passphrase**</dt> <dt>2150695020 (0x8031006c)</dt></span><span class="sxs-lookup"><span data-stu-id="38a12-130"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>           | <span data-ttu-id="38a12-131">Die Gruppenrichtlinien Einstellung, die die Kompatibilität mit der Konformität erfordert, verhindert, dass die Passphrase generiert oder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="38a12-131">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span><br/> |
| <dl> <span data-ttu-id="38a12-132"><dt>**F \_ E \_ Richtlinie \_ ungültige \_ Passphrasen \_ Länge**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="38a12-132"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl>  | <span data-ttu-id="38a12-133">Die angegebene Passphrase entspricht nicht den Anforderungen an die minimale oder maximale Länge.</span><span class="sxs-lookup"><span data-stu-id="38a12-133">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                             |
| <dl> <span data-ttu-id="38a12-134"><dt>**F \_ E \_ - \_ richtlinienpass Phrase \_ zu \_ einfach**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="38a12-134"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>      | <span data-ttu-id="38a12-135">Die Passphrase erfüllt nicht die Komplexitäts Anforderungen, die vom Administrator in der Gruppenrichtlinie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="38a12-135">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>            |
| <dl> <span data-ttu-id="38a12-136"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="38a12-136"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                       | <span data-ttu-id="38a12-137">Das Volume ist bereits durch BitLocker-Laufwerkverschlüsselung gesperrt.</span><span class="sxs-lookup"><span data-stu-id="38a12-137">The volume is already locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="38a12-138">Das Laufwerk muss in der Systemsteuerung entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="38a12-138">You must unlock the drive from Control Panel.</span></span><br/>     |
| <dl> <span data-ttu-id="38a12-139"><dt>**F \_ E \_ überlappendes \_ Update**</dt> <dt>2150694948 (0x80310024)</dt></span><span class="sxs-lookup"><span data-stu-id="38a12-139"><dt>**FVE\_E\_OVERLAPPED\_UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span></span> </dl>                   | <span data-ttu-id="38a12-140">Der Kontroll Block für das verschlüsselte Volume wurde von einem anderen Thread aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="38a12-140">The control block for the encrypted volume was updated by another thread.</span></span><br/>                                     |
| <dl> <span data-ttu-id="38a12-141"><dt>**F \_ E \_ Key \_ Protector \_ \_ wird nicht unterstützt**</dt> <dt>2150695017 (0x80310069)</dt></span><span class="sxs-lookup"><span data-stu-id="38a12-141"><dt>**FVE\_E\_KEY\_PROTECTOR\_NOT\_SUPPORTED**</dt> <dt>2150695017 (0x80310069)</dt></span></span> </dl>       | <span data-ttu-id="38a12-142">Die Schlüssel Schutzvorrichtung wird von der Version von BitLocker-Laufwerkverschlüsselung, die sich aktuell auf dem Volume befindet, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38a12-142">The key protector is not supported by the version of BitLocker Drive Encryption currently on the volume.</span></span><br/>      |
| <dl> <span data-ttu-id="38a12-143"><dt>**F \_ E \_ OS- \_ Volumen \_ Passphrase \_ nicht \_ zulässig**</dt> <dt>2150695021 (0x8031006d)</dt></span><span class="sxs-lookup"><span data-stu-id="38a12-143"><dt>**FVE\_E\_OS\_VOLUME\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695021 (0x8031006D)</dt></span></span> </dl> | <span data-ttu-id="38a12-144">Die Passphrase kann dem Betriebssystem Volume nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="38a12-144">The passphrase cannot be added to the operating system volume.</span></span> <br/>                                               |
| <dl> <span data-ttu-id="38a12-145"><dt>**F \_ E \_ Protector \_ vorhanden**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="38a12-145"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>                    | <span data-ttu-id="38a12-146">Die angegebene Schlüssel Schutzvorrichtung ist auf diesem Volume bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="38a12-146">The provided key protector already exists on this volume.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="38a12-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38a12-147">Requirements</span></span>



| <span data-ttu-id="38a12-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38a12-148">Requirement</span></span> | <span data-ttu-id="38a12-149">Wert</span><span class="sxs-lookup"><span data-stu-id="38a12-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38a12-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="38a12-150">Minimum supported client</span></span><br/> | <span data-ttu-id="38a12-151">Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38a12-151">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="38a12-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="38a12-152">Minimum supported server</span></span><br/> | <span data-ttu-id="38a12-153">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38a12-153">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="38a12-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="38a12-154">Namespace</span></span><br/>                | <span data-ttu-id="38a12-155">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="38a12-155">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="38a12-156">MOF</span><span class="sxs-lookup"><span data-stu-id="38a12-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38a12-157"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="38a12-157"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38a12-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38a12-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38a12-159">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="38a12-159">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




