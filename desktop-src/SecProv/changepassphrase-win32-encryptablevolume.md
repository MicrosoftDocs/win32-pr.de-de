---
description: Verwendet die neue Passphrase zum Abrufen eines neuen abgeleiteten Schlüssels.
ms.assetid: 89398bae-a2a2-466c-8a1e-a702018d679f
title: Changepasspphrase-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f28a78c6cb923b4f8934ec5cc8962b91b7f5139f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351423"
---
# <a name="changepassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="5a013-103">Changepasspphrase-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="5a013-103">ChangePassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="5a013-104">Die **changepasspphrase** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " verwendet die neue Passphrase zum Abrufen eines neuen abgeleiteten Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="5a013-104">The **ChangePassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the new passphrase to obtain a new derived key.</span></span> <span data-ttu-id="5a013-105">Nachdem der abgeleitete Schlüssel berechnet wurde, wird der neue abgeleitete Schlüssel verwendet, um den Hauptschlüssel des verschlüsselten Volumes zu sichern.</span><span class="sxs-lookup"><span data-stu-id="5a013-105">After the derived key is calculated, the new derived key is used to secure the encrypted volume's master key.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a013-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a013-106">Syntax</span></span>


```mof
uint32 ChangePassphrase(
  [in]  string VolumeKeyProtectorID,
  [in]  string NewPassphrase,
  [out] string NewProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="5a013-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a013-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a013-108">*Volumekeyprotectorid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a013-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a013-109">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5a013-109">Type: **string**</span></span>

<span data-ttu-id="5a013-110">Ein eindeutiger Zeichen folgen Bezeichner, der zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a013-110">A unique string identifier that is used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="5a013-111">*Newpasspphrase* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a013-111">*NewPassphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a013-112">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5a013-112">Type: **string**</span></span>

<span data-ttu-id="5a013-113">Eine aktualisierte Zeichenfolge, die die Passphrase angibt.</span><span class="sxs-lookup"><span data-stu-id="5a013-113">An updated string that specifies the passphrase.</span></span>

</dd> <dt>

<span data-ttu-id="5a013-114">*Newprotectorid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5a013-114">*NewProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a013-115">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5a013-115">Type: **string**</span></span>

<span data-ttu-id="5a013-116">Ein aktualisierter eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="5a013-116">An updated unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a013-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a013-117">Return value</span></span>

<span data-ttu-id="5a013-118">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a013-118">Type: **uint32**</span></span>

<span data-ttu-id="5a013-119">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="5a013-119">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="5a013-120">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="5a013-120">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="5a013-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a013-121">Description</span></span>                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a013-122"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5a013-122"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="5a013-123">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5a013-123">The method was successful.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="5a013-124"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="5a013-124"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                      | <span data-ttu-id="5a013-125">Das Volume ist bereits durch BitLocker-Laufwerkverschlüsselung gesperrt.</span><span class="sxs-lookup"><span data-stu-id="5a013-125">The volume is already locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="5a013-126">Das Laufwerk muss in der Systemsteuerung entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="5a013-126">You must unlock the drive from Control Panel.</span></span><br/>   |
| <dl> <span data-ttu-id="5a013-127"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="5a013-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="5a013-128">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5a013-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="5a013-129">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="5a013-129">Add a key protector to enable BitLocker.</span></span> <br/>                           |
| <dl> <span data-ttu-id="5a013-130"><dt>**F \_ E \_ überlappendes \_ Update**</dt> <dt>2150694948 (0x80310024)</dt></span><span class="sxs-lookup"><span data-stu-id="5a013-130"><dt>**FVE\_E\_OVERLAPPED\_UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span></span> </dl>                  | <span data-ttu-id="5a013-131">Der Kontroll Block für das verschlüsselte Volume wurde von einem anderen Thread aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5a013-131">The control block for the encrypted volume was updated by another thread.</span></span><br/>                                   |
| <dl> <span data-ttu-id="5a013-132"><dt>**F \_ E \_ ungültiger \_ \_ schutzschutztyp**</dt> <dt>2150694970 (0x8031003a)</dt></span><span class="sxs-lookup"><span data-stu-id="5a013-132"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl>            | <span data-ttu-id="5a013-133">Die angegebene Schlüssel Schutzvorrichtung weist nicht den richtigen Typ auf.</span><span class="sxs-lookup"><span data-stu-id="5a013-133">The specified key protector is not of the correct type.</span></span> <br/>                                                    |
| <dl> <span data-ttu-id="5a013-134"><dt>**F \_ E \_ Richtlinie \_ ungültige \_ Passphrasen \_ Länge**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="5a013-134"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl> | <span data-ttu-id="5a013-135">Die aktualisierte Passphrase entspricht nicht den Mindestanforderungen oder der maximalen Länge.</span><span class="sxs-lookup"><span data-stu-id="5a013-135">The updated passphrase provided does not meet the minimum or maximum length requirements.</span></span> <br/>                  |
| <dl> <span data-ttu-id="5a013-136"><dt>**F \_ E \_ - \_ richtlinienpass Phrase \_ zu \_ einfach**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="5a013-136"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>     | <span data-ttu-id="5a013-137">Die aktualisierte Passphrase erfüllt nicht die Komplexitäts Anforderungen, die vom Administrator in der Gruppenrichtlinie festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="5a013-137">The updated passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="5a013-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a013-138">Requirements</span></span>



| <span data-ttu-id="5a013-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a013-139">Requirement</span></span> | <span data-ttu-id="5a013-140">Wert</span><span class="sxs-lookup"><span data-stu-id="5a013-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a013-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5a013-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5a013-142">Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a013-142">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5a013-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5a013-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5a013-144">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a013-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5a013-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a013-145">Namespace</span></span><br/>                | <span data-ttu-id="5a013-146">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="5a013-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="5a013-147">MOF</span><span class="sxs-lookup"><span data-stu-id="5a013-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a013-148"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5a013-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a013-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a013-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a013-150">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="5a013-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




