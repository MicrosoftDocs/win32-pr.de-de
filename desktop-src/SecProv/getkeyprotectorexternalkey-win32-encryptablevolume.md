---
description: Ruft den externen Schlüssel für eine angegebene Schlüssel Schutzvorrichtung ab.
ms.assetid: d2b5e7d4-97c1-4d7f-a155-b5cdca2b552e
title: Getkeyprotectorexternalkey-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7125038a9e93803f7f8773ce5da078983a5a544c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214515"
---
# <a name="getkeyprotectorexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="7a60f-103">Getkeyprotectorexternalkey-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="7a60f-103">GetKeyProtectorExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="7a60f-104">Die **getkeyprotectorexternalkey** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " Ruft den externen Schlüssel für eine bestimmte Schlüssel Schutzvorrichtung des entsprechenden Typs ab.</span><span class="sxs-lookup"><span data-stu-id="7a60f-104">The **GetKeyProtectorExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the external key for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="7a60f-105">Der Bezeichner für die Schlüssel Schutzvorrichtung muss auf eine Schlüssel Schutzvorrichtung vom Typ "externer Schlüssel", "TPM und PIN und Systemstart Schlüssel" oder "TPM und Systemstart Schlüssel" verweisen.</span><span class="sxs-lookup"><span data-stu-id="7a60f-105">The key protector identifier must refer to a key protector of type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="7a60f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a60f-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorExternalKey(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="7a60f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a60f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a60f-108">*Volumekeyprotectorid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a60f-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a60f-109">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7a60f-109">Type: **string**</span></span>

<span data-ttu-id="7a60f-110">Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="7a60f-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="7a60f-111">*ExternalKey* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7a60f-111">*ExternalKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a60f-112">Typ: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="7a60f-112">Type: **uint8\[\]**</span></span>

<span data-ttu-id="7a60f-113">Ein Bytearray, das den externen 256-Bit-Schlüssel angibt, mit dem das entsprechende Volume entsperrt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7a60f-113">An array of bytes that specifies the 256-bit external key that can be used to unlock the corresponding volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a60f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a60f-114">Return value</span></span>

<span data-ttu-id="7a60f-115">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7a60f-115">Type: **uint32**</span></span>

<span data-ttu-id="7a60f-116">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="7a60f-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="7a60f-117">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="7a60f-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="7a60f-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a60f-118">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a60f-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7a60f-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="7a60f-120">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7a60f-120">The method was successful.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="7a60f-121"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="7a60f-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="7a60f-122">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="7a60f-122">The volume is locked.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="7a60f-123"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="7a60f-123"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="7a60f-124">Der *volumekeyprotectorid-* Parameter verweist nicht auf eine Schlüssel Schutzvorrichtung vom Typ "externer Schlüssel", "TPM und PIN und Systemstart Schlüssel" oder "TPM und Systemstart Schlüssel".</span><span class="sxs-lookup"><span data-stu-id="7a60f-124">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="7a60f-125"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="7a60f-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="7a60f-126">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7a60f-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="7a60f-127">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="7a60f-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="7a60f-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a60f-128">Remarks</span></span>

<span data-ttu-id="7a60f-129">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="7a60f-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7a60f-130">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="7a60f-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7a60f-131">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7a60f-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7a60f-132">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7a60f-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a60f-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a60f-133">Requirements</span></span>



| <span data-ttu-id="7a60f-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a60f-134">Requirement</span></span> | <span data-ttu-id="7a60f-135">Wert</span><span class="sxs-lookup"><span data-stu-id="7a60f-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a60f-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a60f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7a60f-137">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a60f-137">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7a60f-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a60f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7a60f-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a60f-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7a60f-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a60f-140">Namespace</span></span><br/>                | <span data-ttu-id="7a60f-141">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="7a60f-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="7a60f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="7a60f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a60f-143"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7a60f-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a60f-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a60f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a60f-145">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="7a60f-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
