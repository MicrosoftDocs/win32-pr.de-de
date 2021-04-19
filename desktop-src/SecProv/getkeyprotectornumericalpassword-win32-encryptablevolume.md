---
description: Ruft das numerische Kennwort für eine angegebene Schlüssel Schutzvorrichtung ab.
ms.assetid: 5c4663fb-285d-471c-b355-82d553a7e686
title: GetKeyProtectorNumericalPassword-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 73a6c774386cd88195074092323969d97f4d7563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346293"
---
# <a name="getkeyprotectornumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="485e9-103">GetKeyProtectorNumericalPassword-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="485e9-103">GetKeyProtectorNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="485e9-104">Die **GetKeyProtectorNumericalPassword** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " Ruft das numerische Kennwort für eine bestimmte Schlüssel Schutzvorrichtung des entsprechenden Typs ab.</span><span class="sxs-lookup"><span data-stu-id="485e9-104">The **GetKeyProtectorNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the numerical password for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="485e9-105">Die schlüsselschutzschutzkennung muss auf eine Schlüssel Schutzvorrichtung vom Typ "numerisches Kennwort" verweisen.</span><span class="sxs-lookup"><span data-stu-id="485e9-105">The key protector identifier must refer to a key protector of type "Numerical Password".</span></span>

## <a name="syntax"></a><span data-ttu-id="485e9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="485e9-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorNumericalPassword(
  [in]  string VolumeKeyProtectorID,
  [out] string NumericalPassword
);
```



## <a name="parameters"></a><span data-ttu-id="485e9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="485e9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="485e9-108">*Volumekeyprotectorid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="485e9-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="485e9-109">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="485e9-109">Type: **string**</span></span>

<span data-ttu-id="485e9-110">Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="485e9-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="485e9-111">*Numericalpassword* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="485e9-111">*NumericalPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="485e9-112">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="485e9-112">Type: **string**</span></span>

<span data-ttu-id="485e9-113">Eine Zeichenfolge, die das Kennwort darstellt, das zum Entsperren des entsprechenden Volumes verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="485e9-113">A string that represents the password that can be used to unlock the corresponding volume.</span></span>

<span data-ttu-id="485e9-114">Das numerische Kennwort ist 48 Ziffern.</span><span class="sxs-lookup"><span data-stu-id="485e9-114">The numerical password is 48 digits.</span></span> <span data-ttu-id="485e9-115">Diese Ziffern sind in acht Gruppen von 6 Ziffern unterteilt, wobei die letzte Ziffer in jeder Gruppe einen Prüfsummen Wert für die Gruppe angibt.</span><span class="sxs-lookup"><span data-stu-id="485e9-115">These digits are divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="485e9-116">Wenn eine Gruppe von sechs Ziffern als x1, x2, X3, X4, x5 und x6 gekennzeichnet ist, wird die Ziffer "Prüfsumme x6" als "– x1 + x2 – X3 + X4 – x5 mod 11" berechnet.</span><span class="sxs-lookup"><span data-stu-id="485e9-116">Assuming that a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="485e9-117">Die Gruppen von Ziffern sind durch einen Bindestrich getrennt.</span><span class="sxs-lookup"><span data-stu-id="485e9-117">The groups of digits are separated by a hyphen.</span></span> <span data-ttu-id="485e9-118">Daher ist "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" das Format des zurückgegebenen Kennworts.</span><span class="sxs-lookup"><span data-stu-id="485e9-118">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" is the format of the returned password.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="485e9-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="485e9-119">Return value</span></span>

<span data-ttu-id="485e9-120">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="485e9-120">Type: **uint32**</span></span>

<span data-ttu-id="485e9-121">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="485e9-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="485e9-122">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="485e9-122">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="485e9-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="485e9-123">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="485e9-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="485e9-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="485e9-125">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="485e9-125">The method was successful.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="485e9-126"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="485e9-126"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="485e9-127">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="485e9-127">The volume is locked.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="485e9-128"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="485e9-128"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="485e9-129">Der *volumekeyprotectorid-* Parameter verweist nicht auf eine Schlüssel Schutzvorrichtung des Typs "numerisches Kennwort".</span><span class="sxs-lookup"><span data-stu-id="485e9-129">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password".</span></span><br/> |
| <dl> <span data-ttu-id="485e9-130"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="485e9-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="485e9-131">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="485e9-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="485e9-132">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="485e9-132">Add a key protector to enable BitLocker.</span></span> <br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="485e9-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="485e9-133">Remarks</span></span>

<span data-ttu-id="485e9-134">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="485e9-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="485e9-135">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="485e9-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="485e9-136">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="485e9-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="485e9-137">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="485e9-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="485e9-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="485e9-138">Requirements</span></span>



| <span data-ttu-id="485e9-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="485e9-139">Requirement</span></span> | <span data-ttu-id="485e9-140">Wert</span><span class="sxs-lookup"><span data-stu-id="485e9-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="485e9-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="485e9-141">Minimum supported client</span></span><br/> | <span data-ttu-id="485e9-142">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="485e9-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="485e9-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="485e9-143">Minimum supported server</span></span><br/> | <span data-ttu-id="485e9-144">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="485e9-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="485e9-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="485e9-145">Namespace</span></span><br/>                | <span data-ttu-id="485e9-146">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="485e9-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="485e9-147">MOF</span><span class="sxs-lookup"><span data-stu-id="485e9-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="485e9-148"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="485e9-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="485e9-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="485e9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="485e9-150">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="485e9-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
