---
description: Gibt den Verschlüsselungsalgorithmus und die Schlüsselgröße an, die auf dem Volume verwendet werden.
ms.assetid: 89df3dfc-4789-4d3c-b267-d8e26758e754
title: Getencryptionmethod-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetEncryptionMethod
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 16fb9b00976b652bcc9643ab5ec4912029898424
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352627"
---
# <a name="getencryptionmethod-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c9649-103">Getencryptionmethod-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="c9649-103">GetEncryptionMethod method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c9649-104">Die **getencryptionmethod** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt den Verschlüsselungsalgorithmus und die Schlüsselgröße an, die auf dem Volume verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9649-104">The **GetEncryptionMethod** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the encryption algorithm and key size used on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9649-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9649-105">Syntax</span></span>


```mof
uint32 GetEncryptionMethod(
  [out] uint32 EncryptionMethod,
  [out] string SelfEncryptionDriveEncryptionMethod
);
```



## <a name="parameters"></a><span data-ttu-id="c9649-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9649-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9649-107">*Verschlüsselungsmethode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c9649-107">*EncryptionMethod* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9649-108">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9649-108">Type: **uint32**</span></span>

<span data-ttu-id="c9649-109">Eine ganze Zahl ohne Vorzeichen, die den Verschlüsselungsalgorithmus und die Schlüsselgröße angibt, die auf dem Volume verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9649-109">An unsigned integer that specifies the encryption algorithm and key size used on the volume.</span></span>



| <span data-ttu-id="c9649-110">Wert</span><span class="sxs-lookup"><span data-stu-id="c9649-110">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="c9649-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c9649-111">Meaning</span></span>                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span><dl> <span data-ttu-id="c9649-112"><dt>**Keine**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c9649-112"><dt>**None**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="c9649-113">Das Volume ist nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="c9649-113">The volume is not encrypted.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="AES_128_WITH_DIFFUSER"></span><span id="aes_128_with_diffuser"></span><dl> <span data-ttu-id="c9649-114"><dt>**AES \_ 128 \_ mit \_ diffuser**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c9649-114"><dt>**AES\_128\_WITH\_DIFFUSER**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="c9649-115">Das Volume wurde mithilfe einer AES-Schlüsselgröße von 128 Bits vollständig oder teilweise mit dem Advanced Encryption Standard (AES)-Algorithmus verschlüsselt, der durch eine diffuser-Schicht erweitert wurde.</span><span class="sxs-lookup"><span data-stu-id="c9649-115">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer, using an AES key size of 128 bits.</span></span> <span data-ttu-id="c9649-116">Diese Methode ist nicht mehr auf Geräten verfügbar, auf denen Windows 8.1 oder höher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9649-116">This method is no longer available on devices running Windows 8.1 or higher.</span></span><br/> |
| <span id="AES_256_WITH_DIFFUSER"></span><span id="aes_256_with_diffuser"></span><dl> <span data-ttu-id="c9649-117"><dt>**AES \_ 256 \_ mit \_ diffuser**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c9649-117"><dt>**AES\_256\_WITH\_DIFFUSER**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="c9649-118">Das Volume wurde mithilfe einer AES-Schlüsselgröße von 256 Bits vollständig oder teilweise mit dem Advanced Encryption Standard (AES)-Algorithmus verschlüsselt, der durch eine diffuser-Schicht erweitert wurde.</span><span class="sxs-lookup"><span data-stu-id="c9649-118">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer, using an AES key size of 256 bits.</span></span> <span data-ttu-id="c9649-119">Diese Methode ist nicht mehr auf Geräten verfügbar, auf denen Windows 8.1 oder höher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9649-119">This method is no longer available on devices running Windows 8.1 or higher.</span></span><br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <span data-ttu-id="c9649-120"><dt>**AES \_ 128**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c9649-120"><dt>**AES\_128**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="c9649-121">Das Volume wurde mit dem Advanced Encryption Standard (AES)-Algorithmus vollständig oder teilweise verschlüsselt, wobei eine AES-Schlüsselgröße von 128 Bits verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c9649-121">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm, using an AES key size of 128 bits.</span></span><br/>                                                                                                             |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <span data-ttu-id="c9649-122"><dt>**AES \_ 256**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c9649-122"><dt>**AES\_256**</dt> <dt>4</dt></span></span> </dl>                                             | <span data-ttu-id="c9649-123">Das Volume wurde mit dem Advanced Encryption Standard (AES)-Algorithmus vollständig oder teilweise verschlüsselt, wobei eine AES-Schlüsselgröße von 256 Bits verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c9649-123">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm, using an AES key size of 256 bits.</span></span><br/>                                                                                                             |
| <span id="HARDWARE_ENCRYPTION"></span><span id="hardware_encryption"></span><dl> <span data-ttu-id="c9649-124"><dt>**Hardware \_ Verschlüsselung**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c9649-124"><dt>**HARDWARE\_ENCRYPTION**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="c9649-125">Das Volume wurde mithilfe der Hardwarefunktionen des Laufwerks vollständig oder teilweise verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="c9649-125">The volume has been fully or partially encrypted by using the hardware capabilities of the drive.</span></span><br/>                                                                                                                                                      |
| <span id="XTS_AES_128"></span><span id="xts_aes_128"></span><dl> <span data-ttu-id="c9649-126"><dt>**XTS \_ AES \_ 128**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c9649-126"><dt>**XTS\_AES\_128**</dt> <dt>6</dt></span></span> </dl>                                | <span data-ttu-id="c9649-127">Das Volume wurde mit XTS vollständig oder teilweise verschlüsselt, wobei die Advanced Encryption Standard (AES) und eine AES-Schlüsselgröße von 128 Bits verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9649-127">The volume has been fully or partially encrypted with XTS using the Advanced Encryption Standard (AES), and an AES key size of 128 bits.</span></span> <span data-ttu-id="c9649-128">Diese Methode ist nur auf Geräten verfügbar, auf denen Windows 10, Version 1511 oder höher, ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9649-128">This method is only available on devices running Windows 10, version 1511 or higher.</span></span><br/>                          |
| <span id="XTS_AES_256"></span><span id="xts_aes_256"></span><dl> <span data-ttu-id="c9649-129"><dt>**XTS \_ AES \_ 256**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c9649-129"><dt>**XTS\_AES\_256**</dt> <dt>7</dt></span></span> </dl>                                | <span data-ttu-id="c9649-130">Das Volume wurde mit XTS vollständig oder teilweise verschlüsselt, wobei die Advanced Encryption Standard (AES) und eine AES-Schlüsselgröße von 256 Bits verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9649-130">The volume has been fully or partially encrypted with XTS using the Advanced Encryption Standard (AES), and an AES key size of 256 bits.</span></span> <span data-ttu-id="c9649-131">Diese Methode ist nur auf Geräten verfügbar, auf denen Windows 10, Version 1511 oder höher, ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9649-131">This method is only available on devices running Windows 10, version 1511 or higher.</span></span><br/>                          |
| <dl> <span data-ttu-id="c9649-132"><dt>(UInt32) – 1</dt></span><span class="sxs-lookup"><span data-stu-id="c9649-132"><dt>(uint32)–1</dt></span></span> </dl>                                                                                                                                                          | <span data-ttu-id="c9649-133">UNBEKANNT</span><span class="sxs-lookup"><span data-stu-id="c9649-133">UNKNOWN</span></span><br/> <span data-ttu-id="c9649-134">Das Volume wurde vollständig oder teilweise mit einem unbekannten Algorithmus und Schlüsselgröße verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="c9649-134">The volume has been fully or partially encrypted with an unknown algorithm and key size.</span></span><br/>                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="c9649-135">*Selfencryptiondriveverschlüsseltionmethod* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c9649-135">*SelfEncryptionDriveEncryptionMethod* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9649-136">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c9649-136">Type: **string**</span></span>

<span data-ttu-id="c9649-137">Der Verschlüsselungsalgorithmus wird auf dem selbst verschlüsselnden Laufwerk konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c9649-137">The encryption algorithm is configured on the self-encrypting drive.</span></span> <span data-ttu-id="c9649-138">Eine NULL-Zeichenfolge bedeutet, dass entweder BitLocker Software Verschlüsselung verwendet oder keine Verschlüsselungsmethode gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="c9649-138">A null string means that either BitLocker is using software encryption or no encryption method is reported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9649-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9649-139">Return value</span></span>

<span data-ttu-id="c9649-140">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9649-140">Type: **uint32**</span></span>

<span data-ttu-id="c9649-141">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="c9649-141">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c9649-142">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="c9649-142">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="c9649-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9649-143">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="c9649-144"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c9649-144"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="c9649-145">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c9649-145">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c9649-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9649-146">Remarks</span></span>

<span data-ttu-id="c9649-147">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="c9649-147">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c9649-148">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="c9649-148">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c9649-149">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c9649-149">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c9649-150">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c9649-150">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9649-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9649-151">Requirements</span></span>



| <span data-ttu-id="c9649-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9649-152">Requirement</span></span> | <span data-ttu-id="c9649-153">Wert</span><span class="sxs-lookup"><span data-stu-id="c9649-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9649-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9649-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c9649-155">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9649-155">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c9649-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9649-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c9649-157">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9649-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c9649-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9649-158">Namespace</span></span><br/>                | <span data-ttu-id="c9649-159">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="c9649-159">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c9649-160">MOF</span><span class="sxs-lookup"><span data-stu-id="c9649-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9649-161"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c9649-161"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9649-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9649-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9649-163">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="c9649-163">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
