---
description: Ändert die PIN, die einem verschlüsselten Volume zugeordnet ist.
ms.assetid: 8b0043cc-cf86-44e5-ab7c-038a6782f347
title: Changepin-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 385f8cc66eb08bc020cc126cec587eee57a14ca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525694"
---
# <a name="changepin-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c933a-103">Changepin-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="c933a-103">ChangePIN method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c933a-104">Die **changepin** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " ändert die PIN, die einem verschlüsselten Volume zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c933a-104">The **ChangePIN** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class changes the PIN associated with an encrypted volume.</span></span> <span data-ttu-id="c933a-105">Wenn die Gruppenrichtlinie "Erweiterte Pins für den Start zulassen" aktiviert ist, kann eine PIN zusätzlich zu den Zahlen Buchstaben, Symbole und Leerzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c933a-105">If the "Allow enhanced PINs for startup" group policy is enabled, a PIN can contain letters, symbols, and spaces in addition to numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="c933a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c933a-106">Syntax</span></span>


```mof
uint32 ChangePIN(
  [in] string VolumeKeyProtectorID,
  [in] string NewPIN
);
```



## <a name="parameters"></a><span data-ttu-id="c933a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c933a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c933a-108">*Volumekeyprotectorid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c933a-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c933a-109">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c933a-109">Type: **string**</span></span>

<span data-ttu-id="c933a-110">Der eindeutige Zeichen folgen Bezeichner, mit dem eine verschlüsselte volumeschlüsselschutzvorrichtung verwaltet wird</span><span class="sxs-lookup"><span data-stu-id="c933a-110">The unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="c933a-111">*Newpin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c933a-111">*NewPIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c933a-112">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c933a-112">Type: **string**</span></span>

<span data-ttu-id="c933a-113">Eine vom Benutzer angegebene persönliche Identifikations Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c933a-113">A user-specified personal identification string.</span></span> <span data-ttu-id="c933a-114">Diese Zeichenfolge muss aus einer Sequenz von 4 bis 20 Ziffern bestehen, oder, wenn die Gruppenrichtlinie "Erweiterte Pins für den Start zulassen" aktiviert ist, 4 bis 20 Buchstaben, Symbole, Leerzeichen oder Ziffern.</span><span class="sxs-lookup"><span data-stu-id="c933a-114">This string must consist of a sequence of 4 to 20 digits or, if the "Allow enhanced PINs for startup" group policy is enabled, 4 to 20 letters, symbols, spaces, or numbers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c933a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c933a-115">Return value</span></span>

<span data-ttu-id="c933a-116">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c933a-116">Type: **uint32**</span></span>

<span data-ttu-id="c933a-117">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="c933a-117">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c933a-118">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="c933a-118">Return code/value</span></span>                                                                                                                                                                                | <span data-ttu-id="c933a-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c933a-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c933a-120"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c933a-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                | <span data-ttu-id="c933a-121">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c933a-121">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="c933a-122"><dt>**F \_ E \_ Bootable \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="c933a-122"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>              | <span data-ttu-id="c933a-123">Auf diesem Computer wurde eine Start fähige CD/DVD gefunden.</span><span class="sxs-lookup"><span data-stu-id="c933a-123">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="c933a-124">Entfernen Sie die CD/DVD, und starten Sie den Computer neu.</span><span class="sxs-lookup"><span data-stu-id="c933a-124">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="c933a-125"><dt>**F \_ E \_ ungültige \_ Pin \_**</dt> -Zeichen <dt>2150695066 (0x8031009a)</dt></span><span class="sxs-lookup"><span data-stu-id="c933a-125"><dt>**FVE\_E\_INVALID\_PIN\_CHARS**</dt> <dt>2150695066 (0x8031009A)</dt></span></span> </dl>          | <span data-ttu-id="c933a-126">Der *newpin* -Parameter enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c933a-126">The *NewPIN* parameter contains characters that are not valid.</span></span> <span data-ttu-id="c933a-127">Wenn der Gruppenrichtlinie "Erweiterte Pins für den Start zulassen" deaktiviert ist, werden nur Ziffern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c933a-127">When the "Allow enhanced PINs for startup" Group Policy is disabled, only numbers are supported.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="c933a-128"><dt>**F \_ E \_ ungültiger \_ \_ schutzschutztyp**</dt> <dt>2150694970 (0x8031003a)</dt></span><span class="sxs-lookup"><span data-stu-id="c933a-128"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl>     | <span data-ttu-id="c933a-129">Der *volumekeyprotectorid-* Parameter verweist nicht auf eine Schlüssel Schutzvorrichtung des Typs "numerisches Kennwort" oder "externer Schlüssel".</span><span class="sxs-lookup"><span data-stu-id="c933a-129">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="c933a-130">Verwenden Sie entweder die [**protectkeywithnumericalpassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) -Methode oder die [**protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md) -Methode, um eine Schlüssel Schutzvorrichtung des entsprechenden Typs zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c933a-130">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |
| <dl> <span data-ttu-id="c933a-131"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="c933a-131"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>               | <span data-ttu-id="c933a-132">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="c933a-132">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="c933a-133"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="c933a-133"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>               | <span data-ttu-id="c933a-134">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c933a-134">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="c933a-135">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="c933a-135">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="c933a-136"><dt>**F \_ E \_ Richtlinie \_ ungültige \_ Pin- \_ Länge**</dt> <dt>2150695016 (0x80310068)</dt></span><span class="sxs-lookup"><span data-stu-id="c933a-136"><dt>**FVE\_E\_POLICY\_INVALID\_PIN\_LENGTH**</dt> <dt>2150695016 (0x80310068)</dt></span></span> </dl> | <span data-ttu-id="c933a-137">Der angegebene *newpin* -Parameter ist entweder länger als 20 Zeichen, kürzer als 4 Zeichen oder kürzer als die durch Gruppenrichtlinie angegebene Mindestlänge.</span><span class="sxs-lookup"><span data-stu-id="c933a-137">The *NewPIN* parameter supplied is either longer than 20 characters, shorter than 4 characters, or shorter than the minimum length specified by Group Policy.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="c933a-138"><dt>**F \_ E \_ Protector \_ nicht \_ gefunden**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="c933a-138"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>        | <span data-ttu-id="c933a-139">Die angegebene Schlüssel Schutzvorrichtung ist auf dem Volume nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c933a-139">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="c933a-140"><dt>**TSB \_ E- \_ Dienst wird \_ nicht \_ ausgeführt**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="c933a-140"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl>        | <span data-ttu-id="c933a-141">Auf diesem Computer wurde keine kompatible Trusted Platform Module (TPM) gefunden.</span><span class="sxs-lookup"><span data-stu-id="c933a-141">No compatible Trusted Platform Module (TPM) is found on this computer.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="c933a-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c933a-142">Remarks</span></span>

<span data-ttu-id="c933a-143">Die **changepin** -Methode erstellt eine neue TPM-und PIN-Schutzvorrichtung basierend auf den vorhandenen Schutz Informationen und der neu bereitgestellten PIN.</span><span class="sxs-lookup"><span data-stu-id="c933a-143">The **ChangePIN** method creates a new TPM and PIN protector based on the existing protector information and the newly provided PIN.</span></span> <span data-ttu-id="c933a-144">Die neue Schutzvorrichtung weist dieselbe GUID auf.</span><span class="sxs-lookup"><span data-stu-id="c933a-144">The new protector will have the same GUID.</span></span> <span data-ttu-id="c933a-145">Die **changepin** -Methode kann auch aufgerufen werden, um die PIN einer beliebigen Schlüssel Schutzvorrichtung zu ändern, die eine PIN verwendet, z. b. TPM und PIN oder TPM mit PIN und USB.</span><span class="sxs-lookup"><span data-stu-id="c933a-145">The **ChangePIN** method can also be called to change the PIN of any key protector that uses a PIN, for example, TPM and PIN or TPM with PIN and USB.</span></span>

<span data-ttu-id="c933a-146">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="c933a-146">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c933a-147">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="c933a-147">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c933a-148">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c933a-148">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c933a-149">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c933a-149">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c933a-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c933a-150">Requirements</span></span>



| <span data-ttu-id="c933a-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c933a-151">Requirement</span></span> | <span data-ttu-id="c933a-152">Wert</span><span class="sxs-lookup"><span data-stu-id="c933a-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c933a-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c933a-153">Minimum supported client</span></span><br/> | <span data-ttu-id="c933a-154">Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c933a-154">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c933a-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c933a-155">Minimum supported server</span></span><br/> | <span data-ttu-id="c933a-156">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c933a-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c933a-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="c933a-157">Namespace</span></span><br/>                | <span data-ttu-id="c933a-158">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="c933a-158">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c933a-159">MOF</span><span class="sxs-lookup"><span data-stu-id="c933a-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c933a-160"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c933a-160"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c933a-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c933a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c933a-162">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="c933a-162">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
