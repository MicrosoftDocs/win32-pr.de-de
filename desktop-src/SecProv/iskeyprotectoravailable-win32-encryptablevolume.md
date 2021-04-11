---
description: Gibt an, ob Schutzvorrichtungen für das Volume verfügbar sind.
ms.assetid: 92a959ea-27ec-4d38-a955-846bfd7b3a60
title: Iskeyprotectoravailable-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsKeyProtectorAvailable
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a80f731bf77a39d1e16c7dfe9cca4884b80eec49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214512"
---
# <a name="iskeyprotectoravailable-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="11a73-103">Iskeyprotectoravailable-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="11a73-103">IsKeyProtectorAvailable method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="11a73-104">Die **iskeyprotectoravailable** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt an, ob Schutzvorrichtungen für das Volume verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="11a73-104">The **IsKeyProtectorAvailable** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether protectors are available for the volume.</span></span>

<span data-ttu-id="11a73-105">Wenn ein schutzschutztyp bereitgestellt wird, gibt die Methode an, ob Schutzvorrichtungen des angegebenen Typs für das Volume verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="11a73-105">If a protector type is provided, then the method indicates whether protectors of the specified type are available for the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="11a73-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="11a73-106">Syntax</span></span>


```mof
uint32 IsKeyProtectorAvailable(
  [in, optional] uint32  KeyProtectorType,
  [out]          boolean IsKeyProtectorAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="11a73-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="11a73-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11a73-108">*Keyprotector Type* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="11a73-108">*KeyProtectorType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="11a73-109">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11a73-109">Type: **uint32**</span></span>

<span data-ttu-id="11a73-110">Eine ganze Zahl ohne Vorzeichen, die den Typ der abgefragten volumeschlüsselschutzvorrichtung angibt.</span><span class="sxs-lookup"><span data-stu-id="11a73-110">An unsigned integer that indicates the type of volume key protector queried.</span></span>

<span data-ttu-id="11a73-111">Wenn dieser Parameter nicht angegeben wird, werden alle verfügbaren Schlüssel Schutzvorrichtungen des Volumes abgefragt.</span><span class="sxs-lookup"><span data-stu-id="11a73-111">If this parameter is not specified, all available key protectors of the volume are queried.</span></span>



| <span data-ttu-id="11a73-112">Wert</span><span class="sxs-lookup"><span data-stu-id="11a73-112">Value</span></span>                                                                         | <span data-ttu-id="11a73-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="11a73-113">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="11a73-114"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="11a73-114"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="11a73-115">Alle Typen.</span><span class="sxs-lookup"><span data-stu-id="11a73-115">All types.</span></span><br/> <span data-ttu-id="11a73-116">Alle Schlüssel Schutzvorrichtungen werden abgefragt.</span><span class="sxs-lookup"><span data-stu-id="11a73-116">All key protectors are queried.</span></span><br/> |
| <dl> <span data-ttu-id="11a73-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="11a73-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="11a73-118">Trusted Platform Module (TPM).</span><span class="sxs-lookup"><span data-stu-id="11a73-118">Trusted Platform Module (TPM).</span></span><br/>                        |
| <dl> <span data-ttu-id="11a73-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="11a73-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="11a73-120">Externer Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="11a73-120">External key.</span></span><br/>                                         |
| <dl> <span data-ttu-id="11a73-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="11a73-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="11a73-122">Numerisches Kennwort.</span><span class="sxs-lookup"><span data-stu-id="11a73-122">Numerical password.</span></span><br/>                                   |
| <dl> <span data-ttu-id="11a73-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="11a73-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="11a73-124">TPM und PIN.</span><span class="sxs-lookup"><span data-stu-id="11a73-124">TPM And PIN.</span></span><br/>                                          |
| <dl> <span data-ttu-id="11a73-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="11a73-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="11a73-126">TPM-und Systemstart Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="11a73-126">TPM And Startup Key.</span></span><br/>                                  |
| <dl> <span data-ttu-id="11a73-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="11a73-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="11a73-128">TPM-und PIN-und Systemstart Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="11a73-128">TPM And PIN And Startup Key.</span></span><br/>                          |
| <dl> <span data-ttu-id="11a73-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="11a73-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="11a73-130">Öffentlicher Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="11a73-130">Public Key.</span></span><br/>                                           |
| <dl> <span data-ttu-id="11a73-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="11a73-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="11a73-132">Passphrase.</span><span class="sxs-lookup"><span data-stu-id="11a73-132">Passphrase.</span></span><br/>                                           |
| <dl> <span data-ttu-id="11a73-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="11a73-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="11a73-134">TPM-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="11a73-134">TPM Certificate</span></span><br/>                                       |
| <dl> <span data-ttu-id="11a73-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="11a73-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="11a73-136">Sicherheits-ID (SID)</span><span class="sxs-lookup"><span data-stu-id="11a73-136">Security Identifier (SID)</span></span><br/>                             |



 

</dd> <dt>

<span data-ttu-id="11a73-137">*Iskeyprotector available* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="11a73-137">*IsKeyProtectorAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11a73-138">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="11a73-138">Type: **boolean**</span></span>

<span data-ttu-id="11a73-139">Ein boolescher Wert, der angibt, ob eine volumeschlüsselschutzvorrichtung des angegebenen Typs auf dem Volume vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="11a73-139">A Boolean value that indicates whether a volume key protector of the specified type exists on the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11a73-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11a73-140">Return value</span></span>

<span data-ttu-id="11a73-141">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11a73-141">Type: **uint32**</span></span>

<span data-ttu-id="11a73-142">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="11a73-142">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="11a73-143">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="11a73-143">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="11a73-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11a73-144">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11a73-145"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="11a73-145"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                         | <span data-ttu-id="11a73-146">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="11a73-146">The method was successful.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="11a73-147"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="11a73-147"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl> | <span data-ttu-id="11a73-148">Der *keyprotectortype* -Parameter wird angegeben, verweist jedoch nicht auf einen gültigen schlüsselschutzschutztyp.</span><span class="sxs-lookup"><span data-stu-id="11a73-148">The *KeyProtectorType* parameter is specified but does not refer to a valid key protector type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="11a73-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11a73-149">Remarks</span></span>

<span data-ttu-id="11a73-150">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="11a73-150">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="11a73-151">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="11a73-151">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="11a73-152">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="11a73-152">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="11a73-153">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="11a73-153">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11a73-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11a73-154">Requirements</span></span>



| <span data-ttu-id="11a73-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11a73-155">Requirement</span></span> | <span data-ttu-id="11a73-156">Wert</span><span class="sxs-lookup"><span data-stu-id="11a73-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11a73-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11a73-157">Minimum supported client</span></span><br/> | <span data-ttu-id="11a73-158">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11a73-158">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="11a73-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11a73-159">Minimum supported server</span></span><br/> | <span data-ttu-id="11a73-160">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11a73-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="11a73-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="11a73-161">Namespace</span></span><br/>                | <span data-ttu-id="11a73-162">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="11a73-162">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="11a73-163">MOF</span><span class="sxs-lookup"><span data-stu-id="11a73-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11a73-164"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="11a73-164"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11a73-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11a73-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11a73-166">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="11a73-166">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
