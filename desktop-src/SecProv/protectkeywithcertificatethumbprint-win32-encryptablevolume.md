---
description: Überprüft die EKU-Objekt Kennung (Enhanced Key Usage, EKU) des angegebenen Zertifikats.
ms.assetid: 7096cead-c44a-404c-b1e1-3e0ab27070f8
title: Protectkeywithcertifitorethenumbprint-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: e0b47aabccaacfb3ab81968b8a93037aad304f8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373188"
---
# <a name="protectkeywithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="0aa96-103">Protectkeywithcertifitorethenumbprint-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="0aa96-103">ProtectKeyWithCertificateThumbprint method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="0aa96-104">Die **protectkeywithcertifigateethumbprint** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " überprüft die EKU- [*Objekt Kennung*](../secgloss/o-gly.md) (Enhanced Key Usage, EKU) des bereitgestellten Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="0aa96-104">The **ProtectKeyWithCertificateThumbprint** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class validates the Enhanced Key Usage (EKU) [*object identifier*](../secgloss/o-gly.md) (OID) of the provided certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aa96-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0aa96-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithCertificateThumbprint(
  [in, optional] string FriendlyName,
  [in]           string CertThumbprint,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="0aa96-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0aa96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aa96-107">*FriendlyName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="0aa96-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0aa96-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0aa96-108">Type: **string**</span></span>

<span data-ttu-id="0aa96-109">Eine Zeichenfolge, die einen vom Benutzer zugewiesenen Zeichen folgen Bezeichner für diese Schlüssel Schutzvorrichtung angibt.</span><span class="sxs-lookup"><span data-stu-id="0aa96-109">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="0aa96-110">Wenn dieser Parameter nicht angegeben wird, wird der *FriendlyName* -Parameter mit dem Antragsteller Namen im Zertifikat erstellt.</span><span class="sxs-lookup"><span data-stu-id="0aa96-110">If this parameter is not specified, the *FriendlyName* parameter is created by using the Subject Name in the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="0aa96-111">*Certthumbprint* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0aa96-111">*CertThumbprint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aa96-112">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0aa96-112">Type: **string**</span></span>

<span data-ttu-id="0aa96-113">Eine Zeichenfolge, die den Zertifikat Fingerabdruck angibt.</span><span class="sxs-lookup"><span data-stu-id="0aa96-113">A string that specifies the certificate thumbprint.</span></span>

</dd> <dt>

<span data-ttu-id="0aa96-114">*Volumekeyprotectorid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0aa96-114">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0aa96-115">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0aa96-115">Type: **string**</span></span>

<span data-ttu-id="0aa96-116">Eine Zeichenfolge, die die erstellte Schlüssel Schutzvorrichtung eindeutig identifiziert, die zum Verwalten dieser Schlüssel Schutzvorrichtung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0aa96-116">A string that uniquely identifies the created key protector that can be used to manage this key protector.</span></span>

<span data-ttu-id="0aa96-117">Wenn das Laufwerk die Hardware Verschlüsselung unterstützt und BitLocker keinen bandbesitz hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüssel Schutzvorrichtung wird in die pro-Band-Metadaten geschrieben.</span><span class="sxs-lookup"><span data-stu-id="0aa96-117">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aa96-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0aa96-118">Return value</span></span>

<span data-ttu-id="0aa96-119">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0aa96-119">Type: **uint32**</span></span>

<span data-ttu-id="0aa96-120">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="0aa96-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="0aa96-121">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="0aa96-121">Return code/value</span></span>                                                                                                                                                                                           | <span data-ttu-id="0aa96-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0aa96-122">Description</span></span>                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0aa96-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0aa96-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                           | <span data-ttu-id="0aa96-124">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0aa96-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="0aa96-125"><dt>**Fehler \_ Ungültige \_ Daten**</dt> <dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="0aa96-125"><dt>**ERROR\_INVALID\_DATA**</dt> <dt>13 (0xD)</dt></span></span> </dl>                                           | <span data-ttu-id="0aa96-126">Die Daten sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="0aa96-126">The data is not valid.</span></span><br/>                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="0aa96-127"><dt>**F \_ E \_ nicht- \_ BitLocker- \_ OID**</dt> <dt>2150695022 (0x8031006e)</dt></span><span class="sxs-lookup"><span data-stu-id="0aa96-127"><dt>**FVE\_E\_NON\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl>                     | <span data-ttu-id="0aa96-128">Das EKU-Attribut des angegebenen Zertifikats gestattet es nicht, für BitLocker-Laufwerkverschlüsselung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0aa96-128">The EKU attribute of the specified certificate does not permit it to be used for BitLocker Drive Encryption.</span></span> <span data-ttu-id="0aa96-129">BitLocker erfordert nicht, dass ein Zertifikat ein EKU-Attribut aufweist. Wenn jedoch ein Zertifikat konfiguriert ist, muss es auf eine OID festgelegt werden, die mit der für BitLocker konfigurierten OID übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="0aa96-129">BitLocker does not require that a certificate have an EKU attribute, but if one is configured, it must be set to an OID that matches the OID configured for BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="0aa96-130"><dt>**F \_ E \_ - \_ richtlinienbenutzerzertifikat \_ \_ nicht \_ zulässig**</dt> <dt>2150695026 (0x80310072)</dt></span><span class="sxs-lookup"><span data-stu-id="0aa96-130"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_NOT\_ALLOWED**</dt> <dt>2150695026 (0x80310072)</dt></span></span> </dl> | <span data-ttu-id="0aa96-131">In Gruppenrichtlinie können Benutzerzertifikate, z. b. Smartcards, nicht mit BitLocker verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0aa96-131">Group Policy does not permit user certificates, such as smart cards, to be used with BitLocker.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="0aa96-132"><dt>**F \_ E \_ Policy \_ User \_ CERT \_ muss \_ \_ HW**</dt> <dt>2150695028 (0x80310074)</dt> sein.</span><span class="sxs-lookup"><span data-stu-id="0aa96-132"><dt>**FVE\_E\_POLICY\_USER\_CERT\_MUST\_BE\_HW**</dt> <dt>2150695028 (0x80310074)</dt></span></span> </dl>        | <span data-ttu-id="0aa96-133">Gruppenrichtlinie müssen Sie für die Verwendung von BitLocker eine Smartcard angeben.</span><span class="sxs-lookup"><span data-stu-id="0aa96-133">Group Policy requires that you supply a smart card to use BitLocker.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="0aa96-134"><dt>**F \_ E- \_ Richtlinie \_ untersagt \_ selfsigned**</dt> <dt>2150695046 (0x80310086)</dt></span><span class="sxs-lookup"><span data-stu-id="0aa96-134"><dt>**FVE\_E\_POLICY\_PROHIBITS\_SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span></span> </dl>           | <span data-ttu-id="0aa96-135">Die Verwendung von selbst signierten Zertifikaten wird in Gruppenrichtlinie nicht zugelassen.</span><span class="sxs-lookup"><span data-stu-id="0aa96-135">Group Policy does not permit the use of self-signed certificates.</span></span><br/>                                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="0aa96-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0aa96-136">Remarks</span></span>

<span data-ttu-id="0aa96-137">Wenn die OID nicht mit der ID identisch ist, die dem Dienst Controller in der Registrierung zugeordnet ist, tritt bei dieser Methode ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0aa96-137">If the OID does not match the one associated with the service controller in the registry, this method fails.</span></span> <span data-ttu-id="0aa96-138">Dadurch wird verhindert, dass der Benutzer die Data Recovery Agent-Schutzvorrichtungen (DRA) manuell auf dem Volume festlegt.</span><span class="sxs-lookup"><span data-stu-id="0aa96-138">This prevents the user from setting data recovery agent (DRA) protectors manually on the volume.</span></span> <span data-ttu-id="0aa96-139">DRAs werden nur vom Dienst festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0aa96-139">DRAs are only to be set by the service.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa96-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0aa96-140">Requirements</span></span>



| <span data-ttu-id="0aa96-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0aa96-141">Requirement</span></span> | <span data-ttu-id="0aa96-142">Wert</span><span class="sxs-lookup"><span data-stu-id="0aa96-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa96-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0aa96-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0aa96-144">Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0aa96-144">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0aa96-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0aa96-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0aa96-146">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0aa96-146">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0aa96-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="0aa96-147">Namespace</span></span><br/>                | <span data-ttu-id="0aa96-148">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="0aa96-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="0aa96-149">MOF</span><span class="sxs-lookup"><span data-stu-id="0aa96-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0aa96-150"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0aa96-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aa96-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0aa96-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aa96-152">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="0aa96-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
