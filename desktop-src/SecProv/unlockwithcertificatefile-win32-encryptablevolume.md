---
description: Verwendet die angegebene Zertifikat Datei, um den abgeleiteten Schlüssel abzurufen und das verschlüsselte Volume zu entsperren.
ms.assetid: 41811d38-5c89-4372-9dbc-3de45b05011f
title: Unlockwithcertificatefile-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d7ce1705c0ec457f64eb825e49334e76a14c184c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369015"
---
# <a name="unlockwithcertificatefile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c2620-103">Unlockwithcertificatefile-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="c2620-103">UnlockWithCertificateFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c2620-104">Die **unlockwithcertificatefile** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " verwendet die angegebene [*Zertifikat*](../secgloss/c-gly.md) Datei, um den abgeleiteten Schlüssel abzurufen und das verschlüsselte Volume zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="c2620-104">The **UnlockWithCertificateFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided [*certificate*](../secgloss/c-gly.md) file to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="c2620-105">Wenn die Festplatte Hardware Verschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "entsperrt" fest.</span><span class="sxs-lookup"><span data-stu-id="c2620-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c2620-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2620-106">Syntax</span></span>


```mof
uint32 UnlockWithCertificateFile(
  [in] string FileName,
  [in] string PIN
);
```



## <a name="parameters"></a><span data-ttu-id="c2620-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2620-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2620-108">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2620-108">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2620-109">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2620-109">Type: **string**</span></span>

<span data-ttu-id="c2620-110">Eine Zeichenfolge, die den Speicherort und den Namen der CER-Datei angibt, die zum Abrufen des Zertifikat Fingerabdrucks verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2620-110">A string that specifies the location and name of the .cer file used to retrieve the certificate thumbprint.</span></span> <span data-ttu-id="c2620-111">Ein [*Verschlüsselungs*](../secgloss/e-gly.md) Zertifikat muss im CER-Format ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der)-codiertes binäres [*x. 509*](../secgloss/x-gly.md) -Format oder Base-64-codiertes x. 509-Format exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="c2620-111">An [*encryption*](../secgloss/e-gly.md) certificate must be exported in .cer format ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-encoded binary [*X.509*](../secgloss/x-gly.md) or Base-64 encoded X.509).</span></span> <span data-ttu-id="c2620-112">Das Verschlüsselungs Zertifikat kann von Microsoft PKI, PKI von Drittanbietern oder selbst signiert generiert werden.</span><span class="sxs-lookup"><span data-stu-id="c2620-112">The encryption certificate may be generated from Microsoft PKI, third-party PKI, or self-signed.</span></span>

</dd> <dt>

<span data-ttu-id="c2620-113">*Pin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2620-113">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2620-114">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2620-114">Type: **string**</span></span>

<span data-ttu-id="c2620-115">Eine vom Benutzer angegebene persönliche Identifikations Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c2620-115">A user-specified personal identification string.</span></span> <span data-ttu-id="c2620-116">Diese Zeichenfolge muss aus einer Sequenz von 4 bis 20 Ziffern bestehen.</span><span class="sxs-lookup"><span data-stu-id="c2620-116">This string must consist of a sequence of 4 to 20 digits.</span></span> <span data-ttu-id="c2620-117">Diese Zeichenfolge wird verwendet, um den [*Schlüsselspeicher Anbieter*](../secgloss/k-gly.md) (KSP) im Hintergrund zu authentifizieren, wenn Sie mit einer [*Smartcard*](../secgloss/s-gly.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2620-117">This string is used to silently authenticate the [*key storage provider*](../secgloss/k-gly.md) (KSP) when used with a [*smart card*](../secgloss/s-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2620-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2620-118">Return value</span></span>

<span data-ttu-id="c2620-119">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2620-119">Type: **uint32**</span></span>

<span data-ttu-id="c2620-120">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="c2620-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c2620-121">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="c2620-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="c2620-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2620-122">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2620-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c2620-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="c2620-124">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c2620-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="c2620-125"><dt>**Fehler \_ Datei \_ nicht \_ gefunden**</dt> <dt>0000000002 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="c2620-125"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>0000000002 (0x2)</dt></span></span> </dl>                 | <span data-ttu-id="c2620-126">Das System kann die angegebene Datei nicht ablegen.</span><span class="sxs-lookup"><span data-stu-id="c2620-126">The system cannot file the specified file.</span></span><br/>                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="c2620-127"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="c2620-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="c2620-128">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c2620-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="c2620-129">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="c2620-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="c2620-130"><dt>**F \_ E \_ \_**</dt> -Fehler bei Authentifizierung <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="c2620-130"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>   | <span data-ttu-id="c2620-131">Das Volume kann mit den bereitgestellten Informationen nicht entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="c2620-131">The volume cannot be unlocked with the provided information.</span></span> <br/>                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="c2620-132"><dt>**F \_ E \_ Protector \_ nicht \_ gefunden**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="c2620-132"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="c2620-133">Die angegebene Schlüssel Schutzvorrichtung ist auf dem Volume nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c2620-133">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="c2620-134">Sie müssen eine andere Schlüssel Schutzvorrichtung eingeben.</span><span class="sxs-lookup"><span data-stu-id="c2620-134">You must enter another key protector.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="c2620-135"><dt>**F \_ E \_ PrivateKey-Authentifizierung ist \_ \_ fehlgeschlagen**</dt> <dt>2150695060 (0x80310094)</dt></span><span class="sxs-lookup"><span data-stu-id="c2620-135"><dt>**FVE\_E\_PRIVATEKEY\_AUTH\_FAILED**</dt> <dt>2150695060 (0x80310094)</dt></span></span> </dl> | <span data-ttu-id="c2620-136">Der [*private Schlüssel*](../secgloss/p-gly.md), der dem angegebenen Zertifikat zugeordnet ist, konnte nicht autorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c2620-136">The [*private key*](../secgloss/p-gly.md), associated with the specified certificate, could not be authorized.</span></span> <span data-ttu-id="c2620-137">Die Autorisierung für den privaten Schlüssel wurde entweder nicht bereitgestellt, oder die angegebene Autorisierung war ungültig.</span><span class="sxs-lookup"><span data-stu-id="c2620-137">The private key authorization was either not provided or the provided authorization was invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c2620-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2620-138">Requirements</span></span>



| <span data-ttu-id="c2620-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2620-139">Requirement</span></span> | <span data-ttu-id="c2620-140">Wert</span><span class="sxs-lookup"><span data-stu-id="c2620-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2620-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2620-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c2620-142">Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2620-142">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c2620-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2620-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c2620-144">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2620-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c2620-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2620-145">Namespace</span></span><br/>                | <span data-ttu-id="c2620-146">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="c2620-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c2620-147">MOF</span><span class="sxs-lookup"><span data-stu-id="c2620-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2620-148"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c2620-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2620-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2620-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2620-150">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="c2620-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
