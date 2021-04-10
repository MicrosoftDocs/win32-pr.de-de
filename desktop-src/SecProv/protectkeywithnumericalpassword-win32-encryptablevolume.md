---
description: Sichert den Verschlüsselungsschlüssel des Volumes mit einem speziell formatierten 48-stelligen Kennwort.
ms.assetid: 23e0b79a-2feb-441a-9785-7ecd3bb4b6c6
title: Protectkeywithnumericalpassword-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: fd17727bc71dbbe517b6424135e1205035027a00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866952"
---
# <a name="protectkeywithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="19bdc-103">Protectkeywithnumericalpassword-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="19bdc-103">ProtectKeyWithNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="19bdc-104">Die **protectkeywithnumericalpassword** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " sichert den Verschlüsselungsschlüssel des Volumes mit einem speziell formatierten 48-stelligen Kennwort.</span><span class="sxs-lookup"><span data-stu-id="19bdc-104">The **ProtectKeyWithNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key with a specially formatted 48-digit password.</span></span> <span data-ttu-id="19bdc-105">Dieses numerische Kennwort kann für die Wiederherstellung nach Authentifizierungs Fehlern anderer Schlüsselschutz Vorrichtungen (z. b. TPM) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19bdc-105">This numerical password can be used to recover from the authentication failures of other key protectors (for example, TPM).</span></span>

<span data-ttu-id="19bdc-106">Für das Volume wird eine Schlüssel Schutzvorrichtung vom Typ "numerisches Kennwort" erstellt.</span><span class="sxs-lookup"><span data-stu-id="19bdc-106">A key protector of type "Numerical Password" is created for the volume.</span></span>

<span data-ttu-id="19bdc-107">Verwenden Sie die [**isnumericalpasswordvalid-**](isnumericalpasswordvalid-win32-encryptablevolume.md) Methode, um das Format des numerischen Kennworts zu validieren.</span><span class="sxs-lookup"><span data-stu-id="19bdc-107">Use the [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md) method to validate the format of the numerical password.</span></span>

## <a name="syntax"></a><span data-ttu-id="19bdc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="19bdc-108">Syntax</span></span>


```mof
uint32 ProtectKeyWithNumericalPassword(
  [in, optional] string FriendlyName,
  [in, optional] string NumericalPassword,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="19bdc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="19bdc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19bdc-110">*FriendlyName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="19bdc-110">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19bdc-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="19bdc-111">Type: **string**</span></span>

<span data-ttu-id="19bdc-112">Eine Zeichenfolge, die einen vom Benutzer zugewiesenen Bezeichner für diese Schlüssel Schutzvorrichtung angibt.</span><span class="sxs-lookup"><span data-stu-id="19bdc-112">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="19bdc-113">Wenn dieser Parameter nicht angegeben wird, wird ein leerer Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="19bdc-113">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="19bdc-114">*Numericalpassword* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="19bdc-114">*NumericalPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19bdc-115">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="19bdc-115">Type: **string**</span></span>

<span data-ttu-id="19bdc-116">Eine Zeichenfolge, die das speziell formatierte numerische Kennwort mit 48-Ziffern angibt.</span><span class="sxs-lookup"><span data-stu-id="19bdc-116">A string that specifies the specially formatted 48-digit numerical password.</span></span>

<span data-ttu-id="19bdc-117">Das numerische Kennwort muss 48 Ziffern enthalten.</span><span class="sxs-lookup"><span data-stu-id="19bdc-117">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="19bdc-118">Diese Ziffern können in 8 Gruppen mit 6 Ziffern aufgeteilt werden, wobei die letzte Ziffer in jeder Gruppe einen Prüfsummen Wert für die Gruppe angibt.</span><span class="sxs-lookup"><span data-stu-id="19bdc-118">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="19bdc-119">Jede Gruppe von 6 Ziffern muss von 11 teilbar sein und muss kleiner als 720896 sein.</span><span class="sxs-lookup"><span data-stu-id="19bdc-119">Each group of 6 digits must be divisible by 11 and must be less than 720896.</span></span> <span data-ttu-id="19bdc-120">Wenn eine Gruppe von sechs Ziffern als x1, x2, X3, X4, x5 und x6 bezeichnet wird, wird die Ziffer "Prüfsumme x6" als "– x1 + x2 – X3 + X4 – x5 mod 11" berechnet.</span><span class="sxs-lookup"><span data-stu-id="19bdc-120">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="19bdc-121">Die Gruppen von Ziffern können optional durch ein Leerzeichen oder einen Bindestrich getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="19bdc-121">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="19bdc-122">"Xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" oder "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" kann daher auch gültige numerische Kenn Wörter enthalten.</span><span class="sxs-lookup"><span data-stu-id="19bdc-122">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

<span data-ttu-id="19bdc-123">Wenn kein numerisches Kennwort angegeben wird, wird eine nach dem Zufallsprinzip generiert.</span><span class="sxs-lookup"><span data-stu-id="19bdc-123">If no numerical password is specified, one is randomly generated.</span></span> <span data-ttu-id="19bdc-124">Verwenden Sie die [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) -Methode, um das zufällig generierte Kennwort abzurufen.</span><span class="sxs-lookup"><span data-stu-id="19bdc-124">Use the [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) method to obtain the randomly generated password.</span></span>

</dd> <dt>

<span data-ttu-id="19bdc-125">*Volumekeyprotectorid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="19bdc-125">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19bdc-126">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="19bdc-126">Type: **string**</span></span>

<span data-ttu-id="19bdc-127">Eine Zeichenfolge, die der eindeutige Bezeichner ist, der der erstellten Schutzvorrichtung zugeordnet ist und der zum Verwalten der Schlüssel Schutzvorrichtung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="19bdc-127">A string that is the unique identifier associated with the created protector and that can be used to manage the key protector.</span></span>

<span data-ttu-id="19bdc-128">Wenn das Laufwerk die Hardware Verschlüsselung unterstützt und BitLocker keinen bandbesitz hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüssel Schutzvorrichtung wird in die pro-Band-Metadaten geschrieben.</span><span class="sxs-lookup"><span data-stu-id="19bdc-128">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19bdc-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19bdc-129">Return value</span></span>

<span data-ttu-id="19bdc-130">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="19bdc-130">Type: **uint32**</span></span>

<span data-ttu-id="19bdc-131">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="19bdc-131">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="19bdc-132">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="19bdc-132">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="19bdc-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19bdc-133">Description</span></span>                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="19bdc-134"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="19bdc-134"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="19bdc-135">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="19bdc-135">The method was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="19bdc-136"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="19bdc-136"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="19bdc-137">Der *numericalpassword* -Parameter weist kein gültiges Format auf.</span><span class="sxs-lookup"><span data-stu-id="19bdc-137">The *NumericalPassword* parameter does not have a valid format.</span></span><br/> |
| <dl> <span data-ttu-id="19bdc-138"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="19bdc-138"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="19bdc-139">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="19bdc-139">The volume is locked.</span></span><br/>                                           |
| <dl> <span data-ttu-id="19bdc-140"><dt>**F \_ E \_ Ungültiges Kenn \_ Wort \_ Format**</dt> <dt>2150694965 (0x80310035)</dt></span><span class="sxs-lookup"><span data-stu-id="19bdc-140"><dt>**FVE\_E\_INVALID\_PASSWORD\_FORMAT**</dt> <dt>2150694965 (0x80310035)</dt></span></span> </dl> | <span data-ttu-id="19bdc-141">Der *numericalpassword* -Parameter weist kein gültiges Format auf.</span><span class="sxs-lookup"><span data-stu-id="19bdc-141">The *NumericalPassword* parameter does not have a valid format.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="19bdc-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19bdc-142">Remarks</span></span>

<span data-ttu-id="19bdc-143">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="19bdc-143">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="19bdc-144">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="19bdc-144">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="19bdc-145">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="19bdc-145">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="19bdc-146">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="19bdc-146">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19bdc-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19bdc-147">Requirements</span></span>



| <span data-ttu-id="19bdc-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19bdc-148">Requirement</span></span> | <span data-ttu-id="19bdc-149">Wert</span><span class="sxs-lookup"><span data-stu-id="19bdc-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19bdc-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19bdc-150">Minimum supported client</span></span><br/> | <span data-ttu-id="19bdc-151">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19bdc-151">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="19bdc-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19bdc-152">Minimum supported server</span></span><br/> | <span data-ttu-id="19bdc-153">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19bdc-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="19bdc-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="19bdc-154">Namespace</span></span><br/>                | <span data-ttu-id="19bdc-155">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="19bdc-155">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="19bdc-156">MOF</span><span class="sxs-lookup"><span data-stu-id="19bdc-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19bdc-157"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="19bdc-157"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19bdc-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19bdc-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19bdc-159">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="19bdc-159">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
