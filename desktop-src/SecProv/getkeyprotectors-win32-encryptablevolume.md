---
description: Listet die Schutzvorrichtungen auf, mit denen der Verschlüsselungsschlüssel des Volumes geschützt wird.
ms.assetid: ea88f128-c835-49e3-a395-c5ba472fff4b
title: Getkeyprotector-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3a7d6a4110953d905b10eb4f7ef9a255af77897a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353036"
---
# <a name="getkeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="8b90b-103">Getkeyprotector-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="8b90b-103">GetKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="8b90b-104">Die **getkeyprotector** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " listet die Schutzvorrichtungen auf, mit denen der Verschlüsselungsschlüssel des Volumes geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="8b90b-104">The **GetKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class lists the protectors used to secure the volume's encryption key.</span></span> <span data-ttu-id="8b90b-105">Wenn ein schutzschutztyp bereitgestellt wird, werden nur volumeschlüsselschutzvorrichtungen des angegebenen Typs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8b90b-105">If a protector type is provided, then only volume key protectors of the specified type are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b90b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b90b-106">Syntax</span></span>


```mof
uint32 GetKeyProtectors(
  [in, optional] uint32 KeyProtectorType,
  [out]          string VolumeKeyProtectorID[]
);
```



## <a name="parameters"></a><span data-ttu-id="8b90b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b90b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b90b-108">*Keyprotector Type* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8b90b-108">*KeyProtectorType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b90b-109">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b90b-109">Type: **uint32**</span></span>

<span data-ttu-id="8b90b-110">Eine ganze Zahl ohne Vorzeichen, die den Typ der zurück zugebende Schlüssel Schutzvorrichtung angibt.</span><span class="sxs-lookup"><span data-stu-id="8b90b-110">An unsigned integer that specifies the type of key protector to return.</span></span>

<span data-ttu-id="8b90b-111">Wenn dieser Parameter nicht angegeben wird, werden alle verfügbaren Schlüssel Schutzvorrichtungen des Volumes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8b90b-111">If this parameter is not specified, all available key protectors of the volume are returned.</span></span>



| <span data-ttu-id="8b90b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="8b90b-112">Value</span></span>                                                                         | <span data-ttu-id="8b90b-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8b90b-113">Meaning</span></span>                                                           |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="8b90b-114"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8b90b-114"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="8b90b-115">Alle Typen.</span><span class="sxs-lookup"><span data-stu-id="8b90b-115">All types.</span></span><br/> <span data-ttu-id="8b90b-116">Alle Schlüssel Schutzvorrichtungen werden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8b90b-116">All key protectors are returned.</span></span><br/> |
| <dl> <span data-ttu-id="8b90b-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8b90b-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="8b90b-118">Trusted Platform Module (TPM).</span><span class="sxs-lookup"><span data-stu-id="8b90b-118">Trusted Platform Module (TPM).</span></span><br/>                         |
| <dl> <span data-ttu-id="8b90b-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8b90b-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="8b90b-120">Externer Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="8b90b-120">External key.</span></span><br/>                                          |
| <dl> <span data-ttu-id="8b90b-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8b90b-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="8b90b-122">Numerisches Kennwort.</span><span class="sxs-lookup"><span data-stu-id="8b90b-122">Numeric password.</span></span><br/>                                      |
| <dl> <span data-ttu-id="8b90b-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8b90b-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="8b90b-124">TPM und PIN.</span><span class="sxs-lookup"><span data-stu-id="8b90b-124">TPM And PIN.</span></span><br/>                                           |
| <dl> <span data-ttu-id="8b90b-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="8b90b-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="8b90b-126">TPM-und Systemstart Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="8b90b-126">TPM And Startup Key.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8b90b-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="8b90b-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="8b90b-128">TPM-und PIN-und Systemstart Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="8b90b-128">TPM And PIN And Startup Key.</span></span><br/>                           |
| <dl> <span data-ttu-id="8b90b-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="8b90b-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="8b90b-130">Öffentlicher Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="8b90b-130">Public Key.</span></span><br/>                                            |
| <dl> <span data-ttu-id="8b90b-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="8b90b-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="8b90b-132">Passphrase.</span><span class="sxs-lookup"><span data-stu-id="8b90b-132">Passphrase.</span></span><br/>                                            |
| <dl> <span data-ttu-id="8b90b-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="8b90b-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="8b90b-134">TPM-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="8b90b-134">TPM Certificate</span></span><br/>                                        |
| <dl> <span data-ttu-id="8b90b-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="8b90b-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="8b90b-136">Sicherheits-ID (SID)</span><span class="sxs-lookup"><span data-stu-id="8b90b-136">Security Identifier (SID)</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="8b90b-137">*Volumekeyprotectorid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8b90b-137">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b90b-138">Typ: **Zeichen \[ \] Folge**</span><span class="sxs-lookup"><span data-stu-id="8b90b-138">Type: **string\[\]**</span></span>

<span data-ttu-id="8b90b-139">Ein Array von Zeichen folgen, die die zum Schutz des Verschlüsselungsschlüssels des Volumes verwendeten Schlüssel Schutzvorrichtungen identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8b90b-139">An array of strings that identify the key protectors used to secure the volume's encryption key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b90b-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b90b-140">Return value</span></span>

<span data-ttu-id="8b90b-141">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b90b-141">Type: **uint32**</span></span>

<span data-ttu-id="8b90b-142">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="8b90b-142">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="8b90b-143">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="8b90b-143">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="8b90b-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b90b-144">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8b90b-145"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8b90b-145"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="8b90b-146">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8b90b-146">The method was successful.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="8b90b-147"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="8b90b-147"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="8b90b-148">Der *volumekeyprotectorid-* Parameter ist angegeben, verweist jedoch nicht auf einen gültigen *keyprotectortype*.</span><span class="sxs-lookup"><span data-stu-id="8b90b-148">The *VolumeKeyProtectorID* parameter is specified but does not refer to a valid *KeyProtectorType*.</span></span><br/> |
| <dl> <span data-ttu-id="8b90b-149"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="8b90b-149"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="8b90b-150">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8b90b-150">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="8b90b-151">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="8b90b-151">Add a key protector to enable BitLocker.</span></span> <br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="8b90b-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b90b-152">Remarks</span></span>

<span data-ttu-id="8b90b-153">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="8b90b-153">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8b90b-154">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="8b90b-154">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="8b90b-155">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8b90b-155">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8b90b-156">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="8b90b-156">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b90b-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b90b-157">Requirements</span></span>



| <span data-ttu-id="8b90b-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b90b-158">Requirement</span></span> | <span data-ttu-id="8b90b-159">Wert</span><span class="sxs-lookup"><span data-stu-id="8b90b-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b90b-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b90b-160">Minimum supported client</span></span><br/> | <span data-ttu-id="8b90b-161">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b90b-161">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8b90b-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b90b-162">Minimum supported server</span></span><br/> | <span data-ttu-id="8b90b-163">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b90b-163">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8b90b-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b90b-164">Namespace</span></span><br/>                | <span data-ttu-id="8b90b-165">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="8b90b-165">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="8b90b-166">MOF</span><span class="sxs-lookup"><span data-stu-id="8b90b-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b90b-167"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8b90b-167"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b90b-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b90b-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b90b-169">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="8b90b-169">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
