---
description: 'ProtectKeyWithPassphrase-Methode der Win32_EncryptableVolume Klasse: Verwendet die Passphrase, um den abgeleiteten Schlüssel zu erhalten.'
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: ProtectKeyWithPassphrase-Methode der Win32_EncryptableVolume Klasse
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
ms.openlocfilehash: 2a7772b1b65890fedbdbb8dcced1ad851f3845b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098348"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6ff4a-103">ProtectKeyWithPassphrase-Methode der Win32 \_ EncryptableVolume-Klasse</span><span class="sxs-lookup"><span data-stu-id="6ff4a-103">ProtectKeyWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6ff4a-104">Die **ProtectKeyWithPassphrase-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) verwendet die Passphrase, um den abgeleiteten Schlüssel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-104">The **ProtectKeyWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="6ff4a-105">Nachdem der abgeleitete Schlüssel berechnet wurde, wird der abgeleitete Schlüssel verwendet, um den Hauptschlüssel des verschlüsselten Volumes zu sichern.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-105">After the derived key is calculated, the derived key is used to secure the encrypted volume's master key.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ff4a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ff4a-106">Syntax</span></span>


```mof
uint32 ProtectKeyWithPassphrase(
  [in, optional] string FriendlyName,
  [in]           string Passphrase,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="6ff4a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ff4a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ff4a-108">*FriendlyName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="6ff4a-108">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6ff4a-109">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ff4a-109">Type: **string**</span></span>

<span data-ttu-id="6ff4a-110">Eine Zeichenfolge, die einen vom Benutzer zugewiesenen Zeichenfolgenbezeichner für diese Schlüsselschutzvorrichtung angibt.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-110">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="6ff4a-111">Wenn dieser Parameter nicht angegeben wird, wird ein leerer Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-111">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="6ff4a-112">*Passphrase* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6ff4a-112">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ff4a-113">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ff4a-113">Type: **string**</span></span>

<span data-ttu-id="6ff4a-114">Eine Zeichenfolge, die die Passphrase angibt.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-114">A string that specifies the passphrase.</span></span>

</dd> <dt>

<span data-ttu-id="6ff4a-115">*VolumeKeyProtectorID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6ff4a-115">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ff4a-116">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ff4a-116">Type: **string**</span></span>

<span data-ttu-id="6ff4a-117">Eine Zeichenfolge, die die erstellte Schlüsselschutzvorrichtung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-117">A string that uniquely identifies the created key protector.</span></span>

<span data-ttu-id="6ff4a-118">Wenn das Laufwerk hardwareverschlüsselung unterstützt und BitLocker keinen Bandbesitz übernommen hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüsselschutzvorrichtung wird in die Metadaten pro Band geschrieben.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-118">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ff4a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ff4a-119">Return value</span></span>

<span data-ttu-id="6ff4a-120">Typ: **uint32**</span><span class="sxs-lookup"><span data-stu-id="6ff4a-120">Type: **uint32**</span></span>

<span data-ttu-id="6ff4a-121">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="6ff4a-122">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="6ff4a-122">Return code/value</span></span>                                                                                                                                                                                        | <span data-ttu-id="6ff4a-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ff4a-123">Description</span></span>                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6ff4a-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6ff4a-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                        | <span data-ttu-id="6ff4a-125">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-125">The method was successful.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="6ff4a-126"><dt>**FVE \_ E \_ \_ NICHT ZULÄSSIG IM \_ \_ ABGESICHERTEN \_ MODUS**</dt> <dt>2150694976 (0x80310040)</dt></span><span class="sxs-lookup"><span data-stu-id="6ff4a-126"><dt>**FVE\_E\_NOT\_ALLOWED\_IN\_SAFE\_MODE**</dt> <dt>2150694976 (0x80310040)</dt></span></span> </dl>         | <span data-ttu-id="6ff4a-127">BitLocker-Laufwerkverschlüsselung können nur zu Wiederherstellungszwecken verwendet werden, wenn sie im abgesicherten Modus verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-127">BitLocker Drive Encryption can only be used for recovery purposes when used in Safe Mode.</span></span><br/>                     |
| <dl> <span data-ttu-id="6ff4a-128"><dt>**FVE \_ E \_ POLICY \_ PASSPHRASE NOT \_ \_ ALLOWED**</dt> <dt>2150695018 (0x8031006A) (E POLICY PASSPHRASE NOT ALLOWED 2150695018 (E POLICY PASSPHRASE NOT ALLOWED 2150695018 (E</dt> POLICY PASSPHRASE NOT ALLOWED 21</span><span class="sxs-lookup"><span data-stu-id="6ff4a-128"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695018 (0x8031006A)</dt></span></span> </dl>     | <span data-ttu-id="6ff4a-129">Die Gruppenrichtlinie lässt die Erstellung einer Passphrase nicht zu.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-129">Group policy does not permit the creation of a passphrase.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="6ff4a-130"><dt>**FVE \_ E \_ FIPS \_ VERHINDERT \_ PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span><span class="sxs-lookup"><span data-stu-id="6ff4a-130"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>           | <span data-ttu-id="6ff4a-131">Die Gruppenrichtlinieneinstellung, die FIPS-Konformität erfordert, hat verhindert, dass die Passphrase generiert oder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-131">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span><br/> |
| <dl> <span data-ttu-id="6ff4a-132"><dt>**FVE \_ E \_ POLICY \_ INVALID \_ PASSPHRASE \_ LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="6ff4a-132"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl>  | <span data-ttu-id="6ff4a-133">Die angegebene Passphrase erfüllt nicht die Mindest- oder Höchstlängenanforderungen.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-133">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                             |
| <dl> <span data-ttu-id="6ff4a-134"><dt>**FVE \_ E \_ POLICY \_ PASSPHRASE \_ TOO \_ SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="6ff4a-134"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>      | <span data-ttu-id="6ff4a-135">Die Passphrase erfüllt nicht die Komplexitätsanforderungen, die der Administrator in der Gruppenrichtlinie festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-135">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>            |
| <dl> <span data-ttu-id="6ff4a-136"><dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="6ff4a-136"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                       | <span data-ttu-id="6ff4a-137">Das Volume ist bereits durch BitLocker-Laufwerkverschlüsselung gesperrt.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-137">The volume is already locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="6ff4a-138">Sie müssen das Laufwerk aus Systemsteuerung entsperren.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-138">You must unlock the drive from Control Panel.</span></span><br/>     |
| <dl> <span data-ttu-id="6ff4a-139"><dt>**FVE \_ E \_ OVERLAPPED \_ UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span><span class="sxs-lookup"><span data-stu-id="6ff4a-139"><dt>**FVE\_E\_OVERLAPPED\_UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span></span> </dl>                   | <span data-ttu-id="6ff4a-140">Der Kontrollblock für das verschlüsselte Volume wurde von einem anderen Thread aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-140">The control block for the encrypted volume was updated by another thread.</span></span><br/>                                     |
| <dl> <span data-ttu-id="6ff4a-141"><dt>**FVE \_ E KEY PROTECTOR NOT SUPPORTED 2150695017 (0X80310069) \_ (E-SCHLÜSSELSCHUTZVORRICHTUNG \_ WIRD NICHT \_ \_ UNTERSTÜTZT**</dt> <dt>2150695017 (0x80310069)</dt></span><span class="sxs-lookup"><span data-stu-id="6ff4a-141"><dt>**FVE\_E\_KEY\_PROTECTOR\_NOT\_SUPPORTED**</dt> <dt>2150695017 (0x80310069)</dt></span></span> </dl>       | <span data-ttu-id="6ff4a-142">Die Schlüsselschutzvorrichtung wird von der Version von BitLocker-Laufwerkverschlüsselung, die sich derzeit auf dem Volume befindet, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-142">The key protector is not supported by the version of BitLocker Drive Encryption currently on the volume.</span></span><br/>      |
| <dl> <span data-ttu-id="6ff4a-143"><dt>**FVE \_ E \_ \_ BETRIEBSSYSTEMVOLUME \_ PASSPHRASE \_ NICHT \_ ZULÄSSIG**</dt> <dt>2150695021 (0x8031006D)</dt></span><span class="sxs-lookup"><span data-stu-id="6ff4a-143"><dt>**FVE\_E\_OS\_VOLUME\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695021 (0x8031006D)</dt></span></span> </dl> | <span data-ttu-id="6ff4a-144">Die Passphrase kann dem Betriebssystemvolume nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-144">The passphrase cannot be added to the operating system volume.</span></span> <br/>                                               |
| <dl> <span data-ttu-id="6ff4a-145"><dt>**FVE \_ E \_ PROTECTOR \_ EXISTS**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="6ff4a-145"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>                    | <span data-ttu-id="6ff4a-146">Die bereitgestellte Schlüsselschutzvorrichtung ist auf diesem Volume bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-146">The provided key protector already exists on this volume.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="6ff4a-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ff4a-147">Requirements</span></span>



| <span data-ttu-id="6ff4a-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ff4a-148">Requirement</span></span> | <span data-ttu-id="6ff4a-149">Wert</span><span class="sxs-lookup"><span data-stu-id="6ff4a-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff4a-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ff4a-150">Minimum supported client</span></span><br/> | <span data-ttu-id="6ff4a-151">Nur Windows 7 Enterprise- und Windows 7 \[ Ultimate-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ff4a-151">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6ff4a-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ff4a-152">Minimum supported server</span></span><br/> | <span data-ttu-id="6ff4a-153">Nur Windows Server 2008 \[ R2-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ff4a-153">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6ff4a-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ff4a-154">Namespace</span></span><br/>                | <span data-ttu-id="6ff4a-155">\\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="6ff4a-155">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6ff4a-156">MOF</span><span class="sxs-lookup"><span data-stu-id="6ff4a-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ff4a-157"><dt>Win32 \_ encryptablevolume.mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ff4a-157"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ff4a-158">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6ff4a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff4a-159">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="6ff4a-159">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




