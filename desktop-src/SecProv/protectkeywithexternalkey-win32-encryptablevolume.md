---
description: Sichert den Verschlüsselungsschlüssel des Volumes mit einem externen 256-Bit-Schlüssel.
ms.assetid: 768cef38-a00f-4faa-bbe3-9d4a19be2f6d
title: Protectkeywithexternalkey-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: adcbdfdb9ea55139626bf3d1657b2e154c8d2b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348974"
---
# <a name="protectkeywithexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="90b29-103">Protectkeywithexternalkey-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="90b29-103">ProtectKeyWithExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="90b29-104">Die **protectkeywithexternalkey** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " sichert den Verschlüsselungsschlüssel des Volumes mit einem externen 256-Bit-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="90b29-104">The **ProtectKeyWithExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key with a 256-bit external key.</span></span> <span data-ttu-id="90b29-105">Dieser externe Schlüssel kann zur Wiederherstellung nach Authentifizierungs Fehlern anderer Schlüsselschutz Vorrichtungen (z. b. TPM) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90b29-105">This external key can be used to recover from the authentication failures of other key protectors (for example, TPM).</span></span>

<span data-ttu-id="90b29-106">Verwenden Sie die [**saveexternalkeytofile**](saveexternalkeytofile-win32-encryptablevolume.md) -Methode, um diesen externen Schlüssel in einer Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="90b29-106">Use the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method to save this external key to a file.</span></span> <span data-ttu-id="90b29-107">USB-Speichergeräte, die diesen externen Schlüssel enthalten, können beim Starten des Computers als Systemstart Schlüssel oder Wiederherstellungs Schlüssel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90b29-107">USB memory devices that contain this external key can be used as a startup key or a recovery key when the computer starts.</span></span>

<span data-ttu-id="90b29-108">Für das Volume wird eine Schlüssel Schutzvorrichtung vom Typ "externer Schlüssel" erstellt.</span><span class="sxs-lookup"><span data-stu-id="90b29-108">A key protector of type "External Key" is created for the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="90b29-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="90b29-109">Syntax</span></span>


```mof
uint32 ProtectKeyWithExternalKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="90b29-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="90b29-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90b29-111">*FriendlyName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="90b29-111">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="90b29-112">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90b29-112">Type: **string**</span></span>

<span data-ttu-id="90b29-113">Eine Zeichenfolge, die einen vom Benutzer zugewiesenen Bezeichner für diese Schlüssel Schutzvorrichtung angibt.</span><span class="sxs-lookup"><span data-stu-id="90b29-113">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="90b29-114">Wenn dieser Parameter nicht angegeben wird, wird ein leerer Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="90b29-114">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="90b29-115">*ExternalKey* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="90b29-115">*ExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="90b29-116">Typ: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="90b29-116">Type: **uint8\[\]**</span></span>

<span data-ttu-id="90b29-117">Ein Bytearray, das den externen 256-Bit-Schlüssel angibt, mit dem das Volume entsperrt wird.</span><span class="sxs-lookup"><span data-stu-id="90b29-117">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span>

<span data-ttu-id="90b29-118">Wenn kein externer Schlüssel angegeben ist, wird eine nach dem Zufallsprinzip generiert.</span><span class="sxs-lookup"><span data-stu-id="90b29-118">If no external key is specified, one is randomly generated.</span></span> <span data-ttu-id="90b29-119">Verwenden Sie die [**getkeyprotectorexternalkey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) -Methode, um den zufällig generierten Schlüssel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="90b29-119">Use the [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) method to obtain the randomly generated key.</span></span>

</dd> <dt>

<span data-ttu-id="90b29-120">*Volumekeyprotectorid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="90b29-120">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90b29-121">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90b29-121">Type: **string**</span></span>

<span data-ttu-id="90b29-122">Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="90b29-122">A unique string identifier used to manage an encrypted volume key protector.</span></span>

<span data-ttu-id="90b29-123">Wenn das Laufwerk die Hardware Verschlüsselung unterstützt und BitLocker keinen bandbesitz hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüssel Schutzvorrichtung wird in die pro-Band-Metadaten geschrieben.</span><span class="sxs-lookup"><span data-stu-id="90b29-123">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90b29-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90b29-124">Return value</span></span>

<span data-ttu-id="90b29-125">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="90b29-125">Type: **uint32**</span></span>

<span data-ttu-id="90b29-126">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="90b29-126">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="90b29-127">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="90b29-127">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="90b29-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90b29-128">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="90b29-129"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="90b29-129"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="90b29-130">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="90b29-130">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="90b29-131"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="90b29-131"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="90b29-132">Der *ExternalKey* -Parameter wird bereitgestellt, ist aber kein Array der Größe 4.</span><span class="sxs-lookup"><span data-stu-id="90b29-132">The *ExternalKey* parameter is provided but is not an array of size 4.</span></span><br/>            |
| <dl> <span data-ttu-id="90b29-133"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="90b29-133"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="90b29-134">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="90b29-134">The volume is locked.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="90b29-135"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="90b29-135"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="90b29-136">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="90b29-136">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="90b29-137">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="90b29-137">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="90b29-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90b29-138">Remarks</span></span>

<span data-ttu-id="90b29-139">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="90b29-139">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="90b29-140">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="90b29-140">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="90b29-141">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="90b29-141">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="90b29-142">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="90b29-142">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90b29-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90b29-143">Requirements</span></span>



| <span data-ttu-id="90b29-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90b29-144">Requirement</span></span> | <span data-ttu-id="90b29-145">Wert</span><span class="sxs-lookup"><span data-stu-id="90b29-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90b29-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90b29-146">Minimum supported client</span></span><br/> | <span data-ttu-id="90b29-147">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90b29-147">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="90b29-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90b29-148">Minimum supported server</span></span><br/> | <span data-ttu-id="90b29-149">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90b29-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="90b29-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="90b29-150">Namespace</span></span><br/>                | <span data-ttu-id="90b29-151">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="90b29-151">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="90b29-152">MOF</span><span class="sxs-lookup"><span data-stu-id="90b29-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90b29-153"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="90b29-153"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90b29-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90b29-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90b29-155">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="90b29-155">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
