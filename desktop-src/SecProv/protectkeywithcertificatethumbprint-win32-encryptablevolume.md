---
description: 'ProtectKeyWithCertificateThumbprint-Methode der Win32_EncryptableVolume-Klasse: Überprüft den EKU-Objektbezeichner (Enhanced Key Usage, erweiterte Schlüsselverwendung) des bereitgestellten Zertifikats.'
ms.assetid: 7096cead-c44a-404c-b1e1-3e0ab27070f8
title: ProtectKeyWithCertificateThumbprint-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 8c71684bf66d8d14df60c9ff09083f507b114024
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110578"
---
# <a name="protectkeywithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="bd2af-103">ProtectKeyWithCertificateThumbprint-Methode der Win32 \_ EncryptableVolume-Klasse</span><span class="sxs-lookup"><span data-stu-id="bd2af-103">ProtectKeyWithCertificateThumbprint method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="bd2af-104">Die **ProtectKeyWithCertificateThumbprint-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) überprüft den EKU-Objektbezeichner (Enhanced Key Usage, erweiterte Schlüsselverwendung) des bereitgestellten Zertifikats. [](../secgloss/o-gly.md)</span><span class="sxs-lookup"><span data-stu-id="bd2af-104">The **ProtectKeyWithCertificateThumbprint** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class validates the Enhanced Key Usage (EKU) [*object identifier*](../secgloss/o-gly.md) (OID) of the provided certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd2af-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd2af-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithCertificateThumbprint(
  [in, optional] string FriendlyName,
  [in]           string CertThumbprint,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="bd2af-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd2af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd2af-107">*FriendlyName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="bd2af-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd2af-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bd2af-108">Type: **string**</span></span>

<span data-ttu-id="bd2af-109">Eine Zeichenfolge, die einen vom Benutzer zugewiesenen Zeichenfolgenbezeichner für diese Schlüsselschutzvorrichtung angibt.</span><span class="sxs-lookup"><span data-stu-id="bd2af-109">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="bd2af-110">Wenn dieser Parameter nicht angegeben ist, wird der *FriendlyName-Parameter* mithilfe des Antragstellernamens im Zertifikat erstellt.</span><span class="sxs-lookup"><span data-stu-id="bd2af-110">If this parameter is not specified, the *FriendlyName* parameter is created by using the Subject Name in the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="bd2af-111">*CertThumbprint* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bd2af-111">*CertThumbprint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd2af-112">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bd2af-112">Type: **string**</span></span>

<span data-ttu-id="bd2af-113">Eine Zeichenfolge, die den Zertifikatfingerabdruck angibt.</span><span class="sxs-lookup"><span data-stu-id="bd2af-113">A string that specifies the certificate thumbprint.</span></span>

</dd> <dt>

<span data-ttu-id="bd2af-114">*VolumeKeyProtectorID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bd2af-114">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd2af-115">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bd2af-115">Type: **string**</span></span>

<span data-ttu-id="bd2af-116">Eine Zeichenfolge, die die erstellte Schlüsselschutzvorrichtung eindeutig identifiziert, die zum Verwalten dieser Schlüsselschutzvorrichtung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="bd2af-116">A string that uniquely identifies the created key protector that can be used to manage this key protector.</span></span>

<span data-ttu-id="bd2af-117">Wenn das Laufwerk Hardwareverschlüsselung unterstützt und BitLocker keinen Bandbesitz übernommen hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüsselschutzvorrichtung wird pro Bandmetadaten in geschrieben.</span><span class="sxs-lookup"><span data-stu-id="bd2af-117">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd2af-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd2af-118">Return value</span></span>

<span data-ttu-id="bd2af-119">Typ: **uint32**</span><span class="sxs-lookup"><span data-stu-id="bd2af-119">Type: **uint32**</span></span>

<span data-ttu-id="bd2af-120">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="bd2af-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="bd2af-121">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="bd2af-121">Return code/value</span></span>                                                                                                                                                                                           | <span data-ttu-id="bd2af-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd2af-122">Description</span></span>                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bd2af-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bd2af-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                           | <span data-ttu-id="bd2af-124">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="bd2af-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="bd2af-125"><dt>**FEHLER \_ INVALID \_ DATA**</dt> <dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="bd2af-125"><dt>**ERROR\_INVALID\_DATA**</dt> <dt>13 (0xD)</dt></span></span> </dl>                                           | <span data-ttu-id="bd2af-126">Die Daten sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="bd2af-126">The data is not valid.</span></span><br/>                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="bd2af-127"><dt>**FVE \_ E \_ NON \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="bd2af-127"><dt>**FVE\_E\_NON\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl>                     | <span data-ttu-id="bd2af-128">Das EKU-Attribut des angegebenen Zertifikats lässt nicht zu, dass es für die BitLocker-Laufwerkverschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="bd2af-128">The EKU attribute of the specified certificate does not permit it to be used for BitLocker Drive Encryption.</span></span> <span data-ttu-id="bd2af-129">BitLocker erfordert nicht, dass ein Zertifikat über ein EKU-Attribut verfügt, aber wenn eines konfiguriert ist, muss es auf eine OID festgelegt werden, die der für BitLocker konfigurierten OID entspricht.</span><span class="sxs-lookup"><span data-stu-id="bd2af-129">BitLocker does not require that a certificate have an EKU attribute, but if one is configured, it must be set to an OID that matches the OID configured for BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="bd2af-130"><dt>**FVE \_ E \_ POLICY USER CERTIFICATE NOT ALLOWED \_ \_ \_ \_**</dt> <dt>2150695026 (0x80310072) (E POLICY USER CERTIFICATE NOT ALLOWED 2150695026 (0x80310072)</dt></span><span class="sxs-lookup"><span data-stu-id="bd2af-130"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_NOT\_ALLOWED**</dt> <dt>2150695026 (0x80310072)</dt></span></span> </dl> | <span data-ttu-id="bd2af-131">Gruppenrichtlinie lässt nicht zu, dass Benutzerzertifikate, z. B. Smartcards, mit BitLocker verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="bd2af-131">Group Policy does not permit user certificates, such as smart cards, to be used with BitLocker.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="bd2af-132"><dt>**FVE \_ E \_ POLICY \_ USER \_ CERT MUSS \_ \_ \_ HW**</dt> <dt>2150695028 (0x80310074) SEIN.</dt></span><span class="sxs-lookup"><span data-stu-id="bd2af-132"><dt>**FVE\_E\_POLICY\_USER\_CERT\_MUST\_BE\_HW**</dt> <dt>2150695028 (0x80310074)</dt></span></span> </dl>        | <span data-ttu-id="bd2af-133">Gruppenrichtlinie müssen Sie eine Smartcard für die Verwendung von BitLocker verwenden.</span><span class="sxs-lookup"><span data-stu-id="bd2af-133">Group Policy requires that you supply a smart card to use BitLocker.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="bd2af-134"><dt>**FVE \_ E \_ POLICY VERHINDERT DIE \_ \_ SELBSTSIGNIERTE**</dt> <dt>2150695046 (0x80310086)</dt></span><span class="sxs-lookup"><span data-stu-id="bd2af-134"><dt>**FVE\_E\_POLICY\_PROHIBITS\_SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span></span> </dl>           | <span data-ttu-id="bd2af-135">Gruppenrichtlinie nicht die Verwendung selbstsignierter Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="bd2af-135">Group Policy does not permit the use of self-signed certificates.</span></span><br/>                                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="bd2af-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd2af-136">Remarks</span></span>

<span data-ttu-id="bd2af-137">Wenn die OID nicht mit der OID übereinstimmen, die dem Dienstcontroller in der Registrierung zugeordnet ist, schlägt diese Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="bd2af-137">If the OID does not match the one associated with the service controller in the registry, this method fails.</span></span> <span data-ttu-id="bd2af-138">Dadurch wird verhindert, dass der Benutzer Schutzvorrichtungen des Datenwiederherstellungs-Agents (DRA) manuell auf dem Volume festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="bd2af-138">This prevents the user from setting data recovery agent (DRA) protectors manually on the volume.</span></span> <span data-ttu-id="bd2af-139">DRAs müssen nur vom Dienst festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bd2af-139">DRAs are only to be set by the service.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd2af-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd2af-140">Requirements</span></span>



| <span data-ttu-id="bd2af-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd2af-141">Requirement</span></span> | <span data-ttu-id="bd2af-142">Wert</span><span class="sxs-lookup"><span data-stu-id="bd2af-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd2af-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd2af-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bd2af-144">Nur Windows 7 Enterprise- und Windows 7 \[ Ultimate-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd2af-144">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bd2af-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd2af-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bd2af-146">Nur Windows Server 2008 \[ R2-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd2af-146">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bd2af-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="bd2af-147">Namespace</span></span><br/>                | <span data-ttu-id="bd2af-148">\\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="bd2af-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="bd2af-149">MOF</span><span class="sxs-lookup"><span data-stu-id="bd2af-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd2af-150"><dt>Win32 \_ encryptablevolume.mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd2af-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd2af-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bd2af-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd2af-152">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="bd2af-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
