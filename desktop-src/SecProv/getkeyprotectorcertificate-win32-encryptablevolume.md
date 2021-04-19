---
description: Ruft den öffentlichen Schlüssel und den Zertifikat Fingerabdruck für die Schutzvorrichtung eines öffentlichen Schlüssels ab.
ms.assetid: 86fd0562-feb9-4b85-b27b-30270f864d8e
title: Getkeyprotectorcertificate-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3954d3c55c4695e501d486f309598569b1facfc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364132"
---
# <a name="getkeyprotectorcertificate-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6fffa-103">Getkeyprotectorcertificate-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="6fffa-103">GetKeyProtectorCertificate method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6fffa-104">Die **getkeyprotectorcertificate** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " Ruft den [*öffentlichen Schlüssel*](../secgloss/p-gly.md) und den [*Zertifikat*](../secgloss/c-gly.md) Fingerabdruck für die Schutzvorrichtung eines öffentlichen Schlüssels ab.</span><span class="sxs-lookup"><span data-stu-id="6fffa-104">The **GetKeyProtectorCertificate** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the [*public key*](../secgloss/p-gly.md) and [*certificate*](../secgloss/c-gly.md) thumbprint for a public key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fffa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fffa-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PublicKey[],
  [out] string CertThumbprint,
  [out] uint32 CertType
);
```



## <a name="parameters"></a><span data-ttu-id="6fffa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fffa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fffa-107">*Volumekeyprotectorid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6fffa-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fffa-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6fffa-108">Type: **string**</span></span>

<span data-ttu-id="6fffa-109">Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="6fffa-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="6fffa-110">*PublicKey* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6fffa-110">*PublicKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fffa-111">Typ: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="6fffa-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="6fffa-112">Ein Bytearray, das den öffentlichen Schlüssel angibt.</span><span class="sxs-lookup"><span data-stu-id="6fffa-112">An array of bytes that specifies the public key.</span></span>

</dd> <dt>

<span data-ttu-id="6fffa-113">*Certthumbprint* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6fffa-113">*CertThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fffa-114">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6fffa-114">Type: **string**</span></span>

<span data-ttu-id="6fffa-115">Eine Zeichenfolge, die den Zertifikat Fingerabdruck angibt.</span><span class="sxs-lookup"><span data-stu-id="6fffa-115">A string that specifies the certificate thumbprint.</span></span>

</dd> <dt>

<span data-ttu-id="6fffa-116">*Certtype* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6fffa-116">*CertType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fffa-117">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fffa-117">Type: **uint32**</span></span>

<span data-ttu-id="6fffa-118">Eine ganze Zahl ohne Vorzeichen, die den Typ der Schlüssel Schutzvorrichtung angibt.</span><span class="sxs-lookup"><span data-stu-id="6fffa-118">An unsigned integer that specifies the type of the key protector.</span></span> <span data-ttu-id="6fffa-119">Diese Ganzzahl wird zur Unterscheidung zwischen Data Recovery Agent (DRA) und Benutzer Zertifikaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="6fffa-119">This integer is used to differentiate between data recovery agent (DRA) and user certificates.</span></span>



| <span data-ttu-id="6fffa-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6fffa-120">Value</span></span>                                                                        | <span data-ttu-id="6fffa-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6fffa-121">Meaning</span></span>                                  |
|------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="6fffa-122"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6fffa-122"><dt>1</dt></span></span> </dl> | <span data-ttu-id="6fffa-123">Das Zertifikat ist ein DRA-.</span><span class="sxs-lookup"><span data-stu-id="6fffa-123">The certificate is a DRA.</span></span><br/>     |
| <dl> <span data-ttu-id="6fffa-124"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6fffa-124"><dt>2</dt></span></span> </dl> | <span data-ttu-id="6fffa-125">Das Zertifikat ist keine DRA.</span><span class="sxs-lookup"><span data-stu-id="6fffa-125">The certificate is not a DRA.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fffa-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6fffa-126">Return value</span></span>

<span data-ttu-id="6fffa-127">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fffa-127">Type: **uint32**</span></span>

<span data-ttu-id="6fffa-128">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="6fffa-128">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="6fffa-129">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="6fffa-129">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="6fffa-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fffa-130">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6fffa-131"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6fffa-131"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="6fffa-132">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6fffa-132">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="6fffa-133"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="6fffa-133"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                               | <span data-ttu-id="6fffa-134">Die angegebene Schlüssel Schutzvorrichtung ist keine Schlüssel Schutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="6fffa-134">The specified key protector is not a key protector.</span></span> <span data-ttu-id="6fffa-135">Sie müssen eine andere Schlüssel Schutzvorrichtung eingeben.</span><span class="sxs-lookup"><span data-stu-id="6fffa-135">You must enter another key protector.</span></span><br/>            |
| <dl> <span data-ttu-id="6fffa-136"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="6fffa-136"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                      | <span data-ttu-id="6fffa-137">Dieses Laufwerk ist BitLocker-Laufwerkverschlüsselung gesperrt.</span><span class="sxs-lookup"><span data-stu-id="6fffa-137">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="6fffa-138">Dieses Volume muss in der Systemsteuerung entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="6fffa-138">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="6fffa-139"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="6fffa-139"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="6fffa-140">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6fffa-140">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="6fffa-141">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="6fffa-141">Add a key protector to enable BitLocker.</span></span> <br/>                    |
| <dl> <span data-ttu-id="6fffa-142"><dt>**F \_ E \_ - \_ richtlinienbenutzerzertifikat \_ \_ erforderlich**</dt> <dt>2150695027 (0x80310073)</dt></span><span class="sxs-lookup"><span data-stu-id="6fffa-142"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_REQUIRED**</dt> <dt>2150695027 (0x80310073)</dt></span></span> </dl> | <span data-ttu-id="6fffa-143">Gruppenrichtlinie erfordert die Verwendung eines Benutzer Zertifikats, z. b. eine Smartcard.</span><span class="sxs-lookup"><span data-stu-id="6fffa-143">Group Policy requires the use of a user certificate, such as a smart card.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="6fffa-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fffa-144">Remarks</span></span>

<span data-ttu-id="6fffa-145">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="6fffa-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6fffa-146">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="6fffa-146">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="6fffa-147">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6fffa-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6fffa-148">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="6fffa-148">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6fffa-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fffa-149">Requirements</span></span>



| <span data-ttu-id="6fffa-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fffa-150">Requirement</span></span> | <span data-ttu-id="6fffa-151">Wert</span><span class="sxs-lookup"><span data-stu-id="6fffa-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fffa-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6fffa-152">Minimum supported client</span></span><br/> | <span data-ttu-id="6fffa-153">Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6fffa-153">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6fffa-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6fffa-154">Minimum supported server</span></span><br/> | <span data-ttu-id="6fffa-155">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6fffa-155">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6fffa-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="6fffa-156">Namespace</span></span><br/>                | <span data-ttu-id="6fffa-157">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="6fffa-157">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6fffa-158">MOF</span><span class="sxs-lookup"><span data-stu-id="6fffa-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6fffa-159"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6fffa-159"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fffa-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fffa-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fffa-161">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="6fffa-161">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
