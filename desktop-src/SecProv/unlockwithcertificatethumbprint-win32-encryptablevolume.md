---
description: Verwendet den angegebenen Zertifikat Fingerabdruck, um den abgeleiteten Schlüssel abzurufen und das verschlüsselte Volume zu entsperren.
ms.assetid: 41c25d17-db1b-427e-907b-a547483927e0
title: Unlockwithcertifitorethumschlag Print-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5955334b6c147feea43d5e0a2c83a8e00050d900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750825"
---
# <a name="unlockwithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="a370e-103">Unlockwithcertifierethumschlag Print-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="a370e-103">UnlockWithCertificateThumbprint method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="a370e-104">Die **unlockwithcertifi-** Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " verwendet den angegebenen Fingerabdruck des [*Zertifikats*](../secgloss/c-gly.md) , um den abgeleiteten Schlüssel abzurufen und das verschlüsselte Volume zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="a370e-104">The **UnlockWithCertificateThumbprint** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided [*certificate*](../secgloss/c-gly.md) thumbprint to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="a370e-105">Wenn die Festplatte Hardware Verschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "entsperrt" fest.</span><span class="sxs-lookup"><span data-stu-id="a370e-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a370e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a370e-106">Syntax</span></span>


```mof
uint32 UnlockWithCertificateThumbprint(
  [in] string CertThumbprint,
  [in] string PIN
);
```



## <a name="parameters"></a><span data-ttu-id="a370e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a370e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a370e-108">*Certthumbprint* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a370e-108">*CertThumbprint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a370e-109">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a370e-109">Type: **string**</span></span>

<span data-ttu-id="a370e-110">Der Fingerabdruck Wert 0 wird akzeptiert und führt zu einer Suche nach dem lokalen Speicher für das entsprechende Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="a370e-110">A thumbprint value of 0 is accepted and results in a search of the local store for the appropriate certificate.</span></span> <span data-ttu-id="a370e-111">Wenn ein einzelnes BitLocker-Zertifikat gefunden wird, ist die Suche erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a370e-111">If a single BitLocker certificate is found, the search is successful.</span></span> <span data-ttu-id="a370e-112">Wenn keines oder mehrere Zertifikate gefunden werden, schlägt die Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="a370e-112">If none or more than one certificate is found, the method fails.</span></span>

</dd> <dt>

<span data-ttu-id="a370e-113">*Pin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a370e-113">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a370e-114">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a370e-114">Type: **string**</span></span>

<span data-ttu-id="a370e-115">Eine vom Benutzer angegebene persönliche Identifikations Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a370e-115">A user-specified personal identification string.</span></span> <span data-ttu-id="a370e-116">Diese Zeichenfolge muss aus einer Sequenz von 4 bis 20 Ziffern bestehen.</span><span class="sxs-lookup"><span data-stu-id="a370e-116">This string must consist of a sequence of 4 to 20 digits.</span></span> <span data-ttu-id="a370e-117">Diese Zeichenfolge wird verwendet, um den [*Schlüsselspeicher Anbieter*](../secgloss/k-gly.md) (KSP) im Hintergrund zu authentifizieren, wenn Sie mit einer [*Smartcard*](../secgloss/s-gly.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a370e-117">This string is used to silently authenticate the [*key storage provider*](../secgloss/k-gly.md) (KSP) when used with a [*smart card*](../secgloss/s-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a370e-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a370e-118">Return value</span></span>

<span data-ttu-id="a370e-119">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a370e-119">Type: **uint32**</span></span>

<span data-ttu-id="a370e-120">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="a370e-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="a370e-121">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="a370e-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="a370e-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a370e-122">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a370e-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="a370e-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="a370e-124">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a370e-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="a370e-125"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="a370e-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="a370e-126">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a370e-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="a370e-127">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="a370e-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="a370e-128"><dt>**F \_ E \_ \_**</dt> -Fehler bei Authentifizierung <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="a370e-128"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>   | <span data-ttu-id="a370e-129">Das Volume kann nicht mit den bereitgestellten Informationen entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="a370e-129">The volume cannot be unlocked by using the provided information.</span></span> <br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="a370e-130"><dt>**F \_ E \_ Protector \_ nicht \_ gefunden**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="a370e-130"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="a370e-131">Die angegebene Schlüssel Schutzvorrichtung ist auf dem Volume nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a370e-131">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="a370e-132">Sie müssen eine andere Schlüssel Schutzvorrichtung eingeben.</span><span class="sxs-lookup"><span data-stu-id="a370e-132">You must enter another key protector.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="a370e-133"><dt>**F \_ E \_ PrivateKey-Authentifizierung ist \_ \_ fehlgeschlagen**</dt> <dt>2150695060 (0x80310094)</dt></span><span class="sxs-lookup"><span data-stu-id="a370e-133"><dt>**FVE\_E\_PRIVATEKEY\_AUTH\_FAILED**</dt> <dt>2150695060 (0x80310094)</dt></span></span> </dl> | <span data-ttu-id="a370e-134">Der dem angegebenen Zertifikat zugeordnete [*private Schlüssel*](../secgloss/p-gly.md) konnte nicht autorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a370e-134">The [*private key*](../secgloss/p-gly.md) associated with the specified certificate could not be authorized.</span></span> <span data-ttu-id="a370e-135">Die Autorisierung für den privaten Schlüssel wurde entweder nicht bereitgestellt, oder die angegebene Autorisierung war nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="a370e-135">The private key authorization was either not provided or the provided authorization was not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a370e-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a370e-136">Requirements</span></span>



| <span data-ttu-id="a370e-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a370e-137">Requirement</span></span> | <span data-ttu-id="a370e-138">Wert</span><span class="sxs-lookup"><span data-stu-id="a370e-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a370e-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a370e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a370e-140">Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a370e-140">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a370e-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a370e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a370e-142">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a370e-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a370e-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="a370e-143">Namespace</span></span><br/>                | <span data-ttu-id="a370e-144">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="a370e-144">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="a370e-145">MOF</span><span class="sxs-lookup"><span data-stu-id="a370e-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a370e-146"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a370e-146"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a370e-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a370e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a370e-148">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="a370e-148">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
