---
description: Ändert einen externen Schlüssel, der einem verschlüsselten Volume zugeordnet ist.
ms.assetid: 14c7e643-f685-40bb-be86-aabc5b883d7e
title: Changeexternalkey-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangeExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7441666ded1acc2234df84fc98ce6d02a117167d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362861"
---
# <a name="changeexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="e6324-103">Changeexternalkey-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="e6324-103">ChangeExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="e6324-104">Die **changeexternalkey** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " ändert einen externen Schlüssel, der einem verschlüsselten Volume zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e6324-104">The **ChangeExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class changes an external key that is associated with an encrypted volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6324-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6324-105">Syntax</span></span>


```mof
uint32 ChangeExternalKey(
  [in]           string VolumeKeyProtectorID,
  [in, optional] uint8   NewExternalKey[],
  [out]          string NewVolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="e6324-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6324-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6324-107">*Volumekeyprotectorid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6324-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6324-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6324-108">Type: **string**</span></span>

<span data-ttu-id="e6324-109">Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="e6324-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

 <span data-ttu-id="e6324-110">" *Netwexternalkey* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e6324-110">*NewExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e6324-111">Typ: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="e6324-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="e6324-112">Ein Bytearray, das den externen 256-Bit-Schlüssel angibt, mit dem das Volume entsperrt wird.</span><span class="sxs-lookup"><span data-stu-id="e6324-112">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span>

</dd> <dt>

<span data-ttu-id="e6324-113">*Newvolumekeyprotectorid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e6324-113">*NewVolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6324-114">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6324-114">Type: **string**</span></span>

<span data-ttu-id="e6324-115">Ein aktualisierter eindeutiger Zeichen folgen Bezeichner, der zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung verwendet wird</span><span class="sxs-lookup"><span data-stu-id="e6324-115">An updated unique string identifier that is used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6324-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6324-116">Return value</span></span>

<span data-ttu-id="e6324-117">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6324-117">Type: **uint32**</span></span>

<span data-ttu-id="e6324-118">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="e6324-118">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="e6324-119">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="e6324-119">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="e6324-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6324-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e6324-121"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="e6324-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="e6324-122">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e6324-122">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="e6324-123"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="e6324-123"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                    | <span data-ttu-id="e6324-124">Der Parameter " *netwexternalkey* " ist kein Array der Größe 32.</span><span class="sxs-lookup"><span data-stu-id="e6324-124">The *NewExternalKey* parameter is not an array of size 32.</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="e6324-125"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="e6324-125"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>           | <span data-ttu-id="e6324-126">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="e6324-126">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="e6324-127"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="e6324-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="e6324-128">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e6324-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="e6324-129">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="e6324-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="e6324-130"><dt>**F \_ E \_ Bootable \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="e6324-130"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>          | <span data-ttu-id="e6324-131">Auf diesem Computer wurde eine Start fähige CD/DVD gefunden.</span><span class="sxs-lookup"><span data-stu-id="e6324-131">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="e6324-132">Entfernen Sie die CD/DVD, und starten Sie den Computer neu.</span><span class="sxs-lookup"><span data-stu-id="e6324-132">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="e6324-133"><dt>**F \_ E \_ Protector \_ nicht \_ gefunden**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="e6324-133"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="e6324-134">Die angegebene Schlüssel Schutzvorrichtung ist auf dem Volume nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e6324-134">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="e6324-135"><dt>**F \_ E \_ ungültiger \_ \_ schutzschutztyp**</dt> <dt>2150694970 (0x8031003a)</dt></span><span class="sxs-lookup"><span data-stu-id="e6324-135"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="e6324-136">Der *volumekeyprotectorid-* Parameter verweist nicht auf eine Schlüssel Schutzvorrichtung des Typs "numerisches Kennwort" oder "externer Schlüssel".</span><span class="sxs-lookup"><span data-stu-id="e6324-136">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="e6324-137">Verwenden Sie entweder die [**protectkeywithnumericalpassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) -Methode oder die [**protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md) -Methode, um eine Schlüssel Schutzvorrichtung des entsprechenden Typs zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e6324-137">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e6324-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6324-138">Remarks</span></span>

<span data-ttu-id="e6324-139">Diese Methode kann verwendet werden, um den externen Schlüssel für jede Schlüssel Schutzvorrichtung zu ändern, die einen externen Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6324-139">This method can be used to change the external key for any key protector that uses an external key.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6324-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6324-140">Requirements</span></span>



| <span data-ttu-id="e6324-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6324-141">Requirement</span></span> | <span data-ttu-id="e6324-142">Wert</span><span class="sxs-lookup"><span data-stu-id="e6324-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6324-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6324-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e6324-144">Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6324-144">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e6324-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6324-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e6324-146">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6324-146">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e6324-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6324-147">Namespace</span></span><br/>                | <span data-ttu-id="e6324-148">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="e6324-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="e6324-149">MOF</span><span class="sxs-lookup"><span data-stu-id="e6324-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6324-150"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e6324-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6324-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6324-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6324-152">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="e6324-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




