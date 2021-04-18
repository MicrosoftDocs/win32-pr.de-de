---
description: Gibt den Typ einer angegebenen Schlüssel Schutzvorrichtung an.
ms.assetid: 17cdde18-3979-4a19-b36e-aa71994148c9
title: Getkeyprotectortype-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorType
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 483394f2e1c80f97442a9e6758f604093d513c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529786"
---
# <a name="getkeyprotectortype-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="427b5-103">Getkeyprotectortype-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="427b5-103">GetKeyProtectorType method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="427b5-104">Die **getkeyprotectortype** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt den Typ einer angegebenen Schlüssel Schutzvorrichtung an.</span><span class="sxs-lookup"><span data-stu-id="427b5-104">The **GetKeyProtectorType** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the type of a given key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="427b5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="427b5-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorType(
  [in]  string VolumeKeyProtectorID,
  [out] uint32 KeyProtectorType
);
```



## <a name="parameters"></a><span data-ttu-id="427b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="427b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="427b5-107">*Volumekeyprotectorid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="427b5-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="427b5-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="427b5-108">Type: **string**</span></span>

<span data-ttu-id="427b5-109">Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="427b5-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="427b5-110">*Keyprotector Type* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="427b5-110">*KeyProtectorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="427b5-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="427b5-111">Type: **uint32**</span></span>

<span data-ttu-id="427b5-112">Eine ganze Zahl ohne Vorzeichen, die den Typ der Schlüssel Schutzvorrichtung angibt.</span><span class="sxs-lookup"><span data-stu-id="427b5-112">An unsigned integer that specifies the type of the key protector.</span></span>



| <span data-ttu-id="427b5-113">Wert</span><span class="sxs-lookup"><span data-stu-id="427b5-113">Value</span></span>                                                                         | <span data-ttu-id="427b5-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="427b5-114">Meaning</span></span>                                              |
|-------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="427b5-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="427b5-115"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="427b5-116">Unbekannter oder anderer schutzvorrichtungstyp</span><span class="sxs-lookup"><span data-stu-id="427b5-116">Unknown or other protector type</span></span><br/>           |
| <dl> <span data-ttu-id="427b5-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="427b5-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="427b5-118">Trusted Platform Module (TPM)</span><span class="sxs-lookup"><span data-stu-id="427b5-118">Trusted Platform Module (TPM)</span></span><br/>             |
| <dl> <span data-ttu-id="427b5-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="427b5-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="427b5-120">Externer Schlüssel</span><span class="sxs-lookup"><span data-stu-id="427b5-120">External key</span></span><br/>                              |
| <dl> <span data-ttu-id="427b5-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="427b5-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="427b5-122">Numerisches Kennwort</span><span class="sxs-lookup"><span data-stu-id="427b5-122">Numerical password</span></span><br/>                        |
| <dl> <span data-ttu-id="427b5-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="427b5-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="427b5-124">TPM und PIN</span><span class="sxs-lookup"><span data-stu-id="427b5-124">TPM And PIN</span></span><br/>                               |
| <dl> <span data-ttu-id="427b5-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="427b5-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="427b5-126">TPM-und Systemstart Schlüssel</span><span class="sxs-lookup"><span data-stu-id="427b5-126">TPM And Startup Key</span></span><br/>                       |
| <dl> <span data-ttu-id="427b5-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="427b5-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="427b5-128">TPM-und PIN-und Systemstart Schlüssel</span><span class="sxs-lookup"><span data-stu-id="427b5-128">TPM And PIN And Startup Key</span></span><br/>               |
| <dl> <span data-ttu-id="427b5-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="427b5-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="427b5-130">Öffentlicher Schlüssel</span><span class="sxs-lookup"><span data-stu-id="427b5-130">Public Key</span></span><br/>                                |
| <dl> <span data-ttu-id="427b5-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="427b5-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="427b5-132">Passphrase</span><span class="sxs-lookup"><span data-stu-id="427b5-132">Passphrase</span></span><br/>                                |
| <dl> <span data-ttu-id="427b5-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="427b5-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="427b5-134">TPM-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="427b5-134">TPM Certificate</span></span><br/>                           |
| <dl> <span data-ttu-id="427b5-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="427b5-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="427b5-136">CryptoAPI Next Generation (CNG) Protector</span><span class="sxs-lookup"><span data-stu-id="427b5-136">CryptoAPI Next Generation (CNG) Protector</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="427b5-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="427b5-137">Return value</span></span>

<span data-ttu-id="427b5-138">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="427b5-138">Type: **uint32**</span></span>

<span data-ttu-id="427b5-139">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="427b5-139">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="427b5-140">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="427b5-140">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="427b5-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="427b5-141">Description</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="427b5-142"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="427b5-142"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="427b5-143">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="427b5-143">The method was successful.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="427b5-144"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="427b5-144"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="427b5-145">Der *volumekeyprotectorid-* Parameter verweist nicht auf einen gültigen *keyprotectortype*.</span><span class="sxs-lookup"><span data-stu-id="427b5-145">The *VolumeKeyProtectorID* parameter does not refer to a valid *KeyProtectorType*.</span></span><br/> |
| <dl> <span data-ttu-id="427b5-146"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="427b5-146"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="427b5-147">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="427b5-147">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="427b5-148">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="427b5-148">Add a key protector to enable BitLocker.</span></span> <br/>  |



 

## <a name="remarks"></a><span data-ttu-id="427b5-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="427b5-149">Remarks</span></span>

<span data-ttu-id="427b5-150">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="427b5-150">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="427b5-151">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="427b5-151">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="427b5-152">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="427b5-152">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="427b5-153">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="427b5-153">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="427b5-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="427b5-154">Requirements</span></span>



| <span data-ttu-id="427b5-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="427b5-155">Requirement</span></span> | <span data-ttu-id="427b5-156">Wert</span><span class="sxs-lookup"><span data-stu-id="427b5-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="427b5-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="427b5-157">Minimum supported client</span></span><br/> | <span data-ttu-id="427b5-158">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="427b5-158">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="427b5-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="427b5-159">Minimum supported server</span></span><br/> | <span data-ttu-id="427b5-160">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="427b5-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="427b5-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="427b5-161">Namespace</span></span><br/>                | <span data-ttu-id="427b5-162">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="427b5-162">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="427b5-163">MOF</span><span class="sxs-lookup"><span data-stu-id="427b5-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="427b5-164"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="427b5-164"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="427b5-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="427b5-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="427b5-166">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="427b5-166">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
