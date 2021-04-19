---
description: Verwendet einen bereitgestellten externen Schlüssel für den Zugriff auf den Inhalt eines Datenvolumens.
ms.assetid: e383767e-8557-469c-bc44-f67591c46f23
title: Unlockwithexternalkey-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 4b599f098856937ae5610156cba96a1deea1f64b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363363"
---
# <a name="unlockwithexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="03922-103">Unlockwithexternalkey-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="03922-103">UnlockWithExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="03922-104">Die **unlockwithexternalkey** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " verwendet einen bereitgestellten externen Schlüssel für den Zugriff auf den Inhalt eines Datenvolumens.</span><span class="sxs-lookup"><span data-stu-id="03922-104">The **UnlockWithExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses a provided external key to access the contents of a data volume.</span></span>

<span data-ttu-id="03922-105">Der Verschlüsselungsschlüssel des Volumes muss mit einer oder mehreren Schlüssel Schutzvorrichtungen des Typs "externer Schlüssel" gesichert werden, indem die [**protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md) -Methode verwendet wird, um das Volume mit dieser Methode entsperren zu können.</span><span class="sxs-lookup"><span data-stu-id="03922-105">The volume's encryption key must have been secured with one or more key protectors of the type "External Key" using the [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to be able to unlock the volume with this method.</span></span>

> [!Note]  
> <span data-ttu-id="03922-106">Wenn die Festplatte Hardware Verschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "entsperrt" fest.</span><span class="sxs-lookup"><span data-stu-id="03922-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="03922-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="03922-107">Syntax</span></span>


```mof
uint32 UnlockWithExternalKey(
  [in] uint8 ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="03922-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="03922-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03922-109">*ExternalKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03922-109">*ExternalKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03922-110">Typ: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="03922-110">Type: **uint8\[\]**</span></span>

<span data-ttu-id="03922-111">Ein Bytearray, das den externen 256-Bit-Schlüssel angibt, mit dem das Volume entsperrt wird.</span><span class="sxs-lookup"><span data-stu-id="03922-111">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span> <span data-ttu-id="03922-112">Dieser Schlüssel kann durch Aufrufen der [**getexternalkeyfromfile**](getexternalkeyfromfile-win32-encryptablevolume.md) -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="03922-112">This key can be obtained by calling the [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03922-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03922-113">Return value</span></span>

<span data-ttu-id="03922-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03922-114">Type: **uint32**</span></span>

<span data-ttu-id="03922-115">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="03922-115">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="03922-116">Wenn das Volume bereits entsperrt ist, gibt diese Methode 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="03922-116">If the volume is already unlocked, this method returns 0.</span></span>



| <span data-ttu-id="03922-117">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="03922-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="03922-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03922-118">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="03922-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="03922-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="03922-120">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="03922-120">The method was successful.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="03922-121"><dt>**Fehler \_ Es \_**</dt> wurde <dt>kein Wert gefunden (0x)</dt> .</span><span class="sxs-lookup"><span data-stu-id="03922-121"><dt>**ERROR\_NOT\_FOUND**</dt> <dt>No value given (0x)</dt></span></span> </dl>          | <span data-ttu-id="03922-122">Das Volume weist keine Schlüssel Schutzvorrichtung vom Typ "externer Schlüssel" auf.</span><span class="sxs-lookup"><span data-stu-id="03922-122">The volume does not have a key protector of the type "External Key".</span></span><br/>                                                             |
| <dl> <span data-ttu-id="03922-123"><dt>**Fehler \_ Ungültiges \_ Kennwort**</dt> <dt>kein Wert angegeben (0x)</dt></span><span class="sxs-lookup"><span data-stu-id="03922-123"><dt>**ERROR\_INVALID\_PASSWORD**</dt> <dt>No value given (0x)</dt></span></span> </dl>   | <span data-ttu-id="03922-124">Mindestens eine Schlüssel Schutzvorrichtung des Typs "externer Schlüssel" ist vorhanden, aber der angegebene *ExternalKey* -Parameter kann das Volume nicht entsperren.</span><span class="sxs-lookup"><span data-stu-id="03922-124">One or more key protectors of the type "External Key" exist, but the specified *ExternalKey* parameter cannot unlock the volume.</span></span><br/> |
| <dl> <span data-ttu-id="03922-125"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="03922-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="03922-126">Der *ExternalKey* -Parameter ist kein Array der Größe 4.</span><span class="sxs-lookup"><span data-stu-id="03922-126">The *ExternalKey* parameter is not an array of size 4.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="03922-127"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="03922-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="03922-128">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="03922-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="03922-129">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="03922-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="03922-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03922-130">Remarks</span></span>

<span data-ttu-id="03922-131">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="03922-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="03922-132">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="03922-132">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="03922-133">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="03922-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="03922-134">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="03922-134">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03922-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03922-135">Requirements</span></span>



| <span data-ttu-id="03922-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03922-136">Requirement</span></span> | <span data-ttu-id="03922-137">Wert</span><span class="sxs-lookup"><span data-stu-id="03922-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03922-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03922-138">Minimum supported client</span></span><br/> | <span data-ttu-id="03922-139">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03922-139">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="03922-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03922-140">Minimum supported server</span></span><br/> | <span data-ttu-id="03922-141">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03922-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="03922-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="03922-142">Namespace</span></span><br/>                | <span data-ttu-id="03922-143">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="03922-143">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="03922-144">MOF</span><span class="sxs-lookup"><span data-stu-id="03922-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03922-145"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="03922-145"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03922-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03922-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03922-147">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="03922-147">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
