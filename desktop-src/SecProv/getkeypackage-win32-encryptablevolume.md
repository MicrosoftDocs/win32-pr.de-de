---
description: Exportiert Informationen, die möglicherweise zum retten verschlüsselter Daten beitragen, wenn das Laufwerk stark beschädigt ist und keine Daten Sicherungsdateien vorhanden sind.
ms.assetid: 3d376a02-3392-433e-b842-24c73074610c
title: Getkeypackage-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyPackage
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d1b2348a90b6b3cd01685c740fdfa67ad5a2d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359439"
---
# <a name="getkeypackage-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="1c6e4-103">Getkeypackage-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="1c6e4-103">GetKeyPackage method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="1c6e4-104">Die **getkeypackage** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " exportiert Informationen, die möglicherweise dazu beitragen, verschlüsselte Daten zu retten, wenn das Laufwerk stark beschädigt ist und keine Daten Sicherungsdateien vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-104">The **GetKeyPackage** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class exports information that may help salvage encrypted data when the drive is severely damaged and no data backup files exist.</span></span>

<span data-ttu-id="1c6e4-105">Die exportierten Informationen bestehen aus dem Verschlüsselungsschlüssel des Volumes, der durch eine Schlüssel Schutzvorrichtung des Typs "numerisches Kennwort" oder "externer Schlüssel" gesichert ist.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-105">The exported information consists of the volume's encryption key secured by a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="1c6e4-106">Um dieses Paket verwenden zu können, müssen Sie auch das entsprechende numerische Kennwort oder den externen Schlüssel speichern.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-106">To make use of this package, you must also save the corresponding numerical password or external key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c6e4-107">Wenn Sie sich für das Exportieren eines Schlüssel Pakets entscheiden, stellen Sie sicher, dass diese Informationen an einem gut geschützten Speicherort aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-107">If you choose to export a key package, make certain to keep this information in a well-protected location.</span></span> <span data-ttu-id="1c6e4-108">Diese Informationen dürfen nicht auf Ihrem Computer enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-108">Do not carry this information with your computer.</span></span> <span data-ttu-id="1c6e4-109">Wenn das Schlüssel Paket verloren geht oder gestohlen wird, müssen Sie das Volume entschlüsseln und mit einem neuen Schlüssel erneut verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-109">If this key package is lost or stolen, you will need to decrypt the volume and reencrypt it by using a new key.</span></span>

 

<span data-ttu-id="1c6e4-110">Im Fall eines Laufwerks Fehlers ist das BitLocker-Reparatur Tool vorhanden, um die verfügbaren Daten zu retten.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-110">In the event of a drive failure, the BitLocker Repair Tool exists to help salvage available data.</span></span> <span data-ttu-id="1c6e4-111">Weitere Informationen zur Verwendung des Schlüssel Pakets durch dieses Tool finden [Sie unter Verwenden des BitLocker-Reparatur Tools zum Wiederherstellen von Daten von einem verschlüsselten Volume in Windows Vista](https://support.microsoft.com/kb/928201).</span><span class="sxs-lookup"><span data-stu-id="1c6e4-111">For more information about how this tool can use the key package, see [How to use the BitLocker Repair Tool to help recover data from an encrypted volume in Windows Vista](https://support.microsoft.com/kb/928201).</span></span>

## <a name="syntax"></a><span data-ttu-id="1c6e4-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c6e4-112">Syntax</span></span>


```mof
uint32 GetKeyPackage(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  KeyPackage[]
);
```



## <a name="parameters"></a><span data-ttu-id="1c6e4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c6e4-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c6e4-114">*Volumekeyprotectorid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c6e4-114">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c6e4-115">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c6e4-115">Type: **string**</span></span>

<span data-ttu-id="1c6e4-116">Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-116">A unique string identifier used to manage an encrypted volume key protector.</span></span> <span data-ttu-id="1c6e4-117">Zum Exportieren eines Schlüssel Pakets müssen Sie eine Schlüssel Schutzvorrichtung vom Typ "numerisch Password" oder "externer Schlüssel" verwenden.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-117">To export a key package, you must use a key protector of type "Numerical Password" or "External Key".</span></span>

</dd> <dt>

<span data-ttu-id="1c6e4-118">*KeyPackage \[ \]* \[out\]</span><span class="sxs-lookup"><span data-stu-id="1c6e4-118">*KeyPackage\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c6e4-119">Typ: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1c6e4-119">Type: **uint8**</span></span>

<span data-ttu-id="1c6e4-120">Ein Bytestream, der den Verschlüsselungsschlüssel für ein Volume enthält, gesichert durch die angegebene Schlüssel Schutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-120">A byte stream that contains the encryption key for a volume, secured by the specified key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c6e4-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c6e4-121">Return value</span></span>

<span data-ttu-id="1c6e4-122">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c6e4-122">Type: **uint32**</span></span>

<span data-ttu-id="1c6e4-123">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-123">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="1c6e4-124">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="1c6e4-124">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="1c6e4-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c6e4-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1c6e4-126"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1c6e4-126"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="1c6e4-127">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-127">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="1c6e4-128"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="1c6e4-128"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>           | <span data-ttu-id="1c6e4-129">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-129">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="1c6e4-130"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="1c6e4-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="1c6e4-131">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="1c6e4-132">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-132">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="1c6e4-133"><dt>**F \_ E \_ Protector \_ nicht \_ gefunden**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="1c6e4-133"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="1c6e4-134">Die angegebene Schlüssel Schutzvorrichtung ist auf dem Volume nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-134">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="1c6e4-135"><dt>**F \_ E \_ ungültiger \_ \_ schutzschutztyp**</dt> <dt>2150694970 (0x8031003a)</dt></span><span class="sxs-lookup"><span data-stu-id="1c6e4-135"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="1c6e4-136">Der *volumekeyprotectorid-* Parameter verweist nicht auf eine Schlüssel Schutzvorrichtung des Typs "numerisches Kennwort" oder "externer Schlüssel".</span><span class="sxs-lookup"><span data-stu-id="1c6e4-136">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="1c6e4-137">Verwenden Sie entweder die [**protectkeywithnumericalpassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) -Methode oder die [**protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md) -Methode, um eine Schlüssel Schutzvorrichtung des entsprechenden Typs zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-137">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1c6e4-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c6e4-138">Remarks</span></span>

<span data-ttu-id="1c6e4-139">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-139">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1c6e4-140">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-140">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1c6e4-141">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1c6e4-141">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1c6e4-142">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="1c6e4-142">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c6e4-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c6e4-143">Requirements</span></span>



| <span data-ttu-id="1c6e4-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c6e4-144">Requirement</span></span> | <span data-ttu-id="1c6e4-145">Wert</span><span class="sxs-lookup"><span data-stu-id="1c6e4-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c6e4-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c6e4-146">Minimum supported client</span></span><br/> | <span data-ttu-id="1c6e4-147">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c6e4-147">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1c6e4-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c6e4-148">Minimum supported server</span></span><br/> | <span data-ttu-id="1c6e4-149">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c6e4-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1c6e4-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c6e4-150">Namespace</span></span><br/>                | <span data-ttu-id="1c6e4-151">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="1c6e4-151">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="1c6e4-152">MOF</span><span class="sxs-lookup"><span data-stu-id="1c6e4-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c6e4-153"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1c6e4-153"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c6e4-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c6e4-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c6e4-155">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="1c6e4-155">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
