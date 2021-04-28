---
description: 'ProtectKeyWithCertificateFile-Methode der Win32_EncryptableVolume-Klasse: Überprüft den OID (Enhanced Key Usage)-Objektbezeichner (Enhanced Key Usage, erweiterte Schlüsselverwendung) des bereitgestellten Zertifikats.'
ms.assetid: cc716524-f976-4d75-84f3-693e277030e6
title: ProtectKeyWithCertificateFile-Methode der Win32_EncryptableVolume Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d61a0bd0d31c14f13edd9ef610e8f6d3ed20f037
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110563"
---
# <a name="protectkeywithcertificatefile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="1687a-103">ProtectKeyWithCertificateFile-Methode der Win32 \_ EncryptableVolume-Klasse</span><span class="sxs-lookup"><span data-stu-id="1687a-103">ProtectKeyWithCertificateFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="1687a-104">Die **ProtectKeyWithCertificateFile-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) überprüft den EKU-Objektbezeichner [*(Enhanced*](../secgloss/o-gly.md) Key Usage) des bereitgestellten Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="1687a-104">The **ProtectKeyWithCertificateFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class validates the Enhanced Key Usage (EKU) [*object identifier*](../secgloss/o-gly.md) (OID) of the provided certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="1687a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1687a-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithCertificateFile(
  [in, optional] string FriendlyName,
  [in]           string FileName,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="1687a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1687a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1687a-107">*FriendlyName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1687a-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1687a-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1687a-108">Type: **string**</span></span>

<span data-ttu-id="1687a-109">Eine Zeichenfolge, die einen vom Benutzer zugewiesenen Zeichenfolgenbezeichner für diese Schlüsselschutzvorrichtung angibt.</span><span class="sxs-lookup"><span data-stu-id="1687a-109">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="1687a-110">Wenn dieser Parameter nicht angegeben wird, wird *der FriendlyName-Parameter* mithilfe des Betreffnamens im Zertifikat erstellt.</span><span class="sxs-lookup"><span data-stu-id="1687a-110">If this parameter is not specified, the *FriendlyName* parameter is created by using the Subject Name in the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="1687a-111">*FileName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1687a-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1687a-112">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1687a-112">Type: **string**</span></span>

<span data-ttu-id="1687a-113">Eine Zeichenfolge, die den Speicherort und den Namen der CER-Datei angibt, die zum Aktivieren von BitLocker verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1687a-113">A string that specifies the location and name of the .cer file used to enable BitLocker.</span></span> <span data-ttu-id="1687a-114">Ein Verschlüsselungszertifikat muss im CER-Format exportiert werden ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-codierte binäre [*X.509-*](../secgloss/x-gly.md) oder Base-64-codierte X.509).</span><span class="sxs-lookup"><span data-stu-id="1687a-114">An encryption certificate must be exported in .cer format ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-encoded binary [*X.509*](../secgloss/x-gly.md) or Base-64 encoded X.509).</span></span> <span data-ttu-id="1687a-115">Das Verschlüsselungszertifikat kann von Microsoft PKI, PKI eines Drittanbieters oder selbstsigniertem Zertifikat generiert werden.</span><span class="sxs-lookup"><span data-stu-id="1687a-115">The encryption certificate may be generated from Microsoft PKI, third-party PKI, or self-signed.</span></span>

</dd> <dt>

<span data-ttu-id="1687a-116">*VolumeKeyProtectorID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1687a-116">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1687a-117">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1687a-117">Type: **string**</span></span>

<span data-ttu-id="1687a-118">Eine Zeichenfolge, die die erstellte Schlüsselschutzvorrichtung eindeutig identifiziert, die zum Verwalten dieser Schlüsselschutzvorrichtung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1687a-118">A string that uniquely identifies the created key protector that can be used to manage this key protector.</span></span>

<span data-ttu-id="1687a-119">Wenn das Laufwerk hardwareverschlüsselung unterstützt und BitLocker keinen Bandbesitz übernommen hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüsselschutzvorrichtung wird in die Metadaten pro Band geschrieben.</span><span class="sxs-lookup"><span data-stu-id="1687a-119">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1687a-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1687a-120">Return value</span></span>

<span data-ttu-id="1687a-121">Typ: **uint32**</span><span class="sxs-lookup"><span data-stu-id="1687a-121">Type: **uint32**</span></span>

<span data-ttu-id="1687a-122">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="1687a-122">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="1687a-123">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="1687a-123">Return code/value</span></span>                                                                                                                                                                                           | <span data-ttu-id="1687a-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1687a-124">Description</span></span>                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1687a-125"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1687a-125"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                           | <span data-ttu-id="1687a-126">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1687a-126">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="1687a-127"><dt>**FVE \_ E \_ NON \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="1687a-127"><dt>**FVE\_E\_NON\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl>                     | <span data-ttu-id="1687a-128">Das EKU-Attribut des angegebenen Zertifikats lässt nicht zu, dass es für BitLocker-Laufwerkverschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1687a-128">The EKU attribute of the specified certificate does not permit it to be used for BitLocker Drive Encryption.</span></span> <span data-ttu-id="1687a-129">BitLocker erfordert nicht, dass ein Zertifikat über ein EKU-Attribut verfügt, aber wenn eines konfiguriert ist, muss es auf eine OID festgelegt werden, die der für BitLocker konfigurierten OID entspricht.</span><span class="sxs-lookup"><span data-stu-id="1687a-129">BitLocker does not require that a certificate have an EKU attribute, but if one is configured, it must be set to an OID that matches the OID configured for BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="1687a-130"><dt>**FVE \_ E \_ POLICY USER CERTIFICATE NOT ALLOWED \_ \_ \_ \_**</dt> <dt>2150695026 (E POLICY USER CERTIFICATE NOT ALLOWED 2150695026 (E POLICY USER CERTIFICATE NOT ALLOWED 2150695026 (0X80310072))</dt></span><span class="sxs-lookup"><span data-stu-id="1687a-130"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_NOT\_ALLOWED**</dt> <dt>2150695026 (0x80310072)</dt></span></span> </dl> | <span data-ttu-id="1687a-131">Gruppenrichtlinie lässt nicht zu, dass Benutzerzertifikate wie Smartcards mit BitLocker verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1687a-131">Group Policy does not permit user certificates, such as smart cards, to be used with BitLocker.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="1687a-132"><dt>**FVE \_ E \_ POLICY \_ USER \_ CERT MUST BE \_ \_ \_ HW**</dt> <dt>2150695028 (0x80310074)</dt></span><span class="sxs-lookup"><span data-stu-id="1687a-132"><dt>**FVE\_E\_POLICY\_USER\_CERT\_MUST\_BE\_HW**</dt> <dt>2150695028 (0x80310074)</dt></span></span> </dl>        | <span data-ttu-id="1687a-133">Gruppenrichtlinie erfordert, dass Sie eine Smartcard für die Verwendung von BitLocker bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1687a-133">Group Policy requires that you supply a smart card to use BitLocker.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="1687a-134"><dt>**FVE \_ E \_ POLICY \_ PROHIBITS \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span><span class="sxs-lookup"><span data-stu-id="1687a-134"><dt>**FVE\_E\_POLICY\_PROHIBITS\_SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span></span> </dl>           | <span data-ttu-id="1687a-135">Gruppenrichtlinie lässt die Verwendung von selbstsignieren Zertifikaten nicht zu.</span><span class="sxs-lookup"><span data-stu-id="1687a-135">Group Policy does not permit the use of self-signed certificates.</span></span><br/>                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="1687a-136"><dt>**FEHLER \_ DATEI \_ NICHT \_ GEFUNDEN**</dt> <dt>00000000002 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="1687a-136"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>0000000002 (0x2)</dt></span></span> </dl>                                | <span data-ttu-id="1687a-137">Das System kann die angegebene Datei nicht finden.</span><span class="sxs-lookup"><span data-stu-id="1687a-137">The system cannot find the specified file.</span></span><br/>                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="1687a-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1687a-138">Remarks</span></span>

<span data-ttu-id="1687a-139">Wenn die OID nicht mit der OID übereinstimmt, die dem Dienstcontroller in der Registrierung zugeordnet ist, schlägt diese Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="1687a-139">If the OID does not match the one associated with the service controller in the registry, this method fails.</span></span> <span data-ttu-id="1687a-140">Dadurch wird verhindert, dass der Benutzer Schutzvorrichtungen für den Datenwiederherstellungs-Agent (Data Recovery Agent, DRA) manuell auf dem Volume festlegt.</span><span class="sxs-lookup"><span data-stu-id="1687a-140">This prevents the user from setting data recovery agent (DRA) protectors manually on the volume.</span></span> <span data-ttu-id="1687a-141">DRAs müssen nur vom Dienst festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1687a-141">DRAs are only to be set by the service.</span></span>

## <a name="requirements"></a><span data-ttu-id="1687a-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1687a-142">Requirements</span></span>



| <span data-ttu-id="1687a-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1687a-143">Requirement</span></span> | <span data-ttu-id="1687a-144">Wert</span><span class="sxs-lookup"><span data-stu-id="1687a-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1687a-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1687a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1687a-146">Nur Windows 7 Enterprise- und Windows 7 \[ Ultimate-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1687a-146">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1687a-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1687a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1687a-148">Nur Windows Server 2008 \[ R2-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1687a-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1687a-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="1687a-149">Namespace</span></span><br/>                | <span data-ttu-id="1687a-150">Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="1687a-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="1687a-151">MOF</span><span class="sxs-lookup"><span data-stu-id="1687a-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1687a-152"><dt>Win32 \_ encryptablevolume.mof</dt></span><span class="sxs-lookup"><span data-stu-id="1687a-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1687a-153">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1687a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1687a-154">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="1687a-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
